---
title: مجموعات جودة الصنف
description: يصف هذا الموضوع كيفيه استخدام مجموعات جوده الصنف وإنشاءها لتجميع المنتجات بشكل منطقي حتى يمكن تعيينها لعمليات اقتران الجودة لإنشاء أوامر الجودة تلقائيا.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956530"
---
# <a name="item-quality-groups"></a><span data-ttu-id="9fc8b-103">مجموعات جودة الصنف</span><span class="sxs-lookup"><span data-stu-id="9fc8b-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fc8b-104">تمثل مجموعة الجودة متطلبات الاختبار الشائعة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="9fc8b-105">يصف هذا الموضوع كيفيه استخدام مجموعات جوده الصنف وإنشاءها لتجميع المنتجات بشكل منطقي حتى يمكن تعيينها لعمليات اقتران الجودة لإنشاء أوامر الجودة تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="9fc8b-106">لإعداد العناصر التي تم تعيينها لمجموعة الجودة، أو مجموعات الجودة التي تم تعيينها لعنصر، وتحريرها وعرضها، انتقل إلى **إدارة المخزون \> الإعداد \> مجموعات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="9fc8b-107">وبعد تحديد متطلبات الاختبار في صفحة **مجموعات الاختبار**، يمكنك تحديد القواعد لإنشاء أوامر الجودة تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="9fc8b-108">ولتبسيط العملية، لا يلزمك تحديد القواعد للأصناف الفردية.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="9fc8b-109">بدلاً من ذلك، يمكنك تحديد القواعد لمجموعة الجودة في صفحة **اقترانات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="9fc8b-110">مثال لمجموعه نوعيه صنف</span><span class="sxs-lookup"><span data-stu-id="9fc8b-110">Example of an item quality group</span></span>

<span data-ttu-id="9fc8b-111">تقوم الشركة المصنعة بشراء العديد من المواد الخام المتعددة التي لها نفس متطلبات الاختبار الخاصة بالفحص الوارد.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="9fc8b-112">ولذلك، تحدد الشركة مجموعة الجودة، ثم تقوم بتعيين أرقام الأصناف المرتبطة بالمواد الخام إلى تلك المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="9fc8b-113">ولاحقاً، تشتري الشركة نوعًا جديدًا من المواد الخام له نفس متطلبات الاختبارات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="9fc8b-114">وبدلاً من إعداد متطلبات الاختبار الجديدة للمواد الجديدة، تضيف الشركة رقم الصنف للمواد الجديدة إلى مجموعة الجودة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="9fc8b-115">كما تنتج نفس الشركة الأصناف التي تشتمل على نفس متطلبات اختبارات الإنتاج وتقوم بشحن الأصناف التي تشتمل على نفس متطلبات اختبارات ما قبل الشحن.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="9fc8b-116">ولذلك، تحدد الشركة مجموعتي جودة إضافيتين، ثم تقوم بتعيين أرقام الأصناف ذات الصلة لكل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="9fc8b-117">إنشاء مجموعة جودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-117">Create a quality group</span></span>

<span data-ttu-id="9fc8b-118">لإنشاء مجموعة جودة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="9fc8b-119">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> مجموعات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="9fc8b-120">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9fc8b-121">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="9fc8b-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9fc8b-122">**مجموعه الجودة** – أدخل معرفا فريدا أو اسما لمجموعه الجودة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="9fc8b-123">**الوصف** - أدخل وصفًا مفصلاً لمجموعة الجودة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="9fc8b-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="9fc8b-125">إضافة عناصر يدويًا إلى مجموعة الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-125">Manually add items to a quality group</span></span>

