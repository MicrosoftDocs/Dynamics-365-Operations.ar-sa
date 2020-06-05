---
title: استكشاف أخطاء تحسين التخطيط وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع تحسين التخطيط.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2020
ms.locfileid: "3366991"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="6d1f9-103">استكشاف أخطاء تحسين التخطيط وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="6d1f9-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d1f9-104">يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="6d1f9-105">عدم إكمال تثبيت الوظيفة الإضافية لتحسين أداء التخطيط</span><span class="sxs-lookup"><span data-stu-id="6d1f9-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="6d1f9-106">يتطلب تحسين التخطيط توافر بيئة ذات توفر عالي الطبقة 2 أو أعلى مع تمكين Lifecycle Services (LCS) (ليست بيئة OneBox)، مع الإصدار Dynamics 365 Supply Chain Management 10.0.7 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="6d1f9-107">إذا حاولت تثبيت الوظيفة الإضافية في بيئة OneBox، فلن يكتمل التثبيت.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="6d1f9-108">**الإصلاح**: قم بإلغاء التثبيت واستخدم بيئة عالية التوافر، من الطبقة 2 أو أعلى (ليس بيئة OneBox).</span><span class="sxs-lookup"><span data-stu-id="6d1f9-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="6d1f9-109">فشل تخطيط الوظائف الدفعية عند تمكين تحسين أداء التخطيط</span><span class="sxs-lookup"><span data-stu-id="6d1f9-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="6d1f9-110">عند تمكين تحسين التخطيط، يتم تعطيل مشغل التخطيط الرئيسي المضمن تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="6d1f9-111">تفشل الوظائف الدفعة للتخطيط الرئيسي التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن إذا تم تشغيلها أثناء تكمين تحسين أداء التخطيط.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="6d1f9-112">قد تتلقي رسالة خطأ مثل *هذه العملية أطلقت عملية تخطيط رئيسي غير مدعومة عند تمكين تحسين التخطيط*.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="6d1f9-113">**الإصلاح**: قم بإلغاء كافة الوظائف الدفعية للتخطيط الرئيسي التي تم إنشاؤها لمحرك تخطيط Supply Chain Management المضمن.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="6d1f9-114">تختلف نتائج تحسين التخطيط عن النتائج السابقة</span><span class="sxs-lookup"><span data-stu-id="6d1f9-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="6d1f9-115">تختلف نتائج تحسين التخطيط عن تصميم التخطيط الرئيسي المضمن في بعض المناطق.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="6d1f9-116">ويمكن أيضًا أن يحدث ذلك بسبب الميزات المعلقة.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="6d1f9-117">**الإصلاح** : قم بتشغيل تحليل ملاءمة تحسين التخطيط ، ثم قم بتحليل النتائج في حين الرجوع إلى الوثائق ذات الصلة لفهم التأثير.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="6d1f9-118">لمزيد من المعلومات، راجع [تحليل ملائمة تحسين التخطيط](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6d1f9-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="6d1f9-119">التخطيط الرئيسي لا يحترم الحد الزمني للتغطية</span><span class="sxs-lookup"><span data-stu-id="6d1f9-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="6d1f9-120">يحدث ذلك بسبب وجود ميزة معلقة لتحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="6d1f9-121">**الإصلاح**: حتى تتوفر الميزة المعلقة، قم بتصفية الأوامر المخططة أو حذفها الإزالة اقتراحات التوريد خارج الحد الزمني للتغطية.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="6d1f9-122">لا يمكن تمكين تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="6d1f9-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="6d1f9-123">يجب أن تكون **حالة الاتصال** **متصل** قبل أن تتمكن من تعيين **استخدام تحسين التخطيط** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="6d1f9-124">لمزيد من المعلومات، راجع [الشروع في العمل مع تحسين التخطيط](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="6d1f9-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="6d1f9-125">**الإصلاح**: تأكد من تثبيت الوظيفة الإضافية لتحسين أداء التخطيط بنجاح.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="6d1f9-126">ظهور رسالة خطأ أثناء CTP</span><span class="sxs-lookup"><span data-stu-id="6d1f9-126">Error message is shown during CTP</span></span>

<span data-ttu-id="6d1f9-127">إذا حاولت تشغيل المتاح للتعهد (CTP) من أمر مبيعات عند تمكين تحسين التخطيط، ستتلقى رسالة الخطأ التالية: *هذه العملية أطلقت التخطيط الرئيسي غير المدعوم عند تمكين تحسين أداء التخطيط*.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="6d1f9-128">يرتبط هذا الأمر بميزة معلقة تم تخطيطها كجزء من دعم أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="6d1f9-129">**الإصلاح:** تجنب حسابات CTP عند تمكين تحسين أداء التخطيط حتى يتوفر دعم CTP.</span><span class="sxs-lookup"><span data-stu-id="6d1f9-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d1f9-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6d1f9-130">Additional resources</span></span>

[<span data-ttu-id="6d1f9-131">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="6d1f9-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="6d1f9-132">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="6d1f9-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
