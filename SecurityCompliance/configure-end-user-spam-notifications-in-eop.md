---
title: Настройка уведомлений пользователей о спаме в службе EOP
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: e9947db5-1dd1-4493-872d-7362b24c7ba0
ms.collection:
- M365-security-compliance
description: Вы можете настроить уведомления пользователя о нежелательной почте для используемой по умолчанию политики фильтрации содержимого в компании или для настраиваемых политик фильтрации содержимого, которые применяются к доменам.
ms.openlocfilehash: 07bca81f06a347bbce5e997e570553f85deb5c1d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151461"
---
# <a name="configure-end-user-spam-notifications-in-eop"></a><span data-ttu-id="8296c-103">Настройка уведомлений пользователей о спаме в службе EOP</span><span class="sxs-lookup"><span data-stu-id="8296c-103">Configure end-user spam notifications in EOP</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8296c-104">Эта статья предназначена для клиентов изолированной службы Exchange Online Protection (EOP), которые обеспечивают защиту своих локальных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="8296c-104">This topic is for Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes.</span></span> <span data-ttu-id="8296c-105">Пользователи Exchange Online, которые защищают размещенные в облаке почтовые ящики, должны прочитать следующий раздел: [Настройка уведомлений о нежелательной почте для конечных пользователей в Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="8296c-105">Exchange Online customers who are protecting cloud-hosted mailboxes should read the following topic instead: [Configure end-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md).</span></span> 
  
<span data-ttu-id="8296c-p102">Вы можете настроить уведомления пользователя о нежелательной почте для используемой по умолчанию политики фильтрации содержимого в компании или для настраиваемых политик фильтрации содержимого, которые применяются к доменам. Если включены уведомления пользователя о спаме, конечные пользователи смогут самостоятельно управлять своими сообщениями, которые находятся на карантине нежелательной почты. Уведомления конечного пользователя о нежелательных сообщениях нельзя использовать с политиками, которые применяются к пользователям, группам или к политике с исключениями.</span><span class="sxs-lookup"><span data-stu-id="8296c-p102">You can configure end-user spam notifications for the default company-wide content filter policy or for custom content filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="8296c-p103">Уведомления конечного пользователя о нежелательных сообщениях содержат список всех сообщений, помещенных на карантин нежелательной почты, которые получил пользователь в течение определенного вами периода (можно указать значение между 1 и 15 днями). Можно также настроить язык сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="8296c-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="8296c-111">После получения сообщения с уведомлением пользователи могут выбрать один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="8296c-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="8296c-112">**Просмотрите** сообщение, если вы хотите предварительно просмотреть содержимое или заголовок, прежде чем предпринимать действия.</span><span class="sxs-lookup"><span data-stu-id="8296c-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="8296c-113">**Скачайте** сообщение, если вы хотите просмотреть сообщение и вложения (если они есть) на устройстве, прежде чем предпринимать действия.</span><span class="sxs-lookup"><span data-stu-id="8296c-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="8296c-114">**Отпустите** , если сообщение не является спамом и вы хотите, чтобы Office 365 отправлял сообщение в ваш почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="8296c-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="8296c-115">**Выпуск _Амп_ разрешить отправителю** , если сообщение не является нежелательным, и вы хотите, чтобы Office 365 добавить отправителя в список надежных отправителей и получателей для будущих сообщений.</span><span class="sxs-lookup"><span data-stu-id="8296c-115">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails.</span></span> <span data-ttu-id="8296c-116">Имейте в виду, что у администратора могут быть другие конфигурации разрешений и блокировок в Организации, которые переопределяют список надежных отправителей.</span><span class="sxs-lookup"><span data-stu-id="8296c-116">Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="8296c-117">**Выпустите _Амп_ отчет**, если сообщение не спама и вы хотите отправить его в свой почтовый ящик и сообщить в корпорацию Майкрософт для анализа.</span><span class="sxs-lookup"><span data-stu-id="8296c-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="8296c-118">\*\*\*\* Заблокируйте, если вы хотите, чтобы Office 365 добавить отправителя в список заблокированных отправителей.</span><span class="sxs-lookup"><span data-stu-id="8296c-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="8296c-119">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="8296c-119">What do you need to know before you begin?</span></span>
<span data-ttu-id="8296c-120"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="8296c-120"></span></span>

