---
title: Цепочки сертификатов Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 использует ряд различных поставщиков. Ниже описаны полный перечень известных Office 365 корневые сертификаты, которые клиенты могут возникать при доступе к Office 365. Сведения о сертификатах, которые может потребоваться установить в собственную инфраструктуру, ознакомьтесь со статьей Plan стороннего SSL-сертификатов для Office 365. Следующие сведения о сертификате применяется ко всем экземплярам по всему миру и Национальный облака Office 365.
ms.openlocfilehash: 1dcc2dc38bb8e3239a3be3983791b0c60917dc5e
ms.sourcegitcommit: 13f40ff7c1799152bf45af2d8110f4f3235b770a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2018
ms.locfileid: "25549769"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="86a92-106">Цепочки сертификатов Office 365</span><span class="sxs-lookup"><span data-stu-id="86a92-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="86a92-p102">Office 365 использует ряд различных поставщиков. Ниже описаны полный перечень известных Office 365 корневые сертификаты, которые клиенты могут возникать при доступе к Office 365. Сведения о сертификатах, может потребоваться установить в собственную инфраструктуру содержатся в разделе [Планирование сторонних SSL-сертификатов для Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Следующие сведения о сертификате применяется ко всем экземплярам по всему миру и Национальный облака Office 365.</span><span class="sxs-lookup"><span data-stu-id="86a92-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="86a92-111">**Тип сертификата**</span><span class="sxs-lookup"><span data-stu-id="86a92-111">**Certificate type**</span></span>|<span data-ttu-id="86a92-112">**P7b – загрузить (en)**</span><span class="sxs-lookup"><span data-stu-id="86a92-112">**P7b download**</span></span>|<span data-ttu-id="86a92-113">**Конечные точки списка отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-113">**CRL Endpoints**</span></span>|<span data-ttu-id="86a92-114">**Конечные точки OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="86a92-115">**Конечные точки Местоположений**</span><span class="sxs-lookup"><span data-stu-id="86a92-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="86a92-116">Общедоступные доверенные корневые сертификаты</span><span class="sxs-lookup"><span data-stu-id="86a92-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="86a92-117">Office 365 корневой сертификат набора (p7b –)</span><span class="sxs-lookup"><span data-stu-id="86a92-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="86a92-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="86a92-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="86a92-120">Недоступно</span><span class="sxs-lookup"><span data-stu-id="86a92-120">N/A</span></span>  <br/> |<span data-ttu-id="86a92-121">Недоступно</span><span class="sxs-lookup"><span data-stu-id="86a92-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="86a92-122">Общедоступные надежные промежуточных сертификатов</span><span class="sxs-lookup"><span data-stu-id="86a92-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="86a92-123">Набор Office 365 промежуточных сертификатах (p7b –)</span><span class="sxs-lookup"><span data-stu-id="86a92-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="86a92-124">cdp1.public trust.com</span><span class="sxs-lookup"><span data-stu-id="86a92-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="86a92-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="86a92-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="86a92-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="86a92-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="86a92-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="86a92-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="86a92-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="86a92-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="86a92-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="86a92-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="86a92-131">crl3.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="86a92-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="86a92-132">crl4.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="86a92-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="86a92-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="86a92-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="86a92-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="86a92-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="86a92-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="86a92-136">OCSP.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="86a92-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="86a92-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="86a92-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="86a92-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="86a92-139">OCSP.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="86a92-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="86a92-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="86a92-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="86a92-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="86a92-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="86a92-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="86a92-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="86a92-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="86a92-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="86a92-144">корневой c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="86a92-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="86a92-145">root-C3-cA2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="86a92-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="86a92-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="86a92-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="86a92-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="86a92-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="86a92-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="86a92-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="86a92-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="86a92-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="86a92-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="86a92-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="86a92-151">Разверните корневой и промежуточные разделах ниже, чтобы просмотреть дополнительные сведения о поставщиках сертификата.</span><span class="sxs-lookup"><span data-stu-id="86a92-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="86a92-152">Сведения о сертификате корневого Office 365</span><span class="sxs-lookup"><span data-stu-id="86a92-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="86a92-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="86a92-153"></span></span>

 <span data-ttu-id="86a92-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="86a92-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="86a92-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="86a92-155">|:-----|</span></span>
|<span data-ttu-id="86a92-156">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="86a92-157">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-157">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-158">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-158"></span></span>|
|<span data-ttu-id="86a92-159">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-159">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-160">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-160"></span></span>|
|<span data-ttu-id="86a92-161">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-162">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-162"></span></span>|
|<span data-ttu-id="86a92-163">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-164">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-164"></span></span>|
|<span data-ttu-id="86a92-165">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-165">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-166">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-166"></span></span>|
|<span data-ttu-id="86a92-167">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-168">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-168"></span></span>|
|<span data-ttu-id="86a92-169">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-170">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-170"></span></span>|
|<span data-ttu-id="86a92-171">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-172">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-172"></span></span>|
|<span data-ttu-id="86a92-173">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-174">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-174"></span></span>|
   
 <span data-ttu-id="86a92-175">**КОРНЕВОЙ CNNIC**</span><span class="sxs-lookup"><span data-stu-id="86a92-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-176">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-176">**Subject**</span></span>|
|<span data-ttu-id="86a92-177">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-177"></span></span>|
|<span data-ttu-id="86a92-178">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-178">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-179">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-179"></span></span>|
|<span data-ttu-id="86a92-180">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-180">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-181">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-181"></span></span>|
|<span data-ttu-id="86a92-182">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-183">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-183"></span></span>|
|<span data-ttu-id="86a92-184">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-185">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-185"></span></span>|
|<span data-ttu-id="86a92-186">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-186">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-187">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-187"></span></span>|
|<span data-ttu-id="86a92-188">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-189">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-189"></span></span>|
|<span data-ttu-id="86a92-190">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-191">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-191"></span></span>|
|<span data-ttu-id="86a92-192">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-193">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-193"></span></span>|
|<span data-ttu-id="86a92-194">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-195">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-195"></span></span>|
|<span data-ttu-id="86a92-196">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-197">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-197"></span></span>|
   
 <span data-ttu-id="86a92-198">**DigiCert глобального корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="86a92-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-199">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-199">**Subject**</span></span>|
|<span data-ttu-id="86a92-200">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-200"></span></span>|
|<span data-ttu-id="86a92-201">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-201">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-202">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-202"></span></span>|
|<span data-ttu-id="86a92-203">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-203">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-204">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-204"></span></span>|
|<span data-ttu-id="86a92-205">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-206">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-206"></span></span>|
|<span data-ttu-id="86a92-207">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-208">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-208"></span></span>|
|<span data-ttu-id="86a92-209">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-209">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-210">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-210"></span></span>|
|<span data-ttu-id="86a92-211">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-212">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-212"></span></span>|
|<span data-ttu-id="86a92-213">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-214">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-214"></span></span>|
|<span data-ttu-id="86a92-215">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-216">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-216"></span></span>|
|<span data-ttu-id="86a92-217">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-218">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-218"></span></span>|
|<span data-ttu-id="86a92-219">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-220">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-220"></span></span>|
   
 <span data-ttu-id="86a92-221">**Сертификат DigiCert высокой надежности корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="86a92-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-222">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-222">**Subject**</span></span>|
