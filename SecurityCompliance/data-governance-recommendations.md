---
title: Как определяется содержимое для рекомендаций по управлению данными
ms.author: brendonb
author: stephow-MSFT
manager: laurawi
ms.date: 1/15/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ROBOTS: NOINDEX, NOFOLLOW
description: Центр безопасности и соответствия требованиям Office 365 предоставляет рекомендации для управления данными на основе текущей настройки вашей организации и позволяет выполнить подготовку за пару щелчков. Некоторые из этих рекомендаций определяют конкретное содержимое в организации и указывают рекомендованные действия по управлению этим содержимым. Например, рекомендация может обнаружить элементы, содержащие важный деловой контент (например, связанные с адвокатской тайной сведения или соглашения о неразглашении) и затем позволяет автоматически присвоить метки хранения к этим элементам, чтобы обеспечить их конфиденциальность и правильное хранение. В этой статье перечислены рекомендации по управлению данными, которые вы можете встретить, и описано, какое содержимое обнаруживается для срабатывания каждой из них.
ms.openlocfilehash: a3f803105ea5c2626c8c2a26ad898df5f45af2f0
ms.sourcegitcommit: c7737903ff2e1d047682ee61f7ac21b0bdd1c6fd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "28263950"
---
# <a name="how-content-is-identified-for-data-governance-recommendations"></a><span data-ttu-id="736fc-106">Как определяется содержимое для рекомендаций по управлению данными</span><span class="sxs-lookup"><span data-stu-id="736fc-106">How content is identified for data-governance recommendations</span></span>

<span data-ttu-id="736fc-p102">Центр безопасности и соответствия требованиям Office 365 предоставляет рекомендации для управления данными на основе текущей настройки вашей организации и позволяет выполнить подготовку за пару щелчков. Некоторые из этих рекомендаций определяют конкретное содержимое в организации и указывают рекомендованные действия по управлению этим содержимым. Например, рекомендация может обнаружить элементы, содержащие важный деловой контент (например, связанные с адвокатской тайной сведения или соглашения о неразглашении) и затем позволяет автоматически присвоить метки хранения к этим элементам, чтобы обеспечить их конфиденциальность и правильное хранение.</span><span class="sxs-lookup"><span data-stu-id="736fc-p102">The Office 365 Security & Compliance Center provides recommendations for data governance based on your org's current setup and lets you set things up in a couple clicks. Some of these recommendations detect specific content in your organization and then provide recommended steps for managing that content. For example, a recommendation might detect items that contain business-critical content (such as attorney-client privilege or NDA info), and then let you automatically apply a retention label to those items to ensure that they’re classified and retained as needed.</span></span>

<span data-ttu-id="736fc-110">В этой статье перечислены рекомендации по управлению данными, которые вы можете встретить, и описано, какое содержимое обнаруживается для срабатывания каждой из них.</span><span class="sxs-lookup"><span data-stu-id="736fc-110">This topic lists the data-governance recommendations you might see and describes what content is detected to trigger each one.</span></span>

## <a name="clean-up-voicemail"></a><span data-ttu-id="736fc-111">Очистить голосовую почту</span><span class="sxs-lookup"><span data-stu-id="736fc-111">Clean up voicemail</span></span>

