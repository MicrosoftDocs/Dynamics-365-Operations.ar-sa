---
title: إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف
description: ينقلك تسجيل المهام هذا عبر إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.‬
author: twheeloc
manager: AnnBe
ms.date: 07-01-2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b539129e62b9b0b10df1f505cbfec5c1143138
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141616"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="8bbca-103">إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف</span><span class="sxs-lookup"><span data-stu-id="8bbca-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8bbca-104">ينقلك تسجيل المهام هذا عبر إعداد مجموعات ضريبة المبيعات ومجموعات ضريبة مبيعات الصنف.‬</span><span class="sxs-lookup"><span data-stu-id="8bbca-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="8bbca-105">إن مجموعات ضريبة المبيعات هي مجموعات أكواد ضريبة المبيعات المرتبطة بالعملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="8bbca-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="8bbca-106">وهي مرتبطة أيضًا بحسابات دفتر الأستاذ للحركات التي لم يتم ترحيلها لعميل أو مورّد بعينه.</span><span class="sxs-lookup"><span data-stu-id="8bbca-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="8bbca-107">أما مجموعات ضريبة مبيعات الصنف فهي مجموعات أكواد ضريبة المبيعات المرتبطة بموارد كالمنتجات مثلاً.</span><span class="sxs-lookup"><span data-stu-id="8bbca-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="8bbca-108">يتم تحديد ضرائب المبيعات التي تطبق على حركة معينة عن طريق أكواد ضريبة المبيعات المضمنة في كل من مجموعة ضريبة المبيعات وفي مجموعة ضريبة مبيعات الصنف للحركة.</span><span class="sxs-lookup"><span data-stu-id="8bbca-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="8bbca-109">يمكن حساب ضريبة المبيعات فقط في حال تحديد مجموعة ضريبة مبيعات ومجموعة ضريبة مبيعات الصنف لكل حركة يجب أن يتم حساب أو تسجيل ضريبة المبيعات لها.</span><span class="sxs-lookup"><span data-stu-id="8bbca-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="8bbca-110">انتقل إلى **جزء التنقل > الوحدات النمطية > الضريبة > ضرائب غير مباشرة > ضريبة المبيعات > مجموعات ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="8bbca-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-111">Click **New**.</span></span>
3. <span data-ttu-id="8bbca-112">في الحقل **مجموعة ضريبة المبيعات**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8bbca-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="8bbca-113">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8bbca-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8bbca-114">بدّل توسيع قسم **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="8bbca-115">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-115">Click **Add**.</span></span>
7. <span data-ttu-id="8bbca-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bbca-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8bbca-117">في الحقل **كود ضريبة المبيعات**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8bbca-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8bbca-118">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bbca-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8bbca-119">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-119">Click **Save**.</span></span>
11. <span data-ttu-id="8bbca-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8bbca-120">Close the page.</span></span>
12. <span data-ttu-id="8bbca-121">انتقل إلى **الضريبة‬ > ضرائب غير مباشرة‬ > ضريبة المبيعات > مجموعات ضرائب مبيعات الأصناف**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="8bbca-122">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-122">Click **New**.</span></span>
14. <span data-ttu-id="8bbca-123">في الحقل **مجموعة ضرائب المبيعات للأصناف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8bbca-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="8bbca-124">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8bbca-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="8bbca-125">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-125">Click **Add**.</span></span>
17. <span data-ttu-id="8bbca-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bbca-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="8bbca-127">في الحقل **كود ضريبة المبيعات**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8bbca-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="8bbca-128">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8bbca-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="8bbca-129">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8bbca-129">Click **Save**.</span></span>

