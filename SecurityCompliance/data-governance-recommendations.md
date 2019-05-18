---
title: Как определяется содержимое для рекомендаций по управлению данными
ms.author: brendonb
author: stephow-MSFT
manager: laurawi
ms.date: 1/15/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: Центр безопасности и соответствия требованиям Office 365 предоставляет рекомендации для управления данными на основе текущей настройки вашей организации и позволяет выполнить подготовку за пару щелчков. Некоторые из этих рекомендаций определяют конкретное содержимое в организации и указывают рекомендованные действия по управлению этим содержимым. Например, рекомендация может обнаружить элементы, содержащие важный деловой контент (например, связанные с адвокатской тайной сведения или соглашения о неразглашении) и затем позволяет автоматически присвоить метки хранения к этим элементам, чтобы обеспечить их конфиденциальность и правильное хранение. В этой статье перечислены рекомендации по управлению данными, которые вы можете встретить, и описано, какое содержимое обнаруживается для срабатывания каждой из них.
ms.openlocfilehash: 3d96b7c15d5b6a0f6ec3bbf467bd8a1099af559a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153711"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a><span data-ttu-id="c71d5-106">Как определяется содержимое для рекомендаций по управлению данными</span><span class="sxs-lookup"><span data-stu-id="c71d5-106">How content is identified for data-governance recommendations</span></span>

<span data-ttu-id="c71d5-p102">Центр безопасности и соответствия требованиям Office 365 предоставляет рекомендации для управления данными на основе текущей настройки вашей организации и позволяет выполнить подготовку за пару щелчков. Некоторые из этих рекомендаций определяют конкретное содержимое в организации и указывают рекомендованные действия по управлению этим содержимым. Например, рекомендация может обнаружить элементы, содержащие важный деловой контент (например, связанные с адвокатской тайной сведения или соглашения о неразглашении) и затем позволяет автоматически присвоить метки хранения к этим элементам, чтобы обеспечить их конфиденциальность и правильное хранение.</span><span class="sxs-lookup"><span data-stu-id="c71d5-p102">The Office 365 Security & Compliance Center provides recommendations for data governance based on your org's current setup and lets you set things up in a couple clicks. Some of these recommendations detect specific content in your organization and then provide recommended steps for managing that content. For example, a recommendation might detect items that contain business-critical content (such as attorney-client privilege or NDA info), and then let you automatically apply a retention label to those items to ensure that they’re classified and retained as needed.</span></span>

<span data-ttu-id="c71d5-110">В этой статье перечислены рекомендации по управлению данными, которые вы можете встретить, и описано, какое содержимое обнаруживается для срабатывания каждой из них.</span><span class="sxs-lookup"><span data-stu-id="c71d5-110">This topic lists the data-governance recommendations you might see and describes what content is detected to trigger each one.</span></span>

## <a name="clean-up-voicemail"></a><span data-ttu-id="c71d5-111">Очистить голосовую почту</span><span class="sxs-lookup"><span data-stu-id="c71d5-111">Clean up voicemail</span></span>

