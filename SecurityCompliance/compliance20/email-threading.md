---
title: Потоки почты
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d4328971a6b13c60c4d8b9f5b6db310d72a5b215
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706000"
---
# <a name="email-threading"></a><span data-ttu-id="5cd8f-102">Потоки почты</span><span class="sxs-lookup"><span data-stu-id="5cd8f-102">Email threading</span></span>

<span data-ttu-id="5cd8f-p101">Рассмотрите возможность в беседе электронной почты, которая существовала некоторое время. В большинстве случаев последнее сообщение электронной почты в потоке будет включать содержимое всех выше по электронной почте; Просмотр последнего электронной почты предоставит полный контекст беседы, произошло в потоке. Threading электронной почты определяет такие по электронной почте, поэтому рецензентов можно просмотреть часть собирать документы без потери любого контекста.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-p101">Consider an email conversation that has been going on for a while. In most cases, the last email on the thread will include the contents of all the preceding emails; reviewing the last email will give a complete context of the conversation that happened in the thread. Email threading identifies such emails so that reviewers can review a fraction of collected documents without losing any context.</span></span>

## <a name="what-does-email-threading-do"></a><span data-ttu-id="5cd8f-106">Что такое threading электронной почты?</span><span class="sxs-lookup"><span data-stu-id="5cd8f-106">What does email threading do?</span></span>

<span data-ttu-id="5cd8f-p102">Threading электронной почты анализирует каждого электронной почты и desconstructs его для отдельных сообщений. Каждое сообщение электронной почты — это цепочка отдельных сообщений. Затем анализирует все сообщения электронной почты в рабочее множество для определения ли сообщение электронной почты содержит уникальный содержимое или если цепочке полностью содержащихся в разных электронной почты. В итоге по электронной почте делятся на четыре категории:</span><span class="sxs-lookup"><span data-stu-id="5cd8f-p102">Email threading parses each email and desconstructs it to individual messages; each email is a chain of individual messages. Then, it analyzes all emails in the working set to determine whether an email has unique content or if the chain is wholly contained in a different email. In the end emails are divided into four categories:</span></span>

- <span data-ttu-id="5cd8f-110">**Включающий**: последнего сообщения в сообщение электронной почты имеет уникальный контент, а сообщение электронной почты все вложения, которые были включены в другие которых содержимое полностью содержащихся в это сообщение по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-110">**Inclusive**: the last message in the email has unique content, and the email has all of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>


- <span data-ttu-id="5cd8f-111">**Включающий минус**: последнего сообщения в сообщение электронной почты содержит уникальный содержимое, но сообщение электронной почты не содержит некоторые вложения, которые были включены в другие которых содержимое полностью содержащихся в это сообщение по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-111">**Inclusive minus**: the last message in the email has unique content, but the email does not contain some of the attachments that were included in other emails of which the content is wholly contained in this email.</span></span>

- <span data-ttu-id="5cd8f-112">**Включительно копии**: точную копию включительно/включительно минус электронной почты</span><span class="sxs-lookup"><span data-stu-id="5cd8f-112">**Inclusive copy**: an exact copy of an inclusive/inclusive minus email</span></span>

- <span data-ttu-id="5cd8f-113">**None**: контент это сообщение полностью содержащихся в по крайней мере один электронной почты, помеченные как "минус" включительно/включительно.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-113">**None**: The content of this email is wholly contained in at least one email that is marked as inclusive/inclusive minus.</span></span>

## <a name="how-is-it-different-from-conversations-in-outlook"></a><span data-ttu-id="5cd8f-114">Как это отличается от бесед в Outlook?</span><span class="sxs-lookup"><span data-stu-id="5cd8f-114">How is it different from conversations in Outlook?</span></span>
<span data-ttu-id="5cd8f-p103">С первого взгляда звучит очень похоже на группирование беседы в программе Outlook. Однако есть некоторые важные различия. Необходимо учитывать в беседе электронной почты, который получил разделенными на две беседы; Например кто-то ответил сообщения электронной почты, который не является узнать последние новости в окне беседы, поэтому последние два сообщения электронной почты в окне беседы имеют уникальные материалы.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-p103">At a glance, this sounds very similar to conversation groupings in Outlook. However, there are some important distinctions. Consider an email conversation that got forked into two conversation; for instance, someone responded to an email that is not the latest in the conversation so the last two emails in the conversation both have unique content.</span></span>

<span data-ttu-id="5cd8f-p104">Outlook будет по-прежнему групповой сообщения электронной почты в одной беседы; чтение только последнее сообщение электронной почты будет означать отсутствует контекст электронной почты с последним секунды, который также содержит уникальный содержимого. Так как потоков электронной почты разбор каждое сообщение электронной почты в отдельных компонентов и сравнивает их, threading электронной почты пометить как последние два сообщения электронной почты как inclusives, проверка того, что не пропустить любого контекста до тех пор, пока читать все сообщения электронной почты помечено как включительно.</span><span class="sxs-lookup"><span data-stu-id="5cd8f-p104">Outlook would still group the emails into a single conversation; reading only the last email would mean missing the context of the second-to-last email, which also contains unique content. Because email threading parses out each email into individual components and compares them, email threading would mark both of the last two emails as inclusives, ensuring that you won't miss any context as long as you read all emails marked as inclusive.</span></span>