--- 
title: "إعداد التدرج الهرمي لفئات التدبير"
description: "يوضح هذا الإجراء كيفية إنشاء عقد جديد في تدرج هرمي لفئات التدبير وكيفية تكوين فئة تدبير لاستخدامها في عملية تدبير."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="77af3-103">إعداد التدرج الهرمي لفئات التدبير</span><span class="sxs-lookup"><span data-stu-id="77af3-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="77af3-104">يوضح هذا الإجراء كيفية إنشاء عقد جديد في تدرج هرمي لفئات التدبير وكيفية تكوين فئة تدبير لاستخدامها في عملية تدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="77af3-105">وعادة ما تُنفذ هذه المهام عن طريق إدارة شراء.</span><span class="sxs-lookup"><span data-stu-id="77af3-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="77af3-106">قبل أن تتمكن من البدء في هذا الإجراء، يجب أن يكون هناك تدرج هرمي للفئات من نوع التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="77af3-107">إذا كنت تستخدم شركة عرض تقديمي للبيانات، يمكنك تنفيذ هذا الإجراء في شركة USMF.</span><span class="sxs-lookup"><span data-stu-id="77af3-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="77af3-108">أضف فئة تدبير جديدة.</span><span class="sxs-lookup"><span data-stu-id="77af3-108">Add a new procurement category</span></span>
1. <span data-ttu-id="77af3-109">انتقل إلى التدبير والتوريد > ..</span><span class="sxs-lookup"><span data-stu-id="77af3-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="77af3-110">> فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-110">> Procurement categories.</span></span>
2. <span data-ttu-id="77af3-111">انقر فوق "تحرير التدرج الهرمي للفئات".</span><span class="sxs-lookup"><span data-stu-id="77af3-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="77af3-112">يتم عرض التدرج الهرمي الحالي لفئات التدبير في الجانب الأيسر من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="77af3-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="77af3-113">أنت على وشك تعديل هرم فئات التدبير:</span><span class="sxs-lookup"><span data-stu-id="77af3-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="77af3-114">انقر فوق "عقدة فئة جديدة"</span><span class="sxs-lookup"><span data-stu-id="77af3-114">Click New category node.</span></span>
    * <span data-ttu-id="77af3-115">يحدد النظام العقدة العليا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="77af3-115">The system selects the top node by default.</span></span> <span data-ttu-id="77af3-116">إذا كنت تنفذ هذا الإجراء كدليل مهمة، يمكنك النقر فوق الزر "إلغاء التأمين" وتحديد عقدة أصلية أخرى لإدراج العقدة الجديدة بها.</span><span class="sxs-lookup"><span data-stu-id="77af3-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="77af3-117">بمجرد أن يتم ذلك، قم بتأمين "دليل المهمة" مرة أخرى وانقر فوق "عقدة الفئة الجديدة".</span><span class="sxs-lookup"><span data-stu-id="77af3-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="77af3-118">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="77af3-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="77af3-119">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="77af3-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="77af3-120">في الحقل "الاسم المألوف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="77af3-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="77af3-121">الاسم المألوف اختياري.</span><span class="sxs-lookup"><span data-stu-id="77af3-121">The friendly name is optional.</span></span> <span data-ttu-id="77af3-122">سيُعرض في عمليات البحث عن الفئات مع اسم الفئة.</span><span class="sxs-lookup"><span data-stu-id="77af3-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="77af3-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="77af3-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="77af3-124">إضافة منتجات إلى فئة التدبير الجديدة</span><span class="sxs-lookup"><span data-stu-id="77af3-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="77af3-125">انتقل إلى التدبير والتوريد > ..</span><span class="sxs-lookup"><span data-stu-id="77af3-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="77af3-126">> فئات التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-126">> Procurement categories.</span></span>
    * <span data-ttu-id="77af3-127">حدد العقدة التي أضفتها للتو.</span><span class="sxs-lookup"><span data-stu-id="77af3-127">Select the node you just added.</span></span> <span data-ttu-id="77af3-128">إذا كنت تنفذ هذا الإجراء كدليل مهمة، فقد تحتاج إلى إلغاء تأمين دليل المهمة لتحديد العقدة.</span><span class="sxs-lookup"><span data-stu-id="77af3-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="77af3-129">قم بتبديل توسيع القسم "المنتجات".</span><span class="sxs-lookup"><span data-stu-id="77af3-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="77af3-130">انقر فوق" إضافة" لربط المنتجات بفئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="77af3-131">حدد المنتج الذي تريد إضافته إلى فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="77af3-132">انقر فوق السهم لتحديد المنتج.</span><span class="sxs-lookup"><span data-stu-id="77af3-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="77af3-133">حدد منتجًا آخر تريد إضافته إلى فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="77af3-134">انقر فوق السهم لتحديد المنتج.</span><span class="sxs-lookup"><span data-stu-id="77af3-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="77af3-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="77af3-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="77af3-136">إضافة مورّدين معتمدين ومفضلين</span><span class="sxs-lookup"><span data-stu-id="77af3-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="77af3-137">بدّل توسيع المقطع "المورِّدون‬‬".</span><span class="sxs-lookup"><span data-stu-id="77af3-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="77af3-138">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="77af3-138">Click Add.</span></span>
    * <span data-ttu-id="77af3-139">يمكنك إضافة مورد لفئة تدبير وتحديد ما إذا كان أحد الموردين مفضلًا للفئة أم معتمدًا لها فقط.</span><span class="sxs-lookup"><span data-stu-id="77af3-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="77af3-140">عند حذف مورد من فئة، لا يتم حذف الحركات التاريخية الموجودة مع المورد في الفئة.</span><span class="sxs-lookup"><span data-stu-id="77af3-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="77af3-141">حدد المورد الذي تريد إضافته إلى الفئة.</span><span class="sxs-lookup"><span data-stu-id="77af3-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="77af3-142">انقر فوق السهم لتحديد المورد.</span><span class="sxs-lookup"><span data-stu-id="77af3-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="77af3-143">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="77af3-143">Click OK.</span></span>
