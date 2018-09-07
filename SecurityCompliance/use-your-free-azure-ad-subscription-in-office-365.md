---
title: Использование бесплатной подписки на Azure Active Directory в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/8/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: d104fb44-1c42-4541-89a6-1f67be22e4ad
description: Сведения о том, как получать доступ к Azure Active Directory в составе платной подписки организации на Office 365.
ms.openlocfilehash: f09dbfa00782abf408dd6bcf37341652189d8ea6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534954"
---
# <a name="use-your-free-azure-active-directory-subscription-in-office-365"></a><span data-ttu-id="0b539-103">Использование бесплатной подписки на Azure Active Directory в Office 365</span><span class="sxs-lookup"><span data-stu-id="0b539-103">Use your free Azure Active Directory subscription</span></span>

<span data-ttu-id="0b539-p101">Если у вашей организации есть платная подписка на Office 365, Microsoft Dynamics CRM Online, Enterprise Mobility + Security E3 или другие службы Майкрософт, у вас есть бесплатная подписка на Microsoft Azure Active Directory. Вы и другие администраторы можете использовать Azure AD для создания учетных записей групп и пользователей, а также для управления ими. Для работы с Azure AD нужно просто войти на портал Azure, используя учетную запись Office 365.</span><span class="sxs-lookup"><span data-stu-id="0b539-p101">If your organization has a paid subscription to Office 365, Microsoft Dynamics CRM Online, Enterprise Mobility Suite, or other Microsoft services, you have a free subscription to Microsoft Azure Active Directory. You and other admins can use Azure AD to create and manage user and group accounts. To use Azure AD, just go to the Azure portal and sign in using your Office 365 account.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="0b539-107">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="0b539-107">Before you begin</span></span>

<span data-ttu-id="0b539-p102">Для доступа к порталу Azure (шаг 1, описанный далее) используйте сеанс закрытого просмотра, а не обычный, так как это предотвратит передачу текущих учетных данных в Azure. Чтобы начать сеанс просмотра InPrivate в Internet Explorer или сеанс закрытого просмотра в Mozilla FireFox, просто нажмите клавиши CTRL+SHIFT+P. Чтобы начать сеанс закрытого просмотра в Google Chrome (зовется режимом инкогнито), нажмите клавиши CTRL+SHIFT+N.</span><span class="sxs-lookup"><span data-stu-id="0b539-p102">Use a private browsing session (not a regular session) to access the Azure portal (in step 1 below) because this will prevent the credential that you are currently logged on with from being passed to Azure. To open an InPrivate Browsing session in Internet Explorer or a Private Browsing session in Mozilla FireFox, just press CTRL+SHIFT+P. To open a private browsing session in Google Chrome (called an incognito window), press CTRL+SHIFT+N.</span></span>
  
## <a name="access-azure-active-directory"></a><span data-ttu-id="0b539-111">Доступ к Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0b539-111">Isolation and Access Control in Azure Active Directory</span></span>

1. <span data-ttu-id="0b539-112">Войдите на сайт [portal.azure.com](https://portal.azure.com), используя рабочую или учебную учетную запись Office 365.</span><span class="sxs-lookup"><span data-stu-id="0b539-112">Go to [portal.azure.com](https://portal.azure.com) and sign in with your Office 365 work or student account.</span></span> 
    
2. <span data-ttu-id="0b539-113">На панели навигации портала Azure выберите **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0b539-113">In the left navigation pane in the Azure portal, click **Azure Active Directory**.</span></span>
    
    ![На панели навигации портала Azure, расположенной слева, выберите пункт "Azure Active Directory".](media/97d2d72f-ac20-46ab-898c-851f6009b453.png)
  
    <span data-ttu-id="0b539-115">Отобразится центр администрирования **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0b539-115">The **Azure Active Directory** admin center is displayed.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="0b539-116">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0b539-116">More information</span></span>

- <span data-ttu-id="0b539-p103">Кроме того, доступ к центру администрирования **Azure Active Directory** можно получить в Центре администрирования Office 365. Откройте Центр администрирования Office 365 и на панели навигации слева выберите **Центры администрирования** \> **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="0b539-p103">You can also access the **Azure Active Directory** admin center from the Office 365 admin center. In the left navigation pane of the Office 365 admin center , click **Admin centers** \> **Azure Active Directory**.</span></span>
    
- <span data-ttu-id="0b539-119">Сведения об управлении пользователями и группами, а также о выполнении других задач по управлению каталогом см. в статье [Управление каталогом Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administer).</span><span class="sxs-lookup"><span data-stu-id="0b539-119">For information about managing users and groups and performing other directory management tasks, see [Administering your Azure AD directoryhttp://go.microsoft.com/fwlink/p/?LinkId=512488](https://docs.microsoft.com/azure/active-directory/active-directory-administer).</span></span>
