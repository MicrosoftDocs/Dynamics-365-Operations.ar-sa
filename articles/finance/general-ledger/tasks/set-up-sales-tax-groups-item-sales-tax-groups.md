---
title: إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف
description: ينقلك تسجيل المهام هذا عبر إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.‬
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24210129f7595c6544234c20915f4003bf0e1eb8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984687"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="499b0-103">إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف</span><span class="sxs-lookup"><span data-stu-id="499b0-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="499b0-104">ينقلك تسجيل المهام هذا عبر إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.‬</span><span class="sxs-lookup"><span data-stu-id="499b0-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="499b0-105">إن مجموعات ضريبة المبيعات هي مجموعات أكواد ضريبة المبيعات المرتبطة بالعملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="499b0-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="499b0-106">وهي مرتبطة أيضًا بحسابات دفتر الأستاذ للحركات التي لم يتم ترحيلها لعميل أو مورّد بعينه.</span><span class="sxs-lookup"><span data-stu-id="499b0-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="499b0-107">أما مجموعات ضريبة مبيعات الصنف فهي مجموعات أكواد ضريبة المبيعات المرتبطة بموارد كالمنتجات مثلاً.</span><span class="sxs-lookup"><span data-stu-id="499b0-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="499b0-108">يتم تحديد ضرائب المبيعات التي تطبق على حركة معينة عن طريق أكواد ضريبة المبيعات المضمنة في كل من مجموعة ضريبة المبيعات وفي مجموعة ضريبة مبيعات الصنف للحركة.</span><span class="sxs-lookup"><span data-stu-id="499b0-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="499b0-109">يمكن حساب ضريبة المبيعات فقط في حال تحديد مجموعة ضريبة مبيعات ومجموعة ضريبة مبيعات الصنف لكل حركة يجب أن يتم حساب أو تسجيل ضريبة المبيعات لها.</span><span class="sxs-lookup"><span data-stu-id="499b0-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="499b0-110">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > ضرائب غير مباشرة > ضريبة المبيعات > مجموعات ضريبة المبيعات** .</span><span class="sxs-lookup"><span data-stu-id="499b0-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups** .</span></span>
2. <span data-ttu-id="499b0-111">انقر فوق **جديد** .</span><span class="sxs-lookup"><span data-stu-id="499b0-111">Click **New** .</span></span>
3. <span data-ttu-id="499b0-112">في الحقل **مجموعة ضريبة المبيعات** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="499b0-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="499b0-113">في حقل **الوصف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="499b0-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="499b0-114">بدّل توسيع قسم **الإعداد** .</span><span class="sxs-lookup"><span data-stu-id="499b0-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="499b0-115">انقر فوق **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="499b0-115">Click **Add** .</span></span>
7. <span data-ttu-id="499b0-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="499b0-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="499b0-117">في الحقل **كود ضريبة المبيعات** ، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="499b0-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="499b0-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="499b0-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="499b0-119">انقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="499b0-119">Click **Save** .</span></span>
11. <span data-ttu-id="499b0-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="499b0-120">Close the page.</span></span>
12. <span data-ttu-id="499b0-121">انتقل إلى **الضريبة‬ > ضرائب غير مباشرة‬ > ضريبة المبيعات > مجموعات ضرائب مبيعات الأصناف** .</span><span class="sxs-lookup"><span data-stu-id="499b0-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups** .</span></span>
13. <span data-ttu-id="499b0-122">انقر فوق **جديد** .</span><span class="sxs-lookup"><span data-stu-id="499b0-122">Click **New** .</span></span>
14. <span data-ttu-id="499b0-123">في الحقل **مجموعة ضرائب المبيعات للأصناف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="499b0-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="499b0-124">في حقل **الوصف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="499b0-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="499b0-125">انقر فوق **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="499b0-125">Click **Add** .</span></span>
17. <span data-ttu-id="499b0-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="499b0-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="499b0-127">في الحقل **كود ضريبة المبيعات** ، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="499b0-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="499b0-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="499b0-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="499b0-129">انقر فوق **حفظ** .</span><span class="sxs-lookup"><span data-stu-id="499b0-129">Click **Save** .</span></span>

