---
title: متطلبات النظام وسياسة التحديث في Talent
description: يسرد هذا الموضوع متطلبات Dynamics 365 Talent. وقد تم أيضًا توضيح سياسة التحديث.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b8bf44fc76be968b0b04fd894c39b4c19fd374ce
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024150"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="142f0-104">متطلبات النظام وسياسة التحديث في Talent</span><span class="sxs-lookup"><span data-stu-id="142f0-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="142f0-105">يصف هذا الموضوع متطلبات Microsoft Dynamics 365 Talent، بما في ذلك Attract وOnboard وCore HR.</span><span class="sxs-lookup"><span data-stu-id="142f0-105">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="142f0-106">كما يوضح البلدان والمناطق التي يتوفر فيها Talent، بالإضافة إلى معلومات حول لغات وترجمة بيانات Talent.</span><span class="sxs-lookup"><span data-stu-id="142f0-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="142f0-107">علاوةً على ذلك، يوفر هذا الموضوع سياسة تحديث Talent.</span><span class="sxs-lookup"><span data-stu-id="142f0-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="142f0-108">مستعرضات الويب المدعومة</span><span class="sxs-lookup"><span data-stu-id="142f0-108">Supported web browsers</span></span>

<span data-ttu-id="142f0-109">يمكن تشغيل Microsoft Dynamics 365 Talent في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة:</span><span class="sxs-lookup"><span data-stu-id="142f0-109">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="142f0-110">Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10</span><span class="sxs-lookup"><span data-stu-id="142f0-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="142f0-111">Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7</span><span class="sxs-lookup"><span data-stu-id="142f0-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="142f0-112">Google Chrome (أحدث إصدار تمت إتاحته للجمهور)</span><span class="sxs-lookup"><span data-stu-id="142f0-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="142f0-113">Apple Safari (أحدث إصدار تمت إتاحته للجمهور)</span><span class="sxs-lookup"><span data-stu-id="142f0-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="142f0-114">للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج.</span><span class="sxs-lookup"><span data-stu-id="142f0-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="142f0-115">لالتقاط الصور التي تم إنشاؤها من مسجل المهام، وتضمينها في مستندات Microsoft Word، يجب عليك تثبيت ملحق Chrome.</span><span class="sxs-lookup"><span data-stu-id="142f0-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="142f0-116">تم بدء تشغيل محرر سير العمل كتطبيق ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="142f0-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="142f0-117">يدعم كل من Microsoft Edge وInternet Explorer (على إصدار معتمد من Microsoft Windows) فقط تطبيقات ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="142f0-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="142f0-118">يتطلب تطبيق ClickOnce محرر سير العمل نظام تشغيل متوافق 64 بت.</span><span class="sxs-lookup"><span data-stu-id="142f0-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="142f0-119">لمعاينة ملفات PDF، ننصح باستخدام المستعرضات الحديثة مثل Microsoft Edge (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Google Chrome (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو الكمبيوتر اللوحي Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="142f0-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="142f0-120">متطلبات الشبكة</span><span class="sxs-lookup"><span data-stu-id="142f0-120">Network requirements</span></span>
> * <span data-ttu-id="142f0-121">تم تصميم Dynamics 365 Talent للشبكات مع زمن وصول من 250-300 مللي ثانية أو أقل.</span><span class="sxs-lookup"><span data-stu-id="142f0-121">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="142f0-122">زمن الوصول هذا هو زمن الوصول من عميل المستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Talent.</span><span class="sxs-lookup"><span data-stu-id="142f0-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="142f0-123">نوصي باختبار زمن وصول الشبكة على [www.azurespeed.com](https://www.azurespeed.com "اختبار زمن وصول Azure").</span><span class="sxs-lookup"><span data-stu-id="142f0-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="142f0-124">تعتمد متطلبات عرض النطاق الترددي لتطبيق Talent على السيناريو.</span><span class="sxs-lookup"><span data-stu-id="142f0-124">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="142f0-125">تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps).</span><span class="sxs-lookup"><span data-stu-id="142f0-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="142f0-126">لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي.</span><span class="sxs-lookup"><span data-stu-id="142f0-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="142f0-127">يُصعب للغاية حساب الاستخدام المستزامن لموقع ما.</span><span class="sxs-lookup"><span data-stu-id="142f0-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="142f0-128">بالنسبة إلى العملاء المهتمين بمتطلبات النطاق الترددي، يمكنهم استخدام إصدارًا تجريبيًا من Talent.</span><span class="sxs-lookup"><span data-stu-id="142f0-128">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="142f0-129">تطبيقات Microsoft Office المدعومة</span><span class="sxs-lookup"><span data-stu-id="142f0-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="142f0-130">لتثبيت الوظائف الإضافية لكل من Microsoft Excel وWord، يجب أن يكون Microsoft Office 2016 for Windows أو Mac مثبتًا على جهازك.</span><span class="sxs-lookup"><span data-stu-id="142f0-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="142f0-131">للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف أخطاء تكامل Office‏ وإصلاحها](../dev-itpro/office-integration/office-integration-troubleshooting.md "استكشاف أخطاء تكامل Office‏ وإصلاحها").</span><span class="sxs-lookup"><span data-stu-id="142f0-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="142f0-132">لعرض المستندات التي تم إنشاؤها بواسطة وظيفة التصدير إلى Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="142f0-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="142f0-133">التوافر الإقليمي واللغات والترجمة</span><span class="sxs-lookup"><span data-stu-id="142f0-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="142f0-134">يمكنك تنزيل ملف PDF للبلدان والمناطق واللغات التي تدعم Talent في [التوافر الدولي لتطبيق Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="142f0-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="142f0-135">وعلى الرغم من ترجمة واجهة المستخدم إلى لغات أخرى، يتم تخزين كافة بيانات المستخدم باللغة التي تم إدخالها بها.</span><span class="sxs-lookup"><span data-stu-id="142f0-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="142f0-136">يمكنك إنشاء رسائل البريد الكتروني والقوالب بلغات أخرىـ ولكن بعض البيانات مثل معلومات الجدولة لا تتوفر حاليًا إلا باللغة الإنجليزية.</span><span class="sxs-lookup"><span data-stu-id="142f0-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="142f0-137">إذا كنت مطور برامج تهتم بإنشاء تخصيصات خاصة ببلد أو منطقة، أو في إنشاء حل لبلد أو منطقة لا تدعمها حاليًا Microsoft، فراجع [العولمة](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="142f0-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="142f0-138">سياسة التحديث</span><span class="sxs-lookup"><span data-stu-id="142f0-138">Update policy</span></span>

<span data-ttu-id="142f0-139">يتم تقديم الخدمات لتطبيق Talent في إطار عرض سحابي.</span><span class="sxs-lookup"><span data-stu-id="142f0-139">Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="142f0-140">تعتبر تحديثات Talent متواصلة ومطبقة بشكل تلقائي بواسطة Microsoft.</span><span class="sxs-lookup"><span data-stu-id="142f0-140">Talent updates are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="142f0-141">يتم إصدار التحديثات في وتيرة منتظمة وستتم في جميع البيئات.</span><span class="sxs-lookup"><span data-stu-id="142f0-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="142f0-142">يتم دعم Talent تماشيًا مع [دورة حياة دعم Microsoft](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "دورة حياة دعم Microsoft،") التي توفر إرشادات متناسقة ومتوقعة لتوفر دعم المنتج.</span><span class="sxs-lookup"><span data-stu-id="142f0-142">Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