<span data-ttu-id="8296c-121">Предполагаемое время выполнения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="8296c-121">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="8296c-p105">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье Запись "Защита от нежелательной почты" в разделе [Разрешения на функции в службе EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="8296c-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature permissions in EOP](eop/feature-permissions-in-eop.md) topic.</span></span> 
  
<span data-ttu-id="8296c-124">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="8296c-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="8296c-125">Настройка уведомлений пользователя о нежелательной почте с помощью Центра администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="8296c-125">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="8296c-126">В Центре администрирования Exchange перейдите к разделу **Защита** \> **Фильтр содержимого**.</span><span class="sxs-lookup"><span data-stu-id="8296c-126">In the Exchange admin center (EAC), navigate to **Protection** \> **Content filter**.</span></span>
    
2. <span data-ttu-id="8296c-127">Выберите политику фильтрации содержимого, для которой нужно включить уведомления пользователя о спаме (по умолчанию они отключены).</span><span class="sxs-lookup"><span data-stu-id="8296c-127">Select the content filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="8296c-128">На правой панели, на которой отображается сводная информация о вашей политике, выберите ссылку **Включить уведомления пользователя о нежелательной почте**.</span><span class="sxs-lookup"><span data-stu-id="8296c-128">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="8296c-129">В следующем диалоговом окне можно настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="8296c-129">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="8296c-p106">**Включить уведомления пользователя о нежелательной почте** Установите этот флажок, если нужно включить уведомления для этой политики. (И наоборот: если эта политика включена, снимите этот флажок, если нужно отключить уведомления пользователя о нежелательной почте для этой политики.)</span><span class="sxs-lookup"><span data-stu-id="8296c-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="8296c-p107">**Отправлять уведомления пользователя о нежелательной почте каждые (дн.)** Укажите, как часто необходимо отправлять пользователям уведомления о нежелательной почте. Значение по умолчанию  3 дня. Допустимый интервал значений  от 1 до 15 дней. Например, если вы укажете 7 дней, уведомление будет включать список всех сообщений за последние 7 дней, которые предназначались этому пользователю, но были ошибочно поставлены на карантин нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="8296c-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="8296c-136">**Язык уведомлений** В раскрывающемся списке выберите язык, на котором пользователю будут отправляться уведомления о нежелательной почте для этой политики.</span><span class="sxs-lookup"><span data-stu-id="8296c-136">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="8296c-p108">Нажмите кнопку **Сохранить**. Сводка ваших текущих параметров политики фильтрации содержимого, включая параметры уведомлений пользователя о нежелательной почте, отображается на правой панели.</span><span class="sxs-lookup"><span data-stu-id="8296c-p108">Click **save**. A summary of your content filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="8296c-p109">Уведомления пользователя о спаме будут работать только для включенных политик фильтрации содержимого. >  Уведомления о нежелательной почте отправляются конечному пользователю один раз в день. Время доставки уведомления не гарантируется для каждого конкретного пользователя, и его нельзя настроить.</span><span class="sxs-lookup"><span data-stu-id="8296c-p109">End-user spam notifications will only be functional for content filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="8296c-142">**Совет:** Если вы хотите протестировать уведомления о нежелательной почте пользователей, отправив их ограниченному набору пользователей, прежде чем приступать к их полному внедрению, создайте настраиваемую политику фильтрации содержимого, позволяющую пользователям получать уведомления о нежелательной почте для доменов, в которых они находятся.</span><span class="sxs-lookup"><span data-stu-id="8296c-142">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom content filter policy that enables end-user spam notifications for the domains in which the users reside.</span></span> <span data-ttu-id="8296c-143">Затем в центре администрирования Exchange в разделе \*\* \> правила\*\*обработки почтового ящика создайте правило для обработки почтового ящика (также называемое правилом транспорта), чтобы заблокировать сообщения от Quarantine@messaging.microsoft.com (адрес электронной почты, который отправляет уведомления) с исключениями для нужных пользователей. для получения уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8296c-143">Then, in the EAC, under **Mail flow \> rules**, create a mail flow rule (also known as a transport rule) to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications.</span></span> <span data-ttu-id="8296c-144">На следующем рисунке показан пример создания исключения для двух пользователей (SaraD и AlexD) с домена Contoso.com:</span><span class="sxs-lookup"><span data-stu-id="8296c-144">The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Правило транспорта для тестирования уведомлений пользователей о нежелательной почте](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="8296c-146">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="8296c-146">For more information</span></span>

[<span data-ttu-id="8296c-147">Настройка политик фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="8296c-147">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
