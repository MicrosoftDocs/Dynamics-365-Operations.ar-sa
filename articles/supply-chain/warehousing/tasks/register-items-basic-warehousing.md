---
title: تسجيل أصناف لصنف ممكَّن للتخزين الأساسي باستخدام دفتر يومية وصول الصنف
description: يوضح هذا الإجراء كيفية تسجيل الأصناف باستخدام دفتر يومية وصول الصنف عند استخدام "التخزين الأساسي" في الوحدة النمطية لإدارة المخزون.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3edf84135e675b6259972327f80c9b6a91821139
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254157"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="571c3-103">تسجيل أصناف لصنف ممكَّن للتخزين الأساسي باستخدام دفتر يومية وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="571c3-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="571c3-104">يوضح هذا الإجراء كيفية تسجيل الأصناف باستخدام دفتر يومية وصول الصنف عند استخدام "التخزين الأساسي" في الوحدة النمطية لإدارة المخزون.</span><span class="sxs-lookup"><span data-stu-id="571c3-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="571c3-105">يتم ذلك عادة عن طريق موظف الاستقبال.</span><span class="sxs-lookup"><span data-stu-id="571c3-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="571c3-106">يمكنك تشغيل هذا الإجراء في شركة بيانات العرض التوضيحي USMF مع قيم الأمثلة الموضحة.</span><span class="sxs-lookup"><span data-stu-id="571c3-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="571c3-107">إذا كنت لا تستخدم USMF، فتحتاج للحصول على أمر شراء مؤكد مع بند أمر شراء مفتوح قبل بدء هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="571c3-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="571c3-108">يجب أن يكون الصنف على البند صنفًا مخزنًا.</span><span class="sxs-lookup"><span data-stu-id="571c3-108">The item on the line must be stocked.</span></span> <span data-ttu-id="571c3-109">ويجب إقران الصنف بمجموعة أبعاد تخزين، حيث يكون الموقع والمستودع نشطين.</span><span class="sxs-lookup"><span data-stu-id="571c3-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="571c3-110">إنشاء رأس دفتر يومية وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="571c3-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="571c3-111">انتقل إلى إدارة المخزون > إدخالات دفتر اليومية > وصول الصنف > وصول الصنف.</span><span class="sxs-lookup"><span data-stu-id="571c3-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="571c3-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="571c3-112">Click New.</span></span>
3. <span data-ttu-id="571c3-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="571c3-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="571c3-114">إذا كنت تستخدم USMF، فيمكنك كتابة WHS.</span><span class="sxs-lookup"><span data-stu-id="571c3-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="571c3-115">أما إذا كنت تستخدم بيانات أخرى، فيجب أن تتوفر الخصائص التالية في دفتر اليومية الذي تختار اسمه: يجب تعيين "موقع انتقاء الشيك" إلى "لا" ويجب تعيين "إدارة العزل‬" إلى "لا".</span><span class="sxs-lookup"><span data-stu-id="571c3-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="571c3-116">في الحقل "إيصال التعبئة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="571c3-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="571c3-117">هذا هو معرف إيصال التعبئة من إيصال التعبئة الصادر عن المورّد.</span><span class="sxs-lookup"><span data-stu-id="571c3-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="571c3-118">أضف رقمًا فريدًا.</span><span class="sxs-lookup"><span data-stu-id="571c3-118">Add a unique number.</span></span>  
5. <span data-ttu-id="571c3-119">في حقل "الرقم"، حدد أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="571c3-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="571c3-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="571c3-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="571c3-121">إضافة بنود إلى دفتر يومية وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="571c3-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="571c3-122">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="571c3-122">Click Functions.</span></span>
2. <span data-ttu-id="571c3-123">انقر فوق "إنشاء بنود".</span><span class="sxs-lookup"><span data-stu-id="571c3-123">Click Create lines.</span></span>
    * <span data-ttu-id="571c3-124">يمكن إدخال البنود يدويًا في دفتر اليومية هذا أو إنشاؤها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="571c3-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="571c3-125">سوف يظهر لك هذا كيفية إنشاء البنود تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="571c3-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="571c3-126">حدد خانة الاختيار "تهيئة الكمية‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="571c3-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="571c3-127">سيؤدي ذلك إلى تهيئة الكمية الموجودة في بنود دفتر اليومية مع الكمية غير المسجلة من بند أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="571c3-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="571c3-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="571c3-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="571c3-129">ترحيل دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="571c3-129">Post the journal</span></span>
1. <span data-ttu-id="571c3-130">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="571c3-130">Click Post.</span></span>
2. <span data-ttu-id="571c3-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="571c3-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="571c3-132">إنشاء إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="571c3-132">Generate the product receipt</span></span>
1. <span data-ttu-id="571c3-133">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="571c3-133">Click Functions.</span></span>
2. <span data-ttu-id="571c3-134">انقر فوق "إيصال استلام المنتجات".</span><span class="sxs-lookup"><span data-stu-id="571c3-134">Click Product receipt.</span></span>
3. <span data-ttu-id="571c3-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="571c3-135">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]