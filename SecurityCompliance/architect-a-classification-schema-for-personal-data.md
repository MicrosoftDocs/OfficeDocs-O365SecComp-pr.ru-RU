---
title: Разработка архитектуры схемы классификации для персональных данных
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Strat_O365_Enterprise
- Ent_O365
- GDPR
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Определите, целесообразно ли вашей организации внедрять метки в рамках плана по соблюдению регламента GDPR.
ms.openlocfilehash: 4ec495d82a37742d1315673e2a7d089778cd52e4
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223538"
---
# <a name="architect-a-classification-schema-for-personal-data"></a><span data-ttu-id="e1ef8-103">Разработка архитектуры схемы классификации для персональных данных</span><span class="sxs-lookup"><span data-stu-id="e1ef8-103">Architect a classification schema for personal data</span></span>

<span data-ttu-id="e1ef8-p101">В предыдущих статьях из этой серии рассматривалось использование типов конфиденциальной информации для определения персональных данных, подпадающих под действие регламента GDPR. Типы конфиденциальной информации — это разновидность классификации. Возможно, вам понадобится только эта классификация. Тем не менее многие организации внедряют более широкую стратегию управления данными с использованием меток. Ознакомьтесь с этой статьей, чтобы решить, нужно ли вам внедрять метки в рамках своего плана по соблюдению регламента GDPR. Если вы примете это решение, воспользуйтесь инструкциями и примерами, приведенными в настоящей статье.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p101">Previous articles in this series focus on using sensitive information types to identify personal data that is subject to GDPR. Sensitive information types are a form of classification. This might be all the classification you need. However, many organizations implement a broader data governance strategy using labels. Use this topic to decide if you also want to implement labels as part of your GDPR plan. If you do, this topic provides some guidance and examples.</span></span>

<span data-ttu-id="e1ef8-p102">Примечание. Определение схемы классификации для организации и настройка политики, меток и условий требуют тщательного планирования и подготовки. Важно понимать, что за этот процесс не отвечает ваш ИТ-отдел. При разработке соответствующей схемы классификации и применения меток для данных вашей организации обязательно сотрудничайте со своим юридическим отделом и группой по обеспечению соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p102">Note: Defining a classification schema for an organization and configuring policies, labels, and conditions requires careful planning and preparation. It is important to realize that this is not an IT driven process. Be sure to work with your legal and compliance team to develop an appropriate classification and labeling schema for your organization’s data.</span></span>

## <a name="decide-if-you-are-using-labels-in-addition-to-sensitive-data-types"></a><span data-ttu-id="e1ef8-113">Принятие решения о целесообразности использования меток в дополнение к типам конфиденциальных данных</span><span class="sxs-lookup"><span data-stu-id="e1ef8-113">Decide if you are using labels in addition to sensitive data types</span></span>

<span data-ttu-id="e1ef8-p103">Вы можете воспользоваться одним из двух подходов к классификации персональных данных в Office 365. Любой из них можно применить для защиты данных в соответствии с регламентом GDPR. Если вы решили использовать для классификации только типы конфиденциальной информации, можете пропустить оставшуюся часть этой статьи.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p103">You can take one of two approaches for classification in Office 365 for personal information. Either of these can be used for GDPR protection. If decide to use only sensitive information types for classification, you can skip the rest of this topic.</span></span>

<span data-ttu-id="e1ef8-117">Выберите один из приведенных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-117">Choose one of the following options.</span></span>

### <a name="option-1-use-only-office-365-sensitive-information-types"></a><span data-ttu-id="e1ef8-118">Вариант 1. Использование только типов конфиденциальной информации Office 365</span><span class="sxs-lookup"><span data-stu-id="e1ef8-118">Option 1: Use only Office 365 sensitive information types</span></span>

-   <span data-ttu-id="e1ef8-119">Типы конфиденциальной информации целесообразно использовать для определения и защиты персональных данных, которые подпадают под действие регламента GDPR и других типов нормативных требований.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-119">Sensitive information types work well to identify and protect personal data subject to GDPR and other types of regulations.</span></span>

-   <span data-ttu-id="e1ef8-120">Этот вариант более простой, чем расширенный план по управлению данными с использованием меток.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-120">These are simpler to use if your organization doesn’t already have or plan to implement a broader data governance plan using labels.</span></span>

