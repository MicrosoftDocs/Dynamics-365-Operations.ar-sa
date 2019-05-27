---
title: تحديد قواعد تغطية للأصناف
description: شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565639"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="9992d-103">تحديد قواعد تغطية للأصناف</span><span class="sxs-lookup"><span data-stu-id="9992d-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9992d-104">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9992d-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9992d-105">يوضح هذا الإجراء كيفية إنشاء قواعد التغطية وتجاوز إعدادات التغطية لصنف معين.</span><span class="sxs-lookup"><span data-stu-id="9992d-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="9992d-106">كما يوضح كيفية تعيين إعدادات المخزون الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="9992d-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="9992d-107">إنشاء مجموعة تغطية</span><span class="sxs-lookup"><span data-stu-id="9992d-107">Create a coverage group</span></span>
1. <span data-ttu-id="9992d-108">انتقل إلى مجموعات التغطية.</span><span class="sxs-lookup"><span data-stu-id="9992d-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="9992d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9992d-109">Click New.</span></span>
3. <span data-ttu-id="9992d-110">في الحقل "مجموعة التغطية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9992d-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="9992d-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9992d-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9992d-112">في الحقل "التقويم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9992d-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="9992d-113">اختر التقويم الذي يستخدمه التخطيط الرئيسي لإنشاء اقتراحات التزويد للعناصر في هذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="9992d-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="9992d-114">في الحقل "كود التغطية‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="9992d-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="9992d-115">حدد "متطلب" لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="9992d-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="9992d-116">في الحقل "الحد الزمني للتغطية (بالأيام)‬"، أدخل "90".</span><span class="sxs-lookup"><span data-stu-id="9992d-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="9992d-117">للعناصر الموجودة في هذه المجموعة، سوف ينشئ التخطيط الرئيسي اقتراحات التزويد لغاية 90 يومًا في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="9992d-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="9992d-118">في الحقل "الأيام السالبة‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="9992d-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="9992d-119">في الحقل "الأيام الموجبة‬‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="9992d-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="9992d-120">قم بتوسيع أو طي القسم الآخر.</span><span class="sxs-lookup"><span data-stu-id="9992d-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="9992d-121">في الحقل "استلام الهامش المضاف إلى تاريخ المتطلبات‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="9992d-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="9992d-122">على سبيل المثال، إذا تم تعيين هامش الاستلام على يوم واحد وتمت جدولة بند أمر شراء لاستلامه في 15 مايو، فسيحسب التخطيط الرئيسي تاريخ الاستلام المعدل باعتباره 16 مايو.</span><span class="sxs-lookup"><span data-stu-id="9992d-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="9992d-123">في الحقل "إصدار الهامش المقتطع من تاريخ المتطلبات‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="9992d-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="9992d-124">على سبيل المثال، إذا تم تعيين حد الأمان‬ على يوم واحد وتمت جدولة بند أمر مبيعات للتسليم في 15 مايو، فستحسب الجدولة الرئيسية تاريخ التسليم المعدل باعتباره 14 مايو.</span><span class="sxs-lookup"><span data-stu-id="9992d-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="9992d-125">في الحقل "تمت إضافة ‏‫هامش حد الطلب‬ إلى وقت إنتاج الصنف‬"، أدخل "1".</span><span class="sxs-lookup"><span data-stu-id="9992d-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="9992d-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9992d-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="9992d-127">إنشاء منتج جديد</span><span class="sxs-lookup"><span data-stu-id="9992d-127">Create a new product</span></span>
1. <span data-ttu-id="9992d-128">انتقل إلى "المنتجات الصادرة‬".</span><span class="sxs-lookup"><span data-stu-id="9992d-128">Go to Released products.</span></span>
2. <span data-ttu-id="9992d-129">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9992d-129">Click New.</span></span>
3. <span data-ttu-id="9992d-130">في الحقل "رقم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9992d-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="9992d-131">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9992d-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="9992d-132">في الحقل "مجموعة نماذج الصنف‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9992d-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9992d-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9992d-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9992d-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9992d-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9992d-135">في الحقل "مجموعة الأصناف‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9992d-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9992d-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9992d-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9992d-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9992d-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9992d-138">في الحقل "مجموعة أبعاد التخزين‬‬‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9992d-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9992d-139">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9992d-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="9992d-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9992d-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9992d-141">في الحقل "مجموعة أبعاد التعقب‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9992d-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="9992d-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9992d-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="9992d-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9992d-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9992d-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="9992d-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="9992d-145">إعداد إعدادات الأوامر الافتراضية</span><span class="sxs-lookup"><span data-stu-id="9992d-145">Setup default order settings</span></span>
1. <span data-ttu-id="9992d-146">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="9992d-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="9992d-147">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="9992d-147">Click Default order settings.</span></span>
3. <span data-ttu-id="9992d-148">في الحقل "موقع المشتريات"، اكتب الموقع المستخدم كافتراضي عند إنشاء أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="9992d-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="9992d-149">في الحقل "موقع المخزون‬"، اكتب الموقع الذي سيتم تخزين الصنف فيه.</span><span class="sxs-lookup"><span data-stu-id="9992d-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="9992d-150">قم بتوسيع أو طي قسم المخزون.</span><span class="sxs-lookup"><span data-stu-id="9992d-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="9992d-151">عيّن الخيار "متعدد" إلى "10".</span><span class="sxs-lookup"><span data-stu-id="9992d-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="9992d-152">عيّن الحد الأدنى</span><span class="sxs-lookup"><span data-stu-id="9992d-152">Set Min.</span></span> <span data-ttu-id="9992d-153">لكمية الطلب إلى "10".</span><span class="sxs-lookup"><span data-stu-id="9992d-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="9992d-154">عيّن الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="9992d-154">Set Max.</span></span> <span data-ttu-id="9992d-155">لكمية الطلب إلى "100".</span><span class="sxs-lookup"><span data-stu-id="9992d-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="9992d-156">عيّن "كمية الطلب القياسية‬" إلى "10".</span><span class="sxs-lookup"><span data-stu-id="9992d-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="9992d-157">في الحقل "الحد الأدنى لوقت إنتاج المشتريات‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9992d-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="9992d-158">حدد خانة الاختيار أيام العمل أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="9992d-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="9992d-159">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9992d-159">Click Save.</span></span>
13. <span data-ttu-id="9992d-160">في الحقل "نوع الأمر الافتراضي"، حدد "أمر شراء".</span><span class="sxs-lookup"><span data-stu-id="9992d-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="9992d-161">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9992d-161">Click Save.</span></span>
15. <span data-ttu-id="9992d-162">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9992d-162">Close the page.</span></span>
    * <span data-ttu-id="9992d-163">قم بإغلاق صفحة ‏‫"إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="9992d-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="9992d-164">إضافة صنف إلى مجموعة تغطية</span><span class="sxs-lookup"><span data-stu-id="9992d-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="9992d-165">قم بتوسيع أو طي قسم الخطة.</span><span class="sxs-lookup"><span data-stu-id="9992d-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="9992d-166">في الحقل "مجموعة التغطية"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9992d-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9992d-167">في القائمة، ابحث عن مجموعة التغطية التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="9992d-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="9992d-168">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9992d-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="9992d-169">إنشاء قواعد تغطية الصنف</span><span class="sxs-lookup"><span data-stu-id="9992d-169">Create item coverage rules</span></span>