|<span data-ttu-id="86a92-223">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-223"></span></span>|
|<span data-ttu-id="86a92-224">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-224">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-225">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-225"></span></span>|
|<span data-ttu-id="86a92-226">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-226">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-227">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-227"></span></span>|
|<span data-ttu-id="86a92-228">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-229">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-229"></span></span>|
|<span data-ttu-id="86a92-230">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-231">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-231"></span></span>|
|<span data-ttu-id="86a92-232">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-232">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-233">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-233"></span></span>|
|<span data-ttu-id="86a92-234">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-235">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-235"></span></span>|
|<span data-ttu-id="86a92-236">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-237">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-237"></span></span>|
|<span data-ttu-id="86a92-238">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-239">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-239"></span></span>|
|<span data-ttu-id="86a92-240">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-241">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-241"></span></span>|
|<span data-ttu-id="86a92-242">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-243">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-243"></span></span>|
   
 <span data-ttu-id="86a92-244">**Центр сертификации Class 3 корневого ДОВЕРИЯ D 2 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="86a92-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-245">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-245">**Subject**</span></span>|
|<span data-ttu-id="86a92-246">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-246"></span></span>|
|<span data-ttu-id="86a92-247">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-247">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-248">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-248"></span></span>|
|<span data-ttu-id="86a92-249">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-249">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-250">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-250"></span></span>|
|<span data-ttu-id="86a92-251">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-252">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-252"></span></span>|
|<span data-ttu-id="86a92-253">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-254">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-254"></span></span>|
|<span data-ttu-id="86a92-255">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-255">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-256">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-256"></span></span>|
|<span data-ttu-id="86a92-257">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-258">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-258"></span></span>|
|<span data-ttu-id="86a92-259">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-260">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-260"></span></span>|
|<span data-ttu-id="86a92-261">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-262">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-262"></span></span>|
|<span data-ttu-id="86a92-263">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-264">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-264"></span></span>|
|<span data-ttu-id="86a92-265">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-265">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-266">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-266"></span></span>|
   
 <span data-ttu-id="86a92-267">**Центр сертификации Class 3 корневого ДОВЕРИЯ D 2 высокой Надежности 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="86a92-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-268">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-268">**Subject**</span></span>|
|<span data-ttu-id="86a92-269">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-269"></span></span>|
|<span data-ttu-id="86a92-270">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-270">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-271">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-271"></span></span>|
|<span data-ttu-id="86a92-272">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-272">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-273">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-273"></span></span>|
|<span data-ttu-id="86a92-274">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-275">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-275"></span></span>|
|<span data-ttu-id="86a92-276">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-277">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-277"></span></span>|
|<span data-ttu-id="86a92-278">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-278">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-279">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-279"></span></span>|
|<span data-ttu-id="86a92-280">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-281">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-281"></span></span>|
|<span data-ttu-id="86a92-282">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-283">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-283"></span></span>|
|<span data-ttu-id="86a92-284">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-285">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-285"></span></span>|
|<span data-ttu-id="86a92-286">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-287">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-287"></span></span>|
|<span data-ttu-id="86a92-288">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-288">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-289">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-289"></span></span>|
   
 <span data-ttu-id="86a92-290">**Переход на летнее время корневого ЦС X3**</span><span class="sxs-lookup"><span data-stu-id="86a92-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-291">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-291">**Subject**</span></span>|
|<span data-ttu-id="86a92-292">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-292"></span></span>|
|<span data-ttu-id="86a92-293">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-293">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-294">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-294"></span></span>|
|<span data-ttu-id="86a92-295">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-295">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-296">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-296"></span></span>|
|<span data-ttu-id="86a92-297">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-298">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-298"></span></span>|
|<span data-ttu-id="86a92-299">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-300">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-300"></span></span>|
|<span data-ttu-id="86a92-301">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-301">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-302">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-302"></span></span>|
|<span data-ttu-id="86a92-303">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-304">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-304"></span></span>|
|<span data-ttu-id="86a92-305">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-306">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-306"></span></span>|
|<span data-ttu-id="86a92-307">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-308">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-308"></span></span>|
|<span data-ttu-id="86a92-309">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-310">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-310"></span></span>|
   
 <span data-ttu-id="86a92-311">**Доверенный корневой центр сертификации - G2**</span><span class="sxs-lookup"><span data-stu-id="86a92-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-312">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-312">**Subject**</span></span>|
|<span data-ttu-id="86a92-313">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-313"></span></span>|
|<span data-ttu-id="86a92-314">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-314">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-315">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-315"></span></span>|
|<span data-ttu-id="86a92-316">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-316">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-317">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-317"></span></span>|
|<span data-ttu-id="86a92-318">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-319">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-319"></span></span>|
|<span data-ttu-id="86a92-320">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-321">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-321"></span></span>|
|<span data-ttu-id="86a92-322">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-322">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-323">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-323"></span></span>|
|<span data-ttu-id="86a92-324">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-325">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-325"></span></span>|
|<span data-ttu-id="86a92-326">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-327">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-327"></span></span>|
|<span data-ttu-id="86a92-328">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-329">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-329"></span></span>|
|<span data-ttu-id="86a92-330">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-331">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-331"></span></span>|
   
 <span data-ttu-id="86a92-332">**Центр сертификации Entrust.NET (2048)**</span><span class="sxs-lookup"><span data-stu-id="86a92-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-333">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-333">**Subject**</span></span>|
|<span data-ttu-id="86a92-334">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-334"></span></span>|
|<span data-ttu-id="86a92-335">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-335">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-336">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-336"></span></span>|
|<span data-ttu-id="86a92-337">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-337">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-338">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-338"></span></span>|
|<span data-ttu-id="86a92-339">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-340">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-340"></span></span>|
|<span data-ttu-id="86a92-341">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-342">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-342"></span></span>|
|<span data-ttu-id="86a92-343">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-343">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-344">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-344"></span></span>|
|<span data-ttu-id="86a92-345">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-346">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-346"></span></span>|
|<span data-ttu-id="86a92-347">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-348">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-348"></span></span>|
|<span data-ttu-id="86a92-349">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-350">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-350"></span></span>|
|<span data-ttu-id="86a92-351">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-352">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-352"></span></span>|
   
 <span data-ttu-id="86a92-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="86a92-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-354">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-354">**Subject**</span></span>|
|<span data-ttu-id="86a92-355">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-355"></span></span>|
|<span data-ttu-id="86a92-356">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-356">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-357">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-357"></span></span>|
|<span data-ttu-id="86a92-358">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-358">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-359">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-359"></span></span>|
|<span data-ttu-id="86a92-360">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-361">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-361"></span></span>|
|<span data-ttu-id="86a92-362">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-363">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-363"></span></span>|
|<span data-ttu-id="86a92-364">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-364">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-365">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-365"></span></span>|
|<span data-ttu-id="86a92-366">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-367">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-367"></span></span>|
|<span data-ttu-id="86a92-368">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-369">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-369"></span></span>|
|<span data-ttu-id="86a92-370">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-371">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-371"></span></span>|
|<span data-ttu-id="86a92-372">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-373">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-373"></span></span>|
|<span data-ttu-id="86a92-374">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-375">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-375"></span></span>|
|<span data-ttu-id="86a92-376">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-376">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-377">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-377"></span></span>|
   
 <span data-ttu-id="86a92-378">**GlobalSign корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="86a92-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-379">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-379">**Subject**</span></span>|
