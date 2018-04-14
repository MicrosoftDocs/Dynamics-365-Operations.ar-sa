--- 
title: "إعداد المهام الإضافية"
description: "يوضح هذا الإجراء كيفية إعداد مهمة إضافية."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 29b39ad74c064da88154a77299cedc9babe3786b
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="539b2-103">إعداد المهام الإضافية</span><span class="sxs-lookup"><span data-stu-id="539b2-103">Set up accessorial assignments</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="539b2-104">يوضح هذا الإجراء كيفية إعداد مهمة إضافية.</span><span class="sxs-lookup"><span data-stu-id="539b2-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="539b2-105">عادة ما يتم ذلك عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="539b2-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="539b2-106">قبل استخدام هذا الدليل تحتاج إلى تشغيل الدليل "إعداد مصاريف الموزع الإضافية والأصول الإضافية‬".</span><span class="sxs-lookup"><span data-stu-id="539b2-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="539b2-107">إعداد المهام الإضافية</span><span class="sxs-lookup"><span data-stu-id="539b2-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="539b2-108">انتقل إلى إدارة النقل > إعداد > التقييم‬ > مهام إضافية.</span><span class="sxs-lookup"><span data-stu-id="539b2-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="539b2-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="539b2-109">Click New.</span></span>
3. <span data-ttu-id="539b2-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="539b2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="539b2-111">بدّل توسيع المقطع "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="539b2-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="539b2-112">في الحقل "الموزِّع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="539b2-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="539b2-113">في القائمة، حدد الموزِّع‬ الذي أنشأت سجلاً رئيسيًا إضافيًا له عندما قمت بتشغيل الدليل "إعداد مصاريف الموزع الإضافية والأصول الإضافية‬".</span><span class="sxs-lookup"><span data-stu-id="539b2-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="539b2-114">في الحقل "معرف الموزِّع الإضافي‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="539b2-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="539b2-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="539b2-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="539b2-116">بدّل توسيع المقطع "المعايير".</span><span class="sxs-lookup"><span data-stu-id="539b2-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="539b2-117">في المقطع "مشروط‬"، يمكنك أن تختار المعايير الدقيقة للتوقيت الذي يجب فيه تطبيق التكلفة، استنادًا إلى القيم المختلفة المقدمة هنا.</span><span class="sxs-lookup"><span data-stu-id="539b2-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="539b2-118">عيّن الخيار "تطبيق دائمًا‬‬‬" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="539b2-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="539b2-119">في الحقل "مستوى التعيين الإضافي‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="539b2-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="539b2-120">بدّل توسيع المقطع "الحساب".</span><span class="sxs-lookup"><span data-stu-id="539b2-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="539b2-121">في الحقل "نوع الرسوم الإضافية‬"، حدد "الأساسي".</span><span class="sxs-lookup"><span data-stu-id="539b2-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="539b2-122">يحدد نوع "الرسوم الإضافية‬" كيفية حساب التكلفة الفعلية.</span><span class="sxs-lookup"><span data-stu-id="539b2-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="539b2-123">في هذا المثال، إنها تكلفة أساسية.</span><span class="sxs-lookup"><span data-stu-id="539b2-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="539b2-124">في الحقل "الرسوم الإضافية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="539b2-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="539b2-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="539b2-125">Click Save.</span></span>


