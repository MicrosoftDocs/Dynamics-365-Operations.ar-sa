---
title: إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150028"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="87fc0-103">إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="87fc0-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87fc0-104">يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="87fc0-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="87fc0-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="87fc0-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="87fc0-106">يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم".</span><span class="sxs-lookup"><span data-stu-id="87fc0-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="87fc0-107">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="87fc0-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="87fc0-108">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="87fc0-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="87fc0-109">حدد **تعريف نموذج متغير المنتج**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="87fc0-110">حدد **كود nomenclature للمنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="87fc0-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-111">Select **New**.</span></span>
4. <span data-ttu-id="87fc0-112">في الحقل **الاسم**، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="87fc0-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="87fc0-113">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="87fc0-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="87fc0-114">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-114">Select **Add**.</span></span>
7. <span data-ttu-id="87fc0-115">حدد رقم **أصل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="87fc0-116">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-116">Select **Add**.</span></span>
9. <span data-ttu-id="87fc0-117">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="87fc0-118">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="87fc0-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="87fc0-119">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-119">Select **Add**.</span></span>
12. <span data-ttu-id="87fc0-120">حدد **اللون**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-120">Select **Color**.</span></span>
13. <span data-ttu-id="87fc0-121">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-121">Select **Add**.</span></span>
14. <span data-ttu-id="87fc0-122">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="87fc0-123">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="87fc0-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="87fc0-124">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-124">Select **Add**.</span></span>
17. <span data-ttu-id="87fc0-125">حدد **الحجم**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-125">Select **Size**.</span></span>
18. <span data-ttu-id="87fc0-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="87fc0-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="87fc0-127">تعيين nomenclature إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="87fc0-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="87fc0-128">حدد **مجموعات أبعاد المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="87fc0-129">حدد **مجموعة أبعاد المنتجات SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="87fc0-130">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-130">Select **Edit**.</span></span>
4. <span data-ttu-id="87fc0-131">حدد **نعم** في الحقل **استخدام كود nomenclature**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="87fc0-132">أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="87fc0-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="87fc0-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="87fc0-133">Close the page.</span></span>