|<span data-ttu-id="86a92-380">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-380"></span></span>|
|<span data-ttu-id="86a92-381">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-381">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-382">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-382"></span></span>|
|<span data-ttu-id="86a92-383">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-383">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-384">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-384"></span></span>|
|<span data-ttu-id="86a92-385">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-386">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-386"></span></span>|
|<span data-ttu-id="86a92-387">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-388">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-388"></span></span>|
|<span data-ttu-id="86a92-389">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-389">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-390">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-390"></span></span>|
|<span data-ttu-id="86a92-391">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-392">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-392"></span></span>|
|<span data-ttu-id="86a92-393">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-394">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-394"></span></span>|
|<span data-ttu-id="86a92-395">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-396">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-396"></span></span>|
|<span data-ttu-id="86a92-397">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-398">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-398"></span></span>|
   
 <span data-ttu-id="86a92-399">**Thawte основной корневого ЦС - G3**</span><span class="sxs-lookup"><span data-stu-id="86a92-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-400">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-400">**Subject**</span></span>|
|<span data-ttu-id="86a92-401">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-401"></span></span>|
|<span data-ttu-id="86a92-402">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-402">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-403">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-403"></span></span>|
|<span data-ttu-id="86a92-404">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-404">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-405">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-405"></span></span>|
|<span data-ttu-id="86a92-406">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-407">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-407"></span></span>|
|<span data-ttu-id="86a92-408">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-409">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-409"></span></span>|
|<span data-ttu-id="86a92-410">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-410">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-411">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-411"></span></span>|
|<span data-ttu-id="86a92-412">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-413">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-413"></span></span>|
|<span data-ttu-id="86a92-414">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-415">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-415"></span></span>|
|<span data-ttu-id="86a92-416">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-417">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-417"></span></span>|
|<span data-ttu-id="86a92-418">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-419">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-419"></span></span>|
   
 <span data-ttu-id="86a92-420">**Главный общедоступный ЦС класса VeriSign 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="86a92-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-421">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-421">**Subject**</span></span>|
|<span data-ttu-id="86a92-422">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-422"></span></span>|
|<span data-ttu-id="86a92-423">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-423">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-424">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-424"></span></span>|
|<span data-ttu-id="86a92-425">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-425">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-426">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-426"></span></span>|
|<span data-ttu-id="86a92-427">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-428">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-428"></span></span>|
|<span data-ttu-id="86a92-429">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-430">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-430"></span></span>|
|<span data-ttu-id="86a92-431">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-431">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-432">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-432"></span></span>|
|<span data-ttu-id="86a92-433">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-434">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-434"></span></span>|
|<span data-ttu-id="86a92-435">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-436">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-436"></span></span>|
|<span data-ttu-id="86a92-437">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-438">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-438"></span></span>|
|<span data-ttu-id="86a92-439">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-440">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="86a92-441">Сведения о промежуточных сертификатах Office 365</span><span class="sxs-lookup"><span data-stu-id="86a92-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="86a92-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="86a92-442"></span></span>

 <span data-ttu-id="86a92-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="86a92-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-444">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-444">**Subject**</span></span>|
|<span data-ttu-id="86a92-445">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-445"></span></span>|
|<span data-ttu-id="86a92-446">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-446">**Issuer**</span></span>|
|<span data-ttu-id="86a92-447">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-447"></span></span>|
|<span data-ttu-id="86a92-448">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-448">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-449">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-449"></span></span>|
|<span data-ttu-id="86a92-450">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-450">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-451">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-451"></span></span>|
|<span data-ttu-id="86a92-452">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-453">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-453"></span></span>|
|<span data-ttu-id="86a92-454">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-455">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-455"></span></span>|
|<span data-ttu-id="86a92-456">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-456">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-457">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-457"></span></span>|
|<span data-ttu-id="86a92-458">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-459">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-459"></span></span>|
|<span data-ttu-id="86a92-460">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-461">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-461"></span></span>|
|<span data-ttu-id="86a92-462">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-463">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-463"></span></span>|
|<span data-ttu-id="86a92-464">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-465">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-465"></span></span>|
|<span data-ttu-id="86a92-466">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-467">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-467"></span></span>|
|<span data-ttu-id="86a92-468">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="86a92-468">**AIA URLs**</span></span>|
|<span data-ttu-id="86a92-469">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-469"></span></span>|
|<span data-ttu-id="86a92-470">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-470">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-471">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-471"></span></span>|
|<span data-ttu-id="86a92-472">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-473">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-473"></span></span>|
   
 <span data-ttu-id="86a92-474">**Центра сертификации Class 3 D-TRUST SSL 1 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="86a92-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-475">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-475">**Subject**</span></span>|
|<span data-ttu-id="86a92-476">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-476"></span></span>|
|<span data-ttu-id="86a92-477">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-477">**Issuer**</span></span>|
|<span data-ttu-id="86a92-478">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-478"></span></span>|
|<span data-ttu-id="86a92-479">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="86a92-480">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-480"></span></span>|
|<span data-ttu-id="86a92-481">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-481">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-482">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-482"></span></span>|
|<span data-ttu-id="86a92-483">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-483">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-484">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-484"></span></span>|
|<span data-ttu-id="86a92-485">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-486">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-486"></span></span>|
|<span data-ttu-id="86a92-487">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-488">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-488"></span></span>|
|<span data-ttu-id="86a92-489">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-489">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-490">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-490"></span></span>|
|<span data-ttu-id="86a92-491">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-492">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-492"></span></span>|
|<span data-ttu-id="86a92-493">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-494">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-494"></span></span>|
|<span data-ttu-id="86a92-495">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-496">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-496"></span></span>|
|<span data-ttu-id="86a92-497">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-498">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-498"></span></span>|
|<span data-ttu-id="86a92-499">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-500">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-500"></span></span>|
|<span data-ttu-id="86a92-501">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-501">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-502">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-502"></span></span>|
|<span data-ttu-id="86a92-503">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-504">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-504"></span></span>|
   
 <span data-ttu-id="86a92-505">**Центра сертификации Class 3 D-TRUST SSL 1 высокой Надежности 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="86a92-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-506">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-506">**Subject**</span></span>|