-   <span data-ttu-id="e1ef8-121">Типы конфиденциальной информации используются с правилами защиты от потери данных (как и метки Office).</span><span class="sxs-lookup"><span data-stu-id="e1ef8-121">These work with DLP rules (so do Office labels).</span></span>

-   <span data-ttu-id="e1ef8-122">В будущем их можно будет применять с Cloud App Security для обнаружения конфиденциальной информации в других приложениях SaaS.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-122">In the future these will work with Cloud App Security so you can detect sensitive information in other SaaS apps.</span></span>

### <a name="option-2-use-sensitive-information-types--office-labels"></a><span data-ttu-id="e1ef8-123">Вариант 2. Использование типов конфиденциальной информации и меток Office</span><span class="sxs-lookup"><span data-stu-id="e1ef8-123">Option 2: Use sensitive information types + Office labels</span></span>

-   <span data-ttu-id="e1ef8-124">Типы конфиденциальной информации — это необходимый компонент, так как они понадобятся для автоматического применения меток к персональным данным, подпадающим под действие регламента GDPR.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-124">You’ll need sensitive information types to automatically apply labels to personal data that is subject to GDPR, so these are a prerequisite.</span></span>

-   <span data-ttu-id="e1ef8-125">Метки Office позволяют включить персональные данные, на которые распространяется регламент GDPR, в расширенный план по управлению данными для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-125">Using Office labels allows you to include personal data that is subject to GDPR into a broader data governance plan for your organization.</span></span>

-   <span data-ttu-id="e1ef8-126">В будущем метки Office будут объединены с метками Azure Information Protection для создания единой подсистемы классификации и применения меток.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-126">Later, Office labels will converge with Azure Information Protection labels into a unified classification and labeling engine.</span></span>

## <a name="develop-a-label-schema-that-includes-personal-data"></a><span data-ttu-id="e1ef8-127">Разработка схемы меток, включающей персональные данные</span><span class="sxs-lookup"><span data-stu-id="e1ef8-127">Develop a label schema that includes personal data</span></span>

<span data-ttu-id="e1ef8-p104">Прежде чем воспользоваться техническими возможностями для применения меток и защиты, сначала определите схему классификации для своей организации. Возможно, у нее уже имеется схема классификации, что упрощает добавление персональных данных. В этой статье приведен пример схемы классификации. При необходимости вы можете использовать его в качестве отправной точки.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p104">Before using technical capabilities to apply labels and protection, first work across your organization to define a classification schema. Your organization might already have a classification schema, which makes it easier to add personal data. This topic includes an example classification schema. You can use this as a starting point, if needed.</span></span>

### <a name="getting-started"></a><span data-ttu-id="e1ef8-132">Начало работы</span><span class="sxs-lookup"><span data-stu-id="e1ef8-132">Getting started</span></span>

<span data-ttu-id="e1ef8-p105">Сначала выберите количество и имена меток, которые необходимо внедрить. При этом не беспокойтесь об используемых технологиях и способах применения меток. Примените эту схему в пределах всей организации, в том числе к данным, которые хранятся в локальной среде и других облачных службах.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p105">Begin by deciding on the number and names of labels to implement. Do this activity without worrying about which technology to use and how labels will be applied. Apply this schema universally throughout your organization, including data that resides on premises and in other cloud services.</span></span>

### <a name="recommendations"></a><span data-ttu-id="e1ef8-136">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="e1ef8-136">Recommendations</span></span> 

<span data-ttu-id="e1ef8-137">Разрабатывая и внедряя политики, метки и условия, руководствуйтесь вот какими рекомендациями.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-137">When designing and implementing policies, labels and conditions, consider following these recommendations:</span></span>

-   <span data-ttu-id="e1ef8-p106">Используйте имеющуюся схему классификации (при наличии). Многие организации уже пользуются определенными разновидностями классификации данных. Тщательно проанализируйте имеющуюся схему меток и по возможности используйте ее без изменений. Использование знакомых пользователя меток повысит эффективность их принятия.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p106">Use existing classification schema (if any) — Many organizations already are using data classification in some form. Carefully evaluate the existing label schema and if possible use it as is. Using familiar labels that are recognizable to the end-user will drive adoption.</span></span>

