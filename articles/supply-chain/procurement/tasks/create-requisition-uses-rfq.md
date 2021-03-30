---
title: إنشاء طلب يستخدم طلب عرض أسعار
description: يوضح هذا الموضوع كيفية إضافة معلومات السعر والمورّد إلى طلب شراء من عملية طلب عرض الأسعار.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e67dafd02a3b2a38832d8a4f0e9809adffcbb80
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211828"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="f5934-103">إنشاء طلب يستخدم طلب عرض أسعار</span><span class="sxs-lookup"><span data-stu-id="f5934-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5934-104">يوضح هذا الموضوع كيفية إضافة معلومات السعر والمورّد إلى طلب شراء من عملية طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="f5934-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="f5934-105">يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF، ويجب أن تسجل دخولك كمسؤول لإكمال كافة الخطوات.</span><span class="sxs-lookup"><span data-stu-id="f5934-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="f5934-106">يقوم أخصائيو التدبير عادةً بتنفيذ المهام الموجودة في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="f5934-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="f5934-107">إنشاء طلب</span><span class="sxs-lookup"><span data-stu-id="f5934-107">Create a requisition</span></span>
1. <span data-ttu-id="f5934-108">في جزء التنقل، انتقل إلى **الوحدات النمطية > التدبير والتوريد‬ > طلبات الشراء > طلبات الشراء التي قمتُ بإعدادها‬**.</span><span class="sxs-lookup"><span data-stu-id="f5934-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="f5934-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f5934-109">Select **New**.</span></span>
3. <span data-ttu-id="f5934-110">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f5934-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f5934-111">في الحقل **تاريخ الطلب**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="f5934-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="f5934-112">في الحقل **تاريخ المحاسبة**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="f5934-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="f5934-113">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f5934-113">Select **OK**.</span></span>
7. <span data-ttu-id="f5934-114">في الحقل **السبب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f5934-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="f5934-115">حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="f5934-115">Select **Add line**.</span></span>
9. <span data-ttu-id="f5934-116">في حقل **فئة التدبير**، حدد فئة في الشجرة، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f5934-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="f5934-117">في الحقل **اسم المنتج**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f5934-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="f5934-118">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f5934-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="f5934-119">في الحقل **وحدة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f5934-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="f5934-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f5934-120">Select **Save**.</span></span>
14. <span data-ttu-id="f5934-121">حدد **سير العمل** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="f5934-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="f5934-122">حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="f5934-122">Select **Submit**.</span></span>
16. <span data-ttu-id="f5934-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f5934-123">Close the page.</span></span>
17. <span data-ttu-id="f5934-124">حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="f5934-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="f5934-125">إعادة تعيين مهمة سير عمل</span><span class="sxs-lookup"><span data-stu-id="f5934-125">Reassign a workflow task</span></span>
<span data-ttu-id="f5934-126">تتعلق المهمة التالية بإنشاء طلب عرض أسعار الحصول على عطاءات من مورّدي المنتج.</span><span class="sxs-lookup"><span data-stu-id="f5934-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="f5934-127">في بيانات العرض التوضيحي USMF، يتم إعداد سير عمل الطلب بواسطة قاعدة بحيث إذا لم يتم تحديد أي مورّد، أو إذا كان سعر الوحدة 0 لبند ما، يتم تعيين مهمة إلى عامل معين لإنشاء طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="f5934-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="f5934-128">لمتابعة هذا الدليل، تحتاج إلى إعادة تعيين هذه المهمة إلى مستخدم آخر (أنت).</span><span class="sxs-lookup"><span data-stu-id="f5934-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="f5934-129">يمكنك القيام بذلك فقط إذا سجلت دخولك كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="f5934-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="f5934-130">حدد **سير العمل** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="f5934-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="f5934-131">حدد **عرض المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="f5934-131">Select **View history**.</span></span>
3. <span data-ttu-id="f5934-132">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f5934-132">Refresh the page.</span></span>
4. <span data-ttu-id="f5934-133">قم بتوسيع القسم **تعقب التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="f5934-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="f5934-134">في الشجرة، حدد البند الذي يبدأ بـ "تم تنشيط سير عمل عنصر البند في".‬</span><span class="sxs-lookup"><span data-stu-id="f5934-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="f5934-135">حدد **عرض تفاصيل سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="f5934-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="f5934-136">قم بتوسيع القسم **عناصر العمل**.</span><span class="sxs-lookup"><span data-stu-id="f5934-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="f5934-137">حدد **إعادة تعيين**.</span><span class="sxs-lookup"><span data-stu-id="f5934-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="f5934-138">في حقل **المستخدم**، حدد **المسؤول**.</span><span class="sxs-lookup"><span data-stu-id="f5934-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="f5934-139">حدد **إعادة تعيين**.</span><span class="sxs-lookup"><span data-stu-id="f5934-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="f5934-140">قم بإغلاق الصفحتين.</span><span class="sxs-lookup"><span data-stu-id="f5934-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="f5934-141">إنشاء طلب عرض أسعار (RFQ)</span><span class="sxs-lookup"><span data-stu-id="f5934-141">Create an RFQ</span></span>

