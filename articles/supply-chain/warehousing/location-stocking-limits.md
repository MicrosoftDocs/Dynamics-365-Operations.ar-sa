---
title: حدود مخزون الموقع
description: يصف هذا الموضوع وظيفة حدود مخزون المواقع.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e0adb9d05f0db9bbfe6bfbe72564a4e5e839f163
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004553"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="d4101-103">حدود مخزون الموقع</span><span class="sxs-lookup"><span data-stu-id="d4101-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4101-104">يمكن استخدام صفحه **حدود التخزين في الموقع** (**أداره المستودعات \> اعداد \> المستودع \> التخزين في الموقع**) للتحكم في قدره التحميل في مواقع المستودع دون الحاجة إلى استخدام العمليات الأكثر تقدما لحسابات أحجام المنتجات الفعلية.</span><span class="sxs-lookup"><span data-stu-id="d4101-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="d4101-105">ويتمثل الغرض من حدود مخزون المواقع في تقييم الحد الأقصى للكمية التي يمكن ان يحتويها الموقع.</span><span class="sxs-lookup"><span data-stu-id="d4101-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="d4101-106">يمكنك اعداد الميزة في اي مستوي من المستويات الثلاث، والتي يكون لكل منها علامة التبويب الخاصة بها في الصفحة **حدود التخزين في الموقع**:</span><span class="sxs-lookup"><span data-stu-id="d4101-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="d4101-107">المنتجات</span><span class="sxs-lookup"><span data-stu-id="d4101-107">Products</span></span>
- <span data-ttu-id="d4101-108">متغيرات المنتجات</span><span class="sxs-lookup"><span data-stu-id="d4101-108">Product variants</span></span>
- <span data-ttu-id="d4101-109">أنواع الحاويات</span><span class="sxs-lookup"><span data-stu-id="d4101-109">Container types</span></span>

