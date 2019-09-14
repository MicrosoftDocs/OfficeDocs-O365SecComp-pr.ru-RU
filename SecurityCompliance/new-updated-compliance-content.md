---
title: Новые возможности центра соответствия требованиям Microsoft 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Как и функции в центре соответствия требованиям Microsoft 365, контент справки всегда развивается. Мы постоянно создаем новые статьи, обновляя существующие и внося изменения в соответствии с вашими отзывами. Узнайте о новых возможностях, которые были обновлены в этом месяце.
ms.openlocfilehash: e7600c2f84d0b591c6114c2a61c77d8e2c664056
ms.sourcegitcommit: 9fd606e8d912f4507fbcd9f1fcb9dfcfd20de08b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2019
ms.locfileid: "36980805"
---
# <a name="recent-updates-to-microsoft-365-compliance-content"></a>Последние обновления содержимого соответствия требованиям Microsoft 365

Как и функции в центре соответствия требованиям Microsoft 365, контент справки всегда развивается. Мы постоянно создаем новые статьи, обновляя существующие и внося изменения в соответствии с вашими отзывами. Посмотрите ниже, чтобы узнать о новых и обновленных статьях в этом месяце.

> [!TIP]
> Чтобы оставаться в курсе последних обновлений функций в центре соответствия требованиям Microsoft 365, ознакомьтесь со статьей [новые возможности в центре соответствия требованиям microsoft 365](whats-new.md).

## <a name="august-2019"></a>Август 2019

### <a name="auditing"></a>Аудит

[Управление аудитом почтовых ящиков](enable-mailbox-auditing.md#more-information) обновленный<br>Добавлены сведения о том, как события журнала аудита почтовых ящиков доступны только для пользователей с лицензиями или почтовыми ящиками, для которых администратор вручную включил аудит. Кроме того, новые рекомендации по использованию командлета **Search-маилбоксаудитлог** в Exchange Online PowerShell для поиска пользователей, не имеющих лицензий, в журнале аудита почтовых ящиков.

[Поиск в журнале аудита Office 365 для устранения распространенных сценариев](auditing-troubleshooting-scenarios.md#investigate-why-there-was-a-successful-login-by-a-user-outside-your-organization) обновленный<br>Новый раздел об использовании сквозной проверки подлинности для проверки успешных попыток входа внешними пользователями.

### <a name="content-search--ediscovery"></a>Поиск контента & обнаружения электронных данных

[Настройка фильтрации разрешений для поиска контента](permissions-filtering-for-content-search.md#using-a-filters-list-to-combine-filter-types) обновленный<br>Добавлены сведения об использовании списка фильтров, который позволяет добавить фильтры почтового ящика и сайта в один фильтр разрешений поиска.

[Поиск контента в Office 365](content-search.md#searching-disconnected-or-de-licensed-mailboxes) обновленный<br>Добавлены сведения о поиске отключенных или нелицензированных почтовых ящиков.

[Поиск контента в Office 365](content-search.md#searching-for-content-in-a-sharepoint-multi-geo-environment) обновленный<br>
[Настройка границ соответствия для исследований обнаружения электронных данных в Office 365](set-up-compliance-boundaries.md#searching-and-exporting-content-in-multi-geo-environments) обновленный<br>Добавлены сведения о поиске контента в средах с поддержкой нескольких регионов SharePoint.

### <a name="data-governance"></a>Управление данными

[Общие сведения о неограниченном архивировании в Office 365](unlimited-archiving.md#how-auto-expanding-archiving-works) обновленный<br>Добавлены сведения о том, как в Office 365 добавляется не более 20 дополнительных архивов, что всего составляет 1 ТБ дополнительного хранилища.

### <a name="data-investigations"></a>Расследования данных

[Удаление элементов из исходного расположения](datainvestigations/delete-items-from-original-locations.md) впервые<br>Теперь вы можете выбрать элементы в наборе свидетельств и программно удалить их из исходных расположений в Exchange, SharePoint и OneDrive.

[Управление инцидентом переноса данных в Microsoft 365](datainvestigations/manage-data-spillage-incidents.md#step-4-delete-the-spilled-data) обновленный<br>Добавлены сведения о том, как использовать новые функции "удаление элементов из исходного расположения" для удаления перенесенных данных.

### <a name="permissions"></a>Разрешения

[Разрешения в центре соответствия требованиям microsoft 365 и центре безопасности microsoft 365](permissions-microsoft-365-compliance-security.md) впервые<br>Новые группы ролей Azure Active Directory были выпущены для общедоступной предварительной версии.

### <a name="records-management"></a>Управление записями

[Обзор диспетчера плана файлов (Обновлено)](file-plan-manager.md#export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews)<br>Добавлена таблица со списком допустимых значений, которые будут использоваться в шаблоне Excel.

### <a name="supervision"></a>Контроля

[Политики контроля в Office 365](supervision-policies.md) обновленный<br>Разъяснена поддержка групп и списков рассылки Office 365, добавлены рекомендации по совпадению с ключевыми словами в сообщениях электронной почты и вложениях, а разъяснение поддержки Outlook в каналах Teams.

### <a name="windows-information-protection"></a>Windows Information Protection

[Список приложений Microsoft енлигхтенед для использования с Windows Information Protection (WIP)](https://docs.microsoft.com/windows/security/information-protection/windows-information-protection/enlightened-microsoft-apps-and-wip) обновленный <br>Microsoft 3D Viewer теперь является приложением енлигхтенед.
