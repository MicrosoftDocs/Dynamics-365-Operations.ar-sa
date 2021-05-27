---
title: حساب TDS على الفواتير من صفحة فاتورة النص الحر
description: يوضح هذا الموضوع كيفية حساب الضريبة المخصومة في المصدر (TDS) على الفواتير باستخدام الصفحة فاتورة النص الحر.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023004"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="d0782-103">حساب TDS على الفواتير من صفحة فاتورة النص الحر</span><span class="sxs-lookup"><span data-stu-id="d0782-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0782-104">يوضح هذا الموضوع كيفية حساب الضريبة المخصومة في المصدر (TDS) على الفواتير باستخدام الصفحة **فاتورة النص الحر**:</span><span class="sxs-lookup"><span data-stu-id="d0782-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="d0782-105">انتقل إلى **الحسابات المدينة \> الفواتير \> جميع الفواتير ذات نص حر‬**.</span><span class="sxs-lookup"><span data-stu-id="d0782-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="d0782-106">[![صفحة الفاتورة ذات النص الحر](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="d0782-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="d0782-107">حدد **جديد** لإنشاء فاتورة نص حر، ثم أدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d0782-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="d0782-108">حدد علامة التبويب **الفاتورة**. في القسم **مجموعة ضريبة الخصم**، يعرض الحقل **طبيعة المقيم** طبيعة فئة المقيم الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="d0782-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="d0782-109">في الحقل **مجموعة TDS**، قم بمراجعة مجموعة TDS الافتراضية المحددة للعميل أو تغييرها.</span><span class="sxs-lookup"><span data-stu-id="d0782-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d0782-110">عندما تقوم بتحديد قيمة في الحقل **مجموعة TDS**، يصبح الحقل **مجموعة TDS** غير متوفر.</span><span class="sxs-lookup"><span data-stu-id="d0782-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="d0782-111">يتم حساب TDS فقط إذا تم تعيين الخيار **حساب ضريبة الخصم** إلى **نعم** لجميع العملاء في الصفحة **جميع العملاء**.</span><span class="sxs-lookup"><span data-stu-id="d0782-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="d0782-112">من علامة التبويب **معلومات الضريبة**، في القسم **معلومات الشركة**، في الحقل **الاسم**، حدد اسم الشركة لعنوان بديل تم إعداده للشركة.</span><span class="sxs-lookup"><span data-stu-id="d0782-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="d0782-113">في القسم **ضريبة الخصم**، يعرض الحقل **رقم حساب الضريبة (TAN)** رقم حساب الضريبة (TAN) للشركة المحددة.</span><span class="sxs-lookup"><span data-stu-id="d0782-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="d0782-114">في علامة التبويب **بنود الفاتورة**، قم بإنشاء بنود الفاتورة وأدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="d0782-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="d0782-115">في القسم **مجموعة ضريبة الخصم**، يعرض الحقل **رقم حساب الضريبة (TAN)** رقم TAN، ويعرض الحقل **مجموعة TAN** مجموعة TAN.</span><span class="sxs-lookup"><span data-stu-id="d0782-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="d0782-116">حدد **ضريبة الخصم** لفتح الصفحة **حركات ضريبة الخصم المؤقتة**.</span><span class="sxs-lookup"><span data-stu-id="d0782-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="d0782-117">يحتوي الجزء العلوي من هذه الصفحة على الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="d0782-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="d0782-118">**إجمالي مبلغ ضريبة الخصم** – إجمالي TDS المحسوب للحركة لمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="d0782-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="d0782-119">**القيمة** – النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="d0782-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="d0782-120">يستند إجمالي النسبة المئوية إلى المعادلة التي يتم تحديدها لأكواد الضريبة TDS المرتبطة بمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="d0782-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="d0782-121">**إجمالي مبلغ ضريبة الخصم المعدل** – إجمالي مبلغ TDS المعدل لكافة أكواد الضريبة في مجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="d0782-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="d0782-122">**TDS** – تشير خانة الاختيار المحددة إلى أنه تم إرفاق مجموعة TDS بالحركة.</span><span class="sxs-lookup"><span data-stu-id="d0782-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="d0782-123">تعرض الحقول الموجودة على علامات التبويب **نظرة عامة** و **عام** و **تسوية** مبلغ TDS المحسوب وتفاصيل مبلغ TDS المعدل لكل كود ضريبة TDS مرفق بالمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="d0782-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="d0782-124">حدد **الحد** لفتح الصفحة **الحد**، حيث يمكنك مراجعة الحد الذي يتم تحديده لمكون الضريبة TDS الذي تم إرفاقه بكود ضريبة TDS محدد.</span><span class="sxs-lookup"><span data-stu-id="d0782-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="d0782-125">حدد **مصمم المعادلة** لفتح الصفحة **مصمم المعادلة**، حيث يمكنك مراجعة المعادلة التي يتم تحديدها لكود ضريبة TDS محدد.</span><span class="sxs-lookup"><span data-stu-id="d0782-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="d0782-126">قم بترحيل الفاتورة ذات النص الحر.</span><span class="sxs-lookup"><span data-stu-id="d0782-126">Post the free text invoice.</span></span> <span data-ttu-id="d0782-127">يتم ترحيل مبلغ TDS الذي يتم حسابه في فواتير النص الحر إلى الحساب المدين الذي يتم تحديده لكل كود ضريبة TDS في المجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="d0782-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="d0782-128">يتم تحديد الحسابات المدينة لأكواد ضريبة TDS في الصفحة **أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="d0782-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="d0782-129">حدد **ضريبة الخصم المرحلة** لفتح الصفحة **حركات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="d0782-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="d0782-130">يعرض الحقل **القيمة** النسبة المئوية الإجمالية المستخدمة لحساب TDS الخاصة بالحركة.</span><span class="sxs-lookup"><span data-stu-id="d0782-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="d0782-131">تعرض علامات التبويب **نظرة عامة** و **عام** و **المبلغ** مبالغ TDS التي تم حسابها في بنود الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d0782-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="d0782-132">قم بمراجعة معلومات حساب TDS لكل كود ضريبة TDS مرفق بالمجموعة TDS.</span><span class="sxs-lookup"><span data-stu-id="d0782-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
