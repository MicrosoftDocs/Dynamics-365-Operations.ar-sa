---
title: حساب TDS على الفواتير باستخدام دفاتر اليومية
description: يسرد هذا الموضوع خطوات حساب الضريبة المخصومة في المصدر (TDS) على دفاتر اليومية.
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023012"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="cc263-103">حساب TDS على الفواتير باستخدام دفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="cc263-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc263-104">يسرد هذا الموضوع خطوات حساب الضريبة المخصومة في المصدر (TDS) على دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="cc263-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="cc263-105">ابدأ بفتح الصفحة **دفاتر اليومية العامة** (**دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة**).</span><span class="sxs-lookup"><span data-stu-id="cc263-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="cc263-106">[![دفاتر اليومية العامة](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="cc263-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="cc263-107">قم بإنشاء بنود دفتر اليومية باستخدام نماذج دفاتر اليومية التي يتم سردها في الجدول.</span><span class="sxs-lookup"><span data-stu-id="cc263-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="cc263-108">حدد نوع الحساب ونوع الحساب المقابل، ثم أدخل مبلغ الحركة.</span><span class="sxs-lookup"><span data-stu-id="cc263-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="cc263-109">في الصفحة **دفتر يومية اعتماد الفواتير**، حدد **البحث عن إيصالات** وحدد فواتير لحساب TDS بها.</span><span class="sxs-lookup"><span data-stu-id="cc263-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="cc263-110">اعرض الفواتير التي تم إنشاؤها في الصفحة **سجل الفواتير** أو الصفحة **البحث عن إيصالات**.</span><span class="sxs-lookup"><span data-stu-id="cc263-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="cc263-111">في علامة التبويب **عام** من الصفحة **إيصال دفتر اليومية**، قم بعرض أو تعديل مجموعة TDS الافتراضية المحددة للمورد أو العميل، في الحقل **مجموعة TDS**</span><span class="sxs-lookup"><span data-stu-id="cc263-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="cc263-112">يعتمد مبلغ TDS الذي يتم حسابه في بنود دفتر اليومية على المعادلة المحددة لأكواد الضريبة TDS المدرجة في الحقل **مجموعة TDS**.</span><span class="sxs-lookup"><span data-stu-id="cc263-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="cc263-113">لا يتوفر الحقل **مجموعة ضريبة الخصم**  والحقل **مجموعة TCS** عندما تقوم بتحديد مجموعة TDS في الحقل **مجموعة TDS**.</span><span class="sxs-lookup"><span data-stu-id="cc263-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="cc263-114">يتوفر الحقل **مجموعة ضريبة الخصم** في الصفحة **دفتر اليومية العام** فقط.</span><span class="sxs-lookup"><span data-stu-id="cc263-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="cc263-115">يتم حساب TDS فقط إذا تم تحديد خانة اختيار **حساب ضريبة الخصم** للمورد أو العميل في الصفحتين **جميع الموردين** أو **جميع العملاء**.</span><span class="sxs-lookup"><span data-stu-id="cc263-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="cc263-116">حدد علامة التبويب **معلومات الضريبة**: حدد العناوين البديلة لشركة يتم إعدادها للشركة في هذا الحقل، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="cc263-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="cc263-117">يمكنك عرض اسم الشركة في الحقل **الاسم**، الموجود ضمن مجموعة الحقل **معلومات الشركة**.</span><span class="sxs-lookup"><span data-stu-id="cc263-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="cc263-118">تعرض طبيعة فئة المقيم للمورد أو العميل في الحقل **طبيعة حقل المقيم**، والتي توجد ضمن مجموعة الحقل **ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="cc263-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="cc263-119">في الحقل **رقم حساب الضريبة** (**TAN**)، اعرض TAN الخاص باسم الشركة المحدد الذي يتم عرضه.</span><span class="sxs-lookup"><span data-stu-id="cc263-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="cc263-120">حدد **ضريبة الخصم** في قائمة **ضريبة الخصم** لفتح الصفحة **حركات ضريبة الخصم المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="cc263-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="cc263-121">يتم عرض الحقول التالية في الجزء العلوي من الصفحة **حركات ضريبة الخصم المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="cc263-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="cc263-122">**إجمالي مبلغ ضريبة الخصم** - إجمالي TDS المحسوب للحركة لمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc263-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="cc263-123">**القيمة** - النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="cc263-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="cc263-124">يستند إجمالي النسبة المئوية إلى المعادلة التي يتم تحديدها لأكواد الضريبة TDS المرتبطة بمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc263-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="cc263-125">**إجمالي مبلغ ضريبة الخصم المعدل** - إجمالي مبلغ TDS المعدل لكافة أكواد الضريبة في مجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc263-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="cc263-126">**TDS** - في حالة تحديده، يتم إرفاق مجموعة TDS بالحركة.</span><span class="sxs-lookup"><span data-stu-id="cc263-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="cc263-127">تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **التعديل** في الصفحة **حركات ضريبة الخصم المؤقتة** تفاصيل مبلغ TDS المحسوب ومبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc263-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="cc263-128">حدد **الحد** لفتح الصفجة **الحد**.</span><span class="sxs-lookup"><span data-stu-id="cc263-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="cc263-129">اعرض الحد والحد الاستثنائي المحدد لمكون الضريبة TDS المرفق بكود ضريبة TDS محدد في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc263-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="cc263-130">حدد **مصمم الصيغ** لفتح النموذج **مصمم الصيغة**.</span><span class="sxs-lookup"><span data-stu-id="cc263-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="cc263-131">اعرض المعادلة المحددة لكود ضريبة TDS محدد في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc263-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="cc263-132">قم بإغلاق الصفحات **مصمم المعادلة** و **حركات ضريبة الخصم المؤقتة** للرجوع إلى الصفحة **إيصال دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="cc263-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="cc263-133">أدخل التفاصيل الأخرى المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="cc263-133">Enter the other required details.</span></span> <span data-ttu-id="cc263-134">تحقق من صحة دفتر اليومية وقم بترحيله.</span><span class="sxs-lookup"><span data-stu-id="cc263-134">Validate and post the journal.</span></span> <span data-ttu-id="cc263-135">يتم ترحيل مبلغ TDS الذي يتم حسابه على فواتير الشراء إلى الحساب الدائن.</span><span class="sxs-lookup"><span data-stu-id="cc263-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="cc263-136">يتم ترحيل مبلغ TDS الذي يتم حسابه في فواتير المبيعات إلى الحساب المدين الذي يتم تحديده لكل كود ضريبة TDS في المجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc263-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="cc263-137">يتم تحديد الحسابات الدائنة أو الحسابات المدينة لأكواد ضريبة TDS في الصفحة **أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="cc263-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="cc263-138">حدد **ضريبة الخصم المرحلة** لفتح الصفحة **حركات** **ضريبة** **الحركات**.</span><span class="sxs-lookup"><span data-stu-id="cc263-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="cc263-139">في الحقل **القيمة**، يتم عرض إجمالي النسبة المئوية المستخدمة لحساب TDS للحركة.</span><span class="sxs-lookup"><span data-stu-id="cc263-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="cc263-140">تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **مبلغ** في الصفحة حركات ضريبة الخصم المؤقتة تفاصيل مبلغ TDS المحسوب ومبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="cc263-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
