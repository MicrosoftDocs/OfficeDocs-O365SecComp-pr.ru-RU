---
title: Настройка уведомлений пользователя о спаме в Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: bfc91c73-a955-40e1-a95f-ad466624339a
description: Вы можете настроить уведомлений о нежелательной почте конечных пользователей для политики по умолчанию для фильтра нежелательной почты всей компании или для политик фильтров настраиваемых нежелательной почты, которые применяются к доменам.
ms.openlocfilehash: 4a4c7c6b139fe0f8b0a1f6b69c1b95e321293af5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027536"
---
# <a name="configure-end-user-spam-notifications-in-exchange-online"></a><span data-ttu-id="97c81-103">Настройка уведомлений пользователя о спаме в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="97c81-103">Configure end-user spam notifications in Exchange Online</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97c81-p101">Этот раздел предназначен для Exchange Online пользователи, которые защита облачные почтовые ящики. Вместо этого клиентов автономной Exchange Online Protection (EOP), которые защита локальные почтовые ящики должны прочтите следующий раздел: [Настройка уведомлений о нежелательной почте конечных пользователей в службе EOP](configure-end-user-spam-notifications-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="97c81-p101">This topic is for Exchange Online customers who are protecting cloud-hosted mailboxes. Exchange Online Protection (EOP) standalone customers who are protecting on-premises mailboxes should read the following topic instead: [Configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md).</span></span> 
  
<span data-ttu-id="97c81-p102">Вы можете настроить уведомлений о нежелательной почте конечных пользователей для политики по умолчанию для фильтра нежелательной почты всей компании или для политик фильтров настраиваемых нежелательной почты, которые применяются к доменам. Включение уведомлений конечных пользователей нежелательных сообщений позволяет пользователям самостоятельно управлять сообщения, помещенные на карантин нежелательной почты. Уведомления о нежелательной почте конечных пользователей не может использоваться с помощью политик, применяемых к пользователям или группам или политики исключения.</span><span class="sxs-lookup"><span data-stu-id="97c81-p102">You can configure end-user spam notifications for the default company-wide spam filter policy or for custom spam filter policies that are applied to domains. Enabling end-user spam notification messages lets your end users self-manage their own spam-quarantined messages. End-user spam notifications cannot be used with policies applied to users or groups, or to a policy with exceptions.</span></span>
  
<span data-ttu-id="97c81-p103">Уведомления конечного пользователя о нежелательных сообщениях содержат список всех сообщений, помещенных на карантин нежелательной почты, которые получил пользователь в течение определенного вами периода (можно указать значение между 1 и 15 днями). Можно также настроить язык сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="97c81-p103">End-user spam notifications contain a list of all spam-quarantined messages that the end user has received during a time period that you configure (you can specify a value between 1 and 15 days). You can also configure the language in which the notification message is written.</span></span>
  
<span data-ttu-id="97c81-111">После получения уведомления, конечные пользователи могут щелкните, чтобы переместить нежелательных сообщений электронной почты в своей папки "Входящие", или будет отправлен отчет нежелательных сообщений электронной почты как не являющиеся нежелательными, в этом случае его в группу анализа нежелательной почты Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97c81-111">After receiving a notification message, end users can click to move the spam email to their inbox, or report the spam email as Not Junk, in which case it will be sent to the Microsoft Spam Analysis Team.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="97c81-112">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="97c81-112">What do you need to know before you begin?</span></span>

<span data-ttu-id="97c81-113">Предполагаемое время выполнения: 2 минуты.</span><span class="sxs-lookup"><span data-stu-id="97c81-113">Estimated time to complete: 2 minutes</span></span>
  
