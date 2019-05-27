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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566100"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="c57ac-103">حركة خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="c57ac-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c57ac-104">يتناول هذا الإجراء عملية خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="c57ac-105">يجب إكمال المهام التالية قبل إكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="c57ac-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="c57ac-106">إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="c57ac-107">إنشاء اتفاقية تسهيلات بنكية لخطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="c57ac-108">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c57ac-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="c57ac-109">إنشاء أمر مبيعات بخطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="c57ac-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="c57ac-110">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c57ac-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c57ac-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c57ac-111">Click New.</span></span>
3. <span data-ttu-id="c57ac-112">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c57ac-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="c57ac-113">قم بتوسيع القسم "عام".</span><span class="sxs-lookup"><span data-stu-id="c57ac-113">Expand the General section.</span></span>
5. <span data-ttu-id="c57ac-114">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c57ac-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="c57ac-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c57ac-116">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c57ac-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="c57ac-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c57ac-118">في حقل "‏‫نوع المستند البنكي‬"، حدد "خطاب الضمان".</span><span class="sxs-lookup"><span data-stu-id="c57ac-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="c57ac-119">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="c57ac-119">Click OK.</span></span>
11. <span data-ttu-id="c57ac-120">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c57ac-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="c57ac-121">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c57ac-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="c57ac-122">قم بتوسيع قسم "تفاصيل البند".</span><span class="sxs-lookup"><span data-stu-id="c57ac-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="c57ac-123">انقر فوق علامة التبويب "التسليم".</span><span class="sxs-lookup"><span data-stu-id="c57ac-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="c57ac-124">ملاحظة: حدد ‏‫التحكم في تاريخ التسليم‬ = بلا</span><span class="sxs-lookup"><span data-stu-id="c57ac-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="c57ac-125">في حقل "‏‫تاريخ الشحن المطلوب‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c57ac-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="c57ac-126">في حقل "‏‫تاريخ الشحن المؤكد‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c57ac-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="c57ac-127">عملية طلب خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="c57ac-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="c57ac-128">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="c57ac-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="c57ac-129">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="c57ac-130">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="c57ac-131">انقر فوق طلب لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="c57ac-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="c57ac-132">في حقل "النوع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c57ac-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="c57ac-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c57ac-134">في الحقل "القيمة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c57ac-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="c57ac-135">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="c57ac-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="c57ac-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-136">Click OK.</span></span>
10. <span data-ttu-id="c57ac-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c57ac-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="c57ac-138">عملية إرسال خطاب الضمان إلى البنك</span><span class="sxs-lookup"><span data-stu-id="c57ac-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="c57ac-139">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="c57ac-140">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c57ac-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c57ac-141">انقر فوق "تقديم للبنك" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c57ac-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="c57ac-142">في الحقل "الحساب البنكي‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c57ac-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="c57ac-143">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c57ac-144">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="c57ac-145">عملية استلام خطاب الضمان من البنك</span><span class="sxs-lookup"><span data-stu-id="c57ac-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="c57ac-146">انقر فوق "استلام من البنك‬" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="c57ac-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="c57ac-147">في حقل "رقم البنك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c57ac-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="c57ac-148">تحقق من القيم الموجودة في الحقلين الهامش المحتسب والمصروفات.</span><span class="sxs-lookup"><span data-stu-id="c57ac-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="c57ac-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-149">Click OK.</span></span>
4. <span data-ttu-id="c57ac-150">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="c57ac-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="c57ac-151">تحقق من سجل "‏‫استلام من البنك".</span><span class="sxs-lookup"><span data-stu-id="c57ac-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="c57ac-152">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="c57ac-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="c57ac-153">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c57ac-153">Click Lines.</span></span>
    * <span data-ttu-id="c57ac-154">تحقق من ترحيل إدخالات دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="c57ac-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="c57ac-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c57ac-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="c57ac-156">عملية إعطاء خطاب الضمان للمستفيد</span><span class="sxs-lookup"><span data-stu-id="c57ac-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="c57ac-157">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c57ac-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c57ac-158">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c57ac-159">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="c57ac-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c57ac-160">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="c57ac-161">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="c57ac-162">انقر فوق "‏‫منح للمستفيد‬" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c57ac-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="c57ac-163">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-163">Click OK.</span></span>
