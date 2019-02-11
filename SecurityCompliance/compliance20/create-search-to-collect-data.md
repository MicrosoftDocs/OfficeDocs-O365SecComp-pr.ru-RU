---
title: Создание поискового запроса для сбора данных
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
ms.openlocfilehash: 773137cbfc73d449766e04bf7eccc77f8bdd0cca
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706140"
---
# <a name="create-a-search-to-collect-data"></a>Создание поискового запроса для сбора данных

На вкладке **Поиск** в случае можно создать новый поиск, нажав кнопку **Создать поиска** и выполнив мастера.

## <a name="name-your-search-and-give-description"></a>Имя операции поиска и предоставить описание

Каждый поиска с дела должны иметь уникальные имена. Можно ввести описание для поиска. 

## <a name="define-your-conditions"></a>Определение условия

Можно определить условия поиска с использованием карт готовые условие или с помощью ключевого слова Query Language (KQL). Для получения дополнительных сведений см [построения поисковых запросов](building-search-queries.md).

## <a name="choose-the-custodians-to-search-from"></a>Выберите custodians выполнять поиск по

После определения всех условий, необходимо выбрать местоположения, в которых требуется выполнить поиск. — Это один из способов сделать это путем указания каких custodians уже добавлен в рамках данного экземпляра, который нужно найти. Можно, выбрав пункт custodian поиска будет выполняться все источники данных, сопоставленные с custodian. [Работа с custodians](managing-custodians.md) более подробные сведения о том, как добавить custodians в случай и управлять их источники данных.

## <a name="choose-non-custodial-locations"></a>Выберите не наказание расположения

В некоторых случаях вы можете выполнять поиск источников данных, которые не связан с custodian. В этом случае можно указать место, нужно выполнить поиск, или выберите Поиск все расположения контента для определенной службы Office 365 (например поиск всех почтовых ящиков Exchange или все SharePoint и OneDrive для бизнеса сайтов).