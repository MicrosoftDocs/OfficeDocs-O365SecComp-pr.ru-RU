---
title: Трассировка сообщений в центре соответствия требованиям & безопасности
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Администраторы могут использовать Трассировка сообщений в центре соответствия требованиям & безопасности, чтобы узнать, что происходит в сообщениях.
ms.openlocfilehash: 9dfdab4adc5caba55664e93b49c8428791670ab3
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685621"
---
# <a name="message-trace-in-the-security--compliance-center"></a><span data-ttu-id="9f303-103">Трассировка сообщений в центре соответствия требованиям & безопасности</span><span class="sxs-lookup"><span data-stu-id="9f303-103">Message trace in the Security & Compliance Center</span></span>

<span data-ttu-id="9f303-p101">Трассировка сообщений в центре соответствия требованиям & безопасности следует сообщений электронной почты, проходящих через организации Exchange Online. Можно определить, если сообщение было получено, отклонено, отложенной или доставлено службой. Также показаны действия, которые были сделаны в сообщении перед его связаться с вами его конечное состояние.</span><span class="sxs-lookup"><span data-stu-id="9f303-p101">Message trace in the Security & Compliance Center follows email messages as they travel through your Exchange Online organization. You can determine if a message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="9f303-p102">Трассировка сообщений в центре соответствия требованиям & безопасности расширяет трассировки, который был доступен в центре администрирования Exchange (EAC). Сведения из трассировки можно использовать для эффективного ответы на вопросы пользователей о что случилось с сообщения, помещенные, устранение неполадок потока почты и проверки изменения политики.</span><span class="sxs-lookup"><span data-stu-id="9f303-p102">Message trace in the Security & Compliance Center improves upon message trace that was available in the Exchange admin center (EAC). You can use the information from message trace to efficiently answer user questions about what happened to their messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="9f303-109">Открыть сообщение трассировки</span><span class="sxs-lookup"><span data-stu-id="9f303-109">Open message trace</span></span>

