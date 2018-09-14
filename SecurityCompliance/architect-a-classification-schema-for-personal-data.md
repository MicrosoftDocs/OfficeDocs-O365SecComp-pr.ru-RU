---
title: Разработка архитектуры схемы классификации для персональных данных
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
ms.custom: ''
ms.assetid: ''
search.appverid:
- MET150
description: Определите, целесообразно ли вашей организации внедрять метки в рамках плана по соблюдению регламента GDPR.
ms.openlocfilehash: 82eec50284f0aa4b0b74346c9fbbfc717dc08d07
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272254"
---
# <a name="architect-a-classification-schema-for-personal-data"></a>Разработка архитектуры схемы классификации для персональных данных

В предыдущих статьях из этой серии рассматривалось использование типов конфиденциальной информации для определения персональных данных, подпадающих под действие регламента GDPR. Типы конфиденциальной информации — это разновидность классификации. Возможно, вам понадобится только эта классификация. Тем не менее многие организации внедряют более широкую стратегию управления данными с использованием меток. Ознакомьтесь с этой статьей, чтобы решить, нужно ли вам внедрять метки в рамках своего плана по соблюдению регламента GDPR. Если вы примете это решение, воспользуйтесь инструкциями и примерами, приведенными в настоящей статье.

Примечание. Определение схемы классификации для организации и настройка политики, меток и условий требуют тщательного планирования и подготовки. Важно понимать, что за этот процесс не отвечает ваш ИТ-отдел. При разработке соответствующей схемы классификации и применения меток для данных вашей организации обязательно сотрудничайте со своим юридическим отделом и группой по обеспечению соответствия требованиям.

## <a name="decide-if-you-are-using-labels-in-addition-to-sensitive-data-types"></a>Принятие решения о целесообразности использования меток в дополнение к типам конфиденциальных данных

Вы можете воспользоваться одним из двух подходов к классификации персональных данных в Office 365. Любой из них можно применить для защиты данных в соответствии с регламентом GDPR. Если вы решили использовать для классификации только типы конфиденциальной информации, можете пропустить оставшуюся часть этой статьи.

Выберите один из приведенных ниже вариантов.

### <a name="option-1-use-only-office-365-sensitive-information-types"></a>Вариант 1. Использование только типов конфиденциальной информации Office 365

-   Типы конфиденциальной информации целесообразно использовать для определения и защиты персональных данных, которые подпадают под действие регламента GDPR и других типов нормативных требований.

-   Этот вариант более простой, чем расширенный план по управлению данными с использованием меток.

-   Типы конфиденциальной информации используются с правилами защиты от потери данных (как и метки Office).

-   В будущем их можно будет применять с Cloud App Security для обнаружения конфиденциальной информации в других приложениях SaaS.

### <a name="option-2-use-sensitive-information-types--office-labels"></a>Вариант 2. Использование типов конфиденциальной информации и меток Office

-   Типы конфиденциальной информации — это необходимый компонент, так как они понадобятся для автоматического применения меток к персональным данным, подпадающим под действие регламента GDPR.

-   Метки Office позволяют включить персональные данные, на которые распространяется регламент GDPR, в расширенный план по управлению данными для вашей организации.

-   В будущем метки Office будут объединены с метками Azure Information Protection для создания единой подсистемы классификации и применения меток.

## <a name="develop-a-label-schema-that-includes-personal-data"></a>Разработка схемы меток, включающей персональные данные

Прежде чем воспользоваться техническими возможностями для применения меток и защиты, сначала определите схему классификации для своей организации. Возможно, у нее уже имеется схема классификации, что упрощает добавление персональных данных. В этой статье приведен пример схемы классификации. При необходимости вы можете использовать его в качестве отправной точки.

### <a name="getting-started"></a>Начало работы

Сначала выберите количество и имена меток, которые необходимо внедрить. При этом не беспокойтесь об используемых технологиях и способах применения меток. Примените эту схему в пределах всей организации, в том числе к данным, которые хранятся в локальной среде и других облачных службах.

### <a name="recommendations"></a>Рекомендации 

