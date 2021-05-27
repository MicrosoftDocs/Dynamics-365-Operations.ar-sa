---
title: إعداد رسوم الدفع للمدفوعات إلى هيئة TDS
description: يوضح هذا الموضوع كيفية إعداد رسوم الدفع التي يتم تحميلها بالنسبة لمدفوعات هيئة ضريبة المخصومة في المصدر (TDS).
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023013"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="c02c6-103">إعداد رسوم الدفع للمدفوعات إلى هيئة TDS</span><span class="sxs-lookup"><span data-stu-id="c02c6-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c02c6-104">يوضح هذا الموضوع كيفية إعداد رسوم الدفع التي يتم تحميلها بالنسبة لمدفوعات هيئة ضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="c02c6-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="c02c6-105">انتقل إلى **الحسابات المدينة \> إعداد الدفع \> رسوم الدفع**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="c02c6-106">[![صفحة رسوم الدفع](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="c02c6-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="c02c6-107">حدد **جديد** لإنشاء رسوم الدفع، ثم أدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c02c6-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="c02c6-108">في الحقل **نوع الرسوم**، حدد نوع رسوم الدفع:</span><span class="sxs-lookup"><span data-stu-id="c02c6-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="c02c6-109">**بلا**</span><span class="sxs-lookup"><span data-stu-id="c02c6-109">**None**</span></span>
    - <span data-ttu-id="c02c6-110">**الفائدة** يتم تحميل الفائدة على المدفوعات المتأخرة التي يتم إجراؤها على مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="c02c6-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="c02c6-111">**أخرى** يتم تحميل الفوائد الأخرى على المدفوعات المتأخرة التي يتم إجراؤها على مورد هيئة TDS.</span><span class="sxs-lookup"><span data-stu-id="c02c6-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="c02c6-112">إذا قمت بتحديد **الفائدة** أو **أخرى**، فإنه يتم تعيين الحقل **التكلفة** تلقائيًا إلى **دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="c02c6-113">إذا قمت بتحديد **الفائدة** أو **أخرى** في الحقل **نوع الحقل**، في الحقل **الحساب الرئيسي**، حدد حساب دفتر الأستاذ لترحيل الفائدة أو المصاريف الأخرى إليه.</span><span class="sxs-lookup"><span data-stu-id="c02c6-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="c02c6-114">أدخل التفاصيل الأخرى المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c02c6-114">Enter the other required details.</span></span>
6. <span data-ttu-id="c02c6-115">في جزء الإجراء، حدد **إعداد رسوم الدفع** لفتح الصفحة **إعداد رسوم الدفع**، حيث يمكنك إعداد رسوم الدفع لمجموعات متعددة من البنوك وطرق الدفع ومواصفات الدفع والعملات وفترات التاريخ.</span><span class="sxs-lookup"><span data-stu-id="c02c6-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="c02c6-116">[![صفحة إعداد رسوم الدفع](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="c02c6-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="c02c6-117">في علامة التبويب **نظرة عامة**، في الحقل **التجميع**، حدد البنوك التي تقوم بإعداد رسوم الدفع لها:</span><span class="sxs-lookup"><span data-stu-id="c02c6-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="c02c6-118">**الجدول** – تكون الرسوم صالحة لحساب بنك معين.</span><span class="sxs-lookup"><span data-stu-id="c02c6-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="c02c6-119">**المجموعة** – تكون الرسوم صالحة لمجموعة بنك معين.</span><span class="sxs-lookup"><span data-stu-id="c02c6-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="c02c6-120">**الكل** – الرسوم صالحة لكافة حسابات البنوك..</span><span class="sxs-lookup"><span data-stu-id="c02c6-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="c02c6-121">إذا قمت بتحديد **جدول** أو **مجموعة** في الحقل **التجميع**، في الحقل **علاقة البنك**، حدد الحساب البنكي المحدد أو المجموعة البنكية التي تقوم بإعداد رسوم الدفع لها.</span><span class="sxs-lookup"><span data-stu-id="c02c6-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="c02c6-122">في الحقل **طريقة الدفع**، حدد طريقة الدفع لدفع الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="c02c6-123">في الحقل **مواصفات الدفع**، حدد أو أدخل كود مواصفات الدفع الذي يتم إنشاؤه في الصفحة **مواصفات الدفع**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="c02c6-124">يتم استخدام مواصفات الدفع مع طرق الدفع التي تتم بواسطة تحويل الأموال إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="c02c6-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="c02c6-125">في الحقل **عملة الدفع**، حدد العملة التي تنشط الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="c02c6-126">لا يمكن تنشيط الرسوم إلا من خلال الحركات التي تستخدم العملة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c02c6-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="c02c6-127">في حالة ترك هذا الحقل فارغًا، تقوم كافة العملات بتنشيط الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="c02c6-128">في الحقل **النسبة المئوية/المبلغ**، حدد أسلوب الحساب.</span><span class="sxs-lookup"><span data-stu-id="c02c6-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="c02c6-129">الخيارات هي **المبلغ** و **النسبة المئوية** و **الفاصل**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="c02c6-130">في الحقل **مبلغ الرسوم**، حدد مبلغ الرسوم إما كنسبة مئوية من الدفع أو المبلغ الخاص بدفع واحد.</span><span class="sxs-lookup"><span data-stu-id="c02c6-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="c02c6-131">في الحقل **عملة الرسوم**، حدد كود العملة للرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="c02c6-132">حدد علامة التبويب **عام** لعرض تفاصيل حساب البنك المحدد أو تعديلها.</span><span class="sxs-lookup"><span data-stu-id="c02c6-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="c02c6-133">[![علامة التبويب عام](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="c02c6-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="c02c6-134">في الحقل **الحد الأدنى**، أدخل الحد الأدنى لمبلغ الحركة الذي يقوم بتنشيط الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="c02c6-135">في الحقل **الحد الأقصى**، أدخل الحد الأقصى لمبلغ الحركة الذي يقوم بتنشيط الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="c02c6-136">في الحقل **من تاريخ** إلى **تاريخ**، حدد نطاق تاريخ لحساب الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="c02c6-137">في الحقل **الحد الأدنى للرسوم**، حدد مبلغ الرسوم إما كنسبة مئوية من الدفع أو المبلغ الخاص بدفع واحد.</span><span class="sxs-lookup"><span data-stu-id="c02c6-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="c02c6-138">في الحقل **مجموعة ضرائب المبيعات**، حدد مجموعة ضريبة المبيعات المطلوب استخدامها لحساب ضريبة المبيعات لمبلغ الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="c02c6-139">في الحقل **مجموعة ضرائب مبيعات الصنف**، حدد مجموعة ضريبة المبيعات المطلوب استخدامها لحساب ضريبة مبيعات الصنف لمبلغ الرسوم.</span><span class="sxs-lookup"><span data-stu-id="c02c6-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="c02c6-140">حدد علامة التبويب **الفاصل الزمني**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="c02c6-141">[![علامة التبويب الفاصل الزمني](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="c02c6-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="c02c6-142">في الحقل **أيام**، أدخل عدد الأيام بين تاريخ ترحيل (تاريخ الخصم) الدفع وتاريخ استحقاق السند الإذني.</span><span class="sxs-lookup"><span data-stu-id="c02c6-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="c02c6-143">في الحقل **النسبة المئوية/المبلغ**، حدد ما إذا كانت المواصفات نسبة مئوية أو مبلغ معين.</span><span class="sxs-lookup"><span data-stu-id="c02c6-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="c02c6-144">في الحقل **مبلغ الرسوم**، أدخل مبلغ الرسوم إما كنسبة مئوية من الدفع أو المبلغ الخاص بدفع واحد.</span><span class="sxs-lookup"><span data-stu-id="c02c6-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="c02c6-145">قم بإغلاق الصفحة **إعداد رسوم الدفع**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="c02c6-146">قم بإغلاق الصفحة **رسوم الدفع**.</span><span class="sxs-lookup"><span data-stu-id="c02c6-146">Close the **Payment fee** page.</span></span>