<span data-ttu-id="d4101-110">بالنسبة لكل مستوي ، يمكنك تحديد قيم حقل مختلفه.</span><span class="sxs-lookup"><span data-stu-id="d4101-110">For each level, you can define different field values.</span></span> <span data-ttu-id="d4101-111">سيقوم النظام بعد ذلك بتقييم قدره موقع محدد ، استنادا إلى قيمتي **الكمية** و **الوحدة** لكل صف.</span><span class="sxs-lookup"><span data-stu-id="d4101-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="d4101-112">سيقوم أولا بتحديد سجل المطابقة المفصل.</span><span class="sxs-lookup"><span data-stu-id="d4101-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="d4101-113">علي سبيل المثال ، سيتم تقييم الصف الذي يحتوي علي قيمه في الحقل **معرف ملف التعريف الموقع** قبل صف يحتوي علي قيمه فقط في حقل **المستودع**.</span><span class="sxs-lookup"><span data-stu-id="d4101-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="d4101-114">سيتم أيضا تقييم القدرة المتبقية ، استنادا إلى قيمه **الكمية** الخاصة بسجل حد مخزون الموقع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d4101-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="d4101-115">في القسم **المنتجات** من الصفحة، يمكنك تحديد قيم الحقل التالية للبحث عن حدود التخزين في الموقع:</span><span class="sxs-lookup"><span data-stu-id="d4101-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="d4101-116">المستودع</span><span class="sxs-lookup"><span data-stu-id="d4101-116">Warehouse</span></span>
- <span data-ttu-id="d4101-117">معرف ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="d4101-117">Location profile ID</span></span>
- <span data-ttu-id="d4101-118"> الموق</span><span class="sxs-lookup"><span data-stu-id="d4101-118">Location</span></span>
- <span data-ttu-id="d4101-119">معرف فئة حجم العبوة</span><span class="sxs-lookup"><span data-stu-id="d4101-119">Pack size category ID</span></span>
- <span data-ttu-id="d4101-120">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="d4101-120">Item number</span></span>
- <span data-ttu-id="d4101-121">الوحدة</span><span class="sxs-lookup"><span data-stu-id="d4101-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="d4101-122">ليس من الضروري تحديد قيمه **الوحدة** لكل سجل من سجلات حد التخزوين في الموقع.</span><span class="sxs-lookup"><span data-stu-id="d4101-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="d4101-123">ستعتمد حسابات قدره الموقع علي كميات وحدات المخزون.</span><span class="sxs-lookup"><span data-stu-id="d4101-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="d4101-124">في حاله عدم تحديد تحويل وحده لقيمه يتم استخدامها ، سيتم تخطي سجل حد مخزون الموقع ، كما لو تم تحديد قيمه **رقم صنف** آخر لها.</span><span class="sxs-lookup"><span data-stu-id="d4101-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="d4101-125">مثال - استلام أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="d4101-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="d4101-126">يستند هذا المثال إلى مجموعه بيانات توضيحية *USMF* نظيفة، حيث يتم تعيين القيم التالية في علامة التبويب **متغيرات المنتج** من الصفحة **حدود التخزين في الموقع**.</span><span class="sxs-lookup"><span data-stu-id="d4101-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="d4101-127">المستودع</span><span class="sxs-lookup"><span data-stu-id="d4101-127">Warehouse</span></span> | <span data-ttu-id="d4101-128">معرف ملف تعريف الموقع</span><span class="sxs-lookup"><span data-stu-id="d4101-128">Location profile ID</span></span> | <span data-ttu-id="d4101-129">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="d4101-129">Item number</span></span> | <span data-ttu-id="d4101-130">الحجم</span><span class="sxs-lookup"><span data-stu-id="d4101-130">Size</span></span> | <span data-ttu-id="d4101-131">الكمية</span><span class="sxs-lookup"><span data-stu-id="d4101-131">Quantity</span></span> | <span data-ttu-id="d4101-132">الوحدة</span><span class="sxs-lookup"><span data-stu-id="d4101-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="d4101-133">24</span><span class="sxs-lookup"><span data-stu-id="d4101-133">24</span></span>        | <span data-ttu-id="d4101-134">الأرضية</span><span class="sxs-lookup"><span data-stu-id="d4101-134">FLOOR</span></span>               | <span data-ttu-id="d4101-135">D0013</span><span class="sxs-lookup"><span data-stu-id="d4101-135">D0013</span></span>       | <span data-ttu-id="d4101-136">‏‫م‬</span><span class="sxs-lookup"><span data-stu-id="d4101-136">M</span></span>    | <span data-ttu-id="d4101-137">300</span><span class="sxs-lookup"><span data-stu-id="d4101-137">300</span></span>      | <span data-ttu-id="d4101-138">وحدة</span><span class="sxs-lookup"><span data-stu-id="d4101-138">Ea</span></span>   |
| <span data-ttu-id="d4101-139">24</span><span class="sxs-lookup"><span data-stu-id="d4101-139">24</span></span>        | <span data-ttu-id="d4101-140">الأرضية</span><span class="sxs-lookup"><span data-stu-id="d4101-140">FLOOR</span></span>               | <span data-ttu-id="d4101-141">D0013</span><span class="sxs-lookup"><span data-stu-id="d4101-141">D0013</span></span>       | <span data-ttu-id="d4101-142">L</span><span class="sxs-lookup"><span data-stu-id="d4101-142">L</span></span>    | <span data-ttu-id="d4101-143">240</span><span class="sxs-lookup"><span data-stu-id="d4101-143">240</span></span>      | <span data-ttu-id="d4101-144">وحدة</span><span class="sxs-lookup"><span data-stu-id="d4101-144">Ea</span></span>   |
| <span data-ttu-id="d4101-145">24</span><span class="sxs-lookup"><span data-stu-id="d4101-145">24</span></span>        | <span data-ttu-id="d4101-146">الأرضية</span><span class="sxs-lookup"><span data-stu-id="d4101-146">FLOOR</span></span>               | <span data-ttu-id="d4101-147">D0013</span><span class="sxs-lookup"><span data-stu-id="d4101-147">D0013</span></span>       | <span data-ttu-id="d4101-148">س</span><span class="sxs-lookup"><span data-stu-id="d4101-148">S</span></span>    | <span data-ttu-id="d4101-149">360</span><span class="sxs-lookup"><span data-stu-id="d4101-149">360</span></span>      | <span data-ttu-id="d4101-150">وحدة</span><span class="sxs-lookup"><span data-stu-id="d4101-150">Ea</span></span>   |

