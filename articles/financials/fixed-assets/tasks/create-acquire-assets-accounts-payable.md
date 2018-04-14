--- 
title: "إنشاء والحصول على الأصول من الحسابات الدائنة"
description: "سينقلك دليل المهمة هذا عبر عملية إنشاء أصل ثابت والاستحواذ عليه بواسطة عملية الشراء."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ae6f2358cb8e7d1f093f9fcbf60b0957e9e6a629
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="22b77-103">إنشاء والحصول على الأصول من الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="22b77-103">Create and acquire assets from accounts payable</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22b77-104">سينقلك دليل المهمة هذا عبر عملية إنشاء أصل ثابت والاستحواذ عليه بواسطة عملية الشراء.</span><span class="sxs-lookup"><span data-stu-id="22b77-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span> <span data-ttu-id="22b77-105">إنه يستخدم دور المحاسب وموظفي الحسابات الدائنة وشركة العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="22b77-105">It uses the Accountant and Accounts payable clerks and the demo company USMF.</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="22b77-106">تعيين محددات الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="22b77-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="22b77-107">انتقل إلى الأصول الثابتة > إعداد > معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="22b77-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="22b77-108">قم بتوسيع المقطع "أوامر الشراء" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="22b77-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="22b77-109">حدد خانة الاختيار "السماح بالحصول على الأصل من الشراء‬".</span><span class="sxs-lookup"><span data-stu-id="22b77-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="22b77-110">حدد خانة الاختيار "إنشاء أصل أثناء ترحيل إيصال استلام المنتجات أو الفاتورة‬".</span><span class="sxs-lookup"><span data-stu-id="22b77-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="22b77-111">إنشاء فاتورة مورّد جديدة</span><span class="sxs-lookup"><span data-stu-id="22b77-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="22b77-112">انتقل إلى الحسابات الدائنة > مساحات العمل > إدخال فاتورة المورّدين.</span><span class="sxs-lookup"><span data-stu-id="22b77-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="22b77-113">انقر فوق "فاتورة مورّد جديدة".</span><span class="sxs-lookup"><span data-stu-id="22b77-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="22b77-114">في الحقل "حساب الفاتورة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="22b77-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="22b77-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="22b77-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="22b77-116">في الحقل "الرقم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="22b77-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="22b77-117">في الحقل "تاريخ الترحيل"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="22b77-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="22b77-118">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="22b77-118">Click Add line.</span></span>
8. <span data-ttu-id="22b77-119">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="22b77-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="22b77-120">يمكن استخدام الأصناف غير المخزنة أو فئات التدبير للاستحواذ على الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="22b77-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="22b77-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="22b77-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="22b77-122">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="22b77-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="22b77-123">سينشئ بند فاتورة واحد أصلاً ثابتًا واحدًا فقط، بغض النظر عن الكمية.</span><span class="sxs-lookup"><span data-stu-id="22b77-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="22b77-124">سيتم نقل قيمة حقل كمية الفاتورة إلى كمية الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="22b77-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="22b77-125">في حقل "سعر الوحدة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="22b77-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="22b77-126">قم بتوسيع المقطع "تفاصيل البند" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="22b77-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="22b77-127">انقر فوق علامة التبويب "الأصول الثابتة".</span><span class="sxs-lookup"><span data-stu-id="22b77-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="22b77-128">حدد خانة الاختيار "إنشاء أصل ثابت جديد‬".</span><span class="sxs-lookup"><span data-stu-id="22b77-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="22b77-129">في الحقل "مجموعة الأصول الثابتة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="22b77-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="22b77-130">في القائمة، حدد مجموعة الأصول الثابتة التي سيتم استخدامها عند إنشاء الأصل الثابت الجديد.</span><span class="sxs-lookup"><span data-stu-id="22b77-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="22b77-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="22b77-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="22b77-132">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="22b77-132">Click Post.</span></span>
    * <span data-ttu-id="22b77-133">سيتم إنشاء الأصل الثابت والاستحواذ عليه عند ترحيل الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="22b77-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  