-   <span data-ttu-id="e1ef8-p107">В начале используйте стандартные политики и метки. Все решения поставляются с набором предопределенных политик и меток. Тщательно оцените, насколько они соответствуют вашим юридическим и бизнес-требованиям, и по возможности используйте именно их, а не создавайте новые.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p107">Start with default policies and labels — All solutions come with a set of predefined policies and labels. Carefully evaluate these against the organizations legal and business requirements and consider using them instead of creating new ones.</span></span>

-   <span data-ttu-id="e1ef8-p108">Начните с малого. Вы можете создать практически неограниченное количество меток. Тем не менее большое число основных и вложенных меток отрицательно скажется на их принятии. Слишком много вариантов выбора часто приводят к невозможности выбора.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p108">Start small — There is virtually no limit to the number of labels that can be created. However, large numbers of labels and sub-labels will negatively impact the adoption. Too many choices often means no choice at all.</span></span>

-   <span data-ttu-id="e1ef8-146">Применяйте сценарии и варианты использования. Определите варианты использования, характерные для организации и созданные на основе регламента GDPR, чтобы проверить, будет ли предполагаемая конфигурация применения меток и классификации работать на практике.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-146">Use scenarios and use cases — Identify common use cases within the organization and use scenarios derived from the GDPR to verify if the envisioned label and classification configuration will work in practice.</span></span>

-   <span data-ttu-id="e1ef8-p109">Определите целесообразность использования новой метки в каждом запросе. Действительно ли нужна новая метка для каждого сценария или варианта использования, либо достаточно ли воспользоваться уже имеющейся меткой? Сведите количество меток к минимуму, чтобы улучшить их принятие.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p109">Question every request for a new label, does every scenario or use case really need a new label or can we use what we already have? Keeping the number of labels to a minimum improves adoption.</span></span>

-   <span data-ttu-id="e1ef8-p110">Используйте вложенные метки для ключевых отделов. Некоторые отделы отличаются особыми требованиями, для которых требуются особенные метки. Определите эти метки в качестве вложенных меток. Кроме того, рассмотрите возможность использования политик с областью действия, которые применяются к группам пользователей, а не ко всей организации.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p110">Use sub-labels for key departments, some departments will have specific needs that require specific labels. Define these labels as sub-labels to an existing label and consider using scoped policies that are assigned to user groups instead of globally.</span></span>

-   <span data-ttu-id="e1ef8-p111">Рассмотрите возможность использования политик с областью действия. Политики, нацеленные на определенные подмножества пользователей, предотвращают чрезмерное количество меток. Политика с областью действия позволяет назначить роль или относящиеся к конкретному отделу метки (в том числе вложенные) сотрудникам, которые работают именно в этом отделе.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p111">Consider scoped policies, polices targeted at subsets of users will prevent "label overload". A scoped policy enables assigning role or department specific (sub-)labels to just employees that work for that specific department.</span></span>

-   <span data-ttu-id="e1ef8-p112">Используйте понятные имена меток. В качестве имен меток не рекомендуется использовать жаргонные слова, стандартные сокращения или акронимы. Целесообразно использовать понятные пользователям имена, чтобы улучшить принятие меток. Например, вместо таких меток, как PII, PCI, HIPAA, LBI, MBI и HBI, используйте имена типа "Не бизнес-данные", "Общедоступные", "Общие", "Конфиденциально" и "Строго конфиденциально".</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p112">Use meaningful label names, it is recommended not to use jargon, standards or acronyms as label names. Try to use names that resonate with the end user to improve adoption. Instead of using labels like PII, PCI, HIPAA, LBI, MBI and HBI consider names like Non-Business, Public, General, Confidential and Highly Confidential.</span></span>