6. <span data-ttu-id="77af3-144">حدد صف الموردين الذي تريد تعديله.</span><span class="sxs-lookup"><span data-stu-id="77af3-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="77af3-145">في الحقل "حالة المورد"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="77af3-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="77af3-146">يحدد إعداد التحديد المورد في قاعدة سياسة الفئات ما إذا كان الموردون المفضلون أو المعتمدون أو جميع الموردين متوفرين في طلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="77af3-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="77af3-147">إضافة معلومات إضافية إلى الفئة</span><span class="sxs-lookup"><span data-stu-id="77af3-147">Add additional information to the category</span></span>
1. <span data-ttu-id="77af3-148">قم بتبديل توسيع قسم "مجموعات معايير تقييم المورّد".</span><span class="sxs-lookup"><span data-stu-id="77af3-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="77af3-149">تتيح لك علامة التبويب هذه تحديد المعايير التي يجب تصنيف الموردين في فئة التدبير على أساسها.</span><span class="sxs-lookup"><span data-stu-id="77af3-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="77af3-150">للقيام بذلك، عليك بالنقر فوق "إضافة" وتحديد مجموعة تقييم مورد تحتوي على المعايير التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="77af3-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="77af3-151">قم بتبديل توسيع قسم "الاستبيانات".</span><span class="sxs-lookup"><span data-stu-id="77af3-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="77af3-152">تتيح لك علامة التبويب هذه إضافة الاستبيانات التي ستظهر في الطلب، طالما قمت بتعيين نوع النشاط على "طلب".</span><span class="sxs-lookup"><span data-stu-id="77af3-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="77af3-153">ثم يتعين على الطالب ملء استبيان قبل إرسال طلب لمنتج معين أو منتجات معينة في فئة التدبير.</span><span class="sxs-lookup"><span data-stu-id="77af3-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="77af3-154">قم بتبديل توسيع قسم مجموعات "ضرائب مبيعات الأصناف".</span><span class="sxs-lookup"><span data-stu-id="77af3-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="77af3-155">في الحقل "مجموعة ضرائب مبيعات الأصناف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="77af3-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="77af3-156">حدد مجموعة ضريبة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="77af3-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="77af3-157">قم بتبديل توسيع قسم "صفحة الفئات".</span><span class="sxs-lookup"><span data-stu-id="77af3-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="77af3-158">يتم إنشاء صفحات الفئات في صفحة التسلسل الهرمي للفئات.</span><span class="sxs-lookup"><span data-stu-id="77af3-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="77af3-159">وتتضمن هذه الصفحات معلومات حول فئة التدبير مثل معلومات عن نوع المنتجات في فئة ما أو صور المنتجات في فئة ما أو إعلانات مثل الخصومات المتوفرة في فئة.</span><span class="sxs-lookup"><span data-stu-id="77af3-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="77af3-160">تُعرض المعلومات المتوفرة في صفحة فئات بطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="77af3-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="77af3-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="77af3-161">Close the page.</span></span>


