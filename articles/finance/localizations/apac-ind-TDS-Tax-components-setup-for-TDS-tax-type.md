---
title: إعداد مكونات الضريبة لنوع ضريبة TDS
description: يوضح هذا الموضوع كيفية إعداد مكونات ضريبة الخصم لنوع الضريبة المخصومة في المصدر (TDS). ويوضح أيضًا كيفية تحديد الحد المستخدم لحساب TDS لكل مكون TDS.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022993"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="97ccf-104">إعداد مكونات الضريبة لنوع ضريبة TDS</span><span class="sxs-lookup"><span data-stu-id="97ccf-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97ccf-105">يوضح هذا الموضوع كيفية إعداد مكونات ضريبة الخصم لنوع الضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="97ccf-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="97ccf-106">تعد مكونات TDS هي TDS والرسوم الإضافية وPE-Cess وSHE Cess.</span><span class="sxs-lookup"><span data-stu-id="97ccf-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="97ccf-107">ويوضح هذا الموضوع أيضًا كيفية تحديد الحد المستخدم لحساب TDS لكل مكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="97ccf-108">بالإضافة إلى ذلك، يمكنك تعريف الحد الاستثنائي الذي يتم استخدامه لحساب TDS لكل مكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="97ccf-109">لإعداد ممكونات TDS‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="97ccf-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="97ccf-110">انتقل إلى **الضريبة \> الإعدادات \> ضريبة الخصم \> مكونات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="97ccf-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="97ccf-111">[![صفحة مكونات ضرائب الخصم](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="97ccf-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="97ccf-112">في الحقل **نوع الضريبة**، حدد **TDS** لإعداد مكونات ضريبة الخصم لنوع الضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="97ccf-113">في جزء الإجراءات، حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="97ccf-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="97ccf-114">في الحقل **مكون ضريبة الخصم**، أدخل اسمًا لمكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="97ccf-115">في الحقل **مجموعة مكون ضريبة الخصم**، حدد مجموعة مكونات ضريبة الخصم TDS لإرفاق المكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="97ccf-116">في علامة التبويب السريعة **عام** في الحقل **الوصف**، أدخل وصفًا لمكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="97ccf-117">في جزء الإجراء، حدد **الحد** لفتح الصفحة **الحد**، بحيث يمكنك تحديد الحد المستخدم لحساب TDS لمكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="97ccf-118">استخدم الحقلين **من تاريخ** و **إلى تاريخ** لتحديد الفترة التي يسري عليها الحد.</span><span class="sxs-lookup"><span data-stu-id="97ccf-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="97ccf-119">في علامة التبويب السريعة **عام**، في الحقل **الحد**، أدخل مبلغ الحد المستخدم لحساب TDS لمكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="97ccf-120">سيتم خصم الضريبة في المصدر فقط عندما يزيد مبلغ الفاتورة التراكمي عن الحد.</span><span class="sxs-lookup"><span data-stu-id="97ccf-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="97ccf-121">على سبيل المثال، إذا كان مبلغ الحد 10.000، سيتم حساب TDS بعد أن يتجاوز مبلغ الفاتورة التراكمي 10.000 (بمعنى آخر، عندما يكون المبلغ 10.001ا أو أكثر).</span><span class="sxs-lookup"><span data-stu-id="97ccf-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="97ccf-122">في الحقل **الحد الاستثنائي**، أدخل مبلغ الحد الاستثنائي الذي يتم استخدامه لحساب TDS لمكون TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="97ccf-123">سيتم خصم الضريبة في المصدر ببند الفاتورة فقط عندما يزيد مبلغ الفاتورة التراكمي عن الحد الاستثنائي.</span><span class="sxs-lookup"><span data-stu-id="97ccf-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="97ccf-124">على سبيل المثال، إذا كان مبلغ الحد الاستثنائي 5.000، فإنه يتم حساب TDS في بند فاتورة محدد إذا كان مبلغ بند الفاتورة يتجاوز 5.000 (بمعنى آخر، إذا كان المبلغ 5.001ا أو أكثر).</span><span class="sxs-lookup"><span data-stu-id="97ccf-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="97ccf-125">[![صفحة الحد](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="97ccf-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="97ccf-126">يجب أن يكون مبلغ الحد الاستثنائي أقل من أو مساويًا لمبلغ الحد.</span><span class="sxs-lookup"><span data-stu-id="97ccf-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="97ccf-127">يتم خصم الضريبة للحركة إذا كان مبلغ الحركة يتجاوز الحد الاستثنائي، حتى وإن لم يكن مبلغ الفاتورة التراكمي متجاوزًا للحد الذي يتم تحديده في الحقل **الحد**.</span><span class="sxs-lookup"><span data-stu-id="97ccf-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="97ccf-128">قم بإغلاق الصفحة **الحد** للرجوع إلى الصفحة **مكونات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="97ccf-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="97ccf-129">في جزء الإجراء، حدد **نسخ** لفتح مربع الحوار **نسخ مكونات ضريبة الخصم**، حتى يمكنك نسخ مكونات TDS التي تم إعدادها لمجموعة مكون TDS واحدة لمجموعة مكون TDS أخرى.</span><span class="sxs-lookup"><span data-stu-id="97ccf-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="97ccf-130">في الحقل **من**، حدد مجموعة مكون TDS لنسخ مكونات TDS منها.</span><span class="sxs-lookup"><span data-stu-id="97ccf-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="97ccf-131">في الحقل **إلى**، حدد مجموعة مكون ضريبة الخصم لنسخ مكونات TDS إليها.</span><span class="sxs-lookup"><span data-stu-id="97ccf-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97ccf-132">ولا يتم نسخ مكونات TDS الشائعة المرفقة بكل من مجموعتي مكونات TDS.</span><span class="sxs-lookup"><span data-stu-id="97ccf-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="97ccf-133">حدد **موافق** لنسخ مكونات TDS لمجموعة مكون TDS الأخرى وإنشائها في الصفحة **مكونات ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="97ccf-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="97ccf-134">[![مربع حوار نسخ مكونات ضريبة الخصم](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="97ccf-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="97ccf-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="97ccf-135">Close the page.</span></span>
