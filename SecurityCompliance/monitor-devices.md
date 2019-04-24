---
title: Мониторинг устройств в Центре безопасности Microsoft 365
description: В этой статье рассказывается о том, как можно хранить ваши устройства в надежном, актуальном и плашечных угрозах в Организации.
keywords: безопасность, вредоносные программы, Microsoft 365, M365, центр безопасности, монитор, отчет, устройства
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 31d89b8bbcad98814ff33764bad24bffbbba4968
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263624"
---
# <a name="monitor-devices-in-microsoft-365-security"></a><span data-ttu-id="06051-104">Мониторинг устройств в Центре безопасности Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="06051-104">Monitor devices in Microsoft 365 security</span></span>

<span data-ttu-id="06051-105">Обеспечьте безопасность и актуальность ваших устройств, а также возможность выявления потенциальных угроз в центре безопасности Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="06051-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="06051-106">Просмотр оповещений устройства</span><span class="sxs-lookup"><span data-stu-id="06051-106">View device alerts</span></span>

<span data-ttu-id="06051-107">Получение обновленных предупреждений о действиях с нарушением безопасности и других угрозах на устройствах из пакета ATP для защитника Windows (доступно с помощью лицензии "по").</span><span class="sxs-lookup"><span data-stu-id="06051-107">Get up-to-date alerts about breach activity and other threats on your devices from Windows Defender ATP (available with an E5 license).</span></span> <span data-ttu-id="06051-108">Центр безопасности Microsoft 365 имеет несколько карточек, позволяющих эффективно отслеживать эти оповещения на высоком уровне, в зависимости от предпочтительного рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="06051-108">Microsoft 365 security center has several cards that allow you to effectively monitor these alerts at a high-level, depending on your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="06051-109">Отслеживание оповещений о высокой степени влияния</span><span class="sxs-lookup"><span data-stu-id="06051-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="06051-110">Каждое оповещение для защитника Windows ATP имеет соответствующую степень серьезности, среднюю, низкую или информационную, которая указывает на потенциальное влияние на сеть, если оно оставлено необслуживаемым.</span><span class="sxs-lookup"><span data-stu-id="06051-110">Each Windows Defender ATP alert has a corresponding severity—high, medium, low, or informational—that indicates its potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="06051-111">Используйте карточку серьезности оповещений для **устройств** , чтобы сосредоточиться на более серьезных оповещениях и может требовать немедленный отклик.</span><span class="sxs-lookup"><span data-stu-id="06051-111">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="06051-112">Из этой карточки вы можете просмотреть дополнительные сведения на портале Центра безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="06051-112">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Карточка серьезности оповещений устройств](./media/security-docs/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="06051-114">Общие сведения об источниках оповещений</span><span class="sxs-lookup"><span data-stu-id="06051-114">Understand sources of alerts</span></span>

<span data-ttu-id="06051-115">"Защитник Windows" использует данные из широкого диапазона датчиков безопасности и источников аналитики для создания оповещений.</span><span class="sxs-lookup"><span data-stu-id="06051-115">Windows Defender ATP leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="06051-116">Например, он может использовать сведения об обнаружении антиВирусной программы "Защитник Windows" и стороннего антивредоносного по, а также собственную логику, предоставляемую через API веб-службы.</span><span class="sxs-lookup"><span data-stu-id="06051-116">For example, it can use detection information from Windows Defender Antivirus and third-party antimalware, as well as your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="06051-117">В карточке источников **обнаружения оповещений для устройств** показано распределение оповещений по источнику.</span><span class="sxs-lookup"><span data-stu-id="06051-117">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="06051-118">С помощью этой карточки можно отслеживать действия, связанные с определенными источниками, в частности настраиваемые источники.</span><span class="sxs-lookup"><span data-stu-id="06051-118">This card can help you track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="06051-119">Кроме того, вы можете сосредоточиться на оповещениях, поступающих от датчиков, которые не настроены для автоматической блокировки вредоносных действий или компонентов.</span><span class="sxs-lookup"><span data-stu-id="06051-119">You can also use this to focus on alerts coming from sensors that are not configured to automatically block malicious activity or components.</span></span>

![Карточка источников обнаружения оповещений для устройств](./media/security-docs/device-alert-detection-sources.png)

