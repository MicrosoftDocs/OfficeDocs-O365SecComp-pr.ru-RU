---
title: Автоматическое применение метки конфиденциальности к содержимому
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
description: При создании метки конфиденциальности ее можно автоматически назначить документу или сообщению электронной почты или можно предложить пользователям выбрать рекомендованную метку.
ms.openlocfilehash: 3009056989b0cc26f8b2c76db4318042ce470482
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214846"
---
# <a name="apply-a-sensitivity-label-to-content-automatically"></a><span data-ttu-id="efe37-103">Автоматическое применение метки конфиденциальности к содержимому</span><span class="sxs-lookup"><span data-stu-id="efe37-103">Apply a sensitivity label to content automatically</span></span>

<span data-ttu-id="efe37-104">При создании метки конфиденциальности ее можно автоматически назначить содержимому с конфиденциальной информацией или можно предложить пользователям применить рекомендованную метку.</span><span class="sxs-lookup"><span data-stu-id="efe37-104">When you create a sensitivity label, you can automatically assign that label to content containing sensitive information, or you can prompt users to apply the label that you recommend.</span></span>

<span data-ttu-id="efe37-105">Возможность автоматически применять метки конфиденциальности к содержимому важна, потому что:</span><span class="sxs-lookup"><span data-stu-id="efe37-105">The ability to apply sensitivity labels to content automatically is important because:</span></span>

- <span data-ttu-id="efe37-106">вам не придется обучать пользователей работе со всеми категориями;</span><span class="sxs-lookup"><span data-stu-id="efe37-106">You don't need to train your users on all of your classifications.</span></span>

- <span data-ttu-id="efe37-107">вам не нужно будет рассчитывать на то, что пользователи правильно классифицируют все содержимое;</span><span class="sxs-lookup"><span data-stu-id="efe37-107">You don't need to rely on users to classify all content correctly.</span></span>

- <span data-ttu-id="efe37-108">пользователям больше не нужно будет знать о ваших политиках — они могут сосредоточиться на своей работе.</span><span class="sxs-lookup"><span data-stu-id="efe37-108">Users no longer need to know about your policies - they can instead focus on their work.</span></span>

