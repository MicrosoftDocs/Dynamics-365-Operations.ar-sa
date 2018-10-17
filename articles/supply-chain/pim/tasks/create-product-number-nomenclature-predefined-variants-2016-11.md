--- 
title: "إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫"
description: "يوضح هذا الدليل كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="2f174-103">إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="2f174-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f174-104">يوضح هذا الدليل كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="2f174-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="2f174-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="2f174-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2f174-106">يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم".</span><span class="sxs-lookup"><span data-stu-id="2f174-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="2f174-107">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="2f174-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="2f174-108">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="2f174-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="2f174-109">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="2f174-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="2f174-110">انقر فوق "كود nomenclature للمنتج‬".</span><span class="sxs-lookup"><span data-stu-id="2f174-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="2f174-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2f174-111">Click New.</span></span>
4. <span data-ttu-id="2f174-112">في الحقل "الاسم"، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، ColorSize...</span><span class="sxs-lookup"><span data-stu-id="2f174-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="2f174-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2f174-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2f174-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2f174-114">Click Add.</span></span>
7. <span data-ttu-id="2f174-115">انقر فوق "رقم أصل المنتج".</span><span class="sxs-lookup"><span data-stu-id="2f174-115">Click Product master number.</span></span>
8. <span data-ttu-id="2f174-116">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2f174-116">Click Add.</span></span>
9. <span data-ttu-id="2f174-117">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="2f174-117">Click Text constant.</span></span>
10. <span data-ttu-id="2f174-118">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2f174-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="2f174-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2f174-119">Click Add.</span></span>
12. <span data-ttu-id="2f174-120">انقر فوق "اللون".</span><span class="sxs-lookup"><span data-stu-id="2f174-120">Click Color.</span></span>
13. <span data-ttu-id="2f174-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2f174-121">Click Add.</span></span>
14. <span data-ttu-id="2f174-122">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="2f174-122">Click Text constant.</span></span>
15. <span data-ttu-id="2f174-123">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2f174-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="2f174-124">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2f174-124">Click Add.</span></span>
17. <span data-ttu-id="2f174-125">انقر فوق "الحجم".</span><span class="sxs-lookup"><span data-stu-id="2f174-125">Click Size.</span></span>
18. <span data-ttu-id="2f174-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2f174-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="2f174-127">تعيين nomenclature إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="2f174-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="2f174-128">انقر فوق "مجموعات أبعاد المنتجات".</span><span class="sxs-lookup"><span data-stu-id="2f174-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="2f174-129">حدد مجموعة أبعاد المنتجات SizeCol.</span><span class="sxs-lookup"><span data-stu-id="2f174-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="2f174-130">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="2f174-130">Click Edit.</span></span>
4. <span data-ttu-id="2f174-131">حدد "نعم" في الحقل "استخدام كود nomenclature".</span><span class="sxs-lookup"><span data-stu-id="2f174-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="2f174-132">في حقل "كود nomenclature لرقم متغير المنتج‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2f174-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="2f174-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2f174-133">Close the page.</span></span>


