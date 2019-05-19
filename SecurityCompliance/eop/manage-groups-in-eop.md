---
title: Управление группами в EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 212e68ac-6330-47e9-a169-6cf5e2f21e13
description: С помощью Exchange Online Protection (EOP) для организации Exchange можно создавать группы с включенной поддержкой почты. EOP также позволяет определять или обновлять свойства групп, указывающие членство, адреса электронной почты и другие данные групп.
ms.openlocfilehash: 090f76d034dcdcbc774666830fd0cbc54815f8c0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153141"
---
# <a name="manage-groups-in-eop"></a><span data-ttu-id="e83be-104">Управление группами в EOP</span><span class="sxs-lookup"><span data-stu-id="e83be-104">Manage groups in EOP</span></span>

 <span data-ttu-id="e83be-p102">С помощью Exchange Online Protection (EOP) для организации Exchange можно создавать группы с включенной поддержкой почты. EOP также позволяет определять или обновлять свойства групп, указывающие членство, адреса электронной почты и другие данные групп. В зависимости от своих требований вы можете создать группы рассылки или группы безопасности. Такие группы можно создать с помощью Центра администрирования Exchange или удаленной консоли Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e83be-p102">You can use Exchange Online Protection (EOP) to create mail-enabled groups for an Exchange organization. You can also use EOP to define or update group properties that specify membership, email addresses, and other aspects of groups. You can create distribution groups and security groups, depending on your needs. These groups can be created by using the Exchange admin center (EAC) or via remote Windows PowerShell.</span></span> 
  
## <a name="types-of-mail-enabled-groups"></a><span data-ttu-id="e83be-109">Типы групп с включенной поддержкой почты</span><span class="sxs-lookup"><span data-stu-id="e83be-109">Types of mail-enabled groups</span></span>

<span data-ttu-id="e83be-110">Для организации Exchange вы можете создать группы двух типов.</span><span class="sxs-lookup"><span data-stu-id="e83be-110">You can create two types of groups for your Exchange organization:</span></span>
  
- <span data-ttu-id="e83be-p103">[Создание группы в Центре администрирования Exchange](manage-groups-in-eop.md) (также известные как группы рассылки)  это коллекции пользователей электронной почты, такие как команда сотрудников или другая специализированная группа, которым необходимо получать или отправлять сообщения электронной почты, представляющие интерес для всех участников. Группы рассылки создаются исключительно для распространения сообщений электронной почты. В EOP под группой рассылки подразумевается любая группа с включенной поддержкой почты вне зависимости от ее контекста безопасности.</span><span class="sxs-lookup"><span data-stu-id="e83be-p103">[Create a group in the EAC](manage-groups-in-eop.md) (also known as distribution groups) are collections of email users, such as a team or other ad hoc group, who need to receive or send email regarding a common area of interest. Distribution groups are exclusively for distributing email messages. In EOP, a distribution group refers to any mail-enabled group, whether or not it has a security context.</span></span>
    
- <span data-ttu-id="e83be-p104">[Изменение или удаление группы в Центре администрирования Exchange](manage-groups-in-eop.md) (также известные как группы безопасности)  это коллекции пользователей электронной почты, которым нужны разрешения на доступ на уровне ролей администраторов. Например, вам может понадобиться предоставить определенной группе пользователей разрешения на уровне роли администратора, чтобы они могли настраивать параметры защиты от нежелательной почты и вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="e83be-p104">[Edit or remove a group in the EAC](manage-groups-in-eop.md) (also known as security groups) are collections of email users who need access permissions for Admin roles. For example, you might want to give specific group of users admin role permissions so they can configure anti-spam and anti-malware settings.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e83be-p105">По умолчанию все новые группы безопасности требуют проверки подлинности всех отправителей. Это запрещает внешним отправителям отправлять сообщения в группы безопасности с включенной поддержкой почты.</span><span class="sxs-lookup"><span data-stu-id="e83be-p105">By default, all new mail-enabled security groups require that all senders be authenticated. This prevents external senders from sending messages to mail-enabled security groups.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="e83be-118">Приступая к работе</span><span class="sxs-lookup"><span data-stu-id="e83be-118">Before you begin</span></span>

