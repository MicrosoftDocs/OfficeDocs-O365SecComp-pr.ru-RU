---
title: Создание политики типов конфиденциальной информации для организации с помощью шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Сводка: политика шифрования сообщений Office 365 для типов конфиденциальной информации.'
ms.openlocfilehash: 44966303ec7c58fdd82f733e1922073de848cf73
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834838"
---
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a><span data-ttu-id="fe8fe-103">Создание политики типов конфиденциальной информации для организации с помощью шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="fe8fe-103">Create a sensitive information type policy for your organization using Office 365 Message Encryption</span></span>

<span data-ttu-id="fe8fe-104">Для создания политики типов конфиденциальной информации с помощью шифрования сообщений Office 365 можно использовать правила для обработки почты Exchange или предотвращение потери данных (DLP) Office 365.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create a sensitive information type policy with Office 365 Message Encryption.</span></span> <span data-ttu-id="fe8fe-105">Чтобы создать правило для процесса обработки почты Exchange, можно использовать центр администрирования Exchange или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-105">To create an Exchange mail flow rule, you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="fe8fe-106">Создание политики с помощью правил для почтового процесса в центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="fe8fe-106">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="fe8fe-107">Войдите в центр администрирования Exchange и перейдите к разделу**правила**для обработки **почтового процесса** > .</span><span class="sxs-lookup"><span data-stu-id="fe8fe-107">Sign in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**.</span></span> <span data-ttu-id="fe8fe-108">На странице Правила создайте правило, которое применяет шифрование сообщений Office 365.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-108">On the Rules page, create a rule that applies Office 365 Message Encryption.</span></span> <span data-ttu-id="fe8fe-109">Вы можете создать правило на основе таких условий, как присутствие определенных ключевых слов или типов конфиденциальной информации в сообщении или вложении.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-109">You can create a rule based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="fe8fe-110">Создание политики с помощью правил для почтового процесса в PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe8fe-110">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="fe8fe-111">Используйте рабочую или учебную учетную запись с разрешениями глобального администратора в организации Office 365, запустите сеанс Windows PowerShell и подключитесь к Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-111">Use a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="fe8fe-112">Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="fe8fe-112">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span> <span data-ttu-id="fe8fe-113">Используйте командлеты Set – IRMConfiguration и New – TransportRule для создания политики.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-113">Use the Set-IRMConfiguration and New-TransportRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="fe8fe-114">Пример правила для процесса обработки почты, созданного с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe8fe-114">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="fe8fe-115">Выполните следующие команды в PowerShell, чтобы создать правило потока обработки почты Exchange, которое автоматически шифрует сообщения, отправляемые за границы Организации, с помощью политики *только для шифрования* , если сообщения электронной почты или их вложения содержат следующие конфиденциальные сведения типом</span><span class="sxs-lookup"><span data-stu-id="fe8fe-115">Run the following commands in PowerShell to create an Exchange mail flow rule that automatically encrypts emails sent outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="fe8fe-116">Номер маршрутизации код банка ABA</span><span class="sxs-lookup"><span data-stu-id="fe8fe-116">ABA routing number</span></span>
- <span data-ttu-id="fe8fe-117">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="fe8fe-117">Credit card Number</span></span>
- <span data-ttu-id="fe8fe-118">Номер агентства для применения наркотиков (DEA)</span><span class="sxs-lookup"><span data-stu-id="fe8fe-118">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="fe8fe-119">США/ВЕЛИКОБРИТАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe8fe-119">U.S. / U.K.</span></span> <span data-ttu-id="fe8fe-120">passport number</span><span class="sxs-lookup"><span data-stu-id="fe8fe-120">passport number</span></span>
- <span data-ttu-id="fe8fe-121">Номер банковского счета США</span><span class="sxs-lookup"><span data-stu-id="fe8fe-121">U.S. bank account number</span></span>
- <span data-ttu-id="fe8fe-122">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="fe8fe-122">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="fe8fe-123">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="fe8fe-123">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="fe8fe-124">Как получатели обращаются к вложениям</span><span class="sxs-lookup"><span data-stu-id="fe8fe-124">How recipients access attachments</span></span>

<span data-ttu-id="fe8fe-125">После того как Office 365 шифрует сообщение, получатели имеют неограниченный доступ к вложениям при обращении к зашифрованным электронным сообщениям и их открытии.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-125">After Office 365 encrypts a message, recipients have unrestricted access to attachments when they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="fe8fe-126">Подготовка к выполнению этого изменения</span><span class="sxs-lookup"><span data-stu-id="fe8fe-126">To prepare for this change</span></span>

<span data-ttu-id="fe8fe-127">Вам может потребоваться обновить любую документацию конечного пользователя и обучающие материалы, чтобы подготовить пользователей в Организации к этому изменению.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-127">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span> <span data-ttu-id="fe8fe-128">Предоставьте им доступ к этим ресурсам по шифрованию сообщений Office 365, используя соответствующие пользователи:</span><span class="sxs-lookup"><span data-stu-id="fe8fe-128">Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="fe8fe-129">Отправка, просмотр зашифрованных сообщений и ответ на них в Outlook для компьютера</span><span class="sxs-lookup"><span data-stu-id="fe8fe-129">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="fe8fe-130">Видео Office 365 Essentials: шифрование сообщений Office</span><span class="sxs-lookup"><span data-stu-id="fe8fe-130">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="fe8fe-131">Просмотр изменений в журнале аудита</span><span class="sxs-lookup"><span data-stu-id="fe8fe-131">View these changes in the Audit log</span></span>

<span data-ttu-id="fe8fe-132">Office 365 выполняет аудит этого действия и делает его доступным для администраторов Office 365.</span><span class="sxs-lookup"><span data-stu-id="fe8fe-132">Office 365 audits this activity and makes it available to Office 365 administrators.</span></span> <span data-ttu-id="fe8fe-133">Операция — "New-TransportRule", а фрагмент примера записи аудита из поиска в журнале аудита в центре безопасности _Амп_ соответствия требованиям ниже:</span><span class="sxs-lookup"><span data-stu-id="fe8fe-133">The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="fe8fe-134">Отключение или Настройка политики типов конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="fe8fe-134">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="fe8fe-135">После создания правила для почтовых ящиков Exchange вы можете [отключить или изменить правило](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , перейдя к \*\*\*\* > **правилам** обработки почтового ящика в центре администрирования Exchange, и отключить правило "*шифровать исходящие сообщения электронной почты от"* . ".</span><span class="sxs-lookup"><span data-stu-id="fe8fe-135">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
