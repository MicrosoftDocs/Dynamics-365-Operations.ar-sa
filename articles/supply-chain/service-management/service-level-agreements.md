---
title: نظرة عامة على اتفاقيات مستوى الخدمة
description: في اتفاقية مستوى الخدمة، يوافق العميل على أدنى وقت للاستجابة استنادًا إلى الوقت الذي تقوم فيه شركة الخدمة بتسجيل المشكلة ومتى تم حل المشكلة.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b06e537b010b6b32799f76964cb85af892bc3f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216127"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="a9523-103">نظرة عامة على اتفاقيات مستوى الخدمة</span><span class="sxs-lookup"><span data-stu-id="a9523-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a9523-104">اتفاقية مستوى الخدمة (SLA) هي عبارة عن اتفاقية بين شركة خدمة وعميل خدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="a9523-105">في اتفاقية مستوى الخدمة، يوافق العميل على أدنى وقت للاستجابة استنادًا إلى الوقت الذي تقوم فيه شركة الخدمة بتسجيل المشكلة ومتى تم حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="a9523-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="a9523-106">تطبق اتفاقية مستوى الخدمة أسلوبًا قياسيًا للخدمةالمقدمة للعملاء، كما توضح لشركة الخدمة متى ينبغي إكمال إحدى مهام الخدمات.</span><span class="sxs-lookup"><span data-stu-id="a9523-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="a9523-107">ويمكن إنشاء أي عدد من اتفاقيات مستوى الخدمة وذلك لتوفير مستويات مختلفة من الخدمة لعميل الخدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="a9523-108">إنشاء اتفاقية مستوى الخدمة</span><span class="sxs-lookup"><span data-stu-id="a9523-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="a9523-109">انقر فوق **إدارة الخدمة** \> **الإعداد** \> **اتفاقيات الخدمة** \> **اتفاقيات مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="a9523-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="a9523-110">اكتب اسم اتفاقية مستوى الخدمة في الحقل **اتفاقية مستوى الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="a9523-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="a9523-111">اكتب الوقت الذي تريد فيه السماح بإكمال استدعاءات الخدمة المرفقة باتفاقية مستوى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="a9523-112">ثم حدد تقويماً إذا كنت ترغب في أن تستند اتفاقية مستوى الخدمة إلى تقويم معين.</span><span class="sxs-lookup"><span data-stu-id="a9523-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="a9523-113">تطبيق اتفاقية مستوى الخدمة</span><span class="sxs-lookup"><span data-stu-id="a9523-113">Apply a service level agreement</span></span>

<span data-ttu-id="a9523-114">يتم تطبيق اتفاقية مستوى الخدمة مباشرة على اتفاقية خدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="a9523-115">يتم قياس أوامر الخدمة التي يتم إنشاؤها يدويًا وإرفاقها باتفاقية خدمة تتضمن اتفاقية مستوى خدمة مقابل اتفاقية مستوى الخدمة تلك.</span><span class="sxs-lookup"><span data-stu-id="a9523-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="a9523-116">لا يتم إرفاق أوامر الخدمة التي يتم إنشاؤها تلقائيًا باتفاقية مستوى خدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="a9523-117">تطبيق اتفاقية مستوى الخدمة على اتفاقية الخدمة</span><span class="sxs-lookup"><span data-stu-id="a9523-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="a9523-118">انقر فوق **إدارة الخدمة** \> **عام** \> **اتفاقيات الخدمة‬** \> **اتفاقيات الخدمة‬**.</span><span class="sxs-lookup"><span data-stu-id="a9523-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="a9523-119">حدد اتفاقية الخدمة التي ترغب في تطبيق اتفاقية مستوى الخدمة عليها، ثم انقر فوق **تحرير** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="a9523-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="a9523-120">في حقل **اتفاقية مستوى الخدمة**، حدد اتفاقية مستوى الخدمة التي تريد تعيينها.</span><span class="sxs-lookup"><span data-stu-id="a9523-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="a9523-121">تطبيق اتفاقية مستوى الخدمة على ‏‏مجموعة اتفاقيات الخدمات</span><span class="sxs-lookup"><span data-stu-id="a9523-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="a9523-122">انقر فوق **إدارة الخدمة** \> **الإعداد** \> **اتفاقيات الخدمة** \> **مجموعات اتفاقيات الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="a9523-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="a9523-123">في حقل **اتفاقية مستوى الخدمة**، حدد اتفاقية مستوى الخدمة التي تريد تعيينها.</span><span class="sxs-lookup"><span data-stu-id="a9523-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="a9523-124">تتبع الوقت في أمر خدمة مقابل اتفاقية مستوى خدمة</span><span class="sxs-lookup"><span data-stu-id="a9523-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="a9523-125">عند إنشاء أمر خدمة جديد لاتفاقية خدمة تم تعيين اتفاقية مستوى خدمة إليها، يتم بدء الفترة الزمنية لتسليم الخدمة، ويبدأ النظام في تعقب وقت التسليم.</span><span class="sxs-lookup"><span data-stu-id="a9523-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="a9523-126">فضلاً عن ذلك، يمكن تعيين الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="a9523-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="a9523-127">يمكن تشغيل تسجيل الوقت وإيقافه في أمر الخدمة وذلك لتسجيل إجمالي الوقت المستغرق في أوامر الخدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="a9523-128">يمكن مراقبة الالتزام بالفاصل الزمني الذي تم تعيينه في اتفاقية مستوى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="a9523-129">يمكن تحديد أكواد السبب التي يلزم تعيينها في حالة تجاوز الفاصل الزمني المحدد باتفاقية مستوى الخدمة.</span><span class="sxs-lookup"><span data-stu-id="a9523-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9523-130">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="a9523-130">See also</span></span>

[<span data-ttu-id="a9523-131">عرض التوافق مع اتفاقيات مستوى الخدمة</span><span class="sxs-lookup"><span data-stu-id="a9523-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


