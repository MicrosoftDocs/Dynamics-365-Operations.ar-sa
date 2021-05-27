---
title: قم بتسوية مدفوعات TDS لموردي هيئة TDS وإنشاء TDS في تشالان
description: يوضح هذا الموضوع كيفية تسوية المدفوعات الضريبية المخصومة في المصدر (TDS) لموردي هيئة TDS.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023005"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="6fcca-103">قم بتسوية مدفوعات TDS لموردي هيئة TDS وإنشاء TDS في تشالان</span><span class="sxs-lookup"><span data-stu-id="6fcca-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fcca-104">يوضح هذا الموضوع كيفية تسوية المدفوعات الضريبية المخصومة في المصدر (TDS) لموردي هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="6fcca-105">انتقل إلى **الحسابات الدائنة \> المدفوعات \> دفتر يومية المدفوعات للمورد**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="6fcca-106">[![صفحة دفتر يومية دفع المورّد](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="6fcca-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="6fcca-107">في الصفحة **دفتر يومية المدفوعات للمورد**، حدد **جديد** لإنشاء بند دفتر يومية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="6fcca-108">في الحقل **الحساب**، حدد مورد هيئة TDS لتسوية مدفوعات TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="6fcca-109">حدد **حركات التسوية** لفتح الصفحة **حركات التسوية**، حيث يمكنك عرض حركات TDS التي تمت تسويتها لمورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="6fcca-110">يتم عرض حركات TDS التي تمت تسويتها لفترة تسوية بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="6fcca-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="6fcca-111">يتم عرض حركات TDS حيث تكون طبيعة فئة المقيم هي **الشركة** كبند حركة واحد.</span><span class="sxs-lookup"><span data-stu-id="6fcca-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="6fcca-112">يتم عرض حركات TDS حيث تكون طبيعة فئة المقيم هي **HUF** أو **شركة** أو **فردي** أو **رابطة الأشخاص** أو **هيئة الأفراد** أو **السلطة المحلية** أو **أخرى** كبند حركة واحد.</span><span class="sxs-lookup"><span data-stu-id="6fcca-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="6fcca-113">يظهر الحقل **مبلغ** إجمالي مبلغ TDS المستحق دفعه إلى مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="6fcca-114">حدد **حركات ضريبة الخصم** لعرض حركات TDS المختلفة التي يتم تضمينها لسجل التسوية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="6fcca-115">يمكنك عرض تقسيم كل حركة TDS يتم تضمينها في عملية التسوية لفترة التسوية في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="6fcca-116">في علامة التبويب **نظرة عامة**، حدد خانة الاختيار **وضع علامة** لحركات TDS لتسويتها إلى مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="6fcca-117">تعرض علامة التبويب **نظرة عامة** المعلومات التالية لكل حركة TDS مفتوحة:</span><span class="sxs-lookup"><span data-stu-id="6fcca-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="6fcca-118">**التاريخ** – تاريخ حركة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="6fcca-119">**الإيصال** – رقم الإيصال.</span><span class="sxs-lookup"><span data-stu-id="6fcca-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="6fcca-120">**المصدر** – الوحدة النمطية التي يتم ترحيل حركة TDS إليها.</span><span class="sxs-lookup"><span data-stu-id="6fcca-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="6fcca-121">**المورد/العميل** – رقم حساب العميل أو المورد الذي يتم خصم TDS منه.</span><span class="sxs-lookup"><span data-stu-id="6fcca-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="6fcca-122">**اسم المستقطع منه/الطرف** – اسم المورد أو العميل الذي يتم خصم TDS منه.</span><span class="sxs-lookup"><span data-stu-id="6fcca-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="6fcca-123">**طبيعة المقيم** – طبيعة فئة المقيم التي ينتمي إليها المستقطع منه.</span><span class="sxs-lookup"><span data-stu-id="6fcca-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="6fcca-124">**المبلغ** – مبلغ الفاتورة الذي يتم حساب TDS به.</span><span class="sxs-lookup"><span data-stu-id="6fcca-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="6fcca-125">**مبلغ الضريبة** – مبلغ TDS الذي تم حسابه للحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcca-126">قم بإلغاء تحديد خانة الاختيار **وضع علامة** لأية حركات TDS يجب عدم تسويتها إلى مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="6fcca-127">في علامة التبويب **عام**، يعرض الحقل **PAN** رقم الحساب الدائم (PAN) للمستقطع منه.</span><span class="sxs-lookup"><span data-stu-id="6fcca-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="6fcca-128">يعرض الحقل **التاريخ** تاريخ حساب TDS، ويعرض الحقل **القيمة** إجمالي النسبة المئوية التي تم استخدامها لحساب TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="6fcca-129">حدد **الإيصال** لعرض إدخالات الإيصال لحركة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="6fcca-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-130">Close the page.</span></span>
10. <span data-ttu-id="6fcca-131">حدد **مكونات ضريبة الخصم** لفتح الصفحة **مكونات ضريبة الخصم**، حيث يمكنك عرض TDS الذي تم حسابه لكل مكون ضريبة TDS لكود ضريبة TDS محدد.</span><span class="sxs-lookup"><span data-stu-id="6fcca-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="6fcca-132">في علامة التبويب **نظرة عامة**، يعرض الحقل **مكون الضريبة** مكون ضريبة TDS الذي تم استخدامه للحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="6fcca-133">يظهر الحقل **مبلغ** مبلغ TDS الذي تم حسابه لمكون الضريبة TDS، بالعملة الأساسية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="6fcca-134">يظهر الحقل **المبلغ التراكمي** إجمالي مبلغ TDS الذي تم حسابه لمكون الضريبة TDS لكافة الحركات التي تمت تسويتها.</span><span class="sxs-lookup"><span data-stu-id="6fcca-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="6fcca-135">في علامة التبويب **مبلغ**، يعرض القسم **العملة الافتراضية** مبلغ TDS الذي تم حسابه لمكون الضريبة TDS، بالعملة الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="6fcca-136">يعرض القسم **العملة الثانوية** المبلغ بالعملة الثانوية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="6fcca-137">قم بإغلاق الصفحة **مكونات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="6fcca-138">في الصفحة **تحرير الحركة المفتوحة**، في الحقل **مبلغ**، لاحظ أنه يتم تحديث المبلغ الإجمالي المطلوب تسويته إلى مورد هيئة TDS لفترة التسوية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="6fcca-139">لتسوية حركات TDS الخاصة بفترات تسوية TDS المختلفة إلى مورد هيئة TDS، حدد خانة الاختيار **وضع علامة** للحركات.</span><span class="sxs-lookup"><span data-stu-id="6fcca-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="6fcca-140">قم بإغلاق الصفحة **تحرير الحركة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcca-141">في حالة تحديد عدد قليل فقط من الحركات للتسوية في الصفحة **حركات ضريبة الخصم**، فإنه يتم تحديث إجمالي مبلغ TDS للحركات المحددة في الحقل **تصحيح** في الصفحة **تحرير الحركة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="6fcca-142">ويتم تحديث مبلغ التصحيح في بند دفتر اليومية في الصفحة **إيصال دفتر اليومية**، ويتم إغلاق الصفحة **تحرير الحركة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="6fcca-143">في الصفحة **إيصال دفتر اليومية**، يعرض الحقل **مدين** المبلغ الإجمالي للدفع إلى مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="6fcca-144">أدخل تفاصيل الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="6fcca-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6fcca-145">إذا كان لحركات TDS أرقام حساب ضريبة مختلفة (TAN)، فإنه يتم إنشاء بنود دفتر اليومية لكل TAN في الصفحة **إيصال دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="6fcca-146">في علامة التبويب **رسوم الدفع**، في الحقل **معرف الرسوم**، حدد معرف الرسوم الذي يحتوي على نوع رسوم **الفائدة** أو **أخرى** لخصم رسوم الدفع للمدفوعات المتأخرة التي يتم إجراؤها لمورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="6fcca-147">في علامة التبويب **معلومات الضريبة**، في القسم **معلومات الشركة**، يعرض القسم **الاسم** اسم الشركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="6fcca-148">في القسم **ضريبة الخصم**، يعرض الحقل **رقم الحساب الضريبي (TAN)** TAN المرفق ببند الحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="6fcca-149">تحقق من صحة دفتر اليومية وقم بترحيله.</span><span class="sxs-lookup"><span data-stu-id="6fcca-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="6fcca-150">حدد **ضريبة الخصم \> معلومات تشالان‬** لإدخال تفاصيل تشالان‬ للحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="6fcca-151">يعرض الحقل **الإيصال** رقم إيصال الحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="6fcca-152">حدد خانة الاختيار **TDS التي تم إيداعها بواسطة إدخال الدفتر** إذا كان مبلغ TDS يتم إيداعه باستخدام إدخال الدفتر.</span><span class="sxs-lookup"><span data-stu-id="6fcca-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="6fcca-153">في الحقل **رقم تشالان‬**، أدخل رقم تشالان‬ الذي يتم استخدامه لإجراء الدفع إلى مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="6fcca-154">في الحقل **التاريخ**، أدخل تاريخ تشالان‬.</span><span class="sxs-lookup"><span data-stu-id="6fcca-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="6fcca-155">في الحقل **اسم البنك**، حدد اسم البنك الذي يجب أن يتم إيداع مبلغ TDS المستحق إلى مورد هيئة TDS به.</span><span class="sxs-lookup"><span data-stu-id="6fcca-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="6fcca-156">يسرد هذا الحقل كافة الحسابات البنكية التي تم إعدادها لمورد هيئة TDS في **الحسابات الدائنة \> كافة الموردين \> الإعداد \> حسابات بنكية**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="6fcca-157">في الحقل **كود BSR**، أدخل الكود الإرجاع الإحصائي الأساسي للبنك (BSR).</span><span class="sxs-lookup"><span data-stu-id="6fcca-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="6fcca-158">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="6fcca-159">مثال</span><span class="sxs-lookup"><span data-stu-id="6fcca-159">Example</span></span>