<span data-ttu-id="c71d5-p103">Эта рекомендация отображается, если в почтовых ящиках пользователей обнаружен тип сообщений электронной почты, определенный как "голосовая почта". Узнайте больше о [свойствах сообщений в Exchange](https://docs.microsoft.com/ru-RU/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="c71d5-p103">This recommendation appears when email messages identified as the message type ‘voicemail’ are detected in users’ mailboxes. Learn more about [message properties in Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span></span>

## <a name="label-attorney-client-privilege-content"></a><span data-ttu-id="c71d5-114">Пометить контент, содержащий адвокатскую тайну</span><span class="sxs-lookup"><span data-stu-id="c71d5-114">Label attorney-client privilege content</span></span> 

<span data-ttu-id="c71d5-115">Эта рекомендация отображается при выполнении любого из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="c71d5-115">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="c71d5-116">В тексте сообщения электронной почты обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c71d5-116">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="c71d5-117">ACP</span><span class="sxs-lookup"><span data-stu-id="c71d5-117">ACP</span></span>
    - <span data-ttu-id="c71d5-118">Общение между адвокатом и клиентом с обеспечением конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="c71d5-118">Attorney Client Privilege</span></span>
    - <span data-ttu-id="c71d5-119">Адвокатская тайна</span><span class="sxs-lookup"><span data-stu-id="c71d5-119">Attorney-Client Privilege</span></span>
    - <span data-ttu-id="c71d5-120">Конфиденциальное общение с адвокатом</span><span class="sxs-lookup"><span data-stu-id="c71d5-120">Attorney-Client Privileged</span></span>

- <span data-ttu-id="c71d5-121">В файлах SharePoint или OneDrive обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c71d5-121">Any combination of these keywords are detected in SharePoint or OneDrive files:</span></span>
    - <span data-ttu-id="c71d5-122">ACP</span><span class="sxs-lookup"><span data-stu-id="c71d5-122">ACP</span></span>
    - <span data-ttu-id="c71d5-123">Общение между адвокатом и клиентом с обеспечением конфиденциальности\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-123">Attorney Client Privilege\*</span></span>
    - <span data-ttu-id="c71d5-124">Адвокатская тайна</span><span class="sxs-lookup"><span data-stu-id="c71d5-124">AC Privilege</span></span>

## <a name="retain-audio-files"></a><span data-ttu-id="c71d5-125">Сохранить звуковые файлы</span><span class="sxs-lookup"><span data-stu-id="c71d5-125">Retain audio files</span></span>

<span data-ttu-id="c71d5-126">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="c71d5-126">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c71d5-127">MP3</span><span class="sxs-lookup"><span data-stu-id="c71d5-127">.MP3</span></span>
- <span data-ttu-id="c71d5-128">WMA</span><span class="sxs-lookup"><span data-stu-id="c71d5-128">.WMA</span></span>
- <span data-ttu-id="c71d5-129">WAV</span><span class="sxs-lookup"><span data-stu-id="c71d5-129">.WAV</span></span>
- <span data-ttu-id="c71d5-130">RA</span><span class="sxs-lookup"><span data-stu-id="c71d5-130">.RA</span></span>
- <span data-ttu-id="c71d5-131">RAM</span><span class="sxs-lookup"><span data-stu-id="c71d5-131">.RAM</span></span>
- <span data-ttu-id="c71d5-132">RM</span><span class="sxs-lookup"><span data-stu-id="c71d5-132">.RM</span></span>
- <span data-ttu-id="c71d5-133">MID</span><span class="sxs-lookup"><span data-stu-id="c71d5-133">.MID</span></span>
- <span data-ttu-id="c71d5-134">OGG</span><span class="sxs-lookup"><span data-stu-id="c71d5-134">.OGG</span></span>
- <span data-ttu-id="c71d5-135">AIFF</span><span class="sxs-lookup"><span data-stu-id="c71d5-135">.AIFF</span></span>
- <span data-ttu-id="c71d5-136">PCM</span><span class="sxs-lookup"><span data-stu-id="c71d5-136">.PCM</span></span>
- <span data-ttu-id="c71d5-137">AAC</span><span class="sxs-lookup"><span data-stu-id="c71d5-137">.AAC</span></span>
- <span data-ttu-id="c71d5-138">FLAC</span><span class="sxs-lookup"><span data-stu-id="c71d5-138">.FLAC</span></span>
- <span data-ttu-id="c71d5-139">ALAC</span><span class="sxs-lookup"><span data-stu-id="c71d5-139">.ALAC</span></span>

## <a name="retain-cad-files"></a><span data-ttu-id="c71d5-140">Сохранить файлы САПР</span><span class="sxs-lookup"><span data-stu-id="c71d5-140">Retain CAD files</span></span>

<span data-ttu-id="c71d5-141">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="c71d5-141">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c71d5-142">3DXML</span><span class="sxs-lookup"><span data-stu-id="c71d5-142">.3DXML</span></span>
- <span data-ttu-id="c71d5-143">ACIS</span><span class="sxs-lookup"><span data-stu-id="c71d5-143">.ACIS</span></span>
- <span data-ttu-id="c71d5-144">ARC</span><span class="sxs-lookup"><span data-stu-id="c71d5-144">.ARC</span></span>
- <span data-ttu-id="c71d5-145">ASM</span><span class="sxs-lookup"><span data-stu-id="c71d5-145">.ASM</span></span>
- <span data-ttu-id="c71d5-146">CAT\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-146">.CAT\*</span></span>
- <span data-ttu-id="c71d5-147">CGR</span><span class="sxs-lookup"><span data-stu-id="c71d5-147">.CGR</span></span>
- <span data-ttu-id="c71d5-148">DW\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-148">.DW\*</span></span>
- <span data-ttu-id="c71d5-149">DX\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-149">.DX\*</span></span>
- <span data-ttu-id="c71d5-150">EDRW</span><span class="sxs-lookup"><span data-stu-id="c71d5-150">.EDRW</span></span>
- <span data-ttu-id="c71d5-151">IAM</span><span class="sxs-lookup"><span data-stu-id="c71d5-151">.IAM</span></span>
- <span data-ttu-id="c71d5-152">IGES</span><span class="sxs-lookup"><span data-stu-id="c71d5-152">.IGES</span></span>
- <span data-ttu-id="c71d5-153">IGS</span><span class="sxs-lookup"><span data-stu-id="c71d5-153">.IGS</span></span>
- <span data-ttu-id="c71d5-154">IPT</span><span class="sxs-lookup"><span data-stu-id="c71d5-154">.IPT</span></span>
- <span data-ttu-id="c71d5-155">JT</span><span class="sxs-lookup"><span data-stu-id="c71d5-155">.JT</span></span>
- <span data-ttu-id="c71d5-156">MF1</span><span class="sxs-lookup"><span data-stu-id="c71d5-156">.MF1</span></span>
- <span data-ttu-id="c71d5-157">NEU</span><span class="sxs-lookup"><span data-stu-id="c71d5-157">.NEU</span></span>
- <span data-ttu-id="c71d5-158">PAR</span><span class="sxs-lookup"><span data-stu-id="c71d5-158">.PAR</span></span>
- <span data-ttu-id="c71d5-159">PKG</span><span class="sxs-lookup"><span data-stu-id="c71d5-159">.PKG</span></span>
- <span data-ttu-id="c71d5-160">PRC</span><span class="sxs-lookup"><span data-stu-id="c71d5-160">.PRC</span></span>
- <span data-ttu-id="c71d5-161">PRT</span><span class="sxs-lookup"><span data-stu-id="c71d5-161">.PRT</span></span>
- <span data-ttu-id="c71d5-162">PSM</span><span class="sxs-lookup"><span data-stu-id="c71d5-162">.PSM</span></span>
- <span data-ttu-id="c71d5-163">PWD</span><span class="sxs-lookup"><span data-stu-id="c71d5-163">.PWD</span></span>
- <span data-ttu-id="c71d5-164">SLD\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-164">.SLD\*</span></span>
- <span data-ttu-id="c71d5-165">STEP</span><span class="sxs-lookup"><span data-stu-id="c71d5-165">.STEP</span></span>
- <span data-ttu-id="c71d5-166">STL</span><span class="sxs-lookup"><span data-stu-id="c71d5-166">.STL</span></span>
- <span data-ttu-id="c71d5-167">STP</span><span class="sxs-lookup"><span data-stu-id="c71d5-167">.STP</span></span>
- <span data-ttu-id="c71d5-168">U3D</span><span class="sxs-lookup"><span data-stu-id="c71d5-168">.U3D</span></span>
- <span data-ttu-id="c71d5-169">UNV</span><span class="sxs-lookup"><span data-stu-id="c71d5-169">.UNV</span></span>
- <span data-ttu-id="c71d5-170">VRML</span><span class="sxs-lookup"><span data-stu-id="c71d5-170">.VRML</span></span>
- <span data-ttu-id="c71d5-171">WRL</span><span class="sxs-lookup"><span data-stu-id="c71d5-171">.WRL</span></span>
- <span data-ttu-id="c71d5-172">X_\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-172">.X_\*</span></span>
- <span data-ttu-id="c71d5-173">XAS</span><span class="sxs-lookup"><span data-stu-id="c71d5-173">.XAS</span></span>
- <span data-ttu-id="c71d5-174">XMT\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-174">.XMT\*</span></span>
- <span data-ttu-id="c71d5-175">XPR</span><span class="sxs-lookup"><span data-stu-id="c71d5-175">.XPR</span></span>

## <a name="retain-image-files"></a><span data-ttu-id="c71d5-176">Сохранить файлы изображений</span><span class="sxs-lookup"><span data-stu-id="c71d5-176">Retain image files</span></span>

<span data-ttu-id="c71d5-177">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="c71d5-177">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c71d5-178">JPEG</span><span class="sxs-lookup"><span data-stu-id="c71d5-178">.JPEG</span></span>
- <span data-ttu-id="c71d5-179">GIF</span><span class="sxs-lookup"><span data-stu-id="c71d5-179">.GIF</span></span>
- <span data-ttu-id="c71d5-180">TIF\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-180">.TIF\*</span></span>
- <span data-ttu-id="c71d5-181">BMP</span><span class="sxs-lookup"><span data-stu-id="c71d5-181">.BMP</span></span>
- <span data-ttu-id="c71d5-182">PNG</span><span class="sxs-lookup"><span data-stu-id="c71d5-182">.PNG</span></span>
- <span data-ttu-id="c71d5-183">RAW</span><span class="sxs-lookup"><span data-stu-id="c71d5-183">.RAW</span></span>
- <span data-ttu-id="c71d5-184">PSD</span><span class="sxs-lookup"><span data-stu-id="c71d5-184">.PSD</span></span>
- <span data-ttu-id="c71d5-185">PSP</span><span class="sxs-lookup"><span data-stu-id="c71d5-185">.PSP</span></span>
- <span data-ttu-id="c71d5-186">JPG</span><span class="sxs-lookup"><span data-stu-id="c71d5-186">.JPG</span></span>
- <span data-ttu-id="c71d5-187">EXIF</span><span class="sxs-lookup"><span data-stu-id="c71d5-187">.EXIF</span></span>
- <span data-ttu-id="c71d5-188">PPM</span><span class="sxs-lookup"><span data-stu-id="c71d5-188">.PPM</span></span>
- <span data-ttu-id="c71d5-189">PGM</span><span class="sxs-lookup"><span data-stu-id="c71d5-189">.PGM</span></span>
- <span data-ttu-id="c71d5-190">PBM</span><span class="sxs-lookup"><span data-stu-id="c71d5-190">.PBM</span></span>
- <span data-ttu-id="c71d5-191">PNM</span><span class="sxs-lookup"><span data-stu-id="c71d5-191">.PNM</span></span>
- <span data-ttu-id="c71d5-192">WEBP</span><span class="sxs-lookup"><span data-stu-id="c71d5-192">.WEBP</span></span>

## <a name="retain-nda-content"></a><span data-ttu-id="c71d5-193">Сохранить содержимое о неразглашении</span><span class="sxs-lookup"><span data-stu-id="c71d5-193">Retain NDA content</span></span> 

<span data-ttu-id="c71d5-194">Эта рекомендация отображается при выполнении любого из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="c71d5-194">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="c71d5-195">В тексте сообщения электронной почты обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c71d5-195">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="c71d5-196">NDA</span><span class="sxs-lookup"><span data-stu-id="c71d5-196">NDA</span></span>
    - <span data-ttu-id="c71d5-197">"Соглашение о нераспространении"</span><span class="sxs-lookup"><span data-stu-id="c71d5-197">“Non-Disclosure Agreement”</span></span>
    - <span data-ttu-id="c71d5-198">"Соглашение о неразглашении"</span><span class="sxs-lookup"><span data-stu-id="c71d5-198">“Non Disclosure Agreement”</span></span>

- <span data-ttu-id="c71d5-199">В файлах формата PDF или DOC в SharePoint или OneDrive обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="c71d5-199">Any combination of these keywords are detected in .PDF or .DOC files in SharePoint or OneDrive:</span></span>
    - <span data-ttu-id="c71d5-200">NDA</span><span class="sxs-lookup"><span data-stu-id="c71d5-200">NDA</span></span>
    - <span data-ttu-id="c71d5-201">Соглашение о неразглашении</span><span class="sxs-lookup"><span data-stu-id="c71d5-201">Non Disclosure Agreement</span></span>

## <a name="retain-software-development-files"></a><span data-ttu-id="c71d5-202">Сохранить файлы разработки программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="c71d5-202">Retain software development files</span></span>

<span data-ttu-id="c71d5-203">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="c71d5-203">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c71d5-204">ASAX</span><span class="sxs-lookup"><span data-stu-id="c71d5-204">.ASAX</span></span>
- <span data-ttu-id="c71d5-205">ASM</span><span class="sxs-lookup"><span data-stu-id="c71d5-205">.ASM</span></span>
- <span data-ttu-id="c71d5-206">ASP\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-206">.ASP\*</span></span>
- <span data-ttu-id="c71d5-207">BAT</span><span class="sxs-lookup"><span data-stu-id="c71d5-207">.BAT</span></span>
- <span data-ttu-id="c71d5-208">CONFIG</span><span class="sxs-lookup"><span data-stu-id="c71d5-208">.CONFIG</span></span>
- <span data-ttu-id="c71d5-209">CS</span><span class="sxs-lookup"><span data-stu-id="c71d5-209">.CS</span></span>
- <span data-ttu-id="c71d5-210">CSS</span><span class="sxs-lookup"><span data-stu-id="c71d5-210">.CSS</span></span>
- <span data-ttu-id="c71d5-211">DISCO</span><span class="sxs-lookup"><span data-stu-id="c71d5-211">.DISCO</span></span>
- <span data-ttu-id="c71d5-212">HTM\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-212">.HTM\*</span></span>
- <span data-ttu-id="c71d5-213">INC</span><span class="sxs-lookup"><span data-stu-id="c71d5-213">.INC</span></span>
- <span data-ttu-id="c71d5-214">JAD</span><span class="sxs-lookup"><span data-stu-id="c71d5-214">.JAD</span></span>
- <span data-ttu-id="c71d5-215">JAVA</span><span class="sxs-lookup"><span data-stu-id="c71d5-215">.JAVA</span></span>
- <span data-ttu-id="c71d5-216">JS\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-216">.JS\*</span></span>
- <span data-ttu-id="c71d5-217">LIB</span><span class="sxs-lookup"><span data-stu-id="c71d5-217">.LIB</span></span>
- <span data-ttu-id="c71d5-218">O</span><span class="sxs-lookup"><span data-stu-id="c71d5-218">.O</span></span>
- <span data-ttu-id="c71d5-219">PHP</span><span class="sxs-lookup"><span data-stu-id="c71d5-219">.PHP</span></span>
- <span data-ttu-id="c71d5-220">РК</span><span class="sxs-lookup"><span data-stu-id="c71d5-220">.RC</span></span>
- <span data-ttu-id="c71d5-221">RESX</span><span class="sxs-lookup"><span data-stu-id="c71d5-221">.RESX</span></span>
- <span data-ttu-id="c71d5-222">RPT</span><span class="sxs-lookup"><span data-stu-id="c71d5-222">.RPT</span></span>
- <span data-ttu-id="c71d5-223">RSS</span><span class="sxs-lookup"><span data-stu-id="c71d5-223">.RSS</span></span>
- <span data-ttu-id="c71d5-224">SCPT</span><span class="sxs-lookup"><span data-stu-id="c71d5-224">.SCPT</span></span>
- <span data-ttu-id="c71d5-225">SRC</span><span class="sxs-lookup"><span data-stu-id="c71d5-225">.SRC</span></span>
- <span data-ttu-id="c71d5-226">VB\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-226">.VB\*</span></span>
- <span data-ttu-id="c71d5-227">WSF</span><span class="sxs-lookup"><span data-stu-id="c71d5-227">.WSF</span></span>
- <span data-ttu-id="c71d5-228">XCODEPROJ</span><span class="sxs-lookup"><span data-stu-id="c71d5-228">.XCODEPROJ</span></span>
- <span data-ttu-id="c71d5-229">XML</span><span class="sxs-lookup"><span data-stu-id="c71d5-229">.XML</span></span>
- <span data-ttu-id="c71d5-230">XSD</span><span class="sxs-lookup"><span data-stu-id="c71d5-230">.XSD</span></span>
- <span data-ttu-id="c71d5-231">XSL\*</span><span class="sxs-lookup"><span data-stu-id="c71d5-231">.XSL\*</span></span>

## <a name="retain-video-files"></a><span data-ttu-id="c71d5-232">Сохранить видеофайлы</span><span class="sxs-lookup"><span data-stu-id="c71d5-232">Retain video files</span></span>

<span data-ttu-id="c71d5-233">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="c71d5-233">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="c71d5-234">AVCHD</span><span class="sxs-lookup"><span data-stu-id="c71d5-234">.AVCHD</span></span>
- <span data-ttu-id="c71d5-235">AVI</span><span class="sxs-lookup"><span data-stu-id="c71d5-235">.AVI</span></span>
- <span data-ttu-id="c71d5-236">FLV</span><span class="sxs-lookup"><span data-stu-id="c71d5-236">.FLV</span></span>
- <span data-ttu-id="c71d5-237">MOV</span><span class="sxs-lookup"><span data-stu-id="c71d5-237">.MOV</span></span>
- <span data-ttu-id="c71d5-238">MP2V</span><span class="sxs-lookup"><span data-stu-id="c71d5-238">.MP2V</span></span>
- <span data-ttu-id="c71d5-239">MP4</span><span class="sxs-lookup"><span data-stu-id="c71d5-239">.MP4</span></span>
- <span data-ttu-id="c71d5-240">MP4V</span><span class="sxs-lookup"><span data-stu-id="c71d5-240">.MP4V</span></span>
- <span data-ttu-id="c71d5-241">MPE</span><span class="sxs-lookup"><span data-stu-id="c71d5-241">.MPE</span></span>
- <span data-ttu-id="c71d5-242">MPEG</span><span class="sxs-lookup"><span data-stu-id="c71d5-242">.MPEG</span></span>
- <span data-ttu-id="c71d5-243">MPEG1</span><span class="sxs-lookup"><span data-stu-id="c71d5-243">.MPEG1</span></span>
- <span data-ttu-id="c71d5-244">MPEG2</span><span class="sxs-lookup"><span data-stu-id="c71d5-244">.MPEG2</span></span>
- <span data-ttu-id="c71d5-245">MPEG4</span><span class="sxs-lookup"><span data-stu-id="c71d5-245">.MPEG4</span></span>
- <span data-ttu-id="c71d5-246">MPG</span><span class="sxs-lookup"><span data-stu-id="c71d5-246">.MPG</span></span>
- <span data-ttu-id="c71d5-247">MPG2</span><span class="sxs-lookup"><span data-stu-id="c71d5-247">.MPG2</span></span>
- <span data-ttu-id="c71d5-248">MPG4</span><span class="sxs-lookup"><span data-stu-id="c71d5-248">.MPG4</span></span>
- <span data-ttu-id="c71d5-249">WMV</span><span class="sxs-lookup"><span data-stu-id="c71d5-249">.WMV</span></span>
- <span data-ttu-id="c71d5-250">XMV</span><span class="sxs-lookup"><span data-stu-id="c71d5-250">.XMV</span></span>
