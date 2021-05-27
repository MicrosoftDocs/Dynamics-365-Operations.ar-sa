---
title: إرفاق أكواد ضريبة TDS بمجموعات ضرائب TDS وتحديد معادلة حساب TDS
description: يوضح هذا الموضوع كيفية إعداد الضريبة المخصومة في مجموعات ضرائب المصدر (TDS) وإرفاق أكواد ضريبة TDS بمجموعات ضريبة TDS. لحساب TDS لمجموعة ضرائب TDS، يجب عليك تحديد المعادلة لأكواد الضريبة TDS المرفقة بها.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023007"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="bd476-104">إرفاق أكواد ضريبة TDS بمجموعات ضرائب TDS وتحديد معادلة حساب TDS</span><span class="sxs-lookup"><span data-stu-id="bd476-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd476-105">يوضح هذا الموضوع كيفية إعداد الضريبة المخصومة في مجموعات ضرائب المصدر (TDS) وإرفاق أكواد ضريبة TDS بمجموعات ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="bd476-106">لحساب TDS لمجموعة ضرائب TDS، يجب عليك تحديد المعادلة لأكواد الضريبة TDS المرفقة بها.</span><span class="sxs-lookup"><span data-stu-id="bd476-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="bd476-107">اتبع هذه الخطوات لإعداد مجموعة ضرائب TDS، وإرفاق أكواد ضريبة TDS بها، وحدد المعادلة لحساب TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="bd476-108">انتقل إلى **ضريبة \> ضرائب غير مباشرة \> ضريبة خصم \> مجموعات ضرائب الخصم**.</span><span class="sxs-lookup"><span data-stu-id="bd476-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="bd476-109">[![صفحة مجموعات ضرائب الخصم](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="bd476-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="bd476-110">في جزء الإجراء، حدد **جديد** لإنشاء مجموعة ضريبة خصم لـ TDS، وأدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bd476-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="bd476-111">في الحقل **نوع الضريبة**، حدد **TDS**.</span><span class="sxs-lookup"><span data-stu-id="bd476-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="bd476-112">في علامة التبويب السريعة **الإعداد**، حدد **إضافة** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="bd476-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="bd476-113">في الحقل **كود ضريبة الخصم**، حدد كود ضريبة TDS لمجموعة ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="bd476-114">يظهر الحقل **اسم ضريبة الخصم** اسم كود الضريبة TDS، ويعرض الحقل **القيمة** القيمة.</span><span class="sxs-lookup"><span data-stu-id="bd476-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="bd476-115">لتجاهل الحد والحد الاستثنائي الذي يتم تحديده لمكون الضريبة TDS الذي يتم إرفاقه بكود ضريبة TDS في حركات TDS، حدد خانة الاختيار **حد الاطلاع**.</span><span class="sxs-lookup"><span data-stu-id="bd476-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="bd476-116">لمنع مجموعة الضريبة من حسابها في حركات، حدد خانة الاختيار **إعفاء**.</span><span class="sxs-lookup"><span data-stu-id="bd476-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="bd476-117">في جزء الإجراء، حدد **المصمم** لفتح مصمم المعادلة، بحيث يمكنك تحديد المعادلة لحساب TDS لمجموعة ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="bd476-118">في الصفحة **المصمم**، تعرض علامة التبويب **الضرائب** أكواد ضريبة TDS التي تم تحديدها لمجموعة ضريبة التي لها TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="bd476-119">[![مصمم الصفحة](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="bd476-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="bd476-120">في علامة التبويب **الحساب**، حدد **TDS** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="bd476-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="bd476-121">يعرض الحقل **المعرف** معرف الأولوية الذي يتم إنشاؤه تلقائيًا لحساب TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="bd476-122">في الحقل **كود الضريبة**، حدد كود ضريبة TDS لتحديد المعادلة.</span><span class="sxs-lookup"><span data-stu-id="bd476-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="bd476-123">تتوفر كافة أكواد ضريبة TDS التي تم تحديدها لمجموعة ضريبة TDS للتحديد في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="bd476-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="bd476-124">في الحقل **الأساس خاضع للضريبة**، حدد أساس حساب TDS:</span><span class="sxs-lookup"><span data-stu-id="bd476-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="bd476-125">**إجمالي المبلغ** – يقوم بحساب الـ TDS استنادًا إلى إجمالي مبلغ الحركة (أي، مبلغ الفاتورة) باستخدام تعبير الحساب الذي يتم تحديده لكود الضريبة.</span><span class="sxs-lookup"><span data-stu-id="bd476-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="bd476-126">**استثناء المبلغ الإجمالي** – يقوم بحساب TDS استنادًا إلى تعبير الحساب الذي يتم تحديده لكود الضريبة.</span><span class="sxs-lookup"><span data-stu-id="bd476-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd476-127">يتعذر تعيين الحقل **الأساس خاضع للضريبة** لكود ضريبة على **استثناء المبلغ الإجمالي** لكود ضريبة TDS الذي يحتوي على معرف الأولوية **1**.</span><span class="sxs-lookup"><span data-stu-id="bd476-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="bd476-128">يستند حساب TDS إلى المعادلة المحددة في الحقل **تعبير الحساب** لكل كود ضريبة مرفق بمجموعة ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="bd476-129">حدد زر علامة الجمع (**+**) أو علامة الطرح (**-**)، أو علامة الضرب (**\**_)، أو علامة القسمة (_*/**) القسمة لإدخال تعبير الحساب لكود ضريبة TDS المحدد في الحقل **تعبير الحساب**.</span><span class="sxs-lookup"><span data-stu-id="bd476-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd476-130">لا يمكن تحديد أي تعبير حساب لكود ضريبة TDS الذي يحتوي على معرف الأولوية **1**.</span><span class="sxs-lookup"><span data-stu-id="bd476-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="bd476-131">لتحديد تعبير الحساب لكود ضريبة TDS في الحقل **تعبير الحساب**، أضف أكواد ضريبة TDS المتوفرة في علامة التبويب **الضرائب**. لإضافة أكواد ضريبة TDS في الحقل **تعبير الحساب**، يمكنك استخدام أي من الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="bd476-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="bd476-132">اسحب كود الضريبة المطلوب من علامة التيبويب **الضرائب** إلى الحقل **تعبير الحساب**.</span><span class="sxs-lookup"><span data-stu-id="bd476-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="bd476-133">اضغط ضغطًا مزدوجًا (أو انقر نقرًا مزدوجًا) على كود الضريبة المطلوبة من علامة التبويب **الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="bd476-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="bd476-134">حدد واضغط مع الاستمرار (أو انقر بزر الماوس الأيمن) على كود الضريبة المطلوبة على علامة التبويب **الضرائب**، ثم حدد **إضافة كود الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="bd476-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd476-135">أدرج تعبير حساب قبل كل كود ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="bd476-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="bd476-136">تظهر أكواد ضريبة TDS التي تمت إضافتها إلى تعبير الحساب بين قوسين (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="bd476-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="bd476-137">لمسح تعبير الحساب الذي يتم تحديده لكود الضريبة في الحقل **تعبير الحساب**، حدد الزر **C**.</span><span class="sxs-lookup"><span data-stu-id="bd476-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="bd476-138">لحذف سجل على علامة التبويب **الحساب**، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="bd476-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="bd476-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bd476-139">Close the page.</span></span>
