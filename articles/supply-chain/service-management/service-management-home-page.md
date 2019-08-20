---
title: إدارة الخدمة
description: استخدم إدارة الخدمة لإنشاء اشتراكات الخدمة واتفاقيات الخدمة، والتعامل مع أوامر الخدمة واستفسارات العملاء، ولإدارة وتحليل تقديم الخدمات للعملاء.
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2fc5361b1b30db29789ff67b56a15eb66a919f5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843279"
---
# <a name="service-management"></a><span data-ttu-id="ca52f-103">إدارة الخدمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ca52f-104">استخدم **إدارة الخدمة** لإنشاء اشتراكات الخدمة واتفاقيات الخدمة، والتعامل مع أوامر الخدمة واستفسارات العملاء، ولإدارة وتحليل تقديم الخدمات للعملاء.</span><span class="sxs-lookup"><span data-stu-id="ca52f-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="ca52f-105">يمكنك استخدام اتفاقيات الخدمة لتعريف الموارد التي يتم استخدامها في زيارة خدمة عادية.</span><span class="sxs-lookup"><span data-stu-id="ca52f-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="ca52f-106">يمكنك أيضا استخدام اتفاقيات الخدمة لعرض كيفية فوترة هذه المصادر إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="ca52f-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="ca52f-107">يمكن لاتفاقية خدمة أن تتضمن اتفاقية مستوى خدمة تحدد أوقات الاستجابة القياسية، وتقدم أدوات لتسجيل الوقت الفعلي.</span><span class="sxs-lookup"><span data-stu-id="ca52f-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="ca52f-108">يمكنك إنشاء أوامر الخدمة لإدارة معلومات حول الزيارات المجدولة وغير المجدولة التي يقوم بها فَنِّي الخدمة إلى موقع أحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="ca52f-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="ca52f-109">أوامر الخدمة تتضمن معلومات مثل:</span><span class="sxs-lookup"><span data-stu-id="ca52f-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="ca52f-110">ساعات العمل التي سيجريها فني الخدمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="ca52f-111">نوع الخدمة أو الإصلاح</span><span class="sxs-lookup"><span data-stu-id="ca52f-111">The type of service or repair</span></span>

3.  <span data-ttu-id="ca52f-112">الصنف الذي سيتم إصلاحه، بما في ذلك تفاصيل حول الأعراض والتشخيص</span><span class="sxs-lookup"><span data-stu-id="ca52f-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="ca52f-113">النفقات والرسوم المتعلقة بالخدمة أو الإصلاح</span><span class="sxs-lookup"><span data-stu-id="ca52f-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="ca52f-114">يمكنك تلقي ومعالجة وإرسال طلبات الخدمة.</span><span class="sxs-lookup"><span data-stu-id="ca52f-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="ca52f-115">بعد إنشاء أمر خدمة، يمكنك استخدام مراحل الخدمة لرصد التقدم المحرز وتحديد القواعد التي تتحكم في الإجراءات التي تم تمكينها في كل مرحلة.</span><span class="sxs-lookup"><span data-stu-id="ca52f-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="ca52f-116">عند اكتمال أمر خدمة، يمكنك تسجيل الخروج عن الأمر للتأكد من أنه كامل ثم ترحيل الأمر لبدء عملية الفوترة.</span><span class="sxs-lookup"><span data-stu-id="ca52f-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="ca52f-117">استخدام أدوات إعداد التقارير لمراقبة هوامش أمر الخدمة وحركات الاشتراك ووصف أعمال الطباعة وإيصالات العمل.</span><span class="sxs-lookup"><span data-stu-id="ca52f-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="ca52f-118">‏‏العمليات التجارية</span><span class="sxs-lookup"><span data-stu-id="ca52f-118">Business processes</span></span>

<span data-ttu-id="ca52f-119">يوضح الرسم التخطيطي التالي العمليات التجارية عالية المستوى في **إدارة الخدمة‬**، ويُظهر أماكن تكامل عمليات الخدمة مع وحدات أخرى في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ca52f-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ca52f-120">[![مخطط العمليات التجارية لإدارة الخدمات](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="ca52f-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="ca52f-121">إدارة خدمة في لمحة</span><span class="sxs-lookup"><span data-stu-id="ca52f-121">Service management at a glance</span></span>

|<span data-ttu-id="ca52f-122">مهام مهمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-122">Important tasks</span></span>           | <span data-ttu-id="ca52f-123">الصفحات الأساسية</span><span class="sxs-lookup"><span data-stu-id="ca52f-123">Primary pages</span></span>                         |<span data-ttu-id="ca52f-124">تقارير شائعة</span><span class="sxs-lookup"><span data-stu-id="ca52f-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="ca52f-125">الوفاء باتفاقيات الخدمات</span><span class="sxs-lookup"><span data-stu-id="ca52f-125">Fulfill service agreements</span></span>|<span data-ttu-id="ca52f-126">اتفاقيات الخدمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-126">Service agreements</span></span>                     |<span data-ttu-id="ca52f-127">هامش أمر الخدمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-127">Service order margin</span></span>         |
|<span data-ttu-id="ca52f-128">التعامل مع استعلامات العميل</span><span class="sxs-lookup"><span data-stu-id="ca52f-128">Handle customer inquiries</span></span> |<span data-ttu-id="ca52f-129">أوامر الخدمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-129">Service orders</span></span>                         |<span data-ttu-id="ca52f-130">وصف العمل</span><span class="sxs-lookup"><span data-stu-id="ca52f-130">Work description</span></span>             |
|                          |<span data-ttu-id="ca52f-131">لوحة الإرسال</span><span class="sxs-lookup"><span data-stu-id="ca52f-131">Dispatch board</span></span>                         |<span data-ttu-id="ca52f-132">الحركة - الاشتراك</span><span class="sxs-lookup"><span data-stu-id="ca52f-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="ca52f-133">حركات رسوم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="ca52f-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="ca52f-134">دمج إدارة خدمة</span><span class="sxs-lookup"><span data-stu-id="ca52f-134">Integration of Service management</span></span>

<span data-ttu-id="ca52f-135">إدارة خدمة يمكن أن تتكامل مع الوحدات النمطية التالية:</span><span class="sxs-lookup"><span data-stu-id="ca52f-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="ca52f-136">المبيعات والتسويق</span><span class="sxs-lookup"><span data-stu-id="ca52f-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="ca52f-137">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="ca52f-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