8. <span data-ttu-id="c57ac-164">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="c57ac-165">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c57ac-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c57ac-166">انقر فوق "‏‫منح للمستفيد‬" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c57ac-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="c57ac-167">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-167">Click OK.</span></span>
12. <span data-ttu-id="c57ac-168">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="c57ac-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="c57ac-169">تحقق من صحة سجل "منح للمستفيد".</span><span class="sxs-lookup"><span data-stu-id="c57ac-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="c57ac-170">عملية زيادة قيمة خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="c57ac-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="c57ac-171">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c57ac-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c57ac-172">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c57ac-173">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="c57ac-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c57ac-174">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="c57ac-175">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="c57ac-176">انقر فوق "‏‫زيادة القيمة‬" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="c57ac-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="c57ac-177">في حقل "‏‫القيمة المطلوب إضافتها‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c57ac-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="c57ac-178">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-178">Click OK.</span></span>
9. <span data-ttu-id="c57ac-179">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="c57ac-180">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c57ac-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c57ac-181">انقر فوق "‏‫زيادة القيمة‬" لفتح مربع حوار الإسقاط.</span><span class="sxs-lookup"><span data-stu-id="c57ac-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="c57ac-182">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-182">Click OK.</span></span>
13. <span data-ttu-id="c57ac-183">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="c57ac-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="c57ac-184">تحقق من سجل "زيادة القيمة".</span><span class="sxs-lookup"><span data-stu-id="c57ac-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="c57ac-185">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c57ac-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="c57ac-186">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="c57ac-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="c57ac-187">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c57ac-187">Click Lines.</span></span>
    * <span data-ttu-id="c57ac-188">تحقق من إدخالات دفتر اليومية المُرحلة.</span><span class="sxs-lookup"><span data-stu-id="c57ac-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="c57ac-189">عملية تصفية خطاب الضمان</span><span class="sxs-lookup"><span data-stu-id="c57ac-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="c57ac-190">انتقل إلى الحسابات المدينة > الأوامر > كافة أوامر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c57ac-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="c57ac-191">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c57ac-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="c57ac-192">في جزء الإجراءات، انقر فوق "إدارة".</span><span class="sxs-lookup"><span data-stu-id="c57ac-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="c57ac-193">انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="c57ac-194">في جزء "الإجراءات"، انقر فوق خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="c57ac-195">انقر فوق "تصفية" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c57ac-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="c57ac-196">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-196">Click OK.</span></span>
8. <span data-ttu-id="c57ac-197">انتقل إلى إدارة النقد والبنك > خطابات الضمان > خطابات الضمان.</span><span class="sxs-lookup"><span data-stu-id="c57ac-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="c57ac-198">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c57ac-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c57ac-199">انقر فوق "تصفية" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c57ac-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="c57ac-200">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c57ac-200">Click OK.</span></span>
12. <span data-ttu-id="c57ac-201">قم بتوسيع قسم "الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="c57ac-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="c57ac-202">تحقق من سجل "تصفية‬".</span><span class="sxs-lookup"><span data-stu-id="c57ac-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="c57ac-203">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c57ac-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c57ac-204">انقر لمتابعة الارتباط الوارد في الحقل "رقم دفعة دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="c57ac-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="c57ac-205">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c57ac-205">Click Lines.</span></span>
    * <span data-ttu-id="c57ac-206">تحقق من إدخالات دفتر اليومية المُرحلة.</span><span class="sxs-lookup"><span data-stu-id="c57ac-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="c57ac-207">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c57ac-207">Close the page.</span></span>

