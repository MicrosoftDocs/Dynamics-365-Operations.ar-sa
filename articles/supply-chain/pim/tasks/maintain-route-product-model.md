---
title: الاحتفاظ بمسار لنموذج منتج
description: يتطلب تشغيل هذا الإجراء تكوين نموذج منتج موجود.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921255"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="4e59e-103">الاحتفاظ بمسار لنموذج منتج</span><span class="sxs-lookup"><span data-stu-id="4e59e-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e59e-104">يتطلب تشغيل هذا الإجراء تكوين نموذج منتج موجود.</span><span class="sxs-lookup"><span data-stu-id="4e59e-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="4e59e-105">يستخدم هذا الإجراء نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF خلال العملية.</span><span class="sxs-lookup"><span data-stu-id="4e59e-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="4e59e-106">إضافة مسار عملية</span><span class="sxs-lookup"><span data-stu-id="4e59e-106">Add a route operation</span></span>

1. <span data-ttu-id="4e59e-107">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="4e59e-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4e59e-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4e59e-109">حدد نموذج مكبر الصوت المتطور لهذا التمرين.</span><span class="sxs-lookup"><span data-stu-id="4e59e-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="4e59e-110">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4e59e-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="4e59e-111">قم بتوسيع قسم **عمليات المسار**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="4e59e-112">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-112">Select **Add**.</span></span>
1. <span data-ttu-id="4e59e-113">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4e59e-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="4e59e-114">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="4e59e-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="4e59e-115">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="4e59e-116">إدخال تفاصيل مسار العمليات</span><span class="sxs-lookup"><span data-stu-id="4e59e-116">Enter route operation details</span></span>

1. <span data-ttu-id="4e59e-117">حدد **تفاصيل عمليات المسارات**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="4e59e-118">في حقل **العملية**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4e59e-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="4e59e-119">في **رقم العملية**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-119">In the **Oper. No.**</span></span> <span data-ttu-id="4e59e-120">، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4e59e-120">field, enter a number.</span></span>
    * <span data-ttu-id="4e59e-121">تحدد أرقام العملية تسلسل المسار.</span><span class="sxs-lookup"><span data-stu-id="4e59e-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="4e59e-122">قد تحصل كل خاصية بعملية مسار على قيمة ثابتة أو يتم تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="4e59e-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="4e59e-123">يؤدي التعيين إلى سمة إلى تعيين القيمة كجزء من التكوين.</span><span class="sxs-lookup"><span data-stu-id="4e59e-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="4e59e-124">في **مجموعة المسارات**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4e59e-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="4e59e-125">تحدد مجموعة المسارات السلوك الأساسي للتكاليف والاستهلاك والإعداد.</span><span class="sxs-lookup"><span data-stu-id="4e59e-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="4e59e-126">حدد علامة التبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="4e59e-127">حدد علامة التبويب **الأوقات**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="4e59e-128">في حقل **كمية العملية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4e59e-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="4e59e-129">حدد العدد الذي سوف تتم معالجته أثناء عملية واحدة.</span><span class="sxs-lookup"><span data-stu-id="4e59e-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="4e59e-130">في حقل **الساعات/الوقت**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4e59e-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="4e59e-131">أدخل نسبة الوقت.</span><span class="sxs-lookup"><span data-stu-id="4e59e-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="4e59e-132">حدد خانة الاختيار **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="4e59e-133">في حقل **وقت التشغيل**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="4e59e-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="4e59e-134">حدد وقت المعالجة للكمية التي قمت بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="4e59e-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="4e59e-135">حدد علامة التبويب **متطلبات المصدر**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="4e59e-136">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-136">Select **Add**.</span></span>
1. <span data-ttu-id="4e59e-137">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4e59e-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="4e59e-138">في حقل **نوع المتطلب**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="4e59e-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="4e59e-139">حدد ما إذا كنت تريد تحديد موارد أو قدرات معينة يجب أن تتوفر لدى الموارد.</span><span class="sxs-lookup"><span data-stu-id="4e59e-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="4e59e-140">في حقل **المتطلب**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="4e59e-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="4e59e-141">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4e59e-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]