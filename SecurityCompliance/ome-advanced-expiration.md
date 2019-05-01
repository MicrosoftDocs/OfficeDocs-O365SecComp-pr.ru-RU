---
title: Установка срока действия электронной почты, зашифрованного с помощью расширенного шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Благодаря расширенным функциям шифрования сообщений Office 365 в начале шифрования сообщений Office 365 (OME) вы можете расширить безопасность электронной почты, установив срок действия электронной почты через настраиваемый шаблон фирменного стиля.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506734"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="7896c-103">Установка срока действия электронной почты, зашифрованного с помощью расширенного шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="7896c-103">Set an expiration date for email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="7896c-104">Расширенное шифрование сообщений Office 365 в определенных подписках доступно на основе шифрования сообщений Office 365.</span><span class="sxs-lookup"><span data-stu-id="7896c-104">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="7896c-105">Расширенное шифрование сообщений включено в [Microsoft 365 корпоративный](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise и Office 365 образования A5.</span><span class="sxs-lookup"><span data-stu-id="7896c-105">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="7896c-106">Если в вашей организации есть подписка на Office 365, которая не включает расширенное шифрование сообщений Office 365, вы можете приобрести дополнительное шифрование сообщений в качестве надстройки с соответствием требованиям к расширенному набору для обеспечения соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="7896c-106">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="7896c-107">Истечение срока действия сообщений можно использовать в сообщениях, отправляемых пользователями внешним получателям, которые используют портал OME для доступа к зашифрованным сообщениям электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7896c-107">You can use message expiration on emails that your users send to external recipients who use the OME Portal to access encrypted emails.</span></span> <span data-ttu-id="7896c-108">Вы можете использовать портал OME для просмотра зашифрованных сообщений электронной почты, отправляемых вашей организацией, и ответа на них с помощью настраиваемого фирменного шаблона, который задает срок действия в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7896c-108">You force recipients to use the OME portal to view and reply to encrypted emails sent by your organization by using a custom branded template that specifies an expiration date in Windows Powershell.</span></span>

<span data-ttu-id="7896c-109">Как глобальный администратор Office 365 при применении фирменной символики компании для настройки внешнего вида ваших сообщений в организации Office 365 можно также указать срок действия этих сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7896c-109">As an O365 global administrator, when you apply your company branding to customize the look of your Office 365 organization's email messages, you can also specify an expiration for these email messages.</span></span> <span data-ttu-id="7896c-110">С помощью расширенного шифрования сообщений Office 365 вы можете создать несколько шаблонов для зашифрованных сообщений электронной почты, исходящих из вашей организации.</span><span class="sxs-lookup"><span data-stu-id="7896c-110">With Office 365 Advanced Message Encryption, you can create multiple templates for encrypted emails originating from your organization.</span></span> <span data-ttu-id="7896c-111">С помощью шаблона можно контролировать, как долго получатели имеют доступ к сообщениям, отправляемым пользователями.</span><span class="sxs-lookup"><span data-stu-id="7896c-111">Using a template, you can control how long recipients have access to mail sent by your users.</span></span>

<span data-ttu-id="7896c-112">Когда конечный пользователь получает почту с установленным сроком действия, пользователь видит дату окончания срока действия в сообщении-оболочке.</span><span class="sxs-lookup"><span data-stu-id="7896c-112">When an end user receives mail that has an expiration date set, the user sees the expiration date in the wrapper email.</span></span> <span data-ttu-id="7896c-113">Если пользователь пытается открыть просроченную почту, на портале OME появляется ошибка.</span><span class="sxs-lookup"><span data-stu-id="7896c-113">If a user tries to open an expired mail, an error appears in the OME portal.</span></span>

<span data-ttu-id="7896c-114">Истечет срок действия только сообщений, отсылаемых внешним получателям.</span><span class="sxs-lookup"><span data-stu-id="7896c-114">Only emails to external recipients are expirable.</span></span>

<span data-ttu-id="7896c-115">С помощью расширенного шифрования сообщений Office 365 каждый раз, когда вы применяете фирменную символику, Office 365 применяет программу-оболочку к электронной почте, удовлетворяющую правилу обработки почты, к которому применяется шаблон.</span><span class="sxs-lookup"><span data-stu-id="7896c-115">With Office 365 Advanced Message Encryption, any time you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="7896c-116">Кроме того, истечение срока действия можно использовать только в том случае, если используется настраиваемая фирменная символика.</span><span class="sxs-lookup"><span data-stu-id="7896c-116">In addition, expiration can only be used if custom branding is used.</span></span>

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a><span data-ttu-id="7896c-117">Создание настраиваемого шаблона фирменной символики для принудительного истечения срока действия почты с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="7896c-117">Create a custom branding template to force mail expiration by using PowerShell</span></span>

1. <span data-ttu-id="7896c-118">[Подключитесь к Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) , используя учетную запись с разрешениями глобального администратора в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="7896c-118">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="7896c-119">Запустите командлет New – OMEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7896c-119">Run the New-OMEConfiguration cmdlet.</span></span>

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

<span data-ttu-id="7896c-120">Где:</span><span class="sxs-lookup"><span data-stu-id="7896c-120">Where:</span></span>

- <span data-ttu-id="7896c-121">Identity — имя настраиваемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="7896c-121">Identity is the name of the custom template.</span></span>

- <span data-ttu-id="7896c-122">Екстерналмаилекспириндайс определяет количество дней, в течение которых получатели должны иметь возможность хранить почту до истечения срока их действия.</span><span class="sxs-lookup"><span data-stu-id="7896c-122">ExternalMailExpiryInDays identifies the number of days you want recipients to be able to keep mail before it expires.</span></span> <span data-ttu-id="7896c-123">Можно использовать любое значение от 1 до 730 дней.</span><span class="sxs-lookup"><span data-stu-id="7896c-123">You can use any value between 1 to 730 days.</span></span>

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="7896c-124">Дополнительные сведения о расширенном шифровании сообщений в Office 365</span><span class="sxs-lookup"><span data-stu-id="7896c-124">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="7896c-125">Расширенное шифрование сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="7896c-125">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="7896c-126">Отзыв сообщения, зашифрованного с помощью расширенного шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="7896c-126">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>](revoke-ome-encrypted-mail.md)

- [<span data-ttu-id="7896c-127">Описание политики сообщений и службы соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="7896c-127">Message policy and compliance service description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)