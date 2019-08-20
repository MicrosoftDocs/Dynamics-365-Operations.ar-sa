---
title: دليل استكشاف أخطاء تكامل البيانات وإصلاحها
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل البيانات وإصلاحها بين Microsoft Dynamics 365 for Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797265"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="fd70b-103">دليل استكشاف أخطاء تكامل البيانات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="fd70b-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="fd70b-104">تمكين تتبع المكون الإضافي في Common Data Service والتحقق من تفاصيل أخطاء المكون الإضافي للكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="fd70b-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="fd70b-105">إذا كنت تواجه مشكلة أو خطأ مع مزامنة الكتابة المزدوجة، يمكنك فحص الأخطاء في سجل التتبع:</span><span class="sxs-lookup"><span data-stu-id="fd70b-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="fd70b-106">قبل أن تتمكن من فحص الأخطاء، يجب تمكين تتبع المكون الإضافي باستخدام الإرشادات في [تسجيل المكون الإضافي](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) لتمكين تتبع المكون الإضافي.</span><span class="sxs-lookup"><span data-stu-id="fd70b-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="fd70b-107">الآن يمكنك فحص الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="fd70b-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="fd70b-108">سجل دخولك إلى Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="fd70b-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="fd70b-109">انقر فوق أيقونة الإعدادات (ترس)، وحدد **إعدادات متقدمة**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="fd70b-110">في قائمة **الإعدادات**، اختر **تخصيص >** سجل تتبع المكون الإضافي.</span><span class="sxs-lookup"><span data-stu-id="fd70b-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="fd70b-111">انقر فوق اسم النوع **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** لعرض تفاصيل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="fd70b-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="fd70b-112">التحقق من أخطاء مزامنة الكتابة المزدوجة في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fd70b-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="fd70b-113">يمكنك التحقق من الأخطاء أثناء الاختبار باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fd70b-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="fd70b-114">سجل دخولك إلى LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fd70b-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="fd70b-115">افتح مشروع LCS الذي اخترته لإجراء اختبار الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="fd70b-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="fd70b-116">انتقل إلى البيئات المستضافة على الشبكة السحابية.</span><span class="sxs-lookup"><span data-stu-id="fd70b-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="fd70b-117">سطح المكتب البعيد إلى Finance and Operations VM باستخدام الحساب المحلي الذي يتم عرضه في LCS.</span><span class="sxs-lookup"><span data-stu-id="fd70b-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="fd70b-118">افتح عارض الأحداث.</span><span class="sxs-lookup"><span data-stu-id="fd70b-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="fd70b-119">انتقل إلى **سجلات التطبيقات والخدمات > Microsoft > Dynamics > AX-DualWriteSync > تشغيلي**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="fd70b-120">يتم عرض الأخطاء والتفاصيل.</span><span class="sxs-lookup"><span data-stu-id="fd70b-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="fd70b-121">كيفية إلغاء ربط بيئة Common Data Service أخرى بتطبيق Finance and Operations وربطها به</span><span class="sxs-lookup"><span data-stu-id="fd70b-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="fd70b-122">يمكنك تحديث الارتباطات باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fd70b-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="fd70b-123">انتقل إلى بيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fd70b-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="fd70b-124">افتح "إدارة البيانات".</span><span class="sxs-lookup"><span data-stu-id="fd70b-124">Open Data Management.</span></span>
+ <span data-ttu-id="fd70b-125">انقر فوق **ارتباط إلى CDS للتطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="fd70b-126">حدد كافة التعيينات قيد التشغيل، وانقر فوق **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="fd70b-127">حدد كافة التعيينات، وانقر فوق **حذف**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd70b-128">لن يظهر الخيار **حذف** إذا تم تحديد القالب **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="fd70b-129">قم بإلغاء تحديده إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="fd70b-129">Unselect it if needed.</span></span> <span data-ttu-id="fd70b-130">القالب **CustomerV3-Account** عبارة عن قالب تم تزويده في وقت سابق ويعمل مع الحل "العميل المتوقع إلى النقدية".</span><span class="sxs-lookup"><span data-stu-id="fd70b-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="fd70b-131">وبسبب إصداره بشكل عمومي، تظهر جميع القوالب تحته.</span><span class="sxs-lookup"><span data-stu-id="fd70b-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="fd70b-132">انقر فوق **إلغاء ربط البيئة**.</span><span class="sxs-lookup"><span data-stu-id="fd70b-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="fd70b-133">انقر فوق **نعم** للتأكيد.</span><span class="sxs-lookup"><span data-stu-id="fd70b-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="fd70b-134">لربط البيئة الجديدة، اتبع الخطوات في [دليل التثبيت](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="fd70b-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