|<span data-ttu-id="86a92-507">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-507"></span></span>|
|<span data-ttu-id="86a92-508">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-508">**Issuer**</span></span>|
|<span data-ttu-id="86a92-509">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-509"></span></span>|
|<span data-ttu-id="86a92-510">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="86a92-511">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-511"></span></span>|
|<span data-ttu-id="86a92-512">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-512">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-513">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-513"></span></span>|
|<span data-ttu-id="86a92-514">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-514">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-515">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-515"></span></span>|
|<span data-ttu-id="86a92-516">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-517">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-517"></span></span>|
|<span data-ttu-id="86a92-518">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-519">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-519"></span></span>|
|<span data-ttu-id="86a92-520">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-520">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-521">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-521"></span></span>|
|<span data-ttu-id="86a92-522">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-523">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-523"></span></span>|
|<span data-ttu-id="86a92-524">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-525">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-525"></span></span>|
|<span data-ttu-id="86a92-526">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-527">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-527"></span></span>|
|<span data-ttu-id="86a92-528">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-529">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-529"></span></span>|
|<span data-ttu-id="86a92-530">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-531">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-531"></span></span>|
|<span data-ttu-id="86a92-532">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-532">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-533">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-533"></span></span>|
|<span data-ttu-id="86a92-534">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-535">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-535"></span></span>|
   
 <span data-ttu-id="86a92-536">**DigiCert облачным службам ЦС-1**</span><span class="sxs-lookup"><span data-stu-id="86a92-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-537">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-537">**Subject**</span></span>|
|<span data-ttu-id="86a92-538">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-538"></span></span>|
|<span data-ttu-id="86a92-539">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-539">**Issuer**</span></span>|
|<span data-ttu-id="86a92-540">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-540"></span></span>|
|<span data-ttu-id="86a92-541">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-541">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-542">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-542"></span></span>|
|<span data-ttu-id="86a92-543">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-543">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-544">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-544"></span></span>|
|<span data-ttu-id="86a92-545">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-546">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-546"></span></span>|
|<span data-ttu-id="86a92-547">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-548">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-548"></span></span>|
|<span data-ttu-id="86a92-549">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-549">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-550">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-550"></span></span>|
|<span data-ttu-id="86a92-551">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-552">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-552"></span></span>|
|<span data-ttu-id="86a92-553">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-554">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-554"></span></span>|
|<span data-ttu-id="86a92-555">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-556">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-556"></span></span>|
|<span data-ttu-id="86a92-557">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-558">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-558"></span></span>|
|<span data-ttu-id="86a92-559">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-560">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-560"></span></span>|
|<span data-ttu-id="86a92-561">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-561">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-562">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-562"></span></span>|
|<span data-ttu-id="86a92-563">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-564">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-564"></span></span>|
   
 <span data-ttu-id="86a92-565">**DigiCert SHA2 высокой надежности сервера центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-566">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-566">**Subject**</span></span>|
|<span data-ttu-id="86a92-567">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-567"></span></span>|
|<span data-ttu-id="86a92-568">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-568">**Issuer**</span></span>|
|<span data-ttu-id="86a92-569">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-569"></span></span>|
|<span data-ttu-id="86a92-570">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-570">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-571">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-571"></span></span>|
|<span data-ttu-id="86a92-572">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-572">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-573">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-573"></span></span>|
|<span data-ttu-id="86a92-574">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-575">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-575"></span></span>|
|<span data-ttu-id="86a92-576">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-577">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-577"></span></span>|
|<span data-ttu-id="86a92-578">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-578">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-579">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-579"></span></span>|
|<span data-ttu-id="86a92-580">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-581">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-581"></span></span>|
|<span data-ttu-id="86a92-582">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-583">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-583"></span></span>|
|<span data-ttu-id="86a92-584">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-585">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-585"></span></span>|
|<span data-ttu-id="86a92-586">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-587">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-587"></span></span>|
|<span data-ttu-id="86a92-588">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-589">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-589"></span></span>|
|<span data-ttu-id="86a92-590">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-590">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-591">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-591"></span></span>|
|<span data-ttu-id="86a92-592">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-593">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-593"></span></span>|
   
 <span data-ttu-id="86a92-594">**Безопасный сервер DigiCert SHA2 ЦС**</span><span class="sxs-lookup"><span data-stu-id="86a92-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-595">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-595">**Subject**</span></span>|
|<span data-ttu-id="86a92-596">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-596"></span></span>|
|<span data-ttu-id="86a92-597">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-597">**Issuer**</span></span>|
|<span data-ttu-id="86a92-598">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-598"></span></span>|
|<span data-ttu-id="86a92-599">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-599">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-600">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-600"></span></span>|
|<span data-ttu-id="86a92-601">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-601">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-602">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-602"></span></span>|
|<span data-ttu-id="86a92-603">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-604">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-604"></span></span>|
|<span data-ttu-id="86a92-605">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-606">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-606"></span></span>|
|<span data-ttu-id="86a92-607">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-607">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-608">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-608"></span></span>|
|<span data-ttu-id="86a92-609">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-610">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-610"></span></span>|
|<span data-ttu-id="86a92-611">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-612">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-612"></span></span>|
|<span data-ttu-id="86a92-613">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-614">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-614"></span></span>|
|<span data-ttu-id="86a92-615">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-616">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-616"></span></span>|
|<span data-ttu-id="86a92-617">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-618">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-618"></span></span>|
|<span data-ttu-id="86a92-619">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-619">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-620">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-620"></span></span>|
|<span data-ttu-id="86a92-621">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-622">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-622"></span></span>|
   
 <span data-ttu-id="86a92-623">**Доверенный центр сертификации - L1C**</span><span class="sxs-lookup"><span data-stu-id="86a92-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-624">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-624">**Subject**</span></span>|
|<span data-ttu-id="86a92-625">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-625"></span></span>|
|<span data-ttu-id="86a92-626">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-626">**Issuer**</span></span>|
|<span data-ttu-id="86a92-627">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-627"></span></span>|
|<span data-ttu-id="86a92-628">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-628">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-629">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-629"></span></span>|
|<span data-ttu-id="86a92-630">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-630">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-631">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-631"></span></span>|
|<span data-ttu-id="86a92-632">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-633">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-633"></span></span>|
|<span data-ttu-id="86a92-634">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-635">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-635"></span></span>|
|<span data-ttu-id="86a92-636">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-636">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-637">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-637"></span></span>|
|<span data-ttu-id="86a92-638">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-639">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-639"></span></span>|
|<span data-ttu-id="86a92-640">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-641">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-641"></span></span>|
|<span data-ttu-id="86a92-642">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-643">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-643"></span></span>|
|<span data-ttu-id="86a92-644">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-645">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-645"></span></span>|
|<span data-ttu-id="86a92-646">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-647">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-647"></span></span>|
|<span data-ttu-id="86a92-648">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-648">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-649">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-649"></span></span>|
|<span data-ttu-id="86a92-650">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-651">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-651"></span></span>|
   
 <span data-ttu-id="86a92-652">**Доверенный центр сертификации - L1K**</span><span class="sxs-lookup"><span data-stu-id="86a92-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-653">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-653">**Subject**</span></span>|
