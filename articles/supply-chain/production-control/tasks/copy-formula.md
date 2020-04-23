---
title: ‏‫نسخ معادلة‬
description: يركز هذا الإجراء على إنشاء معادلة تتضمن نفس المكونات التي تتضمنها معادلة موجودة، ولكن مع اختلافات بسيطة.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 624e06c2184764f3fd8df3ddf7d90753ef2cb9d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210929"
---
# <a name="copy-a-formula"></a><span data-ttu-id="d6635-103">‏‫نسخ معادلة‬</span><span class="sxs-lookup"><span data-stu-id="d6635-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6635-104">يركز هذا الإجراء على إنشاء معادلة تتضمن نفس المكونات التي تتضمنها معادلة موجودة، ولكن مع اختلافات بسيطة.</span><span class="sxs-lookup"><span data-stu-id="d6635-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="d6635-105">لإنشاء بنود المعادلة، يمكنك استخدام دالة النسخ لنسخ معادلة موجودة تحتوي على معظم المكونات التي تحتاجها.</span><span class="sxs-lookup"><span data-stu-id="d6635-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="d6635-106">ثم يمكنك إجراء أية تغييرات ضرورية على البنود الفردية في الإصدار الجديد.</span><span class="sxs-lookup"><span data-stu-id="d6635-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="d6635-107">باستخدام دالة النسخ، لا يلزمك إنشاء معادلات متعددة متماثلة تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="d6635-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="d6635-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USP2.‬</span><span class="sxs-lookup"><span data-stu-id="d6635-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="d6635-109">إنشاء معادلة</span><span class="sxs-lookup"><span data-stu-id="d6635-109">Create a formula</span></span>
1. <span data-ttu-id="d6635-110">انتقل إلى إدارة معلومات المنتج > قوائم مكونات الصنف والمعادلات‬ > المعادلات.</span><span class="sxs-lookup"><span data-stu-id="d6635-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="d6635-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d6635-111">Click New.</span></span>
3. <span data-ttu-id="d6635-112">في الحقل "المعادلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d6635-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="d6635-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d6635-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d6635-114">اكتب اسمًا ذا معنى للمعادلة.</span><span class="sxs-lookup"><span data-stu-id="d6635-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="d6635-115">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6635-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d6635-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6635-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d6635-117">في الحقل "مجموعة الأصناف‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6635-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d6635-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d6635-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d6635-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6635-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d6635-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d6635-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="d6635-121">نسخ بنود المعادلة</span><span class="sxs-lookup"><span data-stu-id="d6635-121">Copy formula lines</span></span>
1. <span data-ttu-id="d6635-122">في جزء الإجراءات، انقر فوق "المعادلة".</span><span class="sxs-lookup"><span data-stu-id="d6635-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="d6635-123">انقر فوق نسخ.</span><span class="sxs-lookup"><span data-stu-id="d6635-123">Click Copy.</span></span>
3. <span data-ttu-id="d6635-124">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6635-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d6635-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6635-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6635-126">في الحقل "إصدار المعادلة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6635-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d6635-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6635-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d6635-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d6635-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="d6635-129">ضبط بنود المعادلة المنسوخة</span><span class="sxs-lookup"><span data-stu-id="d6635-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="d6635-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6635-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="d6635-131">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="d6635-131">Click Delete.</span></span>
3. <span data-ttu-id="d6635-132">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="d6635-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="d6635-133">الموافقة على التركيبة</span><span class="sxs-lookup"><span data-stu-id="d6635-133">Approve formula</span></span>
1. <span data-ttu-id="d6635-134">في جزء الإجراءات، انقر فوق "المعادلة".</span><span class="sxs-lookup"><span data-stu-id="d6635-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="d6635-135">انقر فوق "الموافقة على المعادلة".</span><span class="sxs-lookup"><span data-stu-id="d6635-135">Click Approve formula.</span></span>
3. <span data-ttu-id="d6635-136">في الحقل "تمت الموافقة بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d6635-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d6635-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d6635-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6635-138">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="d6635-138">Click Select.</span></span>
6. <span data-ttu-id="d6635-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d6635-139">Click OK.</span></span>

