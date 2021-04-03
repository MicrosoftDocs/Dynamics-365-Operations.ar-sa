---
title: إدارة الإصلاح
description: قم بتجميع المشكلات بشكل منظم لمساعدتك على اقتراح الحلول التي ظهر نجاحها في الماضي.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265709f298d9310d5d647eaa029ece778d2e226e
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470631"
---
# <a name="repair-management"></a><span data-ttu-id="dfe2c-103">إدارة الإصلاح</span><span class="sxs-lookup"><span data-stu-id="dfe2c-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dfe2c-104">لإدارة الإصلاح يمكنك تجميع المشكلات بشكل نظامي.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="dfe2c-105">وهذا يساعدك في اقتراح الحلول التي ظهر نجاحها في الماضي.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="dfe2c-106">قم بإعداد الأعراض والتشخيصات وإعدادات الحل.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="dfe2c-107">بعد ذلك يمكن تطبيقها كل هذا عند استلام عنصر مشابه لإصلاحه.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="dfe2c-108">يمكنك أيضًا إعداد مراحل الإصلاح والتي يمكنها متابعة تقدم إصلاح المشكلة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="dfe2c-109">إعداد إدارة الإصلاح</span><span class="sxs-lookup"><span data-stu-id="dfe2c-109">Setting up repair management</span></span>

<span data-ttu-id="dfe2c-110">استخدام نماذج الإعداد التالية لإدخال المعلومات التي سيتم استخدامها لتحديد الأعراض والتشخيص والحل للإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

- <span data-ttu-id="dfe2c-111">**إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **شروط**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-111">**Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>
- <span data-ttu-id="dfe2c-112">**إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **مناطق الأعراض**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-112">**Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>
-  <span data-ttu-id="dfe2c-113">**إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **مناطق التشخيص**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-113">**Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>
- <span data-ttu-id="dfe2c-114">**إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **الحلول**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-114">**Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>
- <span data-ttu-id="dfe2c-115">**إدارة الخدمة** \> **الإعداد** \> **الإصلاح** \> **مراحل الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-115">**Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="dfe2c-116">الأعراض والشروط</span><span class="sxs-lookup"><span data-stu-id="dfe2c-116">Symptoms and conditions</span></span>

<span data-ttu-id="dfe2c-117">تصف الأعراض يشخص العميل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="dfe2c-118">تتضمن الأعراض ملاحظات العميل التي تشير إلى الحاجة إلى الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="dfe2c-119">يمكنك إعداد مناطق الأعراض وأكوادها والحالات.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="dfe2c-120">تغطي مناطق الأعراض منطقة القصور، ويغطي كود الأعراض أعراض القصور.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="dfe2c-121">يصف الشرط الحالة أو البيئة الموجودة عند حدوث المشكلة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="dfe2c-122">**مثال**</span><span class="sxs-lookup"><span data-stu-id="dfe2c-122">**Example**</span></span>

<span data-ttu-id="dfe2c-123">إحضار كمبيوتر للإصلاح نظراً لتعطل محرك الأقراص الثابتة بعد فترة ممتدة من الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="dfe2c-124">إخفاق محرك الأقراص الثابتة يؤدي إلى خطأ شاشة زرقاء.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="dfe2c-125">أدخل الفني الذي استلم الكمبيوتر الأعراض والشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="dfe2c-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="dfe2c-126">منطقة الأعراض هي محرك الأقراص الثابتة</span><span class="sxs-lookup"><span data-stu-id="dfe2c-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="dfe2c-127">كود الأعراض هو خطأ شاشة زرقاء</span><span class="sxs-lookup"><span data-stu-id="dfe2c-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="dfe2c-128">الشرط هو تعطل القرص الثابت بعد الاستخدام لفترة طويلة</span><span class="sxs-lookup"><span data-stu-id="dfe2c-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="dfe2c-129">التشخيصات والحلول</span><span class="sxs-lookup"><span data-stu-id="dfe2c-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="dfe2c-130">تحتوي حقول التشخيص والحل على عبارات من منظور الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="dfe2c-131">وهي الخطوات التي مر بها الفني لاستقصاء المشكلة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="dfe2c-132">وتغطي منطقة التشخيصات العملية التي يجب إجراؤها لحل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="dfe2c-133">ويعتبر كود التشخيص هو كيفية معالجة المشكلة، وقد يكون الحل هو أن العنصر قد تم إصلاحه أو استبداله أو أن العميل قد قام بإلغاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="dfe2c-134">فمثلاً، إذا تم إصلاح الكمبيوتر، فقد تكون منطقة التشخيصات هي "جزء معيب"، ويكون كود التشخيص هو "تم تثبيت بطاقة فيديو جديدة"، ويكون الحل هو "تم استبداله".</span><span class="sxs-lookup"><span data-stu-id="dfe2c-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="dfe2c-135">مراحل الإصلاح</span><span class="sxs-lookup"><span data-stu-id="dfe2c-135">Repair stages</span></span>

