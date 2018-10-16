---
title: Цепочки сертификатов Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.assetid: 0c03e6b3-e73f-4316-9e2b-bf4091ae96bb
description: Office 365 использует ряд различных поставщиков. Ниже описаны полный перечень известных Office 365 корневые сертификаты, которые клиенты могут возникать при доступе к Office 365. Сведения о сертификатах, которые может потребоваться установить в собственную инфраструктуру, ознакомьтесь со статьей Plan стороннего SSL-сертификатов для Office 365. Следующие сведения о сертификате применяется ко всем экземплярам по всему миру и Национальный облака Office 365.
ms.openlocfilehash: 97e00833e57f8f6b7352650b0efdef51ddba77fa
ms.sourcegitcommit: 659b5f5b38ef7e838cdb44eaa38c18e48d922768
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2018
ms.locfileid: "25575363"
---
# <a name="office-365-certificate-chains"></a><span data-ttu-id="698c0-106">Цепочки сертификатов Office 365</span><span class="sxs-lookup"><span data-stu-id="698c0-106">Office 365 Certificate Chains</span></span>

<span data-ttu-id="698c0-p102">Office 365 использует ряд различных поставщиков. Ниже описаны полный перечень известных Office 365 корневые сертификаты, которые клиенты могут возникать при доступе к Office 365. Сведения о сертификатах, может потребоваться установить в собственную инфраструктуру содержатся в разделе [Планирование сторонних SSL-сертификатов для Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). Следующие сведения о сертификате применяется ко всем экземплярам по всему миру и Национальный облака Office 365.</span><span class="sxs-lookup"><span data-stu-id="698c0-p102">Office 365 leverages a number of different certificate providers. The following describes the complete list of known Office 365 root certificates that customers may encounter when accessing Office 365. For information on the certificates you may need to install in your own infrastructure, see [Plan for third-party SSL certificates for Office 365](https://support.office.com/article/b48cdf63-07e0-4cda-8c12-4871590f59ce). The following certificate information applies to all worldwide and national cloud instances of Office 365.</span></span>
  

|<span data-ttu-id="698c0-111">**Тип сертификата**</span><span class="sxs-lookup"><span data-stu-id="698c0-111">**Certificate type**</span></span>|<span data-ttu-id="698c0-112">**P7b – загрузить (en)**</span><span class="sxs-lookup"><span data-stu-id="698c0-112">**P7b download**</span></span>|<span data-ttu-id="698c0-113">**Конечные точки списка отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-113">**CRL Endpoints**</span></span>|<span data-ttu-id="698c0-114">**Конечные точки OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-114">**OCSP Endpoints**</span></span>|<span data-ttu-id="698c0-115">**Конечные точки Местоположений**</span><span class="sxs-lookup"><span data-stu-id="698c0-115">**AIA Endpoints**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="698c0-116">Общедоступные доверенные корневые сертификаты</span><span class="sxs-lookup"><span data-stu-id="698c0-116">Publicly Trusted Root Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#rootcerts) <br/> |[<span data-ttu-id="698c0-117">Office 365 корневой сертификат набора (p7b –)</span><span class="sxs-lookup"><span data-stu-id="698c0-117">Office 365 Root Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/A/5/A/A5AE01F3-D19B-4A11-9407-801263CEF72C/O365_Root_Certs_20170321.p7b) <br/> |<span data-ttu-id="698c0-118">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-118">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="698c0-119">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-119">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="698c0-120">Недоступно</span><span class="sxs-lookup"><span data-stu-id="698c0-120">N/A</span></span>  <br/> |<span data-ttu-id="698c0-121">Недоступно</span><span class="sxs-lookup"><span data-stu-id="698c0-121">N/A</span></span>  <br/> |
|[<span data-ttu-id="698c0-122">Общедоступные надежные промежуточных сертификатов</span><span class="sxs-lookup"><span data-stu-id="698c0-122">Publicly Trusted Intermediate Certificates</span></span>](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb#IntermediateCerts) <br/> |[<span data-ttu-id="698c0-123">Набор Office 365 промежуточных сертификатах (p7b –)</span><span class="sxs-lookup"><span data-stu-id="698c0-123">Office 365 Intermediate Certificate Bundle (P7B)</span></span>](http://download.microsoft.com/download/4/D/5/4D5339A4-0A4A-46AB-AE52-B179DEDA4BEC/O365_Intermediate_Certs_20170321.p7b)  <br/> |<span data-ttu-id="698c0-124">cdp1.public trust.com</span><span class="sxs-lookup"><span data-stu-id="698c0-124">cdp1.public-trust.com</span></span>  <br/> <span data-ttu-id="698c0-125">CRL.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="698c0-125">crl.cnnic.cn</span></span>  <br/> <span data-ttu-id="698c0-126">CRL.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-126">crl.entrust.net</span></span>  <br/> <span data-ttu-id="698c0-127">CRL.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="698c0-127">crl.globalsign.com</span></span>  <br/> <span data-ttu-id="698c0-128">CRL.GlobalSign.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-128">crl.globalsign.net</span></span>  <br/> <span data-ttu-id="698c0-129">CRL.identrust.com</span><span class="sxs-lookup"><span data-stu-id="698c0-129">crl.identrust.com</span></span>  <br/> <span data-ttu-id="698c0-130">CRL.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="698c0-130">crl.thawte.com</span></span>  <br/> <span data-ttu-id="698c0-131">crl3.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="698c0-131">crl3.digicert.com</span></span>  <br/> <span data-ttu-id="698c0-132">crl4.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="698c0-132">crl4.digicert.com</span></span>  <br/> <span data-ttu-id="698c0-133">s1.symcb.com</span><span class="sxs-lookup"><span data-stu-id="698c0-133">s1.symcb.com</span></span>  <br/> <span data-ttu-id="698c0-134">www.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-134">www.d-trust.net</span></span>  <br/> |<span data-ttu-id="698c0-135">isrg.trustid.OCSP.identrust.com</span><span class="sxs-lookup"><span data-stu-id="698c0-135">isrg.trustid.ocsp.identrust.com</span></span>  <br/> <span data-ttu-id="698c0-136">OCSP.DigiCert.com</span><span class="sxs-lookup"><span data-stu-id="698c0-136">ocsp.digicert.com</span></span>  <br/> <span data-ttu-id="698c0-137">OCSP.Entrust.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-137">ocsp.entrust.net</span></span>  <br/> <span data-ttu-id="698c0-138">OCSP.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="698c0-138">ocsp.globalsign.com</span></span>  <br/> <span data-ttu-id="698c0-139">OCSP.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="698c0-139">ocsp.omniroot.com</span></span>  <br/> <span data-ttu-id="698c0-140">OCSP.startssl.com</span><span class="sxs-lookup"><span data-stu-id="698c0-140">ocsp.startssl.com</span></span>  <br/> <span data-ttu-id="698c0-141">OCSP.Thawte.com</span><span class="sxs-lookup"><span data-stu-id="698c0-141">ocsp.thawte.com</span></span>  <br/> <span data-ttu-id="698c0-142">ocsp2.GlobalSign.com</span><span class="sxs-lookup"><span data-stu-id="698c0-142">ocsp2.globalsign.com</span></span>  <br/> <span data-ttu-id="698c0-143">ocspcnnicroot.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="698c0-143">ocspcnnicroot.cnnic.cn</span></span>  <br/> <span data-ttu-id="698c0-144">корневой c3-ca2-2009.ocsp.d-trust.net</span><span class="sxs-lookup"><span data-stu-id="698c0-144">root-c3-ca2-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="698c0-145">root-C3-cA2-EV-2009.OCSP.d-Trust.NET</span><span class="sxs-lookup"><span data-stu-id="698c0-145">root-c3-ca2-ev-2009.ocsp.d-trust.net</span></span>  <br/> <span data-ttu-id="698c0-146">s2.symcb.com</span><span class="sxs-lookup"><span data-stu-id="698c0-146">s2.symcb.com</span></span>  <br/> |<span data-ttu-id="698c0-147">AIA.startssl.com</span><span class="sxs-lookup"><span data-stu-id="698c0-147">aia.startssl.com</span></span>  <br/> <span data-ttu-id="698c0-148">Apps.identrust.com</span><span class="sxs-lookup"><span data-stu-id="698c0-148">apps.identrust.com</span></span>  <br/> <span data-ttu-id="698c0-149">cacert.omniroot.com</span><span class="sxs-lookup"><span data-stu-id="698c0-149">cacert.omniroot.com</span></span>  <br/> <span data-ttu-id="698c0-150">www.cnnic.CN</span><span class="sxs-lookup"><span data-stu-id="698c0-150">www.cnnic.cn</span></span>  <br/> |
   
<span data-ttu-id="698c0-151">Разверните корневой и промежуточные разделах ниже, чтобы просмотреть дополнительные сведения о поставщиках сертификата.</span><span class="sxs-lookup"><span data-stu-id="698c0-151">Expand the root and intermediate sections below to see additional details about the certificate providers.</span></span>
  
## <a name="office-365-root-certificate-details"></a><span data-ttu-id="698c0-152">Сведения о сертификате корневого Office 365</span><span class="sxs-lookup"><span data-stu-id="698c0-152">Office 365 Root Certificate Details</span></span>
<span data-ttu-id="698c0-153"><a name="RootCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="698c0-153"></span></span>

 <span data-ttu-id="698c0-154">**Baltimore CyberTrust Root**</span><span class="sxs-lookup"><span data-stu-id="698c0-154">**Baltimore CyberTrust Root**</span></span>
  
<span data-ttu-id="698c0-155">|:-----|</span><span class="sxs-lookup"><span data-stu-id="698c0-155">|:-----|</span></span>
|<span data-ttu-id="698c0-156">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-156">**Subject**</span></span>|
|:-----|
|<span data-ttu-id="698c0-157">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-157">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-158">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-158"></span></span>|
|<span data-ttu-id="698c0-159">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-159">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-160">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-160"></span></span>|
|<span data-ttu-id="698c0-161">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-161">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-162">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-162"></span></span>|
|<span data-ttu-id="698c0-163">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-163">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-164">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-164"></span></span>|
|<span data-ttu-id="698c0-165">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-165">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-166">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-166"></span></span>|
|<span data-ttu-id="698c0-167">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-167">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-168">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-168"></span></span>|
|<span data-ttu-id="698c0-169">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-169">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-170">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-170"></span></span>|
|<span data-ttu-id="698c0-171">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-171">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-172">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-172"></span></span>|
|<span data-ttu-id="698c0-173">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-173">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-174">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-174"></span></span>|
   
 <span data-ttu-id="698c0-175">**КОРНЕВОЙ CNNIC**</span><span class="sxs-lookup"><span data-stu-id="698c0-175">**CNNIC ROOT**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-176">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-176">**Subject**</span></span>|
|<span data-ttu-id="698c0-177">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-177"></span></span>|
|<span data-ttu-id="698c0-178">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-178">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-179">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-179"></span></span>|
|<span data-ttu-id="698c0-180">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-180">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-181">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-181"></span></span>|
|<span data-ttu-id="698c0-182">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-182">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-183">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-183"></span></span>|
|<span data-ttu-id="698c0-184">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-184">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-185">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-185"></span></span>|
|<span data-ttu-id="698c0-186">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-186">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-187">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-187"></span></span>|
|<span data-ttu-id="698c0-188">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-188">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-189">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-189"></span></span>|
|<span data-ttu-id="698c0-190">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-190">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-191">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-191"></span></span>|
|<span data-ttu-id="698c0-192">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-192">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-193">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-193"></span></span>|
|<span data-ttu-id="698c0-194">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-194">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-195">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-195"></span></span>|
|<span data-ttu-id="698c0-196">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-196">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-197">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-197"></span></span>|
   
 <span data-ttu-id="698c0-198">**DigiCert глобального корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="698c0-198">**DigiCert Global Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-199">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-199">**Subject**</span></span>|
|<span data-ttu-id="698c0-200">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-200"></span></span>|
|<span data-ttu-id="698c0-201">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-201">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-202">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-202"></span></span>|
|<span data-ttu-id="698c0-203">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-203">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-204">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-204"></span></span>|
|<span data-ttu-id="698c0-205">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-205">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-206">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-206"></span></span>|
|<span data-ttu-id="698c0-207">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-207">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-208">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-208"></span></span>|
|<span data-ttu-id="698c0-209">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-209">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-210">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-210"></span></span>|
|<span data-ttu-id="698c0-211">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-211">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-212">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-212"></span></span>|
|<span data-ttu-id="698c0-213">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-213">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-214">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-214"></span></span>|
|<span data-ttu-id="698c0-215">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-215">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-216">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-216"></span></span>|
|<span data-ttu-id="698c0-217">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-217">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-218">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-218"></span></span>|
|<span data-ttu-id="698c0-219">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-219">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-220">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-220"></span></span>|
   
 <span data-ttu-id="698c0-221">**Сертификат DigiCert высокой надежности корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="698c0-221">**DigiCert High Assurance EV Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-222">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-222">**Subject**</span></span>|
|<span data-ttu-id="698c0-223">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-223"></span></span>|
|<span data-ttu-id="698c0-224">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-224">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-225">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-225"></span></span>|
|<span data-ttu-id="698c0-226">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-226">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-227">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-227"></span></span>|
|<span data-ttu-id="698c0-228">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-228">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-229">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-229"></span></span>|
|<span data-ttu-id="698c0-230">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-230">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-231">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-231"></span></span>|
|<span data-ttu-id="698c0-232">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-232">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-233">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-233"></span></span>|
|<span data-ttu-id="698c0-234">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-234">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-235">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-235"></span></span>|
|<span data-ttu-id="698c0-236">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-236">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-237">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-237"></span></span>|
|<span data-ttu-id="698c0-238">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-238">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-239">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-239"></span></span>|
|<span data-ttu-id="698c0-240">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-240">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-241">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-241"></span></span>|
|<span data-ttu-id="698c0-242">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-242">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-243">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-243"></span></span>|
   
 <span data-ttu-id="698c0-244">**Центр сертификации Class 3 корневого ДОВЕРИЯ D 2 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="698c0-244">**D-TRUST Root Class 3 CA 2 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-245">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-245">**Subject**</span></span>|
|<span data-ttu-id="698c0-246">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-246"></span></span>|
|<span data-ttu-id="698c0-247">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-247">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-248">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-248"></span></span>|
|<span data-ttu-id="698c0-249">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-249">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-250">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-250"></span></span>|
|<span data-ttu-id="698c0-251">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-251">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-252">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-252"></span></span>|
|<span data-ttu-id="698c0-253">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-253">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-254">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-254"></span></span>|
|<span data-ttu-id="698c0-255">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-255">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-256">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-256"></span></span>|
|<span data-ttu-id="698c0-257">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-257">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-258">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-258"></span></span>|
|<span data-ttu-id="698c0-259">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-259">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-260">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-260"></span></span>|
|<span data-ttu-id="698c0-261">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-261">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-262">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-262"></span></span>|
|<span data-ttu-id="698c0-263">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-263">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-264">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-264"></span></span>|
|<span data-ttu-id="698c0-265">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-265">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-266">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-266"></span></span>|
   
 <span data-ttu-id="698c0-267">**Центр сертификации Class 3 корневого ДОВЕРИЯ D 2 высокой Надежности 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="698c0-267">**D-TRUST Root Class 3 CA 2 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-268">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-268">**Subject**</span></span>|
|<span data-ttu-id="698c0-269">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-269"></span></span>|
|<span data-ttu-id="698c0-270">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-270">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-271">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-271"></span></span>|
|<span data-ttu-id="698c0-272">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-272">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-273">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-273"></span></span>|
|<span data-ttu-id="698c0-274">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-274">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-275">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-275"></span></span>|
|<span data-ttu-id="698c0-276">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-276">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-277">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-277"></span></span>|
|<span data-ttu-id="698c0-278">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-278">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-279">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-279"></span></span>|
|<span data-ttu-id="698c0-280">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-280">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-281">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-281"></span></span>|
|<span data-ttu-id="698c0-282">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-282">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-283">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-283"></span></span>|
|<span data-ttu-id="698c0-284">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-284">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-285">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-285"></span></span>|
|<span data-ttu-id="698c0-286">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-286">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-287">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-287"></span></span>|
|<span data-ttu-id="698c0-288">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-288">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-289">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-289"></span></span>|
   
 <span data-ttu-id="698c0-290">**Переход на летнее время корневого ЦС X3**</span><span class="sxs-lookup"><span data-stu-id="698c0-290">**DST Root CA X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-291">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-291">**Subject**</span></span>|
|<span data-ttu-id="698c0-292">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-292"></span></span>|
|<span data-ttu-id="698c0-293">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-293">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-294">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-294"></span></span>|
|<span data-ttu-id="698c0-295">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-295">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-296">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-296"></span></span>|
|<span data-ttu-id="698c0-297">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-297">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-298">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-298"></span></span>|
|<span data-ttu-id="698c0-299">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-299">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-300">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-300"></span></span>|
|<span data-ttu-id="698c0-301">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-301">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-302">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-302"></span></span>|
|<span data-ttu-id="698c0-303">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-303">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-304">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-304"></span></span>|
|<span data-ttu-id="698c0-305">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-305">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-306">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-306"></span></span>|
|<span data-ttu-id="698c0-307">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-307">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-308">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-308"></span></span>|
|<span data-ttu-id="698c0-309">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-309">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-310">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-310"></span></span>|
   
 <span data-ttu-id="698c0-311">**Доверенный корневой центр сертификации - G2**</span><span class="sxs-lookup"><span data-stu-id="698c0-311">**Entrust Root Certification Authority - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-312">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-312">**Subject**</span></span>|
|<span data-ttu-id="698c0-313">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-313"></span></span>|
|<span data-ttu-id="698c0-314">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-314">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-315">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-315"></span></span>|
|<span data-ttu-id="698c0-316">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-316">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-317">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-317"></span></span>|
|<span data-ttu-id="698c0-318">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-318">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-319">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-319"></span></span>|
|<span data-ttu-id="698c0-320">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-320">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-321">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-321"></span></span>|
|<span data-ttu-id="698c0-322">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-322">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-323">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-323"></span></span>|
|<span data-ttu-id="698c0-324">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-324">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-325">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-325"></span></span>|
|<span data-ttu-id="698c0-326">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-326">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-327">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-327"></span></span>|
|<span data-ttu-id="698c0-328">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-328">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-329">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-329"></span></span>|
|<span data-ttu-id="698c0-330">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-330">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-331">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-331"></span></span>|
   
 <span data-ttu-id="698c0-332">**Центр сертификации Entrust.NET (2048)**</span><span class="sxs-lookup"><span data-stu-id="698c0-332">**Entrust.net Certification Authority (2048)**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-333">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-333">**Subject**</span></span>|
|<span data-ttu-id="698c0-334">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-334"></span></span>|
|<span data-ttu-id="698c0-335">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-335">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-336">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-336"></span></span>|
|<span data-ttu-id="698c0-337">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-337">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-338">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-338"></span></span>|
|<span data-ttu-id="698c0-339">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-339">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-340">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-340"></span></span>|
|<span data-ttu-id="698c0-341">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-341">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-342">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-342"></span></span>|
|<span data-ttu-id="698c0-343">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-343">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-344">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-344"></span></span>|
|<span data-ttu-id="698c0-345">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-345">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-346">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-346"></span></span>|
|<span data-ttu-id="698c0-347">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-347">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-348">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-348"></span></span>|
|<span data-ttu-id="698c0-349">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-349">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-350">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-350"></span></span>|
|<span data-ttu-id="698c0-351">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-351">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-352">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-352"></span></span>|
   
 <span data-ttu-id="698c0-353">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="698c0-353">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-354">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-354">**Subject**</span></span>|
|<span data-ttu-id="698c0-355">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-355"></span></span>|
|<span data-ttu-id="698c0-356">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-356">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-357">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-357"></span></span>|
|<span data-ttu-id="698c0-358">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-358">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-359">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-359"></span></span>|
|<span data-ttu-id="698c0-360">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-360">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-361">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-361"></span></span>|
|<span data-ttu-id="698c0-362">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-362">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-363">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-363"></span></span>|
|<span data-ttu-id="698c0-364">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-364">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-365">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-365"></span></span>|
|<span data-ttu-id="698c0-366">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-366">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-367">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-367"></span></span>|
|<span data-ttu-id="698c0-368">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-368">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-369">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-369"></span></span>|
|<span data-ttu-id="698c0-370">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-370">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-371">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-371"></span></span>|
|<span data-ttu-id="698c0-372">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-372">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-373">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-373"></span></span>|
|<span data-ttu-id="698c0-374">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-374">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-375">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-375"></span></span>|
|<span data-ttu-id="698c0-376">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-376">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-377">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-377"></span></span>|
   
 <span data-ttu-id="698c0-378">**GlobalSign корневого ЦС**</span><span class="sxs-lookup"><span data-stu-id="698c0-378">**GlobalSign Root CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-379">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-379">**Subject**</span></span>|
|<span data-ttu-id="698c0-380">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-380"></span></span>|
|<span data-ttu-id="698c0-381">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-381">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-382">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-382"></span></span>|
|<span data-ttu-id="698c0-383">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-383">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-384">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-384"></span></span>|
|<span data-ttu-id="698c0-385">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-385">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-386">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-386"></span></span>|
|<span data-ttu-id="698c0-387">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-387">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-388">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-388"></span></span>|
|<span data-ttu-id="698c0-389">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-389">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-390">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-390"></span></span>|
|<span data-ttu-id="698c0-391">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-391">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-392">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-392"></span></span>|
|<span data-ttu-id="698c0-393">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-393">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-394">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-394"></span></span>|
|<span data-ttu-id="698c0-395">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-395">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-396">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-396"></span></span>|
|<span data-ttu-id="698c0-397">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-397">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-398">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-398"></span></span>|
   
 <span data-ttu-id="698c0-399">**Thawte основной корневого ЦС - G3**</span><span class="sxs-lookup"><span data-stu-id="698c0-399">**thawte Primary Root CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-400">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-400">**Subject**</span></span>|
|<span data-ttu-id="698c0-401">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-401"></span></span>|
|<span data-ttu-id="698c0-402">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-402">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-403">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-403"></span></span>|
|<span data-ttu-id="698c0-404">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-404">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-405">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-405"></span></span>|
|<span data-ttu-id="698c0-406">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-406">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-407">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-407"></span></span>|
|<span data-ttu-id="698c0-408">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-408">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-409">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-409"></span></span>|
|<span data-ttu-id="698c0-410">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-410">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-411">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-411"></span></span>|
|<span data-ttu-id="698c0-412">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-412">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-413">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-413"></span></span>|
|<span data-ttu-id="698c0-414">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-414">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-415">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-415"></span></span>|
|<span data-ttu-id="698c0-416">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-416">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-417">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-417"></span></span>|
|<span data-ttu-id="698c0-418">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-418">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-419">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-419"></span></span>|
   
 <span data-ttu-id="698c0-420">**Главный общедоступный ЦС класса VeriSign 3 - G5**</span><span class="sxs-lookup"><span data-stu-id="698c0-420">**VeriSign Class 3 Public Primary Certification Authority - G5**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-421">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-421">**Subject**</span></span>|
|<span data-ttu-id="698c0-422">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-422"></span></span>|
|<span data-ttu-id="698c0-423">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-423">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-424">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-424"></span></span>|
|<span data-ttu-id="698c0-425">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-425">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-426">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-426"></span></span>|
|<span data-ttu-id="698c0-427">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-427">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-428">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-428"></span></span>|
|<span data-ttu-id="698c0-429">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-429">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-430">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-430"></span></span>|
|<span data-ttu-id="698c0-431">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-431">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-432">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-432"></span></span>|
|<span data-ttu-id="698c0-433">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-433">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-434">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-434"></span></span>|
|<span data-ttu-id="698c0-435">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-435">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-436">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-436"></span></span>|
|<span data-ttu-id="698c0-437">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-437">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-438">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-438"></span></span>|
|<span data-ttu-id="698c0-439">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-439">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-440">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-440"></span></span>|
   
## <a name="office-365-intermediate-certificate-details"></a><span data-ttu-id="698c0-441">Сведения о промежуточных сертификатах Office 365</span><span class="sxs-lookup"><span data-stu-id="698c0-441">Office 365 Intermediate Certificate Details</span></span>
<span data-ttu-id="698c0-442"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="698c0-442"></span></span>

 <span data-ttu-id="698c0-443">**CNNIC SHA256 SSL**</span><span class="sxs-lookup"><span data-stu-id="698c0-443">**CNNIC SHA256 SSL**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-444">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-444">**Subject**</span></span>|
|<span data-ttu-id="698c0-445">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-445"></span></span>|
|<span data-ttu-id="698c0-446">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-446">**Issuer**</span></span>|
|<span data-ttu-id="698c0-447">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-447"></span></span>|
|<span data-ttu-id="698c0-448">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-448">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-449">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-449"></span></span>|
|<span data-ttu-id="698c0-450">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-450">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-451">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-451"></span></span>|
|<span data-ttu-id="698c0-452">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-452">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-453">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-453"></span></span>|
|<span data-ttu-id="698c0-454">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-454">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-455">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-455"></span></span>|
|<span data-ttu-id="698c0-456">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-456">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-457">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-457"></span></span>|
|<span data-ttu-id="698c0-458">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-458">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-459">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-459"></span></span>|
|<span data-ttu-id="698c0-460">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-460">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-461">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-461"></span></span>|
|<span data-ttu-id="698c0-462">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-462">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-463">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-463"></span></span>|
|<span data-ttu-id="698c0-464">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-464">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-465">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-465"></span></span>|
|<span data-ttu-id="698c0-466">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-466">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-467">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-467"></span></span>|
|<span data-ttu-id="698c0-468">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="698c0-468">**AIA URLs**</span></span>|
|<span data-ttu-id="698c0-469">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-469"></span></span>|
|<span data-ttu-id="698c0-470">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-470">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-471">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-471"></span></span>|
|<span data-ttu-id="698c0-472">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-472">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-473">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-473"></span></span>|
   
 <span data-ttu-id="698c0-474">**Центра сертификации Class 3 D-TRUST SSL 1 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="698c0-474">**D-TRUST SSL Class 3 CA 1 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-475">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-475">**Subject**</span></span>|
|<span data-ttu-id="698c0-476">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-476"></span></span>|
|<span data-ttu-id="698c0-477">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-477">**Issuer**</span></span>|
|<span data-ttu-id="698c0-478">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-478"></span></span>|
|<span data-ttu-id="698c0-479">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-479">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="698c0-480">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-480"></span></span>|
|<span data-ttu-id="698c0-481">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-481">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-482">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-482"></span></span>|
|<span data-ttu-id="698c0-483">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-483">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-484">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-484"></span></span>|
|<span data-ttu-id="698c0-485">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-485">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-486">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-486"></span></span>|
|<span data-ttu-id="698c0-487">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-487">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-488">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-488"></span></span>|
|<span data-ttu-id="698c0-489">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-489">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-490">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-490"></span></span>|
|<span data-ttu-id="698c0-491">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-491">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-492">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-492"></span></span>|
|<span data-ttu-id="698c0-493">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-493">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-494">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-494"></span></span>|
|<span data-ttu-id="698c0-495">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-495">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-496">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-496"></span></span>|
|<span data-ttu-id="698c0-497">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-497">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-498">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-498"></span></span>|
|<span data-ttu-id="698c0-499">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-499">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-500">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-500"></span></span>|
|<span data-ttu-id="698c0-501">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-501">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-502">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-502"></span></span>|
|<span data-ttu-id="698c0-503">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-503">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-504">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-504"></span></span>|
   
 <span data-ttu-id="698c0-505">**Центра сертификации Class 3 D-TRUST SSL 1 высокой Надежности 2009 г.**</span><span class="sxs-lookup"><span data-stu-id="698c0-505">**D-TRUST SSL Class 3 CA 1 EV 2009**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-506">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-506">**Subject**</span></span>|
|<span data-ttu-id="698c0-507">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-507"></span></span>|
|<span data-ttu-id="698c0-508">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-508">**Issuer**</span></span>|
|<span data-ttu-id="698c0-509">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-509"></span></span>|
|<span data-ttu-id="698c0-510">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-510">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="698c0-511">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-511"></span></span>|
|<span data-ttu-id="698c0-512">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-512">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-513">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-513"></span></span>|
|<span data-ttu-id="698c0-514">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-514">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-515">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-515"></span></span>|
|<span data-ttu-id="698c0-516">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-516">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-517">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-517"></span></span>|
|<span data-ttu-id="698c0-518">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-518">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-519">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-519"></span></span>|
|<span data-ttu-id="698c0-520">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-520">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-521">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-521"></span></span>|
|<span data-ttu-id="698c0-522">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-522">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-523">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-523"></span></span>|
|<span data-ttu-id="698c0-524">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-524">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-525">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-525"></span></span>|
|<span data-ttu-id="698c0-526">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-526">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-527">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-527"></span></span>|
|<span data-ttu-id="698c0-528">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-528">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-529">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-529"></span></span>|
|<span data-ttu-id="698c0-530">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-530">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-531">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-531"></span></span>|
|<span data-ttu-id="698c0-532">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-532">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-533">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-533"></span></span>|
|<span data-ttu-id="698c0-534">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-534">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-535">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-535"></span></span>|
   
 <span data-ttu-id="698c0-536">**DigiCert облачным службам ЦС-1**</span><span class="sxs-lookup"><span data-stu-id="698c0-536">**DigiCert Cloud Services CA-1**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-537">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-537">**Subject**</span></span>|
|<span data-ttu-id="698c0-538">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-538"></span></span>|
|<span data-ttu-id="698c0-539">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-539">**Issuer**</span></span>|
|<span data-ttu-id="698c0-540">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-540"></span></span>|
|<span data-ttu-id="698c0-541">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-541">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-542">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-542"></span></span>|
|<span data-ttu-id="698c0-543">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-543">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-544">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-544"></span></span>|
|<span data-ttu-id="698c0-545">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-545">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-546">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-546"></span></span>|
|<span data-ttu-id="698c0-547">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-547">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-548">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-548"></span></span>|
|<span data-ttu-id="698c0-549">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-549">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-550">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-550"></span></span>|
|<span data-ttu-id="698c0-551">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-551">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-552">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-552"></span></span>|
|<span data-ttu-id="698c0-553">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-553">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-554">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-554"></span></span>|
|<span data-ttu-id="698c0-555">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-555">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-556">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-556"></span></span>|
|<span data-ttu-id="698c0-557">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-557">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-558">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-558"></span></span>|
|<span data-ttu-id="698c0-559">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-559">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-560">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-560"></span></span>|
|<span data-ttu-id="698c0-561">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-561">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-562">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-562"></span></span>|
|<span data-ttu-id="698c0-563">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-563">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-564">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-564"></span></span>|
   
 <span data-ttu-id="698c0-565">**DigiCert SHA2 высокой надежности сервера центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-565">**DigiCert SHA2 High Assurance Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-566">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-566">**Subject**</span></span>|
|<span data-ttu-id="698c0-567">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-567"></span></span>|
|<span data-ttu-id="698c0-568">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-568">**Issuer**</span></span>|
|<span data-ttu-id="698c0-569">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-569"></span></span>|
|<span data-ttu-id="698c0-570">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-570">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-571">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-571"></span></span>|
|<span data-ttu-id="698c0-572">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-572">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-573">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-573"></span></span>|
|<span data-ttu-id="698c0-574">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-574">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-575">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-575"></span></span>|
|<span data-ttu-id="698c0-576">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-576">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-577">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-577"></span></span>|
|<span data-ttu-id="698c0-578">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-578">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-579">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-579"></span></span>|
|<span data-ttu-id="698c0-580">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-580">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-581">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-581"></span></span>|
|<span data-ttu-id="698c0-582">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-582">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-583">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-583"></span></span>|
|<span data-ttu-id="698c0-584">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-584">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-585">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-585"></span></span>|
|<span data-ttu-id="698c0-586">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-586">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-587">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-587"></span></span>|
|<span data-ttu-id="698c0-588">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-588">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-589">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-589"></span></span>|
|<span data-ttu-id="698c0-590">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-590">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-591">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-591"></span></span>|
|<span data-ttu-id="698c0-592">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-592">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-593">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-593"></span></span>|
   
 <span data-ttu-id="698c0-594">**Безопасный сервер DigiCert SHA2 ЦС**</span><span class="sxs-lookup"><span data-stu-id="698c0-594">**DigiCert SHA2 Secure Server CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-595">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-595">**Subject**</span></span>|
|<span data-ttu-id="698c0-596">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-596"></span></span>|
|<span data-ttu-id="698c0-597">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-597">**Issuer**</span></span>|
|<span data-ttu-id="698c0-598">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-598"></span></span>|
|<span data-ttu-id="698c0-599">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-599">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-600">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-600"></span></span>|
|<span data-ttu-id="698c0-601">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-601">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-602">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-602"></span></span>|
|<span data-ttu-id="698c0-603">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-603">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-604">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-604"></span></span>|
|<span data-ttu-id="698c0-605">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-605">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-606">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-606"></span></span>|
|<span data-ttu-id="698c0-607">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-607">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-608">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-608"></span></span>|
|<span data-ttu-id="698c0-609">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-609">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-610">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-610"></span></span>|
|<span data-ttu-id="698c0-611">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-611">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-612">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-612"></span></span>|
|<span data-ttu-id="698c0-613">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-613">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-614">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-614"></span></span>|
|<span data-ttu-id="698c0-615">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-615">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-616">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-616"></span></span>|
|<span data-ttu-id="698c0-617">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-617">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-618">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-618"></span></span>|
|<span data-ttu-id="698c0-619">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-619">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-620">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-620"></span></span>|
|<span data-ttu-id="698c0-621">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-621">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-622">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-622"></span></span>|
   
 <span data-ttu-id="698c0-623">**Доверенный центр сертификации - L1C**</span><span class="sxs-lookup"><span data-stu-id="698c0-623">**Entrust Certification Authority - L1C**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-624">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-624">**Subject**</span></span>|
|<span data-ttu-id="698c0-625">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-625"></span></span>|
|<span data-ttu-id="698c0-626">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-626">**Issuer**</span></span>|
|<span data-ttu-id="698c0-627">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-627"></span></span>|
|<span data-ttu-id="698c0-628">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-628">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-629">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-629"></span></span>|
|<span data-ttu-id="698c0-630">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-630">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-631">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-631"></span></span>|
|<span data-ttu-id="698c0-632">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-632">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-633">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-633"></span></span>|
|<span data-ttu-id="698c0-634">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-634">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-635">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-635"></span></span>|
|<span data-ttu-id="698c0-636">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-636">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-637">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-637"></span></span>|
|<span data-ttu-id="698c0-638">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-638">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-639">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-639"></span></span>|
|<span data-ttu-id="698c0-640">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-640">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-641">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-641"></span></span>|
|<span data-ttu-id="698c0-642">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-642">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-643">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-643"></span></span>|
|<span data-ttu-id="698c0-644">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-644">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-645">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-645"></span></span>|
|<span data-ttu-id="698c0-646">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-646">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-647">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-647"></span></span>|
|<span data-ttu-id="698c0-648">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-648">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-649">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-649"></span></span>|
|<span data-ttu-id="698c0-650">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-650">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-651">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-651"></span></span>|
   
 <span data-ttu-id="698c0-652">**Доверенный центр сертификации - L1K**</span><span class="sxs-lookup"><span data-stu-id="698c0-652">**Entrust Certification Authority - L1K**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-653">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-653">**Subject**</span></span>|
|<span data-ttu-id="698c0-654">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-654"></span></span>|
|<span data-ttu-id="698c0-655">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-655">**Issuer**</span></span>|
|<span data-ttu-id="698c0-656">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-656"></span></span>|
|<span data-ttu-id="698c0-657">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-657">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-658">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-658"></span></span>|
|<span data-ttu-id="698c0-659">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-659">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-660">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-660"></span></span>|
|<span data-ttu-id="698c0-661">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-661">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-662">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-662"></span></span>|
|<span data-ttu-id="698c0-663">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-663">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-664">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-664"></span></span>|
|<span data-ttu-id="698c0-665">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-665">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-666">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-666"></span></span>|
|<span data-ttu-id="698c0-667">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-667">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-668">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-668"></span></span>|
|<span data-ttu-id="698c0-669">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-669">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-670">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-670"></span></span>|
|<span data-ttu-id="698c0-671">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-671">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-672">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-672"></span></span>|
|<span data-ttu-id="698c0-673">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-673">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-674">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-674"></span></span>|
|<span data-ttu-id="698c0-675">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-675">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-676">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-676"></span></span>|
|<span data-ttu-id="698c0-677">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-677">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-678">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-678"></span></span>|
|<span data-ttu-id="698c0-679">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-679">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-680">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-680"></span></span>|
   
 <span data-ttu-id="698c0-681">**GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="698c0-681">**GlobalSign**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-682">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-682">**Subject**</span></span>|
|<span data-ttu-id="698c0-683">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-683"></span></span>|
|<span data-ttu-id="698c0-684">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-684">**Issuer**</span></span>|
|<span data-ttu-id="698c0-685">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-685"></span></span>|
|<span data-ttu-id="698c0-686">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-686">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-687">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-687"></span></span>|
|<span data-ttu-id="698c0-688">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-688">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-689">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-689"></span></span>|
|<span data-ttu-id="698c0-690">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-690">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-691">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-691"></span></span>|
|<span data-ttu-id="698c0-692">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-692">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-693">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-693"></span></span>|
|<span data-ttu-id="698c0-694">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-694">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-695">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-695"></span></span>|
|<span data-ttu-id="698c0-696">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-696">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-697">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-697"></span></span>|
|<span data-ttu-id="698c0-698">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-698">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-699">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-699"></span></span>|
|<span data-ttu-id="698c0-700">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-700">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-701">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-701"></span></span>|
|<span data-ttu-id="698c0-702">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-702">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-703">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-703"></span></span>|
|<span data-ttu-id="698c0-704">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-704">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-705">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-705"></span></span>|
|<span data-ttu-id="698c0-706">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-706">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-707">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-707"></span></span>|
|<span data-ttu-id="698c0-708">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-708">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-709">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-709"></span></span>|
   
 <span data-ttu-id="698c0-710">**Расширенные проверки ЦС - SHA256 - G2 GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="698c0-710">**GlobalSign Extended Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-711">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-711">**Subject**</span></span>|
|<span data-ttu-id="698c0-712">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-712"></span></span>|
|<span data-ttu-id="698c0-713">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-713">**Issuer**</span></span>|
|<span data-ttu-id="698c0-714">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-714"></span></span>|
|<span data-ttu-id="698c0-715">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-715">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-716">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-716"></span></span>|
|<span data-ttu-id="698c0-717">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-717">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-718">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-718"></span></span>|
|<span data-ttu-id="698c0-719">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-719">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-720">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-720"></span></span>|
|<span data-ttu-id="698c0-721">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-721">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-722">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-722"></span></span>|
|<span data-ttu-id="698c0-723">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-723">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-724">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-724"></span></span>|
|<span data-ttu-id="698c0-725">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-725">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-726">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-726"></span></span>|
|<span data-ttu-id="698c0-727">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-727">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-728">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-728"></span></span>|
|<span data-ttu-id="698c0-729">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-729">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-730">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-730"></span></span>|
|<span data-ttu-id="698c0-731">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-731">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-732">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-732"></span></span>|
|<span data-ttu-id="698c0-733">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-733">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-734">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-734"></span></span>|
|<span data-ttu-id="698c0-735">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-735">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-736">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-736"></span></span>|
|<span data-ttu-id="698c0-737">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-737">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-738">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-738"></span></span>|
   
 <span data-ttu-id="698c0-739">**Расширенные проверки ЦС - SHA256 - G3 GlobalSign**</span><span class="sxs-lookup"><span data-stu-id="698c0-739">**GlobalSign Extended Validation CA - SHA256 - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-740">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-740">**Subject**</span></span>|
|<span data-ttu-id="698c0-741">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-741"></span></span>|
|<span data-ttu-id="698c0-742">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-742">**Issuer**</span></span>|
|<span data-ttu-id="698c0-743">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-743"></span></span>|
|<span data-ttu-id="698c0-744">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-744">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-745">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-745"></span></span>|
|<span data-ttu-id="698c0-746">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-746">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-747">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-747"></span></span>|
|<span data-ttu-id="698c0-748">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-748">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-749">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-749"></span></span>|
|<span data-ttu-id="698c0-750">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-750">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-751">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-751"></span></span>|
|<span data-ttu-id="698c0-752">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-752">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-753">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-753"></span></span>|
|<span data-ttu-id="698c0-754">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-754">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-755">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-755"></span></span>|
|<span data-ttu-id="698c0-756">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-756">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-757">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-757"></span></span>|
|<span data-ttu-id="698c0-758">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-758">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-759">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-759"></span></span>|
|<span data-ttu-id="698c0-760">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-760">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-761">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-761"></span></span>|
|<span data-ttu-id="698c0-762">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-762">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-763">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-763"></span></span>|
|<span data-ttu-id="698c0-764">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-764">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-765">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-765"></span></span>|
|<span data-ttu-id="698c0-766">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-766">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-767">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-767"></span></span>|
   
 <span data-ttu-id="698c0-768">**GlobalSign организации проверки ЦС - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="698c0-768">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-769">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-769">**Subject**</span></span>|
|<span data-ttu-id="698c0-770">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-770"></span></span>|
|<span data-ttu-id="698c0-771">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-771">**Issuer**</span></span>|
|<span data-ttu-id="698c0-772">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-772"></span></span>|
|<span data-ttu-id="698c0-773">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-773">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-774">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-774"></span></span>|
|<span data-ttu-id="698c0-775">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-775">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-776">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-776"></span></span>|
|<span data-ttu-id="698c0-777">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-777">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-778">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-778"></span></span>|
|<span data-ttu-id="698c0-779">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-779">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-780">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-780"></span></span>|
|<span data-ttu-id="698c0-781">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-781">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-782">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-782"></span></span>|
|<span data-ttu-id="698c0-783">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-783">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-784">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-784"></span></span>|
|<span data-ttu-id="698c0-785">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-785">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-786">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-786"></span></span>|
|<span data-ttu-id="698c0-787">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-787">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-788">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-788"></span></span>|
|<span data-ttu-id="698c0-789">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-789">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-790">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-790"></span></span>|
|<span data-ttu-id="698c0-791">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-791">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-792">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-792"></span></span>|
|<span data-ttu-id="698c0-793">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-793">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-794">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-794"></span></span>|
|<span data-ttu-id="698c0-795">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-795">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-796">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-796"></span></span>|
   
 <span data-ttu-id="698c0-797">**GlobalSign организации проверки ЦС - SHA256 - G2**</span><span class="sxs-lookup"><span data-stu-id="698c0-797">**GlobalSign Organization Validation CA - SHA256 - G2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-798">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-798">**Subject**</span></span>|
|<span data-ttu-id="698c0-799">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-799"></span></span>|
|<span data-ttu-id="698c0-800">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-800">**Issuer**</span></span>|
|<span data-ttu-id="698c0-801">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-801"></span></span>|
|<span data-ttu-id="698c0-802">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-802">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-803">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-803"></span></span>|
|<span data-ttu-id="698c0-804">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-804">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-805">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-805"></span></span>|
|<span data-ttu-id="698c0-806">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-806">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-807">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-807"></span></span>|
|<span data-ttu-id="698c0-808">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-808">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-809">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-809"></span></span>|
|<span data-ttu-id="698c0-810">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-810">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-811">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-811"></span></span>|
|<span data-ttu-id="698c0-812">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-812">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-813">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-813"></span></span>|
|<span data-ttu-id="698c0-814">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-814">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-815">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-815"></span></span>|
|<span data-ttu-id="698c0-816">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-816">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-817">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-817"></span></span>|
|<span data-ttu-id="698c0-818">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-818">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-819">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-819"></span></span>|
|<span data-ttu-id="698c0-820">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-820">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-821">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-821"></span></span>|
|<span data-ttu-id="698c0-822">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-822">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-823">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-823"></span></span>|
|<span data-ttu-id="698c0-824">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-824">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-825">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-825"></span></span>|
   
 <span data-ttu-id="698c0-826">**Давайте шифрования центра сертификации X3**</span><span class="sxs-lookup"><span data-stu-id="698c0-826">**Let's Encrypt Authority X3**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-827">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-827">**Subject**</span></span>|
|<span data-ttu-id="698c0-828">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-828"></span></span>|
|<span data-ttu-id="698c0-829">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-829">**Issuer**</span></span>|
|<span data-ttu-id="698c0-830">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-830"></span></span>|
|<span data-ttu-id="698c0-831">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-831">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-832">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-832"></span></span>|
|<span data-ttu-id="698c0-833">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-833">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-834">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-834"></span></span>|
|<span data-ttu-id="698c0-835">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-835">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-836">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-836"></span></span>|
|<span data-ttu-id="698c0-837">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-837">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-838">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-838"></span></span>|
|<span data-ttu-id="698c0-839">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-839">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-840">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-840"></span></span>|
|<span data-ttu-id="698c0-841">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-841">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-842">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-842"></span></span>|
|<span data-ttu-id="698c0-843">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-843">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-844">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-844"></span></span>|
|<span data-ttu-id="698c0-845">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-845">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-846">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-846"></span></span>|
|<span data-ttu-id="698c0-847">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-847">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-848">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-848"></span></span>|
|<span data-ttu-id="698c0-849">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-849">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-850">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-850"></span></span>|
|<span data-ttu-id="698c0-851">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="698c0-851">**AIA URLs**</span></span>|
|<span data-ttu-id="698c0-852">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-852"></span></span>|
|<span data-ttu-id="698c0-853">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-853">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-854">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-854"></span></span>|
|<span data-ttu-id="698c0-855">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-855">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-856">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-856"></span></span>|
   
 <span data-ttu-id="698c0-857">**SHA2 SSL ИТ-отдела Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="698c0-857">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-858">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-858">**Subject**</span></span>|
|<span data-ttu-id="698c0-859">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-859"></span></span>|
|<span data-ttu-id="698c0-860">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-860">**Issuer**</span></span>|
|<span data-ttu-id="698c0-861">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-861"></span></span>|
|<span data-ttu-id="698c0-862">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-862">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-863">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-863"></span></span>|
|<span data-ttu-id="698c0-864">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-864">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-865">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-865"></span></span>|
|<span data-ttu-id="698c0-866">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-866">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-867">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-867"></span></span>|
|<span data-ttu-id="698c0-868">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-868">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-869">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-869"></span></span>|
|<span data-ttu-id="698c0-870">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-870">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-871">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-871"></span></span>|
|<span data-ttu-id="698c0-872">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-872">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-873">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-873"></span></span>|
|<span data-ttu-id="698c0-874">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-874">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-875">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-875"></span></span>|
|<span data-ttu-id="698c0-876">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-876">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-877">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-877"></span></span>|
|<span data-ttu-id="698c0-878">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-878">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-879">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-879"></span></span>|
|<span data-ttu-id="698c0-880">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-880">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-881">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-881"></span></span>|
|<span data-ttu-id="698c0-882">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-882">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-883">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-883"></span></span>|
   
 <span data-ttu-id="698c0-884">**SHA2 SSL ИТ-отдела Майкрософт**</span><span class="sxs-lookup"><span data-stu-id="698c0-884">**Microsoft IT SSL SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-885">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-885">**Subject**</span></span>|
|<span data-ttu-id="698c0-886">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-886"></span></span>|
|<span data-ttu-id="698c0-887">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-887">**Issuer**</span></span>|
|<span data-ttu-id="698c0-888">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-888"></span></span>|
|<span data-ttu-id="698c0-889">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-889">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-890">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-890"></span></span>|
|<span data-ttu-id="698c0-891">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-891">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-892">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-892"></span></span>|
|<span data-ttu-id="698c0-893">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-893">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-894">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-894"></span></span>|
|<span data-ttu-id="698c0-895">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-895">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-896">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-896"></span></span>|
|<span data-ttu-id="698c0-897">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-897">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-898">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-898"></span></span>|
|<span data-ttu-id="698c0-899">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-899">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-900">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-900"></span></span>|
|<span data-ttu-id="698c0-901">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-901">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-902">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-902"></span></span>|
|<span data-ttu-id="698c0-903">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-903">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-904">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-904"></span></span>|
|<span data-ttu-id="698c0-905">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-905">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-906">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-906"></span></span>|
|<span data-ttu-id="698c0-907">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-907">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-908">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-908"></span></span>|
|<span data-ttu-id="698c0-909">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-909">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-910">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-910"></span></span>|
|<span data-ttu-id="698c0-911">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-911">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-912">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-912"></span></span>|
   
 <span data-ttu-id="698c0-913">**ИТ-отдела Майкрософт TLS ЦС 1**</span><span class="sxs-lookup"><span data-stu-id="698c0-913">**Microsoft IT TLS CA 1**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-914">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-914">**Subject**</span></span>|
|<span data-ttu-id="698c0-915">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-915"></span></span>|
|<span data-ttu-id="698c0-916">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-916">**Issuer**</span></span>|
|<span data-ttu-id="698c0-917">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-917"></span></span>|
|<span data-ttu-id="698c0-918">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-918">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-919">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-919"></span></span>|
|<span data-ttu-id="698c0-920">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-920">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-921">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-921"></span></span>|
|<span data-ttu-id="698c0-922">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-922">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-923">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-923"></span></span>|
|<span data-ttu-id="698c0-924">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-924">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-925">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-925"></span></span>|
|<span data-ttu-id="698c0-926">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-926">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-927">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-927"></span></span>|
|<span data-ttu-id="698c0-928">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-928">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-929">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-929"></span></span>|
|<span data-ttu-id="698c0-930">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-930">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-931">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-931"></span></span>|
|<span data-ttu-id="698c0-932">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-932">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-933">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-933"></span></span>|
|<span data-ttu-id="698c0-934">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-934">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-935">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-935"></span></span>|
|<span data-ttu-id="698c0-936">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-936">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-937">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-937"></span></span>|
|<span data-ttu-id="698c0-938">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-938">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-939">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-939"></span></span>|
|<span data-ttu-id="698c0-940">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-940">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-941">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-941"></span></span>|
   
 <span data-ttu-id="698c0-942">**ИТ-отдела Майкрософт TLS ЦС 2**</span><span class="sxs-lookup"><span data-stu-id="698c0-942">**Microsoft IT TLS CA 2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-943">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-943">**Subject**</span></span>|
|<span data-ttu-id="698c0-944">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-944"></span></span>|
|<span data-ttu-id="698c0-945">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-945">**Issuer**</span></span>|
|<span data-ttu-id="698c0-946">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-946"></span></span>|
|<span data-ttu-id="698c0-947">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-947">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-948">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-948"></span></span>|
|<span data-ttu-id="698c0-949">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-949">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-950">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-950"></span></span>|
|<span data-ttu-id="698c0-951">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-951">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-952">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-952"></span></span>|
|<span data-ttu-id="698c0-953">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-953">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-954">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-954"></span></span>|
|<span data-ttu-id="698c0-955">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-955">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-956">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-956"></span></span>|
|<span data-ttu-id="698c0-957">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-957">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-958">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-958"></span></span>|
|<span data-ttu-id="698c0-959">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-959">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-960">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-960"></span></span>|
|<span data-ttu-id="698c0-961">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-961">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-962">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-962"></span></span>|
|<span data-ttu-id="698c0-963">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-963">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-964">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-964"></span></span>|
|<span data-ttu-id="698c0-965">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-965">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-966">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-966"></span></span>|
|<span data-ttu-id="698c0-967">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-967">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-968">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-968"></span></span>|
|<span data-ttu-id="698c0-969">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-969">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-970">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-970"></span></span>|
   
 <span data-ttu-id="698c0-971">**ИТ-отдела Майкрософт TLS ЦС 4**</span><span class="sxs-lookup"><span data-stu-id="698c0-971">**Microsoft IT TLS CA 4**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-972">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-972">**Subject**</span></span>|
|<span data-ttu-id="698c0-973">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-973"></span></span>|
|<span data-ttu-id="698c0-974">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-974">**Issuer**</span></span>|
|<span data-ttu-id="698c0-975">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-975"></span></span>|
|<span data-ttu-id="698c0-976">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-976">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-977">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-977"></span></span>|
|<span data-ttu-id="698c0-978">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-978">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-979">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-979"></span></span>|
|<span data-ttu-id="698c0-980">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-980">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-981">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-981"></span></span>|
|<span data-ttu-id="698c0-982">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-982">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-983">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-983"></span></span>|
|<span data-ttu-id="698c0-984">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-984">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-985">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-985"></span></span>|
|<span data-ttu-id="698c0-986">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-986">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-987">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-987"></span></span>|
|<span data-ttu-id="698c0-988">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-988">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-989">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-989"></span></span>|
|<span data-ttu-id="698c0-990">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-990">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-991">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-991"></span></span>|
|<span data-ttu-id="698c0-992">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-992">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-993">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-993"></span></span>|
|<span data-ttu-id="698c0-994">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-994">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-995">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-995"></span></span>|
|<span data-ttu-id="698c0-996">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-996">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-997">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-997"></span></span>|
|<span data-ttu-id="698c0-998">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-998">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-999">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-999"></span></span>|
   
 <span data-ttu-id="698c0-1000">**ИТ-отдела Майкрософт TLS ЦС 5**</span><span class="sxs-lookup"><span data-stu-id="698c0-1000">**Microsoft IT TLS CA 5**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-1001">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-1001">**Subject**</span></span>|
|<span data-ttu-id="698c0-1002">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1002"></span></span>|
|<span data-ttu-id="698c0-1003">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-1003">**Issuer**</span></span>|
|<span data-ttu-id="698c0-1004">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1004"></span></span>|
|<span data-ttu-id="698c0-1005">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-1005">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-1006">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1006"></span></span>|
|<span data-ttu-id="698c0-1007">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-1007">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-1008">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1008"></span></span>|
|<span data-ttu-id="698c0-1009">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-1009">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-1010">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1010"></span></span>|
|<span data-ttu-id="698c0-1011">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-1011">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-1012">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1012"></span></span>|
|<span data-ttu-id="698c0-1013">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-1013">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-1014">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1014"></span></span>|
|<span data-ttu-id="698c0-1015">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1015">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1016">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1016"></span></span>|
|<span data-ttu-id="698c0-1017">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-1017">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1018">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1018"></span></span>|
|<span data-ttu-id="698c0-1019">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1019">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-1020">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1020"></span></span>|
|<span data-ttu-id="698c0-1021">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1021">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1022">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1022"></span></span>|
|<span data-ttu-id="698c0-1023">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1023">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1024">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1024"></span></span>|
|<span data-ttu-id="698c0-1025">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-1025">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-1026">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1026"></span></span>|
|<span data-ttu-id="698c0-1027">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-1027">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-1028">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1028"></span></span>|
   
 <span data-ttu-id="698c0-1029">**3 высокой Надежности SSL класс Symantec ЦС - G3**</span><span class="sxs-lookup"><span data-stu-id="698c0-1029">**Symantec Class 3 EV SSL CA - G3**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-1030">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-1030">**Subject**</span></span>|
|<span data-ttu-id="698c0-1031">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1031"></span></span>|
|<span data-ttu-id="698c0-1032">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-1032">**Issuer**</span></span>|
|<span data-ttu-id="698c0-1033">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1033"></span></span>|
|<span data-ttu-id="698c0-1034">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1034">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="698c0-1035">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1035"></span></span>|
|<span data-ttu-id="698c0-1036">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-1036">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-1037">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1037"></span></span>|
|<span data-ttu-id="698c0-1038">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-1038">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-1039">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1039"></span></span>|
|<span data-ttu-id="698c0-1040">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-1040">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-1041">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1041"></span></span>|
|<span data-ttu-id="698c0-1042">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-1042">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-1043">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1043"></span></span>|
|<span data-ttu-id="698c0-1044">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-1044">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-1045">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1045"></span></span>|
|<span data-ttu-id="698c0-1046">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1046">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1047">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1047"></span></span>|
|<span data-ttu-id="698c0-1048">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-1048">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1049">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1049"></span></span>|
|<span data-ttu-id="698c0-1050">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1050">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-1051">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1051"></span></span>|
|<span data-ttu-id="698c0-1052">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1052">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1053">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1053"></span></span>|
|<span data-ttu-id="698c0-1054">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1054">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1055">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1055"></span></span>|
|<span data-ttu-id="698c0-1056">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-1056">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-1057">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1057"></span></span>|
|<span data-ttu-id="698c0-1058">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-1058">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-1059">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1059"></span></span>|
   
 <span data-ttu-id="698c0-1060">**Безопасный сервер Symantec класса 3 ЦС - G4**</span><span class="sxs-lookup"><span data-stu-id="698c0-1060">**Symantec Class 3 Secure Server CA - G4**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-1061">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-1061">**Subject**</span></span>|
|<span data-ttu-id="698c0-1062">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1062"></span></span>|
|<span data-ttu-id="698c0-1063">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-1063">**Issuer**</span></span>|
|<span data-ttu-id="698c0-1064">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1064"></span></span>|
|<span data-ttu-id="698c0-1065">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1065">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="698c0-1066">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1066"></span></span>|
|<span data-ttu-id="698c0-1067">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-1067">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-1068">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1068"></span></span>|
|<span data-ttu-id="698c0-1069">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-1069">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-1070">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1070"></span></span>|
|<span data-ttu-id="698c0-1071">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-1071">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-1072">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1072"></span></span>|
|<span data-ttu-id="698c0-1073">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-1073">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-1074">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1074"></span></span>|
|<span data-ttu-id="698c0-1075">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-1075">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-1076">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1076"></span></span>|
|<span data-ttu-id="698c0-1077">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1077">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1078">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1078"></span></span>|
|<span data-ttu-id="698c0-1079">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-1079">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1080">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1080"></span></span>|
|<span data-ttu-id="698c0-1081">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1081">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-1082">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1082"></span></span>|
|<span data-ttu-id="698c0-1083">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1083">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1084">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1084"></span></span>|
|<span data-ttu-id="698c0-1085">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1085">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1086">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1086"></span></span>|
|<span data-ttu-id="698c0-1087">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-1087">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-1088">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1088"></span></span>|
|<span data-ttu-id="698c0-1089">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-1089">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-1090">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1090"></span></span>|
   
 <span data-ttu-id="698c0-1091">**Thawte SHA256 SSL ЦС**</span><span class="sxs-lookup"><span data-stu-id="698c0-1091">**thawte SHA256 SSL CA**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-1092">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-1092">**Subject**</span></span>|
|<span data-ttu-id="698c0-1093">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1093"></span></span>|
|<span data-ttu-id="698c0-1094">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-1094">**Issuer**</span></span>|
|<span data-ttu-id="698c0-1095">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1095"></span></span>|
|<span data-ttu-id="698c0-1096">**Альтернативное имя субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1096">**Subject Alternative Name**</span></span>|
|<span data-ttu-id="698c0-1097">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1097"></span></span>|
|<span data-ttu-id="698c0-1098">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-1098">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-1099">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1099"></span></span>|
|<span data-ttu-id="698c0-1100">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-1100">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-1101">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1101"></span></span>|
|<span data-ttu-id="698c0-1102">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-1102">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-1103">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1103"></span></span>|
|<span data-ttu-id="698c0-1104">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-1104">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-1105">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1105"></span></span>|
|<span data-ttu-id="698c0-1106">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-1106">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-1107">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1107"></span></span>|
|<span data-ttu-id="698c0-1108">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1108">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1109">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1109"></span></span>|
|<span data-ttu-id="698c0-1110">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-1110">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1111">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1111"></span></span>|
|<span data-ttu-id="698c0-1112">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1112">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-1113">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1113"></span></span>|
|<span data-ttu-id="698c0-1114">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1114">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1115">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1115"></span></span>|
|<span data-ttu-id="698c0-1116">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1116">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1117">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1117"></span></span>|
|<span data-ttu-id="698c0-1118">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-1118">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-1119">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1119"></span></span>|
|<span data-ttu-id="698c0-1120">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-1120">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-1121">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1121"></span></span>|
   
 <span data-ttu-id="698c0-1122">**Verizon Akamai ЦС SureServer G14-SHA2**</span><span class="sxs-lookup"><span data-stu-id="698c0-1122">**Verizon Akamai SureServer CA G14-SHA2**</span></span>
  
||
|:-----|
|<span data-ttu-id="698c0-1123">**Тема**</span><span class="sxs-lookup"><span data-stu-id="698c0-1123">**Subject**</span></span>|
|<span data-ttu-id="698c0-1124">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1124"></span></span>|
|<span data-ttu-id="698c0-1125">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="698c0-1125">**Issuer**</span></span>|
|<span data-ttu-id="698c0-1126">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1126"></span></span>|
|<span data-ttu-id="698c0-1127">**Серийный номер**</span><span class="sxs-lookup"><span data-stu-id="698c0-1127">**Serial Number**</span></span>|
|<span data-ttu-id="698c0-1128">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1128"></span></span>|
|<span data-ttu-id="698c0-1129">**Длина открытого ключа**</span><span class="sxs-lookup"><span data-stu-id="698c0-1129">**Public Key Length**</span></span>|
|<span data-ttu-id="698c0-1130">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1130"></span></span>|
|<span data-ttu-id="698c0-1131">**Алгоритм подписи**</span><span class="sxs-lookup"><span data-stu-id="698c0-1131">**Signature Algorithm**</span></span>|
|<span data-ttu-id="698c0-1132">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1132"></span></span>|
|<span data-ttu-id="698c0-1133">**Срок действия не до**</span><span class="sxs-lookup"><span data-stu-id="698c0-1133">**Validity Not Before**</span></span>|
|<span data-ttu-id="698c0-1134">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1134"></span></span>|
|<span data-ttu-id="698c0-1135">**Не после действия**</span><span class="sxs-lookup"><span data-stu-id="698c0-1135">**Validity Not After**</span></span>|
|<span data-ttu-id="698c0-1136">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1136"></span></span>|
|<span data-ttu-id="698c0-1137">**Идентификатор ключа субъекта**</span><span class="sxs-lookup"><span data-stu-id="698c0-1137">**Subject Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1138">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1138"></span></span>|
|<span data-ttu-id="698c0-1139">**Идентификатор ключа центра сертификации**</span><span class="sxs-lookup"><span data-stu-id="698c0-1139">**Authority Key Identifier**</span></span>|
|<span data-ttu-id="698c0-1140">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1140"></span></span>|
|<span data-ttu-id="698c0-1141">**Отпечаток (SHA-1)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1141">**Thumbprint (SHA-1)**</span></span>|
|<span data-ttu-id="698c0-1142">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1142"></span></span>|
|<span data-ttu-id="698c0-1143">**Отпечаток (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1143">**Thumbprint (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1144">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1144"></span></span>|
|<span data-ttu-id="698c0-1145">**ПИН-кода (SHA-256)**</span><span class="sxs-lookup"><span data-stu-id="698c0-1145">**Pin (SHA-256)**</span></span>|
|<span data-ttu-id="698c0-1146">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1146"></span></span>|
|<span data-ttu-id="698c0-1147">**URL-адреса, Местоположений**</span><span class="sxs-lookup"><span data-stu-id="698c0-1147">**AIA URLs**</span></span>|
|<span data-ttu-id="698c0-1148">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1148"></span></span>|
|<span data-ttu-id="698c0-1149">**URL-адреса списков отзыва Сертификатов**</span><span class="sxs-lookup"><span data-stu-id="698c0-1149">**CRL URLs**</span></span>|
|<span data-ttu-id="698c0-1150">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1150"></span></span>|
|<span data-ttu-id="698c0-1151">**URL-адреса OCSP**</span><span class="sxs-lookup"><span data-stu-id="698c0-1151">**OCSP URLs**</span></span>|
|<span data-ttu-id="698c0-1152">:-----</span><span class="sxs-lookup"><span data-stu-id="698c0-1152"></span></span>|
   
## <a name="additional-certificate-paths"></a><span data-ttu-id="698c0-1153">Сертификат дополнительные пути</span><span class="sxs-lookup"><span data-stu-id="698c0-1153">Additional certificate paths</span></span>
<span data-ttu-id="698c0-1154"><a name="IntermediateCerts"> </a></span><span class="sxs-lookup"><span data-stu-id="698c0-1154"></span></span>

<span data-ttu-id="698c0-1155">Следующие включить устаревшие сертификаты, которые не включены выше и объединяются с списке над по времени.</span><span class="sxs-lookup"><span data-stu-id="698c0-1155">The following include legacy certificates that aren't included above and will be merged with the list above over time.</span></span>
  
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


