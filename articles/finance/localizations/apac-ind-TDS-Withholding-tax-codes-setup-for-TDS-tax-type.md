---
title: إعداد أكواد ضريبة الخصم لنوع ضريبة TDS
description: يوضح هذا الموضوع كيفية إعداد أكواد الضريبة المخصومة في المصدر (TDS).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023010"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="c0ef8-103">إعداد أكواد ضريبة الخصم لنوع ضريبة TDS</span><span class="sxs-lookup"><span data-stu-id="c0ef8-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0ef8-104">يوضح هذا الموضوع كيفية إعداد أكواد الضريبة المخصومة في المصدر (TDS).</span><span class="sxs-lookup"><span data-stu-id="c0ef8-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="c0ef8-105">انتقل إلى **الضريبة \> الضرائب غير مباشرة \> ضريبة الخصم \> أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="c0ef8-106">[![صفحة أكواد ضريبة الخصم](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="c0ef8-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="c0ef8-107">في جزء الإجراء، حدد **جديد** لإنشاء كود ضريبة خصم لـ TDS، وأدخل التفاصيل المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="c0ef8-108">في علامة التبويب السريعة **عام**، في الحقل **نوع الضريبة**، حدد **TDS** لتصنيف كود الضريبة ككود ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="c0ef8-109">في الحقل **فترة التسوية**، حدد فترة تسوية TDS لكود ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="c0ef8-110">في الحقل **الحساب الرئيسي**، حدد حساب دفتر الأستاذ الذي يجب ترحيل مبلغ TDS إليه.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="c0ef8-111">في الحقل **الحساب المدين**، حدد الحساب المدينة الذي يجب ترحيل مبلغ TDS الذي تم خصمه من حركات المبيعات إليه.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="c0ef8-112">يتم تعيين الحقل **الأصل** تلقائيًا على **النسبة المئوية للمبلغ الإجمالي**، ولا يمكن تغيير القيمة.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0ef8-113">لا يمكنك تعيين الأصل إلى **النسبة المئوية للمبلغ الصافي** لأكواد الضريبة الخاصة بنوع ضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="c0ef8-114">في الحقل **مكون ضريبة الخصم**، حدد مجموعة مكون ضريبة TDS لكود صريبة TDS إليها.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="c0ef8-115">في جزء الإجراء، حدد **القيم** لفتح الصفحة **قيم ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="c0ef8-116">حدد الحقل **من تاريخ**، أدخل تاريخ البداية لقيمة TDS.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="c0ef8-117">في الحقل **إلى التاريخ**، أدخل تاريخ الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0ef8-118">لا تتوفر الحقول **الحد الأدنى** و **الحد الأعلى** و **استبعاد %** لأكواد الضريبة الخاصة بنوع الضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="c0ef8-119">في الحقل **القيمة**، أدخل النسبة لـ TDS لاحتساب ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="c0ef8-120">قم بإغلاق الصفحة **قيم ضريبة الخصم** للرجوع إلى الصفحة **أكواد ضريبة الخصم**.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0ef8-121">لا يتوافر الزر **الحدود** الموجود على الصفحة **أكواد ضريبة الخصم** لأكواد الضريبة الخاصة بنوع الضريبة TDS.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="c0ef8-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0ef8-122">Close the page.</span></span>
