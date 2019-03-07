---
title: إنشاء قواعد التكوين
description: ويعمل هذا الإجراء على إنشاء قواعد التكوين التي يمكن استخدامها للتكوين المستند إلى بعد لفرض مجموعات معينة في بنود قائمة مكونات الصنف أو منعها.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a315ddecd2e10f508b86ac8ea18a36df71616963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "314729"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="99129-103">إنشاء قواعد التكوين</span><span class="sxs-lookup"><span data-stu-id="99129-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99129-104">ويعمل هذا الإجراء على إنشاء قواعد التكوين التي يمكن استخدامها للتكوين المستند إلى بعد لفرض مجموعات معينة في بنود قائمة مكونات الصنف أو منعها.</span><span class="sxs-lookup"><span data-stu-id="99129-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="99129-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="99129-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="99129-106">وهذا هو الإجراء السابع من أصل ثمانية إجراءات الذي يوضح كيفية إنشاء مجموعات لتكوين مستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="99129-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="99129-107">انتقل إلى إدارة معلومات المنتج > قائمة مكونات الصنف والصيغ > قوائم مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="99129-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="99129-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="99129-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="99129-109">ابحث عن قائمة مكونات الصنف للتكوين المستند إلى بُعد وحددها.</span><span class="sxs-lookup"><span data-stu-id="99129-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="99129-110">في جزء الإجراءات، انقر فوق "خيارات".</span><span class="sxs-lookup"><span data-stu-id="99129-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="99129-111">انقر فوق "تغيير طريقة العرض‬".</span><span class="sxs-lookup"><span data-stu-id="99129-111">Click Change view.</span></span>
5. <span data-ttu-id="99129-112">انقر فوق "عرض الرأس".</span><span class="sxs-lookup"><span data-stu-id="99129-112">Click Header view.</span></span>
    * <span data-ttu-id="99129-113">افتح عرض الرأس الوصول إلى علامة التبويب السريعة "مسار التكوين".</span><span class="sxs-lookup"><span data-stu-id="99129-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="99129-114">قم بتوسيع أو طي قسم مسار التكوين.</span><span class="sxs-lookup"><span data-stu-id="99129-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="99129-115">يجب أن تكون علامة التبويب السريعة "مسار التكوين" في وضع العرض الموسع.</span><span class="sxs-lookup"><span data-stu-id="99129-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="99129-116">انقر فوق "قواعد التكوين".</span><span class="sxs-lookup"><span data-stu-id="99129-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="99129-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="99129-117">Click New.</span></span>
9. <span data-ttu-id="99129-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="99129-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="99129-119">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="99129-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="99129-120">يتم عرض العناصر المضمنة في مجموعة التكوين الحالية.</span><span class="sxs-lookup"><span data-stu-id="99129-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="99129-121">حدد العنصر الذي يمثل الشرط في القاعدة.</span><span class="sxs-lookup"><span data-stu-id="99129-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="99129-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="99129-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="99129-123">في الحقل "الأسلوب‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="99129-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="99129-124">من الممكن فرض إما تحديد عنصر أو إلغاء تحديده من مجموعة تكوين أخرى.</span><span class="sxs-lookup"><span data-stu-id="99129-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="99129-125">في الحقل "المجموعة المشتقة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="99129-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="99129-126">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="99129-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="99129-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="99129-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="99129-128">حدد مجموعة التكوين المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="99129-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="99129-129">في الحقل "رقم الصنف المشتق"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="99129-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="99129-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="99129-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="99129-131">حدد رقم الصنف المطلوب الذي سيتم إما تحديده أو إلغاء تحديده بناءً على الأسلوب الذي يتم اختياره.</span><span class="sxs-lookup"><span data-stu-id="99129-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="99129-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="99129-132">Close the page.</span></span>

