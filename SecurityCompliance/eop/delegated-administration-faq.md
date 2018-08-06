---
title: Вопросы и ответы по делегированному администрированию
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: В этом разделе представлены часто задаваемые вопросы и ответы для партнеров и торговых посредников Майкрософт, которые хотят делегировать задачи администрирования Office 365, в том числе возможность управления службой Exchange Online Protection (EOP) для своих клиентов (компаний).
ms.openlocfilehash: b6096e835f90a0d5f22a39a5df76e52f1a25a79d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027496"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="db13c-103">Вопросы и ответы по делегированному администрированию</span><span class="sxs-lookup"><span data-stu-id="db13c-103">Delegated administration FAQ</span></span>

<span data-ttu-id="db13c-104">В этом разделе представлены часто задаваемые вопросы и ответы для партнеров и торговых посредников Майкрософт, которые хотят делегировать задачи администрирования Office 365, в том числе возможность управления службой Exchange Online Protection (EOP) для своих клиентов (компаний).</span><span class="sxs-lookup"><span data-stu-id="db13c-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>
  
 <span data-ttu-id="db13c-105">**В. Я торговый представитель и мне требуется управлять клиентами заказчика. Как это сделать?**</span><span class="sxs-lookup"><span data-stu-id="db13c-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>
  
<span data-ttu-id="db13c-p101">О. Если вы являетесь партнером или торговым посредником корпорации Майкрософт и зарегистрировались как консультант Майкрософт, вы можете запросить разрешение на администрирование их клиентов в центре администрирования Office 365. Эта возможность называется "делегированным администрированием". Она позволяет вам управлять клиентами Office 365 (в том числе параметрами EOP) своих заказчиков, как если бы вы были администратором в их организациях. Ниже перечислены шаги по настройке делегированного администрирования.</span><span class="sxs-lookup"><span data-stu-id="db13c-p101">A. If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the Office 365 admin center. This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization. The steps for performing delegated administration are as follows:</span></span>
  
1. <span data-ttu-id="db13c-110">Зарегистрируйтесь, чтобы стать [консультантом по Microsoft Office 365](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="db13c-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>
    
2. <span data-ttu-id="db13c-p102">Зарегистрируйтесь для делегированного администрирования Office 365. Для возможности администрирования учетной записи клиента он должен авторизовать вас в качестве делегированного администратора. Для получения утверждения сначала отправьте заказчику [предложение о делегированном администрировании](https://go.microsoft.com/fwlink/?LinkId=396829). (Вы также можете предложить делегированное администрирование заказчику позднее.)</span><span class="sxs-lookup"><span data-stu-id="db13c-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://go.microsoft.com/fwlink/?LinkId=396829). (You can also offer delegated administration to your customer at a later time.)</span></span> 
    
3. <span data-ttu-id="db13c-115">Создайте учетную запись делегированного администрирования, выполнив действия из статьи [Добавление и удаление полномочного администратора](https://go.microsoft.com/fwlink/?LinkId=396831).</span><span class="sxs-lookup"><span data-stu-id="db13c-115">Create the delegated admin account using the steps documented in [Add or delete a delegated admin](https://go.microsoft.com/fwlink/?LinkId=396831).</span></span>
    
<span data-ttu-id="db13c-116">Дополнительные сведения о настройки полномочного администрирования Office 365 см. в статье [Партнерам: ведение бизнеса и управление своей учетной записью Office 365](https://go.microsoft.com/fwlink/?LinkId=301485).</span><span class="sxs-lookup"><span data-stu-id="db13c-116">Visit [Partners: Build your business and administer your Office 365 partner account](https://go.microsoft.com/fwlink/?LinkId=301485) for more information about how to set up Office 365 delegated administration.</span></span> 
  
 <span data-ttu-id="db13c-117">**В. Я являюсь клиентом, а не торговым посредником. Как можно настроить полномочного администратора для моих подчиненных клиентов?**</span><span class="sxs-lookup"><span data-stu-id="db13c-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>
  
<span data-ttu-id="db13c-p103">О. В текущий момент делегированное администрирование доступно только для торговых посредников и партнеров. Однако мы предоставляем пример скрипта Windows PowerShell, который поможет вам применить политики к подчиненным клиентам (компаниям). Дополнительные сведения см. в разделе [Пример скрипта для применения параметров EOP к нескольким клиентам](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="db13c-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>
  
 <span data-ttu-id="db13c-122">**В. Можно ли запретить администратору подчиненного клиента изменить мою политику?**</span><span class="sxs-lookup"><span data-stu-id="db13c-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>
  
<span data-ttu-id="db13c-p104">О. Office 365 в настоящее время не поддерживает такую возможность.</span><span class="sxs-lookup"><span data-stu-id="db13c-p104">A. Office 365 does not currently have this capability.</span></span>
  
 <span data-ttu-id="db13c-125">**В. Можно ли получить консолидированный отчет для всех подчиненных клиентов?**</span><span class="sxs-lookup"><span data-stu-id="db13c-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>
  
<span data-ttu-id="db13c-p105">О. В данный момент консолидированные отчеты для всех управляемых вами компаний недоступен в центре администрирования Office 365. Однако его можно получить с помощью удаленной консоли Windows PowerShell или [веб-службы отчетов](https://go.microsoft.com/fwlink/?LinkId=279926).</span><span class="sxs-lookup"><span data-stu-id="db13c-p105">A. Consolidated reporting across the companies you manage is not available for the Office 365 admin center reports at this time. However, this can be done via remote Windows PowerShell or the [reporting web service](https://go.microsoft.com/fwlink/?LinkId=279926).</span></span> 
  

