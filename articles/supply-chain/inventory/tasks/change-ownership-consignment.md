---
title: تغيير ملكية مخزون الشحن استنادًا إلى الطلب على الإنتاج
description: يوضح هذا الإجراء كيفية تغيير مالك مخزون الشحن من المورّد إلى الكيان القانوني عند وجود طلب على المخزون في الإنتاج.
author: perlynne
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6385fba0b6288416a85f1b7de73d3bb4972a852a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834111"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="f1e67-103">تغيير ملكية مخزون الشحن استنادًا إلى الطلب على الإنتاج</span><span class="sxs-lookup"><span data-stu-id="f1e67-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1e67-104">يوضح هذا الإجراء كيفية تغيير مالك مخزون الشحن من المورّد إلى الكيان القانوني عند وجود طلب على المخزون في الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f1e67-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="f1e67-105">يتم تنفيذ تغيير الملكية هذا بإنشاء وترحيل دفتر يومية تغيير ملكية مخزون.</span><span class="sxs-lookup"><span data-stu-id="f1e67-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="f1e67-106">يمكن إنشاء بنود دفتر يومية تغيير الملكية يدويًا أو، كما هو موضح في هذا التسجيل، استنادًا إلى الطلب على الإنتاج الموجود.</span><span class="sxs-lookup"><span data-stu-id="f1e67-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="f1e67-107">يقوم عادةً المشرف على صالة الإنتاج‬ بتنفيذ هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="f1e67-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="f1e67-108">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو في البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f1e67-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="f1e67-109">إذا كنت تستخدم بياناتك الخاصة، فتأكد من وجود المتطلبات الأساسية التالية: اسم دفتر يومية مخزون تم إعداده لتغيير ملكية المخزون، أصناف متاحة فعليًا مملوكة من المورّد ومسجلة فعليًا، وبند أو أكثر من بنود أوامر الإنتاج خاصة بالمواد.</span><span class="sxs-lookup"><span data-stu-id="f1e67-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="f1e67-110">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="f1e67-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="f1e67-111">عمليات الشحن الصادرة غير معتمدة على الفور ولا يتم دعم المعالجة التلقائية لدفتر يومية الملكية.</span><span class="sxs-lookup"><span data-stu-id="f1e67-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="f1e67-112">إنشاء دفتر يومية ملكية المخزون</span><span class="sxs-lookup"><span data-stu-id="f1e67-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="f1e67-113">انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > الأصناف > تغيير ملكية المخزون.</span><span class="sxs-lookup"><span data-stu-id="f1e67-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="f1e67-114">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f1e67-114">Click New.</span></span>
    * <span data-ttu-id="f1e67-115">يستخدم دفتر يومية تغيير ملكية المخزون لتغيير مالك مخزون الشحن من المورّد إلى الكيان القانوني الحالي.</span><span class="sxs-lookup"><span data-stu-id="f1e67-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="f1e67-116">ويتم تنفيذ تغيير الملكية هذا عن طريق تحرير المخزون الفعلي الذي يملكه المورّد، ثم استلام هذا المخزون في الكيان القانوني الحالي.</span><span class="sxs-lookup"><span data-stu-id="f1e67-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="f1e67-117">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="f1e67-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="f1e67-118">يمكنك تحديد فقط أسماء دفاتر يومية المخزون التي لديها نوع دفتر يومية "تغيير الملكية‬".</span><span class="sxs-lookup"><span data-stu-id="f1e67-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="f1e67-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f1e67-119">Click OK.</span></span>
5. <span data-ttu-id="f1e67-120">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="f1e67-120">Click Functions.</span></span>
6. <span data-ttu-id="f1e67-121">انقر فوق "إنشاء بنود دفتر اليومية من أوامر الإنتاج".</span><span class="sxs-lookup"><span data-stu-id="f1e67-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="f1e67-122">يمكنك بدء عملية تغيير الملكية عن طريق الاستعلام عن كافة خطوط الإنتاج التي لديها طلب على استهلاك المواد الخام.</span><span class="sxs-lookup"><span data-stu-id="f1e67-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="f1e67-123">في حقل "حالات إصدار المخزون المُراد تضمينها‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="f1e67-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="f1e67-124">يسمح لك هذا الخيار بإجراء التصفية حسب حالة المشكلة لحركات المخزون.</span><span class="sxs-lookup"><span data-stu-id="f1e67-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="f1e67-125">على سبيل المثال، يمكنك إنشاء بنود دفتر اليومية للمخزون بحالات الكمية المنتقاة والكمية المحجوزة.</span><span class="sxs-lookup"><span data-stu-id="f1e67-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="f1e67-126">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="f1e67-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="f1e67-127">يتيح هذا المقطع تطبيق تصفية إضافية.</span><span class="sxs-lookup"><span data-stu-id="f1e67-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="f1e67-128">على سبيل المثال، يمكنك تحديد تاريخ معين للمواد الخام.</span><span class="sxs-lookup"><span data-stu-id="f1e67-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="f1e67-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f1e67-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="f1e67-130">ترحيل دفتر يومية تغيير ملكية المخزون</span><span class="sxs-lookup"><span data-stu-id="f1e67-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="f1e67-131">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="f1e67-131">Click Post.</span></span>
    * <span data-ttu-id="f1e67-132">عند ترحيل دفتر اليومية، يتم إصدار المخزون المملوك من المورّد باستخدام مرجع "تغيير الملكية".</span><span class="sxs-lookup"><span data-stu-id="f1e67-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="f1e67-133">يتم عندئذٍ استلام المخزون كمخزون فعلي باستخدام حركة مخزون يتم تحديثها بواسطة إيصال استلام منتجات أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f1e67-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="f1e67-134">لاحظ أنه يتم إنشاء فقط الحركات المرتبطة بدفتر اليومية المرحّل.</span><span class="sxs-lookup"><span data-stu-id="f1e67-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="f1e67-135">ولا يتم إنشاء حركات مخزون متوقعة.</span><span class="sxs-lookup"><span data-stu-id="f1e67-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="f1e67-136">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="f1e67-136">Click OK.</span></span>
3. <span data-ttu-id="f1e67-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f1e67-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]