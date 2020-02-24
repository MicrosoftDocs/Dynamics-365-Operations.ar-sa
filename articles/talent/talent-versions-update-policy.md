---
title: متطلبات نظام Talent
description: يسرد هذا الموضوع متطلبات Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
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
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006045"
---
# <a name="talent-system-requirements"></a><span data-ttu-id="1162c-103">متطلبات نظام Talent</span><span class="sxs-lookup"><span data-stu-id="1162c-103">Talent system requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1162c-104">يصف هذا الموضوع متطلبات Microsoft Dynamics 365 Talent، بما في ذلك Attract وOnboard.</span><span class="sxs-lookup"><span data-stu-id="1162c-104">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract and Onboard.</span></span> <span data-ttu-id="1162c-105">كما يوضح البلدان والمناطق التي يتوفر فيها Talent، بالإضافة إلى معلومات حول لغات وترجمة بيانات Talent.</span><span class="sxs-lookup"><span data-stu-id="1162c-105">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="1162c-106">علاوةً على ذلك، يوفر هذا الموضوع سياسة تحديث Talent.</span><span class="sxs-lookup"><span data-stu-id="1162c-106">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="1162c-107">مستعرضات الويب المدعومة</span><span class="sxs-lookup"><span data-stu-id="1162c-107">Supported web browsers</span></span>

