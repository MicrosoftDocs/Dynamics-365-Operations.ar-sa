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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543992"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="3e82e-103">تكوين حقوق الوصول لمراقب كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3e82e-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e82e-104">استخدم هذا الإجراء لتكوين حقوق الوصول لمراقب كائن التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3e82e-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="3e82e-105">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USP2.</span><span class="sxs-lookup"><span data-stu-id="3e82e-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="3e82e-106">تعيين دور مراقب كائن التكلفة</span><span class="sxs-lookup"><span data-stu-id="3e82e-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="3e82e-107">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3e82e-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="3e82e-108">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="3e82e-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3e82e-109">على سبيل المثال، قم بإجراء التصفية بالحقل "اسم المستخدم" باستخدام القيمة "أليسيا".</span><span class="sxs-lookup"><span data-stu-id="3e82e-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="3e82e-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e82e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3e82e-111">انقر فوق "تعيين الأدوار".</span><span class="sxs-lookup"><span data-stu-id="3e82e-111">Click Assign roles.</span></span>
5. <span data-ttu-id="3e82e-112">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3e82e-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="3e82e-113">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="3e82e-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="3e82e-114">تمكين أمان قائمة الوصول</span><span class="sxs-lookup"><span data-stu-id="3e82e-114">Enable access list security</span></span>
1. <span data-ttu-id="3e82e-115">انتقل إلى محاسبة التكاليف > الأبعاد > التدرجات الهرمية للأبعاد‬.</span><span class="sxs-lookup"><span data-stu-id="3e82e-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="3e82e-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="3e82e-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3e82e-117">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="3e82e-117">Select Organization.</span></span>  
3. <span data-ttu-id="3e82e-118">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="3e82e-118">Click Edit.</span></span>
4. <span data-ttu-id="3e82e-119">حدد "نعم" في حقل "التدرج الهرمي لقائمة الوصول".</span><span class="sxs-lookup"><span data-stu-id="3e82e-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="3e82e-120">انقر فوق "عرض التدرج الهرمي".</span><span class="sxs-lookup"><span data-stu-id="3e82e-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="3e82e-121">تعيين حقوق الوصول للمستخدم</span><span class="sxs-lookup"><span data-stu-id="3e82e-121">Assign access rights to user</span></span>
1. <span data-ttu-id="3e82e-122">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3e82e-122">Click New.</span></span>
2. <span data-ttu-id="3e82e-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e82e-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3e82e-124">في حقل "معرّف المستخدم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3e82e-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="3e82e-125">حدد "المسؤول".</span><span class="sxs-lookup"><span data-stu-id="3e82e-125">Select Admin.</span></span>  
4. <span data-ttu-id="3e82e-126">في الشجرة، حدد "المؤسسة\CEO\CFO\FIM".</span><span class="sxs-lookup"><span data-stu-id="3e82e-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="3e82e-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3e82e-127">Click New.</span></span>
6. <span data-ttu-id="3e82e-128">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3e82e-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3e82e-129">في حقل "معرّف المستخدم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="3e82e-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="3e82e-130">حدد "أليسيا".</span><span class="sxs-lookup"><span data-stu-id="3e82e-130">Select Alicia.</span></span>  
8. <span data-ttu-id="3e82e-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3e82e-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="3e82e-132">تمكين حقوق الوصول في محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="3e82e-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="3e82e-133">انتقل إلى محاسبة التكاليف > الإعداد > المعلمات.</span><span class="sxs-lookup"><span data-stu-id="3e82e-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="3e82e-134">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="3e82e-134">Click the General tab.</span></span>
3. <span data-ttu-id="3e82e-135">حدد "نعم" في الحقل "تمكين عرض الوصول لأعضاء بُعد كائن التكلفة‬".</span><span class="sxs-lookup"><span data-stu-id="3e82e-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="3e82e-136">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3e82e-136">Click Save.</span></span>
5. <span data-ttu-id="3e82e-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3e82e-137">Close the page.</span></span>
6. <span data-ttu-id="3e82e-138">انتقل إلى محاسبة التكاليف > الإعداد > تكوين مساحة عمل مراقبة التكلفة.</span><span class="sxs-lookup"><span data-stu-id="3e82e-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="3e82e-139">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="3e82e-139">Click Edit.</span></span>
8. <span data-ttu-id="3e82e-140">حدد "نعم" في الحقل "منشور".</span><span class="sxs-lookup"><span data-stu-id="3e82e-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="3e82e-141">إذا قمت بتعيين هذا الخيار إلى "نعم"، سيتمكن المستخدم الذين تم تعيين أحد الأدوار الأربعة التالية له من مشاهدة التقارير في مساحة عمل التحكم في التكلفة‬: مدير محاسبة التكاليف ومحاسب التكاليف وموظف محاسبة التكاليف ومراقب كائن التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="3e82e-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="3e82e-142">إذا حددت "لا"، فسيتمكن فقط المستخدم الذين تم تعيين أحد الأدوار التالية له من مشاهدة التقارير‬: مدير محاسبة التكاليف ومحاسب التكاليف وموظف محاسبة التكاليف ومراقب كائن التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="3e82e-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="3e82e-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3e82e-143">Click Save.</span></span>

