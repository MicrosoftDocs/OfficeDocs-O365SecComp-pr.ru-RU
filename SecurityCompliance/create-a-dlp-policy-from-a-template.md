---
title: Создание политики защиты от потери данных на основе шаблона
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.NewPolicyFromTemplate
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 59414438-99f5-488b-975c-5023f2254369
description: 'Простой, наиболее распространенные способ начать разработку политик защиты от потери данных — используйте одну из шаблоны, включенные в Office 365. '
ms.openlocfilehash: 4e3a5d731538e4998858b5f9f7a296c43e6774ac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534901"
---
# <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="7cc64-103">Создание политики защиты от потери данных на основе шаблона</span><span class="sxs-lookup"><span data-stu-id="7cc64-103">Create a DLP policy from a template</span></span>

<span data-ttu-id="7cc64-p101">Простой, наиболее распространенные способ начать разработку политик защиты от потери данных — используйте одну из шаблоны, включенные в Office 365. Можно использовать один из этих шаблонов или настроить правила в соответствии с конкретным требованиям вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p101">The easiest, most common way to get started with DLP policies is to use one of the templates included in Office 365. You can use one of these templates as is, or customize the rules to meet your organization's specific compliance requirements.</span></span>
  
<span data-ttu-id="7cc64-p102">Office 365 включает более 40 готовых к использованию шаблонов, которые могут помочь вам удовлетворить ряд распространенных нормативных требований и потребностей бизнес-политики. Например, имеются шаблоны политик защиты от потери данных для следующих документов:</span><span class="sxs-lookup"><span data-stu-id="7cc64-p102">Office 365 includes over 40 ready-to-use templates that can help you meet a wide range of common regulatory and business policy needs. For example, there are DLP policy templates for:</span></span>
  
- <span data-ttu-id="7cc64-108">Акт Грэмма-Лича-Блайли (Акт о модернизации финансовой системы 1999 г.)</span><span class="sxs-lookup"><span data-stu-id="7cc64-108">Gramm-Leach-Bliley Act (GLBA)</span></span>
    
- <span data-ttu-id="7cc64-109">Отраслевой стандарт защиты данных платежных карт (PCI-DSS)</span><span class="sxs-lookup"><span data-stu-id="7cc64-109">Payment Card Industry Data Security Standard (PCI-DSS)</span></span>
    
- <span data-ttu-id="7cc64-110">Законы США о защите персональных данных</span><span class="sxs-lookup"><span data-stu-id="7cc64-110">United States Personally Identifiable Information (U.S. PII)</span></span>
    
- <span data-ttu-id="7cc64-111">Закон США о медицинском страховании (HIPAA)</span><span class="sxs-lookup"><span data-stu-id="7cc64-111">United States Health Insurance Act (HIPAA)</span></span>
    
<span data-ttu-id="7cc64-p103">Вы можете настроить шаблон, изменив любое из существующих правил или добавив новое. Например, вы также можете добавить к правилу новые типы конфиденциальной информации, изменить в нем счетчики, чтобы его было сложнее или проще вызвать, позволить пользователям обходить действия в правиле, предоставив обоснование, или изменить адресатов уведомлений и отчетов об инцидентах. Шаблон политики защиты от потери данных — это отличная отправная точка для многих распространенных сценариев, связанных с соответствием требованиям.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p103">You can fine tune a template by modifying any of the existing rules or adding new ones. For example, you can add new types of sensitive information to a rule, modify the counts in a rule to make it harder or easier to trigger, allow people to override the actions in a rule by providing a business justification, or change who notifications and incident reports are sent to. A DLP policy template is a flexible starting point for many common compliance scenarios.</span></span>
  
<span data-ttu-id="7cc64-115">Вы также можете выбрать настраиваемый шаблон, который не содержит правил по умолчанию, и настроить политику защиты от потери данных с нуля в соответствии с конкретными требованиями организации.</span><span class="sxs-lookup"><span data-stu-id="7cc64-115">You can also choose the Custom template, which has no default rules, and configure your DLP policy from scratch, to meet the specific compliance requirements for your organization.</span></span>
  
