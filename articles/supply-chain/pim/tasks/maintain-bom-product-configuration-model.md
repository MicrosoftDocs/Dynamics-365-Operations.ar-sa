---
title: الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج
description: يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921307"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="7f55d-103">الاحتفاظ ‏‫بقائمة مكونات الصنف‬ لطراز تكوين المنتج</span><span class="sxs-lookup"><span data-stu-id="7f55d-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f55d-104">يتطلب تشغيل هذا الإجراء نموذج تكوين منتج موجود.</span><span class="sxs-lookup"><span data-stu-id="7f55d-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="7f55d-105">يتم استخدام نموذج مكبر الصوت المتطور في شركة العرض التوضيحي USMF لإنشاء هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="7f55d-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="7f55d-106">إضافة بند قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="7f55d-106">Add a BOM line</span></span>

1. <span data-ttu-id="7f55d-107">انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="7f55d-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7f55d-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7f55d-109">حدد مكبر الصوت المتطور لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="7f55d-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="7f55d-110">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7f55d-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="7f55d-111">قم بتوسيع قسم **بنود قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="7f55d-112">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-112">Select **Add**.</span></span>
1. <span data-ttu-id="7f55d-113">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7f55d-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7f55d-114">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7f55d-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="7f55d-115">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="7f55d-116">إضافة تفاصيل بنود قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="7f55d-116">Add BOM line details</span></span>

1. <span data-ttu-id="7f55d-117">حدد **تفاصيل بند قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="7f55d-118">في الحقل **رقم الصنف**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="7f55d-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="7f55d-119">على سبيل المثال، يمكنك تحديد الصنف M0055.</span><span class="sxs-lookup"><span data-stu-id="7f55d-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="7f55d-120">لكل خاصية بند قائمة مكونات الصنف، يمكنك تحديد إذا كانت الخاصية سيُحدد لها قيمة ثابتة أو يتم تعيينها إلى سمة.</span><span class="sxs-lookup"><span data-stu-id="7f55d-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="7f55d-121">حدد خانة الاختيار **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="7f55d-122">حدد *نعم* في حقل **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="7f55d-123">يضمن تعيين خاصية **الحساب** إلى *نعم* إدراج بند قائمة مكونات الصنف في حسابات التكلفة.</span><span class="sxs-lookup"><span data-stu-id="7f55d-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="7f55d-124">حدد علامة التبويب **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="7f55d-125">حدد خانة الاختيار **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="7f55d-126">في الحقل **الكمية**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="7f55d-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7f55d-127">يحدد الحقل "الكمية" كمية الصنف التي سيتم تضمينها في قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="7f55d-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="7f55d-128">قد يكون هذا مرشحًا واضحًا لتعيين سمة.</span><span class="sxs-lookup"><span data-stu-id="7f55d-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="7f55d-129">حدد علامة التبويب **بُعد**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="7f55d-130">تحقق مما إذا كان أي من أبعاد المنتج نشطًا ويجب أن يكون ذا قيمة أو سمة معينة في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="7f55d-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="7f55d-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7f55d-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]