- <span data-ttu-id="e83be-p106">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье Запись "Группы рассылки и группы безопасности" в разделе [Разрешения на функции в службе EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="e83be-p106">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Distribution Groups and Security Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="e83be-121">Обратите внимание, что при создании групп и управлении ими с помощью командлетов удаленной консоли PowerShell вы можете столкнуться с регулированием.</span><span class="sxs-lookup"><span data-stu-id="e83be-121">Be aware that when creating and managing groups by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="e83be-122">Этот командлет использует метод пакетной обработки, из-за чего результаты его выполнения становятся видны через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="e83be-122">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="e83be-123">Сведения об использовании Windows PowerShell для подключения к службе Exchange Online Protection см. в статье [Подключение к Exchange Online Protection с помощью удаленной оболочки PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="e83be-123">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/connect-to-exchange-online-protection-powershell?view=exchange-ps).</span></span>
    
- <span data-ttu-id="e83be-124">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="e83be-124">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="e83be-p107">Возникли проблемы? Обратитесь за помощью к участникам форумов, посвященных Exchange. Посетите форумы по таким продуктам: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) или [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="e83be-p107">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="create-a-group-in-the-eac"></a><span data-ttu-id="e83be-128">Создание группы в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="e83be-128">Create a group in the EAC</span></span>

1. <span data-ttu-id="e83be-129">В Центре администрирования Exchange перейдите в раздел **Получатели** \> **Группы**.</span><span class="sxs-lookup"><span data-stu-id="e83be-129">In the Exchange admin center (EAC), go to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="e83be-p108">Нажмите кнопку **Создать**![Значок добавления](../media/ITPro-EAC-AddIcon.gif), а затем щелкните **Группа рассылки** или **Группа безопасности** в зависимости от ваших потребностей. Отличия между этими группами см. в разделе [Типы групп с включенной поддержкой почты](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="e83be-p108">Click **New**![Add Icon](../media/ITPro-EAC-AddIcon.gif), and then click **Distribution group** or **Security group**, depending on your needs. See [Types of mail-enabled groups](manage-groups-in-eop.md) for the distinction.</span></span> 
    
3. <span data-ttu-id="e83be-132">На странице **Создать группу рассылки** или **Создать группу безопасности** заполните приведенные ниже поля.</span><span class="sxs-lookup"><span data-stu-id="e83be-132">On the **New distribution group** or **New security group** page, complete the following fields:</span></span> 
    
  - <span data-ttu-id="e83be-p109">**Отображаемое имя**. Введите отображаемое имя, уникальное для вашей организации и понятное пользователям EOP. Отображаемое имя является обязательным параметром.</span><span class="sxs-lookup"><span data-stu-id="e83be-p109">**Display name** Type a display name that's unique to your organization and meaningful to EOP users. The display name is required.</span></span> 
    
  - <span data-ttu-id="e83be-p110">**Псевдоним**. Введите уникальный для вашей организации псевдоним группы, содержащий до 64 символов. Пользователи EOP вводят псевдоним в строке "Кому:" сообщения электронной почты, и он сопоставляется с отображаемым именем группы. Если изменить псевдоним, основной SMTP-адрес группы также изменится и будет содержать новый псевдоним. Псевдоним является обязательным параметром.</span><span class="sxs-lookup"><span data-stu-id="e83be-p110">**Alias** Type a group alias of up to 64 characters that's unique to your organization. EOP users type the alias in the To: line of email messages and the alias resolves to the group's display name. If you change the alias, the primary SMTP address for the group also changes and will contain the new alias. The alias is required.</span></span> 
    
  - <span data-ttu-id="e83be-139">**Описание**. Введите описание группы, чтобы сообщить пользователям о ее назначении.</span><span class="sxs-lookup"><span data-stu-id="e83be-139">**Description** Type a description of the group so that people will know the purpose of the group.</span></span> 
    
  - <span data-ttu-id="e83be-p111">**Владельцы**. По умолчанию владельцем группы становится ее создатель. Добавить владельцев можно с помощью кнопки **Добавить**![Значок добавления](../media/ITPro-EAC-AddIcon.gif). Для каждой группы должен существовать по крайней мере один владелец.</span><span class="sxs-lookup"><span data-stu-id="e83be-p111">**Owners** By default, the person who creates the group is the owner. You can add an owner by choosing **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). All groups must have at least one owner.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e83be-143">Владельцы не обязательно должны быть членами группы.</span><span class="sxs-lookup"><span data-stu-id="e83be-143">Owners don't have to be members of the group.</span></span> 
  
  - <span data-ttu-id="e83be-p112">**Члены**. В этом разделе можно добавить членов группы и указать, требуется ли утверждение для пользователей, желающих присоединиться к группе или покинуть ее. Чтобы добавить пользователей в группу, нажмите кнопку **Добавить**![Значок добавления](../media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="e83be-p112">**Members** Use this section to add group members and to specify whether approval is required for people to join or leave the group. To add members to the group, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="e83be-146">Нажмите кнопку **ОК**, чтобы вернуться на исходную страницу.</span><span class="sxs-lookup"><span data-stu-id="e83be-146">Click **OK** to return to the original page.</span></span> 
    
5. <span data-ttu-id="e83be-p113">Закончив, нажмите кнопку **Сохранить**, чтобы создать группу. Новая группа должна отобразиться в списке групп.</span><span class="sxs-lookup"><span data-stu-id="e83be-p113">When you've finished, click **Save** to create the group. The new group should appear in the list of groups.</span></span> 
    
## <a name="edit-or-remove-a-group-in-the-eac"></a><span data-ttu-id="e83be-149">Изменение или удаление группы в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="e83be-149">Edit or remove a group in the EAC</span></span>

1. <span data-ttu-id="e83be-150">В Центре администрирования Exchange последовательно выберите пункты **Получатели** \> **Группы**.</span><span class="sxs-lookup"><span data-stu-id="e83be-150">In the EAC, navigate to **Recipients** \> **Groups**.</span></span>
    
2. <span data-ttu-id="e83be-151">Выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="e83be-151">Do one of the following:</span></span>
    
  - <span data-ttu-id="e83be-152">Чтобы изменить группу, выберите группу рассылки или группы безопасности, которую нужно просмотреть или изменить, и нажмите кнопку **изменить** ![значок](../media/ITPro-EAC-EditIcon.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="e83be-152">To edit a group: In the list of groups, click the distribution or security group that you want to view or change, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span> <span data-ttu-id="e83be-153">При необходимости вы можете обновить общие параметры, а также добавить или удалить владельцев и членов группы.</span><span class="sxs-lookup"><span data-stu-id="e83be-153">You can update general settings, add or remove group owners, and add or remove group members, as needed.</span></span>
    
  - <span data-ttu-id="e83be-154">Удаление группы Выберите группу и нажмите кнопку **Удалить**![Значок "Удалить"](../media/ITPro-EAC-RemoveIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="e83be-154">To remove a group: Select the group and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="e83be-155">После внесения изменений нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e83be-155">When you're finished making your changes, click **Save**.</span></span>
    
## <a name="create-edit-or-remove-a-group-using-remote-windows-powershell"></a><span data-ttu-id="e83be-156">Создание, изменение или удаление группы с помощью удаленной консоли Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e83be-156">Create, edit, or remove a group using remote Windows PowerShell</span></span>

<span data-ttu-id="e83be-p115">В этом разделе содержатся сведения о создании групп и изменении их свойств с помощью удаленной консоли Windows PowerShell. В нем также рассказывается об удалении существующей группы.</span><span class="sxs-lookup"><span data-stu-id="e83be-p115">This section provides information about creating groups and changing their properties by using remote Windows PowerShell. It also shows how to remove an existing group.</span></span> 
  
 <span data-ttu-id="e83be-159">**Создание группы с помощью удаленной консоли Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e83be-159">**To create a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="e83be-p116">В этом примере командлет [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) используется для создания группы рассылки с псевдонимом "itadmin" и именем "ИТ-администраторы". Кроме того, он добавляет пользователей как членов группы.</span><span class="sxs-lookup"><span data-stu-id="e83be-p116">This example uses the [New-EOPDistributionGroup](http://technet.microsoft.com/library/4610dfe5-fca8-4ba8-be3c-535d1753e0f4.aspx) cmdlet to create a distribution group with an alias of itadmin and the name IT Administrators. It also adds users as members of the group.</span></span> 
  
```Powershell
New-EOPDistributionGroup -Type "Distribution" -Name "IT Administrators" -Alias itadmin -Members @("Member1","Member2","Member3") -ManagedBy "Member1"

```

<span data-ttu-id="e83be-162">Чтобы создать группу безопасности вместо группы рассылки, укажите  `-Type "Security"`.</span><span class="sxs-lookup"><span data-stu-id="e83be-162">To create a security group instead of a distribution group, specify  `-Type "Security"` instead.</span></span> 
  
<span data-ttu-id="e83be-163">Убедитесь в успешном создании группы "ИТ-администраторы", запустив командлет [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx), чтобы отобразить сведения о новой группе:</span><span class="sxs-lookup"><span data-stu-id="e83be-163">To verify that you've successfully created the IT Administrators group, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to display information about the new group:</span></span> 
  
```Powershell
Get-Recipient "IT Administrators" | Format-List

```

<span data-ttu-id="e83be-164">Чтобы получить список членов группы, запустите командлет [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx), введя следующий код:</span><span class="sxs-lookup"><span data-stu-id="e83be-164">To get a list of members in the group, run the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "IT Administrators"

```

<span data-ttu-id="e83be-165">Чтобы получить полный список всех своих групп, запустите командлет [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx), введя следующий код:</span><span class="sxs-lookup"><span data-stu-id="e83be-165">To get a full list of all your groups, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup" | FT | more

```

 <span data-ttu-id="e83be-166">**Изменение свойств группы с помощью удаленной консоли Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e83be-166">**To change the properties of a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="e83be-p117">Просматривайте и изменяйте свойства группы с помощью командлетов [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) и [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx). В отличие от Центра администрирования Exchange, удаленная консоль PowerShell позволяет изменять свойства нескольких групп.</span><span class="sxs-lookup"><span data-stu-id="e83be-p117">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlets to view and change properties for groups. An advantage of using remote PowerShell instead of the EAC is the ability to change properties for multiple groups.</span></span> 
  
<span data-ttu-id="e83be-169">Ниже приведены примеры использования удаленной консоли Windows PowerShell с этой целью.</span><span class="sxs-lookup"><span data-stu-id="e83be-169">Here are some examples of using remote Windows PowerShell to change group properties.</span></span>
  
<span data-ttu-id="e83be-170">В этом примере командлет [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) используется, чтобы изменить основной SMTP-адрес (обратный адрес) для группы "Сотрудники Москвы" на sotrudniki.m@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="e83be-170">This example uses the [Set-EOPDistributionGroup](http://technet.microsoft.com/library/689a66c5-a524-4870-88f3-091fd6eae3b7.aspx) cmdlet to change the primary SMTP address (also called the reply address) for the Seattle Employees group to sea.employees@contoso.com.</span></span> 
  
```Powershell
Set-EOPDistributionGroup "Seattle Employees" -PrimarysmptAddress "sea.employees@contoso.com"

```

<span data-ttu-id="e83be-p118">Убедитесь, что свойства группы успешно изменены, проверив изменения с помощью командлета [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx). Одно из преимуществ использования удаленной консоли PowerShell  возможность просмотреть свойства нескольких групп. Чтобы проверить, изменился ли SMTP-адрес группы из примера выше, запустите такую команду:</span><span class="sxs-lookup"><span data-stu-id="e83be-p118">To verify that you've successfully changed the properties for a group, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. One advantage of using remote PowerShell is that you can view multiple properties for multiple groups. In the previous example where the primary SMTP address group was changed, run the following command to verify the new value:</span></span> 
  
```Powershell
Get-Recipient "Seattle Employees" | FL "PrimarySmtpAddress"

```

<span data-ttu-id="e83be-p119">В этом примере командлет [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) используется для обновления всех членов группы "Сотрудники Москвы". Разделяйте всех членов запятой.</span><span class="sxs-lookup"><span data-stu-id="e83be-p119">This example uses the [Update-EOPDistributionGroupMember](http://technet.microsoft.com/library/a6d4f790-1b94-42f8-af6f-fa79c504d8ec.aspx) cmdlet to update all the members of the Seattle Employees group. Use a comma to separate all members.</span></span> 
  
```Powershell
Update-EOPDistributionGroupMember -Identity "Seattle Employees" -Members @("Member1","Member2","Member3","Member4","Member5")

```

<span data-ttu-id="e83be-176">Чтобы получить список всех членов группы "Сотрудники Москвы", запустите командлет [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx):</span><span class="sxs-lookup"><span data-stu-id="e83be-176">To get the list of all the members in the group Seattle Employees, use the [Get-DistributionGroupMember](http://technet.microsoft.com/library/15c71bc5-4246-44ac-8b34-8ccd585294b5.aspx) cmdlet as follows:</span></span> 
  
```Powershell
Get-DistributionGroupMember "Seattle Employees"

```

 <span data-ttu-id="e83be-177">**Удаление группы с помощью удаленной консоли Windows PowerShell**</span><span class="sxs-lookup"><span data-stu-id="e83be-177">**To remove a group using remote Windows PowerShell**</span></span>
  
<span data-ttu-id="e83be-178">В этом примере командлет [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) используется для удаления группы рассылки "ИТ-администраторы".</span><span class="sxs-lookup"><span data-stu-id="e83be-178">This example uses the [Remove-EOPDistributionGroup](http://technet.microsoft.com/library/a17b1307-3187-40b0-a438-c7b35a34c002.aspx) cmdlet to remove a distribution group named IT Administrators.</span></span> 
  
```Powershell
Remove-EOPDistributionGroup -Identity "IT Administrators" 

```

<span data-ttu-id="e83be-179">Чтобы убедиться, что группа удалена, запустите командлет [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) и подтвердите, что группа (в данном случае  "ИТ-администраторы") удалена.</span><span class="sxs-lookup"><span data-stu-id="e83be-179">To verify that the group was removed, run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows, and confirm that the group (in this case "It Administrators") was deleted.</span></span> 
  
```Powershell
Get-Recipient -RecipientType "MailUniversalDistributionGroup"

```