## <a name="example-identify-sensitive-information-across-all-onedrive-for-business-sites-and-restrict-access-for-people-outside-your-organization"></a><span data-ttu-id="7cc64-116">Пример: Определение конфиденциальной информации по всем OneDrive для бизнеса сайтов и ограничения доступа для пользователей вне вашей организации</span><span class="sxs-lookup"><span data-stu-id="7cc64-116">Example: Identify sensitive information across all OneDrive for Business sites and restrict access for people outside your organization</span></span>

<span data-ttu-id="7cc64-p104">OneDrive для бизнеса учетные записи позволяют легко людей в организации для совместной работы и совместного использования документов. Однако общих вопросов о контролеры, что конфиденциальные данные, хранящиеся в OneDrive для бизнеса учетных записей может случайно совместно с людьми за пределами вашей организации. Политики защиты от потери данных, чтобы снизить риск.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p104">OneDrive for Business accounts make it easy for people across your organization to collaborate and share documents. But a common concern for compliance officers is that sensitive information stored in OneDrive for Business accounts may be inadvertently shared with people outside your organization. A DLP policy can help mitigate this risk.</span></span>
  
<span data-ttu-id="7cc64-p105">В этом примере вы создадите политики защиты от потери данных, которая идентифицирует США ЛИЧНЫХ данных, включая номера паспортов отдельных налогоплательщика идентификационного номера (ITIN), номера социального страхования и США. Вы будете начало работы с помощью шаблона и измените шаблон соответствия требованиям вашей организации, в частности, вы будете:</span><span class="sxs-lookup"><span data-stu-id="7cc64-p105">In this example, you'll create a DLP policy that identifies U.S. PII data, which includes Individual Taxpayer Identification Numbers (ITIN), Social Security Numbers, and U.S. passport numbers. You'll get started by using a template, and then you'll modify the template to meet your organization's compliance requirements—specifically, you'll:</span></span>
  
- <span data-ttu-id="7cc64-122">Добавить несколько типов конфиденциальной information—U.S. банковский счет и США драйвер лицензии номеров —, чтобы политики защиты от потери данных обеспечивает защиту еще больше конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="7cc64-122">Add a couple of types of sensitive information—U.S. bank account numbers and U.S. driver's license numbers—so that the DLP policy protects even more of your sensitive data.</span></span>
    
- <span data-ttu-id="7cc64-123">Сделайте более конфиденциальные политики, чтобы одно вхождение конфиденциальной информации, чтобы ограничить доступ для внешних пользователей.</span><span class="sxs-lookup"><span data-stu-id="7cc64-123">Make the policy more sensitive, so that a single occurrence of sensitive information is enough to restrict access for external users.</span></span>
    
- <span data-ttu-id="7cc64-p106">Пользователи могут переопределить действия, предоставляя бизнес-требований или отчетов Ложное срабатывание. Таким образом, политики защиты от потери данных не пользователи в вашей организации из выполнять свою работу, если они имеют допустимые бизнес причина общий доступ к конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p106">Allow users to override the actions by providing a business justification or reporting a false positive. This way, your DLP policy won't prevent people in your organization from getting their work done, provided they have a valid business reason for sharing the sensitive information.</span></span>
    
### <a name="create-a-dlp-policy-from-a-template"></a><span data-ttu-id="7cc64-126">Создание политики защиты от потери данных на основе шаблона</span><span class="sxs-lookup"><span data-stu-id="7cc64-126">Create a DLP policy from a template</span></span>

1. <span data-ttu-id="7cc64-127">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="7cc64-127">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="7cc64-p107">Войдите в Office 365 с помощью учетной записи рабочего или школы. Теперь вы безопасности Office 365 &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p107">Sign in to Office 365 using your work or school account. You're now in the Office 365 Security &amp; Compliance Center.</span></span>
    
