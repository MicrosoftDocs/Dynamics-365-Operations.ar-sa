---
title: تصدير خطاب الاعتماد
description: يتناول هذا الإجراء عملية تصدير خطاب اعتماد.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b46ba174d658d27f5349762f3314ea8110490d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976381"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="c26b3-103">تصدير خطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="c26b3-103">Export letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c26b3-104">يتناول هذا الإجراء عملية تصدير خطاب اعتماد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="c26b3-105">وهي اتفاقية يصدرها البنك، وفيها يوافق على ضمان الدفع نيابة عن المشتري، إذا تم استيفاء شروط الاتفاقية المبرمة بين المشتري والبائع.</span><span class="sxs-lookup"><span data-stu-id="c26b3-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="c26b3-106">قم بتشغيل الإجراءين "إعداد التسهيلات البنكية وملفات تعريف الترحيل" و"خطاب الاعتماد_إنشاء اتفاقية تسهيلات بنكية" قبل تنفيذ هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="c26b3-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="c26b3-107">يجب تحديد شركة العرض التوضيحي USMF لتشغيل هذا الإجراء بنجاح.</span><span class="sxs-lookup"><span data-stu-id="c26b3-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="c26b3-108">إنشاء أمر مبيعات لتصدير خطاب اعتماد</span><span class="sxs-lookup"><span data-stu-id="c26b3-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="c26b3-109">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c26b3-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c26b3-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c26b3-110">Click New.</span></span>
3. <span data-ttu-id="c26b3-111">في الحقل "حساب العميل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c26b3-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c26b3-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c26b3-113">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c26b3-114">قم بتوسيع أو طي المقطع "عام".</span><span class="sxs-lookup"><span data-stu-id="c26b3-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="c26b3-115">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c26b3-116">حدد الموقع الذي يتم تخزين الصنف الذي سيتم إصداره.</span><span class="sxs-lookup"><span data-stu-id="c26b3-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="c26b3-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c26b3-118">في الحقل "المستودع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c26b3-119">حدد المخزن الذي يتم به تخزين الصنف الذي سيتم إصداره.</span><span class="sxs-lookup"><span data-stu-id="c26b3-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="c26b3-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c26b3-121">ملاحظة: ينبغي تحديد حقل "نوع المستند البنكي" بقيمة "‏‫خطاب الاعتماد‬".</span><span class="sxs-lookup"><span data-stu-id="c26b3-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="c26b3-122">في حقل "‏‫نوع المستند البنكي‬"، حدد "خطاب الاعتماد".</span><span class="sxs-lookup"><span data-stu-id="c26b3-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="c26b3-123">قم بتوسيع قسم التسليم أو طيه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="c26b3-124">حدد ‏‫التحكم في تاريخ التسليم‬ = بلا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="c26b3-125">في حقل "‏‫تاريخ الاستلام المطلوب‬‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="c26b3-126">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c26b3-126">Click OK.</span></span>
15. <span data-ttu-id="c26b3-127">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c26b3-128">حدد العنصر المطلوب إصداره/بيعه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="c26b3-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c26b3-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="c26b3-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c26b3-131">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="c26b3-132">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="c26b3-133">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="c26b3-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="c26b3-134">في حقل "‏‫تاريخ الشحن المطلوب‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="c26b3-135">في حقل "‏‫تاريخ الشحن المؤكد‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="c26b3-136">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="c26b3-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="c26b3-137">انقر فوق خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="c26b3-138">في حقل "رقم المستند البنكي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c26b3-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="c26b3-139">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="c26b3-140">قم بتوسيع قسم تفاصيل البنك أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="c26b3-141">في حقل "‏‫بنك الإصدار‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="c26b3-142">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="c26b3-143">في حقل "‏‫البنك المُبلغ‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="c26b3-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c26b3-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="c26b3-145">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="c26b3-146">انقر فوق إحضار عمليات الشحن من أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c26b3-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="c26b3-147">انقر فوق إصدار المستند البنكي.</span><span class="sxs-lookup"><span data-stu-id="c26b3-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="c26b3-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c26b3-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="c26b3-149">ترحيل إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="c26b3-149">Post Packing slip</span></span>
1. <span data-ttu-id="c26b3-150">في "جزء الإجراءات"، انقر فوق "انتقاء وتعبئة‬".</span><span class="sxs-lookup"><span data-stu-id="c26b3-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="c26b3-151">انقر فوق "ترحيل إيصال التعبئة".</span><span class="sxs-lookup"><span data-stu-id="c26b3-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="c26b3-152">قم بتوسيع القسم "المعلمات" أو طيه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="c26b3-153">في الحقل "الكمية"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="c26b3-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="c26b3-154">قم بتوسيع قسم الإعداد أو طيه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="c26b3-155">في حقل "‏‫تاريخ إيصال التعبئة‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="c26b3-156">حدد رقم الشحنة.</span><span class="sxs-lookup"><span data-stu-id="c26b3-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="c26b3-157">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c26b3-158">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c26b3-158">Click OK.</span></span>
10. <span data-ttu-id="c26b3-159">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c26b3-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="c26b3-160">‏‫ترحيل فواتير المبيعات</span><span class="sxs-lookup"><span data-stu-id="c26b3-160">Post sales invoice</span></span>
1. <span data-ttu-id="c26b3-161">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="c26b3-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="c26b3-162">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="c26b3-162">Click Invoice.</span></span>
3. <span data-ttu-id="c26b3-163">قم بتوسيع قسم النظرة العامة أو طيه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="c26b3-164">حدد رقم الشحنة.</span><span class="sxs-lookup"><span data-stu-id="c26b3-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="c26b3-165">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c26b3-166">قم بتوسيع قسم الإعداد أو طيه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="c26b3-167">في حقل تاريخ الفاتورة، قم بإدخال تاريخ.</span><span class="sxs-lookup"><span data-stu-id="c26b3-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="c26b3-168">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c26b3-168">Click OK.</span></span>
9. <span data-ttu-id="c26b3-169">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c26b3-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="c26b3-170">حالة مستندات الشحن التي تم إرسالها</span><span class="sxs-lookup"><span data-stu-id="c26b3-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="c26b3-171">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="c26b3-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="c26b3-172">انقر فوق خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="c26b3-173">قم بتوسيع قسم البنود أو طيه.</span><span class="sxs-lookup"><span data-stu-id="c26b3-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="c26b3-174">ملاحظة: يجب تعيين حقل "‏‫المستند المرسل" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="c26b3-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="c26b3-175">التحقق من تصدير خطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="c26b3-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="c26b3-176">انتقل إلى ‏‫إدارة النقد والبنوك > خطابات الاعتماد > تصدير خطاب الاعتماد واستيراد تحصيلات.</span><span class="sxs-lookup"><span data-stu-id="c26b3-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="c26b3-177">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c26b3-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c26b3-178">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c26b3-179">تحقق من أن حالة شحنة ‏‫تصدير خطاب الاعتماد‬ هي "مفوترة".</span><span class="sxs-lookup"><span data-stu-id="c26b3-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="c26b3-180">دفع العميل</span><span class="sxs-lookup"><span data-stu-id="c26b3-180">Customer payment</span></span>
1. <span data-ttu-id="c26b3-181">انتقل إلى الحسابات المدينة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="c26b3-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c26b3-182">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c26b3-182">Click New.</span></span>
3. <span data-ttu-id="c26b3-183">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c26b3-184">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c26b3-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c26b3-185">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c26b3-186">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c26b3-186">Click Lines.</span></span>
7. <span data-ttu-id="c26b3-187">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c26b3-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="c26b3-188">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c26b3-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="c26b3-189">انقر فوق "التسويات".</span><span class="sxs-lookup"><span data-stu-id="c26b3-189">Click Settlement.</span></span>
10. <span data-ttu-id="c26b3-190">حدد خانة الاختيار في رأس الإجماليات.</span><span class="sxs-lookup"><span data-stu-id="c26b3-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="c26b3-191">ملاحظة: قم بتعيين حقل "إظهار" إلى "خطاب الاعتماد".</span><span class="sxs-lookup"><span data-stu-id="c26b3-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="c26b3-192">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c26b3-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="c26b3-193">حدد خانة اختيار "وضع علامة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="c26b3-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="c26b3-194">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c26b3-194">Click OK.</span></span>
14. <span data-ttu-id="c26b3-195">انقر فوق علامة التبويب "الدفع".</span><span class="sxs-lookup"><span data-stu-id="c26b3-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="c26b3-196">التحقق من رقم المستند البنكي وتفاصيل رقم الشحنة</span><span class="sxs-lookup"><span data-stu-id="c26b3-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="c26b3-197">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="c26b3-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="c26b3-198">التحقق من تصدير خطاب الاعتماد بعد الدفع</span><span class="sxs-lookup"><span data-stu-id="c26b3-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="c26b3-199">انتقل إلى ‏‫إدارة النقد والبنوك > خطابات الاعتماد > تصدير خطاب الاعتماد واستيراد تحصيلات.</span><span class="sxs-lookup"><span data-stu-id="c26b3-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="c26b3-200">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c26b3-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c26b3-201">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c26b3-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c26b3-202">التحقق من حالة الشحنة = تم استلام المدفوعات ومبلغ الرصيد = 0.00.</span><span class="sxs-lookup"><span data-stu-id="c26b3-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

