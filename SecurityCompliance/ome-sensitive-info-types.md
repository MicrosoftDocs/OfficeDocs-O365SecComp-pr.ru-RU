---
title: Новая политика шифрования сообщений Office 365 для конфиденциальной информации
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Сводка: Автоматически применяется политика шифрования сообщений Office 365 для развертывания для всех клиентов типы конфиденциальной информации.'
ms.openlocfilehash: a8cd132af2b1429698ea92779a3c54559e2b13e2
ms.sourcegitcommit: b936a2fd4b7f7a7099b96cc29580ed55bdb8bf2b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/10/2019
ms.locfileid: "27789457"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="aded8-103">Политика шифрования сообщений Office 365 для конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="aded8-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="aded8-p101">Мы будет создание новой политики автоматического в клиентах службы Office 365, которые будут применяться шифрования сообщений Office 365 на все сообщения электронной почты, которые содержат конфиденциальные данные и отправляются за пределами вашей организации. В этом правила потока обработки почты Exchange автоматически создается в клиент Office 365, чтобы вашей организации будет защищен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aded8-p101">We will be creating a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to all emails that contain sensitive information and that are being sent outside your organization. This new Exchange mail flow rule will be automatically created in your Office 365 tenant so that your organization will be protected by default.</span></span>

## <a name="when-to-expect-the-update-for-your-tenant"></a><span data-ttu-id="aded8-106">Когда планируется завершить обновление для клиента</span><span class="sxs-lookup"><span data-stu-id="aded8-106">When to expect the update for your tenant</span></span>

<span data-ttu-id="aded8-p102">Вашей организации будет получать уведомления в центре Office 365 сообщение о том, дату, на котором будет создан эта политика автоматического клиента. Будет предоставлен по крайней мере 30-дневной уведомление, а также имеется возможность отказаться. Сценарий, в котором можно отключить потенциально является, если у вас есть решения сторонних производителей защиту от потери данных, уже выполняет сканирование на наличие типов конфиденциальной. Дополнительные сведения о способах отказаться доступны далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="aded8-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types. More details on how to opt-out are available later in this article.</span></span>

## <a name="sensitive-information-type-policy-details"></a><span data-ttu-id="aded8-110">Сведения о политике типов конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="aded8-110">Sensitive information type policy details</span></span>

<span data-ttu-id="aded8-111">Правило поток почты Exchange будут создаваться в вашей организации, которые будут автоматически шифровать сообщения электронной почты за пределами вашей организации с *Зашифровать-только для* политики, если по электронной почте или вложения содержат следующие типы конфиденциальной информации:</span><span class="sxs-lookup"><span data-stu-id="aded8-111">An Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="aded8-112">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="aded8-112">ABA routing number</span></span>
- <span data-ttu-id="aded8-113">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="aded8-113">Credit card Number</span></span>
- <span data-ttu-id="aded8-114">Номер наркотиков бюро принудительное применение (DEA)</span><span class="sxs-lookup"><span data-stu-id="aded8-114">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="aded8-p103">США / номер паспорта Соединенное Королевство</span><span class="sxs-lookup"><span data-stu-id="aded8-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="aded8-117">Номер США банковского счета</span><span class="sxs-lookup"><span data-stu-id="aded8-117">U.S. bank account number</span></span>
- <span data-ttu-id="aded8-118">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="aded8-118">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="aded8-119">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="aded8-119">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="aded8-120">Те типы конфиденциальной региональными параметрами вашей организации, могут отличаться и будут передаваться в центр сообщений уведомлений.</span><span class="sxs-lookup"><span data-stu-id="aded8-120">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="aded8-121">Что нужно сделать, чтобы подготовиться к этому изменению?</span><span class="sxs-lookup"><span data-stu-id="aded8-121">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="aded8-p104">Обновить или изменить любые существующие параметры конфигурации Office 365 до этого нового не нужно. Тем не менее может потребоваться обновление применимых пользовательская документация и обучающие материалы для подготовки пользователей в вашей организации, чтобы это изменение. Совместное использование этих ресурсов шифрования сообщений Office 365 с вашими пользователями соответствующим образом:</span><span class="sxs-lookup"><span data-stu-id="aded8-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="aded8-125">Отправка, просмотр и ответ на зашифрованные сообщения в Outlook для ПК</span><span class="sxs-lookup"><span data-stu-id="aded8-125">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="aded8-126">Office 365 Essentials видео: Шифрование сообщений Office</span><span class="sxs-lookup"><span data-stu-id="aded8-126">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="aded8-127">Это изменение представления в журнале аудита?</span><span class="sxs-lookup"><span data-stu-id="aded8-127">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="aded8-p105">Это действие аудита и доступна для пользователей.  Операция не «New-TransportRule» и меньше фрагмент пример записи аудита из поиска журнала аудита в центр соответствия требованиям и безопасности:</span><span class="sxs-lookup"><span data-stu-id="aded8-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="aded8-130">*{«CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345», «Типом записи»: 1, «ResultStatus»: «True», «UserKey»: «Оператор Microsoft»,» UserType»: 3, «версия»: 1, «рабочая нагрузка»: «Exchange», «ClientIP»: «123.456.147.68:17584», «ObjectId»: «идентификатор пользователя «,»»: «Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","parameters»: {«Имя»: «Организация», «Значение»: "d 123456 221-12346" {«Имя»: «ApplyRightsProtectionTemplate», «Значение»: «Шифрование»}, {«Имя»: «Имя», «Значение»: «Шифрование исходящих конфиденциальные сообщения электронной почты (вне поля правила)»}, {«Имя»:» MessageContainsDataClassifications»... и т.д.*</span><span class="sxs-lookup"><span data-stu-id="aded8-130">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="aded8-131">Как я отказаться?</span><span class="sxs-lookup"><span data-stu-id="aded8-131">How do I opt-out?</span></span>

<span data-ttu-id="aded8-132">Если вы хотите отказаться от этого изменения, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="aded8-132">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="aded8-p106">Использование рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, начало сеанса Windows PowerShell и подключитесь к Exchange Online. Сведения содержатся в разделе [подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="aded8-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>
2. <span data-ttu-id="aded8-135">Используйте командлет Set-IRMConfiguration следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aded8-135">Run the Set-IRMConfiguration cmdlet as follows:</span></span>

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a><span data-ttu-id="aded8-136">Как отключить или настроить автоматическую политики?</span><span class="sxs-lookup"><span data-stu-id="aded8-136">How do I disable or customize the automatic policy?</span></span>

<span data-ttu-id="aded8-137">Если вы не отказаться от этого изменения и правила потока обработки почты Exchange уже создана, можно [отключить или изменить правило](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , перейдя на **поток почты** > **правил** в Exchange admin center (EAC) и отключить правило «*зашифровать Исходящие конфиденциальные сообщения электронной почты (вне поля правила)*«.</span><span class="sxs-lookup"><span data-stu-id="aded8-137">If you didn’t opt-out of this change and the Exchange mail flow rule has already been created, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
