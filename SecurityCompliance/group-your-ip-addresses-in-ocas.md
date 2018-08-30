---
title: Группирование IP-адресов для упрощения управления в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Чтобы легко определять наборы IP-адресов, которые будут использоваться в облаке приложения Office 365 безопасность реального офиса IP-адреса, например, можно настроить группы диапазонов IP-адресов.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534268"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a><span data-ttu-id="9975e-103">Группирование IP-адресов для упрощения управления в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9975e-103">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="9975e-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="9975e-104">****Evaluation** \>**</span></span>|<span data-ttu-id="9975e-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="9975e-105">****Planning** \>**</span></span>|<span data-ttu-id="9975e-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="9975e-106">****Deployment** \>**</span></span>|<span data-ttu-id="9975e-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="9975e-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9975e-108">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="9975e-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9975e-109">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="9975e-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="9975e-110">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="9975e-110">You are here!</span></span>  <br/> [<span data-ttu-id="9975e-111">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9975e-111">Next steps</span></span>](#next-steps) <br/> |[<span data-ttu-id="9975e-112">Начать использование</span><span class="sxs-lookup"><span data-stu-id="9975e-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="9975e-p101">Чтобы легко определять наборы IP-адресов, которые будут использоваться в облаке приложения Office 365 безопасность реального офиса IP-адреса, например, можно настроить группы диапазонов IP-адресов. Определение этих диапазонов позволяет отметить и распределения по категориям и затем можно использовать теги и отображаются и изучению категорий, которые необходимо настроить как действие журналы и оповещения.</span><span class="sxs-lookup"><span data-stu-id="9975e-p101">To easily identify sets of IP addresses that you'll use in Office 365 Cloud App Security, such as your physical office IP addresses, you can set up groups of IP address ranges. Defining these ranges lets you tag and categorize them, and then you can use tags and categories to customize how your activity logs and alerts are displayed and investigated.</span></span>
  
<span data-ttu-id="9975e-p102">Каждой группе диапазонов IP-адресов будут помечены имена тегов, которые можно выбрать, а затем теги можно разделить на основе списка по умолчанию категорий IP-адрес (например, Корпоративная, административные, Risky и VPN). Поддерживаются адреса IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="9975e-p102">Each group of IP ranges can be tagged with tag names that you choose, and then the tags can be categorized based on a default list of IP categories (such as Corporate, Administrative, Risky, and VPN). Both IPv4 and IPv6 addresses are supported.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9975e-p103">Необходимо быть глобальным администратором или администратор безопасности для выполнения процедур, описанных в этой статье. Чтобы получить дополнительные сведения, обратитесь к разделу [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9975e-p103">You must be a global administrator or security administrator to perform the procedures in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a><span data-ttu-id="9975e-119">Чтобы настроить диапазон IP-адресов в облаке приложения Office 365 безопасности</span><span class="sxs-lookup"><span data-stu-id="9975e-119">To set up an IP address range in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="9975e-p104">Как глобальный администратор или администратор безопасности, перейдите к [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы. (Вы перейдете к безопасности &amp; центре соответствия требованиям.)</span><span class="sxs-lookup"><span data-stu-id="9975e-p104">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="9975e-122">В разделе Безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Расширенное Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="9975e-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="9975e-123">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="9975e-123">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="9975e-125">В правом верхнем углу страницы щелкните **Параметры** \> **диапазоны IP-адресов**.</span><span class="sxs-lookup"><span data-stu-id="9975e-125">On the upper right of the page, click **Settings** \> **IP address ranges**.</span></span>
    
    ![В облаке приложения O365 безопасности нажмите кнопку Параметры, чтобы получить доступ к параметров системы и данных](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. <span data-ttu-id="9975e-127">Нажмите кнопку Создать, который имеет следующий вид: знак плюс ( **+**).</span><span class="sxs-lookup"><span data-stu-id="9975e-127">Click the new button, which resembles a plus sign ( **+**).</span></span>
    
6. <span data-ttu-id="9975e-128">В окне **новый диапазон** укажите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9975e-128">In the **New IP address range** window, specify the following values:</span></span> 
    
|<span data-ttu-id="9975e-129">**Поля или списка**</span><span class="sxs-lookup"><span data-stu-id="9975e-129">**Field or list**</span></span>|<span data-ttu-id="9975e-130">**Действия**</span><span class="sxs-lookup"><span data-stu-id="9975e-130">**What to do**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9975e-131">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9975e-131">**Name**</span></span> <br/> |<span data-ttu-id="9975e-p105">Это поле используется для управления диапазон IP-адресов и параметры. (Вы не увидите это значение в журналы действий).</span><span class="sxs-lookup"><span data-stu-id="9975e-p105">Use this field to manage your IP address range and settings. (You won't see this value in activities logs.)</span></span>  <br/> |
|<span data-ttu-id="9975e-134">**диапазоны IP-адресов**</span><span class="sxs-lookup"><span data-stu-id="9975e-134">**IP address ranges**</span></span> <br/> |<span data-ttu-id="9975e-p106">Укажите, с помощью нотации префикса сети (также известной как нотацию CIDR). Например 192.168.1.0/27 включает в себя диапазон значений 192.168.1.0 через 192.168.1.31 (включительно).</span><span class="sxs-lookup"><span data-stu-id="9975e-p106">Specify a range, using network prefix notation (also known as CIDR notation). For example, 192.168.1.0/27 includes the range of values 192.168.1.0 through 192.168.1.31 (inclusive).</span></span>  <br/> |
|<span data-ttu-id="9975e-137">**Расположение** и **зарегистрирован поставщика услуг Интернета**</span><span class="sxs-lookup"><span data-stu-id="9975e-137">**Location** and **Registered ISP**</span></span> <br/> |<span data-ttu-id="9975e-p107">Укажите расположение и службы поставщика услуг Интернета для диапазона IP-адресов. Это переопределяет открытые поля для адресов, что полезно для случаев, например, IP-адрес, который будет считаться открыто в Ирландия а на самом деле в США.</span><span class="sxs-lookup"><span data-stu-id="9975e-p107">Specify the location and Internet Service Provider (ISP) for the IP address range. This overrides the public fields defined for the addresses, which is helpful for cases, such as an IP address is that is considered publicly to be in Ireland but is actually in the U.S.</span></span>  <br/> |
|<span data-ttu-id="9975e-140">**Теги**</span><span class="sxs-lookup"><span data-stu-id="9975e-140">**Tags**</span></span> <br/> |<span data-ttu-id="9975e-p108">Использование тегов для имен групп IP-адресов. (В отличие от поля имя, вы увидите теги в журналах активности.) Введите слово или фразу, которая будет использоваться для тега. Можно добавить столько теги для каждого диапазона IP-адресов. И, если вы уже установлено тега и нужно добавить этот диапазон IP-адресов, выберите его в списке текущий тегов, которые отображаются как после начала набора текста.</span><span class="sxs-lookup"><span data-stu-id="9975e-p108">Use tags to name your groups of IP addresses. (Unlike the Name field, you will see Tags in activity logs.) Type a word or phrase that you want to use for a tag. You can add as many tags as you like for each IP address range. And if you've already set up a tag and you want to add this IP address range to it, choose it from the list of current tags that appear as you start typing.</span></span>  <br/> |
|<span data-ttu-id="9975e-145">**Категория**</span><span class="sxs-lookup"><span data-stu-id="9975e-145">**Category**</span></span> <br/> | <span data-ttu-id="9975e-p109">Назначение категорий тегов для упрощения распознает действий, полученные из определенных IP-адресов. Выбрать один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="9975e-p109">Assign categories to your tags to make it easier to recognize activities that come from certain IP addresses. Choose from the following options:  </span></span><br/> <span data-ttu-id="9975e-148">**Административные** Всех IP-адресов из вашего "Администраторы".</span><span class="sxs-lookup"><span data-stu-id="9975e-148">**Administrative** All of the IP addresses of your admins.</span></span>  <br/> <span data-ttu-id="9975e-149">**Облако поставщика** IP-адрес прокси-сервер в облаке.</span><span class="sxs-lookup"><span data-stu-id="9975e-149">**Cloud provider** The IP address of your proxy in the cloud.</span></span>  <br/> <span data-ttu-id="9975e-150">**Корпоративный** Все IP-адресов в вашей внутренней сети, филиалами и перемещения адресов Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="9975e-150">**Corporate** All of the IP addresses in your internal network, your branch offices, and your Wi-Fi roaming addresses.</span></span>  <br/> <span data-ttu-id="9975e-p110">**Рискующий** IP-адреса, исходя из опасной, такие как подозрительные IP-адресов вы видели в прошлом IP-адресов в сетях конкурентов и т. д. По умолчанию, опасные категории включает в себя два тега — IP-адрес: **анонимные прокси-сервера** и **сети**</span><span class="sxs-lookup"><span data-stu-id="9975e-p110">**Risky** Any IP addresses that you consider to be risky, such as suspicious IP addresses you've seen in the past, IP addresses in your competitors' networks, and so on. By default, the Risky categories includes two IP tags: **Anonymous proxy** and **Tor**</span></span> <br/> <span data-ttu-id="9975e-153">**Через VPN** IP-адреса, использующие удаленных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="9975e-153">**VPN** Any IP addresses that your remote workers use.</span></span>  <br/> |
   
7. <span data-ttu-id="9975e-154">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9975e-154">Choose **Save**.</span></span>
    
<span data-ttu-id="9975e-155">После настройки вашей диапазоны IP-адресов, имейте в виду, что только будущих событий влияют эти изменения.</span><span class="sxs-lookup"><span data-stu-id="9975e-155">After you set up your IP address ranges, keep in mind that only future events are affected by these changes.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="9975e-156">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9975e-156">Next steps</span></span>

- [<span data-ttu-id="9975e-157">Политики действия и оповещения</span><span class="sxs-lookup"><span data-stu-id="9975e-157">Activity policies and alerts</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="9975e-158">Функция обнаружения неполадок политик</span><span class="sxs-lookup"><span data-stu-id="9975e-158">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="9975e-159">Интеграция сервера SIEM</span><span class="sxs-lookup"><span data-stu-id="9975e-159">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="9975e-160">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9975e-160">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    

