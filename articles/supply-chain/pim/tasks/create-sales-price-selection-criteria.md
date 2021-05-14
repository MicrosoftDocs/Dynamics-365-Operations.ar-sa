---
title: إنشاء معايير تحديد سعر المبيعات
description: يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920521"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="0d04e-103">إنشاء معايير تحديد سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="0d04e-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d04e-104">يوضح هذا الإجراء كيفية إنشاء معيار تحديد سعر المبيعات لنماذج أسعار المبيعات التي تستند إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="0d04e-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="0d04e-105">يتطلب هذا الإجراء توفر نموذج سعر مبيعات واحد على الأقل.</span><span class="sxs-lookup"><span data-stu-id="0d04e-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="0d04e-106">يستخدم هذا المثال نموذج السعر لنموذج سعر المبيعات لحل "مكبر الصوت" في شركة بيانات العرض التوضيحي USMF.‬</span><span class="sxs-lookup"><span data-stu-id="0d04e-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="0d04e-107">يستخدم مدير المنتج عادةً هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0d04e-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="0d04e-108">إضافة معيار جديد لنموذج سعر مبيعات موجود</span><span class="sxs-lookup"><span data-stu-id="0d04e-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="0d04e-109">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="0d04e-110">في القائمة، حدد الصف الخاص بنموذج المنتج لحل "مكبر الصوت"، ولكن لا تحدد الارتباط الخاص باسم النموذج.</span><span class="sxs-lookup"><span data-stu-id="0d04e-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="0d04e-111">في جزء الإجراءات، حدد **النموذج**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="0d04e-112">حدد **معايير نموذج السعر**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="0d04e-113">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-113">Select **New**.</span></span>
1. <span data-ttu-id="0d04e-114">في حقل **الاسم**، اكتب "مجموعة العملاء 10".</span><span class="sxs-lookup"><span data-stu-id="0d04e-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="0d04e-115">يتم استخدام اسم معيار نموذج السعر للمساعدة في تحديد معايير التحديد الأساسية.</span><span class="sxs-lookup"><span data-stu-id="0d04e-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="0d04e-116">في حقل **نموذج السعر**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0d04e-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="0d04e-117">في حقل **نوع الأمر**، حدد *أمر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="0d04e-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="0d04e-118">يحدد نوع الأمر حقول قاعدة البيانات التي سوف تكون متاحة لاستعلام التحديد.</span><span class="sxs-lookup"><span data-stu-id="0d04e-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="0d04e-119">في حقل **صالح من**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0d04e-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="0d04e-120">في حقل **تنتهي الصلاحية في**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="0d04e-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="0d04e-121">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="0d04e-122">إنشاء استعلام لمعايير التحديد</span><span class="sxs-lookup"><span data-stu-id="0d04e-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="0d04e-123">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-123">Select **Edit**.</span></span>
2. <span data-ttu-id="0d04e-124">في حقل **الجدول**، حدد *العملاء*.</span><span class="sxs-lookup"><span data-stu-id="0d04e-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="0d04e-125">في حقل **الحقل**، حدد *مجموعة العملاء*.</span><span class="sxs-lookup"><span data-stu-id="0d04e-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="0d04e-126">في هذا المثال، سوف نستخدم مجموعة محددة من العملاء لمعايير التحديد.</span><span class="sxs-lookup"><span data-stu-id="0d04e-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="0d04e-127">في حقل **المعايير**، حدد *مجموعة العملاء 10*.</span><span class="sxs-lookup"><span data-stu-id="0d04e-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="0d04e-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0d04e-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]