1. <span data-ttu-id="9f303-110">[Войдите в Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) с помощью рабочая или учебная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="9f303-110">[Sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="9f303-111">Слева вверху щелкните значок средства запуска приложений ![Значок средства запуска приложения Office 365](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) и выберите **Администратор**.</span><span class="sxs-lookup"><span data-stu-id="9f303-111">Select the app launcher icon ![Office 365 app launcher icon](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="9f303-112">В панели навигации слева разверните узел **центра администрирования** и выберите **Безопасность & соответствия требованиям**.</span><span class="sxs-lookup"><span data-stu-id="9f303-112">In the lower-left navigation, expand **Admin centers** and select **Security & Compliance**.</span></span>

4. <span data-ttu-id="9f303-113">На открывшейся странице **Security & Compliance** разверните **поток почты**и выберите **Трассировка сообщений**.</span><span class="sxs-lookup"><span data-stu-id="9f303-113">In the **Security & Compliance** page that opens, expand **Mail flow**, and select **Message trace**.</span></span>

## <a name="message-trace-page"></a><span data-ttu-id="9f303-114">Страница отслеживания сообщений</span><span class="sxs-lookup"><span data-stu-id="9f303-114">Message trace page</span></span>

<span data-ttu-id="9f303-p103">Здесь можно начать новую трассировку по умолчанию, нажав кнопку **Пуск трассировки** . Это будет искать все сообщения для всех отправителей и получателей в течение последних двух дней. Или можно использовать один из сохраненных запросов из доступных запрос категории, либо выполните их как-является или использовать их в качестве основы для собственных запросов:</span><span class="sxs-lookup"><span data-stu-id="9f303-p103">From here you can start a new default trace by clicking on the **Start a trace** button. This will search for all messages for all senders and recipients for the last two days. Or you can use one of the stored queries from the available query categories and either run them as-is or use them as starting points for your own queries:</span></span>

- <span data-ttu-id="9f303-118">**По умолчанию запросы**: встроенные запросы, предоставляемые Office 365.</span><span class="sxs-lookup"><span data-stu-id="9f303-118">**Default queries**: Built-in queries provided by Office 365.</span></span>

- <span data-ttu-id="9f303-119">**Настраиваемые запросов**: запросы раз сохранена с Администраторы в вашей организации для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="9f303-119">**Custom queries**: Queries saved by admins in your organization for future use.</span></span>

- <span data-ttu-id="9f303-p104">**Запросы автоматически сохраненная**: последние десять последним выполнение запросов. Этот список позволяет легко трубку места.</span><span class="sxs-lookup"><span data-stu-id="9f303-p104">**Autosaved queries**: The last ten most recently run queries. This list makes it simple to pick up where you left off.</span></span>

<span data-ttu-id="9f303-122">Также на этой странице — раздел **загружаемым отчетов** для отправки запросов, а также сами отчеты, при наличии доступен для загрузки.</span><span class="sxs-lookup"><span data-stu-id="9f303-122">Also on this page is a **Downloadable reports** section for the requests you've submitted, as well as the reports themselves when they're are available for download.</span></span>

## <a name="options-for-a-new-message-trace"></a><span data-ttu-id="9f303-123">Параметры для новой трассировки</span><span class="sxs-lookup"><span data-stu-id="9f303-123">Options for a new message trace</span></span>

### <a name="filter-by-senders-and-recipients"></a><span data-ttu-id="9f303-124">Фильтровать по отправителям и получателям</span><span class="sxs-lookup"><span data-stu-id="9f303-124">Filter by senders and recipients</span></span>

<span data-ttu-id="9f303-125">Значения по умолчанию, **всем отправителям** и **всех получателей**, но можно использовать следующие поля для фильтрации результатов:</span><span class="sxs-lookup"><span data-stu-id="9f303-125">The default values are **All senders** and **All recipients**, but you can use the following fields to filter the results:</span></span>

- <span data-ttu-id="9f303-p105">**Эти пользователи**: щелкните в этом поле для выбора одного или нескольких отправителей из вашей организации. Кроме того, можно начать введите имя и элементов в списке фильтруются по что ввода, намного как поведение на странице поиска.</span><span class="sxs-lookup"><span data-stu-id="9f303-p105">**By these people**: Click in this field to select one or more senders from your organization. You can also start to type a name and the items in the list will be filtered by what you've typed, much like how a search page behaves.</span></span>

- <span data-ttu-id="9f303-128">**Чтобы эти сотрудники**: щелкните в этом поле для выбора одного или нескольких получателей в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9f303-128">**To these people**: Click in this field to select one or more recipients in your organization.</span></span>

<span data-ttu-id="9f303-p106">Можно также ввести адреса электронной почты внешним отправителям и получателям. Поддерживаются подстановочные знаки (`*@contoso.com` или `scot?@contoso.com`), но нельзя использовать несколько записи с подстановочными знаками в одном поле в то же время.</span><span class="sxs-lookup"><span data-stu-id="9f303-p106">You can also type the email addresses of external senders and recipients. Wildcards are supported (`*@contoso.com` or `scot?@contoso.com`), but you can't use multiple wildcard entries in the same field at the same time.</span></span>

### <a name="time-range"></a><span data-ttu-id="9f303-131">Диапазон времени</span><span class="sxs-lookup"><span data-stu-id="9f303-131">Time range</span></span>

<span data-ttu-id="9f303-p107">Значение по умолчанию — **2 дня**, но можно указать диапазон даты и времени до 90 дней. При использовании диапазонов даты и времени, необходимо учесть следующие проблемы:</span><span class="sxs-lookup"><span data-stu-id="9f303-p107">The default value is **2 days**, but you can specify date/time ranges of up to 90 days. When you use date/time ranges, consider these issues:</span></span>

- <span data-ttu-id="9f303-p108">По умолчанию выберите диапазон времени в представлении **ползунок** с помощью строки времени. Выберите день или параметры, которые отображаются можно только. При попытке выбора промежуточных значение будет привязана пузырьковой начала или окончания для ближайшей отображается параметр.</span><span class="sxs-lookup"><span data-stu-id="9f303-p108">By default, you select the time range in **Slider** view using a time line. You can only select the day or time settings that are displayed. Trying to select an in-between value will snap the start/end bubble to the nearest displayed setting.</span></span>

   ![Диапазон времени ползунок в трассировку сообщений в центре соответствия требованиям & безопасности](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   <span data-ttu-id="9f303-p109">Однако можно также переключиться **пользовательского** представления, где можно указать значения **Дата начала** и **Дата окончания** (в том числе время), а также можно выбрать **часовой пояс** для диапазон даты и времени. Обратите внимание на то, что параметр **часовой пояс** применяется к введенных данных запросов и результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="9f303-p109">But, you can also switch to **Custom** view where you can specify the **Start date** and **End date** values (including times), and you can also select the **Time zone** for the date/time range. Note that the **Time zone** setting applies to both your query inputs and your query results.</span></span>

   ![Настраиваемый диапазон времени в трассировку сообщений в центре соответствия требованиям & безопасности](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   <span data-ttu-id="9f303-p110">Немедленное в **сводном** отчете доступны для 10 дней или меньше результаты. Если указать диапазон времени, который еще немного больше, чем 10 дней, результаты будут задержать как есть только доступно в виде загружаемых CSV-файла ( **улучшенной сводки** или **Extended** отчета).</span><span class="sxs-lookup"><span data-stu-id="9f303-p110">For 10 days or less, the results are available instantly as a **Summary** report. If you specify a time range that's even slightly greater than 10 days, the results will be delayed as they are only available as a downloadable CSV file ( **Enhanced summary** or **Extended** reports).</span></span>

   <span data-ttu-id="9f303-143">Дополнительные сведения о различных типов отчетов обратитесь к разделу [выберите тип отчета](#choose-report-type) в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9f303-143">For more information about the different report types, see the [Choose report type](#choose-report-type) section in this topic.</span></span>

   <span data-ttu-id="9f303-p111">**Примечание**: расширенные сводки и расширенные отчеты подготавливаются с использованием данных заархивированные сообщения трассировки, и он может занять несколько часов до отчет доступен для загрузки. В зависимости от того, сколько Администраторы также был отправлен отчет о запросах в то время можно заметить также задержку перед запуском обработки помещенных в очередь запросов на.</span><span class="sxs-lookup"><span data-stu-id="9f303-p111">**Note**: Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available for download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before processing starts for your queued request.</span></span>

- <span data-ttu-id="9f303-p112">Сохранение запроса в представлении **ползунок** сохраняет относительное время диапазона (например, 3 дня сегодняшнего дня). Сохранение запроса в **настраиваемое** представление сохраняет диапазон абсолютный даты и времени (например, 2018-05-06 13:00 до 2018-05-08 18:00).</span><span class="sxs-lookup"><span data-stu-id="9f303-p112">Saving a query in **Slider** view saves the relative time range (for example, 3 days from today). Saving a query in **Custom** view saves the absolute date/time range (for example, 2018-05-06 13:00 to 2018-05-08 18:00).</span></span>

### <a name="more-search-options"></a><span data-ttu-id="9f303-148">Дополнительные параметры поиска</span><span class="sxs-lookup"><span data-stu-id="9f303-148">More search options</span></span>

#### <a name="delivery-status"></a><span data-ttu-id="9f303-149">Состояние доставки</span><span class="sxs-lookup"><span data-stu-id="9f303-149">Delivery status</span></span>

<span data-ttu-id="9f303-150">Можно оставить значение по умолчанию, **все** выбранные или можно выбрать один из следующих значений для фильтрации результатов:</span><span class="sxs-lookup"><span data-stu-id="9f303-150">You can leave the default value **All** selected, or you can select one of the following values to filter the results:</span></span>

- <span data-ttu-id="9f303-151">**Доставлено**: сообщение было успешно доставлено в место назначения.</span><span class="sxs-lookup"><span data-stu-id="9f303-151">**Delivered**: The message was successfully delivered to the intended destination.</span></span>

- <span data-ttu-id="9f303-152">**Ожидание**: доставки сообщения выполняется попытка или повторной.</span><span class="sxs-lookup"><span data-stu-id="9f303-152">**Pending**: Delivery of the message is being attempted or re-attempted.</span></span>

- <span data-ttu-id="9f303-153">**Развернутая**: получателя группа рассылки была расширена перед доставкой отдельных членов группы.</span><span class="sxs-lookup"><span data-stu-id="9f303-153">**Expanded**: A distribution group recipient was expanded before delivery to the individual members of the group.</span></span>

- <span data-ttu-id="9f303-154">**Ошибка**: не удается доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f303-154">**Failed**: The message was not delivered.</span></span>

- <span data-ttu-id="9f303-p113">**Карантин**: сообщения в карантин (как нежелательная почта, Массовая рассылка или фишинга). Дополнительные сведения см в [карантин сообщения электронной почты в Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f303-p113">**Quarantined**: The message was quarantined (as spam, bulk mail, or phishing). For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span></span>

- <span data-ttu-id="9f303-157">**Фильтрация как нежелательная почта**: сообщение было определяемую нежелательной почты и был отклонен или заблокирован (не помещенных в карантин).</span><span class="sxs-lookup"><span data-stu-id="9f303-157">**Filtered as spam**: The message was identified spam, and was rejected or blocked (not quarantined).</span></span>

- <span data-ttu-id="9f303-p114">**Получения состояния:** Сообщение было получено недавно с Office 365, но другие данные состояния еще недоступны. Проверьте обратно в несколько минут.</span><span class="sxs-lookup"><span data-stu-id="9f303-p114">**Getting status:** The message was recently received by Office 365, but no other status data is yet available. Check back in a few minutes.</span></span>

<span data-ttu-id="9f303-p115">**Примечание**: значения **ожидающих,** **помещенное в карантин**и **фильтр как нежелательной почты** доступны только для операций поиска не превышает 10 дней. Кроме того могут возникнуть задержки 5-10 минут между состояние фактические и переданные доставки.</span><span class="sxs-lookup"><span data-stu-id="9f303-p115">**Note**: The values **Pending,** **Quarantined**, and **Filter as spam** are only available for searches less than 10 days. Also, there might be a 5 to 10 minute delay between the actual and reported delivery status.</span></span>

#### <a name="message-id"></a><span data-ttu-id="9f303-162">ИД сообщения</span><span class="sxs-lookup"><span data-stu-id="9f303-162">Message ID</span></span>

<span data-ttu-id="9f303-p116">Это идентификатор сообщения Интернета (идентификатор клиента), который находится в **Message-ID:** поле заголовка в заголовке сообщения. Пользователи могут предоставить это значение для изучения определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9f303-p116">This is the internet message ID (also known as the Client ID) that's found in the **Message-ID:** header field in the message header. Users can give you this value to investigate specific messages.</span></span>

<span data-ttu-id="9f303-p117">Это значение является постоянным в течение времени жизни сообщения. Для сообщений, созданных в Office 365 или Exchange, значение задается в формате `<GUID@ServerFQDN>`, включая угловые скобки (\< \>). Например `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Другие системы обмена сообщениями могут использовать другой синтаксис или значения. Это значение — это должно быть уникальным, но не все системы электронной почты строго следуйте этим требованиям. Если **Message-ID:** поле заголовка не существует или не задан для входящих сообщений из внешних источников, назначенные произвольного значения.</span><span class="sxs-lookup"><span data-stu-id="9f303-p117">This value is constant for the lifetime of the message. For messages created in Office 365 or Exchange, the value is in the format `<GUID@ServerFQDN>`, including the angle brackets (\< \>). For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Other messaging systems might use different syntax or values. This value is supposed to be unique, but not all email systems strictly follow this requirement. If the **Message-ID:** header field doesn't exist or is blank for incoming messages from external sources, an arbitrary value is assigned.</span></span>

<span data-ttu-id="9f303-171">При использовании **Идентификатор сообщения** для фильтрации результатов, не забудьте включить полной строки, включая любые угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="9f303-171">When you use **Message ID** to filter the results, be sure to include the full string, including any angle brackets.</span></span>

#### <a name="direction"></a><span data-ttu-id="9f303-172">Направление</span><span class="sxs-lookup"><span data-stu-id="9f303-172">Direction</span></span>

<span data-ttu-id="9f303-173">Можно оставить значение по умолчанию, **все** выбранные или можно выбрать **Входящие** (сообщений, отправленных получателям в организации) или **исходящего соединителя** (сообщений, отправляемых с пользователями в вашей организации) для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="9f303-173">You can leave the default value **All** selected, or you can select **Inbound** (messages sent to recipients in your organization) or **Outbound** (messages sent from users in your organization) to filter the results.</span></span>

#### <a name="original-client-ip-address"></a><span data-ttu-id="9f303-174">Исходный IP-адрес клиента</span><span class="sxs-lookup"><span data-stu-id="9f303-174">Original client IP address</span></span>

<span data-ttu-id="9f303-p118">Можно filer результаты, IP-адрес клиента для изучения использованием компьютеров, которые отправки больших объемов нежелательной почты и вредоносных программ. Несмотря на то, что сообщения могут появляться, от различных отправителей, скорее всего, что все сообщения создает тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="9f303-p118">You can filer the results by client IP address to investigate hacked computers that are sending large amounts of spam or malware. Although the messages might appear to come from multiple senders, it's likely that the same computer is generating all of the messages.</span></span>

<span data-ttu-id="9f303-177">**Примечание**: сведения об адресе IP-адрес клиента доступна только для 10 дней и доступна только в отчетах **улучшенной сводки** или **Extended** (загружаемая CSV-файлы).</span><span class="sxs-lookup"><span data-stu-id="9f303-177">**Note**: The client IP address information is only available for 10 days, and is only available in the **Enhanced summary** or **Extended** reports (downloadable CSV files).</span></span>

### <a name="choose-report-type"></a><span data-ttu-id="9f303-178">Выберите тип отчета</span><span class="sxs-lookup"><span data-stu-id="9f303-178">Choose report type</span></span>

<span data-ttu-id="9f303-179">Отчет о доступных типов являются:</span><span class="sxs-lookup"><span data-stu-id="9f303-179">The available report types are:</span></span>

- <span data-ttu-id="9f303-p119">**Сводка**: недоступны, если диапазон времени меньше 10 дней и требуется без дополнительных параметров фильтрации. Результаты доступны практически сразу же после нажатия кнопки **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="9f303-p119">**Summary**: Available if the time range is less than 10 days, and requires no additional filtering options. The results are available almost immediately after you click **Search**.</span></span>

- <span data-ttu-id="9f303-p120">**Улучшенной сводки** или **Extended**: эти отчеты доступны только в качестве загрузки CSV-файлов и требуют одно или несколько из следующих параметров фильтрации независимо от диапазона времени: **эти пользователями**, **эти сотрудники**или \*\* Код сообщения\*\*. Можно использовать подстановочные знаки для отправителей или получателей (например, \*@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="9f303-p120">**Enhanced summary** or **Extended**: These reports are only available as downloadable CSV files, and require one or more of the following filtering options regardless of the time range: **By these people**, **To these people**, or **Message ID**. You can use wildcards for the senders or the recipients (for example, \*@contoso.com).</span></span>

<span data-ttu-id="9f303-184">**Примечания**.</span><span class="sxs-lookup"><span data-stu-id="9f303-184">**Notes**:</span></span>

- <span data-ttu-id="9f303-p121">Расширенные сводки и расширенные отчеты подготавливаются с использованием данных заархивированные сообщения трассировки, и он может занять несколько часов до отчет доступен для загрузки. В зависимости от того, сколько Администраторы также был отправлен отчет о запросах в то время можно заметить также задержку перед запуском помещенных в очередь запроса для обработки.</span><span class="sxs-lookup"><span data-stu-id="9f303-p121">Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available to download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before your queued request starts to be processed.</span></span>

- <span data-ttu-id="9f303-187">Хотя вы можете выбрать отчета улучшенной сводки или расширенные для каких-либо диапазон даты и времени, обычно за последние четыре часа архивных данных не работает, но при этом доступным для этих двух типов отчетов.</span><span class="sxs-lookup"><span data-stu-id="9f303-187">While you can select an Enhanced summary or Extended report for any date/time range, commonly the last four hours of archived data will not yet be available for these two types of reports.</span></span>

<span data-ttu-id="9f303-p122">При нажатии кнопки **Далее**, описанные страницу сводки, в котором приведены параметры фильтрации, которые вы выбрали, уникальный (редактируемые) заголовок отчета и адрес электронной почты, которая получает уведомление о завершении (также редактировать, трассировка сообщений и должны быть в одном из обслуживаемых доменов организации). Щелкните **подготовить отчет** для отправки сообщения трассировки. В главном **трассировки** страницы, можно просматривать состояние отчета в разделе **Downloadable отчетов** .</span><span class="sxs-lookup"><span data-stu-id="9f303-p122">When you click **Next**, you're presented with a summary page that lists the filtering options that you selected, a unique (editable) title for the report, and the email address that receives the notification when the message trace completes (also editable, and must be in one of your organization's accepted domains). Click **Prepare report** to submit the message trace. On the main **Message trace** page, you can see the status of the report in the **Downloadable reports** section.</span></span>

<span data-ttu-id="9f303-191">Дополнительные сведения о сведений, возвращаемых в различных типов отчетов см.</span><span class="sxs-lookup"><span data-stu-id="9f303-191">For more information about the information that's returned in the different report types, see the next section.</span></span>

## <a name="message-trace-results"></a><span data-ttu-id="9f303-192">Результатов трассировки</span><span class="sxs-lookup"><span data-stu-id="9f303-192">Message trace results</span></span>

<span data-ttu-id="9f303-p123">Различных типов отчетов возвращают различные уровни сведений. Сведения, доступные в различных отчетов описан в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="9f303-p123">The different report types return different levels of information. The information that's available in the different reports is described in the following sections.</span></span>

### <a name="summary-report-output"></a><span data-ttu-id="9f303-195">Сводный отчет по вывода</span><span class="sxs-lookup"><span data-stu-id="9f303-195">Summary report output</span></span>

<span data-ttu-id="9f303-196">После выполнения сообщения трассировки, результаты будут отображены, упорядоченные по убыванию даты и времени (последние первого).</span><span class="sxs-lookup"><span data-stu-id="9f303-196">After running the message trace, the results will be listed, sorted by descending date/time (most recent first).</span></span>

![Сводный отчет по результаты для трассировки сообщений в центре соответствия требованиям & безопасности](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

<span data-ttu-id="9f303-198">Сводный отчет содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="9f303-198">The summary report contains the following information:</span></span>

- <span data-ttu-id="9f303-199">**Дата**: Дата и время, когда сообщение было получено службой, пояса времени UTC.</span><span class="sxs-lookup"><span data-stu-id="9f303-199">**Date**: The date and time at which the message was received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="9f303-200">**Отправитель**: адрес электронной почты отправителя (*псевдоним*@*домена*).</span><span class="sxs-lookup"><span data-stu-id="9f303-200">**Sender**: The email address of the sender (*alias*@*domain*).</span></span>

- <span data-ttu-id="9f303-p124">**Получатель**: адрес электронной почты получателя или получателей. Для сообщений, отправленных нескольким получателям имеется одна строка для каждого получателя. Если получатель является группу рассылки, динамическая группа рассылки или группу безопасности с включенной поддержкой почты, группе будет первого получателя, и затем каждый член группы — в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="9f303-p124">**Recipient**: The email address of the recipient or recipients. For a message sent to multiple recipients, there's one line per recipient. If the recipient is a distribution group, dynamic distribution group, or mail-enabled security group, the group will be the first recipient, and then each member of the group is on a separate line.</span></span>

- <span data-ttu-id="9f303-204">**Тема**: сначала 256 символов сообщения **Тема:** поля.</span><span class="sxs-lookup"><span data-stu-id="9f303-204">**Subject**: The first 256 characters of the message's **Subject:** field.</span></span>

- <span data-ttu-id="9f303-205">**Состояние**: эти значения, которые описаны в разделе [состояние доставки](#delivery-status) .</span><span class="sxs-lookup"><span data-stu-id="9f303-205">**Status**: These values are described in the [Delivery status](#delivery-status) section.</span></span>

<span data-ttu-id="9f303-p125">По умолчанию первые 250 результаты, загрузки и будет доступна. При прокрутите список вниз, существует небольшое приостановить загрузка следующего пакета результаты. Вместо прокрутки, нажмите кнопку **загрузить все** для загрузки всех результатов не более 10 000.</span><span class="sxs-lookup"><span data-stu-id="9f303-p125">By default, the first 250 results are loaded and readily available. When you scroll down, there's a slight pause as the next batch of results are loaded. Instead of scrolling, you can click **Load all** to load all of the results up to a maximum of 10,000.</span></span>

<span data-ttu-id="9f303-209">Щелкните заголовок столбца для сортировки результатов на значения этого столбца в возрастающем или убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="9f303-209">You can click on the column headers to sort the results by the values in that column in ascending or descending order.</span></span>

<span data-ttu-id="9f303-210">Можно нажать кнопку **результатов фильтра** для фильтрации результатов по одному или нескольким столбцам.</span><span class="sxs-lookup"><span data-stu-id="9f303-210">You can click **Filter results** to filter the results by one or more columns.</span></span>

<span data-ttu-id="9f303-211">После выбора одного или нескольких строк, нажав кнопку **экспортировать результаты** и выберите **Экспорт всех результатов** **экспорта загрузить результаты**и **Экспортировать выбранный**можно экспортировать результаты.</span><span class="sxs-lookup"><span data-stu-id="9f303-211">You can export the results after you've selected one or more rows by clicking **Export results** and then selecting **Export all results**, **Export loaded results**, or **Export selected**.</span></span>

#### <a name="find-related-records-for-this-message"></a><span data-ttu-id="9f303-212">Поиск связанных записей для данного сообщения</span><span class="sxs-lookup"><span data-stu-id="9f303-212">Find related records for this message</span></span>

<span data-ttu-id="9f303-p126">Связанные сообщения записи являются записями, общими тот же идентификатор сообщения. Помните, что даже одного сообщения между двумя пользователями можно создать несколько записей. Число записей увеличивается, когда сообщения были затронуты расширения группы рассылки, пересылки, правила потока почты (также известной как правила транспорта), и т.д.</span><span class="sxs-lookup"><span data-stu-id="9f303-p126">Related message records are records that shared the same Message ID. Remember, even a single message sent between two people can generate multiple records. The number of records increases when the message is affected by distribution group expansion, forwarding, mail flow rules (also known as transport rules), etc.</span></span>

<span data-ttu-id="9f303-216">После выбора строки флажок связанных записей можно найти в сообщении, нажмите кнопку **найти связанные** , который отображается, или можно выбрать **Дополнительные параметры** ![дополнительные](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Поиск связанных записей для данного сообщения**).</span><span class="sxs-lookup"><span data-stu-id="9f303-216">After you select a row's check box, you can find related records for the message by clicking the **Find related** button that appears, or by selecting **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Find related records for this message**).</span></span>

<span data-ttu-id="9f303-217">Дополнительные сведения о идентификатор сообщения обратитесь к разделу идентификатор сообщения ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="9f303-217">For more information about the Message ID, see the Message ID section earlier in this topic.</span></span>

#### <a name="message-trace-details"></a><span data-ttu-id="9f303-218">Сведений трассировки</span><span class="sxs-lookup"><span data-stu-id="9f303-218">Message trace details</span></span>

<span data-ttu-id="9f303-219">В выходных данных сводный отчет можно просмотреть сведения о сообщение с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="9f303-219">In the summary report output, you can view details about a message by using either of the following methods:</span></span>

- <span data-ttu-id="9f303-220">Выберите строку (щелкните в любом месте строки, кроме флажок).</span><span class="sxs-lookup"><span data-stu-id="9f303-220">Select the row (click anywhere in the row except the check box).</span></span>

- <span data-ttu-id="9f303-221">Установите флажок строку и нажмите кнопку **Дополнительные параметры** ![дополнительные](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Просмотр сведений о сообщении**.</span><span class="sxs-lookup"><span data-stu-id="9f303-221">Select the row's check box and click **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **View message details**.</span></span>

   ![Сведения о после двойного щелчка строки в сводный отчет по результатов трассировки в центре соответствия требованиям & безопасности](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

<span data-ttu-id="9f303-223">Сведений трассировки содержат следующие дополнительные сведения, которого нет в сводный отчет.</span><span class="sxs-lookup"><span data-stu-id="9f303-223">The message trace details contain the following additional information that's not present in the summary report:</span></span>

- <span data-ttu-id="9f303-p127">**Сообщение события**: в этом разделе содержатся классификации строк, которые помогают классифицировать действия, которые служба начинает в сообщениях. Ниже указаны некоторые из наиболее интересных событий, которые могут возникать.</span><span class="sxs-lookup"><span data-stu-id="9f303-p127">**Message events**: This section contains classifications that help categorize the actions that the service takes on messages. Some of the more interesting events that you might encounter are:</span></span>

   - <span data-ttu-id="9f303-226">**Получения**: сообщение было получено службой.</span><span class="sxs-lookup"><span data-stu-id="9f303-226">**Receive**: The message was received by the service.</span></span>

   - <span data-ttu-id="9f303-227">**Отправка**: сообщение было отправлено службой.</span><span class="sxs-lookup"><span data-stu-id="9f303-227">**Send**: The message was sent by the service.</span></span>

   - <span data-ttu-id="9f303-228">**Сбой**: не удалось доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f303-228">**Fail**: The message failed to be delivered.</span></span>

   - <span data-ttu-id="9f303-229">**Предоставление**: сообщение было доставлено в почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="9f303-229">**Deliver**: The message was delivered to a mailbox.</span></span>

   - <span data-ttu-id="9f303-230">**Развернуть**: сообщение было отправлено в группу рассылки, которая была расширена.</span><span class="sxs-lookup"><span data-stu-id="9f303-230">**Expand**: The message was sent to a distribution group that was expanded.</span></span>

   - <span data-ttu-id="9f303-231">**Переключение**: из-за преобразования содержимого, ограничение числа получателей сообщения или агентов получатели были перемещены в раздвоенное сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f303-231">**Transfer**: Recipients were moved to a bifurcated message because of content conversion, message recipient limits, or agents.</span></span>

   - <span data-ttu-id="9f303-232">**Задержки**: доставка сообщений было отложено и может быть повторно попытка более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9f303-232">**Defer**: The message delivery was postponed and might be re-attempted later.</span></span>

   - <span data-ttu-id="9f303-p128">**Разрешено**: сообщения был перенаправлен на новый адрес получателя на основании поиска в Active Directory. В этом случае исходный адрес получателя отображается в отдельной строке в трассировке сообщений вместе с состоянием окончательный доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9f303-p128">**Resolved**: The message was redirected to a new recipient address based on an Active Directory look up. When this happens, the original recipient address is listed in a separate row in the message trace along with the final delivery status for the message.</span></span>

   <span data-ttu-id="9f303-235">Обратите внимание на то, что даже процедура сообщение успешно доставлено будет создавать несколько записей **событий** в трассировке сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f303-235">Note that even an uneventful message that's successfully delivered will generate multiple **Event** entries in the message trace.</span></span>

- <span data-ttu-id="9f303-236">**Дополнительные сведения**: в этом разделе содержатся следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="9f303-236">**More information**: This section contains the following details:</span></span>

   - <span data-ttu-id="9f303-p129">**Код сообщения**: это значение — это описано в разделе [Код сообщения](#message-id) ранее в этом разделе. Например `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="9f303-p129">**Message ID**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

   - <span data-ttu-id="9f303-239">**Размер сообщения**</span><span class="sxs-lookup"><span data-stu-id="9f303-239">**Message size**</span></span>

   - <span data-ttu-id="9f303-p130">**IP-адрес из**: IP-адрес компьютера, отправившего сообщение. Для исходящих сообщений, отправленных с Exchange Online это значение не задан.</span><span class="sxs-lookup"><span data-stu-id="9f303-p130">**From IP**: The IP address of the computer that sent the message. For outbound messages sent from Exchange Online, this value is blank.</span></span>

   - <span data-ttu-id="9f303-p131">**Для IP-адресов**: IP-адрес или адреса, где служба попытка доставки сообщения. Если сообщение имеет несколько получателей, они отображаются. Для входящих сообщений, отправляемых в Exchange Online это значение не задан.</span><span class="sxs-lookup"><span data-stu-id="9f303-p131">**To IP**: The IP address or addresses where the service attempted to deliver the message. If the message has multiple recipients, these are displayed. For inbound messages sent to Exchange Online, this value is blank.</span></span>

### <a name="enhanced-summary-reports"></a><span data-ttu-id="9f303-245">Усовершенствованные сводные отчеты о</span><span class="sxs-lookup"><span data-stu-id="9f303-245">Enhanced summary reports</span></span>

<span data-ttu-id="9f303-p132">Доступные (выполненных) улучшенной сводные отчеты о доступны в разделе **Downloadable отчетов** в начале Трассировка сообщений. Следующие сведения можно найти в отчете:</span><span class="sxs-lookup"><span data-stu-id="9f303-p132">Available (completed) Enhanced summary reports are available in the **Downloadable reports** section at the beginning message trace. The following information is available in the report:</span></span>

- <span data-ttu-id="9f303-248">**origin_timestamp**<sup>\*</sup>: Дата и время, когда сообщение было получено службой, пояса времени UTC изначально.</span><span class="sxs-lookup"><span data-stu-id="9f303-248">**origin_timestamp**<sup>\*</sup>: The date and time when the message was initially received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="9f303-249">**sender_address**: адрес электронной почты отправителя (*псевдоним*@*домена*).</span><span class="sxs-lookup"><span data-stu-id="9f303-249">**sender_address**: The sender's email address (*alias*@*domain*).</span></span>

- <span data-ttu-id="9f303-p133">**Recipient_status**: состояния доставки сообщения получателю. Если сообщение было отправлено нескольким получателям, оно будет отображаться всех получателей, а также соответствующие состояние для каждого из них, в формате: \< *адрес электронной почты*\>##\<*состояние*\>. Например:</span><span class="sxs-lookup"><span data-stu-id="9f303-p133">**Recipient_status**: The status of the delivery of the message to the recipient. If the message was sent to multiple recipients, it will show all the recipients and the corresponding status for each, in the format: \<*email address*\>##\<*status*\>. For example:</span></span>

   - <span data-ttu-id="9f303-253">**##Receive, отправка** означает, что сообщение было получено службой и отправлено в место назначения.</span><span class="sxs-lookup"><span data-stu-id="9f303-253">**##Receive, Send** means the message was received by the service and was sent to the intended destination.</span></span>

   - <span data-ttu-id="9f303-254">**Сбой ##Receive,** означает, что сообщение было получено службы, но доставки в место назначения не удалось.</span><span class="sxs-lookup"><span data-stu-id="9f303-254">**##Receive, Fail** means the message was received by the service but delivery to the intended destination failed.</span></span>

   - <span data-ttu-id="9f303-255">**##Receive, доставка** означает, что сообщение было получено службой и доставлено в почтовый ящик получателя.</span><span class="sxs-lookup"><span data-stu-id="9f303-255">**##Receive, Deliver** means the message was received by the service and was delivered to the recipient's mailbox.</span></span>

- <span data-ttu-id="9f303-256">**message_subject**: сначала 256 символов поле **темы** сообщения.</span><span class="sxs-lookup"><span data-stu-id="9f303-256">**message_subject**: The first 256 characters of the message's **Subject** field.</span></span>

- <span data-ttu-id="9f303-257">**total_bytes**: размер сообщения в байтах, включая вложения.</span><span class="sxs-lookup"><span data-stu-id="9f303-257">**total_bytes**: The size of the message in bytes, including attachments.</span></span>

- <span data-ttu-id="9f303-p134">**message_id**: это значение — это описано в разделе [Код сообщения](#message-id) ранее в этом разделе. Например `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="9f303-p134">**message_id**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

- <span data-ttu-id="9f303-p135">**network_message_id**: значение сообщения уникальный идентификатор, сохраняются для всех копий сообщений, который может быть создан из-за расширения группы рассылки или разветвление. Пример значения — это `1341ac7b13fb42ab4d4408cf7f55890f`.</span><span class="sxs-lookup"><span data-stu-id="9f303-p135">**network_message_id**: A unique message ID value that persists across all copies of the message that might be created due to bifurcation or distribution group expansion. An example value is `1341ac7b13fb42ab4d4408cf7f55890f`.</span></span>

- <span data-ttu-id="9f303-262">**original_client_ip**: IP-адрес клиента отправителя.</span><span class="sxs-lookup"><span data-stu-id="9f303-262">**original_client_ip**: The IP address of the sender's client.</span></span>

- <span data-ttu-id="9f303-263">**направление**: Указывает, является ли сообщение было отправлено входящим (1) или ли оно было отправлено исходящих (2) из вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9f303-263">**directionality**: Indicates whether the message was sent inbound (1) to your organization, or whether it was sent outbound (2) from your organization.</span></span>

- <span data-ttu-id="9f303-p136">**connector_id**: имя соединителя источника и назначения. Дополнительные сведения о соединителях в Exchange Online можно [настроить поток обработки почты с помощью соединителей в Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span><span class="sxs-lookup"><span data-stu-id="9f303-p136">**connector_id**: The name of the source or destination connector. For more information about connectors in Exchange Online, see [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span></span>

- <span data-ttu-id="9f303-266">**delivery_priority**<sup>\*</sup>: ли сообщение отправлено с **высоким**, **низким**или **обычным** приоритетом.</span><span class="sxs-lookup"><span data-stu-id="9f303-266">**delivery_priority**<sup>\*</sup>: Whether the message was sent with **High**, **Low**, or **Normal** priority.</span></span>

<span data-ttu-id="9f303-267"><sup>\*</sup>Эти свойства доступны только в сводные отчеты о улучшенной.</span><span class="sxs-lookup"><span data-stu-id="9f303-267"><sup>\*</sup>These properties are only available in Enhanced summary reports.</span></span>

### <a name="extended-reports"></a><span data-ttu-id="9f303-268">Расширенные отчеты</span><span class="sxs-lookup"><span data-stu-id="9f303-268">Extended reports</span></span>

<span data-ttu-id="9f303-p137">Доступные отчеты Extended (выполненных) доступны в разделе **Downloadable отчетов** в начале трассировки. Практически все сведения из сводного отчета по улучшенной доступна в отчет об Extended (за исключением **origin_timestamp** и **delivery_priority**). Следующие дополнительные сведения доступен только в отчет об Extended:</span><span class="sxs-lookup"><span data-stu-id="9f303-p137">Available (completed) Extended reports are available in the **Downloadable reports** section at the beginning of message trace. Virtually all of the information from an Enhanced summary report is available in an Extended report (with the exception of **origin_timestamp** and **delivery_priority**). The following additional information is only available in an Extended report:</span></span>

- <span data-ttu-id="9f303-272">**client_ip**: IP-адрес сервера электронной почты или обмена мгновенными сообщениями клиента, отправившего сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f303-272">**client_ip**: The IP address of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="9f303-273">**client_hostname**: имя узла или полное доменное имя сервера электронной почты или обмена мгновенными сообщениями клиента, отправившего сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f303-273">**client_hostname**: The host name or FQDN of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="9f303-274">**server_ip**: IP-адрес сервера источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="9f303-274">**server_ip**: The IP address of the source or destination server.</span></span>

- <span data-ttu-id="9f303-275">**server_hostname**: имя узла или полное доменное имя сервера на целевой сервер.</span><span class="sxs-lookup"><span data-stu-id="9f303-275">**server_hostname**: The host name or FQDN of the destination server.</span></span>

- <span data-ttu-id="9f303-p138">**source_context**: Дополнительные сведения, связанные с **исходного** поля. Например:</span><span class="sxs-lookup"><span data-stu-id="9f303-p138">**source_context**: Extra information associated with the **source** field. For example:</span></span>

   - `Protocol Filter Agent`

   - `3489061114359050000`

- <span data-ttu-id="9f303-p139">**источник**: Exchange Online компонент, который несет ответственность за событие. Например:</span><span class="sxs-lookup"><span data-stu-id="9f303-p139">**source**: The Exchange Online component that's responsible for the event. For example:</span></span>

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- <span data-ttu-id="9f303-280">**код_события**: они соответствуют значениям **сообщения события** , которые описаны в разделе [Поиск связанных записей для данного сообщения](#find-related-records-for-this-message) .</span><span class="sxs-lookup"><span data-stu-id="9f303-280">**event_id**: These correspond to the **Message event** values that are explained in the [Find related records for this message](#find-related-records-for-this-message) section.</span></span>

- <span data-ttu-id="9f303-281">**internal_message_id**: идентификатор сообщения, назначенный сервером Exchange Online, который в данный момент обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="9f303-281">**internal_message_id**: A message identifier that's assigned by the Exchange Online server that's currently processing the message.</span></span>

- <span data-ttu-id="9f303-p140">**recipient_address**: адреса получателей сообщения электронной почты. Несколько адресов электронной почты, разделенных знаком точки с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="9f303-p140">**recipient_address**: The email addresses of the message's recipients. Multiple email addresses are separated by the semicolon character (;).</span></span>

- <span data-ttu-id="9f303-284">**recipient_count**: общее число получателей в сообщении.</span><span class="sxs-lookup"><span data-stu-id="9f303-284">**recipient_count**: The total number of recipients in the message.</span></span>

- <span data-ttu-id="9f303-285">**related_recipient_address**: использовать совместно с `EXPAND`, `REDIRECT`, и `RESOLVE` событий для отображения получателей электронной почты адреса, связанные с сообщением.</span><span class="sxs-lookup"><span data-stu-id="9f303-285">**related_recipient_address**: Used with `EXPAND`, `REDIRECT`, and `RESOLVE` events to display other recipient email addresses that are associated with the message.</span></span>

- <span data-ttu-id="9f303-p141">**Справочник по**: в этом поле содержит дополнительные сведения для конкретных типов событий. Например:</span><span class="sxs-lookup"><span data-stu-id="9f303-p141">**reference**: This field contains additional information for specific types of events. For example:</span></span>

   - <span data-ttu-id="9f303-p142">**Уведомления о Доставке**: содержит ссылки на отчет, равный значению **message_id** из связанной уведомление о состоянии доставки (также известной как уведомления о Доставке, отчет о недоставке, отчет о Недоставке или сообщение о возврате), если имя источника данных создается после этого события. Если это сообщение уведомления о Доставке, это поле содержит значение **message_id** исходного сообщения, для создания источника данных.</span><span class="sxs-lookup"><span data-stu-id="9f303-p142">**DSN**: Contains the report link, which is the **message_id** value of the associated delivery status notification (also known as a DSN, non-delivery report, NDR, or bounce message) if a DSN is generated subsequent to this event. If this is a DSN message, this field contains the **message_id** value of the original message that the DSN was generated for.</span></span>

   - <span data-ttu-id="9f303-290">**РАЗВЕРНУТЬ**: содержит значение **related_recipient_address** сообщений, связанных с ними.</span><span class="sxs-lookup"><span data-stu-id="9f303-290">**EXPAND**: Contains the **related_recipient_address** value of the related messages.</span></span>

   - <span data-ttu-id="9f303-291">**Получения**: может содержать значение **message_id** связанные сообщения, если сообщение был создан для других процессов (например, правила папки "Входящие").</span><span class="sxs-lookup"><span data-stu-id="9f303-291">**RECEIVE**: Might contain the **message_id** value of the related message if the message was generated by other processes (for example, Inbox rules).</span></span>

   - <span data-ttu-id="9f303-292">**ОТПРАВКА**: содержит значение **internal_message_id** все уведомления о Доставке сообщения.</span><span class="sxs-lookup"><span data-stu-id="9f303-292">**SEND**: Contains the **internal_message_id** value of any DSN messages.</span></span>

   - <span data-ttu-id="9f303-293">**ПЕРЕКЛЮЧЕНИЕ**: содержит значение **internal_message_id** сообщения, разделенными (например, путем преобразования содержимого, ограничение числа получателей сообщения или агенты).</span><span class="sxs-lookup"><span data-stu-id="9f303-293">**TRANSFER**: Contains the **internal_message_id** value of the message that's being forked (for example, by content conversion, message recipient limits, or agents).</span></span>

   - <span data-ttu-id="9f303-294">**MAILBOXRULE**: содержит значение **internal_message_id** входящего сообщения, которое вызвало правила папки «Входящие» для создания исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f303-294">**MAILBOXRULE**: Contains the **internal_message_id** value of the inbound message that caused the Inbox rule to generate the outbound message.</span></span>

   <span data-ttu-id="9f303-295">Для событий других типов это поле обычно не заполняется.</span><span class="sxs-lookup"><span data-stu-id="9f303-295">For other types of events, this field is usually blank.</span></span>

- <span data-ttu-id="9f303-p143">**return_path**: адрес возврата электронной почты, указанный с помощью команды **MAIL FROM** , отправившего сообщение. Несмотря на то, что это поле никогда не является пустым, он может иметь значение null отправителя адрес, представленные в виде `<>`.</span><span class="sxs-lookup"><span data-stu-id="9f303-p143">**return_path**: The return email address specified by the **MAIL FROM** command that sent the message. Although this field is never empty, it can have the null sender address value represented as `<>`.</span></span>

- <span data-ttu-id="9f303-p144">**message_info**: Дополнительные сведения о сообщении. Например:</span><span class="sxs-lookup"><span data-stu-id="9f303-p144">**message_info**: Additional information about the message. For example:</span></span>

   - <span data-ttu-id="9f303-p145">Дата время отправки сообщения в формате UTC для `DELIVER` и `SEND` события. Дата и время возникновения — это время, если сообщение впервые введена в организацию Exchange Online. Дата время в формате UTC представлен в формате даты и времени ISO 8601: `yyyy-mm-ddThh:mm:ss.fffZ`, где `yyyy` = год, `mm` = месяц, `dd` = день, `T` начало компонент времени `hh` = час, `mm` = минуты, `ss` = секунды, `fff` = доли секунды, и `Z` означает `Zulu`, которая является другим способом для обозначения UTC.</span><span class="sxs-lookup"><span data-stu-id="9f303-p145">The message origination date-time in UTC for `DELIVER` and `SEND` events. The origination date-time is the time when the message first entered the Exchange Online organization. The UTC date-time is represented in the ISO 8601 date-time format: `yyyy-mm-ddThh:mm:ss.fffZ`, where `yyyy` = year, `mm` = month, `dd` = day, `T` indicates the beginning of the time component, `hh` = hour, `mm` = minute, `ss` = second, `fff` = fractions of a second, and `Z` signifies `Zulu`, which is another way to denote UTC.</span></span>

   - <span data-ttu-id="9f303-p146">Ошибки проверки подлинности. Например, вы можете увидеть значение `11a` и тип проверки подлинности, который использовался при возникновении ошибки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9f303-p146">Authentication errors. For example, you might see the value `11a` and the type of authentication that was used when the authentication error occurred.</span></span>

- <span data-ttu-id="9f303-305">**tenant_id**: идентификатор GUID, который представляет организацию Exchange Online (например, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span><span class="sxs-lookup"><span data-stu-id="9f303-305">**tenant_id**: A GUID value that represents the Exchange Online organization (for example, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span></span>

- <span data-ttu-id="9f303-306">**original_server_ip**: IP-адрес исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="9f303-306">**original_server_ip**: The IP address of the original server.</span></span>

- <span data-ttu-id="9f303-p147">**custom_data**: содержит данные, связанные с типами определенных событий. Дополнительные сведения см в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="9f303-p147">**custom_data**: Contains data related to specific event types. For more information, see the following sections.</span></span>

#### <a name="customdata-values"></a><span data-ttu-id="9f303-309">значения custom_data</span><span class="sxs-lookup"><span data-stu-id="9f303-309">custom_data values</span></span>

<span data-ttu-id="9f303-p148">Поле **custom_data** для `AGENTINFO` событие используется по-разному Exchange Online агентам для записи в журнал подробные сведения об обработке сообщений. Некоторые из наиболее интересных агенты описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="9f303-p148">The **custom_data** field for an `AGENTINFO` event is used by a variety of Exchange Online agents to log message processing details. Some of the more interesting agents are described in the following sections.</span></span>

#### <a name="spam-filter-agent"></a><span data-ttu-id="9f303-312">Агент фильтра нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="9f303-312">Spam filter agent</span></span>

<span data-ttu-id="9f303-p149">Значение **custom_data** , начинается с `S:SFA` от агента фильтрации нежелательной почты. В следующей таблице описываются основные сведения о:</span><span class="sxs-lookup"><span data-stu-id="9f303-p149">A **custom_data** value that starts with `S:SFA` is from the spam filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="9f303-315">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9f303-315">**Value**</span></span>|<span data-ttu-id="9f303-316">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f303-316">**Description**</span></span>|
|:-----|:-----|
|`SFV=NSPM`|<span data-ttu-id="9f303-317">Сообщение помечено как не являющееся нежелательным и отправлено указанным получателям.</span><span class="sxs-lookup"><span data-stu-id="9f303-317">The message was marked as non-spam and was sent to the intended recipients.</span></span>|
|`SFV=SPM`|<span data-ttu-id="9f303-318">Сообщение помечено фильтром содержимого как нежелательное.</span><span class="sxs-lookup"><span data-stu-id="9f303-318">The message was marked as spam by the content filter.</span></span>|
|`SFV=BLK`|<span data-ttu-id="9f303-319">Фильтрация была пропущена, а сообщение было заблокировано, так как оно исходило от заблокированного отправителя.</span><span class="sxs-lookup"><span data-stu-id="9f303-319">Filtering was skipped and the message was blocked because it originated from a blocked sender.</span></span>|
|`SFV=SKS`|<span data-ttu-id="9f303-p150">Сообщение помечено как нежелательное до обработки фильтром содержимого. Это применяется к сообщениям, в которых сообщение сопоставлено с правилом транспорта автоматически помечать его как нежелательное и обходить любую дополнительную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="9f303-p150">The message was marked as spam prior to being processed by the content filter. This includes messages where the message matched a Transport rule to automatically mark it as spam and bypass all additional filtering.</span></span>|
|`SCL=<number>`|<span data-ttu-id="9f303-322">Дополнительные сведения о различных значениях вероятности нежелательной почты и их значении см. в разделе [Вероятность нежелательной почты](https://technet.microsoft.com/library/jj200686.aspx).  </span><span class="sxs-lookup"><span data-stu-id="9f303-322">For more information about the different SCL values and what they mean, see [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`PCL=<number>`|<span data-ttu-id="9f303-p151">Значение вероятности фишинга для сообщения. Эти значения можно интерпретировать так же, как и значения SCL, которые задокументированы в [Вероятность нежелательной почты](https://technet.microsoft.com/library/jj200686.aspx).  </span><span class="sxs-lookup"><span data-stu-id="9f303-p151">The Phishing Confidence Level (PCL) value of the message. These can be interpreted the same way as the SCL values documented in [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`DI=SB`|<span data-ttu-id="9f303-325">Отправитель сообщения заблокирован.</span><span class="sxs-lookup"><span data-stu-id="9f303-325">The sender of the message was blocked.</span></span>|
|`DI=SQ`|<span data-ttu-id="9f303-326">Сообщение перемещено в карантин.</span><span class="sxs-lookup"><span data-stu-id="9f303-326">The message was quarantined.</span></span>|
|`DI=SD`|<span data-ttu-id="9f303-327">Сообщение удалено.</span><span class="sxs-lookup"><span data-stu-id="9f303-327">The message was deleted.</span></span>|
|`DI=SJ`|<span data-ttu-id="9f303-328">Сообщение отправлено в папку нежелательной почты получателя.</span><span class="sxs-lookup"><span data-stu-id="9f303-328">The message was sent to the recipient's Junk Email folder.</span></span>|
|`DI=SN`|<span data-ttu-id="9f303-p152">Сообщение перенаправлено через пул доставки высокого риска. Дополнительные сведения см в [пул высокого риска доставки для исходящих сообщений](https://technet.microsoft.com/library/jj200746.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f303-p152">The message was routed through the higher risk delivery pool. For more information, see [High-risk delivery pool for outbound messages](https://technet.microsoft.com/library/jj200746.aspx).</span></span>|
|`DI=SO`|<span data-ttu-id="9f303-331">Сообщение перенаправлено через пул обычной исходящей доставки.</span><span class="sxs-lookup"><span data-stu-id="9f303-331">The message was routed through the normal outbound delivery pool.</span></span>|
|<span data-ttu-id="9f303-332">"SFS = []</span><span class="sxs-lookup"><span data-stu-id="9f303-332">\`SFS=[a]</span></span>|<span data-ttu-id="9f303-333">SFS = [b] "</span><span class="sxs-lookup"><span data-stu-id="9f303-333">SFS=[b]\`</span></span>|<span data-ttu-id="9f303-334">Это означает выполнение правил нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="9f303-334">This denotes that spam rules were matched.</span></span>|
|`IPV=CAL`|<span data-ttu-id="9f303-335">Сообщение пропущено через фильтр нежелательной почты, поскольку IP-адрес указан в списке разрешенных IP-адресов в фильтре подключений.</span><span class="sxs-lookup"><span data-stu-id="9f303-335">The message was allowed through the spam filters because the IP address was specified in an IP Allow list in the connection filter.</span></span>|
|`H=<EHLOstring>`|<span data-ttu-id="9f303-336">Строка HELO или EHLO подключающегося сервера электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f303-336">The HELO or EHLO string of the connecting email server.</span></span>|
|`PTR=<ReverseDNS>`|<span data-ttu-id="9f303-337">Запись PTR отправляющего IP-адреса, называемая также обратным DNS-адресом.</span><span class="sxs-lookup"><span data-stu-id="9f303-337">The PTR record of the sending IP address, also known as the reverse DNS address.</span></span>|

<span data-ttu-id="9f303-338">Пример **custom_data** значения для сообщение, в котором выполняется фильтрация нежелательной почты следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9f303-338">An example **custom_data** value for a message that's filtered for spam like this:</span></span>

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a><span data-ttu-id="9f303-339">Агент фильтра вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="9f303-339">Malware filter agent</span></span>

<span data-ttu-id="9f303-p153">Значение **custom_data** , начинается с `S:AMA` от агента фильтрации вредоносных программ. В следующей таблице описываются основные сведения о:</span><span class="sxs-lookup"><span data-stu-id="9f303-p153">A **custom_data** value that starts with `S:AMA` is from the malware filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="9f303-342">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9f303-342">**Value**</span></span>|<span data-ttu-id="9f303-343">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f303-343">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f303-344">"AMA = СУММ</span><span class="sxs-lookup"><span data-stu-id="9f303-344">\`AMA=SUM</span></span>|<span data-ttu-id="9f303-345">v = 1</span><span class="sxs-lookup"><span data-stu-id="9f303-345">v=1</span></span>|<span data-ttu-id="9f303-346">` or `AMA = EV</span><span class="sxs-lookup"><span data-stu-id="9f303-346">` or `AMA=EV</span></span>|<span data-ttu-id="9f303-347">v = 1"</span><span class="sxs-lookup"><span data-stu-id="9f303-347">v=1\`</span></span>|<span data-ttu-id="9f303-p154">Сообщение было определено вредоносная программа. `SUM` указывает вредоносная программа может был обнаружен любое количество ядер. `EV` указывает, определенного ядром обнаружена вредоносная программа. При обнаружении вредоносной программы обработчиком что это запускает последующие действия.</span><span class="sxs-lookup"><span data-stu-id="9f303-p154">The message was determined to contain malware. `SUM` indicates the malware could've been detected by any number of engines. `EV` indicates the malware was detected by a specific engine. When malware is detected by an engine this triggers the subsequent actions.</span></span>|
|`Action=r`|<span data-ttu-id="9f303-352">Сообщение заменено.</span><span class="sxs-lookup"><span data-stu-id="9f303-352">The message was replaced.</span></span>|
|`Action=p`|<span data-ttu-id="9f303-353">Сообщение не проходило фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="9f303-353">The message was bypassed.</span></span>|
|`Action=d`|<span data-ttu-id="9f303-354">Сообщение отложено.</span><span class="sxs-lookup"><span data-stu-id="9f303-354">The message was deferred.</span></span>|
|`Action=s`|<span data-ttu-id="9f303-355">Сообщение удалено.</span><span class="sxs-lookup"><span data-stu-id="9f303-355">The message was deleted.</span></span>|
|`Action=st`|<span data-ttu-id="9f303-356">Сообщение не проходило фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="9f303-356">The message was bypassed.</span></span>|
|`Action=sy`|<span data-ttu-id="9f303-357">Сообщение не проходило фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="9f303-357">The message was bypassed.</span></span>|
|`Action=ni`|<span data-ttu-id="9f303-358">Сообщение отклонено.</span><span class="sxs-lookup"><span data-stu-id="9f303-358">The message was rejected.</span></span>|
|`Action=ne`|<span data-ttu-id="9f303-359">Сообщение отклонено.</span><span class="sxs-lookup"><span data-stu-id="9f303-359">The message was rejected.</span></span>|
|`Action=b`|<span data-ttu-id="9f303-360">Сообщение заблокировано.</span><span class="sxs-lookup"><span data-stu-id="9f303-360">The message was blocked.</span></span>|
|`Name=<malware>`|<span data-ttu-id="9f303-361">Имя обнаруженной вредоносной программы.</span><span class="sxs-lookup"><span data-stu-id="9f303-361">The name of the malware that was detected.</span></span>|
|`File=<filename>`|<span data-ttu-id="9f303-362">Имя файла, содержащего вредоносные программы.</span><span class="sxs-lookup"><span data-stu-id="9f303-362">The name of the file that contained the malware.</span></span>|

<span data-ttu-id="9f303-363">Пример значения **custom_data** для сообщения, содержащего вредоносные программы выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9f303-363">An example **custom_data** value for a message that contains malware looks like this:</span></span>

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a><span data-ttu-id="9f303-364">Агент правил транспорта</span><span class="sxs-lookup"><span data-stu-id="9f303-364">Transport rule agent</span></span>

<span data-ttu-id="9f303-p155">Значение **custom_data** , начинается с`S:TRA` от агента правил транспорта для правил потока обработки почты (также известной как правила транспорта). В следующей таблице описываются основные сведения о:</span><span class="sxs-lookup"><span data-stu-id="9f303-p155">A **custom_data** value that starts with`S:TRA` is from the transport rule agent for mail flow rules (also known as transport rules). The key details are described in the following table:</span></span>

|<span data-ttu-id="9f303-367">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9f303-367">**Value**</span></span>|<span data-ttu-id="9f303-368">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f303-368">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f303-369">"ETR</span><span class="sxs-lookup"><span data-stu-id="9f303-369">\`ETR</span></span>|<span data-ttu-id="9f303-370">ruleId =<guid>\`</span><span class="sxs-lookup"><span data-stu-id="9f303-370">ruleId=<guid>\`</span></span>|<span data-ttu-id="9f303-371">Выполнено правило идентификатора.</span><span class="sxs-lookup"><span data-stu-id="9f303-371">The rule ID that was matched.</span></span>|
|`St=<datetime>`|<span data-ttu-id="9f303-372">Дата и время в формате UTC, при возникновении соответствующие правила.</span><span class="sxs-lookup"><span data-stu-id="9f303-372">The date and time in UTC when the rule match occurred.</span></span>|
|`Action=<ActionDefinition>`|<span data-ttu-id="9f303-p156">Действие, которая была применена. Список доступных действий в разделе [поток обработки почты действия правил в Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span><span class="sxs-lookup"><span data-stu-id="9f303-p156">The action that was applied. For a list of available actions, see [Mail flow rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span></span>|
|`Mode=<Mode>`|<span data-ttu-id="9f303-p157">Режим правило. Допустимыми значениями являются:</span><span class="sxs-lookup"><span data-stu-id="9f303-p157">The mode of the rule. Valid values are: </span></span><br/><span data-ttu-id="9f303-377">• **Enforce**: все действия правила используются принудительно.</span><span class="sxs-lookup"><span data-stu-id="9f303-377">• **Enforce**: All actions on the rule will be enforced.</span></span> <br/><span data-ttu-id="9f303-378">• **Тест с подсказками политики:**: все действия правила отправляются, но другие принудительные действия не применяются на.</span><span class="sxs-lookup"><span data-stu-id="9f303-378">• **Test with Policy Tips:**: Any Policy Tip actions will be sent, but other enforcement actions will not be acted on.</span></span> <br/><span data-ttu-id="9f303-379">• **Test without Policy Tips**: действия перечисляются в файле журнала, но отправители не получают никаких уведомлений и принудительные действия не применяются на.</span><span class="sxs-lookup"><span data-stu-id="9f303-379">• **Test without Policy Tips**: Actions will be listed in a log file, but senders will not be notified in any way, and enforcement actions will not be acted on.</span></span>|

<span data-ttu-id="9f303-380">Пример значения **custom_data** для сообщений, которая соответствует условиям правила потока обработки почты выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9f303-380">An example **custom_data** value for a messages that matches the conditions of a mail flow rule looks like this:</span></span>

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
