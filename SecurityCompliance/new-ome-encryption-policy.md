---
title: Новая политика шифрования сообщений Office 365 для конфиденциальной информации
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 12/13/2018
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Сводка: Новую политику шифрования сообщений Office 365 для конфиденциальной информации.'
ms.openlocfilehash: 180050d1bf9303f6d29bc126e66ac53211c2fb34
ms.sourcegitcommit: 3aae959ea1ac5ef61a9942c681d334831e6b6038
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2018
ms.locfileid: "27271095"
---
# <a name="new-office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="f2255-103">Новая политика шифрования сообщений Office 365 для конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="f2255-103">New Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="f2255-p101">Мы будет создание новой политики автоматического в клиентах службы Office 365, которые будут применяться шифрования сообщений Office 365 на все сообщения электронной почты, которые содержат конфиденциальные данные и отправляются за пределами вашей организации. В этом правила потока обработки почты Exchange автоматически создается в клиент Office 365, чтобы вашей организации будет защищен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2255-p101">We will be creating a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to all emails that contain sensitive information and that are being sent outside your organization. This new Exchange mail flow rule will be automatically created in your Office 365 tenant so that your organization will be protected by default.</span></span>

## <a name="how-will-this-work"></a><span data-ttu-id="f2255-106">Как будет этой работы?</span><span class="sxs-lookup"><span data-stu-id="f2255-106">How will this work?</span></span>

<span data-ttu-id="f2255-p102">Вашей организации будет получать уведомления в центре Office 365 сообщение о том, дату, на котором будет создан эта политика автоматического клиента. Будет предоставлен по крайней мере 30-дневной уведомление, а также имеется возможность отказаться. Сценарий, в котором можно отключить потенциально является, если у вас есть решения сторонних производителей защиту от потери данных, уже выполняет сканирование на наличие типов конфиденциальной.</span><span class="sxs-lookup"><span data-stu-id="f2255-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types.</span></span>

## <a name="new-policy-details"></a><span data-ttu-id="f2255-109">Новые сведения о политике.</span><span class="sxs-lookup"><span data-stu-id="f2255-109">New policy details</span></span>

<span data-ttu-id="f2255-110">В вашей организации, которые будут автоматически шифровать сообщения электронной почты за пределами вашей организации с будет создано новое правило поток почты Exchange *Только зашифровать* политики, если они содержат следующие типы конфиденциальной информации:</span><span class="sxs-lookup"><span data-stu-id="f2255-110">A new Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if they contain the following sensitive information types:</span></span>

- <span data-ttu-id="f2255-111">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="f2255-111">ABA routing number</span></span>
- <span data-ttu-id="f2255-112">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="f2255-112">Credit card Number</span></span>
- <span data-ttu-id="f2255-113">Номер наркотиков бюро принудительное применение (DEA)</span><span class="sxs-lookup"><span data-stu-id="f2255-113">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="f2255-p103">США / номер паспорта Соединенное Королевство</span><span class="sxs-lookup"><span data-stu-id="f2255-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="f2255-116">Номер США банковского счета</span><span class="sxs-lookup"><span data-stu-id="f2255-116">U.S. bank account number</span></span>
- <span data-ttu-id="f2255-117">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="f2255-117">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="f2255-118">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="f2255-118">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="f2255-119">Те типы конфиденциальной региональными параметрами вашей организации, могут отличаться и будут передаваться в центр сообщений уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f2255-119">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="f2255-120">Что нужно сделать, чтобы подготовиться к этому изменению?</span><span class="sxs-lookup"><span data-stu-id="f2255-120">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="f2255-p104">Обновить или изменить любые существующие параметры конфигурации Office 365 до этого нового не нужно. Тем не менее может потребоваться обновление применимых пользовательская документация и обучающие материалы для подготовки пользователей в вашей организации, чтобы это изменение.</span><span class="sxs-lookup"><span data-stu-id="f2255-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span>

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="f2255-123">Это изменение представления в журнале аудита?</span><span class="sxs-lookup"><span data-stu-id="f2255-123">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="f2255-p105">Это действие аудита и доступна для пользователей.  Операция не «New-TransportRule» и меньше фрагмент пример записи аудита из поиска журнала аудита в центр соответствия требованиям и безопасности:</span><span class="sxs-lookup"><span data-stu-id="f2255-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="f2255-126">*{«CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345», «Типом записи»: 1, «ResultStatus»: «True», «UserKey»: «Оператор Microsoft»,» UserType»: 3, «версия»: 1, «рабочая нагрузка»: «Exchange», «ClientIP»: «123.456.147.68:17584», «ObjectId»: «идентификатор пользователя «,»»: «Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX ( 15.20.1382.008)","parameters»: {«Имя»: «Организация», «Значение»: "d 123456 221-12346" {«Имя»: «ApplyRightsProtectionTemplate», «Значение»: «Шифрование»}, {«Имя»: «Имя», «Значение»: «Шифрование исходящих конфиденциальные сообщения электронной почты (вне поля правила)»}, {«Имя»:» MessageContainsDataClassifications»... и т.д.*</span><span class="sxs-lookup"><span data-stu-id="f2255-126">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="f2255-127">Как я отказаться?</span><span class="sxs-lookup"><span data-stu-id="f2255-127">How do I opt-out?</span></span>

<span data-ttu-id="f2255-128">Если вы хотите отказаться от этого изменения, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="f2255-128">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="f2255-129">Подключение к [Exchange Online PowerShell](https://aka.ms/exopowershell) , как пользователь с ролью глобального администратора.</span><span class="sxs-lookup"><span data-stu-id="f2255-129">Connect to [Exchange Online PowerShell](https://aka.ms/exopowershell) as a user with the global administrator role.</span></span>
2.  <span data-ttu-id="f2255-130">Выполните следующий код после проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="f2255-130">Run the following code after authenticating:</span></span>

    ```
    Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
    ```

## <a name="how-do-i-disable-the-automatic-policy"></a><span data-ttu-id="f2255-131">Как отключить автоматическое политики?</span><span class="sxs-lookup"><span data-stu-id="f2255-131">How do I disable the automatic policy?</span></span>

<span data-ttu-id="f2255-132">Если вы не отказаться от этого изменения правила почты Exchange уже создана, можно [отключить правило](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , перейдя на **поток почты** > **правил** в Exchange admin center (EAC) и отключить правило «*шифровать исходящие конфиденциальные сообщения электронной почты (вне поля правила)*«.</span><span class="sxs-lookup"><span data-stu-id="f2255-132">If you didn’t opt-out of this change and the Exchange mail rule has already been created, you can [disable the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