<span data-ttu-id="dfe2c-136">تبين مراحل الإصلاح مدى التقدم في عملية الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="dfe2c-137">وتكون المحددة الخاصة بتوقيع مرحلة الإصلاح هي **منتهي** التي تشير إلى أن بند الإصلاح قد اكتمل، وقد تم تسجيل تاريخ الانتهاء ووقته.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="dfe2c-138">تطبيق إدارة الإصلاح</span><span class="sxs-lookup"><span data-stu-id="dfe2c-138">Applying repair management</span></span>

<span data-ttu-id="dfe2c-139">لتطبيق إدارة الإصلاح على أحد العناصر، يجب أن يتم إعداد هذا العنصر بعلاقة كائن الخدمة في أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="dfe2c-140">ومن أمر الخدمة يمكنك إنشاء بند إصلاح بالمعلومات حول المشكلة الحالية.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="dfe2c-141">وفي بند الإصلاح يمكنك تعريف كائن الخدمة الذي يتم إصلاحه والمعلومات حول الأعراض والتشخيص والتنفيذ.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="dfe2c-142">كما يمكنك إنشاء إشعار لبند الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="dfe2c-143">كما يمكنك إنشاء بنود إصلاح لكل خطوة في عملية الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="dfe2c-144">إنشاء بند إصلاح في أمر خدمة</span><span class="sxs-lookup"><span data-stu-id="dfe2c-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="dfe2c-145">انتقل إلى **إدارة الخدمة** \> **عام** \> **أوامر الخدمات** \> **أوامر الخدمات**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-145">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="dfe2c-146">حدد أمر الخدمة الذي يحتوي على الكائن المراد إصلاحه.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="dfe2c-147">حدد **الإصلاح** \> **بنود الإصلاح** لفتح نموذج **بنود الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-147">Select **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="dfe2c-148">حدد **جديد** لإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-148">Select **New** to create a new line.</span></span>

5.  <span data-ttu-id="dfe2c-149">حدد أحد كائنات الخدمة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-149">Select a service object.</span></span> <span data-ttu-id="dfe2c-150">يمكن تحديد أي كائن من كائنات الخدمة التي تم إعدادها بعلاقة كائن في أمر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="dfe2c-151">حدد أيًا من الأعراض أو التشخيصات أو قيم التنفيذ التي تم تعينها مسبقًا وذات الصلة في بند الإصلاح ثم حدد علامة التبويب **ملاحظة** لإنشاء ملاحظة في بند الإصلاح إذا كانت هناك حاجة إلى ذلك.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then select the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="dfe2c-152">حدد **حفظ** لحفظ بند الإصلاح الجديد.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-152">Select **Save** to save the new repair line.</span></span> <span data-ttu-id="dfe2c-153">يتم تحديث حقل **تاريخ ووقت الإنشاء‬** في علامة التبويب **عام** في النموذج **بنود الإصلاح** بوقت الحفظ.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="dfe2c-154">تعقب التقدم وحل مشكلة إصلاح</span><span class="sxs-lookup"><span data-stu-id="dfe2c-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="dfe2c-155">يمكن تعيين مراحل الإصلاح لبند الإصلاح لأجل تعقب تقدم الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="dfe2c-156">عند حل إصلاح مشكلة، يمكنك إغلاق بند الإصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="dfe2c-157">قم بتعيين مرحلة الإصلاح على مرحلة مع تمكين خاصية **منتهى**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="dfe2c-158">يتم تسجيل التاريخ والوقت الحاليين كوقت الانتهاء في البند.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="dfe2c-159">إغلاق بند الإصلاح لمشكلة تم حلها</span><span class="sxs-lookup"><span data-stu-id="dfe2c-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="dfe2c-160">افتح النموذج **بنود الإصلاح**.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="dfe2c-161">اتبع الإجراء المذكور سابقًا في هذا الموضوع لإنشاء بند إصلاح.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="dfe2c-162">حدد بند الإصلاح الذي يحتوي على المشكلة المراد إغلاقها.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="dfe2c-163">في الحقل **مرحلة الإصلاح**، حدد المرحلة التي تم تمكين الخاصية **منتهي** بها.</span><span class="sxs-lookup"><span data-stu-id="dfe2c-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]