Разрабатывая и внедряя политики, метки и условия, руководствуйтесь вот какими рекомендациями.

-   Используйте имеющуюся схему классификации (при наличии). Многие организации уже пользуются определенными разновидностями классификации данных. Тщательно проанализируйте имеющуюся схему меток и по возможности используйте ее без изменений. Использование знакомых пользователя меток повысит эффективность их принятия.

-   В начале используйте стандартные политики и метки. Все решения поставляются с набором предопределенных политик и меток. Тщательно оцените, насколько они соответствуют вашим юридическим и бизнес-требованиям, и по возможности используйте именно их, а не создавайте новые.

-   Начните с малого. Вы можете создать практически неограниченное количество меток. Тем не менее большое число основных и вложенных меток отрицательно скажется на их принятии. Слишком много вариантов выбора часто приводят к невозможности выбора.

-   Применяйте сценарии и варианты использования. Определите варианты использования, характерные для организации и созданные на основе регламента GDPR, чтобы проверить, будет ли предполагаемая конфигурация применения меток и классификации работать на практике.

-   Определите целесообразность использования новой метки в каждом запросе. Действительно ли нужна новая метка для каждого сценария или варианта использования, либо достаточно ли воспользоваться уже имеющейся меткой? Сведите количество меток к минимуму, чтобы улучшить их принятие.

-   Используйте вложенные метки для ключевых отделов. Некоторые отделы отличаются особыми требованиями, для которых требуются особенные метки. Определите эти метки в качестве вложенных меток. Кроме того, рассмотрите возможность использования политик с областью действия, которые применяются к группам пользователей, а не ко всей организации.

-   Рассмотрите возможность использования политик с областью действия. Политики, нацеленные на определенные подмножества пользователей, предотвращают чрезмерное количество меток. Политика с областью действия позволяет назначить роль или относящиеся к конкретному отделу метки (в том числе вложенные) сотрудникам, которые работают именно в этом отделе.

-   Используйте понятные имена меток. В качестве имен меток не рекомендуется использовать жаргонные слова, стандартные сокращения или акронимы. Целесообразно использовать понятные пользователям имена, чтобы улучшить принятие меток. Например, вместо таких меток, как PII, PCI, HIPAA, LBI, MBI и HBI, используйте имена типа "Не бизнес-данные", "Общедоступные", "Общие", "Конфиденциально" и "Строго конфиденциально".

### <a name="example-classification-schema"></a>Пример схемы классификации

<table>
<thead>
<tr class="header">
<th align="left"><strong>Имя метки</strong></th>
<th align="left"><strong>Описание</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Персональные</td>
<td align="left">Не бизнес-данные, предназначенные только для личного использования.</td>
</tr>
<tr class="even">
<td align="left">Общедоступные</td>
<td align="left">Бизнес-данные, специально подготовленные и утвержденные для предоставления широкой публике.</td>
</tr>
<tr class="odd">
<td align="left">Данные клиента</td>
<td align="left">Бизнес-данные, содержащие личные сведения, например номера кредитных карт, банковских счетов и социального страхования.</td>
</tr>
<tr class="even">
<td align="left">Данные о персонале</td>
<td align="left">Данные отдела кадров о сотрудниках Contoso, например номер сотрудника и сведения о зарплате.</td>
</tr>
<tr class="odd">
<td align="left">Конфиденциально</td>
<td align="left">Конфиденциальные бизнес-данные, предоставление которых не тем людям может нанести ущерб организации. Примеры: контракты, отчеты системы безопасности, прогнозные сводки и данные о продажах клиентам.</td>
</tr>
<tr class="even">
<td align="left">Строго конфиденциально</td>
<td align="left">Строго конфиденциальные бизнес-данные, предоставление которых не тем людям может нанести ущерб организации. Примеры: информация о сотрудниках и клиентах, пароли, исходный код и финансовые отчеты, о которых объявляется заранее.</td>
</tr>
</tbody>
</table>

## <a name="define-a-taxonomy-and-search-criteria-for-each-label"></a>Определение таксономии и условий поиска для каждой метки