<span data-ttu-id="6fcca-160">تتم تسوية الفترة 04/01/2009 لمجموعة مكون TDS **الإيجار** باستخدام عملية تسوية TDS الدورية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="6fcca-161">يتم ترحيل إجمالي مبلغ TDS الذي يبلغ 141.625.00 إلى حساب هيئة مورد TDS لفترة تسوية TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="6fcca-162">يمكنك عرض هذا المبلغ في الحقل **المبلغ** في الصفحة **تحرير الحركة المفتوحة** لمورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="6fcca-163">إذا قمت بتحديد **حركات ضريبة الخصم** لعرض حركات TDS المختلفة التي تمت تسويتها للفترة، يتم عرض المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="6fcca-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="6fcca-164">مبلغ TDS</span><span class="sxs-lookup"><span data-stu-id="6fcca-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="6fcca-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-165">16,995.00</span></span>  |
| <span data-ttu-id="6fcca-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-166">22,660.00</span></span>  |
| <span data-ttu-id="6fcca-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-167">28,325.00</span></span>  |
| <span data-ttu-id="6fcca-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-168">16,995.00</span></span>  |
| <span data-ttu-id="6fcca-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-169">28,325.00</span></span>  |
| <span data-ttu-id="6fcca-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-170">16,995.00</span></span>  |
| <span data-ttu-id="6fcca-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-171">11,330.00</span></span>  |

