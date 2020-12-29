---
title: حركة خطاب الضمان
description: يتناول هذا الإجراء عملية خطاب الضمان.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440042"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="093dd-103">حركة خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="093dd-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="093dd-104">يتناول هذا الإجراء عملية خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="093dd-105">يجب إكمال المهام التالية قبل إكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="093dd-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="093dd-106">إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="093dd-107">إنشاء اتفاقية تسهيلات بنكية لخطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="093dd-108">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="093dd-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="093dd-109">إنشاء أمر مبيعات بخطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="093dd-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="093dd-110">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="093dd-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="093dd-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="093dd-111">Click New.</span></span>
3. <span data-ttu-id="093dd-112">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="093dd-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="093dd-113">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="093dd-113">Expand the General section.</span></span>
5. <span data-ttu-id="093dd-114">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="093dd-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="093dd-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="093dd-116">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="093dd-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="093dd-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="093dd-118">في حقل "‏‫نوع المستند البنكي‬"، حدد "خطاب الضمان".</span><span class="sxs-lookup"><span data-stu-id="093dd-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="093dd-119">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="093dd-119">Click OK.</span></span>
11. <span data-ttu-id="093dd-120">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="093dd-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="093dd-121">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="093dd-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="093dd-122">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="093dd-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="093dd-123">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="093dd-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="093dd-124">ملاحظة: حدد ‏‫التحكم في تاريخ التسليم‬ = بلا</span><span class="sxs-lookup"><span data-stu-id="093dd-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="093dd-125">في حقل "‏‫تاريخ الشحن المطلوب‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="093dd-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="093dd-126">في حقل "‏‫تاريخ الشحن المؤكد‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="093dd-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="093dd-127">عملية طلب خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="093dd-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="093dd-128">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="093dd-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="093dd-129">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="093dd-130">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="093dd-131">انقر فوق طلب لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="093dd-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="093dd-132">في حقل "النوع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="093dd-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="093dd-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="093dd-134">في الحقل "القيمة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="093dd-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="093dd-135">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="093dd-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="093dd-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-136">Click OK.</span></span>
10. <span data-ttu-id="093dd-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="093dd-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="093dd-138">عملية إرسال خطاب الضمان إلى البنك</span><span class="sxs-lookup"><span data-stu-id="093dd-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="093dd-139">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="093dd-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="093dd-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="093dd-141">انقر فوق "تقديم للبنك" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="093dd-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="093dd-142">في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="093dd-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="093dd-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="093dd-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="093dd-145">عملية استلام خطاب الضمان من البنك</span><span class="sxs-lookup"><span data-stu-id="093dd-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="093dd-146">انقر فوق "استلام من البنك‬" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="093dd-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="093dd-147">في حقل "رقم البنك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="093dd-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="093dd-148">تحقق من القيم الموجودة في الحقلين الهامش المحتسب والمصروفات.</span><span class="sxs-lookup"><span data-stu-id="093dd-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="093dd-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-149">Click OK.</span></span>
4. <span data-ttu-id="093dd-150">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="093dd-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="093dd-151">تحقق من سجل "‏‫استلام من البنك".</span><span class="sxs-lookup"><span data-stu-id="093dd-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="093dd-152">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="093dd-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="093dd-153">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="093dd-153">Click Lines.</span></span>
    * <span data-ttu-id="093dd-154">تحقق من ترحيل إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="093dd-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="093dd-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="093dd-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="093dd-156">عملية إعطاء خطاب الضمان للمستفيد</span><span class="sxs-lookup"><span data-stu-id="093dd-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="093dd-157">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="093dd-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="093dd-158">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="093dd-159">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="093dd-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="093dd-160">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="093dd-161">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="093dd-162">انقر فوق "‏‫منح للمستفيد‬" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="093dd-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="093dd-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-163">Click OK.</span></span>
8. <span data-ttu-id="093dd-164">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="093dd-165">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="093dd-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="093dd-166">انقر فوق "‏‫منح للمستفيد‬" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="093dd-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="093dd-167">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-167">Click OK.</span></span>
12. <span data-ttu-id="093dd-168">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="093dd-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="093dd-169">تحقق من صحة سجل "منح للمستفيد".</span><span class="sxs-lookup"><span data-stu-id="093dd-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="093dd-170">عملية زيادة قيمة خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="093dd-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="093dd-171">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="093dd-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="093dd-172">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="093dd-173">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="093dd-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="093dd-174">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="093dd-175">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="093dd-176">انقر فوق "‏‫زيادة القيمة‬" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="093dd-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="093dd-177">في حقل "‏‫القيمة المطلوب إضافتها‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="093dd-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="093dd-178">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-178">Click OK.</span></span>
9. <span data-ttu-id="093dd-179">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="093dd-180">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="093dd-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="093dd-181">انقر فوق "‏‫زيادة القيمة‬" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="093dd-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="093dd-182">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-182">Click OK.</span></span>
13. <span data-ttu-id="093dd-183">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="093dd-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="093dd-184">تحقق من سجل "زيادة القيمة".</span><span class="sxs-lookup"><span data-stu-id="093dd-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="093dd-185">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="093dd-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="093dd-186">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="093dd-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="093dd-187">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="093dd-187">Click Lines.</span></span>
    * <span data-ttu-id="093dd-188">تحقق من إدخالات دفتر اليومية المُرحلة.</span><span class="sxs-lookup"><span data-stu-id="093dd-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="093dd-189">عملية تصفية خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="093dd-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="093dd-190">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="093dd-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="093dd-191">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="093dd-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="093dd-192">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="093dd-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="093dd-193">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="093dd-194">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="093dd-195">انقر فوق "تصفية" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="093dd-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="093dd-196">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-196">Click OK.</span></span>
8. <span data-ttu-id="093dd-197">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="093dd-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="093dd-198">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="093dd-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="093dd-199">انقر فوق "تصفية" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="093dd-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="093dd-200">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="093dd-200">Click OK.</span></span>
12. <span data-ttu-id="093dd-201">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="093dd-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="093dd-202">تحقق من سجل "تصفية‬".</span><span class="sxs-lookup"><span data-stu-id="093dd-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="093dd-203">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="093dd-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="093dd-204">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="093dd-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="093dd-205">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="093dd-205">Click Lines.</span></span>
    * <span data-ttu-id="093dd-206">تحقق من إدخالات دفتر اليومية المُرحلة.</span><span class="sxs-lookup"><span data-stu-id="093dd-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="093dd-207">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="093dd-207">Close the page.</span></span>

