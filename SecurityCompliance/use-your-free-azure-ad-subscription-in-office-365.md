---
title: Использование бесплатной подписки на Azure Active Directory в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/8/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority\
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: d104fb44-1c42-4541-89a6-1f67be22e4ad
description: Сведения о том, как получать доступ к Azure Active Directory в составе платной подписки организации на Office 365.
ms.openlocfilehash: c49f6ca6aba109346ceea4558fe050b0cc561600
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242606"
---
# <a name="use-your-free-azure-active-directory-subscription-in-office-365"></a><span data-ttu-id="9ba2c-103">Использование бесплатной подписки на Azure Active Directory в Office 365</span><span class="sxs-lookup"><span data-stu-id="9ba2c-103">Use your free Azure Active Directory subscription in Office 365</span></span>

<span data-ttu-id="9ba2c-p101">Если у вашей организации есть платная подписка на Office 365, Microsoft Dynamics CRM Online, Enterprise Mobility + Security E3 или другие службы Майкрософт, у вас есть бесплатная подписка на Microsoft Azure Active Directory. Вы и другие администраторы можете использовать Azure AD для создания учетных записей групп и пользователей, а также для управления ими. Для работы с Azure AD нужно просто войти на портал Azure, используя учетную запись Office 365.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-p101">If your organization has a paid subscription to Office 365, Microsoft Dynamics CRM Online, Enterprise Mobility Suite, or other Microsoft services, you have a free subscription to Microsoft Azure Active Directory. You and other admins can use Azure AD to create and manage user and group accounts. To use Azure AD, just go to the Azure portal and sign in using your Office 365 account.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="9ba2c-107">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="9ba2c-107">Before you begin</span></span>

<span data-ttu-id="9ba2c-p102">Для доступа к порталу Azure (шаг 1, описанный далее) используйте сеанс закрытого просмотра, а не обычный, так как это предотвратит передачу текущих учетных данных в Azure. Чтобы начать сеанс просмотра InPrivate в Internet Explorer или сеанс закрытого просмотра в Mozilla FireFox, просто нажмите клавиши CTRL+SHIFT+P. Чтобы начать сеанс закрытого просмотра в Google Chrome (зовется режимом инкогнито), нажмите клавиши CTRL+SHIFT+N.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-p102">Use a private browsing session (not a regular session) to access the Azure portal (in step 1 below) because this will prevent the credential that you are currently logged on with from being passed to Azure. To open an InPrivate Browsing session in Internet Explorer or a Private Browsing session in Mozilla FireFox, just press CTRL+SHIFT+P. To open a private browsing session in Google Chrome (called an incognito window), press CTRL+SHIFT+N.</span></span>
  
## <a name="access-azure-active-directory"></a><span data-ttu-id="9ba2c-111">Доступ к Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9ba2c-111">Access Azure Active Directory</span></span>

1. <span data-ttu-id="9ba2c-112">Войдите на сайт [portal.azure.com](https://portal.azure.com), используя рабочую или учебную учетную запись Office 365.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-112">Go to [portal.azure.com](https://portal.azure.com) and sign in with your Office 365 work or student account.</span></span> 
    
2. <span data-ttu-id="9ba2c-113">На панели навигации портала Azure выберите **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-113">In the left navigation pane in the Azure portal, click **Azure Active Directory**.</span></span>
    
    ![На панели навигации портала Azure, расположенной слева, выберите пункт "Azure Active Directory".](media/97d2d72f-ac20-46ab-898c-851f6009b453.png)
  
    <span data-ttu-id="9ba2c-115">Отобразится центр администрирования **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-115">The **Azure Active Directory** admin center is displayed.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="9ba2c-116">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="9ba2c-116">More information</span></span>

- <span data-ttu-id="9ba2c-117">Вы также можете получить доступ к центру администрирования **Azure Active Directory** из центра администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-117">You can also access the **Azure Active Directory** admin center from the Microsoft 365 admin center.</span></span> <span data-ttu-id="9ba2c-118">в левой области навигации центра администрирования Microsoft 365 щелкните **центр** \> администрирования **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9ba2c-118">In the left navigation pane of the Microsoft 365 admin center , click **Admin centers** \> **Azure Active Directory**.</span></span>
    
- <span data-ttu-id="9ba2c-119">Сведения об управлении пользователями и группами, а также о выполнении других задач по управлению каталогом см. в статье [Управление каталогом Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administer).</span><span class="sxs-lookup"><span data-stu-id="9ba2c-119">For information about managing users and groups and performing other directory management tasks, see [Manage your Azure AD directory](https://docs.microsoft.com/azure/active-directory/active-directory-administer).</span></span>