<span data-ttu-id="06051-121">Из этой карточки вы можете просмотреть дополнительные сведения на портале Центра безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="06051-121">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="06051-122">Сведения о типах угроз, инициирующих оповещения</span><span class="sxs-lookup"><span data-stu-id="06051-122">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="06051-123">Пакет ATP для защитника Windows сортирует каждое оповещение в категории, представляющей определенный этап в цепочке атак, или тип компонента угрозы.</span><span class="sxs-lookup"><span data-stu-id="06051-123">Windows Defender ATP sorts each alert into a category representing a certain stage in the attack chain or a type of threat component.</span></span> <span data-ttu-id="06051-124">Например, обнаруженные действия с угрозой могут быть отнесены к категории "Латерал Replace", чтобы указать, что действие приводило к попытке получить доступ к другим устройствам в сети и, возможно, произошло после того, как злоумышленник получит первоначальный фусолд.</span><span class="sxs-lookup"><span data-stu-id="06051-124">For example, detected threat activity might be categorized into “lateral movement” to indicate that the activity involved an attempt to reach other devices on the network and has likely occurred after attackers have gained an initial foothold.</span></span> <span data-ttu-id="06051-125">При обнаружении компонент для работы с угрозой может быть классифицирован в широком смысле как "Вредоносная" или как можно точнее, например "", "Перенос учетных данных" или других типов вредоносных или нежелательных программ.</span><span class="sxs-lookup"><span data-stu-id="06051-125">When detected, a threat component might either be classified broadly as “malware” or more specifically as “ransomware”, “credential stealing” or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="06051-126">В карточке **категории угроз для устройств** показано распределение оповещений по этим категориям.</span><span class="sxs-lookup"><span data-stu-id="06051-126">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="06051-127">Эти сведения можно использовать для определения действий по угрозам, например попыток кражи учетных данных, которые могут значительно повлиять на появление попыток социального проектирования, например.</span><span class="sxs-lookup"><span data-stu-id="06051-127">You can use this information to identify threat activity, such as attempts at credential theft, which can have more significant impact compared to attempts at social engineering, for example.</span></span> <span data-ttu-id="06051-128">Кроме того, вы можете использовать эту возможность для отслеживания потенциально необратимых угроз, таких как шантажистом.</span><span class="sxs-lookup"><span data-stu-id="06051-128">You can also use this to monitor for potentially destructive threats like ransomware.</span></span>

