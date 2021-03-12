---
title: إعداد أكواد ضريبة المبيعات
description: يشرح هذا الموضوع كيفية إعداد ‏‫أكواد ضريبة المبيعات‬ في Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f6df5ed3fc49b537845e7d418d4953c0faee5f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994530"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="d347e-103">إعداد أكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="d347e-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d347e-104">يشرح هذا الموضوع كيفية إعداد ‏‫أكواد ضريبة المبيعات‬.</span><span class="sxs-lookup"><span data-stu-id="d347e-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="d347e-105">يتم إنشاء أكواد ضريبة المبيعات لكل ضريبة أو رسم غير مباشر يلزم على الكيان القانوني حسابه وتحصيله ودفعه لهيئات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d347e-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="d347e-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d347e-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d347e-107">انتقل إلى **جزء التنقل > الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > أكواد ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="d347e-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="d347e-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d347e-108">Select **New**.</span></span>
3. <span data-ttu-id="d347e-109">في الحقل **كود ضريبة المبيعات**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d347e-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="d347e-110">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d347e-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d347e-111">حدد **فترة تسوية** عن طريق فتح القائمة المنسدلة لتحديد هيئة ضريبة المبيعات حيث يجب الإبلاغ عن ضريبة المبيعات ودفعها ولتحديد الفترات الزمنية للإبلاغ والدفع.</span><span class="sxs-lookup"><span data-stu-id="d347e-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="d347e-112">حدد **مجموعة ترحيل دفتر أستاذ** لتحديد الحسابات الرئيسية لترحيل ضريبة المبيعات إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="d347e-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="d347e-113">وسّع علامة التبويب السريعة **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="d347e-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="d347e-114">تتضمن هذه حقولاً متعددة تتحكم في كيفية حساب مبالغ ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d347e-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="d347e-115">إملأ هذه الحقول حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="d347e-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="d347e-116">في **جزء الإجراءات** في أعلى الواجهة، حدد **كود ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="d347e-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="d347e-117">حدد **القيم**.</span><span class="sxs-lookup"><span data-stu-id="d347e-117">Select **Values**.</span></span>
10. <span data-ttu-id="d347e-118">أدخل قيمة كود الضريبة هذا في عمود **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="d347e-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="d347e-119">على علامة التبويب السريعة **الحساب**، في الحقل "الأصل‬"، إذا تم تحديد "المبلغ لكل وحدة‬"، فسيتم ضرب القيمة في الكمية على الحركة لحساب مبلغ ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d347e-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="d347e-120">إذا لم يكن كود الضريبة عبارة عن ضريبة تستند إلى وحدة، فستكون القيمة عبارة عن نسبة مئوية مطبقة على الأصل لكود الضريبة هذا لحساب مبلغ ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="d347e-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="d347e-121">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d347e-121">Select **Save**.</span></span>
12. <span data-ttu-id="d347e-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d347e-122">Close the page.</span></span>
13. <span data-ttu-id="d347e-123">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d347e-123">Select **Save**.</span></span>