<span data-ttu-id="1162c-108">يمكن تشغيل Microsoft Dynamics 365 Talent في أيٍّ من مستعرضات الويب التالية التي تعمل على أنظمة التشغيل المحددة:</span><span class="sxs-lookup"><span data-stu-id="1162c-108">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="1162c-109">Microsoft Edge (أحدث إصدار تمت إتاحته للجمهور) على Windows 10</span><span class="sxs-lookup"><span data-stu-id="1162c-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="1162c-110">Internet Explorer 11 على Windows 10 أو Windows 8.1 أو Windows 7</span><span class="sxs-lookup"><span data-stu-id="1162c-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="1162c-111">Google Chrome (أحدث إصدار تمت إتاحته للجمهور)</span><span class="sxs-lookup"><span data-stu-id="1162c-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="1162c-112">Apple Safari (أحدث إصدار تمت إتاحته للجمهور)</span><span class="sxs-lookup"><span data-stu-id="1162c-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="1162c-113">للعثور على أحدث إصدار لكل مستعرض ويب، انتقل إلى موقع ويب الشركة المصنعة للبرنامج.</span><span class="sxs-lookup"><span data-stu-id="1162c-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="1162c-114">لالتقاط الصور التي تم إنشاؤها من مسجل المهام، وتضمينها في مستندات Microsoft Word، يجب عليك تثبيت ملحق Chrome.</span><span class="sxs-lookup"><span data-stu-id="1162c-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="1162c-115">تم بدء تشغيل محرر سير العمل كتطبيق ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="1162c-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="1162c-116">يدعم كل من Microsoft Edge وInternet Explorer (على إصدار معتمد من Microsoft Windows) فقط تطبيقات ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="1162c-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="1162c-117">يتطلب تطبيق ClickOnce محرر سير العمل نظام تشغيل متوافق 64 بت.</span><span class="sxs-lookup"><span data-stu-id="1162c-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="1162c-118">لمعاينة ملفات PDF، ننصح باستخدام المستعرضات الحديثة مثل Microsoft Edge (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Google Chrome (آخر إصدار متوفر للجمهور) على نظام التشغيل Windows 10 أو Windows 8.1 أو Windows 8 أو Windows 7 أو الكمبيوتر اللوحي Google Nexus 10.</span><span class="sxs-lookup"><span data-stu-id="1162c-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="1162c-119">متطلبات الشبكة</span><span class="sxs-lookup"><span data-stu-id="1162c-119">Network requirements</span></span>
> * <span data-ttu-id="1162c-120">تم تصميم Dynamics 365 Talent للشبكات مع زمن وصول من 250-300 مللي ثانية أو أقل.</span><span class="sxs-lookup"><span data-stu-id="1162c-120">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="1162c-121">زمن الوصول هذا هو زمن الوصول من عميل المستعرض إلى مركز بيانات Microsoft Azure الذي يستضيف Talent.</span><span class="sxs-lookup"><span data-stu-id="1162c-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="1162c-122">نوصي باختبار زمن وصول الشبكة على [www.azurespeed.com](https://www.azurespeed.com "اختبار زمن انتقال Azure").</span><span class="sxs-lookup"><span data-stu-id="1162c-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="1162c-123">تعتمد متطلبات عرض النطاق الترددي لتطبيق Talent على السيناريو.</span><span class="sxs-lookup"><span data-stu-id="1162c-123">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="1162c-124">تتطلب السيناريوهات الأكثر شيوعاً عرض نطاق ترددي لأكثر من 50 كيلو بايت في الثانية (KBps).</span><span class="sxs-lookup"><span data-stu-id="1162c-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="1162c-125">لا تقم بحساب متطلبات النطاق الترددي من موقع عميل من خلال ضرب عدد المستخدمين في متطلبات الحد الأدنى للنطاق الترددي.</span><span class="sxs-lookup"><span data-stu-id="1162c-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="1162c-126">يُصعب للغاية حساب الاستخدام المستزامن لموقع ما.</span><span class="sxs-lookup"><span data-stu-id="1162c-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="1162c-127">بالنسبة إلى العملاء المهتمين بمتطلبات النطاق الترددي، يمكنهم استخدام إصدارًا تجريبيًا من Talent.</span><span class="sxs-lookup"><span data-stu-id="1162c-127">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="1162c-128">تطبيقات Microsoft Office المدعومة</span><span class="sxs-lookup"><span data-stu-id="1162c-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="1162c-129">لتثبيت الوظائف الإضافية لكل من Microsoft Excel وWord، يجب أن يكون Microsoft Office 2016 for Windows أو Mac مثبتًا على جهازك.</span><span class="sxs-lookup"><span data-stu-id="1162c-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="1162c-130">للحصول على مزيد من التفاصيل حول متطلبات الإصدار، راجع [استكشاف وإصلاح مشاكل تكامل Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "استكشاف أخطاء تكامل Office وإصلاحها").</span><span class="sxs-lookup"><span data-stu-id="1162c-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="1162c-131">لعرض المستندات التي تم إنشاؤها بواسطة وظيفة التصدير إلى Word أو التصدير إلى Excel، يجب عليك تثبيت Microsoft Office 2007 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="1162c-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="1162c-132">التوافر الإقليمي واللغات والترجمة</span><span class="sxs-lookup"><span data-stu-id="1162c-132">Regional availability, languages, and localization</span></span>

<span data-ttu-id="1162c-133">يمكنك تنزيل ملف PDF للبلدان والمناطق واللغات التي تدعم Talent في [التوافر الدولي لتطبيق Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="1162c-133">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="1162c-134">وعلى الرغم من ترجمة واجهة المستخدم إلى لغات أخرى، يتم تخزين كافة بيانات المستخدم باللغة التي تم إدخالها بها.</span><span class="sxs-lookup"><span data-stu-id="1162c-134">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="1162c-135">يمكنك إنشاء رسائل البريد الكتروني والقوالب بلغات أخرىـ ولكن بعض البيانات مثل معلومات الجدولة لا تتوفر حاليًا إلا باللغة الإنجليزية.</span><span class="sxs-lookup"><span data-stu-id="1162c-135">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="1162c-136">إذا كنت مطور برامج تهتم بإنشاء تخصيصات خاصة ببلد أو منطقة، أو في إنشاء حل لبلد أو منطقة لا تدعمها حاليًا Microsoft، فراجع [العولمة](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="1162c-136">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

