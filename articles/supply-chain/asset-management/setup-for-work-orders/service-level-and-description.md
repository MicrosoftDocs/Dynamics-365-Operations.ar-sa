---
title: مستوى الخدمة ووصفها
description: يشرح هذا الموضوع مستوى الخدمة ووصفها في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 647358fcdd53ba95b571185ae269bc8d6b869c18
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421419"
---
# <a name="service-level-and-description"></a><span data-ttu-id="c4358-103">مستوى الخدمة ووصفها</span><span class="sxs-lookup"><span data-stu-id="c4358-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c4358-104">عند إنشاء أمر عمل، قد ترغب في تحديد مستويات الخدمة له وإضافة وصف عام له.</span><span class="sxs-lookup"><span data-stu-id="c4358-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="c4358-105">يمكنك إنشاء مستويات خدمة أمر العمل في الصفحة **مستويات خدمة أمر العمل** وإضافة الأوصاف في صفحة **وصف أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="c4358-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="c4358-106">إنشاء مستوى خدمة</span><span class="sxs-lookup"><span data-stu-id="c4358-106">Create a service level</span></span>

1. <span data-ttu-id="c4358-107">حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="c4358-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="c4358-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c4358-108">Select **New**.</span></span>
3. <span data-ttu-id="c4358-109">في الحقل **مستوى الخدمة**، أدخل مستوى الخدمة (على سبيل المثال، رقم).</span><span class="sxs-lookup"><span data-stu-id="c4358-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="c4358-110">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="c4358-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="c4358-111">على علامة التبويب السريعة **أوامر العمل**، يمكنك تحديد تواريخ وأوقات البدء والانتهاء المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="c4358-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="c4358-112">تحدد الحقول الموجودة على علامة التبويب السريعة الفترة التي يجب بدء وانتهاء أوامر العمل فيها.</span><span class="sxs-lookup"><span data-stu-id="c4358-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="c4358-113">وتُستخدم لأوامر العمل التي يتم إنشاؤها يدويًا وأوامر العمل التي يتم إنشاؤها بناءً على طلبات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="c4358-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="c4358-114">في الحقل **يوم البدء**، أدخل عدد الأيام لتحديد الفترة التي يجب أن يبدأ خلالها أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="c4358-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="c4358-115">يتم حساب عدد الأيام من تاريخ إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="c4358-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="c4358-116">على سبيل المثال، إذا كان يجب بدء أمر العمل عند إنشائه، أدخل **0**.</span><span class="sxs-lookup"><span data-stu-id="c4358-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="c4358-117">إذا كان يجب بدء أمر العمل في خلال أسبوع من إنشائه، أدخل **7**.</span><span class="sxs-lookup"><span data-stu-id="c4358-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="c4358-118">لتعيين وقت بدء أمر العمل، بالإضافة إلى تاريخ بدء، قم بتعيين الخيار **تعيين وقت البدء** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c4358-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="c4358-119">ثم ادخل وقت البدء في الحقل **وقت البدء**.</span><span class="sxs-lookup"><span data-stu-id="c4358-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="c4358-120">عند تعيين الخيار إلى **لا**، يتم استخدام الوقت الحالي من اليوم.</span><span class="sxs-lookup"><span data-stu-id="c4358-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="c4358-121">في الحقل **يوم الانتهاء**، أدخل عدد الأيام لتحديد الفترة التي يجب أن ينتهي خلالها أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="c4358-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="c4358-122">يتم حساب عدد الأيام من تاريخ بدء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="c4358-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="c4358-123">على سبيل المثال، إذا كان من المفترض أن ينتهي أمر العمل في خلال أسبوع من تاريخ بدئه، فأدخل **7**.</span><span class="sxs-lookup"><span data-stu-id="c4358-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="c4358-124">لتعيين وقت انتهاء أمر العمل، بالإضافة إلى تاريخ انتهاء، قم بتعيين الخيار **تعيين وقت انتهاء** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c4358-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="c4358-125">ثم ادخل وقت الانتهاء في الحقل **وقت الانتهاء**.</span><span class="sxs-lookup"><span data-stu-id="c4358-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="c4358-126">عند تعيين الخيار إلى **لا**، يتم استخدام الوقت الحالي من اليوم.</span><span class="sxs-lookup"><span data-stu-id="c4358-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="c4358-127">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c4358-127">Select **Save**.</span></span>

![صفحة مستوى خدمة أوامر العمل](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="c4358-129">إنشاء وصف</span><span class="sxs-lookup"><span data-stu-id="c4358-129">Create a description</span></span>

1. <span data-ttu-id="c4358-130">حدد **إدارة الأصول** \> **الإعداد** \> **أوامر العمل** \> **الأوصاف**.</span><span class="sxs-lookup"><span data-stu-id="c4358-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="c4358-131">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c4358-131">Select **New**.</span></span>
3. <span data-ttu-id="c4358-132">في الحقل **الوصف**، أدخل الوصف.</span><span class="sxs-lookup"><span data-stu-id="c4358-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="c4358-133">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="c4358-133">Select **Save**.</span></span>
