---
title: Политика шифрования сообщений Office 365 для конфиденциальной информации
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Сводка. Политика шифрования сообщений Office 365 для типов конфиденциальной информации теперь доступны.
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213984"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="fe349-103">Политика шифрования сообщений Office 365 для конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="fe349-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="fe349-p101">Update (1/30/19): в октябре 2018 мы работали с небольшим примером клиентов, чтобы узнать, можно ли упростить защиту, автоматически шифруя конфиденциальные сообщения электронной почты, основанные на определенных типах конфиденциальной информации. На основе положительной обратной связи из этого примера мы решили расширить профиль клиентов на более разнообразную версию в декабре 2018 декабря. После того, как вы выберете сведения о клиентах, мы прослушали ваш отзыв и определили, что клиенты с более сложными средами хотели бы реализовать эти правила с осторожностью, и поэтому мы намерены настроить наши планы.</span><span class="sxs-lookup"><span data-stu-id="fe349-p101">Update (1/30/19): In October 2018, we worked with a small sample of customers to understand if we can simplify protection by automatically encrypting sensitive emails based on certain sensitive information types. Based on positive feedback from this sample, we decided to expand to a more diverse profile of tenants in December 2018. After communicating the next roll-out to select tenants, we listened to your feedback and determined that customers with more complex environments wanted to implement the rules more cautiously, and we are therefore adjusting our plans.</span></span>

<span data-ttu-id="fe349-p102">Если ваша организация была выбрана для выпуска с 15 января 2019, то автоматическая политика не выполняется. Вместо этого мы предоставляем инструкции, приведенные в этой статье, о том, как можно выполнить развертывание йоурселвес. Продолжайте чтение, чтобы узнать, как.</span><span class="sxs-lookup"><span data-stu-id="fe349-p102">If your organization was selected for the roll-out starting January 15, 2019, we will not roll out the automatic policy. Instead, we are providing instructions in this article on how you can complete the roll-out yourselves. Keep reading to find out how.</span></span>

||
|:-----|
|<span data-ttu-id="fe349-p103">Эта статья входит в набор статей, посвященных шифрованию сообщений Office 365. Эта статья предназначена для администраторов и Итпрос. Если вы просто ищете сведения о том, как отправлять или получать зашифрованные сообщения, ознакомьтесь со статьей, посвященной [шифрованИю сообщений Office 365 (OME)](ome.md) , и выберите статью, которая наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="fe349-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a><span data-ttu-id="fe349-113">Создание политики типов конфиденциальной информации для клиента</span><span class="sxs-lookup"><span data-stu-id="fe349-113">How to create the sensitive information type policy for your tenant</span></span>

<span data-ttu-id="fe349-p104">Для создания политики типов конфиденциальной информации можно использовать правила для обработки почты Exchange или предотвращение потери данных (DLP) Office 365. Чтобы создать правило для процесса обработки почты Exchange, вы можете использовать центр администрирования Exchange или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe349-p104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create the sensitive information type policy. To create an Exchange mail flow rule you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="fe349-116">Создание политики с помощью правил для почтового процесса в центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="fe349-116">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="fe349-p105">Войдите в центр администрирования Exchange и перейдите к разделу > **правила**для поток обработки **почты**. В этом случае создайте правило, которое применяет шифрование сообщений Office 365 на основе таких условий, как присутствие определенных ключевых слов или типов конфиденциальной информации в сообщении или вложении.</span><span class="sxs-lookup"><span data-stu-id="fe349-p105">Sign-in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**. There, create a rule that applies Office 365 Message Encryption based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="fe349-119">Создание политики с помощью правил для почтового процесса в PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe349-119">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="fe349-p106">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell). Используйте командлеты Set – IRMConfiguration и New – Транспорруле для создания политики.</span><span class="sxs-lookup"><span data-stu-id="fe349-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Use the Set-IRMConfiguration and New-TransporRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="fe349-123">Пример правила для процесса обработки почты, созданного с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe349-123">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="fe349-124">Выполнение следующих команд в PowerShell создание правила для обработки почты Exchange, которое автоматически шифрует сообщения, находящихся за пресроком Организации, с помощью политики *только для шифрования* , если сообщения электронной почты или их вложения содержат следующие конфиденциальные данные типы сведений:</span><span class="sxs-lookup"><span data-stu-id="fe349-124">Running the following commands in PowerShell create an Exchange mail flow rule that automatically encrypts emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="fe349-125">Номер маршрутизации код банка ABA</span><span class="sxs-lookup"><span data-stu-id="fe349-125">ABA routing number</span></span>
- <span data-ttu-id="fe349-126">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="fe349-126">Credit card Number</span></span>
- <span data-ttu-id="fe349-127">Номер агентства для применения наркотиков (DEA)</span><span class="sxs-lookup"><span data-stu-id="fe349-127">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="fe349-p107">Номер паспорта для США и Великобритании</span><span class="sxs-lookup"><span data-stu-id="fe349-p107">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="fe349-130">Номер банковского счета США</span><span class="sxs-lookup"><span data-stu-id="fe349-130">U.S. bank account number</span></span>
- <span data-ttu-id="fe349-131">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="fe349-131">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="fe349-132">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="fe349-132">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="fe349-133">Как получатели обращаются к вложениям</span><span class="sxs-lookup"><span data-stu-id="fe349-133">How recipients access attachments</span></span>