### <a name="example-classification-schema"></a><span data-ttu-id="e1ef8-156">Пример схемы классификации</span><span class="sxs-lookup"><span data-stu-id="e1ef8-156">Example classification schema</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1ef8-157"><strong>Имя метки</strong></span><span class="sxs-lookup"><span data-stu-id="e1ef8-157"><strong>Label name</strong></span></span></th>
<th align="left"><span data-ttu-id="e1ef8-158"><strong>Описание</strong></span><span class="sxs-lookup"><span data-stu-id="e1ef8-158"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-159">Персональные</span><span class="sxs-lookup"><span data-stu-id="e1ef8-159">Personal</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-160">Не бизнес-данные, предназначенные только для личного использования.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-160">Non-business data, for personal use only.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e1ef8-161">Общедоступные</span><span class="sxs-lookup"><span data-stu-id="e1ef8-161">Public</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-162">Бизнес-данные, специально подготовленные и утвержденные для предоставления широкой публике.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-162">Business data that is specifically prepared and approved for public consumption.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-163">Данные клиента</span><span class="sxs-lookup"><span data-stu-id="e1ef8-163">Customer data</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-p113">Бизнес-данные, содержащие личные сведения, например номера кредитных карт, банковских счетов и социального страхования.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p113">Business data that contains personal identifiable information. Examples are credit card numbers, bank account numbers, and social security numbers.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e1ef8-166">Данные о персонале</span><span class="sxs-lookup"><span data-stu-id="e1ef8-166">HR data</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-167">Данные отдела кадров о сотрудниках Contoso, например номер сотрудника и сведения о зарплате.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-167">Human Resource data about Contoso employees, such as employee number and salary data.</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-168">Конфиденциально</span><span class="sxs-lookup"><span data-stu-id="e1ef8-168">Confidential</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-p114">Конфиденциальные бизнес-данные, предоставление которых не тем людям может нанести ущерб организации. Примеры: контракты, отчеты системы безопасности, прогнозные сводки и данные о продажах клиентам.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p114">Sensitive business data that could cause damage to the business if shared with unauthorized people. Examples include contracts, security reports, forecast summaries, and sales account data.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e1ef8-171">Строго конфиденциально</span><span class="sxs-lookup"><span data-stu-id="e1ef8-171">Highly confidential</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-p115">Строго конфиденциальные бизнес-данные, предоставление которых не тем людям может нанести ущерб организации. Примеры: информация о сотрудниках и клиентах, пароли, исходный код и финансовые отчеты, о которых объявляется заранее.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p115">Very sensitive business data that would cause damage to the business if it was shared with unauthorized people. Examples include employee and customer information, passwords, source code, and pre-announced financial reports.</span></span></td>
</tr>
</tbody>
</table>

## <a name="define-a-taxonomy-and-search-criteria-for-each-label"></a><span data-ttu-id="e1ef8-174">Определение таксономии и условий поиска для каждой метки</span><span class="sxs-lookup"><span data-stu-id="e1ef8-174">Define a taxonomy and search criteria for each label</span></span>

<span data-ttu-id="e1ef8-p116">Следующий шаг после разработки схемы классификации для вашей организации — разработать таксономию и условия поиска этих данных. Вы уже выполнили эти задачи для персональных данных, определив типы конфиденциальной информации, а также настроив или создав новые типы конфиденциальной информации для своей среды.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p116">After developing a classification schema for your organization, the next step is to develop the taxonomy and search criteria for finding this data. For personal data, you’ve already completed this work by identifying sensitive information types and also by customizing or creating new sensitive information types for your environment.</span></span>

<span data-ttu-id="e1ef8-p117">В таблице ниже приведен пример схемы, таксономии и условий поиска для организации. Метки упорядочены по уровню конфиденциальности от наименее до наиболее конфиденциальных, чтобы гарантировать назначение правильной метки данным, которые соответствуют нескольким условиям метки.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-p117">The following table provides an example schema, taxonomy, and search criteria for an organization. The labels are ordered by sensitivity level from least sensitive to most sensitive to ensure that data that matches multiple label conditions is assigned the appropriate label.</span></span>

<span data-ttu-id="e1ef8-179">Примечание. Этот пример конфигурации приведен исключительно для иллюстрации и не предназначен для использования в качестве руководства или справки по развертыванию.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-179">Note: The configuration example is provided for illustration only and is not intended as deployment guidance or reference.</span></span>