![Карточка категорий угроз для устройств](./media/security-docs/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="06051-130">Отслеживание активных оповещений</span><span class="sxs-lookup"><span data-stu-id="06051-130">Monitor active alerts</span></span>

<span data-ttu-id="06051-131">Карточка **состояния оповещения для устройства** указывает количество оповещений, которые не были разрешены и могут потребовать внимания.</span><span class="sxs-lookup"><span data-stu-id="06051-131">The **Device alert status** card indicates the number of alerts that have not been resolved and might require attention.</span></span> <span data-ttu-id="06051-132">Из этой карточки вы можете просмотреть дополнительные сведения на портале Центра безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="06051-132">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

![Карточка состояния оповещения для устройства](./media/security-docs/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="06051-134">Отслеживание классификации разрешенных оповещений</span><span class="sxs-lookup"><span data-stu-id="06051-134">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="06051-135">При разрешении оповещения о продолжении защитника Windows сотрудники отдела безопасности могут указать, было ли оповещение проверено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06051-135">When resolving a Window Defender ATP alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="06051-136">Истинное оповещение, идентифицирующее реальные действия или компоненты угроз</span><span class="sxs-lookup"><span data-stu-id="06051-136">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="06051-137">Ложное оповещение, которое неправильно определило нормальные действия</span><span class="sxs-lookup"><span data-stu-id="06051-137">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="06051-138">На карточке **классификация оповещенИй устройств** показано, были ли разрешенные оповещения классифицированы как "истина" или "ложные".</span><span class="sxs-lookup"><span data-stu-id="06051-138">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="06051-139">Из этой карточки вы можете просмотреть дополнительные сведения на портале Центра безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="06051-139">From this card, you can view more information on the Windows Defender Security Center portal.</span></span>

<span data-ttu-id="06051-140">Примечание. в некоторых случаях сведения об классификации недоступны для определенных оповещений.</span><span class="sxs-lookup"><span data-stu-id="06051-140">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Карточка классификации оповещений для устройств](./media/security-docs/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="06051-142">Отслеживание определения разрешенных оповещений</span><span class="sxs-lookup"><span data-stu-id="06051-142">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="06051-143">В дополнение к классификации того, является ли оповещение истинным или ложным во время разрешения, персонал по обеспечению безопасности может определить тип обычной или вредоносной активности, обнаруженной при проверке оповещения.</span><span class="sxs-lookup"><span data-stu-id="06051-143">In addition to classifying whether an alert is true or false during resolution, your security staff can provide a determination, indicating the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="06051-144">На карточке **определения оповещения для устройства** отображается определение, предоставленное для каждого оповещения, а именно:</span><span class="sxs-lookup"><span data-stu-id="06051-144">The **Device alert determination** card shows the determination provided for each alert, specifically:</span></span>

* <span data-ttu-id="06051-145">**Апт** — Расширенная постоянная угроза, указывающая на то, что обнаруженные действия или компоненты угроз являются частью сложного нарушения безопасности, разработанного для получения фусолд в сети, подверженной уязвимости</span><span class="sxs-lookup"><span data-stu-id="06051-145">**APT** – advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="06051-146">**ВредоносНая программа** — вредоносный файл или код</span><span class="sxs-lookup"><span data-stu-id="06051-146">**Malware** – malicious file or code</span></span>
* <span data-ttu-id="06051-147">**Персонал по безопасности** — обычные действия, выполняемые персоналом по обеспечению безопасности</span><span class="sxs-lookup"><span data-stu-id="06051-147">**Security personnel** – normal activity performed by security staff</span></span>
* <span data-ttu-id="06051-148">**Тестирование безопасности** — действия или компоненты, предназначенные для моделирования фактических угроз и ожидаемые для запуска датчиков безопасности и создания оповещений</span><span class="sxs-lookup"><span data-stu-id="06051-148">**Security testing** – activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="06051-149">**Нежелательное программное обеспечение** — приложения и другое программное обеспечение, которые не считаются вредоносными, но в противном случае нарушают политику или допустимые стандарты использования</span><span class="sxs-lookup"><span data-stu-id="06051-149">**Unwanted software** – apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="06051-150">\*\*\*\* Другие — любое другое определение, которое не относится к предоставленным типам</span><span class="sxs-lookup"><span data-stu-id="06051-150">**Others** – any other determination that does not fall under the provided types</span></span>

<span data-ttu-id="06051-151">Из этой карточки вы можете просмотреть дополнительные сведения в центре безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="06051-151">From this card, you can view more information in Windows Defender security center.</span></span>

![Карточка определения оповещения для устройства](./media/security-docs/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="06051-153">Сведения о том, какие устройства подвержены риску</span><span class="sxs-lookup"><span data-stu-id="06051-153">Understand which devices are at risk</span></span>

<span data-ttu-id="06051-154">**Защита устройства** показывает уровень риска для устройств.</span><span class="sxs-lookup"><span data-stu-id="06051-154">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="06051-155">Уровень риска зависит от таких факторов, как тип и серьезность оповещений на устройстве.</span><span class="sxs-lookup"><span data-stu-id="06051-155">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Карта защиты устройства](./media/security-docs/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="06051-157">Отслеживание и отправка отчетов о состоянии устройств, управляемых Intune</span><span class="sxs-lookup"><span data-stu-id="06051-157">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="06051-158">Следующие мониторинг и отчеты содержат данные от устройств, зарегистрированных в Intune.</span><span class="sxs-lookup"><span data-stu-id="06051-158">The following monitoring and reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="06051-159">Данные из незарегистрированных устройств не входят в состав.</span><span class="sxs-lookup"><span data-stu-id="06051-159">Data from unenrolled devices is not included.</span></span> <span data-ttu-id="06051-160">Просматривать эти карты могут только глобальные администраторы.</span><span class="sxs-lookup"><span data-stu-id="06051-160">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="06051-161">Данные устройства, зарегистрированные в Intune, включают:</span><span class="sxs-lookup"><span data-stu-id="06051-161">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="06051-162">Соответствие устройства требованиям</span><span class="sxs-lookup"><span data-stu-id="06051-162">Device compliance</span></span>
* <span data-ttu-id="06051-163">Устройства с активным вредоносным по</span><span class="sxs-lookup"><span data-stu-id="06051-163">Devices with active malware</span></span>
* <span data-ttu-id="06051-164">Типы вредоносных программ на устройствах</span><span class="sxs-lookup"><span data-stu-id="06051-164">Types of malware on devices</span></span>
* <span data-ttu-id="06051-165">Вредоносные программы на устройствах</span><span class="sxs-lookup"><span data-stu-id="06051-165">Malware on devices</span></span>
* <span data-ttu-id="06051-166">Устройства с обнаружением вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="06051-166">Devices with malware detections</span></span>
* <span data-ttu-id="06051-167">Пользователи с обнаружением вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="06051-167">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="06051-168">Отслеживание соответствия устройства требованиям</span><span class="sxs-lookup"><span data-stu-id="06051-168">Monitor device compliance</span></span>

<span data-ttu-id="06051-169">**Соответствие требованиям устройства** показывает, сколько устройств, зарегистрированных в Intune, соответствуют политикам конфигурации.</span><span class="sxs-lookup"><span data-stu-id="06051-169">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Карта соответствия требованиям устройств](./media/security-docs/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="06051-171">Обнаружение устройств с обнаружением вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="06051-171">Discover devices with malware detections</span></span>

<span data-ttu-id="06051-172">**Обнаружение вредоносных программ для устройств** предоставляет количество устройств, зарегистрированных в Intune, с вредоносными программами, которые не были полностью устранены в связи с ожидающими действиями — перезапусками, полным сканированием или ручными действиями пользователя, или если действие по исправлению не было выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="06051-172">**Device malware detections** provides the number of Intune enrolled devices with malware that have not been fully resolved due to pending actions—a restart, a full scan or manual user actions—or if the remediation action did not complete successfully.</span></span>

![Карточка обнаружения вредоносных программ для устройств](./media/security-docs/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="06051-174">Сведения о типах обнаруженных вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="06051-174">Understand the types of malware detected</span></span>

<span data-ttu-id="06051-175">**Типы вредоносных программ на устройствах** показывают различные виды вредоносных программ, обнаруженных на устройствах, зарегистрированных в Intune.</span><span class="sxs-lookup"><span data-stu-id="06051-175">**Types of malware on devices** shows different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="06051-176">Вы можете исследовать каждый тип в центре безопасности Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="06051-176">You can investigate each type in Microsoft 365 security center.</span></span>

![Тип карты вредоносных программ на устройствах](./media/security-docs/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="06051-178">Общие сведения об определенных вредоносных программах, обнаруженных на устройствах</span><span class="sxs-lookup"><span data-stu-id="06051-178">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="06051-179">**ВредоносНые программы на устройствах** предоставляет список определенных вредоносных программ, обнаруженных на устройствах.</span><span class="sxs-lookup"><span data-stu-id="06051-179">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Карта вредоносных программ на устройствах](./media/security-docs/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="06051-181">Сведения о том, какие устройства имеют большинство вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="06051-181">Understand which devices have the most malware</span></span>

<span data-ttu-id="06051-182">**Устройства с обнаружением вредоносных программ** показывают, какие устройства имеют большинство обнаружений вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="06051-182">**Devices with malware detections** shows which devices have the most malware detections.</span></span> <span data-ttu-id="06051-183">В центре безопасности Microsoft 365 можно проверить, активна ли вредоносная программа, кто использует устройство и его состояние управления в Intune.</span><span class="sxs-lookup"><span data-stu-id="06051-183">In Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Карточка с устройствами с обнаружением вредоносных программ](./media/security-docs/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="06051-185">Сведения о том, какие пользователи имеют устройства с большинством вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="06051-185">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="06051-186">**Пользователи с обнаружением вредоносных программ** показывают пользователей с устройствами, которые использовались с большинством обнаруженных вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="06051-186">**Users with malware detections** shows users with devices that had the most malware detections.</span></span> <span data-ttu-id="06051-187">В центре безопасности Microsoft 365 вы можете узнать, сколько устройств назначено каждому пользователю, и дополнительные сведения о каждом устройстве и о типе вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="06051-187">In Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Пользователи с картой обнаружения вредоносных программ](./media/security-docs/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a><span data-ttu-id="06051-189">Мониторинг развертывания и обнаружения правил ASR и управление ими</span><span class="sxs-lookup"><span data-stu-id="06051-189">Monitor and manage ASR rule deployment and detections</span></span>

<span data-ttu-id="06051-190">[Правила предотвращения снижения уязвимости (ASR)](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) помогают предотвратить действия и приложения, которые обычно используются вредоносной программой для проникновения компьютеров.</span><span class="sxs-lookup"><span data-stu-id="06051-190">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) help prevent actions and apps that are typically used by exploit-seeking malware to infect machines.</span></span> <span data-ttu-id="06051-191">Эти правила определяют, когда и как могут запускаться исполняемые файлы.</span><span class="sxs-lookup"><span data-stu-id="06051-191">These rules control when and how executables can run.</span></span> <span data-ttu-id="06051-192">Например, можно запретить JavaScript или VBScript запускать загруженный исполняемый файл, блокировать вызовы Win32 API из макросов Office или блокировать процессы, которые запускаются с USB-дисков.</span><span class="sxs-lookup"><span data-stu-id="06051-192">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Карточка о снижении уязвимости](./media/security-docs/attack-surface-reduction-rules.png)

<span data-ttu-id="06051-194">В карточке **правила уменьшения уязвимой зоны** представлен обзор развертывания правил на всех устройствах.</span><span class="sxs-lookup"><span data-stu-id="06051-194">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="06051-195">В верхней панели карточки показано общее количество устройств, которые находятся в следующих режимах развертывания:</span><span class="sxs-lookup"><span data-stu-id="06051-195">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="06051-196">**Режим блокировки** — устройства с как минимум одним правилом, настроенными для блокирования обнаруженных действий</span><span class="sxs-lookup"><span data-stu-id="06051-196">**Block mode** – devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="06051-197">**Режим аудита** — устройства без правил, не настроенные для блокирования обнаруженных действий, но у которых есть по крайней мере один набор правил для аудита обнаруженных действий</span><span class="sxs-lookup"><span data-stu-id="06051-197">**Audit mode** – devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="06051-198">**Выкл** . — устройства со всеми правилами ASR отключены.</span><span class="sxs-lookup"><span data-stu-id="06051-198">**Off** – devices with all ASR rules turned off</span></span>

<span data-ttu-id="06051-199">В нижней части этой карточки показаны параметры по правилам для всех устройств.</span><span class="sxs-lookup"><span data-stu-id="06051-199">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="06051-200">На каждой полосе отображается количество устройств, которые настроены на блокировку или обнаружение, а также полностью отключено правило.</span><span class="sxs-lookup"><span data-stu-id="06051-200">Each bar indicates the number of devices that are set to block or audit detection or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="06051-201">Просмотр обнаруженных АВАРИЙных ASR</span><span class="sxs-lookup"><span data-stu-id="06051-201">View ASR detections</span></span>

<span data-ttu-id="06051-202">Чтобы просмотреть подробные сведения об обнаружении правил ASR в сети, выберите **Просмотр обнаружений** в карточке **правила уменьшения уязвимой зоны** .</span><span class="sxs-lookup"><span data-stu-id="06051-202">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="06051-203">Откроется вкладка **обнаружения** на странице подробный отчет.</span><span class="sxs-lookup"><span data-stu-id="06051-203">The **Detections** tab in the detailed report page will open.</span></span>

![Вкладка "обнаружения"](./media/security-docs/detections-tab.png)

<span data-ttu-id="06051-205">На диаграмме, расположенной в верхней части страницы, показано обнаружение с обнаружением стеков по времени, которые были заблокированы или проверены.</span><span class="sxs-lookup"><span data-stu-id="06051-205">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="06051-206">В таблице внизу приведен список самых последних обнаружений.</span><span class="sxs-lookup"><span data-stu-id="06051-206">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="06051-207">Используйте следующие сведения в таблице, чтобы определить природу обнаружений:</span><span class="sxs-lookup"><span data-stu-id="06051-207">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="06051-208">**Обнаруженный файл** — файл, обычно сценарий или документ, содержимое которого активировало вероятные действия по атакам</span><span class="sxs-lookup"><span data-stu-id="06051-208">**Detected file** – the file, typically a script or a document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="06051-209">**Rule (правило** ) — имя, описывающее действия, которые разрабатываются правилом для перехвата.</span><span class="sxs-lookup"><span data-stu-id="06051-209">**Rule** – name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="06051-210">Сведения о существующих правилах ASR</span><span class="sxs-lookup"><span data-stu-id="06051-210">Read about existing ASR rules</span></span>
* <span data-ttu-id="06051-211">**Исходное приложение** — приложение, которое загрузило или выполнило содержимое, вызывающее вероятные действия по атакам.</span><span class="sxs-lookup"><span data-stu-id="06051-211">**Source app** – the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="06051-212">Это может быть легальное приложение, например веб-браузер, приложение Office или системное средство, например PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06051-212">This could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="06051-213">**Издатель** — поставщик, который освободил исходное приложение</span><span class="sxs-lookup"><span data-stu-id="06051-213">**Publisher** – the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="06051-214">Проверка параметров правил для устройства ASR</span><span class="sxs-lookup"><span data-stu-id="06051-214">Review device ASR rule settings</span></span>

<span data-ttu-id="06051-215">На странице отчета " **правила снижения уязвимости** " перейдите на вкладку **Конфигурация** , чтобы просмотреть параметры правил для отдельных устройств.</span><span class="sxs-lookup"><span data-stu-id="06051-215">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="06051-216">Выберите устройство, чтобы получить подробные сведения о том, находится ли каждое правило в режиме блокировки, режиме аудита или полном отключении.</span><span class="sxs-lookup"><span data-stu-id="06051-216">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Вкладка "Конфигурация"](./media/security-docs/configuration-tab.png)

<span data-ttu-id="06051-218">Microsoft Intune предоставляет функции управления для правил ASR.</span><span class="sxs-lookup"><span data-stu-id="06051-218">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="06051-219">Если вы хотите обновить параметры, выберите **начать работу** в разделе **Настройка устройств** на вкладке, чтобы открыть компонент "Управление устройствами в Intune".</span><span class="sxs-lookup"><span data-stu-id="06051-219">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="06051-220">Исключение файлов из правил ASR</span><span class="sxs-lookup"><span data-stu-id="06051-220">Exclude files from ASR rules</span></span>

<span data-ttu-id="06051-221">За счет исключения файлов из обнаружений можно предотвратить нежелательные ложные срабатывания и более уверенно развернуть правила снижения уязвимости в режиме блокировки.</span><span class="sxs-lookup"><span data-stu-id="06051-221">By excluding files from detections, you can prevent unwanted false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="06051-222">Несмотря на то, что исключения файлов для правил сокращения направлений атак управляются в Microsoft Intune, центр безопасности Microsoft 365 предоставляет средство анализа, которое поможет вам определить файлы, активируемые для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="06051-222">While file exclusions for attack surface reduction rules are managed on Microsoft Intune, Microsoft 365 security center provides an analysis tool to help you understand the files that are triggering detections.</span></span> <span data-ttu-id="06051-223">Кроме того, он помогает собирать имена файлов, которые можно исключить из системы.</span><span class="sxs-lookup"><span data-stu-id="06051-223">It also helps collect the names of the files you might want to exclude.</span></span>

<span data-ttu-id="06051-224">Чтобы начать анализ обнаружений и сбор файлов для исключения, перейдите на вкладку " **Добавление исключений** " на странице отчета " **правила уменьшения уязвимой зоны** ".</span><span class="sxs-lookup"><span data-stu-id="06051-224">To start analyzing detections and collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

![Вкладка "Добавление исключений"](./media/security-docs/add-exclusions-tab.png)

<span data-ttu-id="06051-226">В таблице перечислены все имена файлов, обнаруженные правилами сокращения для атак на уязвимую зону.</span><span class="sxs-lookup"><span data-stu-id="06051-226">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="06051-227">После выбора файла или нескольких файлов вы можете узнать, как добавлять эти файлы к исключениям.</span><span class="sxs-lookup"><span data-stu-id="06051-227">Once you select a file or multiple files, you can review the impact of adding those files to your exceptions:</span></span>

* <span data-ttu-id="06051-228">Сокращение общего числа обнаружений</span><span class="sxs-lookup"><span data-stu-id="06051-228">The reduction in the total number of detections</span></span>
* <span data-ttu-id="06051-229">Сокращение общего числа устройств, на которые влияет обнаружение</span><span class="sxs-lookup"><span data-stu-id="06051-229">The reduction in the total number of devices affected by the detections</span></span>

<span data-ttu-id="06051-230">Чтобы получить список выбранных файлов с полными путями для исключения, выберите пункт **Получение путей исключения**.</span><span class="sxs-lookup"><span data-stu-id="06051-230">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="06051-231">Для получения дополнительных сведений об исключении и подробных инструкциях по их добавлению прочитайте статью [Устранение неполадок с правилами снижения уязвимости](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).</span><span class="sxs-lookup"><span data-stu-id="06051-231">For more information about exclusions and detailed instructions about how to add them, read [troubleshoot attack surface reduction rules](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr).</span></span>