> [!NOTE]
> <span data-ttu-id="efe37-p101">Чтобы использовать возможность автоматического применения меток требуется подписка Azure Information Protection P2. Также для этого необходимо [скачать и установить унифицированный клиент присвоения меток Azure Information Protection](https://docs.microsoft.com/ru-RU/azure/information-protection/rms-client/install-unifiedlabelingclient-app). Мы работаем над встроенной поддержкой этой возможности в приложениях Office, чтобы можно было обойтись без унифицированного клиента присвоения меток Azure Information Protection. Кроме того, этот клиент работает только в Windows, поэтому такая возможность пока не поддерживается в Mac, iOS и Android.</span><span class="sxs-lookup"><span data-stu-id="efe37-p101">The capability to apply labels automatically requires an Azure Information Protection P2 subscription. To use this feature, you must [Download and install the Azure Information Protection unified labeling client](https://docs.microsoft.com/ru-RU/azure/information-protection/rms-client/install-unifiedlabelingclient-app). We're working on native support for this feature in Office apps, so that it won't require the Azure Information Protection unified labeling client. Also, the unified labeling client runs only on Windows, so this feature is not yet supported on Mac, iOS, and Android.</span></span>

![Параметры автоматического присвоения меток конфиденциальности](media/Sensitivity_labels_Auto_labeling_options.png)

## <a name="apply-a-sensitivity-label-automatically-based-on-conditions"></a><span data-ttu-id="efe37-114">Автоматическое присвоение меток конфиденциальности в соответствии с условиями</span><span class="sxs-lookup"><span data-stu-id="efe37-114">Apply a sensitivity label automatically based on conditions</span></span>

<span data-ttu-id="efe37-p102">Одна из самых полезных функций меток конфиденциальности — возможность автоматически применять их к содержимому, соответствующему определенным условиям. В этом случае пользователям в организации не требуется применять метки конфиденциальности — Office 365 делает это за них.</span><span class="sxs-lookup"><span data-stu-id="efe37-p102">One of the most powerful features of sensitivity labels is the ability to apply them automatically to content that matches certain conditions. In this case, people in your organization don't need to apply the sensitivity labels - Office 365 does the work for them.</span></span>
   
<span data-ttu-id="efe37-p103">Вы можете настроить автоматическое применение меток конфиденциальности к содержимому, которое содержит определенные типы конфиденциальной информации. При настройке меток конфиденциальности, которые будут применяться, отображается тот же список типов конфиденциальной информации, что и при создании политики защиты от потери данных. Поэтому вы можете, например, применить метку "Строго конфиденциально" к любому содержимому с персональными данными клиента, такими как номера кредитных карт или номера социального страхования.</span><span class="sxs-lookup"><span data-stu-id="efe37-p103">You can choose to apply sensitivity labels to content automatically when that content contains specific types of sensitive information. When you configure a sensitivity label to be applied automatically, you see the same list of sensitive information types as when you create a data loss prevention (DLP) policy. So you can, for example, automatically apply a Highly Confidential label to any content that contains customers' personally identifiable information (PII), such as credit card numbers or social security numbers.</span></span> 

![Параметры количества экземпляров и точности совпадения](media/Sensitivity_labels_instance_count_match_accuracy.png)

<span data-ttu-id="efe37-p104">После выбора типов конфиденциальной информации вы можете уточнить условия, изменив количество экземпляров или точность совпадения. Дополнительные сведения см. в разделе "Настройка правил для упрощения или усложнения сопоставления" [этой статьи](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span><span class="sxs-lookup"><span data-stu-id="efe37-p104">After you choose your sensitive informaton types, you can refine your condition by changing the instance count or match accuracy. For more information, see [Tuning rules to make them easier or harder to match](data-loss-prevention-policies.md#tuning-rules-to-make-them-easier-or-harder-to-match).</span></span>

<span data-ttu-id="efe37-p105">Более того, можно задать условие, чтобы определялись все типы конфиденциальной информации или только один из них. Чтобы условия были более гибкими или сложными, можно добавлять группы и использовать логические операторы в отношении групп. Дополнительные сведения см. в разделе "Группировка и логические операторы" [этой статьи](data-loss-prevention-policies.md#grouping-and-logical-operators).</span><span class="sxs-lookup"><span data-stu-id="efe37-p105">Further, you can choose whether a condition must detect all of the sensitive infromation types, or just one of them. And to make your conditions more flexible or complex, you can add groups and use logical operators between the groups. For more information, see [Grouping and logical operators](data-loss-prevention-policies.md#grouping-and-logical-operators).</span></span>

<span data-ttu-id="efe37-p106">Если метка конфиденциальности применяется автоматически, пользователь видит соответствующее уведомление в своем приложении Office. Он может нажать кнопку **ОК**, чтобы закрыть уведомление.</span><span class="sxs-lookup"><span data-stu-id="efe37-p106">When a sensitivity label is automatically applied, the user sees a notification in their Office app. They can choose **OK** to dismiss the notification.</span></span>

![Уведомление о том, что к документу автоматически применена метка](media/sensitivity_labels_msg_doc_was_auto_labeled.PNG)

## <a name="recommend-that-the-user-apply-a-sensitivity-label"></a><span data-ttu-id="efe37-129">Рекомендация пользователю о применении метки конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="efe37-129">Recommend that the user apply a sensitivity label</span></span>

<span data-ttu-id="efe37-p107">Если нужно, вместо автоматического применения метки к содержимому можно рекомендовать пользователю применить метку. Этот вариант дает пользователям возможность принять классификацию и соответствующую защиту или отклонить рекомендацию, если метка не подходит для документа или сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="efe37-p107">If you prefer, instead of applying a sensitivity label automatically to content, you can recommend to your users that they apply the label. This option provides your users the flexibility of accepting the classification and any associated protection, or dismissing the recommendation if the label is not suitable for their document or email.</span></span>

<span data-ttu-id="efe37-p108">Обратите внимание, что рекомендация меток поддерживается только в Word, PowerPoint и Excel (также требуется установка унифицированного клиента присвоения меток Azure Information Protection). Мы работаем над поддержкой рекомендации меток в Outlook.</span><span class="sxs-lookup"><span data-stu-id="efe37-p108">Note that recommended labels are supported in Word, PowerPoint, and Excel (and require that the Azure Information Proteciton unified labeling client is installed). We're working on support for recommended labels in Outlook.</span></span>

![Параметр для рекомендации метки конфиденциальности пользователям](media/Sensitivity_labels_Recommended_label_option.png)

<span data-ttu-id="efe37-p109">Ниже представлен пример рекомендации о применении метки с пользовательской подсказкой о политике, которая отображается во время настройки условия. Вы можете указать текст, отображаемый в подсказке о политике.</span><span class="sxs-lookup"><span data-stu-id="efe37-p109">Here's an example of a prompt when you configure a condition to apply a label as a recommended action, with a custom policy tip. You can choose what text is displayed in the policy tip.</span></span>

![Предложение применить рекомендованную метку](media/Sensitivity_label_Prompt_for_required_label.png)

## <a name="how-automatic-or-recommended-labels-are-applied"></a><span data-ttu-id="efe37-138">Применение автоматических или рекомендованных меток</span><span class="sxs-lookup"><span data-stu-id="efe37-138">How automatic or recommended labels are applied</span></span>

- <span data-ttu-id="efe37-p110">Автоматическое применение меток используется в Word, Excel и PowerPoint, когда сохраняются документы, и в Outlook, когда отправляются сообщения электронной почты. Настраиваемые условия могут определять конфиденциальную информацию в тексте документов и сообщений, верхних и нижних колонтитулах, но не в строке темы или вложениях к сообщениям.</span><span class="sxs-lookup"><span data-stu-id="efe37-p110">Automatic labeling applies to Word, Excel, and PowerPoint when documents are saved, and to Outlook when emails are sent. These conditions detect sensitive information in the body text in documents and emails, and to headers and footers -- but not in the subject line or attachments of email.</span></span>

- <span data-ttu-id="efe37-p111">Вы не можете использовать автоматическую классификацию для документов и сообщений электронной почты, которые ранее были отмечены вручную или которым ранее была присвоена метка классификации более высокого уровня. Помните, что к документу или сообщению можно применить только одну метку конфиденциальности (в дополнение к одной метке хранения).</span><span class="sxs-lookup"><span data-stu-id="efe37-p111">You cannot use automatic classification for documents and emails that were previously manually labeled, or previously automatically labeled with a higher classification. Remember, a document or email can have only a single sensitivity label applied to it (in addition to a single retention label).</span></span>

- <span data-ttu-id="efe37-p112">Рекомендованная классификация применяется в Word, Excel и PowerPoint при сохранении документов. Мы работаем над поддержкой присвоения рекомендованных меток в Outlook.</span><span class="sxs-lookup"><span data-stu-id="efe37-p112">Recommended classification applies to Word, Excel, and PowerPoint when documents are saved. We're working on support for recommended labeling in Outlook.</span></span>

- <span data-ttu-id="efe37-p113">Нельзя использовать рекомендованную классификацию для документов, которым ранее была присвоена метка классификации более высокого уровня. В таких случаях для содержимого с меткой классификации более высокого уровня пользователю не отображается рекомендация с подсказкой о политике.</span><span class="sxs-lookup"><span data-stu-id="efe37-p113">You cannot use recommended classification for documents that were previously labeled with a higher classification. In this case, when the content's already labeled with a higher classification, the user won't see the prompt with the recommendation and policy tip.</span></span>

## <a name="how-multiple-conditions-are-evaluated-when-they-apply-to-more-than-one-label"></a><span data-ttu-id="efe37-147">Оценка нескольких условий для нескольких меток</span><span class="sxs-lookup"><span data-stu-id="efe37-147">How multiple conditions are evaluated when they apply to more than one label</span></span>

<span data-ttu-id="efe37-p114">Метки оцениваются в порядке, в котором они указаны в политике: первая метка имеет наименьший приоритет (самый низкий уровень конфиденциальности), а последняя — наибольший приоритет (самый высокий уровень конфиденциальности). Дополнительные сведения о приоритете см. в разделе "Приоритет метки (важен порядок)" [этой статьи](sensitivity-labels.md#label-priority-order-matters).</span><span class="sxs-lookup"><span data-stu-id="efe37-p114">The labels are ordered for evaluation according to their position that you specify in the policy: The label positioned first has the lowest position (least sensitive) and the label positioned last has the highest position (most sensitive). For more information on priority, see [Label priority (order matters)](sensitivity-labels.md#label-priority-order-matters).</span></span>