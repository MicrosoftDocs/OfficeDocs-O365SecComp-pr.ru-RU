---
title: Дополнительные параметры фильтрации нежелательной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/26/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: b286f853-b484-4af0-b01f-281fffd85e7a
description: Параметры фильтрации нежелательной почты дополнительно позволяют администраторам изучить различные атрибуты содержимого сообщения. Сведения о присутствии этих атрибутов в сообщении увеличивает показатель нежелательной почты для сообщения (тем самым повышая вероятность его помечаются как нежелательная почта) или помечает сообщение как нежелательная почта. Параметры ASF предназначенных для определенного сообщения свойства, такие как теги HTML и перенаправления URL-адреса, которые обычно находятся в нежелательных сообщений.
ms.openlocfilehash: 4b67c3a9a79c4a51bdebed5ca1a6415cc7bd13ae
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026576"
---
# <a name="advanced-spam-filtering--options"></a><span data-ttu-id="ea46a-105">Дополнительные параметры фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="ea46a-105">Advanced spam filtering  options</span></span>

<span data-ttu-id="ea46a-p102">Параметры фильтрации нежелательной почты дополнительно позволяют администраторам изучить различные атрибуты содержимого сообщения. Сведения о присутствии этих атрибутов в сообщении увеличивает показатель нежелательной почты для сообщения (тем самым повышая вероятность его помечаются как нежелательная почта) или помечает сообщение как нежелательная почта. Параметры ASF предназначенных для определенного сообщения свойства, такие как теги HTML и перенаправления URL-адреса, которые обычно находятся в нежелательных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p102">Advanced spam filtering  options give administrators the ability to inspect various content attributes of a message. The presence of these attributes in a message either increases the spam score of the message (thereby increasing the potential for it to be identified as spam) or marks the message as spam. The ASF options target specific message properties, such as HTML tags and URL redirection, which are commonly found in spam messages.</span></span>
  