<span data-ttu-id="97c81-p104">Вы должны быть назначены разрешения, перед выполнением этой процедуры или процедуры. Чтобы увидеть, какие нужны разрешения, видеть запись «Защита от нежелательной почты» в разделе [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="97c81-p104">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam" entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="97c81-116">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="97c81-116">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-configure-end-user-spam-notifications"></a><span data-ttu-id="97c81-117">Настройка уведомлений пользователя о нежелательной почте с помощью Центра администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="97c81-117">Use the EAC to configure end-user spam notifications</span></span>

1. <span data-ttu-id="97c81-118">В Центре администрирования Exchange перейдите в раздел **Защита** \> **Фильтр спама**.</span><span class="sxs-lookup"><span data-stu-id="97c81-118">In the Exchange admin center (EAC), navigate to **Protection** \> **Spam filter**.</span></span>
    
2. <span data-ttu-id="97c81-119">Выберите политику фильтрации нежелательной почты, для которого необходимо включить уведомления пользователя о спаме (они отключены по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="97c81-119">Select the spam filter policy for which you want to enable end-user spam notifications (they are disabled by default).</span></span>
    
3. <span data-ttu-id="97c81-120">На правой панели, на которой отображается сводная информация о вашей политике, выберите ссылку **Включить уведомления пользователя о нежелательной почте**.</span><span class="sxs-lookup"><span data-stu-id="97c81-120">In the right pane, where the summary information about your policy appears, click the **Configure End-user spam notifications** link.</span></span> 
    
4. <span data-ttu-id="97c81-121">В следующем диалоговом окне можно настроить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="97c81-121">In the subsequent dialog box, you can configure the following options:</span></span>
    
1. <span data-ttu-id="97c81-p105">**Включить уведомления пользователя о нежелательной почте** Установите этот флажок, если нужно включить уведомления для этой политики. (И наоборот: если эта политика включена, снимите этот флажок, если нужно отключить уведомления пользователя о нежелательной почте для этой политики.)</span><span class="sxs-lookup"><span data-stu-id="97c81-p105">**Enable end-user spam notifications** Select this check box in order to enable end-user spam notifications for this policy. (Conversely, if this policy is enabled, you can clear this check box in order to disable end-user spam notifications for this policy.)</span></span> 
    
2. <span data-ttu-id="97c81-p106">**Отправлять уведомления пользователя о нежелательной почте каждые (дн.)** Укажите, как часто необходимо отправлять пользователям уведомления о нежелательной почте. Значение по умолчанию  3 дня. Допустимый интервал значений  от 1 до 15 дней. Например, если вы укажете 7 дней, уведомление будет включать список всех сообщений за последние 7 дней, которые предназначались этому пользователю, но были ошибочно поставлены на карантин нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="97c81-p106">**Send end-user spam notifications every (days)** Specify how often to send end-user spam notifications. The default is 3 days. You can specify between 1 and 15 days. If you specify 7 days, for example, the notification will include a list of all messages intended for that user within the past 7 days that were sent to the spam quarantine instead.</span></span> 
    
3. <span data-ttu-id="97c81-128">**Язык уведомлений** В раскрывающемся списке выберите язык, на котором пользователю будут отправляться уведомления о нежелательной почте для этой политики.</span><span class="sxs-lookup"><span data-stu-id="97c81-128">**Notification language** Using the drop-down list, select the language in which to write end-user spam notifications for this policy.</span></span> 
    
5. <span data-ttu-id="97c81-p107">Нажмите кнопку **Сохранить**. В правой области отображается сводка параметров политики фильтра нежелательной почты, включая параметры уведомлений конечных пользователей нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="97c81-p107">Click **save**. A summary of your spam filter policy settings, including your end-user spam notification settings, appears in the right pane.</span></span>
    
> [!NOTE]
>  <span data-ttu-id="97c81-p108">Уведомления пользователя о спаме будут работать только для включенных политик фильтрации нежелательной почты. > Уведомления о нежелательной почте конечного пользователя отправляются только один раз в день. Время доставки уведомления не гарантируется для одного конкретного клиента и не настраивается.</span><span class="sxs-lookup"><span data-stu-id="97c81-p108">End-user spam notifications will only be functional for spam filter policies that are enabled. >  End-user spam notifications are only sent once per day. The delivery time of the notification cannot be guaranteed for any specific customer and is not configurable.</span></span> 
  
 <span data-ttu-id="97c81-p109">**Совет:** Если вы хотите проверить уведомлений о нежелательной почте конечных пользователей, отправив им ограниченный набор пользователей, прежде чем внедрять их полностью, создайте политику фильтра настраиваемой нежелательной почты, которая позволяет уведомлений о нежелательной почте конечных пользователей для доменов, в которых находятся пользователи. Затем в центре администрирования Exchange в разделе **Потоки почты \> правил**, создать правила транспорта для блокирования сообщений с quarantine@messaging.microsoft.com (адрес электронной почты, который отправляет уведомления) с исключения для пользователей, которые вы хотите получать уведомления. На следующем рисунке приведено пример создания исключения для двух пользователей (SaraD и AlexD) из домена Contoso.com:</span><span class="sxs-lookup"><span data-stu-id="97c81-p109">**Tip:** If you want to test end-user spam notifications by sending them to a limited set of users before fully implementing them, create a custom spam filter policy that enables end-user spam notifications for the domains in which the users reside. Then, in the EAC, under **Mail flow \> rules**, create a transport rule to block messages from quarantine@messaging.microsoft.com (the email address that sends notifications) with exceptions for the users who you want to receive the notifications. The following image is an example of creating an exception for two users (SaraD and AlexD) from domain Contoso.com:</span></span> 
  
![Правило транспорта для тестирования уведомлений пользователей о нежелательной почте](media/EOP-ESN-testspecificusers.jpg)
  
## <a name="for-more-information"></a><span data-ttu-id="97c81-138">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="97c81-138">For more information</span></span>

[<span data-ttu-id="97c81-139">Настройте политики защиты от спама</span><span class="sxs-lookup"><span data-stu-id="97c81-139">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