1. <span data-ttu-id="9992d-170">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="9992d-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="9992d-171">انقر فوق "تغطية الصنف‬".</span><span class="sxs-lookup"><span data-stu-id="9992d-171">Click Item coverage.</span></span>
3. <span data-ttu-id="9992d-172">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="9992d-172">Click New.</span></span>
4. <span data-ttu-id="9992d-173">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="9992d-173">Click the General tab.</span></span>
5. <span data-ttu-id="9992d-174">حدد المربع برأس "تجاوز إعدادات مجموعة التغطية‬".</span><span class="sxs-lookup"><span data-stu-id="9992d-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="9992d-175">في الحقل "الحد الزمني للتغطية (بالأيام)‬"، أدخل "60".</span><span class="sxs-lookup"><span data-stu-id="9992d-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="9992d-176">على الرغم من أن التخطيط لمتطلبات الأصناف الموجودة في مجموعة التغطية يتم قبل 90 يومًا، سيتم التخطيط لهذا البند قبل 60 يومًا.</span><span class="sxs-lookup"><span data-stu-id="9992d-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="9992d-177">في الحقل "الأيام السالبة‬"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="9992d-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="9992d-178">في الحقل "الأيام الموجبة‬‬"، أدخل "2".</span><span class="sxs-lookup"><span data-stu-id="9992d-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="9992d-179">انقر فوق علامة التبويب "الحد الأدنى لوقت الإنتاج‬".</span><span class="sxs-lookup"><span data-stu-id="9992d-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="9992d-180">حدد المربع برأس "الشراء".</span><span class="sxs-lookup"><span data-stu-id="9992d-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="9992d-181">في الحقل "وقت الشراء‬"، أدخل "5".</span><span class="sxs-lookup"><span data-stu-id="9992d-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="9992d-182">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="9992d-182">Click Save.</span></span>

