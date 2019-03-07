---
title: Хранение, зависящее от возникновения события
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: В этой статье описывается, как настроить операции бизнес-процесса, чтобы автоматизировать хранение с помощью событий, используя REST API Microsoft 365.
ms.openlocfilehash: 55bfdccea07b6aaa9227974b43b1b20adcf97ff5
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455091"
---
# <a name="automate-event-based-retention"></a><span data-ttu-id="d9437-103">Автоматизация хранения на основе событий</span><span class="sxs-lookup"><span data-stu-id="d9437-103">Automate event-based retention</span></span>

<span data-ttu-id="d9437-p101">Процессы развертывания содержимого в организации, а также обнаружения избыточных, устаревших и тривиальных данных играют важную роль. Чтобы продолжать соответствовать юридическим, нормативным и бизнес-требованиям, компания должна обеспечить хранение и защиту важной информации, а также быстрый поиск необходимых данных. Хранение только важной и подходящей информации является ключевым фактором успеха.</span><span class="sxs-lookup"><span data-stu-id="d9437-p101">The explosion of content in organizations and how it can become ROT (redundant, obsolete, trivial) is serious business. To continue to meet legal, business, and regulatory compliance challenges, businesses must be able to keep and protect important information and quickly find what’s relevant. Retaining only important, pertinent information is key to a business’s success.</span></span>

<span data-ttu-id="d9437-p102">Поэтому организации могут использовать преимущества решений для хранения в Центре безопасности и соответствия требованиям Office 365. Связанные с хранением операции можно активировать с помощью [меток хранения](labels.md). У метки хранения есть параметр для [определения периода хранения на основе конкретного события](event-driven-retention.md). Обычно период хранения зависит от известной даты, например даты создания или последнего изменения содержимого. Однако у организаций также есть требования по удалению содержимого на основе возникновения событий, например через 7 лет после того, как сотрудник уволился из организации.</span><span class="sxs-lookup"><span data-stu-id="d9437-p102">Hence organizations can take advantage of retention solutions in the Office 365 Security & Compliance Center. Retention can be triggered by using [retention labels](labels.md). A retention label has the option to [base the retention period on a specific event](event-driven-retention.md). Typically, the retention period is based on a known date, such as the creation date or last modified date for the content. However, organizations also have requirements to dispose of content based on the occurrence of an event, such as 7 years after an employee leaves an organization.</span></span>

<span data-ttu-id="d9437-p103">Чтобы обеспечить удаление содержимого в соответствии с требованиями, важно знать, когда происходят события. Из-за стремительного роста объема содержимого становится сложно хранить и удалять данные своевременно и в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="d9437-p103">In order to ensure compliant disposal of content, it is imperative to know when an event takes place. With the volume of content increasing rapidly, it is becoming challenging to retain and dispose content in a timely and compliant manner.</span></span>

<span data-ttu-id="d9437-p104">Хранения на основе событий решает эту проблему. В этой статье описывается, как настроить операции бизнес-процесса, чтобы автоматизировать хранение с помощью событий, используя REST API Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d9437-p104">Event-based retention solves this problem. This topic explains how to set up your business process flows to automate retention through events by using the Microsoft 365 REST API.</span></span>

## <a name="about-event-based-retention"></a><span data-ttu-id="d9437-116">О хранении на основе событий</span><span class="sxs-lookup"><span data-stu-id="d9437-116">About event-based retention</span></span>

<span data-ttu-id="d9437-p105">Независимо от размера организации количество деловых документов, юридических документов, файлов сотрудников, договоров и документов о продукции, которые ежедневно создаются и которыми необходимо управлять, стремительно растет.</span><span class="sxs-lookup"><span data-stu-id="d9437-p105">An organization can be small, medium, or large. The number of business documents, legal documents, employee files, contracts, and product documents that get created and managed on a day to day basis is increasing dramatically.</span></span>

<span data-ttu-id="d9437-p106">Например, каждый день десятки и сотни сотрудников устраиваются на работу в организации или увольняются. Отдел кадров постоянно создает, обновляет или удаляет связанные с сотрудниками документы в соответствии с бизнес-требованиями. Этот процесс регулируется различными политиками, определяемыми для компании:</span><span class="sxs-lookup"><span data-stu-id="d9437-p106">For example, each day, tens and hundreds of employees are joining and leaving organizations. The HR department continues to create, update, or delete employee-related documents as per business requirements. This process is subject to the different retention policies outlined for the business:</span></span>

- <span data-ttu-id="d9437-p107">**Период хранения содержимого может зависеть от известной даты**, например даты создания, последнего изменения содержимого или присвоения ему метки. Пример: вы можете хранить документы в течение семи лет после создания, а затем удалить их.</span><span class="sxs-lookup"><span data-stu-id="d9437-p107">**The period of retention for content can be a known date** such as the date the content was created, last modified or labeled. For example, you might retain documents for seven years after they're created and then delete them.</span></span>

- <span data-ttu-id="d9437-p108">**Период хранения содержимого может зависеть от неизвестной даты**. Например, с помощью меток хранения можно определять зависимость периода хранения от возникновения определенного типа события, такого как увольнение сотрудника из организации.</span><span class="sxs-lookup"><span data-stu-id="d9437-p108">**The period of retention of content can also be an unknown date**. For example, with retention labels, you can also base a retention period on when a specific type of event occurs, such as an employee leaving the organization.</span></span>