<span data-ttu-id="fe349-134">После шифрования сообщения у получателей будет неограниченный доступ к вложениям после того, как они обращаются к ним и открывают зашифрованную электронную почту.</span><span class="sxs-lookup"><span data-stu-id="fe349-134">Once a message is encrypted, recipients will have unrestricted access to attachments once they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="fe349-135">Подготовка к выполнению этого изменения</span><span class="sxs-lookup"><span data-stu-id="fe349-135">To prepare for this change</span></span>

<span data-ttu-id="fe349-p108">Вам может потребоваться обновить любую документацию конечного пользователя и обучающие материалы, чтобы подготовить пользователей в Организации к этому изменению. Предоставьте им доступ к этим ресурсам по шифрованию сообщений Office 365, используя соответствующие пользователи:</span><span class="sxs-lookup"><span data-stu-id="fe349-p108">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="fe349-138">Отправка, просмотр зашифрованных сообщений и ответ на них в Outlook для компьютера</span><span class="sxs-lookup"><span data-stu-id="fe349-138">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="fe349-139">Видео Office 365 Essentials: шифрование сообщений Office</span><span class="sxs-lookup"><span data-stu-id="fe349-139">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="fe349-140">Просмотр изменений в журнале аудита</span><span class="sxs-lookup"><span data-stu-id="fe349-140">View these changes in the Audit log</span></span>

<span data-ttu-id="fe349-p109">Это действие подлежит аудиту и доступно администраторам Office 365. Операция — "New-TransportRule", а фрагмент примера записи аудита из поиска в журнале аудита в центре безопасности _Амп_ соответствия требованиям ниже:</span><span class="sxs-lookup"><span data-stu-id="fe349-p109">This activity is audited and is available to Office 365 administrators. The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="fe349-143">*{"CreationTime": "2018 г. – 11 — 28T23:35:01", "ID": "a1b2c3d4-daa0-4c4f-A019-03a1234a1b0c", "Operation": "New/TransportRule", "Организатионид": "123456 – 221d – 12345", "RecordType": "ResultStatus", "", "UserKey": "оператор Майкрософт", " UserType ": 3," Version ": 1," Рабочая нагрузка ":" Exchange "," Клиентип ":" 123.456.147.68:17584 "," ObjectId ":", "UserId": "Microsoft оператор", "Екстерналакцесс":Труе, "Организатионнаме":"contoso. onmicrosoft. com", "OriginatingServer": "CY4PR13MBXXXX ( 15.20.1382.008) "," Parameters ": {" имя ":" Организация "," значение ":" 123456-221d-12346 "{" Name ":" Апплиригхтспротектионтемплате "," value ":" Encrypting "}, {" Name ":" Name "," value ":" заШифровать исходящие сообщения электронной почты (")"}, {"Name": " MessageContainsDataClassifications "... документов.*</span><span class="sxs-lookup"><span data-stu-id="fe349-143">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span> |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="fe349-144">Отключение или Настройка политики типов конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="fe349-144">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="fe349-145">После создания правила для почтовых ящиков Exchange вы можете [отключить или изменить правило](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , перейдя к \*\*\*\* > **правилам** обработки почтового ящика в центре администрирования Exchange, и отключить правило "*шифровать исходящие сообщения электронной почты от"* . ".</span><span class="sxs-lookup"><span data-stu-id="fe349-145">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
