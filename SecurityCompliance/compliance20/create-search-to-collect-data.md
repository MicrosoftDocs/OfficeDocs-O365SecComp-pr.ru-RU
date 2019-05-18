---
title: Создание поискового запроса для сбора данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 360ba6a67d43a0b78b1104ae64885697009bb222
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155111"
---
# <a name="create-a-search-to-collect-data"></a>Создание поискового запроса для сбора данных

На вкладке **поиски** можно создать новый поиск, нажав кнопку **Новый поиск** и следуя инструкциям мастера.

## <a name="name-your-search-and-give-description"></a>Назвать Поиск и присвоить описание

Каждый Поиск с обращением должен иметь уникальное имя. При необходимости можно ввести описание поиска. 

## <a name="define-your-conditions"></a>Определение условий

Вы можете определить условия поиска с помощью встроенных карточек условий или с помощью языка запросов по ключевым словам (KQL). Более подробную информацию можно узнать в статье [Создание поисковых запросов](building-search-queries.md).

## <a name="choose-the-custodians-to-search-from"></a>Выбор custodians для поиска

Определив условия, необходимо выбрать расположения, в которых будет выполняться поиск. Один из способов сделать это — указать, какие custodians вы уже добавили в тот случай, когда вы хотите выполнить поиск. Выбрав хранитель, вы будете выполнять поиск по всем источникам данных, сопоставленным с хранитель. Для получения дополнительных сведений о том, как добавить custodians к своему случаю и управлять их источниками данных, ознакомьтесь со статьей [Working with custodians](managing-custodians.md) .

## <a name="choose-non-custodial-locations"></a>Выбор расположений, не являющихся кустодиалми

В некоторых случаях может потребоваться поиск в источниках данных, которые не сопоставлены с хранитель. В этом случае можно указать расположения, в которых требуется выполнить поиск, или выбрать поиск по всем расположениям для определенной службы Office 365 (например, поиск по всем почтовым ящикам Exchange или всем сайтам SharePoint и OneDrive для бизнеса).