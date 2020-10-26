---
title: تحديد قواعد تغطية للأصناف
description: شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11d92185bdbcf7aa1a668b6d2aa311805e42293c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3974969"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="59458-103">تحديد قواعد تغطية للأصناف</span><span class="sxs-lookup"><span data-stu-id="59458-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59458-104">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="59458-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="59458-105">يوضح هذا الإجراء كيفية إنشاء قواعد التغطية وتجاوز إعدادات التغطية لصنف معين.</span><span class="sxs-lookup"><span data-stu-id="59458-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="59458-106">كما يوضح كيفية تعيين إعدادات المخزون الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="59458-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="59458-107">إنشاء مجموعة تغطية</span><span class="sxs-lookup"><span data-stu-id="59458-107">Create a coverage group</span></span>
1. <span data-ttu-id="59458-108">انتقل إلى **إلى جزء التنقل > الوحدات النمطية > التخطيط‏‎ الرئيسي > الإعداد > مجموعات التغطية** .</span><span class="sxs-lookup"><span data-stu-id="59458-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups** .</span></span>
2. <span data-ttu-id="59458-109">انقر فوق **جديد** .</span><span class="sxs-lookup"><span data-stu-id="59458-109">Click **New** .</span></span>
3. <span data-ttu-id="59458-110">في الحقل **مجموعة التغطية** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="59458-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="59458-111">في الحقل **الاسم** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="59458-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="59458-112">في الحقل **التقويم** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="59458-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="59458-113">اختر التقويم الذي يستخدمه التخطيط الرئيسي لإنشاء اقتراحات التزويد للعناصر في هذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="59458-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="59458-114">في الحقل **كود التغطية** ، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="59458-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="59458-115">حدد "متطلب" لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="59458-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="59458-116">في الحقل **الحد الزمني للتغطية (بالأيام)** ، أدخل "90".</span><span class="sxs-lookup"><span data-stu-id="59458-116">In the **Coverage time fence (days) field** , enter '90'.</span></span> <span data-ttu-id="59458-117">للعناصر الموجودة في هذه المجموعة، سوف ينشئ التخطيط الرئيسي اقتراحات التزويد لغاية 90 يومًا في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="59458-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="59458-118">في الحقل **الأيام السالبة‬** ، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="59458-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="59458-119">في الحقل **الأيام الموجبة‬** ، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="59458-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="59458-120">قم بتوسيع أو طي القسم **غير ذلك** .</span><span class="sxs-lookup"><span data-stu-id="59458-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="59458-121">ضمن القسم **هوامش الضمان بالأيام‬** ، في الحقل **استلام الهامش المضاف إلى تاريخ المتطلبات** ، ادخل '1'.</span><span class="sxs-lookup"><span data-stu-id="59458-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="59458-122">على سبيل المثال، إذا تم تعيين هامش الاستلام على يوم واحد وتمت جدولة بند أمر شراء لاستلامه في 15 مايو، فسيحسب التخطيط الرئيسي تاريخ الاستلام المعدل باعتباره 16 مايو.</span><span class="sxs-lookup"><span data-stu-id="59458-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="59458-123">في الحقل **إصدار الهامش المقتطع من تاريخ المتطلبات** ، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="59458-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="59458-124">على سبيل المثال، إذا تم تعيين حد الأمان‬ على يوم واحد وتمت جدولة بند أمر مبيعات للتسليم في 15 مايو، فستحسب الجدولة الرئيسية تاريخ التسليم المعدل باعتباره 14 مايو.</span><span class="sxs-lookup"><span data-stu-id="59458-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="59458-125">في الحقل **تمت إضافة ‏‫هامش حد الطلب‬ إلى وقت إنتاج الصنف** ‬، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="59458-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="59458-126">انقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="59458-126">Click **Save** .</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="59458-127">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="59458-127">Create a new product</span></span>
1. <span data-ttu-id="59458-128">‏‫انتقل إلى ‬ **جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .</span><span class="sxs-lookup"><span data-stu-id="59458-128">Go to **Navigation pane > Modules > Product information management > Products > Released products** .</span></span>
2. <span data-ttu-id="59458-129">انقر فوق **جديد** .</span><span class="sxs-lookup"><span data-stu-id="59458-129">Click **New** .</span></span>
3. <span data-ttu-id="59458-130">في الحقل **رقم المنتج** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="59458-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="59458-131">في الحقل **اسم المنتج** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="59458-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="59458-132">في الحقل **مجموعة نماذج الصنف** ، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="59458-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="59458-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="59458-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="59458-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="59458-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="59458-135">في الحقل **مجموعة الأصناف‬‬‬** ، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="59458-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="59458-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="59458-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="59458-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="59458-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="59458-138">في الحقل **مجموعة أبعاد التخزين** ، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="59458-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="59458-139">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="59458-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="59458-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="59458-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="59458-141">في الحقل **مجموعة أبعاد التعقب** ‬، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="59458-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="59458-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="59458-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="59458-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="59458-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="59458-144">انقر فوق **موافق** .</span><span class="sxs-lookup"><span data-stu-id="59458-144">Click **OK** .</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="59458-145">إعداد إعدادات الأوامر الافتراضية</span><span class="sxs-lookup"><span data-stu-id="59458-145">Setup default order settings</span></span>
1. <span data-ttu-id="59458-146">في **جزء الإجراءات** ، انقر فوق **الخطة** .</span><span class="sxs-lookup"><span data-stu-id="59458-146">On the **Action Pane** , click **Plan** .</span></span>
2. <span data-ttu-id="59458-147">ضمن **إعدادات الأوامر‬** ، انقر فوق **إعدادات الأوامر الافتراضية‬** .</span><span class="sxs-lookup"><span data-stu-id="59458-147">Under **Order settings** , click **Default order settings** .</span></span>
3. <span data-ttu-id="59458-148">ضمن **أمر الشراء** ، في حقل **الموقع الافتراضي** ، اكتب الموقع المستخدم كافتراضي عند إنشاء أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="59458-148">Under **Purchase order** , in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="59458-149">في الحقل **المستودع الافتراضي‬** ‬، اكتب الموقع الذي سيتم تخزين الصنف فيه.</span><span class="sxs-lookup"><span data-stu-id="59458-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="59458-150">قم بتوسيع أو طي قسم **المخزون** .</span><span class="sxs-lookup"><span data-stu-id="59458-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="59458-151">في الحقل **متعدد‬** ، اكتب "10".</span><span class="sxs-lookup"><span data-stu-id="59458-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="59458-152">في الحقل **الحد الأدنى لكمية الطلب** ، اكتب "10".</span><span class="sxs-lookup"><span data-stu-id="59458-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="59458-153">في الحقل **الحد الأقصى لكمية الطلب‏‎** ، اكتب "100".</span><span class="sxs-lookup"><span data-stu-id="59458-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="59458-154">في الحقل **كمية الطلب القياسية‬** ، اكتب "10".</span><span class="sxs-lookup"><span data-stu-id="59458-154">In the **Standard order quantity** , type '10'.</span></span>
10. <span data-ttu-id="59458-155">في الحقل **الحد الأدنى لوقت إنتاج المشتريات** ‬، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="59458-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="59458-156">حدد خانة الاختيار **أيام العمل** أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="59458-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="59458-157">انقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="59458-157">Click **Save** .</span></span>
13. <span data-ttu-id="59458-158">في الحقل **نوع الأمر الافتراضي** ، حدد "أمر شراء".</span><span class="sxs-lookup"><span data-stu-id="59458-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="59458-159">انقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="59458-159">Click **Save** .</span></span>
15. <span data-ttu-id="59458-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="59458-160">Close the page.</span></span> <span data-ttu-id="59458-161">قم بإغلاق صفحة ‏‫"إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="59458-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="59458-162">إضافة صنف إلى مجموعة تغطية</span><span class="sxs-lookup"><span data-stu-id="59458-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="59458-163">قم بتوسيع أو طي قسم **الخطة** .</span><span class="sxs-lookup"><span data-stu-id="59458-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="59458-164">في الحقل **مجموعة التغطية** ، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="59458-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="59458-165">في القائمة، ابحث عن **مجموعة التغطية** التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="59458-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="59458-166">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="59458-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="59458-167">إنشاء قواعد تغطية الصنف</span><span class="sxs-lookup"><span data-stu-id="59458-167">Create item coverage rules</span></span>
1. <span data-ttu-id="59458-168">في **جزء الإجراءات** ، انقر فوق **الخطة** .</span><span class="sxs-lookup"><span data-stu-id="59458-168">On the **Action Pane** , click **Plan** .</span></span>
2. <span data-ttu-id="59458-169">ضمن **التغطية** ، انقر فوق **تغطية الصنف‬** .</span><span class="sxs-lookup"><span data-stu-id="59458-169">Under **Coverage** , click **Item coverage** .</span></span>
3. <span data-ttu-id="59458-170">انقر فوق **جديد** .</span><span class="sxs-lookup"><span data-stu-id="59458-170">Click **New** .</span></span>
4. <span data-ttu-id="59458-171">انقر فوق علامة التبويب **عام** .</span><span class="sxs-lookup"><span data-stu-id="59458-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="59458-172">حدد المربع على الرأس **تجاوز إعدادات مجموعة التغطية‬** .</span><span class="sxs-lookup"><span data-stu-id="59458-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="59458-173">في الحقل **الحد الزمني للتغطية (بالأيام)** ، أدخل "60".</span><span class="sxs-lookup"><span data-stu-id="59458-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="59458-174">على الرغم من أن التخطيط لمتطلبات الأصناف الموجودة في مجموعة التغطية يتم قبل 90 يومًا، سيتم التخطيط لهذا البند قبل 60 يومًا.</span><span class="sxs-lookup"><span data-stu-id="59458-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="59458-175">في الحقل **الأيام السالبة‬** ، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="59458-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="59458-176">في الحقل **الأيام الموجبة‬** ، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="59458-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="59458-177">انقر فوق علامة التبويب **الحد الأدنى لوقت الإنتاج** .</span><span class="sxs-lookup"><span data-stu-id="59458-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="59458-178">حدد المربع على الرأس **الشراء** .</span><span class="sxs-lookup"><span data-stu-id="59458-178">Check the box on the header of **Purchase** .</span></span>
11. <span data-ttu-id="59458-179">في الحقل **وقت الشراء** ‬، أدخل "5".</span><span class="sxs-lookup"><span data-stu-id="59458-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="59458-180">انقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="59458-180">Click **Save** .</span></span>

