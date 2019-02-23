---
title: Настройка уведомлений пользователя о спаме в Exchange Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
ms.collection:
- M365-security-compliance
description: Вы можете настроить уведомления о нежелательной почте для пользователей по умолчанию для политики фильтрации нежелательной почты по умолчанию или для настраиваемых политик фильтрации нежелательной почты, которые применяются к доменам.
ms.openlocfilehash: ea2994a3f772b407a35be2d64e8afcc639d24f31
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214499"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="0e69e-103">Настройка уведомлений пользователя о спаме в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0e69e-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e69e-p101">Эта статья предназначена для пользователей Exchange Online, которые защищают размещенные в облаке почтовые ящики. Изолированные клиенты Exchange Online Protection (EOP), защищающие локальные почтовые ящики, должны прочитать следующий раздел: [Настройка уведомлений конечных пользователей о нежелательной почте в EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="0e69e-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="0e69e-p102">Вы можете настроить уведомления о нежелательной почте для пользователей по умолчанию для политики фильтрации нежелательной почты по умолчанию или для настраиваемых политик фильтрации нежелательной почты, которые применяются к доменам. Включение оповещений о нежелательной почте позволяет конечным пользователям самостоятельно управлять своими сообщениями, помещенными в карантин нежелательной почты. Уведомления конечных пользователей о нежелательной почте нельзя использовать с политиками, применяемыми к пользователям или группам, или к политике с исключениями.</span><span class="sxs-lookup"><span data-stu-id="0e69e-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="0e69e-p103">Уведомления конечного пользователя о нежелательных сообщениях содержат список всех сообщений, помещенных на карантин нежелательной почты, которые получил пользователь в течение определенного вами периода (можно указать значение между 1 и 15 днями). Можно также настроить язык сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="0e69e-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="0e69e-111">После получения сообщения с уведомлением пользователи могут выбрать один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="0e69e-111">After receiving a notification message, end users can choose from the following options:</span></span>

<span data-ttu-id="0e69e-112">**Просмотрите** сообщение, если вы хотите предварительно просмотреть содержимое или заголовок, прежде чем предпринимать действия.</span><span class="sxs-lookup"><span data-stu-id="0e69e-112">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

<span data-ttu-id="0e69e-113">**Скачайте** сообщение, если вы хотите просмотреть сообщение и вложения (если они есть) на устройстве, прежде чем предпринимать действия.</span><span class="sxs-lookup"><span data-stu-id="0e69e-113">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

<span data-ttu-id="0e69e-114">**Отпустите** , если сообщение не является спамом и вы хотите, чтобы Office 365 отправлял сообщение в ваш почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="0e69e-114">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

<span data-ttu-id="0e69e-p104">**Выпуск _Амп_ разрешить отправителю** , если сообщение не является нежелательным, и вы хотите, чтобы Office 365 добавить отправителя в список надежных отправителей и получателей для будущих сообщений. Имейте в виду, что у администратора могут быть другие конфигурации разрешений и блокировок в Организации, которые переопределяют список надежных отправителей.</span><span class="sxs-lookup"><span data-stu-id="0e69e-p104">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails. Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

<span data-ttu-id="0e69e-117">**Выпустите _Амп_ отчет**, если сообщение не спама и вы хотите отправить его в свой почтовый ящик и сообщить в корпорацию Майкрософт для анализа.</span><span class="sxs-lookup"><span data-stu-id="0e69e-117">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

<span data-ttu-id="0e69e-118">\*\*\*\* Заблокируйте, если вы хотите, чтобы Office 365 добавить отправителя в список заблокированных отправителей.</span><span class="sxs-lookup"><span data-stu-id="0e69e-118">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="0e69e-119">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="0e69e-119">What do you need to know before you begin?</span></span>

<span data-ttu-id="0e69e-120">Предполагаемое время выполнения: 2 минуты.</span><span class="sxs-lookup"><span data-stu-id="0e69e-120">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="0e69e-p105">Перед выполнением этой процедуры или процедур необходимо назначить разрешения. Чтобы просмотреть необходимые разрешения, обратитесь к разделу "Защита от нежелательной почты" в разделе [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0e69e-p105">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="0e69e-123">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="0e69e-123">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="0e69e-124">Настройка уведомлений пользователя о нежелательной почте с помощью Центра администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="0e69e-124">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="0e69e-125">В Центре администрирования Exchange перейдите в раздел **Защита** \> **Фильтр спама**.</span><span class="sxs-lookup"><span data-stu-id="0e69e-125">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="0e69e-126">Выберите политику фильтрации нежелательной почты, для которой нужно включить уведомления конечных пользователей о нежелательной почте (по умолчанию они отключены).</span><span class="sxs-lookup"><span data-stu-id="0e69e-126">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="0e69e-127">На правой панели, на которой отображается сводная информация о вашей политике, выберите ссылку **Включить уведомления пользователя о нежелательной почте**.</span><span class="sxs-lookup"><span data-stu-id="0e69e-127">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="0e69e-128">В следующем диалоговом окне можно настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="0e69e-128">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="0e69e-p106">**Включить уведомления пользователя о нежелательной почте** Установите этот флажок, если нужно включить уведомления для этой политики. (И наоборот: если эта политика включена, снимите этот флажок, если нужно отключить уведомления пользователя о нежелательной почте для этой политики.)</span><span class="sxs-lookup"><span data-stu-id="0e69e-p106">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="0e69e-p107">**Отправлять уведомления пользователя о нежелательной почте каждые (дн.)** Укажите, как часто необходимо отправлять пользователям уведомления о нежелательной почте. Значение по умолчанию  3 дня. Допустимый интервал значений  от 1 до 15 дней. Например, если вы укажете 7 дней, уведомление будет включать список всех сообщений за последние 7 дней, которые предназначались этому пользователю, но были ошибочно поставлены на карантин нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="0e69e-p107">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="0e69e-135">**Язык уведомлений** В раскрывающемся списке выберите язык, на котором пользователю будут отправляться уведомления о нежелательной почте для этой политики.</span><span class="sxs-lookup"><span data-stu-id="0e69e-135">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="0e69e-p108">Нажмите кнопку **сохранить**. Сводка параметров политики фильтрации нежелательной почты, в том числе параметров уведомлений для конечных пользователей, отображается в правой области.</span><span class="sxs-lookup"><span data-stu-id="0e69e-p108">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="0e69e-p109">Уведомления конечных пользователей о нежелательной почте будут работать только с включенными политиками фильтрации нежелательной почты. уведомления пользователя о нежелательной почте _Гт_ отправляются только один раз в день. Время доставки уведомления не может быть гарантировано для какого-либо конкретного клиента и не может быть настроено.</span><span class="sxs-lookup"><span data-stu-id="0e69e-p109">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="0e69e-p110">**Совет:** Если вы хотите протестировать уведомления о нежелательной почте пользователей, отправив их ограниченному набору пользователей, прежде чем приступать к их полному внедрению, создайте настраиваемую политику фильтрации нежелательной почты, позволяющую пользователям получать уведомления о нежелательной почте для доменов, в которых они находятся. Затем в центре администрирования Exchange в разделе \*\* \> правила\*\*для обработки почты создайте правило транспорта для блокирования сообщений от Quarantine@messaging.microsoft.com (адрес электронной почты, который отправляет уведомления) с исключениями для пользователей, которые хотят получать уведомления. На приведенном ниже рисунке показано, как создать исключение для двух пользователей (Сарад и Алекс) из Contoso.com домена:</span><span class="sxs-lookup"><span data-stu-id="0e69e-p110">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Правило транспорта для тестирования уведомлений пользователей о нежелательной почте](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="0e69e-145">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0e69e-145">For more information</span></span>

[<span data-ttu-id="0e69e-146">Настройте политики защиты от спама</span><span class="sxs-lookup"><span data-stu-id="0e69e-146">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
