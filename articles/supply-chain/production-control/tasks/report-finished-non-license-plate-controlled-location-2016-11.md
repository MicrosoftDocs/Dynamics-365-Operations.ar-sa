--- 
title: "الإبلاغ عن الانتهاء إلى موقع يتم التحكم فيه بواسطة لوحة "
description: "يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a><span data-ttu-id="cd8d8-103">الإبلاغ عن الانتهاء إلى موقع يتم التحكم فيه بواسطة لوحة </span><span class="sxs-lookup"><span data-stu-id="cd8d8-103">Report as finished to a plate-controlled location</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd8d8-104">يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="cd8d8-105">تُعد سياسة العمل القابلة للتطبيق المتطلب الأساسي لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="cd8d8-106">أظهر دليل المهمة السابقة إعداد سياسة العمل.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="cd8d8-107">يتطلب دليل المهام هذا تطبيق Dynamics AX 7.0.1 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="cd8d8-108">إعداد موقع المخرجات</span><span class="sxs-lookup"><span data-stu-id="cd8d8-108">Set up an output location</span></span>
1. <span data-ttu-id="cd8d8-109">انتقل إلى إدارة المؤسسة > الموارد > مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="cd8d8-110">في القائمة، حدد مجموعة الموارد "5102".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="cd8d8-111">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-111">Click Edit.</span></span>
4. <span data-ttu-id="cd8d8-112">في الحقل "مستودع المخرجات"، أدخل "51".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="cd8d8-113">في الحقل "موقع الإخراج"، أدخل "001".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="cd8d8-114">الموقع 001 غير خاضع للتحكم بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="cd8d8-115">يمكنك إعداد موقع إخراج غير لوحة غير مرخصة فقط في حالة وجود سياسة عمل قابلة للتطبيق للموقع.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="cd8d8-116">إنشاء أمر الإنتاج والإبلاغ عنه كمنته</span><span class="sxs-lookup"><span data-stu-id="cd8d8-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="cd8d8-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-117">Close the page.</span></span>
2. <span data-ttu-id="cd8d8-118">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="cd8d8-119">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-119">Click New production order.</span></span>
4. <span data-ttu-id="cd8d8-120">في الحقل "رقم الصنف"، أدخل "L0101".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="cd8d8-121">انقر فوق إنشاء.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-121">Click Create.</span></span>
6. <span data-ttu-id="cd8d8-122">في جزء الإجراءات، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="cd8d8-123">انقر فوق "تقدير".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-123">Click Estimate.</span></span>
8. <span data-ttu-id="cd8d8-124">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-124">Click OK.</span></span>
9. <span data-ttu-id="cd8d8-125">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-125">Click Start.</span></span>
10. <span data-ttu-id="cd8d8-126">انقر فوق علامة التبويب عام.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-126">Click the General tab.</span></span>
11. <span data-ttu-id="cd8d8-127">في الحقل "‏‫استهلاك قائمة مكونات الصنف التلقائي‬"، حدد "أبدًا".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="cd8d8-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-128">Click OK.</span></span>
13. <span data-ttu-id="cd8d8-129">انقر فوق "الإبلاغ كمنتهٍ".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-129">Click Report as finished.</span></span>
14. <span data-ttu-id="cd8d8-130">انقر فوق علامة التبويب عام.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-130">Click the General tab.</span></span>
15. <span data-ttu-id="cd8d8-131">حدد "نعم" في الحقل "قبول الخطأ".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="cd8d8-132">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-132">Click OK.</span></span>
17. <span data-ttu-id="cd8d8-133">في جزء الإجراءات، انقر فوق "مستودع".</span><span class="sxs-lookup"><span data-stu-id="cd8d8-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="cd8d8-134">انقر فوق تفاصيل العمل.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-134">Click Work details.</span></span>
    * <span data-ttu-id="cd8d8-135">عندما تم الإبلاغ عن أمر الإنتاج كمنته، فإنه لا يتم إنشاء عمل للتخزين.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="cd8d8-136">يحدث هذا لأنه يتم تعريف سياسة عمل تمنع إنشاء العمل عندما يتم الإبلاغ عن المنتج L0101 كمنته للموقع 001.</span><span class="sxs-lookup"><span data-stu-id="cd8d8-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  