<span data-ttu-id="6fcca-172">لمبلغ TDS محدد، يمكنك تحديد **مكونات ضريبة الخصم** لعرض TDS الذي تم حسابه لكل مكون ضريبة TDS لكود ضريبة TDS محدد.</span><span class="sxs-lookup"><span data-stu-id="6fcca-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="6fcca-173">بالنسبة لهذا المثال، تقوم بتحديد **مكونات ضريبة الخصم** لمبلغ TDS بمقدار 16.995.00.</span><span class="sxs-lookup"><span data-stu-id="6fcca-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="6fcca-174">يتم عرض مبلغ الضريبة الذي تم حسابه لكل مكون للحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="6fcca-175">مكون الضريبة</span><span class="sxs-lookup"><span data-stu-id="6fcca-175">Tax component</span></span> | <span data-ttu-id="6fcca-176">‏‏المقدار</span><span class="sxs-lookup"><span data-stu-id="6fcca-176">Amount</span></span>    | <span data-ttu-id="6fcca-177">المبلغ التراكمي</span><span class="sxs-lookup"><span data-stu-id="6fcca-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="6fcca-178">TDS</span><span class="sxs-lookup"><span data-stu-id="6fcca-178">TDS</span></span>           | <span data-ttu-id="6fcca-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-179">1,5000.00</span></span> | <span data-ttu-id="6fcca-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-180">125,000.00</span></span>         |
| <span data-ttu-id="6fcca-181">رسوم إضافية</span><span class="sxs-lookup"><span data-stu-id="6fcca-181">Surcharge</span></span>     | <span data-ttu-id="6fcca-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-182">1,500.00</span></span>  | <span data-ttu-id="6fcca-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-183">12,500.00</span></span>          |
| <span data-ttu-id="6fcca-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="6fcca-184">PE-Cess</span></span>       | <span data-ttu-id="6fcca-185">330.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-185">330.00</span></span>    | <span data-ttu-id="6fcca-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-186">2,750.00</span></span>           |
| <span data-ttu-id="6fcca-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="6fcca-187">SHE Cess</span></span>      | <span data-ttu-id="6fcca-188">165.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-188">165.00</span></span>    | <span data-ttu-id="6fcca-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="6fcca-189">1,375.00</span></span>           |

