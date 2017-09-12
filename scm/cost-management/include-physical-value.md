---
title: "تضمين القيمة الفعلية"
description: "يتم استخدام خانة الاختيار \"تضمين القيمة الفعلية‬\" على علامة التبويب السريعة \"نموذج المخزون\" في صفحة مجموعات نماذج الصنف‬ لتحديد ما إذا كانت الحركات المحدّثة فعليًا مأخوذة في الاعتبار عند حساب متوسط سعر التكلفة الحالي للصنف."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fa59031ed2144c2e92399933cd5dd40bfca0f2ae
ms.contentlocale: ar-sa
ms.lasthandoff: 07/18/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="b1832-103">تضمين القيمة الفعلية</span><span class="sxs-lookup"><span data-stu-id="b1832-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b1832-104">يتم استخدام خانة الاختيار "تضمين القيمة الفعلية‬" على علامة التبويب السريعة "نموذج المخزون" في صفحة مجموعات نماذج الصنف‬ لتحديد ما إذا كانت الحركات المحدّثة فعليًا مأخوذة في الاعتبار عند حساب متوسط سعر التكلفة الحالي للصنف.</span><span class="sxs-lookup"><span data-stu-id="b1832-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="b1832-105">تتضمن خانة الاختيار **تضمين القيمة الفعلية‬** القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b1832-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="b1832-106">القيمة</span><span class="sxs-lookup"><span data-stu-id="b1832-106">Value</span></span>    | <span data-ttu-id="b1832-107">النتيجة</span><span class="sxs-lookup"><span data-stu-id="b1832-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1832-108">المحدد</span><span class="sxs-lookup"><span data-stu-id="b1832-108">Selected</span></span> | <span data-ttu-id="b1832-109">يتم استخدام الحركات المحدّثة فعليًا والحركات المحدّثة ماليًا لحساب متوسط سعر التكلفة الحالي.</span><span class="sxs-lookup"><span data-stu-id="b1832-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="b1832-110">تمت تسويته</span><span class="sxs-lookup"><span data-stu-id="b1832-110">Cleared</span></span>  | <span data-ttu-id="b1832-111">يتم استخدام الحركات المحدّثة ماليًا فقط لحساب متوسط سعر التكلفة الحالي.</span><span class="sxs-lookup"><span data-stu-id="b1832-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="b1832-112">تكون خانة الاختيار ذات تأثيرات مختلفة قليلاً، وهذا يتوقف على نموذج المخزون الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="b1832-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="b1832-113">إذا حددت خانة الاختيار **تضمين القيمة الفعلية** عند استخدام نموذج مخزون بنمط ما يرد أولاً يصرف أولاً (FIFO)‬ أو ما يرد أخيرًا يصرف أولاً (LIFO)‬ أو تاريخ ما يرد أخيرًا يصرف أولاً (LIFO)، فإن إغلاق المخزون يقوم أيضًا بتعديلات على الحركات المحدّثة فعليًا.</span><span class="sxs-lookup"><span data-stu-id="b1832-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="b1832-114">إذا لم تحدد خانة الاختيار **تضمين القيمة الفعلية** عند استخدام نماذج المخزون هذه، فإن إقفال المخزون يقوم بإجراء التسويات فقط على الحركات المحدّثة ماليًا.</span><span class="sxs-lookup"><span data-stu-id="b1832-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="b1832-115">عند استخدام نموذج مخزون المتوسط المرجح أو تاريخ المتوسط المرجح، سيقوم إغلاق المخزون بتسوية الحركات المحدّثة ماليًا فقط، بصرف النظر عما إذا تم تحديد خانة الاختيار **تضمين القيمة الفعلية** أم لا.</span><span class="sxs-lookup"><span data-stu-id="b1832-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="b1832-116">**مثال 1** لقد حددت خانة الاختيار**تضمين القيمة الفعلية** وتلقيت أوامر الشراء التالية:</span><span class="sxs-lookup"><span data-stu-id="b1832-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="b1832-117">أمر شراء لكمية قيمتها 2 بسعر تكلفة يبلغ 10.00 دولارات أمريكية تم تحديث إيصال تعبئته.</span><span class="sxs-lookup"><span data-stu-id="b1832-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="b1832-118">أمر شراء لكمية قيمتها 3 بسعر تكلفة يبلغ 12.00 دولارات أمريكية تم تحديث فاتورته.</span><span class="sxs-lookup"><span data-stu-id="b1832-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="b1832-119">في هذه الحالة، سيكون متوسط سعر التكلفة الحالي 11.20 دولار أمريكي نظرًا لاستخدام الحركات المحدّثة فعليًا والحركات المحدّثة ماليًا لحساب سعر التكلفة.</span><span class="sxs-lookup"><span data-stu-id="b1832-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="b1832-120">**مثال 2** لم تحدد خانة الاختيار **تضمين القيمة الفعلية**، وسعر التكلفة في إعداد الصنف هو 10.00 دولار أمريكي.</span><span class="sxs-lookup"><span data-stu-id="b1832-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="b1832-121">تلقيت أمر شراء لكمية قيمتها 20 بسعر تكلفة يبلغ 12.00 دولارات أمريكية تم تحديث إيصال تعبئته.</span><span class="sxs-lookup"><span data-stu-id="b1832-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="b1832-122">عند ترحيل أمر مبيعات، تكون قيمة التكلفة المرحّلة 10.00 دولار أمريكي لأن متوسط سعر التكلفة الحالي لن يتضمن الحركات التي تم ترحيلها فعليًا.</span><span class="sxs-lookup"><span data-stu-id="b1832-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="b1832-123">**ملاحظة:** للمقارنة، إذا حددت خانة الاختيار **تضمين القيمة الفعلية** لهذا الصنف، فستبلغ قيمة التكلفة المرحّلة 12.00 دولارًا عند ترحيل أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="b1832-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