|<span data-ttu-id="86a92-654">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-654"></span></span>|
|<span data-ttu-id="86a92-655">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-655">**Issuer**</span></span>|
|<span data-ttu-id="86a92-656">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-656"></span></span>|
|<span data-ttu-id="86a92-657">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-657">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-658">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-658"></span></span>|
|<span data-ttu-id="86a92-659">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-659">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-660">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-660"></span></span>|
|<span data-ttu-id="86a92-661">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-662">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-662"></span></span>|
|<span data-ttu-id="86a92-663">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-664">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-664"></span></span>|
|<span data-ttu-id="86a92-665">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-665">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-666">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-666"></span></span>|
|<span data-ttu-id="86a92-667">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-668">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-668"></span></span>|
|<span data-ttu-id="86a92-669">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-670">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-670"></span></span>|
|<span data-ttu-id="86a92-671">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-672">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-672"></span></span>|
|<span data-ttu-id="86a92-673">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-674">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-674"></span></span>|
|<span data-ttu-id="86a92-675">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-676">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-676"></span></span>|
|<span data-ttu-id="86a92-677">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-677">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-678">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-678"></span></span>|
|<span data-ttu-id="86a92-679">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-680">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-680"></span></span>|
   
 <span data-ttu-id="86a92-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="86a92-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-682">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-682">**Subject**</span></span>|
|<span data-ttu-id="86a92-683">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-683"></span></span>|
|<span data-ttu-id="86a92-684">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-684">**Issuer**</span></span>|
|<span data-ttu-id="86a92-685">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-685"></span></span>|
|<span data-ttu-id="86a92-686">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-686">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-687">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-687"></span></span>|
|<span data-ttu-id="86a92-688">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-688">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-689">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-689"></span></span>|
|<span data-ttu-id="86a92-690">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-691">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-691"></span></span>|
|<span data-ttu-id="86a92-692">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-693">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-693"></span></span>|
|<span data-ttu-id="86a92-694">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-694">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-695">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-695"></span></span>|
|<span data-ttu-id="86a92-696">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-697">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-697"></span></span>|
|<span data-ttu-id="86a92-698">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-699">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-699"></span></span>|
|<span data-ttu-id="86a92-700">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-701">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-701"></span></span>|
|<span data-ttu-id="86a92-702">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-703">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-703"></span></span>|
|<span data-ttu-id="86a92-704">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-705">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-705"></span></span>|
|<span data-ttu-id="86a92-706">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-706">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-707">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-707"></span></span>|
|<span data-ttu-id="86a92-708">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-709">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-709"></span></span>|
   
 <span data-ttu-id="86a92-710">**Расширенные проверки ЦС - SHA256 - G2 GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="86a92-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-711">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-711">**Subject**</span></span>|
|<span data-ttu-id="86a92-712">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-712"></span></span>|
|<span data-ttu-id="86a92-713">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-713">**Issuer**</span></span>|
|<span data-ttu-id="86a92-714">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-714"></span></span>|
|<span data-ttu-id="86a92-715">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-715">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-716">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-716"></span></span>|
|<span data-ttu-id="86a92-717">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-717">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-718">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-718"></span></span>|
|<span data-ttu-id="86a92-719">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-720">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-720"></span></span>|
|<span data-ttu-id="86a92-721">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-722">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-722"></span></span>|
|<span data-ttu-id="86a92-723">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-723">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-724">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-724"></span></span>|
|<span data-ttu-id="86a92-725">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-726">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-726"></span></span>|
|<span data-ttu-id="86a92-727">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-728">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-728"></span></span>|
|<span data-ttu-id="86a92-729">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-730">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-730"></span></span>|
|<span data-ttu-id="86a92-731">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-732">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-732"></span></span>|
|<span data-ttu-id="86a92-733">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-734">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-734"></span></span>|
|<span data-ttu-id="86a92-735">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-735">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-736">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-736"></span></span>|
|<span data-ttu-id="86a92-737">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-738">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-738"></span></span>|
   
 <span data-ttu-id="86a92-739">**Расширенные проверки ЦС - SHA256 - G3 GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="86a92-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-740">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-740">**Subject**</span></span>|
|<span data-ttu-id="86a92-741">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-741"></span></span>|
|<span data-ttu-id="86a92-742">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-742">**Issuer**</span></span>|
|<span data-ttu-id="86a92-743">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-743"></span></span>|
|<span data-ttu-id="86a92-744">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-744">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-745">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-745"></span></span>|
|<span data-ttu-id="86a92-746">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-746">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-747">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-747"></span></span>|
|<span data-ttu-id="86a92-748">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-749">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-749"></span></span>|
|<span data-ttu-id="86a92-750">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-751">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-751"></span></span>|
|<span data-ttu-id="86a92-752">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-752">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-753">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-753"></span></span>|
|<span data-ttu-id="86a92-754">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-755">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-755"></span></span>|
|<span data-ttu-id="86a92-756">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-757">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-757"></span></span>|
|<span data-ttu-id="86a92-758">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-759">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-759"></span></span>|
|<span data-ttu-id="86a92-760">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-761">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-761"></span></span>|
|<span data-ttu-id="86a92-762">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-763">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-763"></span></span>|
|<span data-ttu-id="86a92-764">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-764">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-765">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-765"></span></span>|
|<span data-ttu-id="86a92-766">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-767">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-767"></span></span>|
   
 <span data-ttu-id="86a92-768">**GlobalSign организации проверки ЦС - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="86a92-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-769">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-769">**Subject**</span></span>|
|<span data-ttu-id="86a92-770">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-770"></span></span>|
|<span data-ttu-id="86a92-771">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-771">**Issuer**</span></span>|
|<span data-ttu-id="86a92-772">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-772"></span></span>|
|<span data-ttu-id="86a92-773">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-773">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-774">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-774"></span></span>|
|<span data-ttu-id="86a92-775">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-775">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-776">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-776"></span></span>|
|<span data-ttu-id="86a92-777">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-778">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-778"></span></span>|
|<span data-ttu-id="86a92-779">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-780">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-780"></span></span>|
|<span data-ttu-id="86a92-781">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-781">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-782">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-782"></span></span>|
|<span data-ttu-id="86a92-783">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-784">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-784"></span></span>|
|<span data-ttu-id="86a92-785">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-786">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-786"></span></span>|
|<span data-ttu-id="86a92-787">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-788">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-788"></span></span>|
|<span data-ttu-id="86a92-789">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-790">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-790"></span></span>|
|<span data-ttu-id="86a92-791">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-792">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-792"></span></span>|
|<span data-ttu-id="86a92-793">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-793">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-794">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-794"></span></span>|
|<span data-ttu-id="86a92-795">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-796">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-796"></span></span>|
   
 <span data-ttu-id="86a92-797">**GlobalSign организации проверки ЦС - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="86a92-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-798">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-798">**Subject**</span></span>|
