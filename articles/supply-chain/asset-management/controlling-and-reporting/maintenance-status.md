---
title: حالة الصيانة
description: يشرح هذا الموضوع كيفية حساب حالة الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918339"
---
# <a name="maintenance-status"></a><span data-ttu-id="25b47-103">حالة الصيانة</span><span class="sxs-lookup"><span data-stu-id="25b47-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="25b47-104">في إدارة الأصول، يمكنك إجراء عملية حسابية للاطلاع على نظرة عامة حول طلبات الصيانة الجديدة والنشطة والمكتملة وأوامر العمل وأنشطة وقت تعطل الصيانة لفترة محدده.</span><span class="sxs-lookup"><span data-stu-id="25b47-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="25b47-105">يمكنك أيضًا رؤية عدد تقييمات الحالات المكتملة لنفس الفترة.</span><span class="sxs-lookup"><span data-stu-id="25b47-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="25b47-106">استخدم هذه العملية الحسابية للحصول على نظرة عامة حول حمل العمل فيما يتعلق بأوامر العمل وطلبات الصيانة الواردة والمكتملة.</span><span class="sxs-lookup"><span data-stu-id="25b47-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="25b47-107">إجراء حساب لحالة الصيانة</span><span class="sxs-lookup"><span data-stu-id="25b47-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="25b47-108">انقر فوق **إدارة الأصول** > **استعلامات** > **حالة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="25b47-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="25b47-109">في مربع الحوار ‏‎**حساب الحالة**، حدد الفترة التي تريد إجراء حساب لها في الحقلين **من تاريخ** و**إلى تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="25b47-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="25b47-110">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود الصيانة فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="25b47-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="25b47-111">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة تكاليف أخطاء الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الحالة على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="25b47-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="25b47-112">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود الصيانة على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="25b47-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="25b47-113">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="25b47-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="25b47-114">في مجموعات جزء الإجراءات **تجميع حسب...**، انقر فوق الأزرار ذات الصلة لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="25b47-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="25b47-115">يتم تمييز أزرار جزء الإجراءات المحددة.</span><span class="sxs-lookup"><span data-stu-id="25b47-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="25b47-116">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="25b47-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="25b47-117">تذكر ضرورة النقر فوق الزر **تحديث** لتحديث الحساب في كل مرة تقوم فيها بإدخال تغييرات عن طريق تنشيط الأزرار **تجميع حسب** أو إلغاء تنشيطها لفترة جديدة.</span><span class="sxs-lookup"><span data-stu-id="25b47-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="25b47-118">انقر فوق **الحالة** إذا كنت تريد إنشاء حساب حالة صيانة جديدة.</span><span class="sxs-lookup"><span data-stu-id="25b47-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="25b47-119">تتضمن النتائج التي تظهر في **حالة الصيانة** فقط طلبات الصيانة وأوامر العمل التي لها تاريخ ووقت بدء فعليين.</span><span class="sxs-lookup"><span data-stu-id="25b47-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="25b47-120">قد يكون تاريخ ووقت الانتهاء فارغين.</span><span class="sxs-lookup"><span data-stu-id="25b47-120">End date and time may be blank.</span></span>

<span data-ttu-id="25b47-121">*المثال 1:*</span><span class="sxs-lookup"><span data-stu-id="25b47-121">*Example 1:*</span></span>

<span data-ttu-id="25b47-122">في الشكل أدناه، تم تنشيط الزرين **السنة** و**الشهر**.</span><span class="sxs-lookup"><span data-stu-id="25b47-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="25b47-123">هنا، يمكنك الحصول على نظرة عامة على الأساس الشهري لحمل العمل والإنتاجية المرتبطة بطلبات الصيانة وأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="25b47-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![الشكل 1](media/13-controlling-and-reporting.png)

<span data-ttu-id="25b47-125">*المثال 2:*</span><span class="sxs-lookup"><span data-stu-id="25b47-125">*Example 2:*</span></span>

<span data-ttu-id="25b47-126">في الشكل أدناه، تمت إضافة معلومات حول مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="25b47-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="25b47-127">يمكنك الآن مقارنة حمل العمل والإنتاجية عبر مواقع العمل، التي قد تمثل مواقع جغرافية أو مصانع أو مناطق عمل.</span><span class="sxs-lookup"><span data-stu-id="25b47-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![الشكل 2](media/14-controlling-and-reporting.png)

