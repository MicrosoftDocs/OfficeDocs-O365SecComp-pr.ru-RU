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
ms.openlocfilehash: 2340128f508a3be389afce86596f7e6395a0bb7e
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608265"
---
# <a name="email-threading"></a>Потоки почты
Рассмотрите возможность в беседе электронной почты, которая существовала некоторое время. В большинстве случаев последнее сообщение электронной почты в потоке будет включать содержимое всех выше по электронной почте; Просмотр последнего электронной почты предоставит полный контекст беседы, произошло в потоке. Threading электронной почты определяет такие по электронной почте, поэтому рецензентов можно просмотреть часть собирать документы без потери любого контекста.

## <a name="what-does-email-threading-do"></a>Что такое threading электронной почты?
Threading электронной почты анализирует каждого электронной почты и desconstructs его для отдельных сообщений. Каждое сообщение электронной почты — это цепочка отдельных сообщений. Затем анализирует все сообщения электронной почты в рабочее множество для определения ли сообщение электронной почты содержит уникальный содержимое или если цепочке полностью содержащихся в разных электронной почты. В итоге по электронной почте делятся на четыре категории:
- Inclusives: последнего сообщения в сообщение электронной почты содержит уникальный содержимое и сообщение электронной почты содержит все вложения, которые были включены в другие которых содержимое полностью содержащихся в это сообщение по электронной почте.
- Включительно минус: последнего сообщения в сообщение электронной почты содержит уникальный содержимое, но сообщение электронной почты не содержит некоторые вложения, которые были включены в другие которых содержимое полностью содержащихся в это сообщение по электронной почте.
- Включительно копии: точную копию включительно/включительно минус электронной почты
- NONE: В этом сообщений электронной почты полностью в содержимое по крайней мере один электронной почты, помеченные как "минус" включительно/включительно.

## <a name="how-is-it-different-from-conversations-in-outlook"></a>Как это отличается от бесед в Outlook?
С первого взгляда звучит очень похоже на группирование беседы в программе Outlook. Однако есть некоторые важные различия. Необходимо учитывать в беседе электронной почты, который получил разделенными на две беседы; Например кто-то ответил сообщения электронной почты, который не является узнать последние новости в окне беседы, поэтому последние два сообщения электронной почты в окне беседы имеют уникальные материалы.

Outlook будет по-прежнему групповой сообщения электронной почты в одной беседы; чтение только последнее сообщение электронной почты будет означать отсутствует контекст электронной почты с последним секунды, который также содержит уникальный содержимого. Так как потоков электронной почты разбор каждое сообщение электронной почты в отдельных компонентов и сравнивает их, threading электронной почты пометить как последние два сообщения электронной почты как inclusives, проверка того, что не пропустить любого контекста до тех пор, пока читать все сообщения электронной почты помечено как включительно.