|<span data-ttu-id="86a92-799">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-799"></span></span>|
|<span data-ttu-id="86a92-800">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-800">**Issuer**</span></span>|
|<span data-ttu-id="86a92-801">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-801"></span></span>|
|<span data-ttu-id="86a92-802">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-802">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-803">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-803"></span></span>|
|<span data-ttu-id="86a92-804">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-804">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-805">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-805"></span></span>|
|<span data-ttu-id="86a92-806">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-807">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-807"></span></span>|
|<span data-ttu-id="86a92-808">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-809">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-809"></span></span>|
|<span data-ttu-id="86a92-810">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-810">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-811">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-811"></span></span>|
|<span data-ttu-id="86a92-812">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-813">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-813"></span></span>|
|<span data-ttu-id="86a92-814">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-815">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-815"></span></span>|
|<span data-ttu-id="86a92-816">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-817">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-817"></span></span>|
|<span data-ttu-id="86a92-818">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-819">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-819"></span></span>|
|<span data-ttu-id="86a92-820">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-821">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-821"></span></span>|
|<span data-ttu-id="86a92-822">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-822">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-823">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-823"></span></span>|
|<span data-ttu-id="86a92-824">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-825">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-825"></span></span>|
   
 <span data-ttu-id="86a92-826">**Давайте шифрования центра сертификации X3**</span><span class="sxs-lookup"><span data-stu-id="86a92-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-827">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-827">**Subject**</span></span>|
|<span data-ttu-id="86a92-828">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-828"></span></span>|
|<span data-ttu-id="86a92-829">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-829">**Issuer**</span></span>|
|<span data-ttu-id="86a92-830">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-830"></span></span>|
|<span data-ttu-id="86a92-831">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-831">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-832">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-832"></span></span>|
|<span data-ttu-id="86a92-833">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-833">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-834">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-834"></span></span>|
|<span data-ttu-id="86a92-835">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-836">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-836"></span></span>|
|<span data-ttu-id="86a92-837">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-838">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-838"></span></span>|
|<span data-ttu-id="86a92-839">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-839">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-840">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-840"></span></span>|
|<span data-ttu-id="86a92-841">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-842">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-842"></span></span>|
|<span data-ttu-id="86a92-843">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-844">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-844"></span></span>|
|<span data-ttu-id="86a92-845">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-846">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-846"></span></span>|
|<span data-ttu-id="86a92-847">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-848">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-848"></span></span>|
|<span data-ttu-id="86a92-849">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-850">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-850"></span></span>|
|<span data-ttu-id="86a92-851">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="86a92-851">**AIA URLs**</span></span>|
|<span data-ttu-id="86a92-852">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-852"></span></span>|
|<span data-ttu-id="86a92-853">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-853">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-854">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-854"></span></span>|
|<span data-ttu-id="86a92-855">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-856">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-856"></span></span>|
   
 <span data-ttu-id="86a92-857">**SHA2 SSL ИТ-отдела Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="86a92-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-858">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-858">**Subject**</span></span>|
|<span data-ttu-id="86a92-859">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-859"></span></span>|
|<span data-ttu-id="86a92-860">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-860">**Issuer**</span></span>|
|<span data-ttu-id="86a92-861">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-861"></span></span>|
|<span data-ttu-id="86a92-862">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-862">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-863">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-863"></span></span>|
|<span data-ttu-id="86a92-864">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-864">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-865">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-865"></span></span>|
|<span data-ttu-id="86a92-866">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-867">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-867"></span></span>|
|<span data-ttu-id="86a92-868">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-869">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-869"></span></span>|
|<span data-ttu-id="86a92-870">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-870">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-871">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-871"></span></span>|
|<span data-ttu-id="86a92-872">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-873">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-873"></span></span>|
|<span data-ttu-id="86a92-874">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-875">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-875"></span></span>|
|<span data-ttu-id="86a92-876">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-877">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-877"></span></span>|
|<span data-ttu-id="86a92-878">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-879">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-879"></span></span>|
|<span data-ttu-id="86a92-880">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-881">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-881"></span></span>|
|<span data-ttu-id="86a92-882">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-882">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-883">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-883"></span></span>|
   
 <span data-ttu-id="86a92-884">**SHA2 SSL ИТ-отдела Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="86a92-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-885">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-885">**Subject**</span></span>|
|<span data-ttu-id="86a92-886">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-886"></span></span>|
|<span data-ttu-id="86a92-887">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-887">**Issuer**</span></span>|
|<span data-ttu-id="86a92-888">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-888"></span></span>|
|<span data-ttu-id="86a92-889">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-889">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-890">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-890"></span></span>|
|<span data-ttu-id="86a92-891">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-891">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-892">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-892"></span></span>|
|<span data-ttu-id="86a92-893">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-894">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-894"></span></span>|
|<span data-ttu-id="86a92-895">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-896">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-896"></span></span>|
|<span data-ttu-id="86a92-897">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-897">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-898">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-898"></span></span>|
|<span data-ttu-id="86a92-899">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-900">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-900"></span></span>|
|<span data-ttu-id="86a92-901">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-902">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-902"></span></span>|
|<span data-ttu-id="86a92-903">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-904">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-904"></span></span>|
|<span data-ttu-id="86a92-905">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-906">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-906"></span></span>|
|<span data-ttu-id="86a92-907">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-908">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-908"></span></span>|
|<span data-ttu-id="86a92-909">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-909">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-910">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-910"></span></span>|
|<span data-ttu-id="86a92-911">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-912">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-912"></span></span>|
   
 <span data-ttu-id="86a92-913">**ИТ-отдела Майкрософт TLS ЦС 1**</span><span class="sxs-lookup"><span data-stu-id="86a92-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-914">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-914">**Subject**</span></span>|
|<span data-ttu-id="86a92-915">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-915"></span></span>|
|<span data-ttu-id="86a92-916">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-916">**Issuer**</span></span>|
|<span data-ttu-id="86a92-917">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-917"></span></span>|
|<span data-ttu-id="86a92-918">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-918">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-919">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-919"></span></span>|
|<span data-ttu-id="86a92-920">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-920">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-921">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-921"></span></span>|
|<span data-ttu-id="86a92-922">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-923">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-923"></span></span>|
|<span data-ttu-id="86a92-924">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-925">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-925"></span></span>|
|<span data-ttu-id="86a92-926">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-926">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-927">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-927"></span></span>|
|<span data-ttu-id="86a92-928">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-929">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-929"></span></span>|
|<span data-ttu-id="86a92-930">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-931">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-931"></span></span>|
|<span data-ttu-id="86a92-932">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-933">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-933"></span></span>|
|<span data-ttu-id="86a92-934">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-935">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-935"></span></span>|
|<span data-ttu-id="86a92-936">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-937">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-937"></span></span>|
|<span data-ttu-id="86a92-938">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-938">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-939">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-939"></span></span>|
|<span data-ttu-id="86a92-940">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-941">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-941"></span></span>|
   
 <span data-ttu-id="86a92-942">**ИТ-отдела Майкрософт TLS ЦС 2**</span><span class="sxs-lookup"><span data-stu-id="86a92-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-943">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-943">**Subject**</span></span>|
