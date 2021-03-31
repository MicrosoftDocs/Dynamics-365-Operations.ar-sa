---
title: إدارة الأخطاء
description: يشرح هذا الموضوع إدارة الأخطاء في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43f996921ccac0b3c85ecea2460cb9e4614f8c04
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226799"
---
# <a name="fault-management"></a><span data-ttu-id="f66b4-103">إدارة الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f66b4-104">في إدارة الأصول، يمكنك استخدام مصمم الأخطاء لإعداد أعراض الأخطاء ومجالات الأخطاء وأنواع الأخطاء على أنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="f66b4-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="f66b4-105">وبهذه الطريقة، يمكنك إدارة الأخطاء التي تم الكشف عنها في الأصول.</span><span class="sxs-lookup"><span data-stu-id="f66b4-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="f66b4-106">بالإضافة إلى ذلك، يمكن تسجيل أسباب الأخطاء والاقتراحات الخاصة بإصلاحها على أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="f66b4-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="f66b4-107">تتكون عملية تسجيل الأخطاء وإدارتها من الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f66b4-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="f66b4-108">أنشئ قائمة بأعراض الأخطاء ومجالات الأخطاء وأنواع الأخطاء التي قد تحدث على أنواع الأصول.‬</span><span class="sxs-lookup"><span data-stu-id="f66b4-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="f66b4-109">في مصمم الأخطاء، يمكنك إعداد الأعراض ومجالات وأنواع الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="f66b4-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="f66b4-110">فيما يلي بعض الأمثلة لمساعدتك على فهم الفرق بين أعراض الأخطاء ومجالات الأخطاء وأنواع الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="f66b4-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="f66b4-111">**أعراض الأخطاء**</span><span class="sxs-lookup"><span data-stu-id="f66b4-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="f66b4-112">فولتيات غير متوازنة</span><span class="sxs-lookup"><span data-stu-id="f66b4-112">Unbalanced voltages</span></span>
- <span data-ttu-id="f66b4-113">دارة قصيرة</span><span class="sxs-lookup"><span data-stu-id="f66b4-113">Short circuit</span></span>
- <span data-ttu-id="f66b4-114">الضوضاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-114">Noise</span></span>
- <span data-ttu-id="f66b4-115">تسرب</span><span class="sxs-lookup"><span data-stu-id="f66b4-115">Leak</span></span>
- <span data-ttu-id="f66b4-116">اهتزازات</span><span class="sxs-lookup"><span data-stu-id="f66b4-116">Vibrations</span></span>

<span data-ttu-id="f66b4-117">**مجالات الأخطاء.**</span><span class="sxs-lookup"><span data-stu-id="f66b4-117">**Fault areas:**</span></span>

- <span data-ttu-id="f66b4-118">كهربائية</span><span class="sxs-lookup"><span data-stu-id="f66b4-118">Electrical</span></span>
- <span data-ttu-id="f66b4-119">ميكانيكية</span><span class="sxs-lookup"><span data-stu-id="f66b4-119">Mechanical</span></span>
- <span data-ttu-id="f66b4-120">هيدروليكية</span><span class="sxs-lookup"><span data-stu-id="f66b4-120">Hydraulic</span></span>
- <span data-ttu-id="f66b4-121">هوائية</span><span class="sxs-lookup"><span data-stu-id="f66b4-121">Pneumatic</span></span>

<span data-ttu-id="f66b4-122">**أنواع الأخطاء,**</span><span class="sxs-lookup"><span data-stu-id="f66b4-122">**Fault types:**</span></span>

- <span data-ttu-id="f66b4-123">خلل في لفة الجزء الثابت الرئيسي</span><span class="sxs-lookup"><span data-stu-id="f66b4-123">Faulty main stator winding</span></span>
- <span data-ttu-id="f66b4-124">خلل في الصمام الثنائي</span><span class="sxs-lookup"><span data-stu-id="f66b4-124">Faulty diode</span></span>
- <span data-ttu-id="f66b4-125">لفات متسخة</span><span class="sxs-lookup"><span data-stu-id="f66b4-125">Dirty windings</span></span>
- <span data-ttu-id="f66b4-126">خلل في المولد</span><span class="sxs-lookup"><span data-stu-id="f66b4-126">Defective generator</span></span>
- <span data-ttu-id="f66b4-127">خلل في المستشعر</span><span class="sxs-lookup"><span data-stu-id="f66b4-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="f66b4-128">إنشاء أعراض الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-128">Create fault symptoms</span></span>

<span data-ttu-id="f66b4-129">اتبع الخطوات التالية لإنشاء قائمة بالأعراض التي يمكن استخدامها في "مصمم الأخطاء".</span><span class="sxs-lookup"><span data-stu-id="f66b4-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f66b4-130">حدد **إدارة الأصول** \> **الإعداد** \> **الخطأ** \> **أعراض الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="f66b4-131">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="f66b4-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f66b4-132">في الحقل **عَرَض الخطأ**، أدخل اسمًا لعَرَض الخطأ‏‎.</span><span class="sxs-lookup"><span data-stu-id="f66b4-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="f66b4-133">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f66b4-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f66b4-134">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="f66b4-135">إنشاء مجالات الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-135">Create fault areas</span></span>

