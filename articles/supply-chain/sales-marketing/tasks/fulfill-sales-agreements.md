---
title: استيفاء اتفاقيات البيع
description: يوضح هذا الإجراء كيفية تنفيذ اتفاقية بيع عن طريق إقران أوامر المبيعات بها.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e32decdd13cb578c1ac026f25a56b37ff7231a9
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146458"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="dd4ee-103">استيفاء اتفاقيات البيع</span><span class="sxs-lookup"><span data-stu-id="dd4ee-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd4ee-104">يوضح هذا الإجراء كيفية تنفيذ اتفاقية بيع عن طريق إقران أوامر المبيعات بها.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="dd4ee-105">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="dd4ee-106">قبل تشغيل هذا الدليل، تأكد أن لديك اتفاقية بيع فعالة من نوع "التزام قيمة المنتج".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="dd4ee-107">وبدلاً من ذلك، يمكنك تشغيل دليل مهمة يسمى "إنشاء اتفاقيات البيع".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="dd4ee-108">إصدار أمر مبيعات من الاتفاقية</span><span class="sxs-lookup"><span data-stu-id="dd4ee-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="dd4ee-109">انتقل إلى المبيعات والتسويق > اتفاقيات المبيعات > اتفاقية البيع.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="dd4ee-110">في القائمة، حدد الاتفاقية التي تريد إصدار البند مقابلها.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="dd4ee-111">في جزء الإجراءات، انقر فوق "اتفاقيات المبيعات".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="dd4ee-112">انقر فوق "إصدار الأمر".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-112">Click Release order.</span></span>
    * <span data-ttu-id="dd4ee-113">وكما يشير النص برأس صفحة "إنشاء أمر إصدار"، ستختلف التفاصيل المطلوبة لبنود أمر المبيعات تبعاً لما إذا كانت الاتفاقية على أساس الكمية أو القيمة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="dd4ee-114">الاتفاقية الواردة في هذا الدليل من النوع "الالتزام بقيمة المنتج".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="dd4ee-115">وهذا سبب فراغ قسم البنود بهذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="dd4ee-116">إذا كان الالتزام استند إلى كمية، فقد يتم نسخ معلومات البنود من الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="dd4ee-117">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-117">Click Create.</span></span>
    * <span data-ttu-id="dd4ee-118">تُعلمك الرسالة أنه تم إنشاء أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="dd4ee-119">وحيث إن الأمر لا يتضمن أية بنود، يجب إضافة تفاصيل بند أمر لإكمال عملية الإصدار.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="dd4ee-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-120">Close the page.</span></span>
7. <span data-ttu-id="dd4ee-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-121">Close the page.</span></span>
8. <span data-ttu-id="dd4ee-122">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="dd4ee-123">في القائمة، ابحث عن الأمر الذي تم إنشاؤه كنتيجة إصدار أمر بالمهمة السابقة ثم افتحه.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="dd4ee-124">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-124">Click Add line.</span></span>
11. <span data-ttu-id="dd4ee-125">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="dd4ee-126">في الحقل "رقم الصنف"، اكتب الصنف المحدد في اتفاقية البيع المقترنة أو حدده.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="dd4ee-127">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="dd4ee-128">تأكد من إدخال كمية الذي تضع المبلغ الصافي أقل من قيمة اتفاقية البيع المرتبطة به.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="dd4ee-129">لاحظ أنه بسبب ربط أمر المبيعات بالاتفاقية، يتم تطبيق النسبة المئوية للخصم على بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="dd4ee-130">انقر فوق "تحديث البند".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-130">Click Update line.</span></span>
15. <span data-ttu-id="dd4ee-131">انقر فوق "تم الإرفاق".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-131">Click Attached.</span></span>
    * <span data-ttu-id="dd4ee-132">تعرض الصفحة "الاتفاقية المرفقة" معرف وشروط الاتفاقية التي يتم إصدار البنود منها.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="dd4ee-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-133">Close the page.</span></span>
17. <span data-ttu-id="dd4ee-134">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="dd4ee-135">انقر فوق "اتفاقية البيع المرفقة".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="dd4ee-136">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="dd4ee-137">انقر فوق علامة التبويب "التنفيذ".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="dd4ee-138">تعرض علامة التبويب "التنفيذ" ملخصاً لجميع بنود أمر المبيعات المقترنة بهذا الالتزام وحالة التنفيذ لها بالإضافة إلى المبلغ أو الكمية التي لم يتم إصدارها بعد.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="dd4ee-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-139">Close the page.</span></span>
22. <span data-ttu-id="dd4ee-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-140">Close the page.</span></span>
23. <span data-ttu-id="dd4ee-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="dd4ee-142">تطبيق اتفاقيات البيع في عملية الطلب</span><span class="sxs-lookup"><span data-stu-id="dd4ee-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="dd4ee-143">انتقل إلى المبيعات والتسويق > أوامر المبيعات > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="dd4ee-144">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-144">Click New.</span></span>
3. <span data-ttu-id="dd4ee-145">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dd4ee-146">في القائمة، ابحث عن العميل المحدد في اتفاقية البيع وحدده.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="dd4ee-147">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="dd4ee-148">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-148">Expand the General section.</span></span>
7. <span data-ttu-id="dd4ee-149">في الحقل "معرف اتفاقية البيع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="dd4ee-150">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dd4ee-151">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-151">Click Yes.</span></span>
10. <span data-ttu-id="dd4ee-152">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-152">Click OK.</span></span>
11. <span data-ttu-id="dd4ee-153">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="dd4ee-154">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="dd4ee-155">في الحقل "رقم الصنف"، اكتب الصنف المحدد في اتفاقية البيع المقترنة أو حدده.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="dd4ee-156">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="dd4ee-157">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="dd4ee-157">Click Save.</span></span>
16. <span data-ttu-id="dd4ee-158">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="dd4ee-159">انقر فوق "ترحيل إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="dd4ee-160">وسّع مقطع "المحددات".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="dd4ee-161">حدد "نعم" في الحقل "الترحيل".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="dd4ee-162">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-162">Click OK.</span></span>
21. <span data-ttu-id="dd4ee-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-163">Click OK.</span></span>
22. <span data-ttu-id="dd4ee-164">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="dd4ee-165">انقر فوق "اتفاقية البيع المرفقة".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="dd4ee-166">انقر فوق علامة التبويب "التنفيذ".</span><span class="sxs-lookup"><span data-stu-id="dd4ee-166">Click the Fulfillment tab.</span></span>

