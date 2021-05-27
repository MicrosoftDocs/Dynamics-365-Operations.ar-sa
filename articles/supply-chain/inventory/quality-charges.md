---
title: رسوم عمليات عدم المطابقة
description: يوضح هذا الموضوع كيفيه إنشاء مصاريف الجودة التي يمكن استخدامها مع العمليات الخاصة بعدم التوافق.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022290"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="dfd61-103">رسوم عمليات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="dfd61-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfd61-104">يوضح هذا الموضوع كيفيه إنشاء مصاريف الجودة التي يمكن استخدامها مع العمليات الخاصة بعدم التوافق.</span><span class="sxs-lookup"><span data-stu-id="dfd61-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="dfd61-105">يمكنك استخدام صفحة **رسوم الجودة** لتحديد أنواع الرسوم التي يمكن إضافتها إلى عمليات عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="dfd61-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="dfd61-106">تمكنك المصاريف من تتبع التفاصيل المتعلقة بالرسوم أو الرسوم التي تدين بها إلى أحد العملاء للمنتجات غير المتوافقة، أو التي يمتلكها المورد بالنسبة للمنتجات غير المتوافقة التي تلقيتها.</span><span class="sxs-lookup"><span data-stu-id="dfd61-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="dfd61-107">ويمكن أيضا استخدام المصاريف لتتبع التكاليف المطلوبة للموردين أو الخدمات الخارجية لاجراء أحدي العمليات.</span><span class="sxs-lookup"><span data-stu-id="dfd61-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="dfd61-108">أمثله لتكاليف الجودة</span><span class="sxs-lookup"><span data-stu-id="dfd61-108">Examples of quality charges</span></span>

<span data-ttu-id="dfd61-109">أنت تعمل لشركه تصنيع.</span><span class="sxs-lookup"><span data-stu-id="dfd61-109">You work for a manufacturing company.</span></span> <span data-ttu-id="dfd61-110">لدي شركتك عقود مع العديد من الموردين.</span><span class="sxs-lookup"><span data-stu-id="dfd61-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="dfd61-111">مقاييس العقود التفصيلية هذه للشحن والاضرار وجوده المنتج للأصناف.</span><span class="sxs-lookup"><span data-stu-id="dfd61-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="dfd61-112">المثل، يكون لدي العديد من العملاء اتفاقيات مع شركتك حول المرتجعات، والاضرار، وجوده المنتج.</span><span class="sxs-lookup"><span data-stu-id="dfd61-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="dfd61-113">يتم تحديد بنيه الرسوم لكل حاله من الحالات والمحددة في العقد.</span><span class="sxs-lookup"><span data-stu-id="dfd61-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="dfd61-114">يمكنك تكوين تكاليف الجودة لتخطيط أنواع مختلفه من المصاريف، مثل *الأضرار* و *الشحنة المتأحرة* و *الجودة*.</span><span class="sxs-lookup"><span data-stu-id="dfd61-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="dfd61-115">وبعد ذلك، عند إنشاء عدم التوافق، قم باضافه عمليه واحده أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="dfd61-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="dfd61-116">بالنسبة لكل عمليه، حدد **الرسوم** لتحديد التفاصيل المتعلقة بالرسوم.</span><span class="sxs-lookup"><span data-stu-id="dfd61-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="dfd61-117">إنشاء تكلفة جودة</span><span class="sxs-lookup"><span data-stu-id="dfd61-117">Create a quality charge</span></span>

1. <span data-ttu-id="dfd61-118">انتقل إلى **إدارة المخزون \> الإعداد \> إدارة الجودة \> رسوم الجودة**.</span><span class="sxs-lookup"><span data-stu-id="dfd61-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="dfd61-119">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="dfd61-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="dfd61-120">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="dfd61-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="dfd61-121">**كود المصاريف** – ادخل معرفا فريدا أو اسما فريدا لتكلفه الجودة.</span><span class="sxs-lookup"><span data-stu-id="dfd61-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="dfd61-122">**الوصف** - أدخل وصفًا مفصلاً لتكلفة الجودة.</span><span class="sxs-lookup"><span data-stu-id="dfd61-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="dfd61-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="dfd61-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="dfd61-124">أضافه تكلفه جوده إلى عمليه عدم توافق</span><span class="sxs-lookup"><span data-stu-id="dfd61-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="dfd61-125">للحصول علي تفاصيل حول كيفيه أضافه عمليات إلى عدم التوافق وتطبيق المصاريف عليها، راجع [عمليات عدم التوافق](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="dfd61-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dfd61-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="dfd61-126">Additional resources</span></span>

- [<span data-ttu-id="dfd61-127">نظرة عامة على إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="dfd61-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="dfd61-128">تمكين إدارة عدم المطابقة والجودة</span><span class="sxs-lookup"><span data-stu-id="dfd61-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="dfd61-129">العاملون المسؤولون عن الموافقة على حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="dfd61-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="dfd61-130">مناطق العزل لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="dfd61-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="dfd61-131">أنواع التشخيص لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="dfd61-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="dfd61-132">مصاريف الجودة لحالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="dfd61-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="dfd61-133">عمليات حالات عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="dfd61-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="dfd61-134">إدارة الجودة لعمليات المستودعات</span><span class="sxs-lookup"><span data-stu-id="dfd61-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