<span data-ttu-id="ea46a-p103">Включение параметров ASF является агрессивным подходом к фильтрации нежелательной почты, и никакие отфильтрованные ими сообщения нельзя указать как ложное срабатывание. Эти сообщения можно идентифицировать путем периодических уведомлений пользователя о спаме и восстановить из карантина нежелательной почты. Их также можно определить по тексту заголовка X, который зависит от параметров ASF и отображается в заголовке Интернета сообщений, для которых обнаружено совпадение с параметром ASF. Дополнительные сведения см. в статье [Заголовки сообщений по защите от нежелательной почты](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="ea46a-p103">Enabling ASF options is an aggressive approach to spam filtering, and any messages that are filtered by these options cannot be reported as false positives. These messages can be identified through periodic end-user spam notifications and salvaged from the spam quarantine. They can also be identified via the X-header text that's specific to each ASF option and which appear in the Internet header of messages where an ASF option has been matched. For more information, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  
<span data-ttu-id="ea46a-p104">Параметры ASF можно включить, выключить или использовать в тестовом режиме при редактировании политик фильтрации содержимого. Дополнительные сведения см. в статье [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Тестовый режим недоступен для параметра **Подложное уведомление о недоставленном сообщении**, **Запись инфраструктуры политики отправителей: серьезный сбой**, **Условная фильтрация идентификатора отправителя: серьезный сбой** и **Массовая рассылка**.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p104">ASF options can be set on, off, or to test mode when you edit your content filter policies. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). Test mode is not available for the **NDR backscatter**, **SPF record: hard fail**, **Conditional Sender ID filtering: hard fail**, and **Bulk mail** options.</span></span> 
  
> [!TIP]
>  <span data-ttu-id="ea46a-p105">Рассмотрите возможность включения параметров ASF в тестовом режиме, чтобы усилить блокирование нежелательной почты, на основании своей среды. Мы рекомендуем клиентам, у которых определенные параметры ASF показывают высокие проценты нежелательной почты, протестировать такие параметры, прежде чем использовать их в производственной среде. >  Организациям, которые беспокоятся о фишинге, рекомендуется включить **запись инфраструктуры политики отправителей: серьезный сбой**.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p105">Consider enabling your ASF options in test mode in order to maximize spam blocking based upon your environment. For customers with high spam percentages for specific ASF options, we recommend that you test these options first before implementing them in your production environment. >  It's recommended that organizations who are concerned about phishing turn on the **SPF record: hard fail** option.</span></span> 
  
<span data-ttu-id="ea46a-119">В следующей таблице описан каждый параметр расширенной фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="ea46a-119">The following table describes each advanced spam filtering option.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="ea46a-120">**Параметр расширенной фильтрации нежелательной почты**</span><span class="sxs-lookup"><span data-stu-id="ea46a-120">**Advanced Spam Filtering Option**</span></span> <br/> |<span data-ttu-id="ea46a-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea46a-121">**Description**</span></span> <br/> |<span data-ttu-id="ea46a-122">**Текст заголовка X**</span><span class="sxs-lookup"><span data-stu-id="ea46a-122">**X-header text**</span></span> <br/> |
|<span data-ttu-id="ea46a-123">**Раздел "Увеличение показателя нежелательной почты"**</span><span class="sxs-lookup"><span data-stu-id="ea46a-123">**Increase Spam Score Section**</span></span> <br/> |<span data-ttu-id="ea46a-p106">Если эти параметры включены, они устанавливают вероятность нежелательной почты соответствующего сообщения равную 5 или 6, т. е. оно предположительно относится к нежелательной почте. Действие, выполняемое с сообщением, соответствует параметру **Нежелательная почта** политики фильтрации содержимого.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-p106">When enabled, these options set the spam confidence level (SCL) of a matched message to 5 or 6, which is considered suspected spam. The action performed on the message will match the **Spam** setting in your content filter policy.  </span></span><br/> ||
|<span data-ttu-id="ea46a-126">ссылки на рисунки с удаленных сайтов</span><span class="sxs-lookup"><span data-stu-id="ea46a-126">Image links to remote sites</span></span>  <br/> |<span data-ttu-id="ea46a-127">Если этот параметр включен, любому сообщению с HTML-содержимым с тегом IMG, обеспечивающим удаленную связь (например, с использованием HTTP), будет присвоен повышенный показатель нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="ea46a-127">When this setting is enabled, any message with HTML content that has an IMG tag that links remotely (for example, using http) will receive an increased spam score.</span></span>  <br/> |<span data-ttu-id="ea46a-128">X-CustomSpam: ссылки на рисунки с удаленных сайтов</span><span class="sxs-lookup"><span data-stu-id="ea46a-128">X-CustomSpam: Image links to remote sites</span></span>  <br/> |
|<span data-ttu-id="ea46a-129">Числовой IP-адрес в URL-адресе</span><span class="sxs-lookup"><span data-stu-id="ea46a-129">Numeric IP address in URL</span></span>  <br/> |<span data-ttu-id="ea46a-130">У сообщений, содержащих числовой URL-адрес (как правило, в виде IP-адреса), повысится показатель нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="ea46a-130">When this setting is enabled, any message that has numeric-based URLs (most often in the form of an IP address) will receive an increased spam score.</span></span>  <br/> |<span data-ttu-id="ea46a-131">X-CustomSpam: числовой IP-адрес в URL-адресе</span><span class="sxs-lookup"><span data-stu-id="ea46a-131">X-CustomSpam: Numeric IP in URL</span></span>  <br/> |
|<span data-ttu-id="ea46a-132">перенаправление URL-адреса на другой порт</span><span class="sxs-lookup"><span data-stu-id="ea46a-132">URL redirect to other port</span></span>  <br/> |<span data-ttu-id="ea46a-133">У сообщений, содержащих гиперссылку, которая перенаправляет пользователя на порт, отличный от порта 80 (обычный порт протокола HTTP), 8080 (альтернативный HTTP-порт) или 443 (HTTPS-порт), повысится показатель нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="ea46a-133">When this setting is enabled, any message that contains a hyperlink that redirects the user to ports other than port 80 (regular HTTP protocol port), 8080 (HTTP alternate port), or 443 (HTTPS port) will receive an increased spam score.</span></span>  <br/> |<span data-ttu-id="ea46a-134">X-CustomSpam: перенаправление URL-адреса на другой порт</span><span class="sxs-lookup"><span data-stu-id="ea46a-134">X-CustomSpam: URL redirect to other port</span></span>  <br/> |
|<span data-ttu-id="ea46a-135">URL-адрес сайта в домене .biz или .info</span><span class="sxs-lookup"><span data-stu-id="ea46a-135">URL to .biz or .info websites</span></span>  <br/> |<span data-ttu-id="ea46a-136">У сообщений, в тексте которых содержится расширение .biz или .info, повысится показатель нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="ea46a-136">When this setting is enabled, any message that contains a .biz or .info extension in the body of a message will receive an increased spam score.</span></span>  <br/> |<span data-ttu-id="ea46a-137">X-CustomSpam: URL-адрес сайта в домене .biz или .info</span><span class="sxs-lookup"><span data-stu-id="ea46a-137">X-CustomSpam: URL to .biz or .info websites</span></span>  <br/> |
|<span data-ttu-id="ea46a-138">**Раздел "Пометка в качестве нежелательной почты"**</span><span class="sxs-lookup"><span data-stu-id="ea46a-138">**Mark as Spam Section**</span></span> <br/> |<span data-ttu-id="ea46a-p107">Если эти параметры включены, они устанавливают вероятность нежелательной почты соответствующего сообщения равную 9, что соответствует нежелательной почте. Действие, выполняемое с сообщением, соответствует параметру **Нежелательное сообщение высокого уровня** политики фильтрации содержимого.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-p107">When enabled, these options set the spam confidence level (SCL) of a matched message to 9, which is considered certain spam. The action performed on the message will match the **High confidence spam** setting in your content filter policy.  </span></span><br/> ||
|<span data-ttu-id="ea46a-141">Пустые сообщения</span><span class="sxs-lookup"><span data-stu-id="ea46a-141">Empty messages</span></span>  <br/> |<span data-ttu-id="ea46a-142">Все сообщения, у которых отсутствует тема, текст и вложения, будут помечены как нежелательные.</span><span class="sxs-lookup"><span data-stu-id="ea46a-142">When this setting is enabled, any message in which the body and subject line are both empty, and which also has no attachment, will be marked as spam.</span></span>  <br/> |<span data-ttu-id="ea46a-143">X-CustomSpam: пустое сообщение</span><span class="sxs-lookup"><span data-stu-id="ea46a-143">X-CustomSpam: Empty Message</span></span>  <br/> |
|<span data-ttu-id="ea46a-144">JavaScript или VBScript в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-144">JavaScript or VBScript in HTML</span></span>  <br/> |<span data-ttu-id="ea46a-p108">Все сообщения, в которых используется JavaScript или Visual Basic Script в формате HTML, будут помечены как нежелательные. Оба эти языка сценариев используются в HTML-сообщении для вызова определенного действия. Браузер анализирует и обрабатывает сценарий вместе с остальной частью документа.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p108">When this setting is enabled, any message that uses JavaScript or Visual Basic Script Edition in HTML will be marked as spam. Both of these scripting languages are used within an HTML message to automatically cause a specific action to occur. The browser will parse and process the script along with the rest of the document.</span></span>  <br/> |<span data-ttu-id="ea46a-148">X-CustomSpam: теги JavaScript или VBScript в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-148">X-CustomSpam: Javascript or VBscript tags in HTML</span></span>  <br/> |
|<span data-ttu-id="ea46a-149">Теги Frame или IFrame в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-149">Frame or IFrame tags in HTML</span></span>  <br/> |<span data-ttu-id="ea46a-p109">Все сообщения, содержащие HTML-теги \<Frame\> или \<IFrame\>, будут помечены как нежелательные. Эти теги используются на веб-сайтах или в HTML-сообщениях для форматирования страницы с целью отображения текста или графических изображений.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p109">When this setting is enabled, any message that contains the \<Frame\> or \<IFrame\> HTML tag will be marked as spam. These tags are used on websites or in HTML messages to format the page for displaying text or graphics.</span></span>  <br/> |<span data-ttu-id="ea46a-152">X-CustomSpam: IFRAME или FRAME в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-152">X-CustomSpam: IFRAME or FRAME in HTML</span></span>  <br/> |
|<span data-ttu-id="ea46a-153">Теги Object в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-153">Object tags in HTML</span></span>  <br/> |<span data-ttu-id="ea46a-p110">Все сообщения, содержащие HTML-теги \<Object\>, будут помечены как нежелательные. Этот HTML-тег позволяет запускать подключаемые модули или приложения в окне HTML.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p110">When this setting is enabled, any message that contains the \<Object\> HTML tag will be marked as spam. This HTML tag allows plug-ins or applications to run in an HTML window.</span></span>  <br/> |<span data-ttu-id="ea46a-156">X-CustomSpam: тег Object в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-156">X-CustomSpam: Object tag in html</span></span>  <br/> |
|<span data-ttu-id="ea46a-157">Теги Embed в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-157">Embed tags in HTML</span></span>  <br/> |<span data-ttu-id="ea46a-p111">Все сообщения, содержащие HTML-теги \<Embed\>, будут помечены как нежелательные. Данный HTML-тег позволяет внедрять в HTML-документы различные типы документов с разным типом данных. Например, звуки, фильмы или рисунки.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p111">When this setting is enabled, any message that contains the \<Embed\> HTML tag will be marked as spam. This HTML tag allows different kinds of documents of varying data types to be embedded into an HTML document. Examples include sounds, movies, or pictures.</span></span>  <br/> |<span data-ttu-id="ea46a-161">X-CustomSpam: тег Embed в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-161">X-CustomSpam: Embed tag in html</span></span>  <br/> |
|<span data-ttu-id="ea46a-162">Теги Form в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-162">Form tags in HTML</span></span>  <br/> |<span data-ttu-id="ea46a-p112">Все сообщения, содержащие HTML-теги \<Form\>, будут помечены как нежелательные. Этот HTML-тег используется для создания форм веб-сайтов. Рекламные почтовые сообщения часто содержат этот тег, чтобы запрашивать у получателя ту или иную информацию.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p112">When this setting is enabled, any message that contains the \<Form\> HTML tag will be marked as spam. This HTML tag is used to create website forms. Email advertisements often include this tag to solicit information from the recipient.</span></span>  <br/> |<span data-ttu-id="ea46a-166">X-CustomSpam: тег Form в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-166">X-CustomSpam: Form tag in html</span></span>  <br/> |
|<span data-ttu-id="ea46a-167">Веб-маяки в HTML</span><span class="sxs-lookup"><span data-stu-id="ea46a-167">Web bugs in HTML</span></span>  <br/> |<span data-ttu-id="ea46a-p113">Все сообщения, содержащие веб-маяки, будут помечены как нежелательные. Веб-маяк — графический объект, позволяющий определить, была ли прочитана веб-страница или сообщение электронной почты. Веб-маяки часто невидимы для получателя, так как обычно представляют собой изображение размером в один пиксель. Безопасные информационные бюллетени также могут содержать веб-маяки, хотя многие пользователи считают это вмешательством в частную жизнь.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p113">When this setting is enabled, any message that contains a Web bug will be marked as spam. A Web bug is a graphic that is designed to determine whether a Web page or email message has been read. Web bugs are often invisible to the recipient because they are typically added to a message as a graphic that is as small as one pixel by one pixel. Legitimate newsletters may also use this technique, although many consider this an invasion of privacy.</span></span>  <br/> |<span data-ttu-id="ea46a-172">X-CustomSpam: веб-ошибка</span><span class="sxs-lookup"><span data-stu-id="ea46a-172">X-CustomSpam: Web bug</span></span>  <br/> |
|<span data-ttu-id="ea46a-173">Список нежелательных слов</span><span class="sxs-lookup"><span data-stu-id="ea46a-173">Apply sensitive word list</span></span>  <br/> |<span data-ttu-id="ea46a-p114">Все сообщения, содержащие слова из такого списка, будут помечены как нежелательные. Использование списка нежелательных слов позволяет легко блокировать слова, часто употребляемые в потенциально оскорбительных сообщениях. Некоторые из этих слов чувствительны к регистру. Администратор не может редактировать этот список. Фильтрация по списку оскорбительных слов применяется как к теме, так и к тексту сообщения.</span><span class="sxs-lookup"><span data-stu-id="ea46a-p114">When this setting is enabled, any message that contains a word from the sensitive word list will be marked as spam. Using the sensitive word list allows easy blocking of words that are associated with potentially offensive messages. Some of these words are case sensitive. As an administrator, you cannot edit this list. Filtering against the sensitive word list is applied to both the subject and message body of a message.</span></span>  <br/> |<span data-ttu-id="ea46a-179">X-CustomSpam: оскорбительные слова в теме или тексте</span><span class="sxs-lookup"><span data-stu-id="ea46a-179">X-CustomSpam: Sensitive word in subject/body</span></span>  <br/> |
|<span data-ttu-id="ea46a-180">Запись инфраструктуры политики отправителей: серьезный сбой</span><span class="sxs-lookup"><span data-stu-id="ea46a-180">SPF record: hard fail</span></span>  <br/> |<span data-ttu-id="ea46a-p115">Если этот параметр включен, сообщения, не прошедшие проверку SPF (т. е. отправленные с IP-адреса, не указанного в записи SPF) будут отмечены как нежелательные. Рекомендуется включить этот параметр, если организация опасается, что может получать фишинговые сообщения.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-p115">When this setting is enabled, messages that fail an SPF check (meaning they were sent from an IP address not specified in the SPF record) will be marked as spam. Turning this setting on is recommended for organizations who are concerned about receiving phishing messages.  </span></span><br/> <span data-ttu-id="ea46a-183">**Примечание.** Для этого параметра недоступен тестовый режим.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-183">**Note:** Test mode is not available for this option.</span></span>  <br/> |<span data-ttu-id="ea46a-184">X-CustomSpam: ошибка записи SPF</span><span class="sxs-lookup"><span data-stu-id="ea46a-184">X-CustomSpam: SPF Record Fail</span></span>  <br/> |
|<span data-ttu-id="ea46a-185">Условная фильтрация идентификатора отправителя: серьезный сбой</span><span class="sxs-lookup"><span data-stu-id="ea46a-185">Conditional Sender ID filtering: hard fail</span></span>  <br/> |<span data-ttu-id="ea46a-p116">Все сообщения, которые не прошли условную проверку идентификатора отправителя с серьезным сбоем, будут помечены как нежелательные. Этот параметр включает в себя проверку инфраструктуры политики отправителей и проверку идентификатора отправителя для защиты от заголовков сообщений, содержащих поддельных отправителей.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-p116">When this setting is enabled, any message that hard fails a conditional Sender ID check is marked as spam. This option combines an SPF check with a Sender ID check to help protect against message headers that contain forged senders.  </span></span><br/> <span data-ttu-id="ea46a-188">**Примечание.** Для этого параметра недоступен тестовый режим.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-188">**Note:** Test mode is not available for this option.</span></span>  <br/> |<span data-ttu-id="ea46a-189">X-CustomSpam: ошибка SPF из записи</span><span class="sxs-lookup"><span data-stu-id="ea46a-189">X-CustomSpam: SPF From Record Fail</span></span>  <br/> |
|<span data-ttu-id="ea46a-190">Подложное уведомление о недоставленном отчете</span><span class="sxs-lookup"><span data-stu-id="ea46a-190">NDR backscatter</span></span>  <br/> |<span data-ttu-id="ea46a-p117">Если вы используете EOP для защиты локальных почтовых ящиков, то при включении этой настройки все допустимые сообщения с отчетом о недоставке доставляются исходному отправителю, а все подложные уведомления о недоставленных сообщениях (нелегальные отчеты о недоставке) помечаются как нежелательные. Если этот параметр не включен, все отчеты о недоставке по-прежнему проходят через фильтрацию нежелательной почты. В таком случае большинство допустимых сообщений будут доставляться исходному отправителю, но не все подложные уведомления о недоставленных сообщениях будут помечены как нежелательные. Тем не менее подложные уведомления о недоставленных сообщениях, которые не помечаются как нежелательные, будут доставлены не исходному, а поддельному отправителю.  </span><span class="sxs-lookup"><span data-stu-id="ea46a-p117">If you're using EOP to protect on-premises mailboxes, when this setting is enabled, all legitimate non-delivery report (NDR) messages are delivered to the original sender, and all backscatter (illegitimate NDR) messages will be marked as spam. If you don't enable this setting, then all NDRs still go through spam filtering. In this case, most legitimate messages will get delivered to the original sender while some, but not all, backscatter messages will get marked as spam. However, backscatter messages that aren't marked as spam won't go to the original sender because it will go to the spoofed sender.  </span></span><br/> <span data-ttu-id="ea46a-195">Если вы используете службу для защиты облачных почтовых ящиков Exchange Online, настраивать этот параметр не нужно.</span><span class="sxs-lookup"><span data-stu-id="ea46a-195">If you're using the service to protect Exchange Online cloud-hosted mailboxes, you don't need to configure this setting.</span></span>  <br/> <span data-ttu-id="ea46a-p118">> [!NOTE]>  В обоих сценариях (для локальных и облачных почтовых ящиков), этот параметр не нужно включать для исходной почты, отправляемой через службу, потому что отчеты о недоставке, которые являются безопасными сообщениями о недоставке, будут автоматически определяться как таковые и возвращаться исходному отправителю. >  Для этого параметра недоступен тестовый режим.           > [!TIP]> Дополнительные сведения о подложных уведомлениях о недоставленных сообщениях и EOP см. в разделе [Подложные уведомления о недоставленном сообщении и EOP](backscatter-messages-and-eop.md).</span><span class="sxs-lookup"><span data-stu-id="ea46a-p118">> [!NOTE]>  For both scenarios (on-premises and cloud-hosted mailboxes), it's also not necessary to enable this setting for outbound mail sent through the service, as NDRs that are legitimate bounce messages will be automatically detected and delivered to the original sender. >  Test mode is not available for this option.           > [!TIP]> For more information about backscatter messages and EOP, see [Backscatter messages and EOP](backscatter-messages-and-eop.md).</span></span>           |<span data-ttu-id="ea46a-199">X-CustomSpam: подложный отчет о недоставке</span><span class="sxs-lookup"><span data-stu-id="ea46a-199">X-CustomSpam: Backscatter NDR</span></span>  <br/> |
|<span data-ttu-id="ea46a-200">Массовая рассылка</span><span class="sxs-lookup"><span data-stu-id="ea46a-200">Bulk mail</span></span>  <br/> |<span data-ttu-id="ea46a-p119">Расширенная фильтрация нежелательной почты больше не используется и заменена параметрами пороговых значений массовой рассылки. Дополнительные сведения о параметрах и инструкции по их настройке см. в статьях [В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?](what-s-the-difference-between-junk-email-and-bulk-email.md) и [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).  </span><span class="sxs-lookup"><span data-stu-id="ea46a-p119">Advanced-spam filtering of bulk email has been retired and replaced with the bulk and email threshold settings. Check out [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Configure your spam filter policies](configure-your-spam-filter-policies.md) for more information and how to configure the settings.  </span></span><br/> ||
   