|<span data-ttu-id="86a92-944">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-944"></span></span>|
|<span data-ttu-id="86a92-945">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-945">**Issuer**</span></span>|
|<span data-ttu-id="86a92-946">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-946"></span></span>|
|<span data-ttu-id="86a92-947">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-947">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-948">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-948"></span></span>|
|<span data-ttu-id="86a92-949">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-949">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-950">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-950"></span></span>|
|<span data-ttu-id="86a92-951">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-952">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-952"></span></span>|
|<span data-ttu-id="86a92-953">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-954">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-954"></span></span>|
|<span data-ttu-id="86a92-955">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-955">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-956">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-956"></span></span>|
|<span data-ttu-id="86a92-957">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-958">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-958"></span></span>|
|<span data-ttu-id="86a92-959">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-960">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-960"></span></span>|
|<span data-ttu-id="86a92-961">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-962">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-962"></span></span>|
|<span data-ttu-id="86a92-963">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-964">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-964"></span></span>|
|<span data-ttu-id="86a92-965">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-966">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-966"></span></span>|
|<span data-ttu-id="86a92-967">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-967">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-968">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-968"></span></span>|
|<span data-ttu-id="86a92-969">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-970">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-970"></span></span>|
   
 <span data-ttu-id="86a92-971">**ИТ-отдела Майкрософт TLS ЦС 4**</span><span class="sxs-lookup"><span data-stu-id="86a92-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-972">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-972">**Subject**</span></span>|
|<span data-ttu-id="86a92-973">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-973"></span></span>|
|<span data-ttu-id="86a92-974">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-974">**Issuer**</span></span>|
|<span data-ttu-id="86a92-975">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-975"></span></span>|
|<span data-ttu-id="86a92-976">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-976">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-977">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-977"></span></span>|
|<span data-ttu-id="86a92-978">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-978">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-979">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-979"></span></span>|
|<span data-ttu-id="86a92-980">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-981">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-981"></span></span>|
|<span data-ttu-id="86a92-982">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-983">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-983"></span></span>|
|<span data-ttu-id="86a92-984">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-984">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-985">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-985"></span></span>|
|<span data-ttu-id="86a92-986">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-987">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-987"></span></span>|
|<span data-ttu-id="86a92-988">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-989">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-989"></span></span>|
|<span data-ttu-id="86a92-990">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-991">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-991"></span></span>|
|<span data-ttu-id="86a92-992">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-993">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-993"></span></span>|
|<span data-ttu-id="86a92-994">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-995">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-995"></span></span>|
|<span data-ttu-id="86a92-996">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-996">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-997">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-997"></span></span>|
|<span data-ttu-id="86a92-998">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-999">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-999"></span></span>|
   
 <span data-ttu-id="86a92-1000">**ИТ-отдела Майкрософт TLS ЦС 5**</span><span class="sxs-lookup"><span data-stu-id="86a92-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-1001">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-1001">**Subject**</span></span>|
|<span data-ttu-id="86a92-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1002"></span></span>|
|<span data-ttu-id="86a92-1003">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-1003">**Issuer**</span></span>|
|<span data-ttu-id="86a92-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1004"></span></span>|
|<span data-ttu-id="86a92-1005">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-1005">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1006"></span></span>|
|<span data-ttu-id="86a92-1007">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1008"></span></span>|
|<span data-ttu-id="86a92-1009">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1010"></span></span>|
|<span data-ttu-id="86a92-1011">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1012"></span></span>|
|<span data-ttu-id="86a92-1013">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1014"></span></span>|
|<span data-ttu-id="86a92-1015">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1016"></span></span>|
|<span data-ttu-id="86a92-1017">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1018"></span></span>|
|<span data-ttu-id="86a92-1019">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1020"></span></span>|
|<span data-ttu-id="86a92-1021">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1022"></span></span>|
|<span data-ttu-id="86a92-1023">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1024"></span></span>|
|<span data-ttu-id="86a92-1025">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1026"></span></span>|
|<span data-ttu-id="86a92-1027">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1028"></span></span>|
   
 <span data-ttu-id="86a92-1029">**3 высокой Надежности SSL класс Symantec ЦС - G3**</span><span class="sxs-lookup"><span data-stu-id="86a92-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-1030">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-1030">**Subject**</span></span>|
|<span data-ttu-id="86a92-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1031"></span></span>|
|<span data-ttu-id="86a92-1032">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-1032">**Issuer**</span></span>|
|<span data-ttu-id="86a92-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1033"></span></span>|
|<span data-ttu-id="86a92-1034">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="86a92-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1035"></span></span>|
|<span data-ttu-id="86a92-1036">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-1036">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1037"></span></span>|
|<span data-ttu-id="86a92-1038">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1039"></span></span>|
|<span data-ttu-id="86a92-1040">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1041"></span></span>|
|<span data-ttu-id="86a92-1042">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1043"></span></span>|
|<span data-ttu-id="86a92-1044">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1045"></span></span>|
|<span data-ttu-id="86a92-1046">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1047"></span></span>|
|<span data-ttu-id="86a92-1048">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1049"></span></span>|
|<span data-ttu-id="86a92-1050">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1051"></span></span>|
|<span data-ttu-id="86a92-1052">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1053"></span></span>|
|<span data-ttu-id="86a92-1054">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1055"></span></span>|
|<span data-ttu-id="86a92-1056">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1057"></span></span>|
|<span data-ttu-id="86a92-1058">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1059"></span></span>|
   
 <span data-ttu-id="86a92-1060">**Безопасный сервер Symantec класса 3 ЦС - G4**</span><span class="sxs-lookup"><span data-stu-id="86a92-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-1061">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-1061">**Subject**</span></span>|
|<span data-ttu-id="86a92-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1062"></span></span>|
|<span data-ttu-id="86a92-1063">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-1063">**Issuer**</span></span>|
|<span data-ttu-id="86a92-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1064"></span></span>|
|<span data-ttu-id="86a92-1065">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="86a92-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1066"></span></span>|
|<span data-ttu-id="86a92-1067">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-1067">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1068"></span></span>|
|<span data-ttu-id="86a92-1069">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1070"></span></span>|
|<span data-ttu-id="86a92-1071">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1072"></span></span>|
|<span data-ttu-id="86a92-1073">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1074"></span></span>|
|<span data-ttu-id="86a92-1075">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1076"></span></span>|
|<span data-ttu-id="86a92-1077">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1078"></span></span>|
|<span data-ttu-id="86a92-1079">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1080"></span></span>|
|<span data-ttu-id="86a92-1081">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1082"></span></span>|
|<span data-ttu-id="86a92-1083">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1084"></span></span>|
|<span data-ttu-id="86a92-1085">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1086"></span></span>|
|<span data-ttu-id="86a92-1087">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1088"></span></span>|
|<span data-ttu-id="86a92-1089">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1090"></span></span>|
   
 <span data-ttu-id="86a92-1091">**Thawte SHA256 SSL ЦС**</span><span class="sxs-lookup"><span data-stu-id="86a92-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-1092">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-1092">**Subject**</span></span>|
|<span data-ttu-id="86a92-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1093"></span></span>|
|<span data-ttu-id="86a92-1094">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-1094">**Issuer**</span></span>|
|<span data-ttu-id="86a92-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1095"></span></span>|
|<span data-ttu-id="86a92-1096">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="86a92-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1097"></span></span>|
|<span data-ttu-id="86a92-1098">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-1098">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1099"></span></span>|
|<span data-ttu-id="86a92-1100">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1101"></span></span>|
|<span data-ttu-id="86a92-1102">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1103"></span></span>|
|<span data-ttu-id="86a92-1104">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1105"></span></span>|
|<span data-ttu-id="86a92-1106">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1107"></span></span>|
|<span data-ttu-id="86a92-1108">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1109"></span></span>|
|<span data-ttu-id="86a92-1110">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1111"></span></span>|
|<span data-ttu-id="86a92-1112">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1113"></span></span>|
|<span data-ttu-id="86a92-1114">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1115"></span></span>|
|<span data-ttu-id="86a92-1116">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1117"></span></span>|
|<span data-ttu-id="86a92-1118">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1119"></span></span>|
|<span data-ttu-id="86a92-1120">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1121"></span></span>|
   
 <span data-ttu-id="86a92-1122">**Verizon Akamai ЦС SureServer G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="86a92-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="86a92-1123">**Тема**</span><span class="sxs-lookup"><span data-stu-id="86a92-1123">**Subject**</span></span>|