1. <span data-ttu-id="f5934-142">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f5934-142">Refresh the page.</span></span>
2. <span data-ttu-id="f5934-143">حدد **طلب عرض أسعار**.</span><span class="sxs-lookup"><span data-stu-id="f5934-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="f5934-144">في حقل **الكيان القانوني للشراء**، حدد **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f5934-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="f5934-145">يجب تحديد الكيان القانوني نفسه الموجود على بند الطلب.</span><span class="sxs-lookup"><span data-stu-id="f5934-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="f5934-146">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f5934-146">In the list, mark the selected row.</span></span> <span data-ttu-id="f5934-147">إذا كان لديك عدة بنود على طلب الشراء، فحدد كل البنود التي تريد إضافتها إلى طلب عرض الأسعار.</span><span class="sxs-lookup"><span data-stu-id="f5934-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="f5934-148">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f5934-148">Select **OK**.</span></span>
6. <span data-ttu-id="f5934-149">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f5934-149">Refresh the page.</span></span>
7. <span data-ttu-id="f5934-150">افتح مربع الحقائق، ثم قم بتوسيع قسم **المستندات المرتبطة**.</span><span class="sxs-lookup"><span data-stu-id="f5934-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="f5934-151">حدد الارتباط الموجود في حقل **طلب عرض أسعار** لفتح طلب عرض الأسعار الذي تم إنشاؤه للتوّ.</span><span class="sxs-lookup"><span data-stu-id="f5934-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="f5934-152">حدد **الرأس**.</span><span class="sxs-lookup"><span data-stu-id="f5934-152">Select **Header**.</span></span>
10. <span data-ttu-id="f5934-153">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f5934-153">Select **Add**.</span></span>
11. <span data-ttu-id="f5934-154">في الحقل **حساب المورد**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f5934-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="f5934-155">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f5934-155">Select **Add**.</span></span>
13. <span data-ttu-id="f5934-156">في الحقل **حساب المورد**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f5934-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="f5934-157">حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="f5934-157">Select **Send**.</span></span>
15. <span data-ttu-id="f5934-158">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f5934-158">Select **OK**.</span></span>
16. <span data-ttu-id="f5934-159">حدد **إدخال رد‬**.</span><span class="sxs-lookup"><span data-stu-id="f5934-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="f5934-160">في جزء الإجراءات، حدد **رد**.</span><span class="sxs-lookup"><span data-stu-id="f5934-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="f5934-161">حدد **نسخ بيانات للرد‬**.</span><span class="sxs-lookup"><span data-stu-id="f5934-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="f5934-162">يؤدي ذلك إلى نسخ بيانات، مثل الكمية والتواريخ، من طلب عرض الأسعار إلى الرد.</span><span class="sxs-lookup"><span data-stu-id="f5934-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="f5934-163">في حقل **سعر الوحدة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f5934-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="f5934-164">هذا هو السعر الذي تلقيته من المورّد.</span><span class="sxs-lookup"><span data-stu-id="f5934-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="f5934-165">قد تحتاج أيضًا إلى إدخال معلومات إضافية من المورّد.</span><span class="sxs-lookup"><span data-stu-id="f5934-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="f5934-166">حدد **قبول**.</span><span class="sxs-lookup"><span data-stu-id="f5934-166">Select **Accept**.</span></span>
21. <span data-ttu-id="f5934-167">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="f5934-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="f5934-168">التأكد من تحويل المورّد والسعر إلى الطلب</span><span class="sxs-lookup"><span data-stu-id="f5934-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="f5934-169">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f5934-169">Close the page.</span></span>
2. <span data-ttu-id="f5934-170">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="f5934-170">Select **Lines**.</span></span>
3. <span data-ttu-id="f5934-171">حدد **المعلومات ذات الصلة**.</span><span class="sxs-lookup"><span data-stu-id="f5934-171">Select **Related information**.</span></span>
4. <span data-ttu-id="f5934-172">حدد **طلب شراء**.</span><span class="sxs-lookup"><span data-stu-id="f5934-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="f5934-173">حدد البند الذي تم تحويله إلى طلب عرض الأسعار (RFQ).</span><span class="sxs-lookup"><span data-stu-id="f5934-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="f5934-174">تأكد من نسخ السعر والمورّد إلى الطلب.</span><span class="sxs-lookup"><span data-stu-id="f5934-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="f5934-175">حدد **سير العمل** لفتح مربع الحوار المنسدل.</span><span class="sxs-lookup"><span data-stu-id="f5934-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="f5934-176">حدد "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="f5934-176">Select Complete.</span></span>
8. <span data-ttu-id="f5934-177">حدد الصفحة .</span><span class="sxs-lookup"><span data-stu-id="f5934-177">Select the page.</span></span>
9. <span data-ttu-id="f5934-178">حدد "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="f5934-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]