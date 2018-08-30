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
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534730"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="0abba-106">Цепочки сертификатов Office 365</span><span class="sxs-lookup"><span data-stu-id="0abba-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="0abba-p102">Office 365 использует ряд различных поставщиков. Ниже описаны полный перечень известных Office 365 корневые сертификаты, которые клиенты могут возникать при доступе к Office 365. Сведения о сертификатах, может потребоваться установить в собственную инфраструктуру содержатся в разделе [Планирование сторонних SSL-сертификатов для Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Следующие сведения о сертификате применяется ко всем экземплярам по всему миру и Национальный облака Office 365.</span><span class="sxs-lookup"><span data-stu-id="0abba-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="0abba-111">**Тип сертификата**</span><span class="sxs-lookup"><span data-stu-id="0abba-111">**Certificate type**</span></span>|<span data-ttu-id="0abba-112">**P7b – загрузить (en)**</span><span class="sxs-lookup"><span data-stu-id="0abba-112">**P7b download**</span></span>|<span data-ttu-id="0abba-113">**Конечные точки списка отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-113">**CRL Endpoints**</span></span>|<span data-ttu-id="0abba-114">**Конечные точки OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="0abba-115">**Конечные точки Местоположений**</span><span class="sxs-lookup"><span data-stu-id="0abba-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="0abba-116">Общедоступные доверенные корневые сертификаты</span><span class="sxs-lookup"><span data-stu-id="0abba-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="0abba-117">Office 365 корневой сертификат набора (p7b –)</span><span class="sxs-lookup"><span data-stu-id="0abba-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="0abba-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="0abba-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="0abba-120">Недоступно</span><span class="sxs-lookup"><span data-stu-id="0abba-120">N/A</span></span>  <br/> |<span data-ttu-id="0abba-121">Недоступно</span><span class="sxs-lookup"><span data-stu-id="0abba-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="0abba-122">Общедоступные надежные промежуточных сертификатов</span><span class="sxs-lookup"><span data-stu-id="0abba-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="0abba-123">Набор Office 365 промежуточных сертификатах (p7b –)</span><span class="sxs-lookup"><span data-stu-id="0abba-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="0abba-124">cdp1.public trust.com</span><span class="sxs-lookup"><span data-stu-id="0abba-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="0abba-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="0abba-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="0abba-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="0abba-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="0abba-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="0abba-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="0abba-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="0abba-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="0abba-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="0abba-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="0abba-131">crl3.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="0abba-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="0abba-132">crl4.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="0abba-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="0abba-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="0abba-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="0abba-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="0abba-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="0abba-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="0abba-136">OCSP.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="0abba-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="0abba-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="0abba-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="0abba-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="0abba-139">OCSP.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="0abba-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="0abba-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="0abba-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="0abba-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="0abba-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="0abba-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="0abba-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="0abba-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="0abba-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="0abba-144">корневой c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="0abba-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="0abba-145">root-C3-cA2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="0abba-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="0abba-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="0abba-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="0abba-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="0abba-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="0abba-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="0abba-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="0abba-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="0abba-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="0abba-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="0abba-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="0abba-151">Разверните корневой и промежуточные разделах ниже, чтобы просмотреть дополнительные сведения о поставщиках сертификата.</span><span class="sxs-lookup"><span data-stu-id="0abba-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="0abba-152">Сведения о сертификате корневого Office 365</span><span class="sxs-lookup"><span data-stu-id="0abba-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="0abba-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="0abba-153"></span></span>

 <span data-ttu-id="0abba-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="0abba-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="0abba-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="0abba-155">|:-----|</span></span>
|<span data-ttu-id="0abba-156">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="0abba-157">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-157">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-158">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-158"></span></span>|
|<span data-ttu-id="0abba-159">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-159">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-160">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-160"></span></span>|
|<span data-ttu-id="0abba-161">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-162">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-162"></span></span>|
|<span data-ttu-id="0abba-163">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-164">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-164"></span></span>|
|<span data-ttu-id="0abba-165">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-165">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-166">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-166"></span></span>|
|<span data-ttu-id="0abba-167">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-168">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-168"></span></span>|
|<span data-ttu-id="0abba-169">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-170">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-170"></span></span>|
|<span data-ttu-id="0abba-171">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-172">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-172"></span></span>|
|<span data-ttu-id="0abba-173">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-174">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-174"></span></span>|
   
 <span data-ttu-id="0abba-175">**КОРНЕВОЙ CNNIC**</span><span class="sxs-lookup"><span data-stu-id="0abba-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-176">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-176">**Subject**</span></span>|
|<span data-ttu-id="0abba-177">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-177"></span></span>|
|<span data-ttu-id="0abba-178">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-178">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-179">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-179"></span></span>|
|<span data-ttu-id="0abba-180">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-180">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-181">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-181"></span></span>|
|<span data-ttu-id="0abba-182">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-183">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-183"></span></span>|
|<span data-ttu-id="0abba-184">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-185">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-185"></span></span>|
|<span data-ttu-id="0abba-186">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-186">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-187">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-187"></span></span>|
|<span data-ttu-id="0abba-188">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-189">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-189"></span></span>|
|<span data-ttu-id="0abba-190">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-191">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-191"></span></span>|
|<span data-ttu-id="0abba-192">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-193">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-193"></span></span>|
|<span data-ttu-id="0abba-194">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-195">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-195"></span></span>|
|<span data-ttu-id="0abba-196">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-197">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-197"></span></span>|
   
 <span data-ttu-id="0abba-198">**DigiCert глобального корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="0abba-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-199">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-199">**Subject**</span></span>|
|<span data-ttu-id="0abba-200">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-200"></span></span>|
|<span data-ttu-id="0abba-201">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-201">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-202">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-202"></span></span>|
|<span data-ttu-id="0abba-203">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-203">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-204">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-204"></span></span>|
|<span data-ttu-id="0abba-205">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-206">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-206"></span></span>|
|<span data-ttu-id="0abba-207">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-208">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-208"></span></span>|
|<span data-ttu-id="0abba-209">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-209">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-210">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-210"></span></span>|
|<span data-ttu-id="0abba-211">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-212">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-212"></span></span>|
|<span data-ttu-id="0abba-213">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-214">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-214"></span></span>|
|<span data-ttu-id="0abba-215">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-216">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-216"></span></span>|
|<span data-ttu-id="0abba-217">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-218">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-218"></span></span>|
|<span data-ttu-id="0abba-219">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-220">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-220"></span></span>|
   
 <span data-ttu-id="0abba-221">**Сертификат DigiCert высокой надежности корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="0abba-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-222">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-222">**Subject**</span></span>|
|<span data-ttu-id="0abba-223">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-223"></span></span>|
|<span data-ttu-id="0abba-224">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-224">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-225">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-225"></span></span>|
|<span data-ttu-id="0abba-226">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-226">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-227">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-227"></span></span>|
|<span data-ttu-id="0abba-228">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-229">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-229"></span></span>|
|<span data-ttu-id="0abba-230">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-231">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-231"></span></span>|
|<span data-ttu-id="0abba-232">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-232">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-233">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-233"></span></span>|
|<span data-ttu-id="0abba-234">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-235">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-235"></span></span>|
|<span data-ttu-id="0abba-236">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-237">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-237"></span></span>|
|<span data-ttu-id="0abba-238">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-239">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-239"></span></span>|
|<span data-ttu-id="0abba-240">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-241">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-241"></span></span>|
|<span data-ttu-id="0abba-242">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-243">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-243"></span></span>|
   
 <span data-ttu-id="0abba-244">**Центр сертификации Class 3 корневого ДОВЕРИЯ D 2 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="0abba-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-245">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-245">**Subject**</span></span>|
|<span data-ttu-id="0abba-246">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-246"></span></span>|
|<span data-ttu-id="0abba-247">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-247">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-248">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-248"></span></span>|
|<span data-ttu-id="0abba-249">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-249">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-250">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-250"></span></span>|
|<span data-ttu-id="0abba-251">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-252">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-252"></span></span>|
|<span data-ttu-id="0abba-253">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-254">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-254"></span></span>|
|<span data-ttu-id="0abba-255">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-255">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-256">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-256"></span></span>|
|<span data-ttu-id="0abba-257">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-258">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-258"></span></span>|
|<span data-ttu-id="0abba-259">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-260">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-260"></span></span>|
|<span data-ttu-id="0abba-261">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-262">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-262"></span></span>|
|<span data-ttu-id="0abba-263">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-264">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-264"></span></span>|
|<span data-ttu-id="0abba-265">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-265">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-266">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-266"></span></span>|
   
 <span data-ttu-id="0abba-267">**Центр сертификации Class 3 корневого ДОВЕРИЯ D 2 высокой Надежности 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="0abba-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-268">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-268">**Subject**</span></span>|
|<span data-ttu-id="0abba-269">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-269"></span></span>|
|<span data-ttu-id="0abba-270">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-270">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-271">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-271"></span></span>|
|<span data-ttu-id="0abba-272">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-272">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-273">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-273"></span></span>|
|<span data-ttu-id="0abba-274">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-275">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-275"></span></span>|
|<span data-ttu-id="0abba-276">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-277">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-277"></span></span>|
|<span data-ttu-id="0abba-278">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-278">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-279">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-279"></span></span>|
|<span data-ttu-id="0abba-280">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-281">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-281"></span></span>|
|<span data-ttu-id="0abba-282">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-283">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-283"></span></span>|
|<span data-ttu-id="0abba-284">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-285">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-285"></span></span>|
|<span data-ttu-id="0abba-286">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-287">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-287"></span></span>|
|<span data-ttu-id="0abba-288">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-288">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-289">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-289"></span></span>|
   
 <span data-ttu-id="0abba-290">**Переход на летнее время корневого ЦС X3**</span><span class="sxs-lookup"><span data-stu-id="0abba-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-291">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-291">**Subject**</span></span>|
|<span data-ttu-id="0abba-292">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-292"></span></span>|
|<span data-ttu-id="0abba-293">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-293">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-294">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-294"></span></span>|
|<span data-ttu-id="0abba-295">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-295">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-296">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-296"></span></span>|
|<span data-ttu-id="0abba-297">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-298">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-298"></span></span>|
|<span data-ttu-id="0abba-299">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-300">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-300"></span></span>|
|<span data-ttu-id="0abba-301">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-301">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-302">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-302"></span></span>|
|<span data-ttu-id="0abba-303">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-304">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-304"></span></span>|
|<span data-ttu-id="0abba-305">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-306">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-306"></span></span>|
|<span data-ttu-id="0abba-307">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-308">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-308"></span></span>|
|<span data-ttu-id="0abba-309">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-310">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-310"></span></span>|
   
 <span data-ttu-id="0abba-311">**Доверенный корневой центр сертификации - G2**</span><span class="sxs-lookup"><span data-stu-id="0abba-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-312">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-312">**Subject**</span></span>|
|<span data-ttu-id="0abba-313">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-313"></span></span>|
|<span data-ttu-id="0abba-314">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-314">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-315">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-315"></span></span>|
|<span data-ttu-id="0abba-316">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-316">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-317">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-317"></span></span>|
|<span data-ttu-id="0abba-318">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-319">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-319"></span></span>|
|<span data-ttu-id="0abba-320">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-321">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-321"></span></span>|
|<span data-ttu-id="0abba-322">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-322">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-323">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-323"></span></span>|
|<span data-ttu-id="0abba-324">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-325">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-325"></span></span>|
|<span data-ttu-id="0abba-326">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-327">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-327"></span></span>|
|<span data-ttu-id="0abba-328">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-329">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-329"></span></span>|
|<span data-ttu-id="0abba-330">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-331">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-331"></span></span>|
   
 <span data-ttu-id="0abba-332">**Центр сертификации Entrust.NET (2048)**</span><span class="sxs-lookup"><span data-stu-id="0abba-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-333">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-333">**Subject**</span></span>|
|<span data-ttu-id="0abba-334">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-334"></span></span>|
|<span data-ttu-id="0abba-335">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-335">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-336">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-336"></span></span>|
|<span data-ttu-id="0abba-337">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-337">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-338">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-338"></span></span>|
|<span data-ttu-id="0abba-339">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-340">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-340"></span></span>|
|<span data-ttu-id="0abba-341">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-342">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-342"></span></span>|
|<span data-ttu-id="0abba-343">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-343">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-344">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-344"></span></span>|
|<span data-ttu-id="0abba-345">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-346">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-346"></span></span>|
|<span data-ttu-id="0abba-347">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-348">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-348"></span></span>|
|<span data-ttu-id="0abba-349">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-350">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-350"></span></span>|
|<span data-ttu-id="0abba-351">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-352">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-352"></span></span>|
   
 <span data-ttu-id="0abba-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="0abba-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-354">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-354">**Subject**</span></span>|
|<span data-ttu-id="0abba-355">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-355"></span></span>|
|<span data-ttu-id="0abba-356">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-356">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-357">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-357"></span></span>|
|<span data-ttu-id="0abba-358">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-358">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-359">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-359"></span></span>|
|<span data-ttu-id="0abba-360">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-361">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-361"></span></span>|
|<span data-ttu-id="0abba-362">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-363">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-363"></span></span>|
|<span data-ttu-id="0abba-364">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-364">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-365">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-365"></span></span>|
|<span data-ttu-id="0abba-366">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-367">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-367"></span></span>|
|<span data-ttu-id="0abba-368">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-369">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-369"></span></span>|
|<span data-ttu-id="0abba-370">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-371">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-371"></span></span>|
|<span data-ttu-id="0abba-372">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-373">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-373"></span></span>|
|<span data-ttu-id="0abba-374">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-375">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-375"></span></span>|
|<span data-ttu-id="0abba-376">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-376">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-377">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-377"></span></span>|
   
 <span data-ttu-id="0abba-378">**GlobalSign корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="0abba-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-379">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-379">**Subject**</span></span>|
|<span data-ttu-id="0abba-380">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-380"></span></span>|
|<span data-ttu-id="0abba-381">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-381">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-382">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-382"></span></span>|
|<span data-ttu-id="0abba-383">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-383">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-384">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-384"></span></span>|
|<span data-ttu-id="0abba-385">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-386">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-386"></span></span>|
|<span data-ttu-id="0abba-387">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-388">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-388"></span></span>|
|<span data-ttu-id="0abba-389">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-389">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-390">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-390"></span></span>|
|<span data-ttu-id="0abba-391">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-392">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-392"></span></span>|
|<span data-ttu-id="0abba-393">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-394">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-394"></span></span>|
|<span data-ttu-id="0abba-395">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-396">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-396"></span></span>|
|<span data-ttu-id="0abba-397">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-398">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-398"></span></span>|
   
 <span data-ttu-id="0abba-399">**Thawte основной корневого ЦС - G3**</span><span class="sxs-lookup"><span data-stu-id="0abba-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-400">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-400">**Subject**</span></span>|
|<span data-ttu-id="0abba-401">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-401"></span></span>|
|<span data-ttu-id="0abba-402">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-402">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-403">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-403"></span></span>|
|<span data-ttu-id="0abba-404">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-404">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-405">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-405"></span></span>|
|<span data-ttu-id="0abba-406">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-407">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-407"></span></span>|
|<span data-ttu-id="0abba-408">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-409">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-409"></span></span>|
|<span data-ttu-id="0abba-410">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-410">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-411">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-411"></span></span>|
|<span data-ttu-id="0abba-412">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-413">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-413"></span></span>|
|<span data-ttu-id="0abba-414">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-415">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-415"></span></span>|
|<span data-ttu-id="0abba-416">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-417">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-417"></span></span>|
|<span data-ttu-id="0abba-418">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-419">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-419"></span></span>|
   
 <span data-ttu-id="0abba-420">**Главный общедоступный ЦС класса VeriSign 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="0abba-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-421">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-421">**Subject**</span></span>|
|<span data-ttu-id="0abba-422">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-422"></span></span>|
|<span data-ttu-id="0abba-423">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-423">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-424">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-424"></span></span>|
|<span data-ttu-id="0abba-425">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-425">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-426">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-426"></span></span>|
|<span data-ttu-id="0abba-427">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-428">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-428"></span></span>|
|<span data-ttu-id="0abba-429">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-430">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-430"></span></span>|
|<span data-ttu-id="0abba-431">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-431">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-432">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-432"></span></span>|
|<span data-ttu-id="0abba-433">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-434">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-434"></span></span>|
|<span data-ttu-id="0abba-435">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-436">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-436"></span></span>|
|<span data-ttu-id="0abba-437">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-438">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-438"></span></span>|
|<span data-ttu-id="0abba-439">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-440">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="0abba-441">Сведения о промежуточных сертификатах Office 365</span><span class="sxs-lookup"><span data-stu-id="0abba-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="0abba-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="0abba-442"></span></span>

 <span data-ttu-id="0abba-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="0abba-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-444">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-444">**Subject**</span></span>|
|<span data-ttu-id="0abba-445">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-445"></span></span>|
|<span data-ttu-id="0abba-446">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-446">**Issuer**</span></span>|
|<span data-ttu-id="0abba-447">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-447"></span></span>|
|<span data-ttu-id="0abba-448">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-448">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-449">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-449"></span></span>|
|<span data-ttu-id="0abba-450">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-450">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-451">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-451"></span></span>|
|<span data-ttu-id="0abba-452">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-453">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-453"></span></span>|
|<span data-ttu-id="0abba-454">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-455">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-455"></span></span>|
|<span data-ttu-id="0abba-456">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-456">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-457">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-457"></span></span>|
|<span data-ttu-id="0abba-458">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-459">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-459"></span></span>|
|<span data-ttu-id="0abba-460">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-461">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-461"></span></span>|
|<span data-ttu-id="0abba-462">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-463">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-463"></span></span>|
|<span data-ttu-id="0abba-464">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-465">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-465"></span></span>|
|<span data-ttu-id="0abba-466">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-467">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-467"></span></span>|
|<span data-ttu-id="0abba-468">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="0abba-468">**AIA URLs**</span></span>|
|<span data-ttu-id="0abba-469">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-469"></span></span>|
|<span data-ttu-id="0abba-470">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-470">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-471">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-471"></span></span>|
|<span data-ttu-id="0abba-472">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-473">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-473"></span></span>|
   
 <span data-ttu-id="0abba-474">**Центра сертификации Class 3 D-TRUST SSL 1 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="0abba-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-475">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-475">**Subject**</span></span>|
|<span data-ttu-id="0abba-476">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-476"></span></span>|
|<span data-ttu-id="0abba-477">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-477">**Issuer**</span></span>|
|<span data-ttu-id="0abba-478">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-478"></span></span>|
|<span data-ttu-id="0abba-479">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="0abba-480">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-480"></span></span>|
|<span data-ttu-id="0abba-481">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-481">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-482">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-482"></span></span>|
|<span data-ttu-id="0abba-483">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-483">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-484">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-484"></span></span>|
|<span data-ttu-id="0abba-485">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-486">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-486"></span></span>|
|<span data-ttu-id="0abba-487">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-488">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-488"></span></span>|
|<span data-ttu-id="0abba-489">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-489">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-490">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-490"></span></span>|
|<span data-ttu-id="0abba-491">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-492">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-492"></span></span>|
|<span data-ttu-id="0abba-493">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-494">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-494"></span></span>|
|<span data-ttu-id="0abba-495">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-496">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-496"></span></span>|
|<span data-ttu-id="0abba-497">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-498">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-498"></span></span>|
|<span data-ttu-id="0abba-499">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-500">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-500"></span></span>|
|<span data-ttu-id="0abba-501">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-501">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-502">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-502"></span></span>|
|<span data-ttu-id="0abba-503">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-504">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-504"></span></span>|
   
 <span data-ttu-id="0abba-505">**Центра сертификации Class 3 D-TRUST SSL 1 высокой Надежности 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="0abba-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-506">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-506">**Subject**</span></span>|
|<span data-ttu-id="0abba-507">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-507"></span></span>|
|<span data-ttu-id="0abba-508">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-508">**Issuer**</span></span>|
|<span data-ttu-id="0abba-509">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-509"></span></span>|
|<span data-ttu-id="0abba-510">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="0abba-511">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-511"></span></span>|
|<span data-ttu-id="0abba-512">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-512">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-513">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-513"></span></span>|
|<span data-ttu-id="0abba-514">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-514">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-515">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-515"></span></span>|
|<span data-ttu-id="0abba-516">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-517">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-517"></span></span>|
|<span data-ttu-id="0abba-518">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-519">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-519"></span></span>|
|<span data-ttu-id="0abba-520">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-520">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-521">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-521"></span></span>|
|<span data-ttu-id="0abba-522">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-523">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-523"></span></span>|
|<span data-ttu-id="0abba-524">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-525">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-525"></span></span>|
|<span data-ttu-id="0abba-526">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-527">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-527"></span></span>|
|<span data-ttu-id="0abba-528">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-529">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-529"></span></span>|
|<span data-ttu-id="0abba-530">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-531">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-531"></span></span>|
|<span data-ttu-id="0abba-532">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-532">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-533">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-533"></span></span>|
|<span data-ttu-id="0abba-534">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-535">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-535"></span></span>|
   
 <span data-ttu-id="0abba-536">**DigiCert облачным службам ЦС-1**</span><span class="sxs-lookup"><span data-stu-id="0abba-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-537">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-537">**Subject**</span></span>|
|<span data-ttu-id="0abba-538">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-538"></span></span>|
|<span data-ttu-id="0abba-539">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-539">**Issuer**</span></span>|
|<span data-ttu-id="0abba-540">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-540"></span></span>|
|<span data-ttu-id="0abba-541">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-541">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-542">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-542"></span></span>|
|<span data-ttu-id="0abba-543">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-543">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-544">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-544"></span></span>|
|<span data-ttu-id="0abba-545">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-546">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-546"></span></span>|
|<span data-ttu-id="0abba-547">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-548">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-548"></span></span>|
|<span data-ttu-id="0abba-549">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-549">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-550">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-550"></span></span>|
|<span data-ttu-id="0abba-551">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-552">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-552"></span></span>|
|<span data-ttu-id="0abba-553">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-554">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-554"></span></span>|
|<span data-ttu-id="0abba-555">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-556">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-556"></span></span>|
|<span data-ttu-id="0abba-557">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-558">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-558"></span></span>|
|<span data-ttu-id="0abba-559">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-560">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-560"></span></span>|
|<span data-ttu-id="0abba-561">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-561">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-562">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-562"></span></span>|
|<span data-ttu-id="0abba-563">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-564">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-564"></span></span>|
   
 <span data-ttu-id="0abba-565">**DigiCert SHA2 высокой надежности сервера центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-566">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-566">**Subject**</span></span>|
|<span data-ttu-id="0abba-567">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-567"></span></span>|
|<span data-ttu-id="0abba-568">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-568">**Issuer**</span></span>|
|<span data-ttu-id="0abba-569">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-569"></span></span>|
|<span data-ttu-id="0abba-570">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-570">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-571">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-571"></span></span>|
|<span data-ttu-id="0abba-572">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-572">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-573">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-573"></span></span>|
|<span data-ttu-id="0abba-574">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-575">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-575"></span></span>|
|<span data-ttu-id="0abba-576">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-577">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-577"></span></span>|
|<span data-ttu-id="0abba-578">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-578">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-579">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-579"></span></span>|
|<span data-ttu-id="0abba-580">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-581">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-581"></span></span>|
|<span data-ttu-id="0abba-582">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-583">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-583"></span></span>|
|<span data-ttu-id="0abba-584">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-585">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-585"></span></span>|
|<span data-ttu-id="0abba-586">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-587">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-587"></span></span>|
|<span data-ttu-id="0abba-588">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-589">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-589"></span></span>|
|<span data-ttu-id="0abba-590">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-590">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-591">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-591"></span></span>|
|<span data-ttu-id="0abba-592">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-593">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-593"></span></span>|
   
 <span data-ttu-id="0abba-594">**Безопасный сервер DigiCert SHA2 ЦС**</span><span class="sxs-lookup"><span data-stu-id="0abba-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-595">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-595">**Subject**</span></span>|
|<span data-ttu-id="0abba-596">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-596"></span></span>|
|<span data-ttu-id="0abba-597">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-597">**Issuer**</span></span>|
|<span data-ttu-id="0abba-598">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-598"></span></span>|
|<span data-ttu-id="0abba-599">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-599">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-600">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-600"></span></span>|
|<span data-ttu-id="0abba-601">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-601">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-602">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-602"></span></span>|
|<span data-ttu-id="0abba-603">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-604">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-604"></span></span>|
|<span data-ttu-id="0abba-605">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-606">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-606"></span></span>|
|<span data-ttu-id="0abba-607">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-607">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-608">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-608"></span></span>|
|<span data-ttu-id="0abba-609">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-610">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-610"></span></span>|
|<span data-ttu-id="0abba-611">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-612">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-612"></span></span>|
|<span data-ttu-id="0abba-613">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-614">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-614"></span></span>|
|<span data-ttu-id="0abba-615">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-616">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-616"></span></span>|
|<span data-ttu-id="0abba-617">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-618">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-618"></span></span>|
|<span data-ttu-id="0abba-619">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-619">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-620">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-620"></span></span>|
|<span data-ttu-id="0abba-621">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-622">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-622"></span></span>|
   
 <span data-ttu-id="0abba-623">**Доверенный центр сертификации - L1C**</span><span class="sxs-lookup"><span data-stu-id="0abba-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-624">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-624">**Subject**</span></span>|
|<span data-ttu-id="0abba-625">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-625"></span></span>|
|<span data-ttu-id="0abba-626">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-626">**Issuer**</span></span>|
|<span data-ttu-id="0abba-627">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-627"></span></span>|
|<span data-ttu-id="0abba-628">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-628">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-629">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-629"></span></span>|
|<span data-ttu-id="0abba-630">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-630">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-631">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-631"></span></span>|
|<span data-ttu-id="0abba-632">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-633">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-633"></span></span>|
|<span data-ttu-id="0abba-634">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-635">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-635"></span></span>|
|<span data-ttu-id="0abba-636">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-636">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-637">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-637"></span></span>|
|<span data-ttu-id="0abba-638">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-639">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-639"></span></span>|
|<span data-ttu-id="0abba-640">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-641">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-641"></span></span>|
|<span data-ttu-id="0abba-642">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-643">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-643"></span></span>|
|<span data-ttu-id="0abba-644">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-645">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-645"></span></span>|
|<span data-ttu-id="0abba-646">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-647">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-647"></span></span>|
|<span data-ttu-id="0abba-648">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-648">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-649">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-649"></span></span>|
|<span data-ttu-id="0abba-650">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-651">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-651"></span></span>|
   
 <span data-ttu-id="0abba-652">**Доверенный центр сертификации - L1K**</span><span class="sxs-lookup"><span data-stu-id="0abba-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-653">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-653">**Subject**</span></span>|
|<span data-ttu-id="0abba-654">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-654"></span></span>|
|<span data-ttu-id="0abba-655">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-655">**Issuer**</span></span>|
|<span data-ttu-id="0abba-656">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-656"></span></span>|
|<span data-ttu-id="0abba-657">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-657">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-658">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-658"></span></span>|
|<span data-ttu-id="0abba-659">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-659">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-660">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-660"></span></span>|
|<span data-ttu-id="0abba-661">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-662">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-662"></span></span>|
|<span data-ttu-id="0abba-663">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-664">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-664"></span></span>|
|<span data-ttu-id="0abba-665">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-665">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-666">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-666"></span></span>|
|<span data-ttu-id="0abba-667">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-668">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-668"></span></span>|
|<span data-ttu-id="0abba-669">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-670">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-670"></span></span>|
|<span data-ttu-id="0abba-671">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-672">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-672"></span></span>|
|<span data-ttu-id="0abba-673">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-674">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-674"></span></span>|
|<span data-ttu-id="0abba-675">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-676">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-676"></span></span>|
|<span data-ttu-id="0abba-677">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-677">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-678">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-678"></span></span>|
|<span data-ttu-id="0abba-679">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-680">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-680"></span></span>|
   
 <span data-ttu-id="0abba-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="0abba-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-682">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-682">**Subject**</span></span>|
|<span data-ttu-id="0abba-683">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-683"></span></span>|
|<span data-ttu-id="0abba-684">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-684">**Issuer**</span></span>|
|<span data-ttu-id="0abba-685">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-685"></span></span>|
|<span data-ttu-id="0abba-686">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-686">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-687">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-687"></span></span>|
|<span data-ttu-id="0abba-688">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-688">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-689">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-689"></span></span>|
|<span data-ttu-id="0abba-690">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-691">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-691"></span></span>|
|<span data-ttu-id="0abba-692">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-693">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-693"></span></span>|
|<span data-ttu-id="0abba-694">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-694">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-695">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-695"></span></span>|
|<span data-ttu-id="0abba-696">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-697">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-697"></span></span>|
|<span data-ttu-id="0abba-698">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-699">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-699"></span></span>|
|<span data-ttu-id="0abba-700">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-701">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-701"></span></span>|
|<span data-ttu-id="0abba-702">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-703">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-703"></span></span>|
|<span data-ttu-id="0abba-704">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-705">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-705"></span></span>|
|<span data-ttu-id="0abba-706">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-706">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-707">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-707"></span></span>|
|<span data-ttu-id="0abba-708">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-709">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-709"></span></span>|
   
 <span data-ttu-id="0abba-710">**Расширенные проверки ЦС - SHA256 - G2 GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="0abba-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-711">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-711">**Subject**</span></span>|
|<span data-ttu-id="0abba-712">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-712"></span></span>|
|<span data-ttu-id="0abba-713">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-713">**Issuer**</span></span>|
|<span data-ttu-id="0abba-714">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-714"></span></span>|
|<span data-ttu-id="0abba-715">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-715">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-716">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-716"></span></span>|
|<span data-ttu-id="0abba-717">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-717">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-718">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-718"></span></span>|
|<span data-ttu-id="0abba-719">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-720">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-720"></span></span>|
|<span data-ttu-id="0abba-721">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-722">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-722"></span></span>|
|<span data-ttu-id="0abba-723">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-723">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-724">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-724"></span></span>|
|<span data-ttu-id="0abba-725">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-726">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-726"></span></span>|
|<span data-ttu-id="0abba-727">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-728">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-728"></span></span>|
|<span data-ttu-id="0abba-729">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-730">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-730"></span></span>|
|<span data-ttu-id="0abba-731">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-732">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-732"></span></span>|
|<span data-ttu-id="0abba-733">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-734">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-734"></span></span>|
|<span data-ttu-id="0abba-735">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-735">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-736">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-736"></span></span>|
|<span data-ttu-id="0abba-737">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-738">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-738"></span></span>|
   
 <span data-ttu-id="0abba-739">**Расширенные проверки ЦС - SHA256 - G3 GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="0abba-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-740">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-740">**Subject**</span></span>|
|<span data-ttu-id="0abba-741">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-741"></span></span>|
|<span data-ttu-id="0abba-742">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-742">**Issuer**</span></span>|
|<span data-ttu-id="0abba-743">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-743"></span></span>|
|<span data-ttu-id="0abba-744">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-744">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-745">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-745"></span></span>|
|<span data-ttu-id="0abba-746">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-746">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-747">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-747"></span></span>|
|<span data-ttu-id="0abba-748">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-749">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-749"></span></span>|
|<span data-ttu-id="0abba-750">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-751">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-751"></span></span>|
|<span data-ttu-id="0abba-752">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-752">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-753">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-753"></span></span>|
|<span data-ttu-id="0abba-754">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-755">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-755"></span></span>|
|<span data-ttu-id="0abba-756">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-757">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-757"></span></span>|
|<span data-ttu-id="0abba-758">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-759">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-759"></span></span>|
|<span data-ttu-id="0abba-760">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-761">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-761"></span></span>|
|<span data-ttu-id="0abba-762">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-763">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-763"></span></span>|
|<span data-ttu-id="0abba-764">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-764">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-765">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-765"></span></span>|
|<span data-ttu-id="0abba-766">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-767">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-767"></span></span>|
   
 <span data-ttu-id="0abba-768">**GlobalSign организации проверки ЦС - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="0abba-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-769">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-769">**Subject**</span></span>|
|<span data-ttu-id="0abba-770">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-770"></span></span>|
|<span data-ttu-id="0abba-771">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-771">**Issuer**</span></span>|
|<span data-ttu-id="0abba-772">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-772"></span></span>|
|<span data-ttu-id="0abba-773">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-773">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-774">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-774"></span></span>|
|<span data-ttu-id="0abba-775">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-775">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-776">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-776"></span></span>|
|<span data-ttu-id="0abba-777">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-778">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-778"></span></span>|
|<span data-ttu-id="0abba-779">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-780">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-780"></span></span>|
|<span data-ttu-id="0abba-781">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-781">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-782">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-782"></span></span>|
|<span data-ttu-id="0abba-783">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-784">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-784"></span></span>|
|<span data-ttu-id="0abba-785">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-786">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-786"></span></span>|
|<span data-ttu-id="0abba-787">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-788">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-788"></span></span>|
|<span data-ttu-id="0abba-789">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-790">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-790"></span></span>|
|<span data-ttu-id="0abba-791">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-792">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-792"></span></span>|
|<span data-ttu-id="0abba-793">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-793">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-794">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-794"></span></span>|
|<span data-ttu-id="0abba-795">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-796">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-796"></span></span>|
   
 <span data-ttu-id="0abba-797">**GlobalSign организации проверки ЦС - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="0abba-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-798">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-798">**Subject**</span></span>|
|<span data-ttu-id="0abba-799">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-799"></span></span>|
|<span data-ttu-id="0abba-800">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-800">**Issuer**</span></span>|
|<span data-ttu-id="0abba-801">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-801"></span></span>|
|<span data-ttu-id="0abba-802">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-802">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-803">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-803"></span></span>|
|<span data-ttu-id="0abba-804">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-804">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-805">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-805"></span></span>|
|<span data-ttu-id="0abba-806">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-807">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-807"></span></span>|
|<span data-ttu-id="0abba-808">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-809">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-809"></span></span>|
|<span data-ttu-id="0abba-810">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-810">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-811">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-811"></span></span>|
|<span data-ttu-id="0abba-812">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-813">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-813"></span></span>|
|<span data-ttu-id="0abba-814">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-815">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-815"></span></span>|
|<span data-ttu-id="0abba-816">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-817">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-817"></span></span>|
|<span data-ttu-id="0abba-818">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-819">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-819"></span></span>|
|<span data-ttu-id="0abba-820">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-821">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-821"></span></span>|
|<span data-ttu-id="0abba-822">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-822">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-823">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-823"></span></span>|
|<span data-ttu-id="0abba-824">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-825">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-825"></span></span>|
   
 <span data-ttu-id="0abba-826">**Давайте шифрования центра сертификации X3**</span><span class="sxs-lookup"><span data-stu-id="0abba-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-827">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-827">**Subject**</span></span>|
|<span data-ttu-id="0abba-828">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-828"></span></span>|
|<span data-ttu-id="0abba-829">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-829">**Issuer**</span></span>|
|<span data-ttu-id="0abba-830">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-830"></span></span>|
|<span data-ttu-id="0abba-831">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-831">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-832">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-832"></span></span>|
|<span data-ttu-id="0abba-833">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-833">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-834">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-834"></span></span>|
|<span data-ttu-id="0abba-835">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-836">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-836"></span></span>|
|<span data-ttu-id="0abba-837">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-838">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-838"></span></span>|
|<span data-ttu-id="0abba-839">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-839">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-840">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-840"></span></span>|
|<span data-ttu-id="0abba-841">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-842">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-842"></span></span>|
|<span data-ttu-id="0abba-843">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-844">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-844"></span></span>|
|<span data-ttu-id="0abba-845">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-846">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-846"></span></span>|
|<span data-ttu-id="0abba-847">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-848">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-848"></span></span>|
|<span data-ttu-id="0abba-849">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-850">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-850"></span></span>|
|<span data-ttu-id="0abba-851">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="0abba-851">**AIA URLs**</span></span>|
|<span data-ttu-id="0abba-852">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-852"></span></span>|
|<span data-ttu-id="0abba-853">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-853">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-854">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-854"></span></span>|
|<span data-ttu-id="0abba-855">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-856">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-856"></span></span>|
   
 <span data-ttu-id="0abba-857">**SHA2 SSL ИТ-отдела Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="0abba-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-858">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-858">**Subject**</span></span>|
|<span data-ttu-id="0abba-859">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-859"></span></span>|
|<span data-ttu-id="0abba-860">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-860">**Issuer**</span></span>|
|<span data-ttu-id="0abba-861">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-861"></span></span>|
|<span data-ttu-id="0abba-862">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-862">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-863">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-863"></span></span>|
|<span data-ttu-id="0abba-864">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-864">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-865">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-865"></span></span>|
|<span data-ttu-id="0abba-866">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-867">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-867"></span></span>|
|<span data-ttu-id="0abba-868">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-869">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-869"></span></span>|
|<span data-ttu-id="0abba-870">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-870">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-871">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-871"></span></span>|
|<span data-ttu-id="0abba-872">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-873">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-873"></span></span>|
|<span data-ttu-id="0abba-874">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-875">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-875"></span></span>|
|<span data-ttu-id="0abba-876">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-877">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-877"></span></span>|
|<span data-ttu-id="0abba-878">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-879">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-879"></span></span>|
|<span data-ttu-id="0abba-880">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-881">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-881"></span></span>|
|<span data-ttu-id="0abba-882">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-882">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-883">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-883"></span></span>|
   
 <span data-ttu-id="0abba-884">**SHA2 SSL ИТ-отдела Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="0abba-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-885">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-885">**Subject**</span></span>|
|<span data-ttu-id="0abba-886">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-886"></span></span>|
|<span data-ttu-id="0abba-887">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-887">**Issuer**</span></span>|
|<span data-ttu-id="0abba-888">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-888"></span></span>|
|<span data-ttu-id="0abba-889">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-889">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-890">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-890"></span></span>|
|<span data-ttu-id="0abba-891">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-891">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-892">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-892"></span></span>|
|<span data-ttu-id="0abba-893">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-894">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-894"></span></span>|
|<span data-ttu-id="0abba-895">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-896">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-896"></span></span>|
|<span data-ttu-id="0abba-897">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-897">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-898">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-898"></span></span>|
|<span data-ttu-id="0abba-899">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-900">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-900"></span></span>|
|<span data-ttu-id="0abba-901">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-902">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-902"></span></span>|
|<span data-ttu-id="0abba-903">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-904">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-904"></span></span>|
|<span data-ttu-id="0abba-905">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-906">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-906"></span></span>|
|<span data-ttu-id="0abba-907">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-908">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-908"></span></span>|
|<span data-ttu-id="0abba-909">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-909">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-910">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-910"></span></span>|
|<span data-ttu-id="0abba-911">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-912">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-912"></span></span>|
   
 <span data-ttu-id="0abba-913">**ИТ-отдела Майкрософт TLS ЦС 1**</span><span class="sxs-lookup"><span data-stu-id="0abba-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-914">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-914">**Subject**</span></span>|
|<span data-ttu-id="0abba-915">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-915"></span></span>|
|<span data-ttu-id="0abba-916">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-916">**Issuer**</span></span>|
|<span data-ttu-id="0abba-917">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-917"></span></span>|
|<span data-ttu-id="0abba-918">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-918">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-919">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-919"></span></span>|
|<span data-ttu-id="0abba-920">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-920">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-921">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-921"></span></span>|
|<span data-ttu-id="0abba-922">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-923">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-923"></span></span>|
|<span data-ttu-id="0abba-924">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-925">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-925"></span></span>|
|<span data-ttu-id="0abba-926">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-926">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-927">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-927"></span></span>|
|<span data-ttu-id="0abba-928">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-929">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-929"></span></span>|
|<span data-ttu-id="0abba-930">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-931">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-931"></span></span>|
|<span data-ttu-id="0abba-932">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-933">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-933"></span></span>|
|<span data-ttu-id="0abba-934">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-935">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-935"></span></span>|
|<span data-ttu-id="0abba-936">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-937">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-937"></span></span>|
|<span data-ttu-id="0abba-938">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-938">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-939">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-939"></span></span>|
|<span data-ttu-id="0abba-940">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-941">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-941"></span></span>|
   
 <span data-ttu-id="0abba-942">**ИТ-отдела Майкрософт TLS ЦС 2**</span><span class="sxs-lookup"><span data-stu-id="0abba-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-943">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-943">**Subject**</span></span>|
|<span data-ttu-id="0abba-944">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-944"></span></span>|
|<span data-ttu-id="0abba-945">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-945">**Issuer**</span></span>|
|<span data-ttu-id="0abba-946">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-946"></span></span>|
|<span data-ttu-id="0abba-947">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-947">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-948">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-948"></span></span>|
|<span data-ttu-id="0abba-949">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-949">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-950">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-950"></span></span>|
|<span data-ttu-id="0abba-951">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-952">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-952"></span></span>|
|<span data-ttu-id="0abba-953">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-954">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-954"></span></span>|
|<span data-ttu-id="0abba-955">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-955">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-956">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-956"></span></span>|
|<span data-ttu-id="0abba-957">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-958">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-958"></span></span>|
|<span data-ttu-id="0abba-959">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-960">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-960"></span></span>|
|<span data-ttu-id="0abba-961">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-962">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-962"></span></span>|
|<span data-ttu-id="0abba-963">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-964">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-964"></span></span>|
|<span data-ttu-id="0abba-965">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-966">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-966"></span></span>|
|<span data-ttu-id="0abba-967">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-967">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-968">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-968"></span></span>|
|<span data-ttu-id="0abba-969">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-970">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-970"></span></span>|
   
 <span data-ttu-id="0abba-971">**ИТ-отдела Майкрософт TLS ЦС 4**</span><span class="sxs-lookup"><span data-stu-id="0abba-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-972">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-972">**Subject**</span></span>|
|<span data-ttu-id="0abba-973">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-973"></span></span>|
|<span data-ttu-id="0abba-974">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-974">**Issuer**</span></span>|
|<span data-ttu-id="0abba-975">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-975"></span></span>|
|<span data-ttu-id="0abba-976">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-976">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-977">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-977"></span></span>|
|<span data-ttu-id="0abba-978">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-978">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-979">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-979"></span></span>|
|<span data-ttu-id="0abba-980">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-981">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-981"></span></span>|
|<span data-ttu-id="0abba-982">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-983">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-983"></span></span>|
|<span data-ttu-id="0abba-984">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-984">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-985">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-985"></span></span>|
|<span data-ttu-id="0abba-986">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-987">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-987"></span></span>|
|<span data-ttu-id="0abba-988">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-989">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-989"></span></span>|
|<span data-ttu-id="0abba-990">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-991">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-991"></span></span>|
|<span data-ttu-id="0abba-992">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-993">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-993"></span></span>|
|<span data-ttu-id="0abba-994">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-995">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-995"></span></span>|
|<span data-ttu-id="0abba-996">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-996">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-997">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-997"></span></span>|
|<span data-ttu-id="0abba-998">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-999">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-999"></span></span>|
   
 <span data-ttu-id="0abba-1000">**ИТ-отдела Майкрософт TLS ЦС 5**</span><span class="sxs-lookup"><span data-stu-id="0abba-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-1001">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-1001">**Subject**</span></span>|
|<span data-ttu-id="0abba-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1002"></span></span>|
|<span data-ttu-id="0abba-1003">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-1003">**Issuer**</span></span>|
|<span data-ttu-id="0abba-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1004"></span></span>|
|<span data-ttu-id="0abba-1005">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-1005">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1006"></span></span>|
|<span data-ttu-id="0abba-1007">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1008"></span></span>|
|<span data-ttu-id="0abba-1009">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1010"></span></span>|
|<span data-ttu-id="0abba-1011">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1012"></span></span>|
|<span data-ttu-id="0abba-1013">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1014"></span></span>|
|<span data-ttu-id="0abba-1015">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1016"></span></span>|
|<span data-ttu-id="0abba-1017">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1018"></span></span>|
|<span data-ttu-id="0abba-1019">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1020"></span></span>|
|<span data-ttu-id="0abba-1021">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1022"></span></span>|
|<span data-ttu-id="0abba-1023">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1024"></span></span>|
|<span data-ttu-id="0abba-1025">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1026"></span></span>|
|<span data-ttu-id="0abba-1027">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1028"></span></span>|
   
 <span data-ttu-id="0abba-1029">**3 высокой Надежности SSL класс Symantec ЦС - G3**</span><span class="sxs-lookup"><span data-stu-id="0abba-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-1030">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-1030">**Subject**</span></span>|
|<span data-ttu-id="0abba-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1031"></span></span>|
|<span data-ttu-id="0abba-1032">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-1032">**Issuer**</span></span>|
|<span data-ttu-id="0abba-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1033"></span></span>|
|<span data-ttu-id="0abba-1034">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="0abba-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1035"></span></span>|
|<span data-ttu-id="0abba-1036">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-1036">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1037"></span></span>|
|<span data-ttu-id="0abba-1038">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1039"></span></span>|
|<span data-ttu-id="0abba-1040">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1041"></span></span>|
|<span data-ttu-id="0abba-1042">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1043"></span></span>|
|<span data-ttu-id="0abba-1044">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1045"></span></span>|
|<span data-ttu-id="0abba-1046">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1047"></span></span>|
|<span data-ttu-id="0abba-1048">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1049"></span></span>|
|<span data-ttu-id="0abba-1050">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1051"></span></span>|
|<span data-ttu-id="0abba-1052">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1053"></span></span>|
|<span data-ttu-id="0abba-1054">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1055"></span></span>|
|<span data-ttu-id="0abba-1056">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1057"></span></span>|
|<span data-ttu-id="0abba-1058">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1059"></span></span>|
   
 <span data-ttu-id="0abba-1060">**Безопасный сервер Symantec класса 3 ЦС - G4**</span><span class="sxs-lookup"><span data-stu-id="0abba-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-1061">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-1061">**Subject**</span></span>|
|<span data-ttu-id="0abba-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1062"></span></span>|
|<span data-ttu-id="0abba-1063">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-1063">**Issuer**</span></span>|
|<span data-ttu-id="0abba-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1064"></span></span>|
|<span data-ttu-id="0abba-1065">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="0abba-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1066"></span></span>|
|<span data-ttu-id="0abba-1067">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-1067">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1068"></span></span>|
|<span data-ttu-id="0abba-1069">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1070"></span></span>|
|<span data-ttu-id="0abba-1071">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1072"></span></span>|
|<span data-ttu-id="0abba-1073">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1074"></span></span>|
|<span data-ttu-id="0abba-1075">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1076"></span></span>|
|<span data-ttu-id="0abba-1077">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1078"></span></span>|
|<span data-ttu-id="0abba-1079">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1080"></span></span>|
|<span data-ttu-id="0abba-1081">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1082"></span></span>|
|<span data-ttu-id="0abba-1083">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1084"></span></span>|
|<span data-ttu-id="0abba-1085">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1086"></span></span>|
|<span data-ttu-id="0abba-1087">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1088"></span></span>|
|<span data-ttu-id="0abba-1089">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1090"></span></span>|
   
 <span data-ttu-id="0abba-1091">**Thawte SHA256 SSL ЦС**</span><span class="sxs-lookup"><span data-stu-id="0abba-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-1092">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-1092">**Subject**</span></span>|
|<span data-ttu-id="0abba-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1093"></span></span>|
|<span data-ttu-id="0abba-1094">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-1094">**Issuer**</span></span>|
|<span data-ttu-id="0abba-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1095"></span></span>|
|<span data-ttu-id="0abba-1096">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="0abba-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1097"></span></span>|
|<span data-ttu-id="0abba-1098">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-1098">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1099"></span></span>|
|<span data-ttu-id="0abba-1100">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1101"></span></span>|
|<span data-ttu-id="0abba-1102">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1103"></span></span>|
|<span data-ttu-id="0abba-1104">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1105"></span></span>|
|<span data-ttu-id="0abba-1106">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1107"></span></span>|
|<span data-ttu-id="0abba-1108">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1109"></span></span>|
|<span data-ttu-id="0abba-1110">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1111"></span></span>|
|<span data-ttu-id="0abba-1112">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1113"></span></span>|
|<span data-ttu-id="0abba-1114">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1115"></span></span>|
|<span data-ttu-id="0abba-1116">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1117"></span></span>|
|<span data-ttu-id="0abba-1118">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1119"></span></span>|
|<span data-ttu-id="0abba-1120">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1121"></span></span>|
   
 <span data-ttu-id="0abba-1122">**Verizon Akamai ЦС SureServer G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="0abba-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="0abba-1123">**Тема**</span><span class="sxs-lookup"><span data-stu-id="0abba-1123">**Subject**</span></span>|
|<span data-ttu-id="0abba-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1124"></span></span>|
|<span data-ttu-id="0abba-1125">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="0abba-1125">**Issuer**</span></span>|
|<span data-ttu-id="0abba-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1126"></span></span>|
|<span data-ttu-id="0abba-1127">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="0abba-1127">**Serial Number**</span></span>|
|<span data-ttu-id="0abba-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1128"></span></span>|
|<span data-ttu-id="0abba-1129">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="0abba-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="0abba-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1130"></span></span>|
|<span data-ttu-id="0abba-1131">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="0abba-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="0abba-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1132"></span></span>|
|<span data-ttu-id="0abba-1133">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="0abba-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="0abba-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1134"></span></span>|
|<span data-ttu-id="0abba-1135">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="0abba-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="0abba-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1136"></span></span>|
|<span data-ttu-id="0abba-1137">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="0abba-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1138"></span></span>|
|<span data-ttu-id="0abba-1139">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="0abba-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="0abba-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1140"></span></span>|
|<span data-ttu-id="0abba-1141">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="0abba-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1142"></span></span>|
|<span data-ttu-id="0abba-1143">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1144"></span></span>|
|<span data-ttu-id="0abba-1145">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="0abba-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="0abba-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1146"></span></span>|
|<span data-ttu-id="0abba-1147">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="0abba-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="0abba-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1148"></span></span>|
|<span data-ttu-id="0abba-1149">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="0abba-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="0abba-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1150"></span></span>|
|<span data-ttu-id="0abba-1151">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="0abba-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="0abba-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="0abba-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="0abba-1153">Сертификат дополнительные пути</span><span class="sxs-lookup"><span data-stu-id="0abba-1153">Additional certificate paths</span></span>
<span data-ttu-id="0abba-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="0abba-1154"></span></span>

<span data-ttu-id="0abba-1155">Следующие включить устаревшие сертификаты, которые не включены выше и объединяются с списке над по времени.</span><span class="sxs-lookup"><span data-stu-id="0abba-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


