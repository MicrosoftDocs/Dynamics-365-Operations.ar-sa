---
title: دليل استكشاف أخطاء تكامل البيانات وإصلاحها
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل البيانات وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249099"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="faaee-103">دليل استكشاف أخطاء تكامل البيانات وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="faaee-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="faaee-104">تمكين سجلات تتبع المكون الإضافي في Common Data Service وفحص تفاصيل أخطاء المكون الإضافي للكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="faaee-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="faaee-105">إذا واجهت مشكلة أو خطأ ما أثناء مزامنة لكتابة المزدوجة، فاتبع الخطوات التالية لفحص الأخطاء الموجودة في سجل التتبع.</span><span class="sxs-lookup"><span data-stu-id="faaee-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="faaee-106">قبل ان تتمكن من فحص الأخطاء، يجب تمكين سجلات تتبع المكون الإضافي.</span><span class="sxs-lookup"><span data-stu-id="faaee-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="faaee-107">للحصول على الإرشادات، راجع القسم "عرض سجلات التتبع" في [البرنامج التعليمي: كتابة مكون إضافي وتسجيله](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="faaee-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="faaee-108">الآن يمكنك فحص الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="faaee-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="faaee-109">سجل دخولك إلى Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="faaee-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="faaee-110">حدد زر **الإعدادات** (رمز الترس)، ثم حدد **الإعدادات المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="faaee-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="faaee-111">في قائمة **الإعدادات**، اختر **تخصيص \> سجل تتبع المكون الإضافي**.</span><span class="sxs-lookup"><span data-stu-id="faaee-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="faaee-112">حدد **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** كاسم النوع لإظهار تفاصيل الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="faaee-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="faaee-113">فحص أخطاء مزامنة الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="faaee-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="faaee-114">اتبع الخطوات التالية لفحص الأخطاء أثناء الاختبار.</span><span class="sxs-lookup"><span data-stu-id="faaee-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="faaee-115">سجل دخولك إلى Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="faaee-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="faaee-116">افتح مشروع LCS لإجراء اختبار الكتابة المزدوجة له.</span><span class="sxs-lookup"><span data-stu-id="faaee-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="faaee-117">حدد **بيئات مستضافة على الشبكة السحابية**.</span><span class="sxs-lookup"><span data-stu-id="faaee-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="faaee-118">أنشئ اتصال سطح مكتب بعيد بالجهاز الظاهري (VM) للتطبيق باستخدام الحساب المحلي الذي يظهر في LCS.</span><span class="sxs-lookup"><span data-stu-id="faaee-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="faaee-119">افتح عارض الأحداث.</span><span class="sxs-lookup"><span data-stu-id="faaee-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="faaee-120">انتقل إلى **سجلات التطبيقات والخدمات \> Microsoft \> Dynamics \> AX-DualWriteSync \> تشغيلي‏‎**.</span><span class="sxs-lookup"><span data-stu-id="faaee-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="faaee-121">تظهر الأخطاء والتفاصيل.</span><span class="sxs-lookup"><span data-stu-id="faaee-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="faaee-122">كيفية إلغاء ربط بيئة Common Data Service بالتطبيق وربط بيئة أخرى</span><span class="sxs-lookup"><span data-stu-id="faaee-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="faaee-123">اتبع الخطوات التالية لتحديث الارتباطات.</span><span class="sxs-lookup"><span data-stu-id="faaee-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="faaee-124">انتقل إلى بيئة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="faaee-124">Go to the application environment.</span></span>
2. <span data-ttu-id="faaee-125">افتح "إدارة البيانات".</span><span class="sxs-lookup"><span data-stu-id="faaee-125">Open Data Management.</span></span>
3. <span data-ttu-id="faaee-126">حدد **ارتباط إلى CDS للتطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="faaee-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="faaee-127">حدد جميع التعيينات قيد التشغيل، ثم حدد **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="faaee-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="faaee-128">حدد حدد جميع التعيينات، ثم حدد‏‎**حذف**.</span><span class="sxs-lookup"><span data-stu-id="faaee-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="faaee-129">لن يتوفر الخيار **حذف** إذا تم تحديد القالب **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="faaee-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="faaee-130">قم بإلغاء تحديد هذا القالب كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="faaee-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="faaee-131">القالب **CustomerV3-Account** عبارة عن قالب تم تزويده في وقت سابق ويعمل مع الحل "العميل المتوقع إلى النقدية".</span><span class="sxs-lookup"><span data-stu-id="faaee-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="faaee-132">وبسبب إصداره بشكل عمومي، يظهر تحت جميع القوالب.</span><span class="sxs-lookup"><span data-stu-id="faaee-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="faaee-133">حدد **إلغاء ربط البيئة**.</span><span class="sxs-lookup"><span data-stu-id="faaee-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="faaee-134">حدد **نعم** لتأكيد العملية.</span><span class="sxs-lookup"><span data-stu-id="faaee-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="faaee-135">لربط البيئة الجديدة، اتبع الخطوات في [دليل التثبيت](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="faaee-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