|<span data-ttu-id="86a92-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1124"></span></span>|
|<span data-ttu-id="86a92-1125">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="86a92-1125">**Issuer**</span></span>|
|<span data-ttu-id="86a92-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1126"></span></span>|
|<span data-ttu-id="86a92-1127">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="86a92-1127">**Serial Number**</span></span>|
|<span data-ttu-id="86a92-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1128"></span></span>|
|<span data-ttu-id="86a92-1129">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="86a92-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="86a92-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1130"></span></span>|
|<span data-ttu-id="86a92-1131">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="86a92-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="86a92-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1132"></span></span>|
|<span data-ttu-id="86a92-1133">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="86a92-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="86a92-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1134"></span></span>|
|<span data-ttu-id="86a92-1135">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="86a92-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="86a92-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1136"></span></span>|
|<span data-ttu-id="86a92-1137">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="86a92-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1138"></span></span>|
|<span data-ttu-id="86a92-1139">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="86a92-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="86a92-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1140"></span></span>|
|<span data-ttu-id="86a92-1141">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="86a92-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1142"></span></span>|
|<span data-ttu-id="86a92-1143">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1144"></span></span>|
|<span data-ttu-id="86a92-1145">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="86a92-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="86a92-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1146"></span></span>|
|<span data-ttu-id="86a92-1147">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="86a92-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="86a92-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1148"></span></span>|
|<span data-ttu-id="86a92-1149">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="86a92-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="86a92-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1150"></span></span>|
|<span data-ttu-id="86a92-1151">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="86a92-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="86a92-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="86a92-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="86a92-1153">Сертификат дополнительные пути</span><span class="sxs-lookup"><span data-stu-id="86a92-1153">Additional certificate paths</span></span>
<span data-ttu-id="86a92-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="86a92-1154"></span></span>

<span data-ttu-id="86a92-1155">Следующие включить устаревшие сертификаты, которые не включены выше и объединяются с списке над по времени.</span><span class="sxs-lookup"><span data-stu-id="86a92-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
```
evsecure-aia.verisign.com
sa.symcb.com
sd.symcb.com
*.omniroot.com
*.verisign.com
*.symcb.com
*.symcd.com
*.verisign.net
*.geotrust.com
*.entrust.net
*.public-trust.com
EVIntl-ocsp.verisign.com
EVSecure-ocsp.verisign.com
isrg.trustid.ocsp.identrust.com
ocsp.digicert.com
ocsp.entrust.net
ocsp.globalsign.com/ExtendedSSLSHA256CACross
ocsp.globalsign.com/rootr1
ocsp.globalsign.com/rootr2
ocsp2.globalsign.com/rootr3
ocsp.int-x3.letsencrypt.org/
ocsp.msocsp.com
ocsp.omniroot.com/baltimoreroot
ocsp2.globalsign.com/gsextendvalsha2g3r3
ocsp2.globalsign.com/gsorganizationvalsha2g2
ocsp2.globalsign.com/gsorganizationvalsha2g3
ocsp2.globalsign.com/rootr3
ocspx.digicert.com
s2.symcb.com
sr.symcd.com
su.symcd.com
vassg142.ocsp.omniroot.com
cdp1.public-trust.com/CRL/Omniroot2025.crl
crl.entrust.net/2048ca.crl
crl.entrust.net/g2ca.crl
crl.entrust.net/level1k.crl
crl.entrust.net/rootca1.crl
crl.globalsign.com/gs/gsextendvalsha2g3r3.crl
crl.globalsign.com/gs/gsorganizationvalsha2g2.crl
crl.globalsign.com/gsorganizationvalsha2g3.crl
crl.globalsign.com/root.crl
crl.globalsign.net/root-r2.crl
crl.globalsign.com/root-r3.crl
crl.globalsign.net/root.crl
crl.identrust.com/DSTROOTCAX3CRL.crl
crl.microsoft.com/pki/mscorp/crl/msitwww1.crl
crl.microsoft.com/pki/mscorp/crl/msitwww2.crl
crl3.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl3.digicert.com/DigiCertGlobalRootCA.crl
crl3.digicert.com/sha2-ev-server-g1.crl
crl3.digicert.com/sha2-ha-server-g5.crl
crl3.digicert.com/ssca-sha2-g5.crl
crl4.digicert.com/DigiCertCloudServicesCA-1-g1.crl
crl4.digicert.com/DigiCertGlobalRootCA.crl
crl4.digicert.com/DigiCertHighAssuranceEVRootCA.crl
crl4.digicert.com/sha2-ev-server-g1.crl
crl4.digicert.com/sha2-ha-server-g5.crl
crl4.digicert.com/ssca-sha2-g5.crl
EVIntl-crl.verisign.com/EVIntl2006.crl
EVSecure-crl.verisign.com/pca3-g5.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww1.crl
mscrl.microsoft.com/pki/mscorp/crl/msitwww2.crl
s1.symcb.com/pca3-g5.crl
sr.symcb.com/sr.crl
su.symcb.com/su.crl
vassg142.crl.omniroot.com/vassg142.crl
aia.entrust.net/l1k-chain256.cer
apps.identrust.com/roots/dstrootcax3.p7c
https://cacert.a.omniroot.com/vassg142.crt
https://cacert.a.omniroot.com/vassg142.der
https://cacert.omniroot.com/baltimoreroot.crt
https://cacert.omniroot.com/baltimoreroot.der
cacerts.digicert.com/DigiCertCloudServicesCA-1.crt
cacerts.digicert.com/DigiCertSHA2ExtendedValidationServerCA.crt
cacerts.digicert.com/DigiCertSHA2HighAssuranceServerCA.crt
cacerts.digicert.com/DigiCertSHA2SecureServerCA.crt
cert.int-x3.letsencrypt.org/
EVIntl-aia.verisign.com/EVIntl2006.cer
secure.globalsign.com/cacert/gsextendvalsha2g2r2.crt
secure.globalsign.com/cacert/gsextendvalsha2g3r3.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g2r1.crt
secure.globalsign.com/cacert/gsorganizationvalsha2g3.crt
sr.symcb.com/sr.crt
su.symcb.com/su.crt
https://www.digicert.com/CACerts/DigiCertGlobalRootCA.crt
https://www.digicert.com/CACerts/DigiCertHighAssuranceEVRootCA.crt
www.microsoft.com/pki/mscorp/msitwww1.crt
www.microsoft.com/pki/mscorp/msitwww2.crt

```


