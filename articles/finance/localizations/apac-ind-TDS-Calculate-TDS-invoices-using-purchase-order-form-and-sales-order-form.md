---
title: حساب فواتير TDS باستخدام نموذج أمر شراء ونموذج أمر مبيعات
description: يسرد هذا الموضوع خطوات حساب الضريبة المخصومة في المصدر (TDS) على أنواع متعددة من الفواتير.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022988"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="4c719-103">حساب فواتير TDS باستخدام نموذج أمر شراء ونموذج أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="4c719-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c719-104">يسرد هذا الموضوع خطوات حساب الضريبة المخصومة في المصدر (TDS) على أنواع متعددة من الفواتير باستخدام الصفحات  **أمر الشراء** و **دفتر يومية الشراء** و **أمر الشراء المفتوح** و **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="4c719-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="4c719-105">قم بإنشاء أمر شراء أو دفتر يومية الشراء أو أمر شراء مفتوح أو أمر شراء باستخدام الصفحة المدرجة.</span><span class="sxs-lookup"><span data-stu-id="4c719-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="4c719-106">أدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="4c719-106">Enter the required details.</span></span>

2. <span data-ttu-id="4c719-107">حدد علامة التبويب **إعداد** لعرض طبيعة مقيم المورد أو العميل.</span><span class="sxs-lookup"><span data-stu-id="4c719-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="4c719-108">يتم سرد هذه المعلومات في الحقل **طبيعة المقيم**، ضمن الحقل **مجموعة ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="4c719-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="4c719-109">في الحقل **مجموعة TDS**، قم بعرض مجموعة TDS الافتراضية المحددة للمورد أو العميل أو تعديلها.</span><span class="sxs-lookup"><span data-stu-id="4c719-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4c719-110">لا يتوفر الحقل **مجموعة TDS** عندما تقوم بتحديد مجموعة TDS في الحقل **مجموعة TDS**.</span><span class="sxs-lookup"><span data-stu-id="4c719-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="4c719-111">يتم حساب TDS فقط إذا تم تحديد خانة اختيار **حساب ضريبة الخصم** للمورد أو العميل في الصفحة **جميع الموردين** أو **جميع العملاء**.</span><span class="sxs-lookup"><span data-stu-id="4c719-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="4c719-112">قم بإنشاء بنود الصنف من علامة التبويب **البنود** وأدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="4c719-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="4c719-113">حدد علامة التبويب **إعداد** (على مستوي البند) لعرض مجموعة TDS المحددة على مستوى الراس أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="4c719-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="4c719-114">يتم عرض المجموعة TDS في الحقل **مجموعة TDS**، التي توجد ضمن مجموعة الحقل **مجموعة ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="4c719-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="4c719-115">حدد علامة التبويب **معلومات الضريبة** وحدد العناوين البديلة التي يتم إعدادها لاسم الشركة المعروض في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="4c719-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="4c719-116">يتم عرض اسم الشركة في الحقل **الاسم**، الموجود ضمن مجموعة الحقل **معلومات الشركة**.</span><span class="sxs-lookup"><span data-stu-id="4c719-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="4c719-117">يتم عرض TAN لاسم الشركة المحددة في الحقل **رقم حساب الضريبة** (**TAN**) مجموعة الحقل **ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="4c719-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="4c719-118">حدد **ضريبة الخصم** لفتح الصفحة **حركات ضريبة الخصم المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="4c719-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="4c719-119">اعرض الحقول التالية في الجزء العلوي من الصفحة **حركات ضريبة الخصم المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="4c719-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="4c719-120">**مبلغ** **ضريبة** **الخصم** **في** **الإجمالي** - يتم حساب إجمالي TDS للحركة لمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="4c719-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="4c719-121">**القيمة** - النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="4c719-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="4c719-122">يستند إجمالي النسبة المئوية إلى المعادلة التي يتم تحديدها لأكواد الضريبة TDS المرتبطة بمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="4c719-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="4c719-123">**إجمالي مبلغ ضريبة الخصم المعدل** - إجمالي مبلغ TDS المعدل لكافة أكواد الضريبة في مجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="4c719-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="4c719-124">**TDS** - في حالة تحديده، يتم إرفاق مجموعة TDS بالحركة.</span><span class="sxs-lookup"><span data-stu-id="4c719-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="4c719-125">تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **التعديل** في الصفحة **حركات ضريبة الخصم المؤقتة** تفاصيل مبلغ TDS المحسوب ومبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="4c719-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="4c719-126">حدد **الحد** لفتح الصفجة **الحد**.</span><span class="sxs-lookup"><span data-stu-id="4c719-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="4c719-127">اعرض الحد المحدد لمكون الضريبة TDS المرفق بكود ضريبة TDS محدد في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4c719-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="4c719-128">حدد **مصمم الصيغ** لفتح الصفحة **مصمم الصيغة**.</span><span class="sxs-lookup"><span data-stu-id="4c719-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="4c719-129">اعرض المعادلة المحددة لكود ضريبة TDS محدد في هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4c719-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="4c719-130">قم بترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="4c719-130">Post the invoice.</span></span> <span data-ttu-id="4c719-131">يتم ترحيل مبلغ TDS المحسوب في فواتير الشراء إلى الحساب الدائن ويتم ترحيل مبلغ TDS الذي تم حسابه في فواتير المبيعات إلى الحساب المدين الذي بتم تحديده لكل كود ضريبة TDS في المجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="4c719-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="4c719-132">يتم تحديد الحسابات الدائنة أو الحسابات المدينة لأكواد ضريبة TDS في الصفحة **أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="4c719-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="4c719-133">حدد **الزر** استعلام **> الفاتورة > الزر ضريبة الخصم المرحلة** لفتح الصفحة **حركة ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="4c719-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="4c719-134">يمكنك عرض النسبة المئوية الإجمالية المستخدمة لحساب TDS للحركة في الحقل **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="4c719-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="4c719-135">تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **المبلغ** على الصفحة **حركات ضريبة الخصم** معلومات TDS المحسوبة للحركة.</span><span class="sxs-lookup"><span data-stu-id="4c719-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="4c719-136">اعرض معلومات حساب TDS لكل كود ضريبة TDS مرفق بالمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="4c719-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
