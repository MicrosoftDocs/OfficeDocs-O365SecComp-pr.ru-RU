---
title: Настройка инфраструктуры политики отправителей в Office 365 для предотвращения спуфинга
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
description: Сводка. В этой статье описано, как обновить запись DNS, чтобы использовать инфраструктуру политики отправителей (SPF) с личным доменом в Office 365. С помощью инфраструктуры политики отправителей можно проверять почту, отправляемую из личного домена.
ms.openlocfilehash: 1670e646d4eb847c72159e0b8b730ae08ea285a8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026366"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a><span data-ttu-id="a076c-104">Настройка инфраструктуры политики отправителей в Office 365 для предотвращения спуфинга</span><span class="sxs-lookup"><span data-stu-id="a076c-104">Set up SPF in Office 365 to help prevent spoofing</span></span>

 <span data-ttu-id="a076c-p102">**Сводка.** В этой статье описано, как обновить запись DNS, чтобы использовать инфраструктуру политики отправителей (SPF) с личным доменом в Office 365. С помощью инфраструктуры политики отправителей можно проверять почту, отправляемую из личного домена.</span><span class="sxs-lookup"><span data-stu-id="a076c-p102">**Summary:** This article describes how to update a Domain Name Service (DNS) record so that you can use Sender Policy Framework (SPF) with your custom domain in Office 365. Using SPF helps to validate outbound email sent from your custom domain.</span></span> 
  
<span data-ttu-id="a076c-p103">Чтобы использовать личный домен в Office 365, в запись DNS необходимо добавить запись SPF TXT для предотвращения спуфинга. Инфраструктура политики отправителей определяет, каким почтовым серверам разрешается отправлять сообщения от вашего имени. Инфраструктура политики отправителей, а также DKIM, DMARC и другие технологии, поддерживаемые Office 365, помогают предотвратить спуфинг и фишинг. Инфраструктура политики отправителей добавляется в виде записи TXT, которую служба DNS использует, чтобы определить, какие почтовые серверы могут отправлять сообщения от имени вашего личного домена. Почтовые системы получателей могут просматривать записи SPF TXT, чтобы определить, было ли сообщение из вашего личного домена отправлено с уполномоченного сервера обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a076c-p103">In order to use a custom domain, Office 365 requires that you add a Sender Policy Framework (SPF) TXT record to your DNS record to help prevent spoofing. SPF identifies which mail servers are allowed to send mail on your behalf. Basically, SPF, along with DKIM, DMARC, and other technologies supported by Office 365 help prevent spoofing and phishing. SPF is added as a TXT record that is used by DNS to identify which mail servers can send mail on behalf of your custom domain. Recipient mail systems refer to the SPF TXT record to determine whether a message from your custom domain comes from an authorized messaging server.</span></span>
  
<span data-ttu-id="a076c-p104">Допустим, ваш личный домен contoso.com использует Office 365. Мы добавим запись SPF TXT, в которой перечислены серверы обмена сообщениями Office 365, разрешенные для домена. Когда сервер получателя получает сообщение от joe@contoso.com, сервер находит запись SPF TXT для домена contoso.com и определяет, является ли сообщение допустимым. Если сервер получателя определит, что сообщение отправлено с сервера, не указанного в списке серверов обмена сообщениями Office 365 в записи SPF, то сервер получателя может отклонить сообщение как спам.</span><span class="sxs-lookup"><span data-stu-id="a076c-p104">For example, let's say that your custom domain contoso.com uses Office 365. You add an SPF TXT record that lists the Office 365 messaging servers as legitimate mail servers for your domain. When the receiving messaging server gets a message from joe@contoso.com, the server looks up the SPF TXT record for contoso.com and finds out whether the message is valid. If the receiving server finds out that the message comes from a server other than the Office 365 messaging servers listed in the SPF record, the receiving mail server can choose to reject the message as spam.</span></span>
  