<span data-ttu-id="e1ef8-180">Крайне важно убедиться, что ваши действия по классификации персональных данных для соответствия требованиям регламента GDPR сочетаются с целями всей организации.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-180">The important takeaway is to ensure that the work you invest to classify personal data for GDPR compliance fits together with the objectives for your entire organization.</span></span>

### <a name="example-schema-taxonomy-and-search-criteria"></a><span data-ttu-id="e1ef8-181">Пример схемы, таксономии и условий поиска</span><span class="sxs-lookup"><span data-stu-id="e1ef8-181">Example schema, taxonomy, and search criteria</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1ef8-182"><strong>Метка</strong></span><span class="sxs-lookup"><span data-stu-id="e1ef8-182"><strong>Label</strong></span></span></th>
<th align="left"><span data-ttu-id="e1ef8-183"><strong>Таксономия</strong></span><span class="sxs-lookup"><span data-stu-id="e1ef8-183"><strong>Taxonomy</strong></span></span></th>
<th align="left"><span data-ttu-id="e1ef8-184"><strong>Метод</strong></span><span class="sxs-lookup"><span data-stu-id="e1ef8-184"><strong>Method</strong></span></span></th>
<th align="left"><span data-ttu-id="e1ef8-185"><strong>Синтаксис поиска</strong></span><span class="sxs-lookup"><span data-stu-id="e1ef8-185"><strong>Search syntax</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-186">Персональные</span><span class="sxs-lookup"><span data-stu-id="e1ef8-186">Personal</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-187">Документы, к которым пользователь вручную применил метку как к персональным.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-187">Documents manually labelled personal by the end user.</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-188">Вручную</span><span class="sxs-lookup"><span data-stu-id="e1ef8-188">Manual</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-189">Документы, к которым пользователь вручную применил метку как к персональным.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-189">Documents manually labelled personal by the end user.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e1ef8-190">Общедоступные</span><span class="sxs-lookup"><span data-stu-id="e1ef8-190">Public</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-191">Документы, содержащие фразу Approved for Public Release ##/#### (без учета регистра), где # представляет собой любую цифру.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-191">Documents containing the case insensitive phrase Approved for Public Release ##/#### where # represents any digit.</span></span></td>
<td align="left"><p><span data-ttu-id="e1ef8-192">KQL</span><span class="sxs-lookup"><span data-stu-id="e1ef8-192">KQL</span></span></p>
<p><span data-ttu-id="e1ef8-193">Регулярное выражение</span><span class="sxs-lookup"><span data-stu-id="e1ef8-193">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1ef8-194">KQL — Approved for Public Release (Утверждено для общедоступного выпуска)\*</span><span class="sxs-lookup"><span data-stu-id="e1ef8-194">KQL — Approved for Public Release\*</span></span></p>
<p><span data-ttu-id="e1ef8-195">Регулярное выражение — (?i)(\bApproved for Public Release \d{2}\/\d{4}\b)</span><span class="sxs-lookup"><span data-stu-id="e1ef8-195">RegEx — (?i)(\bApproved for Public Release \d{2}\/\d{4}\b)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-196">Данные клиента</span><span class="sxs-lookup"><span data-stu-id="e1ef8-196">Customer data</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-197">Типы конфиденциальной информации о гражданах стран ЕС.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-197">Sensitive information types for EU citizen data.</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-198">Типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="e1ef8-198">Sensitive information types</span></span></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e1ef8-199">Управление персоналом — данные о сотрудниках</span><span class="sxs-lookup"><span data-stu-id="e1ef8-199">Human Resources — Employee Data</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-200">Документы, включающие идентификатор сотрудника (с учетом регистра) в формате CONTOSO-9#####, где # представляет собой любую цифру.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-200">Documents that include the case sensitive employee id in the format CONTOSO-9##### where # represents any digit.</span></span></td>
<td align="left"><p><span data-ttu-id="e1ef8-201">KQL</span><span class="sxs-lookup"><span data-stu-id="e1ef8-201">KQL</span></span></p>
<p><span data-ttu-id="e1ef8-202">Регулярное выражение</span><span class="sxs-lookup"><span data-stu-id="e1ef8-202">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1ef8-203">KQL — CONTOSO-9\*</span><span class="sxs-lookup"><span data-stu-id="e1ef8-203">KQL — CONTOSO-9\*</span></span></p>
<p><span data-ttu-id="e1ef8-204">Регулярное выражение — (\bCONTOSO-9\d{5}\b)</span><span class="sxs-lookup"><span data-stu-id="e1ef8-204">RegEx — (\bCONTOSO-9\d{5}\b)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-205">Отдел кадров — данные о зарплате</span><span class="sxs-lookup"><span data-stu-id="e1ef8-205">Human Resources — Salary Data</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-206">Документы, включающие ключевое слово (без учета регистра) Contoso и ключевое слово (без учета регистра) Salary или Compensation</span><span class="sxs-lookup"><span data-stu-id="e1ef8-206">Documents that include the keyword (not case sensitive) Contoso AND either keyword (not case sensitive) Salary OR Compensation</span></span></td>
<td align="left"><p><span data-ttu-id="e1ef8-207">KQL</span><span class="sxs-lookup"><span data-stu-id="e1ef8-207">KQL</span></span></p>
<p><span data-ttu-id="e1ef8-208">Регулярное выражение</span><span class="sxs-lookup"><span data-stu-id="e1ef8-208">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1ef8-209">KQL — Contoso AND (Salary OR Compensation)</span><span class="sxs-lookup"><span data-stu-id="e1ef8-209">KQL — Contoso AND (Salary OR Compensation)</span></span></p>
<p><span data-ttu-id="e1ef8-210">Регулярное выражение — (\bCONTOSO-9\d{5}\b)</span><span class="sxs-lookup"><span data-stu-id="e1ef8-210">RegEx — (\bCONTOSO-9\d{5}\b)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e1ef8-211">Конфиденциально</span><span class="sxs-lookup"><span data-stu-id="e1ef8-211">Confidential</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-212">Документы, содержащие фразу Contoso Confidential (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="e1ef8-212">Documents containing the phrase (not case sensitive) Contoso Confidential.</span></span></td>
<td align="left"><p><span data-ttu-id="e1ef8-213">KQL</span><span class="sxs-lookup"><span data-stu-id="e1ef8-213">KQL</span></span></p>
<p><span data-ttu-id="e1ef8-214">Регулярное выражение</span><span class="sxs-lookup"><span data-stu-id="e1ef8-214">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1ef8-215">KQL — Contoso Confidential</span><span class="sxs-lookup"><span data-stu-id="e1ef8-215">KQL — Contoso Confidential</span></span></p>
<p><span data-ttu-id="e1ef8-216">Регулярное выражение — (?i)(\bContoso Confidential\b)</span><span class="sxs-lookup"><span data-stu-id="e1ef8-216">RegEx — (?i)(\bContoso Confidential\b)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e1ef8-217">Строго конфиденциально</span><span class="sxs-lookup"><span data-stu-id="e1ef8-217">Highly confidential</span></span></td>
<td align="left"><span data-ttu-id="e1ef8-218">Документы, содержащие фразу (с учетом регистра) Contoso Secret или Secret-C####, где # представляет собой любую цифру.</span><span class="sxs-lookup"><span data-stu-id="e1ef8-218">Documents that include either pharase (case sensitive) Contoso Secret or Secret-C#### where # represents any digit.</span></span></td>
<td align="left"><p><span data-ttu-id="e1ef8-219">KQL</span><span class="sxs-lookup"><span data-stu-id="e1ef8-219">KQL</span></span></p>
<p><span data-ttu-id="e1ef8-220">Регулярное выражение</span><span class="sxs-lookup"><span data-stu-id="e1ef8-220">RegEx</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1ef8-221">KQL — Contoso Secret OR Secret-C\*</span><span class="sxs-lookup"><span data-stu-id="e1ef8-221">KQL — Contoso Secret OR Secret-C\*</span></span></p>
<p><span data-ttu-id="e1ef8-222">Регулярное выражение — (?i)(\bContoso Secret\b)|(\bSecret-C\d{4}\b)</span><span class="sxs-lookup"><span data-stu-id="e1ef8-222">RegEx — (?i)(\bContoso Secret\b)|(\bSecret-C\d{4}\b)</span></span></p></td>
</tr>
</tbody>
</table>
