---
title: إنشاء معايير تحديد سعر المبيعات
description: يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed8c60b188b7c7090546e8367455e0f58ce9359b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147674"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="3e713-103">إنشاء معايير تحديد سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="3e713-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e713-104">يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="3e713-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="3e713-105">يتطلب هذا الإجراء توفر نموذج سعر مبيعات واحد على الأقل.</span><span class="sxs-lookup"><span data-stu-id="3e713-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="3e713-106">يستخدم هذا المثال نموذج السعر لنموذج سعر المبيعات لحل "مكبر الصوت" في شركة بيانات العرض التوضيحي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="3e713-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="3e713-107">يستخدم مدير المنتج عادةً هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="3e713-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="3e713-108">إضافة معيار جديد لنموذج سعر مبيعات موجود</span><span class="sxs-lookup"><span data-stu-id="3e713-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="3e713-109">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="3e713-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3e713-110">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="3e713-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="3e713-111">في القائمة، حدد الصف الخاص بنموذج المنتج لحل "مكبر الصوت"، ولكن لا تنقر فوق الارتباط الخاص باسم النموذج.</span><span class="sxs-lookup"><span data-stu-id="3e713-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="3e713-112">في جزء الإجراءات، انقر فوق "النموذج".</span><span class="sxs-lookup"><span data-stu-id="3e713-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="3e713-113">انقر فوق "معايير نموذج السعر".</span><span class="sxs-lookup"><span data-stu-id="3e713-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="3e713-114">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="3e713-114">Click New.</span></span>
7. <span data-ttu-id="3e713-115">في الحقل "الاسم، اكتب "مجموعة العملاء 10".</span><span class="sxs-lookup"><span data-stu-id="3e713-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="3e713-116">يتم استخدام اسم معيار نموذج السعر للمساعدة في تحديد معايير التحديد الأساسية.</span><span class="sxs-lookup"><span data-stu-id="3e713-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="3e713-117">في الحقل "نموذج السعر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3e713-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="3e713-118">في الحقل "نوع الأمر"، حدد "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="3e713-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="3e713-119">يحدد نوع الأمر حقول قاعدة البيانات التي سوف تكون متاحة لاستعلام التحديد.</span><span class="sxs-lookup"><span data-stu-id="3e713-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="3e713-120">في الحقل "صالح من"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3e713-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="3e713-121">في الحقل "تنتهي الصلاحية في‬"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="3e713-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="3e713-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3e713-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="3e713-123">إنشاء استعلام لمعايير التحديد</span><span class="sxs-lookup"><span data-stu-id="3e713-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="3e713-124">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="3e713-124">Click Edit.</span></span>
2. <span data-ttu-id="3e713-125">في الحقل "جدول"، حدد "العملاء".</span><span class="sxs-lookup"><span data-stu-id="3e713-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="3e713-126">في حقل "الحقل"، حدد "مجموعة العملاء".</span><span class="sxs-lookup"><span data-stu-id="3e713-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="3e713-127">في هذا المثال، سوف نستخدم مجموعة محددة من العملاء لمعايير التحديد.</span><span class="sxs-lookup"><span data-stu-id="3e713-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="3e713-128">في حقل "المعايير"، حدد "مجموعة العملاء 10".</span><span class="sxs-lookup"><span data-stu-id="3e713-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="3e713-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3e713-129">Click OK.</span></span>

