---
title: تكوين حقوق الوصول لمراقب كائن التكلفة
description: استخدم هذا الإجراء لتكوين حقوق الوصول لمراقب كائن التكلفة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a931980add70ddc003d8a7c1a78f451bacbf57d4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144486"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="fbd4d-103">تكوين حقوق الوصول لمراقب كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="fbd4d-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbd4d-104">استخدم هذا الإجراء لتكوين حقوق الوصول لمراقب كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="fbd4d-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="fbd4d-106">تعيين دور مراقب كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="fbd4d-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="fbd4d-107">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="fbd4d-108">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="fbd4d-109">على سبيل المثال، قم بإجراء التصفية بالحقل "اسم المستخدم" باستخدام القيمة "أليسيا".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="fbd4d-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fbd4d-111">انقر فوق "تعيين الأدوار".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-111">Click Assign roles.</span></span>
5. <span data-ttu-id="fbd4d-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="fbd4d-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="fbd4d-114">تمكين أمان قائمة الوصول</span><span class="sxs-lookup"><span data-stu-id="fbd4d-114">Enable access list security</span></span>
1. <span data-ttu-id="fbd4d-115">انتقل إلى محاسبة التكاليف > الأبعاد > التدرجات الهرمية للأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="fbd4d-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fbd4d-117">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-117">Select Organization.</span></span>  
3. <span data-ttu-id="fbd4d-118">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-118">Click Edit.</span></span>
4. <span data-ttu-id="fbd4d-119">حدد "نعم" في حقل "التدرج الهرمي لقائمة الوصول".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="fbd4d-120">انقر فوق "عرض التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="fbd4d-121">تعيين حقوق الوصول للمستخدم</span><span class="sxs-lookup"><span data-stu-id="fbd4d-121">Assign access rights to user</span></span>
1. <span data-ttu-id="fbd4d-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-122">Click New.</span></span>
2. <span data-ttu-id="fbd4d-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="fbd4d-124">في حقل "معرّف المستخدم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="fbd4d-125">حدد "المسؤول".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-125">Select Admin.</span></span>  
4. <span data-ttu-id="fbd4d-126">في الشجرة، حدد "المؤسسة\CEO\CFO\FIM".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="fbd4d-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-127">Click New.</span></span>
6. <span data-ttu-id="fbd4d-128">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="fbd4d-129">في حقل "معرّف المستخدم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="fbd4d-130">حدد "أليسيا".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-130">Select Alicia.</span></span>  
8. <span data-ttu-id="fbd4d-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="fbd4d-132">تمكين حقوق الوصول في محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="fbd4d-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="fbd4d-133">انتقل إلى محاسبة التكاليف > الإعداد > المعلمات.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="fbd4d-134">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-134">Click the General tab.</span></span>
3. <span data-ttu-id="fbd4d-135">حدد "نعم" في الحقل "تمكين عرض الوصول لأعضاء بُعد كائن التكلفة‬".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="fbd4d-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-136">Click Save.</span></span>
5. <span data-ttu-id="fbd4d-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-137">Close the page.</span></span>
6. <span data-ttu-id="fbd4d-138">انتقل إلى محاسبة التكاليف > الإعداد > تكوين مساحة عمل مراقبة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="fbd4d-139">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-139">Click Edit.</span></span>
8. <span data-ttu-id="fbd4d-140">حدد "نعم" في الحقل "منشور".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="fbd4d-141">إذا قمت بتعيين هذا الخيار إلى "نعم"، سيتمكن المستخدم الذين تم تعيين أحد الأدوار الأربعة التالية له من مشاهدة التقارير في مساحة عمل التحكم في التكلفة‬: مدير محاسبة التكاليف ومحاسب التكاليف وموظف محاسبة التكاليف ومراقب كائن التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="fbd4d-142">إذا حددت "لا"، فسيتمكن فقط المستخدم الذين تم تعيين أحد الأدوار التالية له من مشاهدة التقارير‬: مدير محاسبة التكاليف ومحاسب التكاليف وموظف محاسبة التكاليف ومراقب كائن التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="fbd4d-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="fbd4d-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="fbd4d-143">Click Save.</span></span>