<span data-ttu-id="d4101-151">يتم اعداد متغيرات منتجات مختلفه لوحده القياس.</span><span class="sxs-lookup"><span data-stu-id="d4101-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="d4101-152">تتم محاذاة هذه المتغيرات مع حدود مخزون الموقع لثلاث بالتات (PL):</span><span class="sxs-lookup"><span data-stu-id="d4101-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="d4101-153">**الحجم المتوسط:** 1 بالتة = 100 لكل واحدة (Ea)</span><span class="sxs-lookup"><span data-stu-id="d4101-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="d4101-154">**الحجم الكبير:** 1 بالتة = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="d4101-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="d4101-155">**الحجم الصغير:** 1 بالتة = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="d4101-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="d4101-156">ذلك، فان كل موقع يتم فيه تعيين قيمه **معرف ملف تعريف الموقع** إلى *الارضيه* يمكن ان يحمل *3* *بالتة* لرقم الصنف *D0013*.</span><span class="sxs-lookup"><span data-stu-id="d4101-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="d4101-157">تحضير للمثال</span><span class="sxs-lookup"><span data-stu-id="d4101-157">Prepare for the example</span></span>

<span data-ttu-id="d4101-158">في هذا المثال ، ستقوم بتشغيل تدفق استلام أمر شراء لبندين.</span><span class="sxs-lookup"><span data-stu-id="d4101-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="d4101-159">ومع ذلك ، يجب عليك أولا تحديث بيانات العرض التوضيحي بالطريقة التالية لضمان ان المواقع تسمح بتحويل الأصناف المختلطة ، ولا يتم استخدام الا المواقع الفارغة من *FL-002* إلى *FL-004*، ولا توجد إيه اعمال وارده مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="d4101-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="d4101-160">بالنسبة للموقع *FL-001*، قم بتغيير قيمه حقل **ملف تعريف الموقع** من *FLOOR* إلى *FLOOR-05*.</span><span class="sxs-lookup"><span data-stu-id="d4101-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="d4101-161">لملف تعريف الموقع *FLOOR*، قم بتعيين خيار **السماح بالعناصر المختلطة** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="d4101-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="d4101-162">قم بإنشاء أمر شراء يتضمن البندين التاليين:</span><span class="sxs-lookup"><span data-stu-id="d4101-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="d4101-163">المستودع</span><span class="sxs-lookup"><span data-stu-id="d4101-163">Warehouse</span></span> | <span data-ttu-id="d4101-164">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="d4101-164">Item number</span></span> | <span data-ttu-id="d4101-165">الحجم</span><span class="sxs-lookup"><span data-stu-id="d4101-165">Size</span></span> | <span data-ttu-id="d4101-166">الكمية</span><span class="sxs-lookup"><span data-stu-id="d4101-166">Quantity</span></span> | <span data-ttu-id="d4101-167">الوحدة</span><span class="sxs-lookup"><span data-stu-id="d4101-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="d4101-168">24</span><span class="sxs-lookup"><span data-stu-id="d4101-168">24</span></span>        | <span data-ttu-id="d4101-169">D0013</span><span class="sxs-lookup"><span data-stu-id="d4101-169">D0013</span></span>       | <span data-ttu-id="d4101-170">س</span><span class="sxs-lookup"><span data-stu-id="d4101-170">S</span></span>    | <span data-ttu-id="d4101-171">4</span><span class="sxs-lookup"><span data-stu-id="d4101-171">4</span></span>        | <span data-ttu-id="d4101-172">PL</span><span class="sxs-lookup"><span data-stu-id="d4101-172">PL</span></span>   |
    | <span data-ttu-id="d4101-173">24</span><span class="sxs-lookup"><span data-stu-id="d4101-173">24</span></span>        | <span data-ttu-id="d4101-174">D0013</span><span class="sxs-lookup"><span data-stu-id="d4101-174">D0013</span></span>       | <span data-ttu-id="d4101-175">L</span><span class="sxs-lookup"><span data-stu-id="d4101-175">L</span></span>    | <span data-ttu-id="d4101-176">4</span><span class="sxs-lookup"><span data-stu-id="d4101-176">4</span></span>        | <span data-ttu-id="d4101-177">PL</span><span class="sxs-lookup"><span data-stu-id="d4101-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="d4101-178">معالجة المثال</span><span class="sxs-lookup"><span data-stu-id="d4101-178">Process the example</span></span>