<span data-ttu-id="736fc-p103">Эта рекомендация отображается, если в почтовых ящиках пользователей обнаружен тип сообщений электронной почты, определенный как "голосовая почта". Узнайте больше о [свойствах сообщений в Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span><span class="sxs-lookup"><span data-stu-id="736fc-p103">This recommendation appears when email messages identified as the message type ‘voicemail’ are detected in users’ mailboxes. Learn more about [message properties in Exchange](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/ediscovery/message-properties-and-search-operators?view=exchserver-2019#searchable-properties-in-exchange).</span></span>

## <a name="label-attorney-client-privilege-content"></a><span data-ttu-id="736fc-114">Пометить контент, содержащий адвокатскую тайну</span><span class="sxs-lookup"><span data-stu-id="736fc-114">Label attorney-client privilege content</span></span> 

<span data-ttu-id="736fc-115">Эта рекомендация отображается при выполнении любого из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="736fc-115">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="736fc-116">В тексте сообщения электронной почты обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="736fc-116">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="736fc-117">ACP</span><span class="sxs-lookup"><span data-stu-id="736fc-117">ACP</span></span>
    - <span data-ttu-id="736fc-118">Общение между адвокатом и клиентом с обеспечением конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="736fc-118">Attorney Client Privilege</span></span>
    - <span data-ttu-id="736fc-119">Адвокатская тайна</span><span class="sxs-lookup"><span data-stu-id="736fc-119">Attorney-Client Privilege</span></span>
    - <span data-ttu-id="736fc-120">Конфиденциальное общение с адвокатом</span><span class="sxs-lookup"><span data-stu-id="736fc-120">Attorney-Client Privileged</span></span>

- <span data-ttu-id="736fc-121">В файлах SharePoint или OneDrive обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="736fc-121">Any combination of these keywords are detected in SharePoint or OneDrive files:</span></span>
    - <span data-ttu-id="736fc-122">ACP</span><span class="sxs-lookup"><span data-stu-id="736fc-122">ACP</span></span>
    - <span data-ttu-id="736fc-123">Общение между адвокатом и клиентом с обеспечением конфиденциальности\*</span><span class="sxs-lookup"><span data-stu-id="736fc-123">Attorney Client Privilege\*</span></span>
    - <span data-ttu-id="736fc-124">Адвокатская тайна</span><span class="sxs-lookup"><span data-stu-id="736fc-124">AC Privilege</span></span>

## <a name="retain-audio-files"></a><span data-ttu-id="736fc-125">Сохранить звуковые файлы</span><span class="sxs-lookup"><span data-stu-id="736fc-125">Retain audio files</span></span>

<span data-ttu-id="736fc-126">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="736fc-126">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="736fc-127">MP3</span><span class="sxs-lookup"><span data-stu-id="736fc-127">MP3 (default)</span></span>
- <span data-ttu-id="736fc-128">WMA</span><span class="sxs-lookup"><span data-stu-id="736fc-128">WMA</span></span>
- <span data-ttu-id="736fc-129">WAV</span><span class="sxs-lookup"><span data-stu-id="736fc-129">WAV</span></span>
- <span data-ttu-id="736fc-130">RA</span><span class="sxs-lookup"><span data-stu-id="736fc-130">.RA</span></span>
- <span data-ttu-id="736fc-131">RAM</span><span class="sxs-lookup"><span data-stu-id="736fc-131">RAM</span></span>
- <span data-ttu-id="736fc-132">RM</span><span class="sxs-lookup"><span data-stu-id="736fc-132">rm</span></span>
- <span data-ttu-id="736fc-133">MID</span><span class="sxs-lookup"><span data-stu-id="736fc-133">.MID</span></span>
- <span data-ttu-id="736fc-134">OGG</span><span class="sxs-lookup"><span data-stu-id="736fc-134">.OGG</span></span>
- <span data-ttu-id="736fc-135">AIFF</span><span class="sxs-lookup"><span data-stu-id="736fc-135">.AIFF</span></span>
- <span data-ttu-id="736fc-136">PCM</span><span class="sxs-lookup"><span data-stu-id="736fc-136">.PCM</span></span>
- <span data-ttu-id="736fc-137">AAC</span><span class="sxs-lookup"><span data-stu-id="736fc-137">.AAC</span></span>
- <span data-ttu-id="736fc-138">FLAC</span><span class="sxs-lookup"><span data-stu-id="736fc-138">.FLAC</span></span>
- <span data-ttu-id="736fc-139">ALAC</span><span class="sxs-lookup"><span data-stu-id="736fc-139">.ALAC</span></span>

## <a name="retain-cad-files"></a><span data-ttu-id="736fc-140">Сохранить файлы САПР</span><span class="sxs-lookup"><span data-stu-id="736fc-140">Retain CAD files</span></span>

<span data-ttu-id="736fc-141">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="736fc-141">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="736fc-142">3DXML</span><span class="sxs-lookup"><span data-stu-id="736fc-142">.3DXML</span></span>
- <span data-ttu-id="736fc-143">ACIS</span><span class="sxs-lookup"><span data-stu-id="736fc-143">.ACIS</span></span>
- <span data-ttu-id="736fc-144">ARC</span><span class="sxs-lookup"><span data-stu-id="736fc-144">ARC
</span></span>
- <span data-ttu-id="736fc-145">ASM</span><span class="sxs-lookup"><span data-stu-id="736fc-145">asm</span></span>
- <span data-ttu-id="736fc-146">CAT\*</span><span class="sxs-lookup"><span data-stu-id="736fc-146">cat</span></span>
- <span data-ttu-id="736fc-147">CGR</span><span class="sxs-lookup"><span data-stu-id="736fc-147">.CGR</span></span>
- <span data-ttu-id="736fc-148">DW\*</span><span class="sxs-lookup"><span data-stu-id="736fc-148">DW</span></span>
- <span data-ttu-id="736fc-149">DX\*</span><span class="sxs-lookup"><span data-stu-id="736fc-149">Dx</span></span>
- <span data-ttu-id="736fc-150">EDRW</span><span class="sxs-lookup"><span data-stu-id="736fc-150">.EDRW</span></span>
- <span data-ttu-id="736fc-151">IAM</span><span class="sxs-lookup"><span data-stu-id="736fc-151">.IAM</span></span>
- <span data-ttu-id="736fc-152">IGES</span><span class="sxs-lookup"><span data-stu-id="736fc-152">.IGES</span></span>
- <span data-ttu-id="736fc-153">IGS</span><span class="sxs-lookup"><span data-stu-id="736fc-153">.IGS</span></span>
- <span data-ttu-id="736fc-154">IPT</span><span class="sxs-lookup"><span data-stu-id="736fc-154">.IPT</span></span>
- <span data-ttu-id="736fc-155">JT</span><span class="sxs-lookup"><span data-stu-id="736fc-155">.JT</span></span>
- <span data-ttu-id="736fc-156">MF1</span><span class="sxs-lookup"><span data-stu-id="736fc-156">.MF1</span></span>
- <span data-ttu-id="736fc-157">NEU</span><span class="sxs-lookup"><span data-stu-id="736fc-157">.NEU</span></span>
- <span data-ttu-id="736fc-158">PAR</span><span class="sxs-lookup"><span data-stu-id="736fc-158">.PAR</span></span>
- <span data-ttu-id="736fc-159">PKG</span><span class="sxs-lookup"><span data-stu-id="736fc-159">.PKG</span></span>
- <span data-ttu-id="736fc-160">PRC</span><span class="sxs-lookup"><span data-stu-id="736fc-160">PRC
</span></span>
- <span data-ttu-id="736fc-161">PRT</span><span class="sxs-lookup"><span data-stu-id="736fc-161">.PRT</span></span>
- <span data-ttu-id="736fc-162">PSM</span><span class="sxs-lookup"><span data-stu-id="736fc-162">.PSM</span></span>
- <span data-ttu-id="736fc-163">PWD</span><span class="sxs-lookup"><span data-stu-id="736fc-163">.PWD</span></span>
- <span data-ttu-id="736fc-164">SLD\*</span><span class="sxs-lookup"><span data-stu-id="736fc-164">.SLD\*</span></span>
- <span data-ttu-id="736fc-165">STEP</span><span class="sxs-lookup"><span data-stu-id="736fc-165">Step</span></span>
- <span data-ttu-id="736fc-166">STL</span><span class="sxs-lookup"><span data-stu-id="736fc-166">.STL</span></span>
- <span data-ttu-id="736fc-167">STP</span><span class="sxs-lookup"><span data-stu-id="736fc-167">.STP</span></span>
- <span data-ttu-id="736fc-168">U3D</span><span class="sxs-lookup"><span data-stu-id="736fc-168">.U3D</span></span>
- <span data-ttu-id="736fc-169">UNV</span><span class="sxs-lookup"><span data-stu-id="736fc-169">.UNV</span></span>
- <span data-ttu-id="736fc-170">VRML</span><span class="sxs-lookup"><span data-stu-id="736fc-170">.VRML</span></span>
- <span data-ttu-id="736fc-171">WRL</span><span class="sxs-lookup"><span data-stu-id="736fc-171">.WRL</span></span>
- <span data-ttu-id="736fc-172">X_\*</span><span class="sxs-lookup"><span data-stu-id="736fc-172">X</span></span>
- <span data-ttu-id="736fc-173">XAS</span><span class="sxs-lookup"><span data-stu-id="736fc-173">.XAS</span></span>
- <span data-ttu-id="736fc-174">XMT\*</span><span class="sxs-lookup"><span data-stu-id="736fc-174">.XMT\*</span></span>
- <span data-ttu-id="736fc-175">XPR</span><span class="sxs-lookup"><span data-stu-id="736fc-175">.XPR</span></span>

## <a name="retain-image-files"></a><span data-ttu-id="736fc-176">Сохранить файлы изображений</span><span class="sxs-lookup"><span data-stu-id="736fc-176">Retain image files</span></span>

<span data-ttu-id="736fc-177">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="736fc-177">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="736fc-178">JPEG</span><span class="sxs-lookup"><span data-stu-id="736fc-178">JPEG</span></span>
- <span data-ttu-id="736fc-179">GIF</span><span class="sxs-lookup"><span data-stu-id="736fc-179">GIF</span></span>
- <span data-ttu-id="736fc-180">TIF\*</span><span class="sxs-lookup"><span data-stu-id="736fc-180">tif</span></span>
- <span data-ttu-id="736fc-181">BMP</span><span class="sxs-lookup"><span data-stu-id="736fc-181">.bmp</span></span>
- <span data-ttu-id="736fc-182">PNG</span><span class="sxs-lookup"><span data-stu-id="736fc-182">PNG</span></span>
- <span data-ttu-id="736fc-183">RAW</span><span class="sxs-lookup"><span data-stu-id="736fc-183">.RAW</span></span>
- <span data-ttu-id="736fc-184">PSD</span><span class="sxs-lookup"><span data-stu-id="736fc-184">.PSD</span></span>
- <span data-ttu-id="736fc-185">PSP</span><span class="sxs-lookup"><span data-stu-id="736fc-185">PSP
</span></span>
- <span data-ttu-id="736fc-186">JPG</span><span class="sxs-lookup"><span data-stu-id="736fc-186">.jpg</span></span>
- <span data-ttu-id="736fc-187">EXIF</span><span class="sxs-lookup"><span data-stu-id="736fc-187">.EXIF</span></span>
- <span data-ttu-id="736fc-188">PPM</span><span class="sxs-lookup"><span data-stu-id="736fc-188">PPM capabilities</span></span>
- <span data-ttu-id="736fc-189">PGM</span><span class="sxs-lookup"><span data-stu-id="736fc-189">.PGM</span></span>
- <span data-ttu-id="736fc-190">PBM</span><span class="sxs-lookup"><span data-stu-id="736fc-190">.PBM</span></span>
- <span data-ttu-id="736fc-191">PNM</span><span class="sxs-lookup"><span data-stu-id="736fc-191">.PNM</span></span>
- <span data-ttu-id="736fc-192">WEBP</span><span class="sxs-lookup"><span data-stu-id="736fc-192">.WEBP</span></span>

## <a name="retain-nda-content"></a><span data-ttu-id="736fc-193">Сохранить содержимое о неразглашении</span><span class="sxs-lookup"><span data-stu-id="736fc-193">Retain NDA content</span></span> 

<span data-ttu-id="736fc-194">Эта рекомендация отображается при выполнении любого из указанных ниже условий.</span><span class="sxs-lookup"><span data-stu-id="736fc-194">This recommendation appears when either of the following criteria are met.</span></span>

- <span data-ttu-id="736fc-195">В тексте сообщения электронной почты обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="736fc-195">Any of combination of these keywords is detected in the body of an email message:</span></span>
    - <span data-ttu-id="736fc-196">NDA</span><span class="sxs-lookup"><span data-stu-id="736fc-196">NDA</span></span>
    - <span data-ttu-id="736fc-197">"Соглашение о нераспространении"</span><span class="sxs-lookup"><span data-stu-id="736fc-197">“Non-Disclosure Agreement”</span></span>
    - <span data-ttu-id="736fc-198">"Соглашение о неразглашении"</span><span class="sxs-lookup"><span data-stu-id="736fc-198">“Non Disclosure Agreement”</span></span>

- <span data-ttu-id="736fc-199">В файлах формата PDF или DOC в SharePoint или OneDrive обнаружено любое сочетание этих ключевых слов:</span><span class="sxs-lookup"><span data-stu-id="736fc-199">Any combination of these keywords are detected in .PDF or .DOC files in SharePoint or OneDrive:</span></span>
    - <span data-ttu-id="736fc-200">NDA</span><span class="sxs-lookup"><span data-stu-id="736fc-200">NDA</span></span>
    - <span data-ttu-id="736fc-201">Соглашение о неразглашении</span><span class="sxs-lookup"><span data-stu-id="736fc-201">Non Disclosure Agreement</span></span>

## <a name="retain-software-development-files"></a><span data-ttu-id="736fc-202">Сохранить файлы разработки программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="736fc-202">Retain software development files</span></span>

<span data-ttu-id="736fc-203">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="736fc-203">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="736fc-204">ASAX</span><span class="sxs-lookup"><span data-stu-id="736fc-204">.ASAX</span></span>
- <span data-ttu-id="736fc-205">ASM</span><span class="sxs-lookup"><span data-stu-id="736fc-205">asm</span></span>
- <span data-ttu-id="736fc-206">ASP\*</span><span class="sxs-lookup"><span data-stu-id="736fc-206">asp</span></span>
- <span data-ttu-id="736fc-207">BAT</span><span class="sxs-lookup"><span data-stu-id="736fc-207">bat</span></span>
- <span data-ttu-id="736fc-208">CONFIG</span><span class="sxs-lookup"><span data-stu-id="736fc-208">.config</span></span>
- <span data-ttu-id="736fc-209">CS</span><span class="sxs-lookup"><span data-stu-id="736fc-209">cs</span></span>
- <span data-ttu-id="736fc-210">CSS</span><span class="sxs-lookup"><span data-stu-id="736fc-210">CSS</span></span>
- <span data-ttu-id="736fc-211">DISCO</span><span class="sxs-lookup"><span data-stu-id="736fc-211">.DISCO</span></span>
- <span data-ttu-id="736fc-212">HTM\*</span><span class="sxs-lookup"><span data-stu-id="736fc-212">htm</span></span>
- <span data-ttu-id="736fc-213">INC</span><span class="sxs-lookup"><span data-stu-id="736fc-213">.INC</span></span>
- <span data-ttu-id="736fc-214">JAD</span><span class="sxs-lookup"><span data-stu-id="736fc-214">.JAD</span></span>
- <span data-ttu-id="736fc-215">JAVA</span><span class="sxs-lookup"><span data-stu-id="736fc-215">Java</span></span>
- <span data-ttu-id="736fc-216">JS\*</span><span class="sxs-lookup"><span data-stu-id="736fc-216">.js</span></span>
- <span data-ttu-id="736fc-217">LIB</span><span class="sxs-lookup"><span data-stu-id="736fc-217">.LIB</span></span>
- <span data-ttu-id="736fc-218">O</span><span class="sxs-lookup"><span data-stu-id="736fc-218">O</span></span>
- <span data-ttu-id="736fc-219">PHP</span><span class="sxs-lookup"><span data-stu-id="736fc-219">PHP</span></span>
- <span data-ttu-id="736fc-220">РК</span><span class="sxs-lookup"><span data-stu-id="736fc-220">.RC</span></span>
- <span data-ttu-id="736fc-221">RESX</span><span class="sxs-lookup"><span data-stu-id="736fc-221">\*.resx</span></span>
- <span data-ttu-id="736fc-222">RPT</span><span class="sxs-lookup"><span data-stu-id="736fc-222">.RPT</span></span>
- <span data-ttu-id="736fc-223">RSS</span><span class="sxs-lookup"><span data-stu-id="736fc-223">RSS</span></span>
- <span data-ttu-id="736fc-224">SCPT</span><span class="sxs-lookup"><span data-stu-id="736fc-224">.SCPT</span></span>
- <span data-ttu-id="736fc-225">SRC</span><span class="sxs-lookup"><span data-stu-id="736fc-225">.SRC</span></span>
- <span data-ttu-id="736fc-226">VB\*</span><span class="sxs-lookup"><span data-stu-id="736fc-226">.vb</span></span>
- <span data-ttu-id="736fc-227">WSF</span><span class="sxs-lookup"><span data-stu-id="736fc-227">.wsf</span></span>
- <span data-ttu-id="736fc-228">XCODEPROJ</span><span class="sxs-lookup"><span data-stu-id="736fc-228">.XCODEPROJ</span></span>
- <span data-ttu-id="736fc-229">XML</span><span class="sxs-lookup"><span data-stu-id="736fc-229">XML</span></span>
- <span data-ttu-id="736fc-230">XSD</span><span class="sxs-lookup"><span data-stu-id="736fc-230">.XSD</span></span>
- <span data-ttu-id="736fc-231">XSL\*</span><span class="sxs-lookup"><span data-stu-id="736fc-231">XSL</span></span>

## <a name="retain-video-files"></a><span data-ttu-id="736fc-232">Сохранить видеофайлы</span><span class="sxs-lookup"><span data-stu-id="736fc-232">Retain video files</span></span>

<span data-ttu-id="736fc-233">Эта рекомендация отображается, если в SharePoint или OneDrive обнаружен любой из указанных ниже типов файлов.</span><span class="sxs-lookup"><span data-stu-id="736fc-233">This recommendation appears when any of the following file types are detected in SharePoint or OneDrive.</span></span>

- <span data-ttu-id="736fc-234">AVCHD</span><span class="sxs-lookup"><span data-stu-id="736fc-234">.AVCHD</span></span>
- <span data-ttu-id="736fc-235">AVI</span><span class="sxs-lookup"><span data-stu-id="736fc-235">avi</span></span>
- <span data-ttu-id="736fc-236">FLV</span><span class="sxs-lookup"><span data-stu-id="736fc-236">.FLV</span></span>
- <span data-ttu-id="736fc-237">MOV</span><span class="sxs-lookup"><span data-stu-id="736fc-237">.MOV</span></span>
- <span data-ttu-id="736fc-238">MP2V</span><span class="sxs-lookup"><span data-stu-id="736fc-238">.MP2V</span></span>
- <span data-ttu-id="736fc-239">MP4</span><span class="sxs-lookup"><span data-stu-id="736fc-239">.MP4</span></span>
- <span data-ttu-id="736fc-240">MP4V</span><span class="sxs-lookup"><span data-stu-id="736fc-240">.MP4V</span></span>
- <span data-ttu-id="736fc-241">MPE</span><span class="sxs-lookup"><span data-stu-id="736fc-241">.MPE</span></span>
- <span data-ttu-id="736fc-242">MPEG</span><span class="sxs-lookup"><span data-stu-id="736fc-242">MPEG</span></span>
- <span data-ttu-id="736fc-243">MPEG1</span><span class="sxs-lookup"><span data-stu-id="736fc-243">.MPEG1</span></span>
- <span data-ttu-id="736fc-244">MPEG2</span><span class="sxs-lookup"><span data-stu-id="736fc-244">.MPEG2</span></span>
- <span data-ttu-id="736fc-245">MPEG4</span><span class="sxs-lookup"><span data-stu-id="736fc-245">.MPEG4</span></span>
- <span data-ttu-id="736fc-246">MPG</span><span class="sxs-lookup"><span data-stu-id="736fc-246">.MPG</span></span>
- <span data-ttu-id="736fc-247">MPG2</span><span class="sxs-lookup"><span data-stu-id="736fc-247">.MPG2</span></span>
- <span data-ttu-id="736fc-248">MPG4</span><span class="sxs-lookup"><span data-stu-id="736fc-248">.MPG4</span></span>
- <span data-ttu-id="736fc-249">WMV</span><span class="sxs-lookup"><span data-stu-id="736fc-249">.WMV</span></span>
- <span data-ttu-id="736fc-250">XMV</span><span class="sxs-lookup"><span data-stu-id="736fc-250">.XMV</span></span>
