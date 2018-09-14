--- 
title: "إنشاء طلب يستخدم طلب عرض أسعار"
description: "يوضح هذا الدليل كيفية إضافة معلومات السعر والمورّد إلى طلب شراء من عملية طلب عرض الأسعار."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="0ba73-103">إنشاء طلب يستخدم طلب عرض أسعار</span><span class="sxs-lookup"><span data-stu-id="0ba73-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ba73-104">يوضح هذا الدليل كيفية إضافة معلومات السعر والمورّد إلى طلب شراء من عملية طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="0ba73-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="0ba73-105">يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF، ويجب أن تسجل دخولك كمسؤول لإكمال كافة الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0ba73-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="0ba73-106">يقوم أخصائيو التدبير عادةً بتنفيذ المهام الموجودة في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="0ba73-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="0ba73-107">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="0ba73-107">Create a requisition</span></span>
1. <span data-ttu-id="0ba73-108">انتقل إلى التدبير والتوريد > طلبات الشراء > طلبات الشراء التي أعددتُها.</span><span class="sxs-lookup"><span data-stu-id="0ba73-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="0ba73-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0ba73-109">Click New.</span></span>
3. <span data-ttu-id="0ba73-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0ba73-111">في الحقل "تاريخ الطلب، أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="0ba73-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="0ba73-112">في الحقل "تاريخ المحاسبة" أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="0ba73-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="0ba73-113">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="0ba73-113">Click OK.</span></span>
7. <span data-ttu-id="0ba73-114">في الحقل "السبب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0ba73-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="0ba73-115">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="0ba73-115">Click Add line.</span></span>
9. <span data-ttu-id="0ba73-116">في حقل "فئة التدبير"، حدد فئة في الشجرة، ثم انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="0ba73-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="0ba73-117">في الحقل "اسم المنتج"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="0ba73-118">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0ba73-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="0ba73-119">في الحقل "وحدة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0ba73-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="0ba73-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0ba73-120">Click Save.</span></span>
14. <span data-ttu-id="0ba73-121">انقر فوق "سير العمل" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0ba73-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="0ba73-122">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="0ba73-122">Click Submit.</span></span>
16. <span data-ttu-id="0ba73-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-123">Close the page.</span></span>
17. <span data-ttu-id="0ba73-124">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="0ba73-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="0ba73-125">إعادة تعيين مهمة سير عمل</span><span class="sxs-lookup"><span data-stu-id="0ba73-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="0ba73-126">تتعلق المهمة التالية بإنشاء طلب عرض أسعار الحصول على عطاءات من مورّدي المنتج.</span><span class="sxs-lookup"><span data-stu-id="0ba73-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="0ba73-127">في بيانات العرض التوضيحي USMF، يتم إعداد سير عمل الطلب بواسطة قاعدة بحيث إذا لم يتم تحديد أي مورّد، أو إذا كان سعر الوحدة 0 لبند ما، يتم تعيين مهمة إلى عامل معين لإنشاء طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="0ba73-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="0ba73-128">لمتابعة هذا الدليل، تحتاج إلى إعادة تعيين هذه المهمة إلى مستخدم آخر (أنت).</span><span class="sxs-lookup"><span data-stu-id="0ba73-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="0ba73-129">يمكنك القيام بذلك فقط إذا سجلت دخولك كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="0ba73-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="0ba73-130">انقر فوق "سير العمل" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0ba73-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="0ba73-131">انقر فوق "عرض السجل".</span><span class="sxs-lookup"><span data-stu-id="0ba73-131">Click View history.</span></span>
3. <span data-ttu-id="0ba73-132">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-132">Refresh the page.</span></span>
4. <span data-ttu-id="0ba73-133">قم بتوسيع المقطع "تعقب التفاصيل‬".</span><span class="sxs-lookup"><span data-stu-id="0ba73-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="0ba73-134">في الشجرة، حدد "البند الذي يبدأ بـ "تم تنشيط سير عمل عنصر البند في"".</span><span class="sxs-lookup"><span data-stu-id="0ba73-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="0ba73-135">انقر فوق "عرض تفاصيل سير العمل".</span><span class="sxs-lookup"><span data-stu-id="0ba73-135">Click View workflow details.</span></span>
7. <span data-ttu-id="0ba73-136">قم بتوسيع مقطع "عناصر العمل".</span><span class="sxs-lookup"><span data-stu-id="0ba73-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="0ba73-137">انقر فوق "إعادة تعيين".</span><span class="sxs-lookup"><span data-stu-id="0ba73-137">Click Reassign.</span></span>
9. <span data-ttu-id="0ba73-138">في حقل "المستخدم"، حدد "المسؤول".</span><span class="sxs-lookup"><span data-stu-id="0ba73-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="0ba73-139">انقر فوق "إعادة تعيين".</span><span class="sxs-lookup"><span data-stu-id="0ba73-139">Click Reassign.</span></span>
11. <span data-ttu-id="0ba73-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-140">Close the page.</span></span>
12. <span data-ttu-id="0ba73-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="0ba73-142">إنشاء طلب عرض أسعار (RFQ)</span><span class="sxs-lookup"><span data-stu-id="0ba73-142">Create an RFQ</span></span>
1. <span data-ttu-id="0ba73-143">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-143">Refresh the page.</span></span>
2. <span data-ttu-id="0ba73-144">انقر فوق "طلب عرض أسعار".</span><span class="sxs-lookup"><span data-stu-id="0ba73-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="0ba73-145">في حقل "الكيان القانوني للشراء"، حدد USMF.</span><span class="sxs-lookup"><span data-stu-id="0ba73-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="0ba73-146">يجب تحديد الكيان القانوني نفسه الموجود على بند الطلب.</span><span class="sxs-lookup"><span data-stu-id="0ba73-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="0ba73-147">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0ba73-148">إذا كان لديك عدة بنود على طلب الشراء، فحدد كل البنود التي تريد إضافتها إلى طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="0ba73-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="0ba73-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0ba73-149">Click OK.</span></span>
6. <span data-ttu-id="0ba73-150">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-150">Refresh the page.</span></span>
7. <span data-ttu-id="0ba73-151">افتح مربع الحقائق، ثم قم بتوسيع مقطع "المستندات المرتبطة".</span><span class="sxs-lookup"><span data-stu-id="0ba73-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="0ba73-152">من المحتمل أن يكون مربع الحقائق مفتوحًا بشكل مسبق.</span><span class="sxs-lookup"><span data-stu-id="0ba73-152">You may already have the FactBox open.</span></span> <span data-ttu-id="0ba73-153">ابحث عن الأيقونة ذات سهم عليها، إلى يسار أزرار تبديل البنود/الرأس.</span><span class="sxs-lookup"><span data-stu-id="0ba73-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="0ba73-154">إذا كان السهم يؤشر إلى اليمين، فهذا يعني أن مربع الحقائق مفتوح بالفعل.</span><span class="sxs-lookup"><span data-stu-id="0ba73-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="0ba73-155">أما إذا كان السهم يؤشر إلى اليسار، فانقر فوقه لفتح مربع الحقائق.</span><span class="sxs-lookup"><span data-stu-id="0ba73-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="0ba73-156">انقر فوق الارتباط الموجود في حقل "طلب عرض أسعار" لفتح طلب عرض الأسعار الذي تم إنشاؤه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="0ba73-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="0ba73-157">انقر فوق "الرأس".</span><span class="sxs-lookup"><span data-stu-id="0ba73-157">Click Header.</span></span>
10. <span data-ttu-id="0ba73-158">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-158">Click Add.</span></span>
11. <span data-ttu-id="0ba73-159">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0ba73-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="0ba73-160">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-160">Click Add.</span></span>
13. <span data-ttu-id="0ba73-161">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0ba73-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="0ba73-162">انقر فوق "إرسال".</span><span class="sxs-lookup"><span data-stu-id="0ba73-162">Click Send.</span></span>
15. <span data-ttu-id="0ba73-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0ba73-163">Click OK.</span></span>
16. <span data-ttu-id="0ba73-164">انقر فوق إدخال رد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-164">Click Enter reply.</span></span>
17. <span data-ttu-id="0ba73-165">في جزء الإجراءات، انقر فوق رد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="0ba73-166">انقر فوق نسخ بيانات للرد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="0ba73-167">يؤدي ذلك إلى نسخ بيانات، مثل الكمية والتواريخ، من طلب عرض الأسعار إلى الرد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="0ba73-168">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0ba73-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="0ba73-169">هذا هو السعر الذي تلقيته من المورّد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="0ba73-170">قد تحتاج أيضًا إلى إدخال معلومات إضافية من المورّد.</span><span class="sxs-lookup"><span data-stu-id="0ba73-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="0ba73-171">انقر فوق "قبول".</span><span class="sxs-lookup"><span data-stu-id="0ba73-171">Click Accept.</span></span>
21. <span data-ttu-id="0ba73-172">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0ba73-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="0ba73-173">التأكد من تحويل المورّد والسعر إلى الطلب</span><span class="sxs-lookup"><span data-stu-id="0ba73-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="0ba73-174">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-174">Close the page.</span></span>
2. <span data-ttu-id="0ba73-175">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="0ba73-175">Click Lines.</span></span>
3. <span data-ttu-id="0ba73-176">انقر فوق "معلومات ذات صلة".</span><span class="sxs-lookup"><span data-stu-id="0ba73-176">Click Related information.</span></span>
4. <span data-ttu-id="0ba73-177">انقر فوق "طلب شراء".</span><span class="sxs-lookup"><span data-stu-id="0ba73-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="0ba73-178">حدد البند الذي تم تحويله إلى طلب عرض الأسعار (RFQ).</span><span class="sxs-lookup"><span data-stu-id="0ba73-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="0ba73-179">تأكد من نسخ السعر والمورّد إلى الطلب.</span><span class="sxs-lookup"><span data-stu-id="0ba73-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="0ba73-180">انقر فوق "سير العمل" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="0ba73-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="0ba73-181">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="0ba73-181">Click Complete.</span></span>
8. <span data-ttu-id="0ba73-182">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ba73-182">Close the page.</span></span>
9. <span data-ttu-id="0ba73-183">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="0ba73-183">Click Complete.</span></span>