<span data-ttu-id="d9437-p109">Событие активирует начало периода хранения, и ко всему содержимому с меткой, относящейся к событию данного типа, применяются действия хранения. Этот процесс называется хранением на основе событий. Дополнительные сведения о нем см. в статье [Общие сведения о хранении, зависящем от возникновения события](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="d9437-p109">The event triggers the start of the retention period, and all content with a label applied for that type of event get the label's retention actions enforced on them. This is called event-based retention - to learn more, see [Overview of event-driven retention](event-driven-retention.md).</span></span>

## <a name="set-up-event-based-retention"></a><span data-ttu-id="d9437-128">Настройка хранении на основе событий</span><span class="sxs-lookup"><span data-stu-id="d9437-128">Set up event-based retention</span></span>

<span data-ttu-id="d9437-129">В этом разделе описываются действия, необходимые для подготовки хранения содержимого.</span><span class="sxs-lookup"><span data-stu-id="d9437-129">This section describes what needs to be done prior to retaining content.</span></span>

### <a name="identify-roles"></a><span data-ttu-id="d9437-130">Определение ролей</span><span class="sxs-lookup"><span data-stu-id="d9437-130">Identify roles</span></span>

<span data-ttu-id="d9437-131">Определите различные роли в организации, которые будут выполнять задачи управления записями, обеспечивающие эффективное хранение деловых документов.</span><span class="sxs-lookup"><span data-stu-id="d9437-131">Identify the different roles in an organization that perform Record Management tasks that would be responsible for effective and efficient retention of business documents.</span></span>

  | <span data-ttu-id="d9437-132">**Роль**</span><span class="sxs-lookup"><span data-stu-id="d9437-132">**Persona**</span></span>| <span data-ttu-id="d9437-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9437-133">**Role**</span></span>|
  | - | - |
  | <span data-ttu-id="d9437-134">Администратор Центра безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d9437-134">Security & Compliance Center admin</span></span> | <span data-ttu-id="d9437-135">Создает типы событий хранения, метки хранения и репозитории записей в SharePoint</span><span class="sxs-lookup"><span data-stu-id="d9437-135">Creates Retention Event types, Retention labels and Record repositories in SharePoint</span></span> |
  | <span data-ttu-id="d9437-136">Управляющий записями</span><span class="sxs-lookup"><span data-stu-id="d9437-136">Records Manager</span></span>                                  | <span data-ttu-id="d9437-137">Предоставляет указания по политикам и расписанию хранения, а также сведения о соответствии требованиям</span><span class="sxs-lookup"><span data-stu-id="d9437-137">Provides Retention Policies and Retention Schedules guidance and compliance details</span></span>   |
  | <span data-ttu-id="d9437-138">Системный администратор (компания)</span><span class="sxs-lookup"><span data-stu-id="d9437-138">System Admin (business)</span></span>                          | <span data-ttu-id="d9437-139">Настраивает внешние системы для работы с Microsoft 365 и управляет ими</span><span class="sxs-lookup"><span data-stu-id="d9437-139">Sets up and manages external systems to work with Microsoft 365</span></span>                       |
  | <span data-ttu-id="d9437-140">Информационный работник</span><span class="sxs-lookup"><span data-stu-id="d9437-140">Information Worker</span></span>                               | <span data-ttu-id="d9437-141">Управляет жизненным циклом своих бизнес-процессов (отдела кадров, финансового отдела, ИТ-отдела и т. д.)</span><span class="sxs-lookup"><span data-stu-id="d9437-141">Manages the lifecycle of their business process (HR, Finance, IT etc)</span></span>                 |

### <a name="set-up-the-security--compliance-center"></a><span data-ttu-id="d9437-142">Настройка Центра безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d9437-142">Set up the Security & Compliance Center</span></span>
  
1. <span data-ttu-id="d9437-143">Администратор соответствия требованиям создает тип события, например увольнение сотрудника, завершение действия договора или прекращение производства продукта (описание пошагового процесса см. в [статье о событиях хранения](https://docs.microsoft.com/ru-RU/office365/securitycompliance/event-driven-retention)).</span><span class="sxs-lookup"><span data-stu-id="d9437-143">Compliance admin creates an event type – for example, Employee Termination or Contract Expiration or End of Product Manufacturing (Please refer to step by step process in [Event retention article](https://docs.microsoft.com/ru-RU/office365/securitycompliance/event-driven-retention)</span></span>
    
1. <span data-ttu-id="d9437-144">Администратор соответствия требованиям создает метку хранения на основе события и связывает метку с типом события.</span><span class="sxs-lookup"><span data-stu-id="d9437-144">Compliance admin creates a retention label based on an event and associates the label with an event type</span></span>
    
1. <span data-ttu-id="d9437-145">Существует 4 типа триггеров меток хранения:</span><span class="sxs-lookup"><span data-stu-id="d9437-145">There are 4 types of triggers for retention labels:</span></span>
            
    1. <span data-ttu-id="d9437-146">Дата создания</span><span class="sxs-lookup"><span data-stu-id="d9437-146">Create date</span></span>
                
    1. <span data-ttu-id="d9437-147">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="d9437-147">Last modified</span></span>
                
    1. <span data-ttu-id="d9437-148">Дата метки (когда содержимому была присвоена метка)</span><span class="sxs-lookup"><span data-stu-id="d9437-148">Label date (when the content was labeled)</span></span>
                
    1. <span data-ttu-id="d9437-149">На основе события</span><span class="sxs-lookup"><span data-stu-id="d9437-149">Event-based</span></span>
    
1. <span data-ttu-id="d9437-150">Администратор соответствия требованиям публикует метку.</span><span class="sxs-lookup"><span data-stu-id="d9437-150">Compliance admin publishes the label</span></span>

### <a name="set-up-sharepoint"></a><span data-ttu-id="d9437-151">Настройка SharePoint</span><span class="sxs-lookup"><span data-stu-id="d9437-151">Set up SharePoint</span></span>
   
<span data-ttu-id="d9437-152">Чтобы создать репозиторий записей, администратор соответствия требованиям выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d9437-152">To create a records repository, the compliance admin:</span></span>

1. <span data-ttu-id="d9437-153">Создает сайт SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d9437-153">Creates a SharePoint site.</span></span>

1. <span data-ttu-id="d9437-154">Выполняет одно из указанных ниже действий:</span><span class="sxs-lookup"><span data-stu-id="d9437-154">Does one of the following:</span></span>
        
    - <span data-ttu-id="d9437-p110">Создает библиотеку SharePoint: задает метку на основе события на уровне библиотеки. Дополнительные сведения см. в разделе "Применение метки хранения по умолчанию ко всему контенту в библиотеке SharePoint, папке или набору документов" [этой статьи](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="d9437-p110">Creates a SharePoint library: Set event-based label at the library level. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
          
    - <span data-ttu-id="d9437-p111">Настраивает набор документов в SharePoint. Дополнительные сведения см. в статье [Общие сведения о наборах документов](https://support.office.com/ru-RU/article/Introduction-to-Document-Sets-3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).</span><span class="sxs-lookup"><span data-stu-id="d9437-p111">Sets up a Document set in SharePoint. For more information, see [Introduction to document sets](https://support.office.com/ru-RU/article/Introduction-to-Document-Sets-3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).</span></span>
      
1. <span data-ttu-id="d9437-p112">Назначает идентификатор ресурса (то есть название продукта или код, используемые в организации, например в роли идентификатора ресурса может выступать код сотрудника) каждому набору документов сотрудника. (При назначении идентификатора ресурса папке каждый элемент в папке автоматически наследует тот же идентификатор ресурса. То есть период хранения всех элементов запускается одним событием.)</span><span class="sxs-lookup"><span data-stu-id="d9437-p112">Assigns Asset Id (asset ID is a product name or code used by the organization, for example, Employee number can be an asset id) to each employee document set (By assigning the asset ID to the folder, every item in that folder automatically inherits the same asset ID. This means all the items can have their retention period triggered by the same event.</span></span>

## <a name="ways-to-trigger-event-based-retention"></a><span data-ttu-id="d9437-161">Способы запуска хранения на основе события</span><span class="sxs-lookup"><span data-stu-id="d9437-161">Ways to trigger event-based retention</span></span>

<span data-ttu-id="d9437-162">Существует два способа запуска хранения на основе события:</span><span class="sxs-lookup"><span data-stu-id="d9437-162">There are two ways in which event-based retention can be triggered:</span></span>

- <span data-ttu-id="d9437-p113">**С помощью пользовательского интерфейса Центра безопасности и соответствия требованиям**. Этот процесс можно использовать для хранения содержимого небольшого объема или в случае, когда активация хранения происходит редко (один раз в месяц или год). Дополнительные сведения об этом методе см. в статье [Общие сведения о хранении, зависящем от возникновения события](event-driven-retention.md). Однако этот способ запуска хранения может занимать много времени и уязвим для ошибок, что ограничивает масштабируемость. Поэтому автоматизированное и простое решение для активации хранения может повысить безопасность данных и улучшить их соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-p113">**Using Security & Compliance Center UI** This is a process that can be used to retain less content at a time or the frequency to trigger retention is not often, such as monthly or yearly. For more information on this method, see [Overview of event-driven retention](event-driven-retention.md). However, this way to trigger retention can be time-consuming and prone to error, thus stunting scalability. Therefore, an automated, seamless solution to trigger retention can enhance the security and compliance of data.</span></span>

- <span data-ttu-id="d9437-p114">**С помощью REST API M365.** Этот процесс можно использовать для хранения большого объема данных и/или в случае частой активации хранения (каждый день или каждую неделю). Этот процесс определяет, когда событие возникает в вашей бизнес-системе, и автоматически создает связанное событие в Центре безопасности и соответствия требованиям. Вам не нужно вручную создавать связанное событие в пользовательском интерфейсе каждый раз, когда происходит исходное событие.</span><span class="sxs-lookup"><span data-stu-id="d9437-p114">**Using a M365 REST API** This process can be used when large amounts of content are to be retained at a time and/or the frequency to trigger retention is often such as daily or weekly. The flow detects when an event occurs in your line-of-business system, and then automatically creates a related event in the Security & Compliance Center. You don't need to manually create an event in the UI each time one occurs.</span></span>

<span data-ttu-id="d9437-170">Существует два способа использования REST API:</span><span class="sxs-lookup"><span data-stu-id="d9437-170">There are two options for using the REST API:</span></span>

- <span data-ttu-id="d9437-p115">**Microsoft Flow или аналогичное приложение** можно использовать для автоматического запуска события. Microsoft Flow — это оркестратор для подключения к другим системам. Для использования Microsoft Flow не требуется пользовательское решение.</span><span class="sxs-lookup"><span data-stu-id="d9437-p115">**Microsoft Flow or a similar application** can be used to trigger the occurrence of an event automatically. Microsoft Flow is an orchestrator for connecting to other systems. Using Microsoft Flow does not require a custom solution.</span></span>

- <span data-ttu-id="d9437-174">**PowerShell или HTTP-клиент для вызова REST API**. Используйте PowerShell (версии 6 или выше) для вызова REST API Microsoft 365, чтобы создать события.</span><span class="sxs-lookup"><span data-stu-id="d9437-174">**PowerShell or an HTTP client to call REST API** Using PowerShell (version 6 or higher) to call Microsoft 365 REST API to create events.</span></span> 

<span data-ttu-id="d9437-p116">REST API — это конечная точка службы, поддерживающая операции (методы) HTTP, которая предоставляет права на создание, получение, обновление или удаление ресурсов службы. Дополнительные сведения см. в разделе "Компоненты запроса/ответа REST API" [этой статьи](https://docs.microsoft.com/ru-RU/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse). В этом случае используя REST API Microsoft 365, можно создавать или получать события с помощью операций (методов) POST и GET.</span><span class="sxs-lookup"><span data-stu-id="d9437-p116">A Rest API is a service endpoint that supports sets of HTTP operations (methods), which provide create/retrieve/update/delete access to the service's resources - for more information, see [Components of a REST API request/response](https://docs.microsoft.com/ru-RU/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse). In this case, by using the Microsoft 365 REST API, events can be created and retrieved using operations (methods) POST and GET.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="d9437-177">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="d9437-177">Example scenarios</span></span>

<span data-ttu-id="d9437-178">Давайте рассмотрим следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="d9437-178">Let’s consider the following scenarios.</span></span>

### <a name="scenario-1-employees-leaving-the-organization"></a><span data-ttu-id="d9437-179">Сценарий 1. Сотрудники увольняются из организации</span><span class="sxs-lookup"><span data-stu-id="d9437-179">Scenario 1: Employees leaving the organization</span></span> 

<span data-ttu-id="d9437-p117">Организация создает и хранит множество документов для каждого сотрудника. Эти документы управляются и хранятся в ходе трудовых отношений с сотрудником. Однако, когда сотрудник увольняется, организация в соответствии с законом и бизнес-требованиями обязана хранить документы об этом сотруднике в течение указанного периода.</span><span class="sxs-lookup"><span data-stu-id="d9437-p117">An organization creates and stores numerous employee related documents per employee. These documents are managed and retained during the employment of each employee. However, when the employee leaves the organization or the employment is terminated, the organization is obligated by legal and business requirements to retain the documents of that employee for a stipulated period.</span></span>

<span data-ttu-id="d9437-183">Если из организации ежедневно увольняется несколько сотрудников, необходимо запускать счетчики хранения сотен или даже тысяч документов каждый день.</span><span class="sxs-lookup"><span data-stu-id="d9437-183">Now if multiple employees leave the organization every day, the organization must trigger the retention clock of hundreds if not thousands of documents each day.</span></span>

<span data-ttu-id="d9437-p118">Кроме того, для каждого сотрудника период хранения рассчитывается на основе типа записи сотрудника (дата увольнения сотрудника + количество дней, месяцев или лет). Например, у документов о зарплате и документов о премии одного и того же сотрудника могут быть разные периоды хранения.</span><span class="sxs-lookup"><span data-stu-id="d9437-p118">In addition to this, the retention period needs to be calculated for each of these employees as Employee termination date + number of days, months or years based on the type of the employee record. For example, worker’s compensation of the employee vs benefits filings of the same employee may need different retention.</span></span>

<span data-ttu-id="d9437-p119">На схеме ниже показано, как с одним событием может быть связано несколько меток. Здесь все файлы с меткой зарплаты сотрудника и файлы с меткой премии сотрудника связаны с одним событием — увольнением сотрудника из организации. У каждого из этих файлов разные счетчики хранения. Поэтому, когда сотрудник увольняется из организации, у этих файлов с метками разный период хранения. Запуск всех этих разных счетчиков хранения для каждого типа файла или метки для каждого сотрудника является очень сложной задачей. А теперь представьте, что это нужно делать для нескольких сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d9437-p119">The diagram below shows how there can be multiple labels that are associated with a single event. Here all the files under Worker’s compensation label and all the files under Employee benefits label are both associated with a single event which is the employee leaving the organization. Each of these different files have different retention clocks. So, when an employee leaves the organization, these files within each label experience a different retention period. To trigger all these different retention clocks for each file type or label for each employee is a very challenging task. Imagine doing this for multiple employees.</span></span>

![Схема типов событий, событий и меток](media/automate-event-driven-retention-event-diagram-employee-leaving.png)

<span data-ttu-id="d9437-193">Поэтому автоматизированный процесс запуска всех этих различных счетчиков хранения для нескольких сотрудников должен работать быстро, быть безошибочным и очень эффективным.</span><span class="sxs-lookup"><span data-stu-id="d9437-193">Hence an automated process to trigger these different retention clocks for multiple employees will be time-saving, error-free and extremely efficient .</span></span>

<span data-ttu-id="d9437-194">**Настройка автоматизированного хранения на основе событий для этого сценария:**</span><span class="sxs-lookup"><span data-stu-id="d9437-194">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Схема ролей и действий для сценария, когда сотрудник увольняется из организации](media/automate-event-driven-retention-employee-termination-diagram.png)

  - <span data-ttu-id="d9437-196">Администратор создает папки сотрудников в наборе документов, например "Марта Артемьева", "Артем Кузнецов".</span><span class="sxs-lookup"><span data-stu-id="d9437-196">Admin c reates employee folders to the Document set such as Jane Doe, John Smith.</span></span>

  - <span data-ttu-id="d9437-197">Администратор добавляет в каждую папку файлы сотрудников, например с данными о премиях и зарплате.</span><span class="sxs-lookup"><span data-stu-id="d9437-197">Admin adds employee files such as Benefits, Payroll, Worker’s Compensation to each employee folder</span></span>

  - <span data-ttu-id="d9437-198">Администратор назначает идентификатор ресурса для каждой папки сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d9437-198">Admin assigns Asset Id to each employee folder.</span></span> 

  - <span data-ttu-id="d9437-199">Администратор Центра безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d9437-199">SCC Admin l</span></span>

  - <span data-ttu-id="d9437-200">выполняет вход в Центр безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-200">ogs into the Security & Compliance Center</span></span>

  - <span data-ttu-id="d9437-201">Администратор Центра безопасности и соответствия требованиям создает связанные с сотрудниками типы событий, например события "Увольнение сотрудника", "Прием сотрудника на работу" в Центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-201">SCC Admin creates employee related events types such as “Employee Termination”, “Employee Hire” events in Security and Compliance Center.</span></span>

  - <span data-ttu-id="d9437-202">Администратор Центра безопасности и соответствия требованиям создает метку "Хранение для сотрудника" в Центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-202">SCC Admin creates “Employee Retention” label in Security and Compliance Center.</span></span>

  - <span data-ttu-id="d9437-203">Эта метка "Хранение для сотрудника" публикуется и вручную или автоматически применяется к файлам сотрудника в SharePoint</span><span class="sxs-lookup"><span data-stu-id="d9437-203">This “Employee Retention” label is published and applied manually or automatically to the employee files in SharePoint</span></span>

  - <span data-ttu-id="d9437-204">Система управления отдела кадров, например Workday, может работать совместно с Microsoft Flow для периодического управления файлами сотрудников</span><span class="sxs-lookup"><span data-stu-id="d9437-204">HR Management System like Workday can work with Microsoft Flow to run periodically to manage employee files</span></span>

  - <span data-ttu-id="d9437-205">Если сотрудник увольняется из организации, Flow активирует REST API хранения на основе событий M365, который запустит счетчик хранения для файлов определенного сотрудника.</span><span class="sxs-lookup"><span data-stu-id="d9437-205">If an employee has left the organization, the Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific employee’s files.</span></span>

#### <a name="using-microsoft-flow"></a><span data-ttu-id="d9437-206">Использование Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="d9437-206">Using Microsoft Flow</span></span>

<span data-ttu-id="d9437-207">Шаг 1. Создайте процесс создания события с помощью REST API Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d9437-207">Step 1- Create a flow to create an event using the Microsoft 365 REST API</span></span>

![Использование Flow для создания события](media/automate-event-driven-retention-flow-1.png)

![Использование Flow для вызова REST API](media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a><span data-ttu-id="d9437-210">Создание события</span><span class="sxs-lookup"><span data-stu-id="d9437-210">Create an event</span></span>

<span data-ttu-id="d9437-211">Пример кода для вызова REST API</span><span class="sxs-lookup"><span data-stu-id="d9437-211">Sample code to call the REST API</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9437-212">Метод</span><span class="sxs-lookup"><span data-stu-id="d9437-212">Method</span></span></th>
<th><span data-ttu-id="d9437-213">POST</span><span class="sxs-lookup"><span data-stu-id="d9437-213">POST</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9437-214">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d9437-214">URL</span></span></td>
<td>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent)</td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-215">Заголовки</span><span class="sxs-lookup"><span data-stu-id="d9437-215">Headers</span></span></td>
<td><span data-ttu-id="d9437-216">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d9437-216">Content-Type</span></span></td>
<td><span data-ttu-id="d9437-217">приложение/atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-217">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9437-218">Основной текст</span><span class="sxs-lookup"><span data-stu-id="d9437-218">Body</span></span></td>
<td><p><span data-ttu-id="d9437-219">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-219">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="d9437-220">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="d9437-220">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="d9437-221">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="d9437-221">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="d9437-222">xmlns='http://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-222">xmlns='http://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="d9437-223">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-223">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="d9437-224">&lt;updated&gt;9/9/2017 10:50:00 PM&lt;/updated&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-224">&lt;updated&gt;9/9/2017 10:50:00 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="d9437-225">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-225">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="d9437-226">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-226">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="d9437-227">&lt;d:Name&gt;Employee Termination &lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-227">&lt;d:Name&gt;Employee Termination &lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="d9437-228">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-228">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="d9437-229">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-229">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="d9437-230">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-230">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span></span></p>
<p><span data-ttu-id="d9437-231">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-231">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="d9437-232">&lt;/content&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-232">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="d9437-233">&lt;/entry&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-233">&lt;/entry&gt;</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-234">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-234">Authentication</span></span></td>
<td><span data-ttu-id="d9437-235">Базовая</span><span class="sxs-lookup"><span data-stu-id="d9437-235">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9437-236">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="d9437-236">Username</span></span></td>
<td><span data-ttu-id="d9437-237">"Complianceuser"</span><span class="sxs-lookup"><span data-stu-id="d9437-237">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-238">Пароль</span><span class="sxs-lookup"><span data-stu-id="d9437-238">Password</span></span></td>
<td><span data-ttu-id="d9437-239">"Compliancepassword"</span><span class="sxs-lookup"><span data-stu-id="d9437-239">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="available-parameters"></a><span data-ttu-id="d9437-240">Доступные параметры</span><span class="sxs-lookup"><span data-stu-id="d9437-240">Available parameters</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9437-241"><strong>Параметры</strong></span><span class="sxs-lookup"><span data-stu-id="d9437-241"><strong>Parameters</strong></span></span></th>
<th><span data-ttu-id="d9437-242"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="d9437-242"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="d9437-243"><strong>Примечания</strong></span><span class="sxs-lookup"><span data-stu-id="d9437-243"><strong>Notes</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9437-244">&lt;d:Name&gt;&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-244">&lt;d:Name&gt;&lt;/d:Name&gt;</span></span></td>
<td><span data-ttu-id="d9437-245">Указание уникального имени события.</span><span class="sxs-lookup"><span data-stu-id="d9437-245">Provide a unique name for the event,</span></span></td>
<td><span data-ttu-id="d9437-p120">Не может содержать начальные и конечные пробелы и следующие символы: % \* \ &amp; &lt; &gt; | # ? , : ;</span><span class="sxs-lookup"><span data-stu-id="d9437-p120">Cannot contain trailing spaces, and the following characters: % \* \ &amp; &lt; &gt; | # ? , : ;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-248">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-248">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span></span></td>
<td><span data-ttu-id="d9437-249">Введите название типа события (или Guid).</span><span class="sxs-lookup"><span data-stu-id="d9437-249">Enter event type name (or Guid),</span></span></td>
<td><span data-ttu-id="d9437-p121">Пример: "Увольнение сотрудника". Тип события должен быть связан с меткой хранения.</span><span class="sxs-lookup"><span data-stu-id="d9437-p121">Example: “Employee termination”. Event type has to be associated with a retention label.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9437-252">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-252">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span></span></td>
<td><span data-ttu-id="d9437-253">Введите "ComplianceAssetId:" + код сотрудника</span><span class="sxs-lookup"><span data-stu-id="d9437-253">Enter “ComplianceAssetId:” + employee Id</span></span></td>
<td><span data-ttu-id="d9437-254">Пример: &quot;ComplianceAssetId:12345&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-254">Example:&quot;ComplianceAssetId:12345&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-255">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-255">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span></span></td>
<td><span data-ttu-id="d9437-256">Дата и время события</span><span class="sxs-lookup"><span data-stu-id="d9437-256">Event Date and Time</span></span></td>
<td><p><span data-ttu-id="d9437-257">Формат: ГГГГ-ММ-ДДTчч:мм:ссZ. Пример:</span><span class="sxs-lookup"><span data-stu-id="d9437-257">Format: yyyy-MM-ddTHH:mm:ssZ, Example:</span></span></p>
<p><span data-ttu-id="d9437-258">2018-12-01T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="d9437-258">2018-12-01T00:00:00Z</span></span></p></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="d9437-259">Коды ответа</span><span class="sxs-lookup"><span data-stu-id="d9437-259">Response codes</span></span>

| <span data-ttu-id="d9437-260">**Код ответа**</span><span class="sxs-lookup"><span data-stu-id="d9437-260">**Response Code**</span></span> | <span data-ttu-id="d9437-261">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9437-261">**Description**</span></span>       |
| ----------------- | --------------------- |
| <span data-ttu-id="d9437-262">302</span><span class="sxs-lookup"><span data-stu-id="d9437-262">302</span></span>               | <span data-ttu-id="d9437-263">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="d9437-263">Redirect</span></span>              |
| <span data-ttu-id="d9437-264">201</span><span class="sxs-lookup"><span data-stu-id="d9437-264">201</span></span>               | <span data-ttu-id="d9437-265">Создано</span><span class="sxs-lookup"><span data-stu-id="d9437-265">Created</span></span>               |
| <span data-ttu-id="d9437-266">403</span><span class="sxs-lookup"><span data-stu-id="d9437-266">403</span></span>               | <span data-ttu-id="d9437-267">Сбой авторизации</span><span class="sxs-lookup"><span data-stu-id="d9437-267">Authorization Failed</span></span>  |
| <span data-ttu-id="d9437-268">401</span><span class="sxs-lookup"><span data-stu-id="d9437-268">401</span></span>               | <span data-ttu-id="d9437-269">Сбой проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-269">Authentication Failed</span></span> |

##### <a name="get-events-based-on-time-range"></a><span data-ttu-id="d9437-270">Получение событий на основе диапазона времени</span><span class="sxs-lookup"><span data-stu-id="d9437-270">Get Events based on time range</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9437-271">Метод</span><span class="sxs-lookup"><span data-stu-id="d9437-271">Method</span></span></th>
<th><span data-ttu-id="d9437-272">GET</span><span class="sxs-lookup"><span data-stu-id="d9437-272">GET</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9437-273">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d9437-273">URL</span></span></td>
<td><ol start="4" type="1">
<li><p><span data-ttu-id="d9437-274">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span><span class="sxs-lookup"><span data-stu-id="d9437-274">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span></span></p></li>
</ol></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-275">Заголовки</span><span class="sxs-lookup"><span data-stu-id="d9437-275">Headers</span></span></td>
<td><span data-ttu-id="d9437-276">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d9437-276">Content-Type</span></span></td>
<td><span data-ttu-id="d9437-277">приложение/atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-277">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-278">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-278">Authentication</span></span></td>
<td><span data-ttu-id="d9437-279">Базовая</span><span class="sxs-lookup"><span data-stu-id="d9437-279">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9437-280">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="d9437-280">Username</span></span></td>
<td><span data-ttu-id="d9437-281">"Complianceuser"</span><span class="sxs-lookup"><span data-stu-id="d9437-281">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9437-282">Пароль</span><span class="sxs-lookup"><span data-stu-id="d9437-282">Password</span></span></td>
<td><span data-ttu-id="d9437-283">"Compliancepassword"</span><span class="sxs-lookup"><span data-stu-id="d9437-283">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="d9437-284">Коды ответа</span><span class="sxs-lookup"><span data-stu-id="d9437-284">Response codes</span></span>

| <span data-ttu-id="d9437-285">**Код ответа**</span><span class="sxs-lookup"><span data-stu-id="d9437-285">**Response Code**</span></span> | <span data-ttu-id="d9437-286">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9437-286">**Description**</span></span>                   |
| ----------------- | --------------------------------- |
| <span data-ttu-id="d9437-287">200</span><span class="sxs-lookup"><span data-stu-id="d9437-287">200</span></span>               | <span data-ttu-id="d9437-288">Все в порядке, список событий в формате atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-288">OK, A list of events in atom+ xml</span></span> |
| <span data-ttu-id="d9437-289">404</span><span class="sxs-lookup"><span data-stu-id="d9437-289">404</span></span>               | <span data-ttu-id="d9437-290">Не найдено</span><span class="sxs-lookup"><span data-stu-id="d9437-290">Not found</span></span>                         |
| <span data-ttu-id="d9437-291">302</span><span class="sxs-lookup"><span data-stu-id="d9437-291">302</span></span>               | <span data-ttu-id="d9437-292">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="d9437-292">Redirect</span></span>                          |
| <span data-ttu-id="d9437-293">401</span><span class="sxs-lookup"><span data-stu-id="d9437-293">401</span></span>               | <span data-ttu-id="d9437-294">Сбой авторизации</span><span class="sxs-lookup"><span data-stu-id="d9437-294">Authorization Failed</span></span>              |
| <span data-ttu-id="d9437-295">403</span><span class="sxs-lookup"><span data-stu-id="d9437-295">403</span></span>               | <span data-ttu-id="d9437-296">Сбой проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-296">Authentication Failed</span></span>             |

##### <a name="get-an-event-by-id"></a><span data-ttu-id="d9437-297">Получение события по идентификатору</span><span class="sxs-lookup"><span data-stu-id="d9437-297">Get an event by ID</span></span>

| <span data-ttu-id="d9437-298">Метод</span><span class="sxs-lookup"><span data-stu-id="d9437-298">Method</span></span>         | <span data-ttu-id="d9437-299">GET</span><span class="sxs-lookup"><span data-stu-id="d9437-299">GET</span></span>   |                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------- |
| <span data-ttu-id="d9437-300">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d9437-300">URL</span></span>            | <span data-ttu-id="d9437-301">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span><span class="sxs-lookup"><span data-stu-id="d9437-301">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span></span> |                      |
| <span data-ttu-id="d9437-302">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9437-302">Header</span></span>         | <span data-ttu-id="d9437-303">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d9437-303">Content-Type</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="d9437-304">приложение/atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-304">application/atom+xml</span></span> |
| <span data-ttu-id="d9437-305">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-305">Authentication</span></span> | <span data-ttu-id="d9437-306">Базовая</span><span class="sxs-lookup"><span data-stu-id="d9437-306">Basic</span></span>                                                                                                                                                                                                                                                              |                      |
| <span data-ttu-id="d9437-307">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="d9437-307">Username</span></span>       | <span data-ttu-id="d9437-308">"Complianceuser"</span><span class="sxs-lookup"><span data-stu-id="d9437-308">“Complianceuser”</span></span>                                                                                                                                                                                                                                                   |                      |
| <span data-ttu-id="d9437-309">Пароль</span><span class="sxs-lookup"><span data-stu-id="d9437-309">Password</span></span>       | <span data-ttu-id="d9437-310">"Compliancepassword"</span><span class="sxs-lookup"><span data-stu-id="d9437-310">“Compliancepassword”</span></span>                                                                                                                                                                                                                                               |                      |

##### <a name="response-codes"></a><span data-ttu-id="d9437-311">Коды ответа</span><span class="sxs-lookup"><span data-stu-id="d9437-311">Response codes</span></span>

| <span data-ttu-id="d9437-312">**Код ответа**</span><span class="sxs-lookup"><span data-stu-id="d9437-312">**Response Code**</span></span> | <span data-ttu-id="d9437-313">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9437-313">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="d9437-314">200</span><span class="sxs-lookup"><span data-stu-id="d9437-314">200</span></span>               | <span data-ttu-id="d9437-315">Все в порядке, текст ответа содержит событие в формате atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-315">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="d9437-316">404</span><span class="sxs-lookup"><span data-stu-id="d9437-316">404</span></span>               | <span data-ttu-id="d9437-317">Не найдено</span><span class="sxs-lookup"><span data-stu-id="d9437-317">Not found</span></span>                                            |
| <span data-ttu-id="d9437-318">302</span><span class="sxs-lookup"><span data-stu-id="d9437-318">302</span></span>               | <span data-ttu-id="d9437-319">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="d9437-319">Redirect</span></span>                                             |
| <span data-ttu-id="d9437-320">401</span><span class="sxs-lookup"><span data-stu-id="d9437-320">401</span></span>               | <span data-ttu-id="d9437-321">Сбой авторизации</span><span class="sxs-lookup"><span data-stu-id="d9437-321">Authorization Failed</span></span>                                 |
| <span data-ttu-id="d9437-322">403</span><span class="sxs-lookup"><span data-stu-id="d9437-322">403</span></span>               | <span data-ttu-id="d9437-323">Сбой проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-323">Authentication Failed</span></span>                                |

##### <a name="get-an-event-by-name"></a><span data-ttu-id="d9437-324">Получение события по имени</span><span class="sxs-lookup"><span data-stu-id="d9437-324">Get an event by name</span></span>

| <span data-ttu-id="d9437-325">Метод</span><span class="sxs-lookup"><span data-stu-id="d9437-325">Method</span></span>         | <span data-ttu-id="d9437-326">GET</span><span class="sxs-lookup"><span data-stu-id="d9437-326">GET</span></span>       |                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| <span data-ttu-id="d9437-327">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d9437-327">URL</span></span>            | <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('EventByRESTPost-2226bfebcc2841a8968ba71f9516b763')> |                      |
| <span data-ttu-id="d9437-328">Заголовки</span><span class="sxs-lookup"><span data-stu-id="d9437-328">Headers</span></span>        | <span data-ttu-id="d9437-329">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d9437-329">Content-Type</span></span>                                                                                                                                 | <span data-ttu-id="d9437-330">приложение/atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-330">application/atom+xml</span></span> |
| <span data-ttu-id="d9437-331">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-331">Authentication</span></span> | <span data-ttu-id="d9437-332">Базовая</span><span class="sxs-lookup"><span data-stu-id="d9437-332">Basic</span></span>                                                                                                                                        |                      |
| <span data-ttu-id="d9437-333">Имя пользователя</span><span class="sxs-lookup"><span data-stu-id="d9437-333">Username</span></span>       | <span data-ttu-id="d9437-334">"Complianceuser"</span><span class="sxs-lookup"><span data-stu-id="d9437-334">“Complianceuser”</span></span>                                                                                                                             |                      |
| <span data-ttu-id="d9437-335">Пароль</span><span class="sxs-lookup"><span data-stu-id="d9437-335">Password</span></span>       | <span data-ttu-id="d9437-336">"Compliancepassword"</span><span class="sxs-lookup"><span data-stu-id="d9437-336">“Compliancepassword”</span></span>                                                                                                                         |                      |

##### <a name="response-codes"></a><span data-ttu-id="d9437-337">Коды ответа</span><span class="sxs-lookup"><span data-stu-id="d9437-337">Response codes</span></span>

| <span data-ttu-id="d9437-338">**Код ответа**</span><span class="sxs-lookup"><span data-stu-id="d9437-338">**Response Code**</span></span> | <span data-ttu-id="d9437-339">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9437-339">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="d9437-340">200</span><span class="sxs-lookup"><span data-stu-id="d9437-340">200</span></span>               | <span data-ttu-id="d9437-341">Все в порядке, текст ответа содержит событие в формате atom+xml</span><span class="sxs-lookup"><span data-stu-id="d9437-341">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="d9437-342">404</span><span class="sxs-lookup"><span data-stu-id="d9437-342">404</span></span>               | <span data-ttu-id="d9437-343">Не найдено</span><span class="sxs-lookup"><span data-stu-id="d9437-343">Not found</span></span>                                            |
| <span data-ttu-id="d9437-344">302</span><span class="sxs-lookup"><span data-stu-id="d9437-344">302</span></span>               | <span data-ttu-id="d9437-345">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="d9437-345">Redirect</span></span>                                             |
| <span data-ttu-id="d9437-346">401</span><span class="sxs-lookup"><span data-stu-id="d9437-346">401</span></span>               | <span data-ttu-id="d9437-347">Сбой авторизации</span><span class="sxs-lookup"><span data-stu-id="d9437-347">Authorization Failed</span></span>                                 |
| <span data-ttu-id="d9437-348">403</span><span class="sxs-lookup"><span data-stu-id="d9437-348">403</span></span>               | <span data-ttu-id="d9437-349">Сбой проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="d9437-349">Authentication Failed</span></span>                                |

#### <a name="using-powershell-ver6-or-higher-or-any-http-client"></a><span data-ttu-id="d9437-350">Использование PowerShell (версии 6 или выше) или любого HTTP-клиента</span><span class="sxs-lookup"><span data-stu-id="d9437-350">Using PowerShell (ver.6 or higher) or any HTTP client</span></span>

<span data-ttu-id="d9437-351">Шаг 1. Подключитесь к PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d9437-351">Step 1: Connect to PowerShell.</span></span>

<span data-ttu-id="d9437-352">Шаг 2. Запустите указанный ниже сценарий.</span><span class="sxs-lookup"><span data-stu-id="d9437-352">Step 2: Run the following script.</span></span>

<table>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d9437-353">param([string]$baseUri)</span><span class="sxs-lookup"><span data-stu-id="d9437-353">param([string]$baseUri)</span></span></p>
<p><span data-ttu-id="d9437-354">$userName = &quot;UserName&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-354">$userName = &quot;UserName&quot;</span></span></p>
<p><span data-ttu-id="d9437-355">$password = &quot;Password&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-355">$password = &quot;Password&quot;</span></span></p>
<p><span data-ttu-id="d9437-356">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span><span class="sxs-lookup"><span data-stu-id="d9437-356">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span></span></p>
<p><span data-ttu-id="d9437-357">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span><span class="sxs-lookup"><span data-stu-id="d9437-357">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span></span></p>
<p><span data-ttu-id="d9437-358">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-358">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span></span></p>
<p><span data-ttu-id="d9437-359">Write-Host &quot;Start to create an event with name: $EventName&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-359">Write-Host &quot;Start to create an event with name: $EventName&quot;</span></span></p>
<p><span data-ttu-id="d9437-360">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-360">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="d9437-361">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="d9437-361">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="d9437-362">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="d9437-362">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="d9437-363">xmlns='http://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-363">xmlns='http://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="d9437-364">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-364">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="d9437-365">&lt;updated&gt;7/14/2017 2:03:36 PM&lt;/updated&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-365">&lt;updated&gt;7/14/2017 2:03:36 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="d9437-366">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-366">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="d9437-367">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-367">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="d9437-368">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-368">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="d9437-369">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-369">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="d9437-370">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-370">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="d9437-371">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-371">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="d9437-372">&lt;/content&gt;</span><span class="sxs-lookup"><span data-stu-id="d9437-372">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="d9437-373">&lt;/entry&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-373">&lt;/entry&gt;&quot;</span></span></p>
<p><span data-ttu-id="d9437-374">$event = $null</span><span class="sxs-lookup"><span data-stu-id="d9437-374">$event = $null</span></span></p>
<p><span data-ttu-id="d9437-375">try</span><span class="sxs-lookup"><span data-stu-id="d9437-375">try</span></span></p>
<p><span data-ttu-id="d9437-376">{</span><span class="sxs-lookup"><span data-stu-id="d9437-376">{</span></span></p>
<p><span data-ttu-id="d9437-377">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri &quot;$baseUri/ComplianceRetentionEvent&quot; -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="d9437-377">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri &quot;$baseUri/ComplianceRetentionEvent&quot; -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="d9437-378">}</span><span class="sxs-lookup"><span data-stu-id="d9437-378">}</span></span></p>
<p><span data-ttu-id="d9437-379">catch</span><span class="sxs-lookup"><span data-stu-id="d9437-379">catch</span></span></p>
<p><span data-ttu-id="d9437-380">{</span><span class="sxs-lookup"><span data-stu-id="d9437-380">{</span></span></p>
<p><span data-ttu-id="d9437-381">$response = $_.Exception.Response</span><span class="sxs-lookup"><span data-stu-id="d9437-381">$response = $_.Exception.Response</span></span></p>
<p><span data-ttu-id="d9437-382">if($response.StatusCode -eq &quot;Redirect&quot;)</span><span class="sxs-lookup"><span data-stu-id="d9437-382">if($response.StatusCode -eq &quot;Redirect&quot;)</span></span></p>
<p><span data-ttu-id="d9437-383">{</span><span class="sxs-lookup"><span data-stu-id="d9437-383">{</span></span></p>
<p><span data-ttu-id="d9437-384">$url = $response.Headers.Location</span><span class="sxs-lookup"><span data-stu-id="d9437-384">$url = $response.Headers.Location</span></span></p>
<p><span data-ttu-id="d9437-385">Write-Host &quot;redirected to $url&quot;</span><span class="sxs-lookup"><span data-stu-id="d9437-385">Write-Host &quot;redirected to $url&quot;</span></span></p>
<p><span data-ttu-id="d9437-386">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="d9437-386">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="d9437-387">}</span><span class="sxs-lookup"><span data-stu-id="d9437-387">}</span></span></p>
<p><span data-ttu-id="d9437-388">}</span><span class="sxs-lookup"><span data-stu-id="d9437-388">}</span></span></p>
<p><span data-ttu-id="d9437-389">$event | fl \*</span><span class="sxs-lookup"><span data-stu-id="d9437-389">$event | fl \*</span></span></p></td>
</tr>
</tbody>
</table>

#### <a name="verify-the-outcome-in-both-options"></a><span data-ttu-id="d9437-390">Проверка результатов обоих вариантов</span><span class="sxs-lookup"><span data-stu-id="d9437-390">Verify the outcome in both options</span></span>

<span data-ttu-id="d9437-391">Шаг 1. Перейдите в Центр безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-391">Step 1: Go to Security & Compliance Center</span></span>

<span data-ttu-id="d9437-392">Шаг 2: Щелкните пункт "Управление данными" и выберите "События".</span><span class="sxs-lookup"><span data-stu-id="d9437-392">Step 2: Click on Events under Data Governance</span></span>

<span data-ttu-id="d9437-393">Шаг 3. Убедитесь, что событие создано.</span><span class="sxs-lookup"><span data-stu-id="d9437-393">Step 3: Verify Event has been created.</span></span>

<span data-ttu-id="d9437-394">Аналогичным образом описанные выше варианты автоматизации хранения на основе событий можно использовать и для следующих сценариев.</span><span class="sxs-lookup"><span data-stu-id="d9437-394">Similarly, the above options to automate event based retention can be used for the following scenarios as well.</span></span>

### <a name="scenario-2-contracts-expiring"></a><span data-ttu-id="d9437-395">Сценарий 2. Окончание действия договоров</span><span class="sxs-lookup"><span data-stu-id="d9437-395">Scenario 2: Contracts Expiring</span></span>

<span data-ttu-id="d9437-p122">Организация может вести несколько записей для одного договора с клиентами, поставщиками и партнерами. Эти документы могут хранится в библиотеке документов, например SharePoint. Окончание действия договора определяет начало периода хранения документов, связанных с договором. Пример: все записи, связанные с договорами, следует хранить в течение пяти лет с момента завершения действия договора. Событием, которое активирует пятилетний период хранения, является завершение действия договора.</span><span class="sxs-lookup"><span data-stu-id="d9437-p122">An organization can have multiple records for a single contract with customers, vendors and partners. These documents can reside in a document library like SharePoint. The ending of a contract determines the start of the retention period of the documents associated with the contract. For example: all records related to contracts need to be retained for five years from the time the contract expires. The event that triggers the five-year retention period is the expiration of the contract.</span></span>

<span data-ttu-id="d9437-401">Система управления отношениями с клиентами может работать совместно с Microsoft 365 и активировать хранение документов договора.</span><span class="sxs-lookup"><span data-stu-id="d9437-401">A Customer Relationship Management (CRM) system can work with Microsoft 365 and trigger retention of Contract documents</span></span>

<span data-ttu-id="d9437-402">**Настройка автоматизированного хранения на основе событий для этого сценария:**</span><span class="sxs-lookup"><span data-stu-id="d9437-402">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Схема ролей и задач для сценария окончания действия договора](media/automate-event-driven-retention-contract-expiration.png)

  - <span data-ttu-id="d9437-404">Администратор создает библиотеку SharePoint с различными папками для каждого типа договора.</span><span class="sxs-lookup"><span data-stu-id="d9437-404">Admin creates a SharePoint library with various folders for each contract type.</span></span>

  - <span data-ttu-id="d9437-405">Администратор добавляет файлы договора, например лицензионные соглашения, договоры о разработке, в папку каждого договора.</span><span class="sxs-lookup"><span data-stu-id="d9437-405">Admin adds contract files such as License Contracts, Development Contracts to each contract folder</span></span>

  - <span data-ttu-id="d9437-406">Администратор назначает идентификатор ресурса для каждой папки договора.</span><span class="sxs-lookup"><span data-stu-id="d9437-406">Admin assigns Asset Id to each contract folder</span></span>

  - <span data-ttu-id="d9437-407">Администратор Центра безопасности и соответствия требованиям выполняет вход в Центр безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-407">SCC Admin logs into the Security & Compliance Center</span></span>

  - <span data-ttu-id="d9437-408">Администратор Центра безопасности и соответствия требованиям создает связанные с договорами типы событий, например события "Создание договора", "Завершение действия договора", в Центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-408">SCC Admin creates contract related events types such as “Contract Creation”, “Contract Expiration” events in Security and Compliance Center.</span></span>

  - <span data-ttu-id="d9437-409">Администратор Центра безопасности и соответствия требованиям создает метку "Завершение действия договора" в Центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-409">SCC Admin creates “Contract Expiration” label in Security and Compliance Center.</span></span>

  - <span data-ttu-id="d9437-410">Эта метка "Завершение действия договора" публикуется и вручную или автоматически применяется к файлам договора в SharePoint</span><span class="sxs-lookup"><span data-stu-id="d9437-410">This “ Contract Expiration” label is published and applied manually or automatically to the contract files in SharePoint</span></span>

  - <span data-ttu-id="d9437-411">Система управления договорами может работать совместно с Microsoft Flow или аналогичным приложением для периодического управления файлами договоров.</span><span class="sxs-lookup"><span data-stu-id="d9437-411">Contract Management System can work with Microsoft Flow or a similar application to run periodically to manage contract files</span></span>

  - <span data-ttu-id="d9437-412">Если срок действия договора завершается, Microsoft Flow активирует REST API хранения на основе событий M365, который запустит счетчик хранения для файлов определенного договора.</span><span class="sxs-lookup"><span data-stu-id="d9437-412">If a contract expires, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific contract’s files.</span></span>

### <a name="scenario-3-end-of-product-manufacturing"></a><span data-ttu-id="d9437-413">Сценарий 3. Прекращение производства продукта</span><span class="sxs-lookup"><span data-stu-id="d9437-413">Scenario 3: End of Product Manufacturing</span></span>

<span data-ttu-id="d9437-p123">Производственная компания, которая изготавливает различные линейки продуктов, создает множество документов с техническими характеристиками производства и ценами. Если продукт перестает производится, все технические характеристики и документы, связанные с этим продуктом, следует хранить в течение определенного периода времени после окончания существования продукта.</span><span class="sxs-lookup"><span data-stu-id="d9437-p123">A manufacturing company that produces different lines of products creates many manufacturing specifications and pricing documents. When the product is no longer manufactured, all specifications and documents linked to this product need to be retained for a specific period after the end of the lifetime of the product.</span></span>

<span data-ttu-id="d9437-416">Система планирования ресурсов предприятия (ERP) может работать совместно с Microsoft 365 и Microsoft Flow для активации хранения.</span><span class="sxs-lookup"><span data-stu-id="d9437-416">An Enterprise Resource Planning (ERP) system can work with Microsoft 365 and Microsoft Flow to trigger retention.</span></span>

<span data-ttu-id="d9437-417">**Настройка автоматизированного хранения на основе событий для этого сценария:**</span><span class="sxs-lookup"><span data-stu-id="d9437-417">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Схема ролей и задач для сценария жизненного цикла продукта](media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - <span data-ttu-id="d9437-419">Администратор создает папки продуктов в наборе документов, например "Продукт 1", "Продукт 2" и т. д.</span><span class="sxs-lookup"><span data-stu-id="d9437-419">Admin creates product folders in the Document set such as Product 1, Product 2, etc.</span></span>

  - <span data-ttu-id="d9437-420">Администратор добавляет файлы продуктов, например технические характеристики производства, цены продуктов и лицензирование продуктов, в каждую папку продукта.</span><span class="sxs-lookup"><span data-stu-id="d9437-420">Admin adds product files such as Manufacturing Specifications, Product Pricing, Product licensing to each product folder</span></span>

  - <span data-ttu-id="d9437-421">Администратор назначает идентификатор ресурса для каждой папки продукта.</span><span class="sxs-lookup"><span data-stu-id="d9437-421">Admin assigns Asset Id to each productfolder.</span></span>

  - <span data-ttu-id="d9437-422">Администратор Центра безопасности и соответствия требованиям выполняет вход в Центр безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-422">SCC Admin logs into the Security & Compliance Center</span></span>

  - <span data-ttu-id="d9437-423">Администратор Центра безопасности и соответствия требованиям создает связанные с сотрудниками типы событий, например события "Начало изготовления продукта", "Завершение изготовление продукта", в Центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-423">SCC Admin creates employee related events types such as “Start of Product Manufacturing”, “End of Product Manufacturing” events in Security and Compliance Center.</span></span>

  - <span data-ttu-id="d9437-424">Администратор Центра безопасности и соответствия требованиям создает метку "Завершение изготовление продукта" в Центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d9437-424">SCC Admin creates “End of Product Manufacturing” label in Security and Compliance Center.</span></span>

  - <span data-ttu-id="d9437-425">Эта метка "Завершение изготовление продукта" публикуется и вручную или автоматически применяется к файлам продукта в SharePoint</span><span class="sxs-lookup"><span data-stu-id="d9437-425">This “ End of Product Manufacturing” label is published and applied manually or automatically to the product files in SharePoint</span></span>

  - <span data-ttu-id="d9437-426">Система ERP может работать совместно с Microsoft Flow или аналогичным приложением для периодического управления файлами продуктов.</span><span class="sxs-lookup"><span data-stu-id="d9437-426">ERP Systems can work with Microsoft Flow or similar applications to run periodically to manage product files</span></span>

  - <span data-ttu-id="d9437-427">Если изготовление продукта завершается, Microsoft Flow активирует REST API хранения на основе событий M365, который запустит счетчик хранения для файлов определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="d9437-427">If the manufacturing of a product ends, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific product’s files.</span></span>

## <a name="appendix"></a><span data-ttu-id="d9437-428">Приложение</span><span class="sxs-lookup"><span data-stu-id="d9437-428">Appendix</span></span>

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a><span data-ttu-id="d9437-429">Использование результатов ответа 302 (перенаправление) для вызова REST API</span><span class="sxs-lookup"><span data-stu-id="d9437-429">Using Redirect 302 response results to call the REST API</span></span>

1.  <span data-ttu-id="d9437-430">Вызовите событие хранения POST с помощью URL-адреса REST API <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (требуются разрешения глобального администратора)</span><span class="sxs-lookup"><span data-stu-id="d9437-430">Invoke a POST retention event call using the REST API URL <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (Global Admin permissions are required)</span></span>

2.  <span data-ttu-id="d9437-p124">Проверьте код ответа. Если получен код 302, получите URL-адрес перенаправления из свойства Location (Расположение) заголовка ответа</span><span class="sxs-lookup"><span data-stu-id="d9437-p124">Check the response code. If it’s 302, then get the redirected URL from Location property of the response header</span></span>

3.  <span data-ttu-id="d9437-433">Вызовите событие хранения POST еще раз с помощью URL-адреса перенаправления</span><span class="sxs-lookup"><span data-stu-id="d9437-433">Invoke the POST retention event call again using the redirected URL.</span></span>

## <a name="credits"></a><span data-ttu-id="d9437-434">Сведения об авторах</span><span class="sxs-lookup"><span data-stu-id="d9437-434">Credits</span></span>

<span data-ttu-id="d9437-435">Редактор статьи:</span><span class="sxs-lookup"><span data-stu-id="d9437-435">This topic was reviewed by:</span></span>

<span data-ttu-id="d9437-436">Antonio Maio</span><span class="sxs-lookup"><span data-stu-id="d9437-436">Antonio Maio</span></span><br/><span data-ttu-id="d9437-437">MVP в сфере приложений и служб Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="d9437-437">Microsoft Office Apps and Services MVP</span></span><br/> <span data-ttu-id="d9437-438">Antonio.Maio@Protiviti.com</span><span class="sxs-lookup"><span data-stu-id="d9437-438">Antonio.Maio@Protiviti.com</span></span>