Следующий шаг после разработки схемы классификации для вашей организации — разработать таксономию и условия поиска этих данных. Вы уже выполнили эти задачи для персональных данных, определив типы конфиденциальной информации, а также настроив или создав новые типы конфиденциальной информации для своей среды.

В таблице ниже приведен пример схемы, таксономии и условий поиска для организации. Метки упорядочены по уровню конфиденциальности от наименее до наиболее конфиденциальных, чтобы гарантировать назначение правильной метки данным, которые соответствуют нескольким условиям метки.

Примечание. Этот пример конфигурации приведен исключительно для иллюстрации и не предназначен для использования в качестве руководства или справки по развертыванию.

Крайне важно убедиться, что ваши действия по классификации персональных данных для соответствия требованиям регламента GDPR сочетаются с целями всей организации.

### <a name="example-schema-taxonomy-and-search-criteria"></a>Пример схемы, таксономии и условий поиска

<table>
<thead>
<tr class="header">
<th align="left"><strong>Метка</strong></th>
<th align="left"><strong>Таксономия</strong></th>
<th align="left"><strong>Метод</strong></th>
<th align="left"><strong>Синтаксис поиска</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Персональные</td>
<td align="left">Документы, к которым пользователь вручную применил метку как к персональным.</td>
<td align="left">Вручную</td>
<td align="left">Документы, к которым пользователь вручную применил метку как к персональным.</td>
</tr>
<tr class="even">
<td align="left">Общедоступные</td>
<td align="left">Документы, содержащие фразу Approved for Public Release ##/#### (без учета регистра), где # представляет собой любую цифру.</td>
<td align="left"><p>KQL</p>
<p>Регулярное выражение</p></td>
<td align="left"><p>KQL — Approved for Public Release (Утверждено для общедоступного выпуска)*</p>
<p>Регулярное выражение — (?i)(\bApproved for Public Release \d{2}\/\d{4}\b)</p></td>
</tr>
<tr class="odd">
<td align="left">Данные клиента</td>
<td align="left">Типы конфиденциальной информации о гражданах стран ЕС.</td>
<td align="left">Типы конфиденциальной информации</td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left">Управление персоналом — данные о сотрудниках</td>
<td align="left">Документы, включающие идентификатор сотрудника (с учетом регистра) в формате CONTOSO-9#####, где # представляет собой любую цифру.</td>
<td align="left"><p>KQL</p>
<p>Регулярное выражение</p></td>
<td align="left"><p>KQL — CONTOSO-9*</p>
<p>Регулярное выражение — (\bCONTOSO-9\d{5}\b)</p></td>
</tr>
<tr class="odd">
<td align="left">Отдел кадров — данные о зарплате</td>
<td align="left">Документы, включающие ключевое слово (без учета регистра) Contoso и ключевое слово (без учета регистра) Salary или Compensation</td>
<td align="left"><p>KQL</p>
<p>Регулярное выражение</p></td>
<td align="left"><p>KQL — Contoso AND (Salary OR Compensation)</p>
<p>Регулярное выражение — (\bCONTOSO-9\d{5}\b)</p></td>
</tr>
<tr class="even">
<td align="left">Конфиденциально</td>
<td align="left">Документы, содержащие фразу Contoso Confidential (без учета регистра).</td>
<td align="left"><p>KQL</p>
<p>Регулярное выражение</p></td>
<td align="left"><p>KQL — Contoso Confidential</p>
<p>Регулярное выражение — (?i)(\bContoso Confidential\b)</p></td>
</tr>
<tr class="odd">
<td align="left">Строго конфиденциально</td>
<td align="left">Документы, содержащие фразу (с учетом регистра) Contoso Secret или Secret-C####, где # представляет собой любую цифру.</td>
<td align="left"><p>KQL</p>
<p>Регулярное выражение</p></td>
<td align="left"><p>KQL — Contoso Secret OR Secret-C*</p>
<p>Регулярное выражение — (?i)(\bContoso Secret\b)|(\bSecret-C\d{4}\b)</p></td>
</tr>
</tbody>
</table>