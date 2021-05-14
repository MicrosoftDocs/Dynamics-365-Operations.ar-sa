---
title: إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920647"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="f864e-103">إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="f864e-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f864e-104">يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f864e-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="f864e-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="f864e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f864e-106">يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم".</span><span class="sxs-lookup"><span data-stu-id="f864e-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="f864e-107">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="f864e-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="f864e-108">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="f864e-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="f864e-109">انتقل إلى **إدارة معلومات المنتج \> إعداد \> ‏‫كود nomenclature للمنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="f864e-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="f864e-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f864e-110">Select **New**.</span></span>
1. <span data-ttu-id="f864e-111">في الحقل **الاسم**، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="f864e-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="f864e-112">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f864e-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="f864e-113">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f864e-113">Select **Add**.</span></span>
1. <span data-ttu-id="f864e-114">حدد رقم **أصل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="f864e-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="f864e-115">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f864e-115">Select **Add**.</span></span>
1. <span data-ttu-id="f864e-116">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="f864e-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="f864e-117">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f864e-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="f864e-118">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f864e-118">Select **Add**.</span></span>
1. <span data-ttu-id="f864e-119">حدد **اللون**.</span><span class="sxs-lookup"><span data-stu-id="f864e-119">Select **Color**.</span></span>
1. <span data-ttu-id="f864e-120">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f864e-120">Select **Add**.</span></span>
1. <span data-ttu-id="f864e-121">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="f864e-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="f864e-122">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f864e-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="f864e-123">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f864e-123">Select **Add**.</span></span>
1. <span data-ttu-id="f864e-124">حدد **الحجم**.</span><span class="sxs-lookup"><span data-stu-id="f864e-124">Select **Size**.</span></span>
1. <span data-ttu-id="f864e-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f864e-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="f864e-126">تعيين nomenclature إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="f864e-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="f864e-127">حدد **مجموعات أبعاد المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="f864e-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="f864e-128">حدد **مجموعة أبعاد المنتجات SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="f864e-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="f864e-129">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f864e-129">Select **Edit**.</span></span>
4. <span data-ttu-id="f864e-130">حدد **نعم** في الحقل **استخدام كود nomenclature**.</span><span class="sxs-lookup"><span data-stu-id="f864e-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="f864e-131">أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="f864e-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="f864e-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f864e-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]