<span data-ttu-id="6fcca-190">إذا قمت بتحديد مبالغ TDS فقط التي تبلغ 16.995.00 و22.660.00 و2,8325.00 للتسوية في الصفحة **حركات ضريبة الخصم**، سيتم عرض المبلغ الإجمالي للتسوية كـ **67,980.00** في الحقل **تصحيح** في الصفحة **تحرير الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="6fcca-191">إذا تم وضع علامة على هذه الحركة للتسوية، يتم إعلاق الصفحة **تحرير الحركة المفتوحة**، ويتم عرض المبلغ **67.980.00** في الحقل **المدين** في الصفحة **إيصال دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="6fcca-192">يمكنك الآن ترحيل دفتر اليومية وإنشاء TDS في تشالان‬.</span><span class="sxs-lookup"><span data-stu-id="6fcca-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="6fcca-193">تسوية المدفوعات المقدمة التي يتم إجراؤها لموردي هيئة TDS</span><span class="sxs-lookup"><span data-stu-id="6fcca-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="6fcca-194">لتعديل دفع مقدم تم إجراؤه على مورد هيئة TDS إلى دفع فعلي، انتقل إلى **الحسابات الدائنة \> الموردون \> جميع الموردين \> تحرير الحركات**.</span><span class="sxs-lookup"><span data-stu-id="6fcca-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="6fcca-195">في حالة تجاوز الدفع الفعلي الذي يتم إجراؤه للدفع المقدم، يتم إنشاء رقمين تشالان‬ للحركة.</span><span class="sxs-lookup"><span data-stu-id="6fcca-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="6fcca-196">ومع ذلك، يتم عرض رقم تشالان‬ الأول فقط في استعلام TDS.</span><span class="sxs-lookup"><span data-stu-id="6fcca-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
