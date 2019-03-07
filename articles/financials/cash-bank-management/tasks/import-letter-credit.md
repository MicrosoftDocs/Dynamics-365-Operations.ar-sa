---
title: استيراد خطاب اعتماد
description: يتناول هذا الإجراء عملية استيراد خطاب اعتماد.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1768494182a79d7a33044498c1e768e61d937d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "313556"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="3158d-103">استيراد خطاب اعتماد</span><span class="sxs-lookup"><span data-stu-id="3158d-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3158d-104">يتناول هذا الإجراء عملية استيراد خطاب اعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="3158d-105">يجب إعداد ما يلي قبل إتمام هذا الإجراء: التسهيلات البنكية وملفات تعريف الترحيل واتفاقية التسهيلات البنكية والتفاصيل البنكية للمورد.</span><span class="sxs-lookup"><span data-stu-id="3158d-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="3158d-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="3158d-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="3158d-107">إنشاء أمر شراء باستخدام خطاب اعتماد</span><span class="sxs-lookup"><span data-stu-id="3158d-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="3158d-108">انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="3158d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3158d-109">Click New.</span></span>
3. <span data-ttu-id="3158d-110">في الحقل "حساب المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="3158d-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3158d-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3158d-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3158d-113">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="3158d-113">Expand the General section.</span></span>
7. <span data-ttu-id="3158d-114">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="3158d-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3158d-116">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="3158d-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="3158d-118">في الحقل "تاريخ المحاسبة" أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="3158d-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="3158d-119">في حقل "‏‫تاريخ التسليم‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="3158d-120">ملاحظة: ينبغي تحديد حقل "نوع المستند البنكي" بقيمة "‏‫خطاب الاعتماد‬".</span><span class="sxs-lookup"><span data-stu-id="3158d-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="3158d-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3158d-121">Click OK.</span></span>
14. <span data-ttu-id="3158d-122">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="3158d-123">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3158d-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="3158d-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="3158d-125">قم بتوسيع القسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="3158d-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="3158d-126">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="3158d-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="3158d-127">في حقل "‏‫تاريخ التسليم‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="3158d-128">في حقل "‏‫تاريخ التسليم المؤكد‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="3158d-129">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="3158d-130">تحديد تفاصيل خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="3158d-131">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="3158d-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="3158d-132">انقر فوق خطاب الاعتماد/ استيراد تحصيلات</span><span class="sxs-lookup"><span data-stu-id="3158d-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="3158d-133">في حقل "تاريخ استمارة التقديم‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="3158d-134">تحقق من أن حقل "‏‫الحساب البنكي‬" هو الحساب البنكي الافتراضي النشط، الذي يعتمد على تاريخ استمارة التقديم.</span><span class="sxs-lookup"><span data-stu-id="3158d-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="3158d-135">في حقل "رقم المستند البنكي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3158d-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="3158d-136">في حقل "تاريخ الاستلام"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="3158d-137">قم بتوسيع القسم "المستند البنكي".</span><span class="sxs-lookup"><span data-stu-id="3158d-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="3158d-138">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="3158d-139">قم بتوسيع القسم "تفاصيل البنك".</span><span class="sxs-lookup"><span data-stu-id="3158d-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="3158d-140">في حقل "‏‫البنك المُبلغ‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="3158d-141">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="3158d-142">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3158d-142">Click Save.</span></span>
33. <span data-ttu-id="3158d-143">انقر فوق إحضار عمليات الشحن من أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="3158d-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-144">Close the page.</span></span>
35. <span data-ttu-id="3158d-145">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="3158d-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="3158d-146">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="3158d-146">Click Confirm.</span></span>
37. <span data-ttu-id="3158d-147">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="3158d-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="3158d-148">انقر فوق خطاب الاعتماد/ استيراد تحصيلات</span><span class="sxs-lookup"><span data-stu-id="3158d-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="3158d-149">انقر فوق "معالجة".</span><span class="sxs-lookup"><span data-stu-id="3158d-149">Click Process.</span></span>
40. <span data-ttu-id="3158d-150">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="3158d-150">Click Confirm.</span></span>
    * <span data-ttu-id="3158d-151">تحقق من أن رصيد التسهيلات يقلل مبلغ أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="3158d-152">في هذا المثال، مبلغ الشراء = 500.00، حد التسهيلات = 10000.00، لذلك، رصيد التسهيلات = 9500.00.</span><span class="sxs-lookup"><span data-stu-id="3158d-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="3158d-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-153">Close the page.</span></span>