<span data-ttu-id="9fc8b-126">لأضافه أصناف إلى مجموعه جوده يدويا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="9fc8b-127">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> مجموعات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="9fc8b-128">حدد مجموعه الجودة التي تريد أضافه أصناف لها.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="9fc8b-129">في جزء الإجراءات، حدد **الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="9fc8b-130">في صفحة **العناصر في مجموعات الجودة**، في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9fc8b-131">وبعد ذلك، بالنسبة للصف الجديد، قم بتعيين حقل **رقم الصنف** إلى رقم الصنف الذي تريد اضافته.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="9fc8b-132">كرر الخطوة السابقة لكل عنصر إضافي يجب عليك إضافته.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="9fc8b-133">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="9fc8b-134">إضافة عدة عناصر إلى مجموعة الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="9fc8b-135">لإضافة عناصر متعددة إلى مجموعة جودة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="9fc8b-136">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> مجموعات الجودة**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="9fc8b-137">قم بإنشاء أو تحديد مجموعة الجودة التي تريد إضافة عناصر إليها.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="9fc8b-138">في جزء الإجراءات، حدد **إضافة أصناف**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="9fc8b-139">في مربع الحوار **استعلام**، ادخل معايير عامل التصفية للأصناف التي تريد اضافتها.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="9fc8b-140">علي سبيل المثال، قد تقوم باجراء تصفيه لكافة الأصناف الموجودة في مجموعه أصناف معينه.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="9fc8b-141">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-141">Select **OK**.</span></span>
1. <span data-ttu-id="9fc8b-142">في مربع الحوار **إضافة عناصر**، تظهر الشبكة كافة العناصر التي تطابق الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="9fc8b-143">راجع النتائج.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-143">Review the results.</span></span>

    <span data-ttu-id="9fc8b-144">إذا كانت هناك إيه تغييرات مطلوبه، فحدد **تحديد** للرجوع إلى مربع الحوار **استعلام**، وقم بتعديل الاستعلام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="9fc8b-145">عندما تتضمن النتائج جميع العناصر التي تريد اضافتها، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="9fc8b-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="9fc8b-147">اقران صنف بمجموعه جوده يدويا</span><span class="sxs-lookup"><span data-stu-id="9fc8b-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="9fc8b-148">لإقران عنصر يدويًا بمجموعة جودة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="9fc8b-149">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> مجموعات جودة العناصر**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="9fc8b-150">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9fc8b-151">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="9fc8b-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9fc8b-152">**رقم الصنف** – حدد رقم الصنف المراد إضافته.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="9fc8b-153">**مجموعه الجودة** - حدد مجموعه الجودة التي سيتم تخصيصها للصنف.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="9fc8b-154">كرر الخطوة السابقة لكل مجموعه اضافيه من الأصناف ومجموعه الجودة التي يجب اضافتها.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="9fc8b-155">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="9fc8b-156">أضافه مجموعه جوده يدويا من صفحه المنتجات التي تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="9fc8b-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="9fc8b-157">لإضافة مجموعة جودة يدويًا من صفحة **المنتجات الصادرة**، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="9fc8b-158">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9fc8b-159">حدد المنتج الذي تريد تعيين مجموعة جودة له.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="9fc8b-160">في جزء الإجراءات، في مفتاح التبويب **إدارة المخزون**، في مجموعة **الجودة**، حدد **مجموعات جودة العناصر**.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="9fc8b-161">في صفحة **العناصر في مجموعات الجودة**، في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9fc8b-162">وبعد ذلك، بالنسبة للصف الجديد، قم بتعيين حقل **مجموعه الجودة** إلى مجموعه الجودة التي ترغب في تعيينها إلى المنتج.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="9fc8b-163">كرر الخطوة السابقة لكل مجموعه جوده اضافيه ترغب في تعيينها للمنتج.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="9fc8b-164">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="9fc8b-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fc8b-165">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9fc8b-165">Additional resources</span></span>

- [<span data-ttu-id="9fc8b-166">أدوات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="9fc8b-167">اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="9fc8b-168">مجموعات اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="9fc8b-169">متغيرات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="9fc8b-170">عمليات اقتران الجودة</span><span class="sxs-lookup"><span data-stu-id="9fc8b-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
