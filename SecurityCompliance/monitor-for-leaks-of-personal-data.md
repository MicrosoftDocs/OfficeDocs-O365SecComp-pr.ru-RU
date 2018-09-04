---
title: Отслеживание утечек персональных данных
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Strat_O365_Enterprise
- Ent_O365
- GDPR
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: Узнайте о трех средствах, которые можно использовать для отслеживания утечек персональных данных.
ms.openlocfilehash: b2ff4e686c3131260327b1c935603693eaa7f816
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272414"
---
# <a name="monitor-for-leaks-of-personal-data"></a>Отслеживание утечек персональных данных

Для отслеживания использования и транспортировки персональных данных можно использовать ряд средств. В этой статье описаны три популярных средства.

![Средства для отслеживания использования и транспортировки персональных данных](Media/Monitor-for-leaks-of-personal-data-image1.png)

На этом рисунке:

-   Сначала используйте отчеты Office 365 для защиты от потери данных, чтобы отслеживать персональные данные в SharePoint Online, OneDrive для бизнеса и передаваемой электронной почте. Они обеспечивают максимальный уровень детализации для отслеживания персональных данных. Тем не менее эти отчеты включают не все службы в Office 365.

-   После этого используйте политики оповещений и журнал аудита Office 365, чтобы отслеживать действия в службах Office 365. Настройте текущее отслеживание или выполните поиск в журнале аудита, чтобы исследовать инцидент. Журнал аудита Office 365 можно использовать в различных службах Office 365, таких как Sway, PowerBI, Dynamics 365, Microsoft Flow, Microsoft Teams, OneDrive для бизнеса и SharePoint Online, а также для обнаружения электронных данных, анализа действий администратора, отслеживания передаваемой почты и неактивных почтовых ящиков. Беседы Skype включаются в неактивные почтовые ящики.

-   Наконец, используйте Microsoft Cloud App Security для отслеживания файлов с конфиденциальными данными в службах SaaS других поставщиков. В ближайшее время вы сможете использовать типы конфиденциальной информации Office 365 и единообразные метки в Azure Information Protection и Office с Cloud App Security. Вы можете настроить политики, которые применяются ко всем или отдельным (например, Box) приложениям SaaS. С помощью Cloud App Security невозможно обнаруживать файлы в Exchange Online, в том числе файлы, вложенные в сообщения электронной почты.

## <a name="office-365-data-loss-prevention-reports"></a>Отчеты о защите от потери данных в Office 365

Создав политики защиты от потери данных, необходимо убедиться, что они работают правильно и помогают обеспечивать соответствие требованиям. С помощью отчетов о защите от потери данных в Office 365 можно быстро просматривать количество совпадений, переопределений и ложных срабатываний касательно таких политик, динамику их использования, а также фильтровать отчеты различными способами и отображать дополнительные сведения, выбирая точки на линии графика.

Отчеты о защите от потери данных позволяют:

-   Сосредоточиться на определенных временных промежутках и определить причины скачков и тенденций.

-   выявить бизнес-процессы, которые нарушают политики защиты от потери данных вашей организации;

-   Определить влияние политик защиты от потери данных на работу вашей организации.

-   просматривать основания, которые пользователи предоставляют для отправки сообщения о ложном срабатывании или для переопределения политики при ознакомлении с подсказкой политики;

-   проверить соответствие требованиям конкретной политики защиты от потери данных, отображая все совпадения с правилами этой политики;

-   просмотреть список файлов с конфиденциальными данными, который соответствует правилам политик защиты от потери данных вашей организации, в области сведений.

Кроме того, эти отчеты можно использовать для точной настройки ваших политик защиты от потери данных при их выполнении в тестовом режиме.

Отчеты о защите от потери данных расположены в Центре безопасности и соответствия требованиям. Перейдите в раздел "Отчеты" \> "Просмотр отчетов". В разделе "Защита от потери данных (DLP)" выберите "Совпадения по правилу и политике защиты от потери данных" или "Ложные срабатывания и переопределения функции защиты от потери данных".