<span data-ttu-id="f66b4-136">اتبع الخطوات التالية لإنشاء قائمة بالمجالات أو المواقع التي يمكن استخدامها في "مصمم الأخطاء".</span><span class="sxs-lookup"><span data-stu-id="f66b4-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f66b4-137">حدد **إدارة الأصول** \> **الإعداد** \> **الخطأ** \> **مجالات الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="f66b4-138">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="f66b4-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f66b4-139">في الحقل **منطقة الخطأ**، أدخل اسمًا لمنطقة الخطأ‏‎.</span><span class="sxs-lookup"><span data-stu-id="f66b4-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="f66b4-140">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f66b4-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f66b4-141">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="f66b4-142">إنشاء أنواع الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-142">Create fault types</span></span>

<span data-ttu-id="f66b4-143">اتبع الخطوات التالية لإنشاء قائمة بأنواع الأخطاء التي يمكن استخدامها في "مصمم الأخطاء".</span><span class="sxs-lookup"><span data-stu-id="f66b4-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="f66b4-144">حدد **إدارة الأصول** \> **الإعداد** \> **الخطأ** \> **أنواع الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="f66b4-145">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="f66b4-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f66b4-146">في حقل **نوع الخطأ**، أدخل اسمًا لنوع الخطأ.</span><span class="sxs-lookup"><span data-stu-id="f66b4-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="f66b4-147">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f66b4-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f66b4-148">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="f66b4-149">إعداد مصمم الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-149">Set up the fault designer</span></span>

<span data-ttu-id="f66b4-150">في مصمم الأخطاء، يمكنك إعداد بيانات الأخطاء على أنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="f66b4-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="f66b4-151">حدد **إدارة الأصول** \> **الإعداد** \> **الخطأ** \> **مصمم الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="f66b4-152">في الجزء الأيمن، حدد نوع الأصل المطلوب إعداد سجل الأخطاء له.</span><span class="sxs-lookup"><span data-stu-id="f66b4-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="f66b4-153">على علامة التبويب السريعة **عَرَض الخطأ**، حدد **إضافة بند**، ثم في حقل **عَرَض الخطأ**، حدد عَرَض الخطأ.</span><span class="sxs-lookup"><span data-stu-id="f66b4-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="f66b4-154">على علامة التبويب السريعة **مجال الخطأ**، حدد **إضافة بند**، ثم في حقل **مجال الخطأ**، حدد مجال الخطأ.</span><span class="sxs-lookup"><span data-stu-id="f66b4-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="f66b4-155">على علامة التبويب السريعة **نوع الخطأ**، حدد **إضافة بند**، ثم في حقل **نوع الخطأ**، حدد نوع الخطأ.</span><span class="sxs-lookup"><span data-stu-id="f66b4-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="f66b4-156">لإنشاء تركيبات من جميع أعراض ومجالات وأنواع الأخطاء الموجود لنوع الأصل المحدد، حدد **إنشاء تركيبات الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="f66b4-157">تكون هذه الوظيفة مفيدة عند إضافة عدد كبير من أعراض ومجالات وأنواع الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="f66b4-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="f66b4-158">من الأسهل حذف البنود لأي تركيبة غير متعلقة بنوع الأصل بدلاً من إنشاء بنود جديدة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f66b4-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f66b4-159">لنسخ إعداد اعراض ومجالات وأنواع الأخطاء من نوع أصل إلى نوع الأصل المحدد، حدد **نسخ من نوع الأصل**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="f66b4-160">حدد **حفظ** لحفظ تغييراتك.</span><span class="sxs-lookup"><span data-stu-id="f66b4-160">Select **Save** to save your changes.</span></span>

![صفحة مصمم الأخطاء](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="f66b4-162">إنشاء أسباب الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-162">Create fault causes</span></span>

<span data-ttu-id="f66b4-163">اتبع الخطوات التالية لإنشاء قائمة بأسباب الأخطاء المعروفة التي يمكن إضافتها إلى أمر عمل أو طلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="f66b4-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="f66b4-164">حدد **إدارة الأصول** \> **الإعداد** \> **الخطأ** \> **أسباب الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="f66b4-165">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="f66b4-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f66b4-166">في حقل **سبب الخطأ**، أدخل اسمًا لسبب الخطأ.</span><span class="sxs-lookup"><span data-stu-id="f66b4-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="f66b4-167">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f66b4-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f66b4-168">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="f66b4-169">إنشاء علاجات للأخطاء</span><span class="sxs-lookup"><span data-stu-id="f66b4-169">Create fault remedies</span></span>

<span data-ttu-id="f66b4-170">اتبع الخطوات التالية لإنشاء قائمة باقتراحات العلاج والإصلاح التي يمكن إضافتها إلى أمر عمل أو طلب صيانة.</span><span class="sxs-lookup"><span data-stu-id="f66b4-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="f66b4-171">حدد **إدارة الأصول** \> **الإعداد** \> **الخطأ** \> **علاجات الأخطاء**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="f66b4-172">حدد **جديد** لإنشاء سجل.</span><span class="sxs-lookup"><span data-stu-id="f66b4-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="f66b4-173">في الحقل **علاج الخطأ**، أدخل اسمًا لعلاج الخطأ‏‎.</span><span class="sxs-lookup"><span data-stu-id="f66b4-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="f66b4-174">في الحقل **الوصف**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f66b4-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="f66b4-175">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f66b4-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="f66b4-176">يمكنك تغيير أسماء أعراض ومجالات وأنواع وعلاجات الأخطاء، كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="f66b4-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="f66b4-177">وتنعكس تغييرات الأسماء بشكل تلقائي في تسجيلات الأخطاء ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="f66b4-177">The name changes are automatically reflected in the related fault registrations.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]