<span data-ttu-id="d4101-179">ستتلقى أولا كميه مقدارها *4* من الوحدة *بالتة* بالحجم *صغير*، وتقوم بمراجعه مواقع البنود الموضوعة للعمل الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d4101-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="d4101-180">ستتلقى بعد ذل كميه مقدارها *4* من الوحدة *بالتة* بالحجم *كبير*، وتقوم بمراجعه مواقع البنود الموضوعة للعمل الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d4101-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="d4101-181">في تطبيق المستودع، سجل دخولك باستخدام *24* كمعرف المستخدم و *1* ككلمة مرور.</span><span class="sxs-lookup"><span data-stu-id="d4101-181">In the warehouse app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="d4101-182">حدد **الوارد** \> **استلام الشراء**.</span><span class="sxs-lookup"><span data-stu-id="d4101-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="d4101-183">استلم *4* *بالتة* من رقم الصنف *D0013* بالحجم *صغير*.</span><span class="sxs-lookup"><span data-stu-id="d4101-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="d4101-184">قم بمراجعه عمل التخزين الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d4101-184">Review the putaway work that was created.</span></span> <span data-ttu-id="d4101-185">يجب أن تشاهد النتيجة التالية:</span><span class="sxs-lookup"><span data-stu-id="d4101-185">You should see the following result:</span></span>

    - <span data-ttu-id="d4101-186">3 بالتة -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="d4101-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="d4101-187">1 بالتة -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="d4101-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="d4101-188">استلم *4* *بالتة* من رقم الصنف *D0013* بالحجم *كبير*.</span><span class="sxs-lookup"><span data-stu-id="d4101-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="d4101-189">قم بمراجعه عمل التخزين الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d4101-189">Review the putaway work that was created.</span></span> <span data-ttu-id="d4101-190">يجب أن تشاهد النتيجة التالية:</span><span class="sxs-lookup"><span data-stu-id="d4101-190">You should see the following result:</span></span>

    - <span data-ttu-id="d4101-191">1 بالتة -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="d4101-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="d4101-192">3 بالتة -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="d4101-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="d4101-193">استنادا إلى النتائج ، قد تستنتج ان النظام فشل في تخصيص مواقع التخزين الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="d4101-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="d4101-194">والا ، لماذا قام النظام باضافه *1* *بالتة* بالحجم *كبير* إلى موقع *FL-003* في الخطوة الاخيره فقط، وليس *2* *بالتة*؟</span><span class="sxs-lookup"><span data-stu-id="d4101-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="d4101-195">وبذلك ، لماذا لا يوجد إجمالي *3* *بالتة* للتخزين في هذا الموقع؟</span><span class="sxs-lookup"><span data-stu-id="d4101-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="d4101-196">لتوضيح هذا الفشل العام ، يجب فهم معايير التحديد لحدود التخزين في الموقع.</span><span class="sxs-lookup"><span data-stu-id="d4101-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="d4101-197">سيقوم النظام أولا بتحديد سجل المطابقة المفصل.</span><span class="sxs-lookup"><span data-stu-id="d4101-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="d4101-198">في هذا المثال ، يعد السجل المطابق الأكثر تفصيلا هو البند حيث قيمة **الحجم** هي *كبير* ، وقيمه **الكمية** هي *240*، وقيمه **الوحدة** هي *Ea*.</span><span class="sxs-lookup"><span data-stu-id="d4101-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="d4101-199">نظرا لأنك تملك العمل المفتوح بالفعل من الاستلام السابق لكميه *120* *Ea* بالحجم *S*، يتم حساب القدرة المتبقية علي انها *240* – *120* = *120* *Ea*.</span><span class="sxs-lookup"><span data-stu-id="d4101-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="d4101-200">لذلك ، يمكن للقدرة المتبقية ان تحمل *1* *بالتة* بقيمة *80* *Ea*.</span><span class="sxs-lookup"><span data-stu-id="d4101-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="d4101-201">لا يمكنك استخدام حدود التخزين في الموقع للتحكم في ، علي سبيل المثال ، تزويد الأصناف التي لها كميات مختلفه في نفس الموقع.</span><span class="sxs-lookup"><span data-stu-id="d4101-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="d4101-202">في هذه الحالة ، استخدم *قالب التزويد*.</span><span class="sxs-lookup"><span data-stu-id="d4101-202">In this case, use a *replenishment template*.</span></span>
