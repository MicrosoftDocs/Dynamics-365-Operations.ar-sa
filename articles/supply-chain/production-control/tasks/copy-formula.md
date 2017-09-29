--- 
title: "‏‫نسخ معادلة‬"
description: "يركز هذا الإجراء على إنشاء معادلة تتضمن نفس المكونات التي تتضمنها معادلة موجودة، ولكن مع اختلافات بسيطة."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 036bd9f592ca584afad9d4b9b7a49a9787076056
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="copy-a-formula"></a><span data-ttu-id="10a6b-103">‏‫نسخ معادلة‬</span><span class="sxs-lookup"><span data-stu-id="10a6b-103">Copy a formula</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10a6b-104">يركز هذا الإجراء على إنشاء معادلة تتضمن نفس المكونات التي تتضمنها معادلة موجودة، ولكن مع اختلافات بسيطة.</span><span class="sxs-lookup"><span data-stu-id="10a6b-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="10a6b-105">لإنشاء بنود المعادلة، يمكنك استخدام دالة النسخ لنسخ معادلة موجودة تحتوي على معظم المكونات التي تحتاجها.</span><span class="sxs-lookup"><span data-stu-id="10a6b-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="10a6b-106">ثم يمكنك إجراء أية تغييرات ضرورية على البنود الفردية في الإصدار الجديد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="10a6b-107">باستخدام دالة النسخ، لا يلزمك إنشاء معادلات متعددة متماثلة تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="10a6b-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="10a6b-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USP2.‬</span><span class="sxs-lookup"><span data-stu-id="10a6b-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="10a6b-109">إنشاء معادلة</span><span class="sxs-lookup"><span data-stu-id="10a6b-109">Create a formula</span></span>
1. <span data-ttu-id="10a6b-110">انتقل إلى إدارة معلومات المنتج > قوائم مكونات الصنف والمعادلات‬ > المعادلات.</span><span class="sxs-lookup"><span data-stu-id="10a6b-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="10a6b-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="10a6b-111">Click New.</span></span>
3. <span data-ttu-id="10a6b-112">في الحقل "المعادلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="10a6b-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="10a6b-113">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="10a6b-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="10a6b-114">اكتب اسمًا ذا معنى للمعادلة.</span><span class="sxs-lookup"><span data-stu-id="10a6b-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="10a6b-115">في الحقل "الموقع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a6b-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10a6b-116">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="10a6b-117">في الحقل "مجموعة الأصناف‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a6b-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="10a6b-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="10a6b-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="10a6b-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="10a6b-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="10a6b-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="10a6b-121">نسخ بنود المعادلة</span><span class="sxs-lookup"><span data-stu-id="10a6b-121">Copy formula lines</span></span>
1. <span data-ttu-id="10a6b-122">في جزء الإجراءات، انقر فوق "المعادلة".</span><span class="sxs-lookup"><span data-stu-id="10a6b-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="10a6b-123">انقر فوق نسخ.</span><span class="sxs-lookup"><span data-stu-id="10a6b-123">Click Copy.</span></span>
3. <span data-ttu-id="10a6b-124">في الحقل "رقم الصنف"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a6b-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="10a6b-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10a6b-126">في الحقل "إصدار المعادلة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a6b-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="10a6b-127">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="10a6b-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10a6b-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="10a6b-129">ضبط بنود المعادلة المنسوخة</span><span class="sxs-lookup"><span data-stu-id="10a6b-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="10a6b-130">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="10a6b-131">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="10a6b-131">Click Delete.</span></span>
3. <span data-ttu-id="10a6b-132">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="10a6b-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="10a6b-133">الموافقة على التركيبة</span><span class="sxs-lookup"><span data-stu-id="10a6b-133">Approve formula</span></span>
1. <span data-ttu-id="10a6b-134">في جزء الإجراءات، انقر فوق "المعادلة".</span><span class="sxs-lookup"><span data-stu-id="10a6b-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="10a6b-135">انقر فوق "الموافقة على المعادلة".</span><span class="sxs-lookup"><span data-stu-id="10a6b-135">Click Approve formula.</span></span>
3. <span data-ttu-id="10a6b-136">في الحقل "تمت الموافقة بواسطة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="10a6b-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="10a6b-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10a6b-138">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="10a6b-138">Click Select.</span></span>
6. <span data-ttu-id="10a6b-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="10a6b-139">Click OK.</span></span>


