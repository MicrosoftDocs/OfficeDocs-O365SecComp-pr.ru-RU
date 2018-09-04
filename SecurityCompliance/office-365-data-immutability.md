---
title: Office 365 неизменности данных
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Определяет и объясняются неизменности данных, либо данные, должно быть включено обнаружение и не может быть удален или изменен.
ms.openlocfilehash: 3a9e897734c1805e25a2e2dd5e0c5f8a3e3de3fd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535121"
---
# <a name="immutability-in-office-365"></a>Неизменность данных в Office 365
Для некоторых организаций, обеспечение соответствия законодательным нормам, требования внутреннего управления или риск судебного требующих сохранения электронной почты и связанных данных в форме, поддерживающего обнаружение. Все данные в системе должно быть включено обнаружение и ни один из его могут быть потеряны или изменены. Стандартный терминов для этого является «неизменяемости». 

Обеспечение неизменности традиционные методы обычно во время работы путем перемещения сообщений электронной почты в хранилище отдельные, только для чтения. Во время такой системы обслуживать цель сохранение элементов почтовых ящиков для обнаружения, они часто влияют на взаимодействие с пользователем значительные способами путем удаления сохраняются элементы из традиционные ежедневный рабочий процесс. Для ИТ-специалистов данный подход к неизменяемость данных требуется развертывания и проведения текущего обслуживания отдельную инфраструктуру server и хранилище. Обнаружение самого выполняется с внешними по отношению к почтовой системы, с помощью связанных развертывания и затраты на обслуживание средств.

Через конфигурация хранения на месте и компоненты политики хранения архивации в Office 365 и совместно со службами в пакет Office 365, как Exchange Online, SharePoint Online, OneDrive для бизнеса и Скайп для бизнеса, Архивация в Office 365 можно сохранить и сохранить множество классов, включая входящие, внутренний и исходящие данные:
- Communications входящей и исходящей электронной почты
- Книги и записи, содержащиеся в форме по электронной почте или в общей электронных документов
- Приглашения на собрания
- Факсы
- Мгновенные сообщения
- Документы, общий доступ во время собрания по сети
- Сообщений голосовой почты

Кроме того Корпорация Майкрософт разработала дополнительных функций, чтобы разрешить [Архивация данных](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) из других источников, благодаря интеграции с сбор данных сторонних производителей и решений для управления. После импорта данных сторонних производителей функции контроля соответствия требованиям Office 365 можно применить к данным, включая хранение для судебного разбирательства, электронного обнаружения на месте и удержания, поиска соответствия требованиям, архивации на месте, аудит и политики хранения. Например когда почтовый ящик располагается на хранение для судебного разбирательства, сторонних производителей данные будут сохранены. Можно выполнить поиск данных сторонних производителей с помощью электронного обнаружения на месте или поиска соответствия. Или можно применить архивации и политики хранения к данным сторонних производителей так же, как и для данных Майкрософт. Одним словом архивирование данных в Office 365 в сторонних производителей могут помочь организации всегда оставаться на соответствующий стандарту государственных организаций и нормативных политик.

Архивация в Office 365 предоставляет 17a-4-совместимые хранилища правило комиссии по бирже по ценным бумагам and (сек) и сохраняет постоянные файлы все данные, собранные в виде без перезаписи, только с помощью политик хранения на месте и политики хранения , включая сохранение блокировки. А именно:
- Все записи, которые хранятся с помощью политик хранения, указанной выше, сохраняются в сфере выделенного хранилища из созданного обычного пользователя. Кроме того только авторизованным пользователям доступа и поиск эти записи, но нельзя изменить или удаляют их.
- Метаданные для каждого элемента включает в себя метка времени, используемый в расчет продолжительность хранения. Отметки времени, применяются при получении нового элемента или создан и не может быть впоследствии изменить или удалить из метаданных.
- Архивация в Office 365 позволяет пользователям для объединения политики хранения различных и удержания для создания политики фрагментарное хранения для определения типа или расположения элементов неизменно сохраняется и длительности таких хранения.
- Сохранение блокировки позволяет пользователям выбирать, следует ли сделать политики ограничения политики. Ограничительная политика запрещает всем пользователям возможность удаления, отключения или внести изменения в политику хранения. Это означает, что после блокировки сохранение включен, не может быть отключен, а также механизм не определен в разделе какие данные из существующего custodians, полученную хранения политик на месте, могут быть перезаписаны, изменения, удаления или удаляется во время период хранения. Более того указанная с хранением блокировки удержания нельзя сокращение или уменьшить. Тем не менее, возможно, в тексте, в случае юридические требования для продолжения хранения сохраненных данных, как указано выше. Сохранение блокировки гарантирует, что никто, даже администраторы или с определенной управления доступом может изменить параметры или перезаписи или удалить данные, которые были сохранены, перенос архивации в Office 365 вместе с рекомендациями, изложенными в выпуске 2003 с Правило 17a-4.

Пользователям лучше понять, как Office 365 можно выполнять в соответствии с их нормативные обязательства, особенно при использовании правила 17a-4 требования, выпущен [Технический документ](https://go.microsoft.com/fwlink/?linkid=830440) , который охватывает архивации Exchange Online, SharePoint Online, OneDrive для бизнеса и Скайп для бизнеса. Технический документ, посвященный также предоставляет глубокий анализ Office 365 архивации функциях и возможностях для каждой требованиям правило SEC 17a-4 и демонстрируется регулируемого клиентам, как Office 365 архивации можно включить их в соответствии с их требования к.