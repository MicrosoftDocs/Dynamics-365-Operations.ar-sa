---
title: إعداد أكواد ضريبة المبيعات
description: يتم إنشاء أكواد ضريبة المبيعات لكل ضريبة أو رسم غير مباشر يلزم على الكيان القانوني حسابه وتحصيله ودفعه لهيئات ضريبة المبيعات.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "349160"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="bd63f-103">إعداد أكواد ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="bd63f-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd63f-104">يتم إنشاء أكواد ضريبة المبيعات لكل ضريبة أو رسم غير مباشر يلزم على الكيان القانوني حسابه وتحصيله ودفعه لهيئات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd63f-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="bd63f-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="bd63f-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="bd63f-106">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > أكواد ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd63f-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="bd63f-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bd63f-107">Click New.</span></span>
3. <span data-ttu-id="bd63f-108">في الحقل "كود ضريبة المبيعات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bd63f-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="bd63f-109">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="bd63f-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bd63f-110">حدد فترة تسوية لتحديد هيئة ضريبة المبيعات حيث يجب الإبلاغ عن ضريبة المبيعات ودفعها ولتحديد الفترات الزمنية للإبلاغ والدفع.</span><span class="sxs-lookup"><span data-stu-id="bd63f-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="bd63f-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bd63f-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bd63f-112">حدد مجموعة ترحيل دفتر أستاذ لتحديد الحسابات الرئيسية لترحيل ضريبة المبيعات إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="bd63f-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="bd63f-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="bd63f-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="bd63f-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bd63f-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bd63f-115">وسّع علامة التبويب السريعة "الحساب".</span><span class="sxs-lookup"><span data-stu-id="bd63f-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="bd63f-116">تتضمن علامة التبويب السريعة "الحساب‬" حقولاً متعددة تتحكم في كيفية حساب مبالغ ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd63f-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="bd63f-117">في جزء الإجراءات، انقر فوق "كود ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="bd63f-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="bd63f-118">انقر فوق "القيم‬".</span><span class="sxs-lookup"><span data-stu-id="bd63f-118">Click Values.</span></span>
13. <span data-ttu-id="bd63f-119">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="bd63f-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="bd63f-120">أدخل قيمة كود الضريبة هذا.</span><span class="sxs-lookup"><span data-stu-id="bd63f-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="bd63f-121">على علامة التبويب السريعة "الحساب"، في الحقل "الأصل‬"، إذا تم تحديد "المبلغ لكل وحدة‬"، فسيتم ضرب القيمة في الكمية على الحركة لحساب مبلغ ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd63f-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="bd63f-122">إذا لم يكن كود الضريبة عبارة عن ضريبة تستند إلى وحدة، فستكون القيمة عبارة عن نسبة مئوية مطبقة على الأصل لكود الضريبة هذا لحساب مبلغ ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="bd63f-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="bd63f-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bd63f-123">Click Save.</span></span>
16. <span data-ttu-id="bd63f-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bd63f-124">Close the page.</span></span>
17. <span data-ttu-id="bd63f-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bd63f-125">Click Save.</span></span>

