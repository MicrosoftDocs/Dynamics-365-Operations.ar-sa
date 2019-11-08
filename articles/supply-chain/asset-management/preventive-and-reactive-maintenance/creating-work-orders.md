---
title: إنشاء أوامر العمل
description: يوضح هذا الموضوع كيفية إنشاء أوامر العمل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e910b2400106baf9f9dc06f6bc0d3daee8e4a43
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570066"
---
# <a name="creating-work-orders"></a><span data-ttu-id="7205e-103">إنشاء أوامر العمل</span><span class="sxs-lookup"><span data-stu-id="7205e-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7205e-104">عندما تنتهي من جدولة مهام الصيانة الوقائية، فإن الخطوة التالية هي إنشاء أوامر عمل للمهام.</span><span class="sxs-lookup"><span data-stu-id="7205e-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="7205e-105">ويتم ذلك في أحد جداول الصيانة.</span><span class="sxs-lookup"><span data-stu-id="7205e-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="7205e-106">قد تتوفر أنواع مراجع مختلفة للمهام المجدولة في جدول صيانة:</span><span class="sxs-lookup"><span data-stu-id="7205e-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="7205e-107">نوع المرجع</span><span class="sxs-lookup"><span data-stu-id="7205e-107">Reference type</span></span> | <span data-ttu-id="7205e-108">الوصف</span><span class="sxs-lookup"><span data-stu-id="7205e-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7205e-109">خطط الصيانة</span><span class="sxs-lookup"><span data-stu-id="7205e-109">Maintenance plans</span></span>     | <span data-ttu-id="7205e-110">مهام الصيانة الوقائية التي تعتمد على أنواع خطط الصيانة "الوقت" أو "العداد".</span><span class="sxs-lookup"><span data-stu-id="7205e-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="7205e-111">دورات الصيانة</span><span class="sxs-lookup"><span data-stu-id="7205e-111">Maintenance rounds</span></span>    | <span data-ttu-id="7205e-112">مهام الصيانة الوقائية التي تحتوي على عدد كبير من الأصول التي تحتاج إلى نوع صيانة مماثل.</span><span class="sxs-lookup"><span data-stu-id="7205e-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="7205e-113">طلب الصيانة</span><span class="sxs-lookup"><span data-stu-id="7205e-113">Maintenance request</span></span>   | <span data-ttu-id="7205e-114">طلب تم إنشاؤه يدويًا لصيانة أصل أو إصلاحه، يمكن تحويله إلى أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="7205e-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="7205e-115">انقر فوق **إدارة الأصول** > **عام‏‎‏‎** > **جدول الصيانة بكامله** أو **بنود جدول الصيانة المفتوحة** أو **مجموعات جداول الصيانة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="7205e-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="7205e-116">حدد مهام الصيانة المجدولة التي تريد إنشاء أمر عمل لها، ثم انقر فوق **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="7205e-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="7205e-117">في مربع الحوار **إنشاء أوامر عمل**، يظهر العدد الإجمالي لساعات التنبؤ للبنود المحددة في الحقل **ساعات التنبؤ بمتطلبات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="7205e-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="7205e-118">في قسم **المعلمات**، حدد عدد أوامر العمل التي يجب إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="7205e-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="7205e-119">يمكنك إنشاء أمر عمل واحد لكل بند من بنود جدول الصيانة، أو عدد من أوامر العمل التي تستند إلى تحديداتك في قسم **أمر عمل واحد لكل**.</span><span class="sxs-lookup"><span data-stu-id="7205e-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="7205e-120">حدد **نوع أمر العمل** الذي سيتم استخدامه في كافة أوامر العمل التي تقوم بإنشائها.</span><span class="sxs-lookup"><span data-stu-id="7205e-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="7205e-121">يبين الرسم التوضيحي التالي مثالاً لمربع الحوار **إنشاء أوامر عمل**.</span><span class="sxs-lookup"><span data-stu-id="7205e-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![الشكل 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="7205e-123">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7205e-123">Click **OK**.</span></span> <span data-ttu-id="7205e-124">يتم إنشاء أمر عمل واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="7205e-124">One or more work orders are created.</span></span>

