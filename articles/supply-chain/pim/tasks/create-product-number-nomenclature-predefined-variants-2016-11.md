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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986037"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="b78c3-103">إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="b78c3-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b78c3-104">يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="b78c3-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="b78c3-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b78c3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b78c3-106">يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم".</span><span class="sxs-lookup"><span data-stu-id="b78c3-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="b78c3-107">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="b78c3-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="b78c3-108">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="b78c3-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="b78c3-109">حدد **تعريف نموذج متغير المنتج** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-109">Select **Product variant model definition** .</span></span>
2. <span data-ttu-id="b78c3-110">حدد **كود nomenclature للمنتج‬** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-110">Select **Product nomenclature** .</span></span>
3. <span data-ttu-id="b78c3-111">حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-111">Select **New** .</span></span>
4. <span data-ttu-id="b78c3-112">في الحقل **الاسم** ، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="b78c3-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="b78c3-113">في حقل **الوصف** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b78c3-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b78c3-114">حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-114">Select **Add** .</span></span>
7. <span data-ttu-id="b78c3-115">حدد رقم **أصل المنتج** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="b78c3-116">حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-116">Select **Add** .</span></span>
9. <span data-ttu-id="b78c3-117">حدد **الثابت النصي** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-117">Select **Text constant** .</span></span>
10. <span data-ttu-id="b78c3-118">في الحقل **النص** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b78c3-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="b78c3-119">حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-119">Select **Add** .</span></span>
12. <span data-ttu-id="b78c3-120">حدد **اللون** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-120">Select **Color** .</span></span>
13. <span data-ttu-id="b78c3-121">حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-121">Select **Add** .</span></span>
14. <span data-ttu-id="b78c3-122">حدد **الثابت النصي** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-122">Select **Text constant** .</span></span>
15. <span data-ttu-id="b78c3-123">في الحقل **النص** ، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b78c3-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="b78c3-124">حدد **إضافة** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-124">Select **Add** .</span></span>
17. <span data-ttu-id="b78c3-125">حدد **الحجم** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-125">Select **Size** .</span></span>
18. <span data-ttu-id="b78c3-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b78c3-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="b78c3-127">تعيين nomenclature إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="b78c3-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="b78c3-128">حدد **مجموعات أبعاد المنتجات** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-128">Select **Product dimension groups** .</span></span>
2. <span data-ttu-id="b78c3-129">حدد **مجموعة أبعاد المنتجات SizeCol** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="b78c3-130">حدد **تحرير** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-130">Select **Edit** .</span></span>
4. <span data-ttu-id="b78c3-131">حدد **نعم** في الحقل **استخدام كود nomenclature** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="b78c3-132">أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬** .</span><span class="sxs-lookup"><span data-stu-id="b78c3-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="b78c3-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b78c3-133">Close the page.</span></span>