<span data-ttu-id="a076c-p105">Кроме того, если на вашем личном домене отсутствует запись SPF TXT, некоторые серверы получателей могут сразу отклонить сообщение. Это вызвано тем, что сервер получателя не может проверить, отправлено ли сообщение с уполномоченного сервера обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a076c-p105">Also, if your custom domain does not have an SPF TXT record, some receiving servers may reject the message outright. This is because the receiving server cannot validate that the message comes from an authorized messaging server.</span></span>
  
<span data-ttu-id="a076c-p106">Если для Office 365 уже настроена почта, то серверы обмена сообщениями Майкрософт уже включены в службу DNS в виде записи SPF TXT. Но в некоторых случаях может потребоваться обновить запись SPF TXT в службе DNS. Например:</span><span class="sxs-lookup"><span data-stu-id="a076c-p106">If you've already set up mail for Office 365, then you have already included Microsoft's messaging servers in DNS as an SPF TXT record. However, there are some cases where you may need to update your SPF TXT record in DNS. For example:</span></span>
  
- <span data-ttu-id="a076c-p107">Раньше, если вы использовали SharePoint Online, в личный домен нужно было добавить другую запись SPF TXT. Этого больше не требуется. Это изменение необходимо для того, чтобы уведомления SharePoint Online не попадали в папку нежелательной почты. Обновите запись SPF TXT, если достигнут предел в 10 запросов и возникают ошибки с сообщениями вроде "превышен предел запросов" и "слишком много прыжков".</span><span class="sxs-lookup"><span data-stu-id="a076c-p107">Previously, you had to add a different SPF TXT record to your custom domain if you were using SharePoint Online. This is no longer required. This change should reduce the risk of SharePoint Online notification messages ending up in the Junk Email folder. Update your SPF TXT record if you are hitting the 10 lookup limit and receiving errors that say things like, "exceeded the lookup limit" and "too many hops".</span></span>
    
- <span data-ttu-id="a076c-125">Используется гибридная среда с Office 365 и локальной службой Exchange.</span><span class="sxs-lookup"><span data-stu-id="a076c-125">If you have a hybrid environment with Office 365 and Exchange on-premises.</span></span>
    
