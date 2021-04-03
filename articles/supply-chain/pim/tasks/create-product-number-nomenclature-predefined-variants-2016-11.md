---
title: إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a4ad70a87cd8c6cab2e9853f4f6c52f574d318a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257401"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="f3301-103">إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="f3301-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3301-104">يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="f3301-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="f3301-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="f3301-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f3301-106">يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم".</span><span class="sxs-lookup"><span data-stu-id="f3301-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="f3301-107">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="f3301-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="f3301-108">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="f3301-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="f3301-109">حدد **تعريف نموذج متغير المنتج**.</span><span class="sxs-lookup"><span data-stu-id="f3301-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="f3301-110">حدد **كود nomenclature للمنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="f3301-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="f3301-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f3301-111">Select **New**.</span></span>
4. <span data-ttu-id="f3301-112">في الحقل **الاسم**، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="f3301-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="f3301-113">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f3301-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="f3301-114">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f3301-114">Select **Add**.</span></span>
7. <span data-ttu-id="f3301-115">حدد رقم **أصل المنتج**.</span><span class="sxs-lookup"><span data-stu-id="f3301-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="f3301-116">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f3301-116">Select **Add**.</span></span>
9. <span data-ttu-id="f3301-117">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="f3301-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="f3301-118">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f3301-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="f3301-119">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f3301-119">Select **Add**.</span></span>
12. <span data-ttu-id="f3301-120">حدد **اللون**.</span><span class="sxs-lookup"><span data-stu-id="f3301-120">Select **Color**.</span></span>
13. <span data-ttu-id="f3301-121">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f3301-121">Select **Add**.</span></span>
14. <span data-ttu-id="f3301-122">حدد **الثابت النصي**.</span><span class="sxs-lookup"><span data-stu-id="f3301-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="f3301-123">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="f3301-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="f3301-124">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="f3301-124">Select **Add**.</span></span>
17. <span data-ttu-id="f3301-125">حدد **الحجم**.</span><span class="sxs-lookup"><span data-stu-id="f3301-125">Select **Size**.</span></span>
18. <span data-ttu-id="f3301-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f3301-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="f3301-127">تعيين nomenclature إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="f3301-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="f3301-128">حدد **مجموعات أبعاد المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="f3301-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="f3301-129">حدد **مجموعة أبعاد المنتجات SizeCol**.</span><span class="sxs-lookup"><span data-stu-id="f3301-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="f3301-130">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="f3301-130">Select **Edit**.</span></span>
4. <span data-ttu-id="f3301-131">حدد **نعم** في الحقل **استخدام كود nomenclature**.</span><span class="sxs-lookup"><span data-stu-id="f3301-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="f3301-132">أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬**.</span><span class="sxs-lookup"><span data-stu-id="f3301-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="f3301-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f3301-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]