Дополнительные сведения см. в статье [Просмотр отчетов о защите от потери данных](https://support.office.com/ru-RU/article/View-the-reports-for-data-loss-prevention-41eb4324-c513-4fa5-91c8-8fbd8aaba83b).

![Отчет, в котором показаны совпадения по политике защиты от потери данных](Media/Monitor-for-leaks-of-personal-data-image2.png)

## <a name="office-365-audit-log-and-alert-policies"></a>Журнал аудита Office 365 и политики оповещений

Журнал аудита Office 365 включает события из Exchange Online, SharePoint Online, OneDrive для бизнеса, Azure Active Directory, Microsoft Teams, Power BI, Sway и других служб Office 365.

Центр безопасности и соответствия требованиям Office 365 поддерживает два способа отслеживания журнала аудита Office 365 и создания отчетов о нем:

-   настройка политик оповещений, просмотр оповещений и отслеживание тенденций: используйте новую политику оповещений и инструменты панели мониторинга оповещений в Центре безопасности и соответствия требованиям Office 365;

-   непосредственный поиск в журнале аудита: поиск можно выполнять по всем событиям в указанном диапазоне дат. Кроме того, можно фильтровать результаты на основе заданных условий, например по пользователю, выполнившему действие, по действию или целевому объекту.

Группы по обеспечению информационной безопасности и соответствия требованиям могут использовать эти средства для упреждающей проверки действий пользователей и администраторов в службах Office 365. Можно настроить автоматические оповещения, чтобы отправлять по электронной почте уведомления об определенных действиях в конкретных семействах веб-сайтов (например, о предоставлении общего доступа к содержимому с веб-сайтов, на которых имеются данные, подпадающие под действие регламента GDPR). Таким образом, эти группы смогут отслеживать соблюдение пользователями корпоративных политик безопасности либо предоставить им дополнительные услуги по обучению.

Кроме того, группы по обеспечению информационной безопасности могут выполнять поиск в журнале аудита для исследования потенциальных нарушений безопасности данных, определяя как первопричины, так и степень этих нарушений. Эта встроенная возможность позволяет обеспечить соответствие требованиям статей 33 и 34 регламента GDPR, согласно которым в течение определенного периода времени о нарушении безопасности данных требуется уведомить как надзорный орган GDPR, так и самих субъектов данных. Записи журнала аудита сохраняются в службе только на протяжении 90 дней. Тем не менее эти журналы часто рекомендуется хранить в течение большего периода времени (и так поступают многие организации).

Доступны решения, которые обеспечивают подписку на единые журналы аудита с помощью API действий управления Microsoft, сохранение записей журналов (при необходимости) и предоставление расширенных панелей мониторинга и оповещений. Пример такого решения — [Microsoft Operations Management Suite (OMS)](https://docs.microsoft.com/ru-RU/azure/operations-management-suite/oms-solution-office-365).

Дополнительные сведения о политиках оповещений и поиске в журнале аудита:

-   [Политики оповещений в Центре безопасности и соответствия требованиям Office 365](https://support.office.com/ru-RU/article/Alert-policies-in-the-Office-365-Security-Compliance-Center-8927B8B9-C5BC-45A8-A9F9-96C732E58264)

-   [Поиск действий пользователей и администраторов в журнале аудита в Office 365](https://support.office.com/ru-RU/article/Search-the-audit-log-for-user-and-admin-activity-in-Office-365-57CA5138-0AE0-4D34-BD40-240441EF2FB6) (введение)

-   [Включение и отключение поиска в журнале аудита Office 365](https://support.office.com/ru-RU/article/Turn-Office-365-audit-log-search-on-or-off-e893b19a-660c-41f2-9074-d3631c95a014)

-   
  [Поиск по журналу аудита в Центре безопасности и соответствия требованиям Office 365](https://support.office.com/en-us/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c?ui=en-US&rs=en-US&ad=US)

-   
  [Search-UnifiedAuditLog](https://technet.microsoft.com/en-us/library/mt238501(v=exchg.160).aspx) (командлет) 

-   [Подробные свойства в журнале аудита Office 365](https://support.office.com/ru-RU/article/Detailed-properties-in-the-Office-365-audit-log-ce004100-9e7f-443e-942b-9b04098fcfc3)

## <a name="microsoft-cloud-app-security"></a>Microsoft Cloud App Security

Microsoft Cloud App Security позволяет обнаруживать другие приложения SaaS, используемые в ваших сетях, и конфиденциальные данные, которые отправляются в эти приложения или из них.

Microsoft Cloud App Security — это полнофункциональная служба, обеспечивающая глубокую наглядность, детальные элементы управления и улучшенную защиту облачных приложений от угроз. Она позволяет идентифицировать более чем 15 000 облачных приложений в сети на всех устройствах, гарантируя постоянную оценку и анализ рисков. Отпадает необходимость в агентах: из брандмауэров и прокси-серверов собираются полные контекстные данные об использовании облачных решений и теневых ИТ.

Для лучшего понимания вашей облачной среды доступная в Cloud App Security функция исследования позволяет получить подробные данные обо всех действиях, файлах и учетных записях для санкционированных и управляемых приложений. Вы можете получить детальные сведения на уровне файлов и определить пути перемещения данных в облачных приложениях.

Например, на рисунке ниже приведены две политики Cloud App Security, которые помогут обеспечить соответствие требованиям регламента GDPR.

![Примеры политик Cloud App Security](Media/Monitor-for-leaks-of-personal-data-image3.png)

Первая политика оповещает вас о предоставлении общего доступа к предопределенному атрибуту личных сведений или выбранному вами настраиваемому выражению за пределами организации из указанных приложений SaaS.

Вторая политика блокирует скачивание файлов на любое неуправляемое устройство. Вы выбираете искомые атрибуты в файлах и приложения SaaS, к которым необходимо применить политику.

В ближайшее время в Cloud App Security будут представлены следующие типы атрибутов:

-   типы конфиденциальной информации Office 365;

-   единообразные метки в Office 365 и Azure Information Protection.

### <a name="cloud-app-security-dashboard"></a>Панель мониторинга Cloud App Security

Если вы еще не начали использовать Cloud App Security, сначала запустите это решение. Получите доступ к Cloud App Security по следующему адресу: <https://portal.cloudappsecurity.com>.

Примечание. Обязательно установите флажок "Автоматически сканировать файлы на наличие меток классификации Azure Information Protection" (в общих параметрах), прежде чем приступить к работе с Cloud App Security или назначить метки. После настройки Cloud App Security выполняет повторное сканирование имеющихся файлов только после их изменения.

![Панель мониторинга со сведениями об оповещениях](Media/Monitor-for-leaks-of-personal-data-image4.png)

Дополнительные сведения:

-   [Развертывание Cloud App Security](https://docs.microsoft.com/ru-RU/cloud-app-security/getting-started-with-cloud-app-security)

-   [Дополнительные сведения о Microsoft Cloud App Security](https://www.microsoft.com/ru-RU/cloud-platform/cloud-app-security)

-   [Блокировка скачивания конфиденциальных данных с помощью прокси-сервера Microsoft Cloud App Security](https://docs.microsoft.com/ru-RU/cloud-app-security/use-case-proxy-block-session-aad)

## <a name="example-file-and-activity-policies-to-detect-sharing-of-personal-data"></a>Примеры политик файлов и действий для обнаружения случаев предоставления общего доступа к персональным данным

### <a name="detect-sharing-of-files-containing-pii--credit-card-number"></a>Обнаружение случаев предоставления общего доступа к файлам, содержащим личные сведения — номер кредитной карты

Отправка оповещений о случаях предоставления общего доступа к файлу, содержащему номер кредитной карты, из утвержденного облачного приложения.

<table>
<thead>
<tr class="header">
<th align="left"><strong>Элемент управления</strong></th>
<th align="left"><strong>Настройки</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Тип политики</td>
<td align="left">Политика файлов</td>
</tr>
<tr class="even">
<td align="left">Шаблон политики</td>
<td align="left">Без шаблона</td>
</tr>
<tr class="odd">
<td align="left">Серьезность политики</td>
<td align="left">Высокая</td>
</tr>
<tr class="even">
<td align="left">Категория</td>
<td align="left">Защита от потери данных</td>
</tr>
<tr class="odd">
<td align="left">Параметры фильтра</td>
<td align="left"><p>Уровень доступа = "Общедоступный (Интернет)", "Общедоступный", "Внешний"</p>
<p>Приложение = &lt;select apps&gt; (используйте этот параметр, чтобы отслеживать только определенные приложения SaaS)</p></td>
</tr>
<tr class="even">
<td align="left">Применимо к</td>
<td align="left">Всем файлам, всем владельцам</td>
</tr>
<tr class="odd">
<td align="left">Проверка содержимого</td>
<td align="left"><p>Включает файлы, которые соответствуют текущему выражению: "Все страны": "Финансы": "Номер кредитной карты"</p>
<p>Флажок "Не требовать наличие релевантного контекста": снят (будут учитываться как ключевые слова, так и регулярное выражение)</p>
<p>Включает файлы с хотя бы 1 совпадением</p>
<p>Флажок "Снять маску с последних четырех символов нарушения": установлен</p></td>
</tr>
<tr class="even">
<td align="left">Оповещения</td>
<td align="left"><p>Флажок "Создать оповещение для каждого соответствующего файла": установлен</p>
<p>Ежедневный лимит оповещений: 1000</p>
<p>Флажок "Выбрать оповещение по электронной почте": установлен</p>
<p>Получатель: infosec@contoso.com</p></td>
</tr>
<tr class="odd">
<td align="left">Управление</td>
<td align="left"><p>Microsoft OneDrive для бизнеса</p>
<p>Придание конфиденциального статуса: установите флажок "Удалить доступ для внешних пользователей"</p>
<p>Все другие флажки: сняты</p>
<p>Microsoft SharePoint Online</p>
<p>Придание конфиденциального статуса: установите флажок "Удалить доступ для внешних пользователей"</p>
<p>Все другие флажки: сняты</p></td>
</tr>
</tbody>
</table>

Похожие политики:

-   обнаружение случаев предоставления общего доступа к файлам, содержащим личные сведения — адрес электронной почты;

-   обнаружение случаев предоставления общего доступа к файлам, содержащим личные сведения — номер паспорта.

### <a name="detect-customer-or-hr-data-in-box-or-onedrive-for-business"></a>Обнаружение данных о клиентах или персонале в приложении Box или OneDrive для бизнеса

Отправка оповещений о передаче файла с меткой "Данные клиента" или "Данные о персонале" в OneDrive для бизнеса или в приложение Box.

Примечания.

-   Для отслеживания приложения Box необходимо настроить соединитель с помощью пакета SDK для API Connector.

-   Для этой политики требуются возможности, которые сейчас доступны только в закрытой предварительной версии.

<table>
<thead>
<tr class="header">
<th align="left"><strong>Элемент управления</strong></th>
<th align="left"><strong>Настройки</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Тип политики</td>
<td align="left">Политика действий</td>
</tr>
<tr class="even">
<td align="left">Шаблон политики</td>
<td align="left">Без шаблона</td>
</tr>
<tr class="odd">
<td align="left">Серьезность политики</td>
<td align="left">Высокая</td>
</tr>
<tr class="even">
<td align="left">Категория</td>
<td align="left">Управление общим доступом</td>
</tr>
<tr class="odd">
<td align="left">Выполнение действий над</td>
<td align="left">Одиночное действие</td>
</tr>
<tr class="even">
<td align="left">Параметры фильтра</td>
<td align="left"><p>Тип действия = отправка файла</p>
<p>Приложение = Microsoft OneDrive для бизнеса и Box</p>
<p>Метка классификации (сейчас доступна в закрытой предварительной версии): Azure Information Protection = "Данные клиента", "Управление персоналом — данные о зарплате", "Управление персоналом — данные о сотрудниках"</p></td>
</tr>
<tr class="odd">
<td align="left">Оповещения</td>
<td align="left"><p>Флажок "Создать оповещение": установлен</p>
<p>Ежедневный лимит оповещений: 1000</p>
<p>Флажок "Выбрать оповещение по электронной почте": установлен</p>
<p>Получатель: infosec@contoso.com</p></td>
</tr>
<tr class="even">
<td align="left">Управление</td>
<td align="left"><p>Все приложения</p>
<p>Флажок "Поместить пользователя в карантин": установлен</p>
<p>Все другие флажки: сняты</p>
<p>Office 365</p>
<p>Флажок "Поместить пользователя в карантин": установлен</p>
<p>Все другие флажки: сняты</p></td>
</tr>
</tbody>
</table>

Похожие политики:

-   обнаружение скачиваний данных о клиентах или персонале в больших объемах — отправка оповещений о случаях, когда отдельный пользователь в течение короткого периода времени скачивает много файлов, содержащих данные о клиентах или персонале;

-   обнаружение случаев предоставления общего доступа к данным о клиентах или персонале — отправка оповещений о случаях предоставления общего доступа к данным о клиентах или персонале.