---
title: الإبلاغ كمنتهي بموقع غير خاضع للتحكم بواسطة لوحة الترخيص (استمارة تقديم، أيار/مايو 2016)
description: يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e96267a80160a63258b97f2e6ac49fad753a93a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148896"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="ef4cc-103">الإبلاغ كمنتهي بموقع غير خاضع للتحكم بواسطة لوحة الترخيص (استمارة تقديم، أيار/مايو 2016)</span><span class="sxs-lookup"><span data-stu-id="ef4cc-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef4cc-104">يبين دليل المهام هذا مثالاً للإبلاغ كمنته إلى موقع غير خاضع للتحكم بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="ef4cc-105">تُعد سياسة العمل القابلة للتطبيق المتطلب الأساسي لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="ef4cc-106">أظهر دليل المهمة السابقة إعداد سياسة العمل.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="ef4cc-107">يتطلب دليل المهام هذا الإصدار 7.0.1 أو أحدث من تطبيق Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="ef4cc-108">إعداد موقع المخرجات</span><span class="sxs-lookup"><span data-stu-id="ef4cc-108">Set up an output location</span></span>
1. <span data-ttu-id="ef4cc-109">انتقل إلى إدارة المؤسسة > الموارد > مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="ef4cc-110">في القائمة، حدد مجموعة الموارد "5102".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="ef4cc-111">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-111">Click Edit.</span></span>
4. <span data-ttu-id="ef4cc-112">في الحقل "مستودع المخرجات"، أدخل "51".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="ef4cc-113">في الحقل "موقع الإخراج"، أدخل "001".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="ef4cc-114">الموقع 001 غير خاضع للتحكم بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="ef4cc-115">يمكنك إعداد موقع إخراج غير لوحة غير مرخصة فقط في حالة وجود سياسة عمل قابلة للتطبيق للموقع.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="ef4cc-116">إنشاء أمر الإنتاج والإبلاغ عنه كمنته</span><span class="sxs-lookup"><span data-stu-id="ef4cc-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="ef4cc-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-117">Close the page.</span></span>
2. <span data-ttu-id="ef4cc-118">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="ef4cc-119">انقر فوق "أمر إنتاج جديد".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-119">Click New production order.</span></span>
4. <span data-ttu-id="ef4cc-120">في الحقل "رقم الصنف"، أدخل "L0101".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="ef4cc-121">انقر فوق إنشاء.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-121">Click Create.</span></span>
6. <span data-ttu-id="ef4cc-122">في جزء الإجراءات، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="ef4cc-123">انقر فوق "تقدير".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-123">Click Estimate.</span></span>
8. <span data-ttu-id="ef4cc-124">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-124">Click OK.</span></span>
9. <span data-ttu-id="ef4cc-125">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-125">Click Start.</span></span>
10. <span data-ttu-id="ef4cc-126">انقر فوق علامة التبويب عام.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-126">Click the General tab.</span></span>
11. <span data-ttu-id="ef4cc-127">في الحقل "‏‫استهلاك قائمة مكونات الصنف التلقائي‬"، حدد "أبدًا".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="ef4cc-128">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-128">Click OK.</span></span>
13. <span data-ttu-id="ef4cc-129">انقر فوق "الإبلاغ كمنتهٍ".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-129">Click Report as finished.</span></span>
14. <span data-ttu-id="ef4cc-130">انقر فوق علامة التبويب عام.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-130">Click the General tab.</span></span>
15. <span data-ttu-id="ef4cc-131">حدد "نعم" في الحقل "قبول الخطأ".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="ef4cc-132">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-132">Click OK.</span></span>
17. <span data-ttu-id="ef4cc-133">في جزء الإجراءات، انقر فوق "مستودع".</span><span class="sxs-lookup"><span data-stu-id="ef4cc-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="ef4cc-134">انقر فوق تفاصيل العمل.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-134">Click Work details.</span></span>
    * <span data-ttu-id="ef4cc-135">عندما تم الإبلاغ عن أمر الإنتاج كمنته، فإنه لا يتم إنشاء عمل للتخزين.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="ef4cc-136">يحدث هذا لأنه يتم تعريف سياسة عمل تمنع إنشاء العمل عندما يتم الإبلاغ عن المنتج L0101 كمنته للموقع 001.</span><span class="sxs-lookup"><span data-stu-id="ef4cc-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

