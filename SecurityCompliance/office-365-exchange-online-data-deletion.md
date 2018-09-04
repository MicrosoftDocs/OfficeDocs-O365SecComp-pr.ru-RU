---
title: Удаление Exchange Online данных Office 365
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
description: Как Мягкая и серьезный удалений данные обрабатываются в Exchange Online.
ms.openlocfilehash: 3a17b09e9c21ae309e00bcb0ddc0b51b93478bc1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534698"
---
# <a name="exchange-online-data-deletion-in-office-365"></a>Удаление Exchange Online данных в Office 365
В Exchange Online, существует два типа удалений: программных удалений и жестко удаления. Это относится к почтовым ящикам и элементы в почтовом ящике.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Удаленные и удаленных почтовых ящиков
Почтовый ящик пользователя удаленные является почтовый ящик, который был удален с помощью центра администрирования Office 365 или командлет Remove-Mailbox и по-прежнему был в корзине Azure Active Directory для менее 30 дней. Почтовый ящик может стать удаленные один из следующих способов:
- Почтовый ящик пользователя, связанного с Azure Active Directory, учетная запись пользователя является удаленные (объект пользователя — из области действия или в контейнере recycle bin).
- Учетная запись пользователя почтового ящика пользователя связанного Azure Active Directory был удален, но почтовый ящик Exchange Online — в разделе хранение для судебного разбирательства или хранение электронных данных.
- Связанный почтовый ящик пользователя Azure Active Directory, учетная запись пользователя был удален за последние 30 дней; Exchange Online его хранения Максимальная длина будет сохранена в почтовый ящик в состоянии удаленные перед его без возможности восстановления удаленных и восстановления.

Почтовый ящик пользователя удаленных является почтовый ящик, который был удален в одном из следующих способов:
- Почтовый ящик пользователя было удаленные более 30 дней и связанный пользователь Azure Active Directory был удалены. Все содержимое почтовых ящиков, такие как сообщения электронной почты, контакты и файлы удаляются без возможности восстановления.
- Учетная запись пользователя, связанный с почтовым ящиком пользователя было удален из Azure Active Directory. Почтовый ящик пользователя теперь удаленные в Exchange Online и остается в состоянии удаленные в течение 30 дней. Если в 30-дневный период нового пользователя Azure Active Directory синхронизируется с исходной учетной записи получателя с одной и той же **ExchangeGuid** или **ArchiveGuid**, лицензированный новой учетной записи для Exchange Online, в результате жестко удаления исходный почтовый ящик пользователя. Все содержимое почтовых ящиков, такие как сообщения электронной почты, контакты и файлы удаляются без возможности восстановления.
- Почтовый ящик удаленные удаляется с помощью **PermanentlyDelete Remove-Mailbox**.

Выше удаления сценариях предполагается, что почтовый ящик пользователя не в любом из состояния удержания, такой как хранение для судебного разбирательства или хранение электронных данных. При наличии любого типа удержание для почтового ящика, невозможно удалить почтовый ящик. Для всех типов получателей пользователя почты какие-либо параметры [хранения](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) игнорируются и не влияют на жестко удалений или обратимо удалений.

## <a name="soft-deleted-and-hard-deleted-items"></a>Удаленные и удаленных элементов
Когда пользователь удаляет элемент почтового ящика (например, сообщения электронной почты, контакт, встречу из календаря или задачи), перемещено в папку элементов для восстановления, а также в вложенной папке с именем удалений. Это называется программных удаления. Как долго удаленные элементы хранятся в удаленные элементы, папки, зависит от срока хранения удаленного элемента, который имеет значение для почтового ящика. Почтовый ящик Exchange Online поддерживает удаленных элементов в течение 14 дней по умолчанию, но Exchange Online администраторы могут изменить этот параметр, чтобы увеличить период вплоть до не более 30 дней. (Подробное описание действий для увеличить срок хранения удаленного элемента для почтового ящика Exchange Online см [Изменить длительность окончательного удаления элементов хранятся в течение почтовый ящик Exchange Online](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention).) Пользователей можно восстанавливать или очистить "Удаленные" до истечения срока действия время хранения удаленных элементов. Для этого они использовать функцию восстановить удаленные элементы в Microsoft Outlook или Outlook в Интернете.

Если пользователь удаляет удаленного элемента с помощью компонента восстановить удаленные элементы в Outlook или Outlook в Интернете, это называется жестко удаления. В Exchange Online функцию восстановления отдельных элементов включена по умолчанию при создании нового почтового ящика, назначены права администратора по-прежнему можно [восстановить](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages) -удаленные элементы, до истечения срока хранения удаленного элемента. Кроме того сообщение при изменении пользователем или процесс, копии исходного элемента также сохраняются при включении функцию восстановления отдельных элементов.

## <a name="page-zeroing"></a>Обнуление страниц
*Zeroing* — это механизм обеспечения безопасности, который записывает нулям или двоичные шаблон через удаленные данные таким образом, более сложны для восстановления удаленных данных. В Exchange Online базы данных почтовых ящиков использование *страниц* в качестве их блока хранилища и реализации перезаписи процедуры, вызов *функции обнуления страниц*. Обнуления страниц включается по умолчанию и не может быть отключен по клиентам или корпорацией Майкрософт. Операции обнуления страниц, записываются в файлы журнала транзакций, чтобы все копии этой базы данных являются страницы обнуленных аналогичным образом. Обнуление страниц на активной копии базы данных приводит к тому, страницы, чтобы получить обнуленных пассивной копии базы данных.

