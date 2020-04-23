---
title: الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج
description: يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa2a22056ff4435d4c66f13c170aeadc02fbe03
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203562"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="ff9f6-103">الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="ff9f6-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff9f6-104">يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="ff9f6-105">يتم استخدام نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="ff9f6-106">إضافة بند قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="ff9f6-106">Add a BOM line</span></span>
1. <span data-ttu-id="ff9f6-107">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="ff9f6-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ff9f6-108">انقر فوق "نماذج تكوين المنتجات".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ff9f6-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ff9f6-110">حدد مكبر الصوت المتطور لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="ff9f6-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ff9f6-112">قم بتوسيع القسم "قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="ff9f6-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-113">Click Add.</span></span>
7. <span data-ttu-id="ff9f6-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ff9f6-115">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ff9f6-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="ff9f6-117">إضافة تفاصيل بنود قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="ff9f6-117">Add BOM line details</span></span>
1. <span data-ttu-id="ff9f6-118">انقر فوق "تفاصيل بنود قائمة مكونات الصنف".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-118">Click BOM line details.</span></span>
2. <span data-ttu-id="ff9f6-119">في الحقل "رقم الصنف"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="ff9f6-120">على سبيل المثال، يمكنك تحديد الصنف M0055.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="ff9f6-121">لكل خاصية بند قائمة مكونات الصنف، يمكنك تحديد إذا كانت الخاصية سيُحدد لها قيمة ثابتة أو يتم تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="ff9f6-122">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-122">Select the Set check box.</span></span>
4. <span data-ttu-id="ff9f6-123">حدد "نعم" في الحقل "حساب".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="ff9f6-124">يضمن تعيين "خاصية الحساب" على "نعم" إدراج بند قائمة مكونات الصنف في حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="ff9f6-125">انقر فوق علامة التبويب "إعداد".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="ff9f6-126">حدد خانة الاختيار "تعيين".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-126">Select the Set check box.</span></span>
7. <span data-ttu-id="ff9f6-127">في حقل الكمية، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ff9f6-128">يحدد الحقل "الكمية" كمية الصنف التي سيتم تضمينها في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="ff9f6-129">قد يكون هذا مرشحًا واضحًا لتعيين سمة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="ff9f6-130">انقر فوق علامة التبويب "البُعد".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="ff9f6-131">تحقق مما إذا كان أي من أبعاد المنتج نشطًا ويجب أن يكون ذا قيمة أو سمة معينة في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="ff9f6-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="ff9f6-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="ff9f6-132">Click OK.</span></span>