42. <span data-ttu-id="3158d-154">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="3158d-155">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3158d-155">Click Save.</span></span>
44. <span data-ttu-id="3158d-156">في جزء الإجراءات، انقر فوق "شراء".</span><span class="sxs-lookup"><span data-stu-id="3158d-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="3158d-157">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="3158d-157">Click Confirm.</span></span>
    * <span data-ttu-id="3158d-158">تعديل خطاب الاعتماد، نتيجة للتغير في سعر الوحدة.</span><span class="sxs-lookup"><span data-stu-id="3158d-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="3158d-159">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="3158d-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="3158d-160">انقر فوق خطاب الاعتماد/ استيراد تحصيلات</span><span class="sxs-lookup"><span data-stu-id="3158d-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="3158d-161">تعديل خطاب الاعتماد، نتيجة للتغير في سعر وحدة الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="3158d-162">انقر فوق "معالجة".</span><span class="sxs-lookup"><span data-stu-id="3158d-162">Click Process.</span></span>
49. <span data-ttu-id="3158d-163">انقر فوق تعديل.</span><span class="sxs-lookup"><span data-stu-id="3158d-163">Click Amend.</span></span>
50. <span data-ttu-id="3158d-164">انقر فوق "إزالة".</span><span class="sxs-lookup"><span data-stu-id="3158d-164">Click Remove.</span></span>
51. <span data-ttu-id="3158d-165">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="3158d-165">Click Yes.</span></span>
52. <span data-ttu-id="3158d-166">انقر فوق إحضار عمليات الشحن من أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="3158d-167">انقر فوق "معالجة".</span><span class="sxs-lookup"><span data-stu-id="3158d-167">Click Process.</span></span>
54. <span data-ttu-id="3158d-168">انقر فوق "تأكيد".</span><span class="sxs-lookup"><span data-stu-id="3158d-168">Click Confirm.</span></span>
    * <span data-ttu-id="3158d-169">تحقق من أن رصيد التسهيلات يقلل مبلغ أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="3158d-170">في هذا المثال، مبلغ الشراء المحرر = 600.00، حد التسهيلات = 10000.00، لذلك، رصيد التسهيلات = 9400.00.</span><span class="sxs-lookup"><span data-stu-id="3158d-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="3158d-171">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="3158d-172">ترحيل إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="3158d-172">Post Packing slip</span></span>
1. <span data-ttu-id="3158d-173">في جزء الإجراءات، انقر فوق "استلام".</span><span class="sxs-lookup"><span data-stu-id="3158d-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="3158d-174">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="3158d-174">Click Product receipt.</span></span>
3. <span data-ttu-id="3158d-175">في حقل "PurchParmTable_Num"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3158d-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="3158d-176">حدد رقم الشحنة التي تم إنشاؤها بالمرجع إلى خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="3158d-177">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3158d-178">في حقل "‏‫‏‫تاريخ إيصال استلام المنتجات‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="3158d-179">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3158d-179">Click OK.</span></span>
7. <span data-ttu-id="3158d-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-180">Close the page.</span></span>
8. <span data-ttu-id="3158d-181">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="3158d-182">التحقق من ‏‫حالة حركة استيراد خطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="3158d-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="3158d-183">انتقل إلى ‏‫إدارة النقد والبنوك > خطابات الاعتماد > استيراد خطاب الاعتماد واستيراد تحصيلات.</span><span class="sxs-lookup"><span data-stu-id="3158d-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="3158d-184">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3158d-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3158d-185">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3158d-186">التحقق من ‏‫حالة حركة استيراد خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-186">Verify the Import letter of credit status.</span></span>    
    *   
4. <span data-ttu-id="3158d-187">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-187">Close the page.</span></span>
5. <span data-ttu-id="3158d-188">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="3158d-189">ترحيل فاتورة الشراء</span><span class="sxs-lookup"><span data-stu-id="3158d-189">Post purchase invoice</span></span>
1. <span data-ttu-id="3158d-190">انتقل إلى الحسابات الدائنة > أوامر الشراء > جميع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="3158d-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="3158d-191">حدد أمر الشراء الذي تم إنشاؤه باستخدام خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="3158d-192">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3158d-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3158d-193">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3158d-194">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="3158d-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="3158d-195">انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="3158d-195">Click Invoice.</span></span>
6. <span data-ttu-id="3158d-196">في الحقل "الرقم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3158d-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="3158d-197">في حقل "رقم الشحنة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="3158d-198">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3158d-199">في حقل تاريخ الفاتورة، قم بإدخال تاريخ.</span><span class="sxs-lookup"><span data-stu-id="3158d-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="3158d-200">انقر فوق تحديث حالة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="3158d-200">Click Update match status.</span></span>
11. <span data-ttu-id="3158d-201">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="3158d-201">Click Post.</span></span>
12. <span data-ttu-id="3158d-202">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-202">Close the page.</span></span>
13. <span data-ttu-id="3158d-203">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="3158d-204">التحقق من ‏‫حالة حركة استيراد خطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="3158d-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="3158d-205">انتقل إلى ‏‫إدارة النقد والبنوك > خطابات الاعتماد > استيراد خطاب الاعتماد واستيراد تحصيلات.</span><span class="sxs-lookup"><span data-stu-id="3158d-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="3158d-206">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3158d-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3158d-207">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3158d-208">التحقق من خطاب الاعتماد للدائن2.</span><span class="sxs-lookup"><span data-stu-id="3158d-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="3158d-209">التحقق من صحة :  حالة الشحن = تفاصيل التسهيلات البنكية المفوترة</span><span class="sxs-lookup"><span data-stu-id="3158d-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="3158d-210">انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="3158d-210">Click View.</span></span>
5. <span data-ttu-id="3158d-211">انقر فوق طباعة استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="3158d-211">Click Print application.</span></span>
6. <span data-ttu-id="3158d-212">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3158d-212">Click OK.</span></span>
    * <span data-ttu-id="3158d-213">تحقق من طباعة استمارة تقديم خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="3158d-214">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-214">Close the page.</span></span>
