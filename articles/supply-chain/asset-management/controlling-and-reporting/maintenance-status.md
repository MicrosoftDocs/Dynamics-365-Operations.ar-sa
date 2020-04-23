---
title: حالة الصيانة
description: يشرح هذا الموضوع كيفية حساب حالة الصيانة في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fbe2b3fd9ce63c34aedb790583dea572d3d9b079
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205450"
---
# <a name="maintenance-status"></a><span data-ttu-id="b0f05-103">حالة الصيانة</span><span class="sxs-lookup"><span data-stu-id="b0f05-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b0f05-104">في إدارة الأصول، يمكنك إجراء عملية حسابية عامة لفترة زمنية محددة للاطلاع على طلبات الصيانة الجديدة والنشطة والمكتملة وأوامر العمل وأنشطة وقت تعطل الصيانة.</span><span class="sxs-lookup"><span data-stu-id="b0f05-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="b0f05-105">يمكنك أيضًا رؤية عدد تقييمات الحالات المكتملة لنفس الفترة.</span><span class="sxs-lookup"><span data-stu-id="b0f05-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="b0f05-106">استخدم هذه العملية الحسابية للحصول على نظرة عامة حول حمل العمل فيما يتعلق بأوامر العمل وطلبات الصيانة الواردة والمكتملة.</span><span class="sxs-lookup"><span data-stu-id="b0f05-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="b0f05-107">إجراء حساب لحالة الصيانة</span><span class="sxs-lookup"><span data-stu-id="b0f05-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="b0f05-108">انقر فوق **إدارة الأصول** > **استعلامات** > **حالة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="b0f05-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="b0f05-109">في مربع الحوار **حساب الحالة** ، حدد الفترة التي تريد إجراء حساب لها في الحقلين **من تاريخ** و **إلى تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="b0f05-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="b0f05-110">يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود الصيانة فيما يتعلق بمواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="b0f05-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="b0f05-111">على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك بنية موقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة تكاليف أخطاء الأصول لموقع عمل في المستوى العلوي، وبالتالي فإن الحالة على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى.</span><span class="sxs-lookup"><span data-stu-id="b0f05-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="b0f05-112">إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود الصيانة على جميع مستويات مواقع العمل التي ترتبط بها.</span><span class="sxs-lookup"><span data-stu-id="b0f05-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="b0f05-113">انقر فوق **موافق** لبدء الحساب.</span><span class="sxs-lookup"><span data-stu-id="b0f05-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="b0f05-114">انقر على الأزرار **تجميع حسب** لإظهار مستوى التفاصيل المطلوب للحساب.</span><span class="sxs-lookup"><span data-stu-id="b0f05-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="b0f05-115">يتم تمييز أزرار **تجميع حسب** المحددة.</span><span class="sxs-lookup"><span data-stu-id="b0f05-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="b0f05-116">انقر فوق زر لتنشيطه أو إلغاء تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="b0f05-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="b0f05-117">تذكر ضرورة النقر فوق الزر **تحديث** لتحديث الحساب في كل مرة تقوم فيها بإدخال تغييرات عن طريق تنشيط الأزرار **تجميع حسب** أو إلغاء تنشيطها، أو من خلال إجراء حسابات لفترة جديدة.</span><span class="sxs-lookup"><span data-stu-id="b0f05-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="b0f05-118">انقر فوق **الحالة** إذا كنت تريد إنشاء حساب حالة صيانة جديدة.</span><span class="sxs-lookup"><span data-stu-id="b0f05-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="b0f05-119">تتضمن النتائج التي تظهر في **حالة الصيانة** فقط طلبات الصيانة وأوامر العمل التي لها تاريخ ووقت بدء فعليين.</span><span class="sxs-lookup"><span data-stu-id="b0f05-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="b0f05-120">قد يكون تاريخ ووقت الانتهاء فارغين.</span><span class="sxs-lookup"><span data-stu-id="b0f05-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="b0f05-121">مثال1</span><span class="sxs-lookup"><span data-stu-id="b0f05-121">Example 1</span></span>

<span data-ttu-id="b0f05-122">في لقطة الشاشة أدناه، تم تنشيط الزرين **السنة** و **الشهر**.</span><span class="sxs-lookup"><span data-stu-id="b0f05-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="b0f05-123">من خلال الخيارات **تجميع حسب** المحددة، يمكنك الحصول على نظرة عامة على أساس شهري لحمل العمل والإنتاجية المرتبطة بطلبات الصيانة وأوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="b0f05-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![مثال علي حمل العمل الشهري](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="b0f05-125">مثال2</span><span class="sxs-lookup"><span data-stu-id="b0f05-125">Example 2</span></span>

<span data-ttu-id="b0f05-126">في لقطة الشاشة أدناه، تمت إضافة معلومات حول مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="b0f05-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="b0f05-127">يمكنك الآن مقارنة حمل العمل والإنتاجية عبر مواقع العمل، التي قد تمثل مواقع جغرافية أو مصانع أو مناطق عمل.</span><span class="sxs-lookup"><span data-stu-id="b0f05-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![مثال علي حمل العمل الشهري مع مواقع العمل](media/14-controlling-and-reporting.png)