- <span data-ttu-id="a076c-126">Вы планируете настроить DKIM и DMARC (рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="a076c-126">You intend to set up DKIM and DMARC (recommended).</span></span>
    
## <a name="updating-your-spf-txt-record-for-office-365"></a><span data-ttu-id="a076c-127">Обновление записи SPF TXT для Office 365</span><span class="sxs-lookup"><span data-stu-id="a076c-127">Updating your SPF TXT record for Office 365</span></span>
<span data-ttu-id="a076c-128"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="a076c-128"></span></span>

<span data-ttu-id="a076c-p108">Прежде чем обновлять запись TXT в службе DNS, необходимо собрать некоторые сведения и определить формат записи. Это поможет избежать ошибок DNS. Расширенные примеры и подробное обсуждение поддерживаемых команд для инфраструктуры политики отправителей см. в разделе [Как инфраструктура политики отправителей помогает предотвратить спуфинг и фишинг в Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).</span><span class="sxs-lookup"><span data-stu-id="a076c-p108">Before you update the TXT record in DNS, you need to gather some information and determine the format of the record. This will help prevent you from generating DNS errors. For advanced examples, a more detailed discussion about supported SPF syntax, see [How SPF works to prevent spoofing and phishing in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).</span></span>
  
<span data-ttu-id="a076c-132">Подготовьте указанные ниже данные.</span><span class="sxs-lookup"><span data-stu-id="a076c-132">Gather this information:</span></span>
  
- <span data-ttu-id="a076c-p109">Текущая запись SPF TXT для личного домена. Сведения о том, как это сделать, см. в статье [Сбор необходимых сведений для создания записей DNS в Office 365](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67).</span><span class="sxs-lookup"><span data-stu-id="a076c-p109">The current SPF TXT record for your custom domain. For instructions, see [Gather the information you need to create Office 365 DNS records](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67).</span></span>
    
- <span data-ttu-id="a076c-p110">IP-адреса всех локальных серверов обмена сообщениями. Пример: **192.168.0.1**.</span><span class="sxs-lookup"><span data-stu-id="a076c-p110">IP addresses of all on-premises messaging servers. For example, **192.168.0.1**.</span></span>
    
- <span data-ttu-id="a076c-p111">Доменные имена, используемые для всех сторонних доменов, которые требуется включить в запись SPF TXT. Некоторые поставщики массовых рассылок настраивают поддомены для своих клиентов. Например, компания MailChimp создала поддомен **servers.mcsv.net**.</span><span class="sxs-lookup"><span data-stu-id="a076c-p111">Domain names to use for all third-party domains that you need to include in your SPF TXT record. Some bulk mail providers have set up subdomains to use for their customers. For example, the company MailChimp has set up **servers.mcsv.net**.</span></span>
    
- <span data-ttu-id="a076c-p112">Определите, какое правило принудительного применения следует использовать для записи SPF TXT. Рекомендуется использовать правило **-all**. Подробные сведения о других вариантах команд см. в разделе [Синтаксис записи SPF TXT для Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365).</span><span class="sxs-lookup"><span data-stu-id="a076c-p112">Determine what enforcement rule you want to use for your SPF TXT record. We recommend **-all**. For detailed information about other syntax options, see [SPF TXT record syntax for Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365).</span></span>
    
### <a name="to-add-or-update-your-spf-txt-record"></a><span data-ttu-id="a076c-143">Добавление и обновление записи типа TXT инфраструктуры политики отправителей</span><span class="sxs-lookup"><span data-stu-id="a076c-143">To add or update your SPF TXT record</span></span>

1. <span data-ttu-id="a076c-144">Создайте запись типа TXT инфраструктуры политики отправителей (если вы еще не сделали этого) с помощью команд из указанной ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="a076c-144">If you have not already done so, form your SPF TXT record by using the syntax from the following table:</span></span>
    
||<span data-ttu-id="a076c-145">**Используемая система**</span><span class="sxs-lookup"><span data-stu-id="a076c-145">**If you're using...**</span></span>|<span data-ttu-id="a076c-146">**Распространенность среди пользователей Office 365**</span><span class="sxs-lookup"><span data-stu-id="a076c-146">**Common for Office 365 customers?**</span></span>|<span data-ttu-id="a076c-147">**Добавляемый параметр**</span><span class="sxs-lookup"><span data-stu-id="a076c-147">**Add this...**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a076c-148">1</span><span class="sxs-lookup"><span data-stu-id="a076c-148">1</span></span>  <br/> |<span data-ttu-id="a076c-149">Любая почтовая система (обязательно)</span><span class="sxs-lookup"><span data-stu-id="a076c-149">Any email system (required)</span></span>  <br/> |<span data-ttu-id="a076c-p113">Распространенная. Все записи SPF TXT начинаются с этого значения</span><span class="sxs-lookup"><span data-stu-id="a076c-p113">Common. All SPF TXT records start with this value</span></span>  <br/> |<span data-ttu-id="a076c-152">v=spf1</span><span class="sxs-lookup"><span data-stu-id="a076c-152">v=spf1</span></span>  <br/> |
|<span data-ttu-id="a076c-153">2 </span><span class="sxs-lookup"><span data-stu-id="a076c-153">2</span></span>  <br/> |<span data-ttu-id="a076c-154">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a076c-154">Exchange Online</span></span>  <br/> |<span data-ttu-id="a076c-155">Распространенная</span><span class="sxs-lookup"><span data-stu-id="a076c-155">Common</span></span>  <br/> |<span data-ttu-id="a076c-156">include:SPF.Protection.Outlook.com</span><span class="sxs-lookup"><span data-stu-id="a076c-156">include:spf.protection.outlook.com</span></span>  <br/> |
|<span data-ttu-id="a076c-157">3 </span><span class="sxs-lookup"><span data-stu-id="a076c-157">3</span></span>  <br/> |<span data-ttu-id="a076c-158">Только для Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a076c-158">Exchange Online dedicated only</span></span>  <br/> |<span data-ttu-id="a076c-159">Нераспространенная</span><span class="sxs-lookup"><span data-stu-id="a076c-159">Not common</span></span>  <br/> |<span data-ttu-id="a076c-160">IP4:23.103.224.0/19 ip4:206.191.224.0/19 ip4:40.103.0.0/16 include:spf.protection.outlook.com</span><span class="sxs-lookup"><span data-stu-id="a076c-160">ip4:23.103.224.0/19 ip4:206.191.224.0/19 ip4:40.103.0.0/16 include:spf.protection.outlook.com</span></span>  <br/> |
|<span data-ttu-id="a076c-161">4 </span><span class="sxs-lookup"><span data-stu-id="a076c-161">4</span></span>  <br/> |<span data-ttu-id="a076c-162">Office 365 Germany, только Microsoft Cloud Germany</span><span class="sxs-lookup"><span data-stu-id="a076c-162">Office 365 Germany, Microsoft Cloud Germany only</span></span>  <br/> |<span data-ttu-id="a076c-163">Нераспространенная</span><span class="sxs-lookup"><span data-stu-id="a076c-163">Not common</span></span>  <br/> |<span data-ttu-id="a076c-164">include:SPF.Protection.Outlook.de</span><span class="sxs-lookup"><span data-stu-id="a076c-164">include:spf.protection.outlook.de</span></span>  <br/> |
|<span data-ttu-id="a076c-165">5 </span><span class="sxs-lookup"><span data-stu-id="a076c-165">5</span></span>  <br/> |<span data-ttu-id="a076c-166">Сторонняя почтовая система</span><span class="sxs-lookup"><span data-stu-id="a076c-166">Third-party email system</span></span>  <br/> |<span data-ttu-id="a076c-167">Нераспространенная</span><span class="sxs-lookup"><span data-stu-id="a076c-167">Not common</span></span>  <br/> |<span data-ttu-id="a076c-168">include:\<доменное имя\>,</span><span class="sxs-lookup"><span data-stu-id="a076c-168">include:\<domain name\></span></span>  <br/> <span data-ttu-id="a076c-169">где <доменное имя> — это доменное имя сторонней почтовой системы.</span><span class="sxs-lookup"><span data-stu-id="a076c-169">Where domain name is the domain name of the third party email system.</span></span>  <br/> |
|<span data-ttu-id="a076c-170">6 </span><span class="sxs-lookup"><span data-stu-id="a076c-170">6</span></span>  <br/> |<span data-ttu-id="a076c-p114">Локальная почтовая система, например Exchange Online Protection с другой почтовой системой</span><span class="sxs-lookup"><span data-stu-id="a076c-p114">On-premises mail system. For example, Exchange Online Protection plus another mail system</span></span>  <br/> |<span data-ttu-id="a076c-173">Нераспространенная</span><span class="sxs-lookup"><span data-stu-id="a076c-173">Not common</span></span>  <br/> | <span data-ttu-id="a076c-174">Используйте один из следующих параметров для каждой дополнительной почтовой системы:</span><span class="sxs-lookup"><span data-stu-id="a076c-174">Use one of these for each additional mail system:</span></span>  <br/>  <span data-ttu-id="a076c-175">ip4:\<  _IP address_\></span><span class="sxs-lookup"><span data-stu-id="a076c-175">ip4:\<  _IP address_\></span></span>  <br/>  <span data-ttu-id="a076c-176">ip6:\<  _IP address_\></span><span class="sxs-lookup"><span data-stu-id="a076c-176">ip6:\<  _IP address_\></span></span>  <br/>  <span data-ttu-id="a076c-177">include:\<  _domain name_\></span><span class="sxs-lookup"><span data-stu-id="a076c-177">include:\<  _domain name_\></span></span>  <br/>  <span data-ttu-id="a076c-178">где значение \<  _IP address_\>  это IP-адрес другой почтовой системы, а \< _domain name_\>  доменное имя другой почтовой системы, которая отправляет сообщения от имени вашего домена.</span><span class="sxs-lookup"><span data-stu-id="a076c-178">Where the value for \<  _IP address_\> is the IP address of the other mail system and \< _domain name_\> is the domain name of the other mail system that sends mail on behalf of your domain.</span></span>  <br/> |
|<span data-ttu-id="a076c-179">7 </span><span class="sxs-lookup"><span data-stu-id="a076c-179">7</span></span>  <br/> |<span data-ttu-id="a076c-180">Любая почтовая система (обязательно)</span><span class="sxs-lookup"><span data-stu-id="a076c-180">Any email system (required)</span></span>  <br/> |<span data-ttu-id="a076c-p115">Распространенная. Все записи SPF TXT заканчиваются этим значением</span><span class="sxs-lookup"><span data-stu-id="a076c-p115">Common. All SPF TXT records end with this value</span></span>  <br/> |<span data-ttu-id="a076c-183">\< _enforcement rule_\></span><span class="sxs-lookup"><span data-stu-id="a076c-183">\< _enforcement rule_\></span></span>  <br/> <span data-ttu-id="a076c-p116">Это может быть одно из нескольких значений. Рекомендуем использовать значение **-all**.  </span><span class="sxs-lookup"><span data-stu-id="a076c-p116">This can be one of several values. We recommend that you use **-all**.  </span></span><br/> |
   
<span data-ttu-id="a076c-186">1.1, например если будет полностью размещенных в Office 365, то есть, необходимо заранее не локальных почтовых серверов вашей TXT SPF запись будет включать строки 1, 2 и 7 и будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a076c-186">1.1  For example, if you are fully-hosted in Office 365, that is, you have no on-premises mail servers, your SPF TXT record would include rows 1, 2, and 7 and would look like this:</span></span>
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

<span data-ttu-id="a076c-p117">1.2 это наиболее распространенные записи Office 365 SPF TXT. Эта запись работает практически всем пользователям, независимо от того, является ли центра данных Office 365 находится в США или в Европе (включая Германия) или в другом месте.</span><span class="sxs-lookup"><span data-stu-id="a076c-p117">1.2  This is the most common Office 365 SPF TXT record. This record works for just about everyone, regardless of whether your Office 365 datacenter is located in the United States, or in Europe (including Germany), or in another location.</span></span>
    
<span data-ttu-id="a076c-p118">1.3 тем не менее если вы приобрели Германии Office 365, частью Microsoft Cloud Германии, следует использовать инструкции include из строки 4 вместо строки 2. Например если будет полностью размещенных в Office 365 Германии, то есть, необходимо заранее не локальных почтовых серверов вашей TXT SPF запись будет включать строки 1, 4 и 7 и будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a076c-p118">1.3  However, if you have purchased Office 365 Germany, part of Microsoft Cloud Germany, you should use the include statement from line 4 instead of line 2. For example, if you are fully-hosted in Office 365 Germany, that is, you have no on-premises mail servers, your SPF TXT record would include rows 1, 4, and 7 and would look like this:</span></span>
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

<span data-ttu-id="a076c-p119">1.4, если уже развернут в Office 365 и были заданы записи SPF TXT для настраиваемого домена и будет перенесен в Office 365 Германия, необходимо обновить запись SPF TXT. Чтобы сделать это, измените **include:spf.protection.outlook.com** на **include.spf.protection.outlook.de**.</span><span class="sxs-lookup"><span data-stu-id="a076c-p119">1.4  If you are already deployed in Office 365 and have set up your SPF TXT records for your custom domain, and you are migrating to Office 365 Germany, you need to update your SPF TXT record. To do this, change **include:spf.protection.outlook.com** to **include.spf.protection.outlook.de**.</span></span>
    
2. <span data-ttu-id="a076c-p120">Создав запись SPF TXT, вам необходимо будет обновить ее в службе DNS. Для домена можно создать только одну запись SPF TXT. Поэтому если такая запись существует, то вместо того чтобы добавлять новую запись, следует обновить существующую. Откройте статью [Создание записей DNS для Office 365 при самостоятельном управлении записями DNS](https://support.office.microsoft.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23), а затем перейдите по ссылке, соответствующей вашему поставщику DNS. (Если ваш поставщик DNS не указан на этой странице, вы можете [выполнить общие инструкции](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) по добавлению записей или обратиться за помощью к поставщику DNS.)</span><span class="sxs-lookup"><span data-stu-id="a076c-p120">Once you have formed your SPF TXT record, you need to update the record in DNS. You can only have one SPF TXT record for a domain. If an SPF TXT record exists, instead of adding a new record, you need to update the existing record. Go to [Create DNS records for Office 365](https://support.office.microsoft.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23), and then click the link for your DNS host. (If your DNS host doesn't have a link on the page, you can [follow the general instructions](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) to add records or contact your DNS host for help.)</span></span> 
    
3. <span data-ttu-id="a076c-198">Проверьте свою запись SPF TXT.</span><span class="sxs-lookup"><span data-stu-id="a076c-198">Test your SPF TXT record.</span></span>
    
## <a name="more-information-about-spf"></a><span data-ttu-id="a076c-199">Дополнительные сведения об инфраструктуре политики отправителей</span><span class="sxs-lookup"><span data-stu-id="a076c-199">More information about SPF</span></span>
<span data-ttu-id="a076c-200"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="a076c-200"></span></span>

<span data-ttu-id="a076c-201">Расширенные примеры, подробное обсуждение поддерживаемого синтаксиса для инфраструктуры политики отправителей и сведения о спуфинге, устранении неполадок и о том, как Office 365 поддерживает инфраструктуру политики отправителей, см. в разделе [Как инфраструктура политики отправителей помогает предотвратить спуфинг и фишинг в Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).</span><span class="sxs-lookup"><span data-stu-id="a076c-201">For advanced examples, a more detailed discussion about supported SPF syntax, spoofing, troubleshooting, and how Office 365 supports SPF, see [How SPF works to prevent spoofing and phishing in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).</span></span>
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a><span data-ttu-id="a076c-202">Дальнейшие действия: после настройки инфраструктуры политики отправителей для Office 365</span><span class="sxs-lookup"><span data-stu-id="a076c-202">Next steps: After you set up SPF for Office 365</span></span>
<span data-ttu-id="a076c-203"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="a076c-203"></span></span>

<span data-ttu-id="a076c-p121">Возникли проблемы с записью типа TXT инфраструктуры политики отправителей? Прочитайте статью [Устранение неполадок: советы и рекомендации по инфраструктуре политики отправителей в Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span><span class="sxs-lookup"><span data-stu-id="a076c-p121">Having trouble with your SPF TXT record? Read [Troubleshooting: Best practices for SPF in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).</span></span>
  
 <span data-ttu-id="a076c-p122">Несмотря на то что инфраструктура политики отправителей разработана для предотвращения спуфинга, существует ряд методик, позволяющих обойти ее. Чтобы защититься от таких атак, по завершении настройки инфраструктуры политики отправителей необходимо настроить DKIM и DMARC для Office 365. Соответствующие инструкции по началу работы см. в статье [Проверка исходящей электронной почты, отправляемой с личного домена в Office 365, с помощью DKIM](use-dkim-to-validate-outbound-email.md). Дальнейшие действия см. в статье [Использование протокола DMARC для проверки электронной почты в Office 365](use-dmarc-to-validate-email.md).</span><span class="sxs-lookup"><span data-stu-id="a076c-p122">SPF is designed to help prevent spoofing, but there are spoofing techniques that SPF cannot protect against. In order to protect against these, once you have set up SPF, you should also configure DKIM and DMARC for Office 365. To get started, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md).</span></span>
  
