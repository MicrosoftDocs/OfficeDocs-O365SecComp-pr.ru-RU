---
title: Вопросы и ответы по делегированному администрированию
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: В этом разделе представлены часто задаваемые вопросы и ответы для партнеров и торговых посредников Майкрософт, которые хотят делегировать задачи администрирования Office 365, в том числе возможность управления службой Exchange Online Protection (EOP) для своих клиентов (компаний).
ms.openlocfilehash: 0121c0a50e7f3ef7e5ab918a69efbd9ed609413e
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "36165645"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="3352e-103">Вопросы и ответы по делегированному администрированию</span><span class="sxs-lookup"><span data-stu-id="3352e-103">Delegated administration FAQ</span></span>

<span data-ttu-id="3352e-104">В этом разделе представлены часто задаваемые вопросы и ответы для партнеров и торговых посредников Майкрософт, которые хотят делегировать задачи администрирования Office 365, в том числе возможность управления службой Exchange Online Protection (EOP) для своих клиентов (компаний).</span><span class="sxs-lookup"><span data-stu-id="3352e-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>
  
 <span data-ttu-id="3352e-105">**В. Я торговый представитель и мне требуется управлять клиентами заказчика. Как это сделать?**</span><span class="sxs-lookup"><span data-stu-id="3352e-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>
  
<span data-ttu-id="3352e-106">О.</span><span class="sxs-lookup"><span data-stu-id="3352e-106">A.</span></span> <span data-ttu-id="3352e-107">Если вы являетесь партнером или реселлером Майкрософт, и вы вошли в систему Microsoft Advisor, вы можете запросить разрешение на администрирование своего клиента в центре администрирования.</span><span class="sxs-lookup"><span data-stu-id="3352e-107">If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the admin center.</span></span> <span data-ttu-id="3352e-108">Это называется делегированным администрированием и позволяет управлять своим клиентом Office 365 (в том числе параметрами EOP), как если бы вы были администратором в Организации.</span><span class="sxs-lookup"><span data-stu-id="3352e-108">This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization.</span></span> <span data-ttu-id="3352e-109">Ниже приведены действия для выполнения делегированного администрирования.</span><span class="sxs-lookup"><span data-stu-id="3352e-109">The steps for performing delegated administration are as follows:</span></span>
  
1. <span data-ttu-id="3352e-110">Зарегистрируйтесь, чтобы стать [консультантом по Microsoft Office 365](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="3352e-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>
    
2. <span data-ttu-id="3352e-p102">Зарегистрируйтесь для делегированного администрирования Office 365. Для возможности администрирования учетной записи клиента он должен авторизовать вас в качестве делегированного администратора. Для получения утверждения сначала отправьте заказчику [предложение о делегированном администрировании](https://go.microsoft.com/fwlink/?LinkId=396829). (Вы также можете предложить делегированное администрирование заказчику позднее.)</span><span class="sxs-lookup"><span data-stu-id="3352e-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://go.microsoft.com/fwlink/?LinkId=396829). (You can also offer delegated administration to your customer at a later time.)</span></span> 
    
3. <span data-ttu-id="3352e-115">Создайте учетную запись делегированного администратора.</span><span class="sxs-lookup"><span data-stu-id="3352e-115">Create the delegated admin account.</span></span>
    
<span data-ttu-id="3352e-116">Дополнительные сведения о настройки полномочного администрирования Office 365 см. в статье [Партнерам: ведение бизнеса и управление своей учетной записью Office 365](https://go.microsoft.com/fwlink/?LinkId=301485).</span><span class="sxs-lookup"><span data-stu-id="3352e-116">Visit [Partners: Build your business and administer your Office 365 partner account](https://go.microsoft.com/fwlink/?LinkId=301485) for more information about how to set up Office 365 delegated administration.</span></span> 
  
 <span data-ttu-id="3352e-117">**В. Я являюсь клиентом, а не торговым посредником. Как можно настроить полномочного администратора для моих подчиненных клиентов?**</span><span class="sxs-lookup"><span data-stu-id="3352e-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>
  
<span data-ttu-id="3352e-p103">О. В текущий момент делегированное администрирование доступно только для торговых посредников и партнеров. Однако мы предоставляем пример скрипта Windows PowerShell, который поможет вам применить политики к подчиненным клиентам (компаниям). Дополнительные сведения см. в разделе [Пример скрипта для применения параметров EOP к нескольким клиентам](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="3352e-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>
  
 <span data-ttu-id="3352e-122">**В. Можно ли запретить администратору подчиненного клиента изменить мою политику?**</span><span class="sxs-lookup"><span data-stu-id="3352e-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>
  
<span data-ttu-id="3352e-p104">О. Office 365 в настоящее время не поддерживает такую возможность.</span><span class="sxs-lookup"><span data-stu-id="3352e-p104">A. Office 365 does not currently have this capability.</span></span>
  
 <span data-ttu-id="3352e-125">**В. Можно ли получить консолидированный отчет для всех подчиненных клиентов?**</span><span class="sxs-lookup"><span data-stu-id="3352e-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>
  
<span data-ttu-id="3352e-126">О.</span><span class="sxs-lookup"><span data-stu-id="3352e-126">A.</span></span> <span data-ttu-id="3352e-127">Отчетность о консолидированных компаниях, которыми вы управляете, недоступна для отчетов центра администрирования Микрсофт 365 в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="3352e-127">Consolidated reporting across the companies you manage is not available for the Micrsoft 365 admin center reports at this time.</span></span> <span data-ttu-id="3352e-128">Однако его можно получить с помощью удаленной консоли Windows PowerShell или [веб-службы отчетов](https://go.microsoft.com/fwlink/?LinkId=279926).</span><span class="sxs-lookup"><span data-stu-id="3352e-128">However, this can be done via remote Windows PowerShell or the [reporting web service](https://go.microsoft.com/fwlink/?LinkId=279926).</span></span> 
  

