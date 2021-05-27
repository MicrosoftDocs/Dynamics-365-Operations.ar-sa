---
title: يتم ترحيل الضريبة إلى حساب دفتر الأستاذ الخطا في الإيصال
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها التي يمكن ان تساعد في حاله ترحيل الضريبة إلى حساب دفتر الأستاذ الخطا في الإيصال.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020081"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="88629-103">يتم ترحيل الضريبة إلى حساب دفتر الأستاذ الخطا في الإيصال</span><span class="sxs-lookup"><span data-stu-id="88629-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88629-104">أثناء الترحيل، قد يتم ترحيل الضريبة إلى حساب دفتر الأستاذ الخاطئ في الإيصال.</span><span class="sxs-lookup"><span data-stu-id="88629-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="88629-105">لاستكشاف هذه المشكلة وإصلاحها، اتبع الخطوات الواردة في الأقسام التالية عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="88629-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="88629-106">تستخدم الامثله الموجودة في هذا الموضوع أمر المبيعات كمستند اعمال.</span><span class="sxs-lookup"><span data-stu-id="88629-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="88629-107">العثور علي كود الضريبة لحركه الضريبة المرحلة بشكل غير صحيح</span><span class="sxs-lookup"><span data-stu-id="88629-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="88629-108">في صفحة **حركات الإيصال**، حدد الحركة التي ترغب في العمل معها، ثم حدد **ضريبة المبيعات المرحلة**.</span><span class="sxs-lookup"><span data-stu-id="88629-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="88629-109">[![زر ضريبة المبيعات المرحلة في صفحه حركات الإيصال](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="88629-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="88629-110">راجع القيمة في الحقل **كود ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="88629-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="88629-111">في هذا المثال، تكون **VAT 19**.</span><span class="sxs-lookup"><span data-stu-id="88629-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="88629-112">[![حقل كود ضريبة المبيعات في صفحه ضريبة المبيعات المرحلة](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="88629-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="88629-113">فحص مجموعه ترحيل دفتر الأستاذ الخاصة بكود الضريبة</span><span class="sxs-lookup"><span data-stu-id="88629-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="88629-114">انتقل إلى **الضريبة** \> **الضرائب غير المباشرة** \> **ضريبة المبيعات** \> **رموز ضرائب المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="88629-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="88629-115">تتيح البحث عن كود الضريبة وتحديده، ثم مراجعه القيمة الموجودة في حقل **مجموعه ترحيل دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="88629-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="88629-116">في هذا المثال، تكون **VAT**.</span><span class="sxs-lookup"><span data-stu-id="88629-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="88629-117">[![حقل مجموعة ترحيل دفتر الأستاذ في صفحة أكواد ضريبة المبيعات](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="88629-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="88629-118">القيمة في حقل **مجموعة ترحيل دفتر الأستاذ** هي ارتباط.</span><span class="sxs-lookup"><span data-stu-id="88629-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="88629-119">لعرض تفاصيل تكوين المجموعة، حدد الارتباط.</span><span class="sxs-lookup"><span data-stu-id="88629-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="88629-120">بدلا من ذلك، حدد ثم اضغط (أو انقر بزر الماوس الأيمن) في الحقل، ثم حدد **عرض التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="88629-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="88629-121">[![أمر عرض التفاصيل](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="88629-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="88629-122">في حقل **ضريبة المبيعات مستحقه الدفع**، تحقق من صحة رقم الحساب، وذلك وفقا لنوع الحركة.</span><span class="sxs-lookup"><span data-stu-id="88629-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="88629-123">وإذا لم تكن كذلك، فحدد الحساب الصحيح الذي سيتم الترحيل اليه.</span><span class="sxs-lookup"><span data-stu-id="88629-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="88629-124">في هذا المثال، يجب ترحيل ضريبة المبيعات الخاصة بامر التوريد إلى حساب ضريبة المبيعات المستحقة الدفع 222200.</span><span class="sxs-lookup"><span data-stu-id="88629-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="88629-125">[![حقل ضريبة المبيعات المستحقة في صفحة مجموعات ترحيل دفتر الأستاذ](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="88629-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="88629-126">يوفر الجدول التالي معلومات حول كل حقل في صفحة **مجموعات ترحيل دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="88629-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="88629-127">الحقل</span><span class="sxs-lookup"><span data-stu-id="88629-127">Field</span></span>                  | <span data-ttu-id="88629-128">الوصف</span><span class="sxs-lookup"><span data-stu-id="88629-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="88629-129">ضريبة المبيعات مستحقة الدفع</span><span class="sxs-lookup"><span data-stu-id="88629-129">Sales tax payable</span></span>      | <span data-ttu-id="88629-130">الحساب الرئيسي لضرائب المبيعات الصادرة المستحقة لهيئه الضرائب.</span><span class="sxs-lookup"><span data-stu-id="88629-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="88629-131">ضريبة المبيعات مستحقة القبض</span><span class="sxs-lookup"><span data-stu-id="88629-131">Sales tax receivable</span></span>   | <span data-ttu-id="88629-132">الحساب الرئيسي للضرائب الواردة الواردة من مصلحة الضرائب.</span><span class="sxs-lookup"><span data-stu-id="88629-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="88629-133">مصروفات ضريبة الانتفاع</span><span class="sxs-lookup"><span data-stu-id="88629-133">Use tax expense</span></span>        | <span data-ttu-id="88629-134">الحساب الرئيسي المستخدم لترحيل ضرائب الاستخدام القابلة للخصم التي لا يطالب بها البائعون أو يقدموا تقارير إلى مصلحة الضرائب كجزء من ضريبة السلع والخدمات (GST) / ضريبة المبيعات المنسقة (HST) في الاتحاد الأوروبي (EU).</span><span class="sxs-lookup"><span data-stu-id="88629-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="88629-135">يجب تحديد **استخدام الضريبة** لرمز ضريبة المبيعات في مجموعة ضريبة المبيعات المستخدمة في الحركة.</span><span class="sxs-lookup"><span data-stu-id="88629-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="88629-136">لا يتوفر هذا الحقل إذا كان **تطبيق قواعد فرض ضرائب على المبيعات** محددًا في صفحة **محددات دفتر الأستاذ العام**.</span><span class="sxs-lookup"><span data-stu-id="88629-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="88629-137">ضريبة الانتفاع الدائنة</span><span class="sxs-lookup"><span data-stu-id="88629-137">Use tax payable</span></span>        | <span data-ttu-id="88629-138">الحساب الرئيسي المستخدم لترحيل ضرائب الاستخدام الوارد التي تمت الدفع لها إلى هيئات الضرائب.</span><span class="sxs-lookup"><span data-stu-id="88629-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="88629-139">حساب التسوية</span><span class="sxs-lookup"><span data-stu-id="88629-139">Settlement account</span></span>     | <span data-ttu-id="88629-140">الحساب الرئيسي المستخدم لترحيل صافي رصيد حسابات دفتر الأستاذ المحدد في حقلي **استخدام الضريبة مستحقة الدفع** و **ضريبة المبيعات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="88629-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="88629-141">الخصم النقدي للمورد</span><span class="sxs-lookup"><span data-stu-id="88629-141">Vendor cash discount</span></span>   | <span data-ttu-id="88629-142">الحساب الرئيسي المستخدم لترحيل خصم نقدي لأكواد ضريبة المبيعات المرتبطة بمجموعة ترحيل دفتر الأستاذ هذه.</span><span class="sxs-lookup"><span data-stu-id="88629-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="88629-143">الخصم النقدي للعميل</span><span class="sxs-lookup"><span data-stu-id="88629-143">Customer case discount</span></span> | <span data-ttu-id="88629-144">الحساب الرئيسي المستخدم لترحيل خصم نقدي لأكواد ضريبة المبيعات المرتبطة بمجموعة ترحيل دفتر الأستاذ هذه.</span><span class="sxs-lookup"><span data-stu-id="88629-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="88629-145">لمزيد من المعلومات، راجع [إعداد مجموعات ترحيل دفتر الأستاذ لضريبة المبيعات](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="88629-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="88629-146">تصحيح في التعليمات البرمجية للتحقق من ابعاد دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="88629-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="88629-147">في الكود، يتم تحديد حساب الترحيل حسب بعد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="88629-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="88629-148">يقوم بعد دفتر الأستاذ بحفظ معرف السجل الخاص بأحد الحسابات في قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="88629-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="88629-149">بالنسبة لأمر التوريد، أضف نقطه توقف في أسلوبي **Tax::saveAndPost()** و **Tax::post()**.</span><span class="sxs-lookup"><span data-stu-id="88629-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="88629-150">انتبه إلى قيمة **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="88629-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="88629-151">[![نموذج لكود أمر المبيعات الذي يحتوي علي نقطه توقف](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="88629-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="88629-152">لأمر الشراء، أضف نقطة توقف عند أسلوبي **TaxPost::saveAndPost()** و **TaxPost::postToTaxTrans()**.</span><span class="sxs-lookup"><span data-stu-id="88629-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="88629-153">انتبه إلى قيمة **\_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="88629-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="88629-154">[![نموذج لكود أمر الشراء الذي يحتوي علي نقطه توقف](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="88629-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="88629-155">قم بتشغيل استعلام SQL التالي للعثور على قيمة عرض الحساب في قاعدة البيانات، بناءً على معرف السجل الذي تم حفظه بواسطة بُعد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="88629-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="88629-156">[![عرض قيمة معرف السجل](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="88629-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="88629-157">افحص Callstack لتجد مكان تعيين قيمة **_ledgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="88629-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="88629-158">عادةً ما تكون القيمة من **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="88629-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="88629-159">في هذه الحالة، يجب إضافة نقطة توقف عند **TmpTaxWorkTrans::insert()** و **TmpTaxWorkTrans::update()** للعثور على مكان تعيين القيمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="88629-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="88629-160">حدد ما إذا كان التخصيص موجودًا</span><span class="sxs-lookup"><span data-stu-id="88629-160">Determine whether customization exists</span></span>

<span data-ttu-id="88629-161">إذا كنت قد أكملت الخطوات الواردة في الأقسام السابقة ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="88629-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="88629-162">في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.</span><span class="sxs-lookup"><span data-stu-id="88629-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