Обнуления страниц записывает двоичные шаблон через-удаленных записей. Шаблон обнуления страниц специально для расширенного обработчика хранилищ (ESE) операций (имя внутреннего СУБД используемого серверами в Exchange Online) и его нет в списке для выполнения операций и фоновых операций обслуживания базы данных. (Фонового обслуживания базы данных — это процесс, который постоянно контрольные суммы и сканирований каждой базы данных. Его основная функция — контрольной суммой страниц базы данных, но он также обрабатывает Очистка пространства и обнуления записей и страниц, которые не были обнуление из-за сбоя хранилища).

В следующей таблице перечислены шаблоны заполнения, соответствующие определенным операциям среды выполнения.

| Операция среды выполнения ESE   | Шаблон заполнения |
|--------------------------|--------------|
| Заменить                  | R            |
| Удалить запись или длинное значение | D            |
| Освобожденное место страницы         | H            |


В следующей таблице перечислены шаблоны заполнения, соответствующие определенным операциям, выполняемым во время фонового обслуживания базы данных ESE.

| Операция фонового обслуживания базы данных ESE | Шаблон заполнения |
|-----------------------------------------------|--------------|
| Удалить запись                                 | D            |
| Удалить длинное значение                             | L            |
| Освобожденное место частично используемой страницы       | Z            |
| Освобожденное место неиспользуемой страницы               | U            |


### <a name="page-zeroing-process"></a>Процесс обнуления страниц
Процесс обнуления страниц зависит от сценария удаления. В следующей таблице описаны сценарии удаления базы данных, и при возникновении функций обнуления страниц.

| Сценарий удаления базы данных | Процесс ESE и временные рамки обнуления данных в базе данных |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Срок действия элемента основанным на срок хранения удаленного элемента. | В асинхронном потоке двоичный шаблон записывается поверх удаленных данных. Это действие выполняется за те миллисекунды, в течение которых происходит удаление записи. Если процесс хранилища завершается сбоем во время ожидания выполнения асинхронного обнуления (или очистка хранилища версий отменяется из-за его роста), обнуление завершается при обработке этого раздела базы данных во время фонового обслуживания базы данных. |
| Сценарий представления: Удаление элементов из Outlook и Outlook на представление веб-папки (например, представление беседы) | Обнуление данных выполняется при обработке этого раздела базы данных во время фонового обслуживания базы данных. |
| Перемещение почтовых ящиков, удаление почтового ящика сценарий: Исходного почтового ящика удален (срок действия удаленного почтового ящика) | Обнуление данных выполняется при обработке этого раздела базы данных во время фонового обслуживания базы данных. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Типы данных почтового ящика без обнуления страниц
Следующие типы данных почтового ящика не предусматривают обнуления страниц:
- **Журналы транзакций базы данных почтовых ящиков** - при удалении журналов транзакций как часть обычной работе нет процесс не нуль блоки в файловой системе, хранятся файлы журнала удаленного. Вероятнее всего, что в файловой системе будет быстро повторно использовать свободное место для только что созданный журналы, но не гарантируется, что это происходит.
- **Файлы каталога индексов содержимого** - Exchange Online использует Search Foundation (также известной как FAST) для индексирования функциональные возможности поиска. Каталог индексов поиска включает в себя несколько десятков файлов, хранящихся на том же как файл базы данных почтовых ящиков. Если сообщение удалены из базы данных почтовых ящиков, связанного контента в каталог поиска не будет удалено сразу же. Удаление содержимого возникает при Search Foundation тени (или объединения с главной копией) множество небольших каталога файлов в один файл размером. После завершения объединения с главной копией файлов меньшего размера каталога, удаляются. Нет процесс не нуль блоки, в которых хранятся файлы удаленного каталога.

## <a name="continuous-replication"></a>Непрерывная репликация
Непрерывная репликация (также известной как доставки журналов и преобразования) — это технология в Exchange Online, который создает и поддерживает копии каждой базы данных почтовых ящиков для обеспечения высокой доступности, устойчивости сайтов и аварийного восстановления. Непрерывная репликация использует поддержка восстановления после сбоя базы данных Exchange Server для предоставления технология, которая выполняет асинхронный обновление одной или нескольких копий базы данных почтовых ящиков. Каждый сервер почтовых ящиков записывает обновления базы данных, созданных в активной базы данных (например, действие электронной почты пользователя) как записи журнала в последовательный набор файлов журнала транзакций 1 МБ. Этот набор файлов, называется потока журнала. В непрерывной репликации потока журнала также используется для асинхронного обновления одного или нескольких копий базы данных. Это осуществляется путем передачи журналов в папку, содержащую пассивной копии активной базы данных и воспроизведения их в пассивная копия базы данных. Если все журналы из активной базы данных будут преобразованы пассивной копии базы данных, затем эквивалентны две базы данных, а именно этот процесс репликации, что физические изменения, сделанные в активной базы данных на все пассивной копии базы данных.

Любые удаления из базы данных почтовых ящиков, ли элемент почтового ящика или ко всему почтовому ящику и как обратимо delete, так и жестко delete, представляет физических изменение активной базы данных. Также обнуления страниц влечет за собой изменения физической активной базы данных. Эти изменения записывается в файлы журнала в процессе, называется непрерывной репликации и при этих файлов журнала будут преобразованы пассивной копии базы данных, на эти пассивных баз данных выполняются те же физические изменения.