3. <span data-ttu-id="7cc64-130">В разделе Безопасность &amp; центре соответствия требованиям \> слева навигации \> **защиту от потери данных** \> **политики** \> **+ Создать политику**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-130">In the Security &amp; Compliance Center \> left navigation \> **Data loss prevention** \> **Policy** \> **+ Create a policy**.</span></span>
    
    ![Создание кнопки политики](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. <span data-ttu-id="7cc64-132">Выберите шаблон политики защиты от потери данных, которая обеспечивает защиту типов конфиденциальной информации, которую нужно \> **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-132">Choose the DLP policy template that protects the types of sensitive information that you need \> **Next**.</span></span>
    
    <span data-ttu-id="7cc64-133">В этом примере будет предложено выбрать **конфиденциальности** \> **США раскрывающие личность обнаружены данные Сотрудников, обработанные данные** , так как он уже содержит большинство типов конфиденциальной информации, которую необходимо защитить — вы добавите несколько более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7cc64-133">In this example, you'll select **Privacy** \> **U.S. Personally Identifiable Information ‎(PII)‎ Data** because it already includes most of the types of sensitive information that you want to protect—you'll add a couple later.</span></span> 
    
    <span data-ttu-id="7cc64-134">При выборе шаблона можно прочитать описание справа, чтобы узнать защищает типов конфиденциальной информации шаблон.</span><span class="sxs-lookup"><span data-stu-id="7cc64-134">When you select a template, you can read the description on the right to learn what types of sensitive information the template protects.</span></span>
    
    ![Страница выбора шаблона политики защиты от потери данных](media/775266f6-ad87-4080-8d7c-97f2e7403b30.png)
  
5. <span data-ttu-id="7cc64-136">Имя политики \> **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-136">Name the policy \> **Next**.</span></span>
    
6. <span data-ttu-id="7cc64-137">Чтобы указать расположение, которые будут политику защиты от потери данных для защиты, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="7cc64-137">To choose the locations that you want the DLP policy to protect, do one of the following:</span></span>
    
  - <span data-ttu-id="7cc64-138">Выбор **всех расположений в Office 365** \> **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-138">Choose **All locations in Office 365** \> **Next**.</span></span>
    
  - <span data-ttu-id="7cc64-p108">Нажмите кнопку **выбрать определенные расположения** \> **Далее**. В этом примере выберите.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p108">Choose **Let me choose specific locations** \> **Next**. For this example, choose this.</span></span>
    
    <span data-ttu-id="7cc64-141">Для включения или исключения всего размещения, например всех сообщений электронной почты Exchange или все учетные записи OneDrive, переключите **состояние** эту папку включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="7cc64-141">To include or exclude an entire location such as all Exchange email or all OneDrive accounts, switch the **Status** of that location on or off.</span></span> 
    
    <span data-ttu-id="7cc64-p109">Чтобы включить только определенные сайты SharePoint или OneDrive для бизнеса учетных записей, переключитесь **состояние** и нажмите кнопку ссылки в разделе **Включить** для выбора определенных узлов или учетные записи. Применение политики к сайту, правил, настроенных в том, что политика автоматически применяется ко всем дочерним сайтам этого узла.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p109">To include only specific SharePoint sites or OneDrive for Business accounts, switch the **Status** to on, and then click the links under **Include** to choose specific sites or accounts. When you apply a policy to a site, the rules configured in that policy are automatically applied to all subsites of that site.</span></span> 
    
    ![Варианты расположений, к которым можно применить политику защиты от потери данных](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
    <span data-ttu-id="7cc64-145">В этом примере для защиты конфиденциальных данных, хранящиеся в все OneDrive для бизнеса учетных записей, отключить **состояние** для **электронной почты Exchange** и **сайтов SharePoint**и оставьте **состояние** на **OneDrive**учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7cc64-145">In this example, to protect sensitive information stored in all OneDrive for Business accounts, turn off the **Status** for both **Exchange email** and **SharePoint sites**, and leave the **Status** on for **OneDrive accounts**.</span></span>
    
7. <span data-ttu-id="7cc64-146">Выберите **Дополнительные параметры** \> **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-146">Choose **Use advanced settings** \> **Next**.</span></span>
    
8. <span data-ttu-id="7cc64-p110">Шаблон политики DLP содержит предопределенных правил с помощью условия и действия, которые обнаруживать и выполнения соответствующих определенных типов конфиденциальной информации. Можно изменить, удалить, или любые существующие правила или добавить новые. По завершении нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p110">A DLP policy template contains predefined rules with conditions and actions that detect and act upon specific types of sensitive information. You can edit, delete, or turn off any of the existing rules, or add new ones. When done, click **Next**.</span></span>
    
    ![Правила были развернуты в шаблоне политики PII "мне Нравится"](media/3bc9f1b6-f8ad-4334-863a-24448bb87687.png)
  
    <span data-ttu-id="7cc64-151">В этом примере шаблон США PII данных включает в себя два предопределенных правил:</span><span class="sxs-lookup"><span data-stu-id="7cc64-151">In this example, the U.S. PII Data template includes two predefined rules:</span></span>
    
  - <span data-ttu-id="7cc64-p111">**Низкий объем контента обнаружена PII США.** Это правило выполняет поиск файлов, содержащих от 1 до 10 вхождений каждого из трех типов конфиденциальной информации (ITIN, SSN и США номера паспортов), где общих файлов с людьми за пределами организации. Если найдено, правило отправляет уведомление по электронной почте главного администратора семейства сайтов, владелец документа и пользователя, который последним изменение в документ.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p111">**Low volume of content detected U.S. PII** This rule looks for files containing between 1 and 10 occurrences of each of three types of sensitive information (ITIN, SSN, and U.S. passport numbers), where the files are shared with people outside the organization. If found, the rule sends an email notification to the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
  - <span data-ttu-id="7cc64-p112">**Большой объем контента обнаружена PII США.** Это правило выполняет поиск файлов, содержащих 10 или более вхождений каждого же трех типов конфиденциальных данных, где общих файлов с людьми за пределами организации. Если найден, это действие также отправляет уведомление по электронной почте, а также ограничивает доступ к файлу. Контент в OneDrive для бизнеса учетная запись это означает, что разрешения для документа ограниченных для всех, кроме главного администратора семейства сайтов, владелец документа и человека, который последнего изменения документа.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p112">**High volume of content detected U.S. PII** This rule looks for files containing 10 or more occurrences of each of the same three sensitive information types, where the files are shared with people outside the organization. If found, this action also sends an email notification, plus it restricts access to the file. For content in a OneDrive for Business account, this means that permissions for the document are restricted for everyone except the primary site collection administrator, document owner, and person who last modified the document.</span></span> 
    
    <span data-ttu-id="7cc64-p113">Для соответствия требованиям вашей организации, можно упростить правила триггер, чтобы одно вхождение конфиденциальной информации, чтобы заблокировать доступ для внешних пользователей. После рассмотрения эти правила, вы понимаете, что нет необходимости правилами низкой и высокой count — требуется только одно правило, который блокирует доступ, если найдены все вхождения конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p113">To meet your organization's specific requirements, you may want to make the rules easier to trigger, so that a single occurrence of sensitive information is enough to block access for external users. After looking at these rules, you understand that you don't need low and high count rules—you need only a single rule that blocks access if any occurrence of sensitive information is found.</span></span>
    
    <span data-ttu-id="7cc64-159">Чтобы развернуть правило, с именем **низкой объем контента обнаружена PII США** \> **Удаление правила**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-159">So you expand the rule named **Low volume of content detected U.S. PII** \> **Delete rule**.</span></span>
    
    ![Правило кнопка "Удалить"](media/bc36f7d2-0fae-4af1-92e8-95ba51077b12.png)
  
9. <span data-ttu-id="7cc64-p114">Сейчас в этом примере вы требуются для добавления двух типов конфиденциальной информации (банка США учетной записи номера и номера лицензий драйвер США), позволяет сотрудникам переопределить правила и измените значение счетчика на любое вхождение. Можно сделать это путем редактирования одно правило, поэтому выберите значение **большой объем контента обнаружена PII США** \> **Изменить правило**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p114">Now, in this example, you need to add two sensitive information types (U.S. bank account numbers and U.S. driver's license numbers), allow people to override a rule, and change the count to any occurrence. You can do all of this by editing one rule, so select **High volume of content detected U.S. PII** \> **Edit rule**.</span></span>
    
    ![Правило кнопка "Изменить"](media/eaf54067-4945-4c98-8dd6-fb2c5d6de075.png)
  
10. <span data-ttu-id="7cc64-p115">Чтобы добавить тип конфиденциальных данных в разделе **условия** \> **типы добавить или изменить**. Затем в разделе **Добавление и изменение типов** \> последовательно выберите пункты **Добавить** \> выберите **Номер банковского счета в США** и **Номер водительского удостоверения США** \> **Добавить** \> **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p115">To add a sensitive information type, in the **Conditions** section \> **Add or change types**. Then, under **Add or change types** \> choose **Add** \> select **U.S. Bank Account Number** and **U.S. Driver's License Number** \> **Add** \> **Done**.</span></span>
    
    ![Параметр, чтобы добавить или изменить типы](media/c6c3ae86-f7db-40a8-a6e4-db11692024be.png)
  
    ![Добавление или изменение области типы](media/fdbb96af-b914-4a6c-a97b-bbd014689965.png)
  
11. <span data-ttu-id="7cc64-p116">Чтобы изменить count (число экземпляров конфиденциальные сведения, необходимые для запуска правила), в разделе **число экземпляров** \> выберите **минимальное** значение для каждого типа \> введите 1. Минимальное количество не может быть пустым. Максимальное число может быть пустым. пустой **Максимальное** значение преобразовать в **любой**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p116">To change the count (the number of instances of sensitive information required to trigger the rule), under **Instance count** \> choose the **min** value for each type \> enter 1. The minimum count cannot be empty. The maximum count can be empty; an empty **max** value convert to **any**.</span></span>
    
    <span data-ttu-id="7cc64-p117">По завершении минимальное количество для всех типов конфиденциальной информации должно быть **1** и максимального числа должен быть **любой**. Другими словами все вхождения этот тип конфиденциальных данных будет соответствовать это условие.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p117">When finished, the min count for all of the sensitive information types should be **1** and the max count should be **any**. In other words, any occurrence of this type of sensitive information will satisfy this condition.</span></span>
    
    ![Экземпляр счетчика для типов конфиденциальной информации](media/5c6e08cb-59a9-4558-b54b-d899836d4737.png)
  
12. <span data-ttu-id="7cc64-174">Для окончательного настройки вы не хотите политик защиты от потери данных для блокирования людей из их работу при имеет допустимый бизнес-требований или появиться Ложное срабатывание, поэтому уведомления пользователя включать параметры, чтобы переопределить блокирующая действие.</span><span class="sxs-lookup"><span data-stu-id="7cc64-174">For the final customization, you don't want your DLP policies to block people from doing their work when they have a valid business justification or encounter a false positive, so you want the user notification to include options to override the blocking action.</span></span>
    
    <span data-ttu-id="7cc64-175">В разделе **уведомления пользователя** можно видеть, что уведомления по электронной почте и советы по политикам включены по умолчанию для этого правила в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="7cc64-175">In the **User notifications** section, you can see that email notifications and policy tips are turned on by default for this rule in the template.</span></span> 
    
    <span data-ttu-id="7cc64-p118">В разделе **переопределяет пользователя** можно видеть, что включены переопределения для бизнес-требований, но не являются переопределений сообщение о ложных срабатываний. Выберите **Переопределить правила автоматически в том случае, если они отчета о ложном срабатывании**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p118">In the **User overrides** section, you can see that overrides for a business justification are turned on, but overrides to report false positives are not. Choose **Override the rule automatically if they report it as a false positive**.</span></span>
    
    ![Уведомления пользователей и разделов переопределений пользователя](media/62720e7a-a939-4c03-b414-67748f3d64a0.png)
  
13. <span data-ttu-id="7cc64-179">В верхней части редактора правила измените имя этого правила по умолчанию, **большой объем контента обнаружена PII США** на **любое содержимое, обнаруженных с помощью PII США.** так как теперь оно запускается все вхождения его типов конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="7cc64-179">At the top of the rule editor, change the name of this rule from the default **High volume of content detected U.S. PII** to **Any content detected with U.S. PII** because it's now triggered by any occurrence of its sensitive information types.</span></span> 
    
14. <span data-ttu-id="7cc64-180">В нижней части редактора правил \> **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-180">At the bottom of the rule editor \> **Save**.</span></span>
    
15. <span data-ttu-id="7cc64-181">Просмотрите условия и действия для этого правила \> **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-181">Review the conditions and actions for this rule \> **Next**.</span></span>
    
    <span data-ttu-id="7cc64-p119">В правой части окна Обратите внимание на то **состояние** переключения для правила. При выключении всей политики всех правил, содержащихся в политике также будут отключены. Тем не менее здесь можно отключить определенное правило без выключения всего политики. Это может быть полезен при необходимости для изучения правило, которое создает большое число ложных срабатываний.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p119">On the right, notice the **Status** switch for the rule. If you turn off an entire policy, all rules contained in the policy are also turned off. However, here you can turn off a specific rule without turning off the entire policy. This can be useful when you need to investigate a rule that is generating a large number of false positives.</span></span> 
    
16. <span data-ttu-id="7cc64-186">На следующей странице чтение знать следующее и затем выберите, следует ли включить правило или протестировать первоначального \> **Далее**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-186">On the next page, read and understand the following, and then choose whether to turn on the rule or test it out first \> **Next**.</span></span>
    
     <span data-ttu-id="7cc64-p120">Перед созданием политик защиты от потери данных можно использовать их в организации постепенно оценки их воздействия и проверка их эффективности перед их полностью соблюдение. Например не должен новую политику защиты от потери данных, чтобы случайно заблокируйте доступ к тысяч документов, которые требуют людей, чтобы выполнять свою работу.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p120">Before you create your DLP policies, you should consider rolling them out gradually to assess their impact and test their effectiveness before you fully enforce them. For example, you don't want a new DLP policy to unintentionally block access to thousands of documents that people require to get their work done.</span></span> 
    
    <span data-ttu-id="7cc64-189">Если вы создаете с большой потенциальном влиянии политик защиты от потери данных, рекомендуется использовать следующие этой последовательности:</span><span class="sxs-lookup"><span data-stu-id="7cc64-189">If you're creating DLP policies with a large potential impact, we recommend following this sequence:</span></span>
    
17. <span data-ttu-id="7cc64-p121">Начните работу в тестовом режиме без подсказок политики, а затем оцените влияние политики с помощью специальных отчетов. Для просмотра количества, расположения, типа и серьезности совпадений политики можно использовать отчеты политики защиты от потери данных. На основании результатов можно настроить правила согласно потребностям. В тестовом режиме политики защиты от потери данных не влияют на эффективность работы сотрудников вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p121">Start in test mode without Policy Tips and then use the DLP reports to assess the impact. You can use DLP reports to view the number, location, type, and severity of policy matches. Based on the results, you can fine tune the rules as needed. In test mode, DLP policies will not impact the productivity of people working in your organization.</span></span> 
    
18. <span data-ttu-id="7cc64-p122">Переключитесь в тестовый режим с уведомлениями и подсказками политики, чтобы начать знакомить пользователей с политиками соответствия требованиям вашей организации и подготовить их к введению новых правил. На этом этапе можно также попросить пользователей сообщать о ложных срабатываниях, чтобы сделать правила еще точнее.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p122">Move to Test mode with notifications and Policy Tips so that you can begin to teach users about your compliance policies and prepare them for the rules that are going to be applied. At this stage, you can also ask users to report false positives so that you can further refine the rules.</span></span>
    
19. <span data-ttu-id="7cc64-p123">Включение политики, чтобы принудительно применяются правила и содержимого защищенного. Следует проанализировать в отчетах защиты от потери данных и отчеты об инциденте или уведомления, чтобы убедиться в том, что результаты, который предполагается.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p123">Turn on the policies so that the rules are enforced and the content's protected. Continue to monitor the DLP reports and any incident reports or notifications to make sure that the results are what you intend.</span></span> 
    
    ![Параметры для использования режима тестирования и включения политики](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
20. <span data-ttu-id="7cc64-199">Проверьте параметры для этой политики \> выберите команду **Создать**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-199">Review your settings for this policy \> choose **Create**.</span></span>
    
<span data-ttu-id="7cc64-200">После создания и включите политику предотвращения потери данных, он будет развернут в любой источников контента, которые он содержит, таких как сайты SharePoint Online или OneDrive для бизнеса учетных записей, политики которого начинается автоматически применение его правил для этого содержимого.</span><span class="sxs-lookup"><span data-stu-id="7cc64-200">After you create and turn on a DLP policy, it's deployed to any content sources that it includes, such as SharePoint Online sites or OneDrive for Business accounts, where the policy begins automatically enforcing its rules on that content.</span></span>
  
## <a name="view-the-status-of-a-dlp-policy"></a><span data-ttu-id="7cc64-201">Просмотр состояния политики защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="7cc64-201">View the status of a DLP policy</span></span>

<span data-ttu-id="7cc64-p124">В любое время можно просмотреть состояние политик защиты от потери данных на странице " **Политика** " в разделе **Защита от потери данных** о безопасности &amp; центре соответствия требованиям. Здесь можно найти важные сведения, например ли успешно включен или отключен политику или ли политика находится в тестовом режиме.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p124">At any time, you can view the status of your DLP policies on the **Policy** page in the **Data loss prevention** section of the Security &amp; Compliance Center. Here you can find important information, such as whether a policy was successfully enabled or disabled, or whether the policy is in test mode.</span></span> 
  
<span data-ttu-id="7cc64-204">Ниже приведены различные состояния и их значение.</span><span class="sxs-lookup"><span data-stu-id="7cc64-204">Here are the different statuses and what they mean.</span></span>
  
|<span data-ttu-id="7cc64-205">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7cc64-205">**Status**</span></span>|<span data-ttu-id="7cc64-206">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cc64-206">**Explanation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7cc64-207">**Включение...**</span><span class="sxs-lookup"><span data-stu-id="7cc64-207">**Turning on…**</span></span> <br/> |<span data-ttu-id="7cc64-p125">Политика развертывается для источников содержимого, которые она включает. Она пока не применяется ко всем источникам.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p125">The policy is being deployed to the content sources that it includes. The policy is not yet enforced on all sources.</span></span>  <br/> |
|<span data-ttu-id="7cc64-210">**Тестирование с уведомлениями**</span><span class="sxs-lookup"><span data-stu-id="7cc64-210">**Testing, with notifications**</span></span> <br/> |<span data-ttu-id="7cc64-p126">Политика находится в тестовом режиме. Действия правила не выполняются, но совпадения политики собираются и их можно просмотреть с помощью отчетов защиты от потери данных. Уведомления о совпадениях политик отправляются указанным получателям.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p126">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="7cc64-214">**Тестирование без уведомлений**</span><span class="sxs-lookup"><span data-stu-id="7cc64-214">**Testing, without notifications**</span></span> <br/> |<span data-ttu-id="7cc64-p127">Политика находится в тестовом режиме. Действия правила не выполняются, но совпадения политики собираются и их можно просмотреть с помощью отчетов защиты от потери данных. Уведомления о совпадениях политик не отправляются указанным получателям.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p127">The policy is in test mode. The actions in a rule are not applied, but policy matches are collected and can be viewed by using the DLP reports. Notifications about policy matches are not sent to the specified recipients.</span></span>  <br/> |
|<span data-ttu-id="7cc64-218">**Включена**</span><span class="sxs-lookup"><span data-stu-id="7cc64-218">**On**</span></span> <br/> |<span data-ttu-id="7cc64-p128">Политика активна и применяется принудительно. Политика успешно развернута во всех источниках контента.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p128">The policy is active and enforced. The policy was successfully deployed to all its content sources.</span></span>  <br/> |
|<span data-ttu-id="7cc64-221">**Отключение...**</span><span class="sxs-lookup"><span data-stu-id="7cc64-221">**Turning off…**</span></span> <br/> |<span data-ttu-id="7cc64-p129">Политика удаляется из источников контента, которые она включает. Политика может оставаться активной и применяться к некоторым источникам. Отключение политики может занять до 45 минут.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p129">The policy is being removed from the content sources that it includes. The policy may still be active and enforced on some sources. Turning off a policy may take up to 45 minutes.</span></span>  <br/> |
|<span data-ttu-id="7cc64-225">**Отключена**</span><span class="sxs-lookup"><span data-stu-id="7cc64-225">**Off**</span></span> <br/> |<span data-ttu-id="7cc64-p130">Политика не активна и не применяется принудительно. Параметры политики (источники, ключевые слова, длительность, и т. д.) сохранены.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p130">The policy is not active and not enforced. The settings for the policy (sources, keywords, duration, etc) are saved.</span></span>  <br/> |
|<span data-ttu-id="7cc64-228">**Удаление...**</span><span class="sxs-lookup"><span data-stu-id="7cc64-228">**Deleting…**</span></span> <br/> |<span data-ttu-id="7cc64-p131">Выполняется удаление политики. Политика не активна и не применяется принудительно.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p131">The policy is in the process of being deleted. The policy is not active and not enforced.</span></span>  <br/> |
   
## <a name="turn-off-a-dlp-policy"></a><span data-ttu-id="7cc64-231">Отключение политики защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="7cc64-231">Turn off a DLP policy</span></span>

<span data-ttu-id="7cc64-p132">Можно изменить или отключить политику предотвращения потери данных в любое время. Отключение политики отключает все правила в политике.</span><span class="sxs-lookup"><span data-stu-id="7cc64-p132">You can edit or turn off a DLP policy at any time. Turning off a policy disables all of the rules in the policy.</span></span>
  
<span data-ttu-id="7cc64-234">Чтобы изменить или отключить политику предотвращения потери данных на странице **Политика** \> выберите политику \> **Изменение политики**.</span><span class="sxs-lookup"><span data-stu-id="7cc64-234">To edit or turn off a DLP policy, on the **Policy** page \> select the policy \> **Edit policy**.</span></span>
  
![Политика кнопка "Изменить"](media/ce319e92-0519-44fe-9507-45a409eaefe4.png)
  
<span data-ttu-id="7cc64-236">Кроме того можно отключить в каждом правиле по отдельности, редактирования политики и переключение отключено **состояние** этого правила, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="7cc64-236">In addition, you can turn off each rule individually by editing the policy and then toggling off the **Status** of that rule, as described above.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="7cc64-237">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="7cc64-237">More information</span></span>

- [<span data-ttu-id="7cc64-238">Обзор политик защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="7cc64-238">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="7cc64-239">Отправка уведомлений и отображение подсказок для политик защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="7cc64-239">Send notifications and show policy tips for DLP policies</span></span>](use-notifications-and-policy-tips.md)
    
- [<span data-ttu-id="7cc64-240">Создание политики защиты от потери данных для защиты документов с помощью FCI или других свойств</span><span class="sxs-lookup"><span data-stu-id="7cc64-240">Create a DLP policy to protect documents with FCI or other properties</span></span>](protect-documents-that-have-fci-or-other-properties.md)
    
- [<span data-ttu-id="7cc64-241">Что входит в шаблоны политик защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="7cc64-241">What the DLP policy templates include</span></span>](what-the-dlp-policy-templates-include.md)
    
- [<span data-ttu-id="7cc64-242">Перечень типов конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="7cc64-242">Sensitive information types inventory</span></span>](what-the-sensitive-information-types-look-for.md)
    

