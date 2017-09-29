--- 
title: "إنشاء رقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫"
description: "يوضح هذا الدليل كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="964e1-103">إنشاء رقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫</span><span class="sxs-lookup"><span data-stu-id="964e1-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="964e1-104">يوضح هذا الدليل كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="964e1-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="964e1-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="964e1-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="964e1-106">يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم".</span><span class="sxs-lookup"><span data-stu-id="964e1-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="964e1-107">وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.</span><span class="sxs-lookup"><span data-stu-id="964e1-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="964e1-108">إنشاء nomenclature لرقم المنتج</span><span class="sxs-lookup"><span data-stu-id="964e1-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="964e1-109">انقر فوق "تعريف نموذج متغير المنتج"ز</span><span class="sxs-lookup"><span data-stu-id="964e1-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="964e1-110">انقر فوق "كود nomenclature للمنتج‬".</span><span class="sxs-lookup"><span data-stu-id="964e1-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="964e1-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="964e1-111">Click New.</span></span>
4. <span data-ttu-id="964e1-112">في الحقل "الاسم"، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، ColorSize...</span><span class="sxs-lookup"><span data-stu-id="964e1-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="964e1-113">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="964e1-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="964e1-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="964e1-114">Click Add.</span></span>
7. <span data-ttu-id="964e1-115">انقر فوق "رقم أصل المنتج".</span><span class="sxs-lookup"><span data-stu-id="964e1-115">Click Product master number.</span></span>
8. <span data-ttu-id="964e1-116">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="964e1-116">Click Add.</span></span>
9. <span data-ttu-id="964e1-117">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="964e1-117">Click Text constant.</span></span>
10. <span data-ttu-id="964e1-118">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="964e1-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="964e1-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="964e1-119">Click Add.</span></span>
12. <span data-ttu-id="964e1-120">انقر فوق "اللون".</span><span class="sxs-lookup"><span data-stu-id="964e1-120">Click Color.</span></span>
13. <span data-ttu-id="964e1-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="964e1-121">Click Add.</span></span>
14. <span data-ttu-id="964e1-122">انقر فوق "الثابت النصي‬".</span><span class="sxs-lookup"><span data-stu-id="964e1-122">Click Text constant.</span></span>
15. <span data-ttu-id="964e1-123">في الحقل "نص"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="964e1-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="964e1-124">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="964e1-124">Click Add.</span></span>
17. <span data-ttu-id="964e1-125">انقر فوق "الحجم".</span><span class="sxs-lookup"><span data-stu-id="964e1-125">Click Size.</span></span>
18. <span data-ttu-id="964e1-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="964e1-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="964e1-127">تعيين nomenclature إلى أصل المنتج</span><span class="sxs-lookup"><span data-stu-id="964e1-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="964e1-128">انقر فوق "مجموعات أبعاد المنتجات".</span><span class="sxs-lookup"><span data-stu-id="964e1-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="964e1-129">حدد مجموعة أبعاد المنتجات SizeCol.</span><span class="sxs-lookup"><span data-stu-id="964e1-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="964e1-130">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="964e1-130">Click Edit.</span></span>
4. <span data-ttu-id="964e1-131">حدد "نعم" في الحقل "استخدام كود nomenclature".</span><span class="sxs-lookup"><span data-stu-id="964e1-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="964e1-132">في حقل "كود nomenclature لرقم متغير المنتج‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="964e1-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="964e1-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="964e1-133">Close the page.</span></span>


