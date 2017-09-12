--- 
title: "إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف"
description: "ينقلك تسجيل المهام هذا عبر إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.‬"
author: twheeloc
manager: AnnBe
ms.date: 11/10/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4d7f1093edcfff65fd466fa8138b1bb5203648b3
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="b9ca4-103">إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف</span><span class="sxs-lookup"><span data-stu-id="b9ca4-103">Set up sales tax groups and item sales tax groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9ca4-104">ينقلك تسجيل المهام هذا عبر إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.‬</span><span class="sxs-lookup"><span data-stu-id="b9ca4-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="b9ca4-105">إن مجموعات ضريبة المبيعات هي مجموعات أكواد ضريبة المبيعات المرتبطة بالعملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="b9ca4-106">وهي مرتبطة أيضًا بحسابات دفتر الأستاذ للحركات التي لم يتم ترحيلها لعميل أو مورّد بعينه.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="b9ca4-107">أما مجموعات ضريبة مبيعات الصنف فهي مجموعات أكواد ضريبة المبيعات المرتبطة بموارد كالمنتجات مثلاً.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="b9ca4-108">يتم تحديد ضرائب المبيعات التي تطبق على حركة معينة عن طريق أكواد ضريبة المبيعات المضمنة في كل من مجموعة ضريبة المبيعات وفي مجموعة ضريبة مبيعات الصنف للحركة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="b9ca4-109">يمكن حساب ضريبة المبيعات فقط في حال تحديد مجموعة ضريبة مبيعات ومجموعة ضريبة مبيعات الصنف لكل حركة يجب أن يتم حساب أو تسجيل ضريبة المبيعات لها.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="b9ca4-110">انتقل إلى الضريبة‬ > ضرائب غير مباشرة‬ > ضريبة المبيعات > مجموعات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="b9ca4-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b9ca4-111">Click New.</span></span>
3. <span data-ttu-id="b9ca4-112">في الحقل "مجموعة ضريبة المبيعات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="b9ca4-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b9ca4-114">بدّل توسيع المقطع "إعداد".</span><span class="sxs-lookup"><span data-stu-id="b9ca4-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="b9ca4-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-115">Click Add.</span></span>
7. <span data-ttu-id="b9ca4-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b9ca4-117">في الحقل "كود ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b9ca4-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b9ca4-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b9ca4-119">Click Save.</span></span>
11. <span data-ttu-id="b9ca4-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-120">Close the page.</span></span>
12. <span data-ttu-id="b9ca4-121">انتقل إلى الضريبة‬ > ضرائب غير مباشرة‬ > ضريبة المبيعات > مجموعات ضرائب مبيعات الأصناف.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="b9ca4-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="b9ca4-122">Click New.</span></span>
14. <span data-ttu-id="b9ca4-123">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="b9ca4-124">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="b9ca4-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-125">Click Add.</span></span>
17. <span data-ttu-id="b9ca4-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="b9ca4-127">في الحقل "كود ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b9ca4-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b9ca4-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="b9ca4-129">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="b9ca4-129">Click Save.</span></span>