8. <span data-ttu-id="3158d-215">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-215">Close the page.</span></span>
9. <span data-ttu-id="3158d-216">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="3158d-217">ترحيل دفتر يومية المدفوعات للمورد لفاتورة الشراء التي تم إنشاؤها باستخدام خطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="3158d-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="3158d-218">انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="3158d-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="3158d-219">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3158d-219">Click New.</span></span>
3. <span data-ttu-id="3158d-220">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="3158d-221">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3158d-222">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="3158d-222">Click Lines.</span></span>
6. <span data-ttu-id="3158d-223">في حقل "التاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="3158d-224">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3158d-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="3158d-225">انقر فوق "تسوية الحركات".</span><span class="sxs-lookup"><span data-stu-id="3158d-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="3158d-226">قم بتوسيع قسم الإجماليات.</span><span class="sxs-lookup"><span data-stu-id="3158d-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="3158d-227">في الحقل "إظهار"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="3158d-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="3158d-228">تحقق من أنه تم تحديث ‏‫حقلي رقم المستند البنكي‬ ورقم الشحنة.</span><span class="sxs-lookup"><span data-stu-id="3158d-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="3158d-229">حدد خانة الاختيار "وضع علامة".</span><span class="sxs-lookup"><span data-stu-id="3158d-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="3158d-230">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3158d-230">Click OK.</span></span>
13. <span data-ttu-id="3158d-231">انقر فوق علامة التبويب "الدفع".</span><span class="sxs-lookup"><span data-stu-id="3158d-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="3158d-232">تحقق من أنه تم تحديث ‏‫حقلي رقم المستند البنكي‬ ورقم الشحنة.</span><span class="sxs-lookup"><span data-stu-id="3158d-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="3158d-233">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="3158d-233">Click Post.</span></span>
15. <span data-ttu-id="3158d-234">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-234">Close the page.</span></span>
16. <span data-ttu-id="3158d-235">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="3158d-236">التحقق من حالة حركة استيراد خطاب الاعتماد‬ بعد دفع الفاتورة</span><span class="sxs-lookup"><span data-stu-id="3158d-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="3158d-237">انتقل إلى ‏‫إدارة النقد والبنوك > خطابات الاعتماد > استيراد خطاب الاعتماد واستيراد تحصيلات.</span><span class="sxs-lookup"><span data-stu-id="3158d-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="3158d-238">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3158d-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3158d-239">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3158d-240">التحقق من ‏‫حالة حركة استيراد خطاب الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="3158d-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="3158d-241">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="3158d-242">التحقق من ‏‫تقرير حد التسهيلات البنكية والاستخدام</span><span class="sxs-lookup"><span data-stu-id="3158d-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="3158d-243">انتقل إلى ‏‫إدارة النقد والبنوك > الاستعلامات والتقارير > خطابات الاعتماد أو الضمان > تقرير التسهيلات البنكية والاستخدام‬.</span><span class="sxs-lookup"><span data-stu-id="3158d-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="3158d-244">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="3158d-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="3158d-245">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="3158d-245">Click Filter.</span></span>
    * <span data-ttu-id="3158d-246">حدد حقل "المعايير" مع الحساب البنكي المطلوب.</span><span class="sxs-lookup"><span data-stu-id="3158d-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="3158d-247">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3158d-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="3158d-248">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3158d-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3158d-249">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3158d-249">Click OK.</span></span>
7. <span data-ttu-id="3158d-250">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3158d-250">Click OK.</span></span>
    * <span data-ttu-id="3158d-251">تحقق من التقرير الذي يسرد الحركات.</span><span class="sxs-lookup"><span data-stu-id="3158d-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="3158d-252">تحقق من سرد التقرير للحركات مع رقم المستند البنكي‬ وحد التسهيلات والمبلغ المستخدم ومبلغ رصيد التسهيلات.</span><span class="sxs-lookup"><span data-stu-id="3158d-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="3158d-253">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3158d-253">Close the page.</span></span>

