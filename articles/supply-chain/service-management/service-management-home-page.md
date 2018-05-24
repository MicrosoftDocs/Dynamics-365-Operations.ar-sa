---
title: "إدارة الخدمة"
description: "استخدم إدارة الخدمة لإنشاء اشتراكات الخدمة واتفاقيات الخدمة، والتعامل مع أوامر الخدمة واستفسارات العملاء، ولإدارة وتحليل تقديم الخدمات للعملاء."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: ar-sa
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="34a87-103">إدارة الخدمة</span><span class="sxs-lookup"><span data-stu-id="34a87-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="34a87-104">استخدم **إدارة الخدمة** لإنشاء اشتراكات الخدمة واتفاقيات الخدمة، والتعامل مع أوامر الخدمة واستفسارات العملاء، ولإدارة وتحليل تقديم الخدمات للعملاء.</span><span class="sxs-lookup"><span data-stu-id="34a87-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="34a87-105">يمكنك استخدام اتفاقيات الخدمة لتعريف الموارد التي يتم استخدامها في زيارة خدمة عادية.</span><span class="sxs-lookup"><span data-stu-id="34a87-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="34a87-106">يمكنك أيضا استخدام اتفاقيات الخدمة لعرض كيفية فوترة هذه المصادر إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="34a87-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="34a87-107">يمكن لاتفاقية خدمة أن تتضمن اتفاقية مستوى خدمة تحدد أوقات الاستجابة القياسية، وتقدم أدوات لتسجيل الوقت الفعلي.</span><span class="sxs-lookup"><span data-stu-id="34a87-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="34a87-108">يمكنك إنشاء أوامر الخدمة لإدارة معلومات حول الزيارات المجدولة وغير المجدولة التي يقوم بها فَنِّي الخدمة إلى موقع أحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="34a87-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="34a87-109">أوامر الخدمة تتضمن معلومات مثل:</span><span class="sxs-lookup"><span data-stu-id="34a87-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="34a87-110">ساعات العمل التي سيجريها فني الخدمة</span><span class="sxs-lookup"><span data-stu-id="34a87-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="34a87-111">نوع الخدمة أو الإصلاح</span><span class="sxs-lookup"><span data-stu-id="34a87-111">The type of service or repair</span></span>

3.  <span data-ttu-id="34a87-112">الصنف الذي سيتم إصلاحه، بما في ذلك تفاصيل حول الأعراض والتشخيص</span><span class="sxs-lookup"><span data-stu-id="34a87-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="34a87-113">النفقات والرسوم المتعلقة بالخدمة أو الإصلاح</span><span class="sxs-lookup"><span data-stu-id="34a87-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="34a87-114">يمكن للعملاء إرسال طلبات الخدمة عبر الإنترنت باستخدام مدخل الشركة على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="34a87-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="34a87-115">يمكنك تلقي ومعالجة وإرسال هذه الطلبات.</span><span class="sxs-lookup"><span data-stu-id="34a87-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="34a87-116">بعد إنشاء أمر خدمة، يمكنك استخدام مراحل الخدمة لرصد التقدم المحرز وتحديد القواعد التي تتحكم في الإجراءات التي تم تمكينها في كل مرحلة.</span><span class="sxs-lookup"><span data-stu-id="34a87-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="34a87-117">عند اكتمال أمر خدمة، يمكنك تسجيل الخروج عن الأمر للتأكد من أنه كامل ثم ترحيل الأمر لبدء عملية الفوترة.</span><span class="sxs-lookup"><span data-stu-id="34a87-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="34a87-118">استخدام أدوات إعداد التقارير لمراقبة هوامش أمر الخدمة وحركات الاشتراك ووصف أعمال الطباعة وإيصالات العمل.</span><span class="sxs-lookup"><span data-stu-id="34a87-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="34a87-119">‏‏العمليات التجارية</span><span class="sxs-lookup"><span data-stu-id="34a87-119">Business processes</span></span>

<span data-ttu-id="34a87-120">يوضح المخطط التالي العمليات التجارية عالية المستوى لـ **إدارة الخدمة**، ويظهر أين تتكامل عمليات خدمة مع الوحدات النمطية الأخرى في Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="34a87-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="34a87-121">[![مخطط العمليات التجارية لإدارة الخدمات](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="34a87-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="34a87-122">إدارة خدمة في لمحة</span><span class="sxs-lookup"><span data-stu-id="34a87-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="34a87-123">مهام مهمة</span><span class="sxs-lookup"><span data-stu-id="34a87-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="34a87-124">النماذج الأولية</span><span class="sxs-lookup"><span data-stu-id="34a87-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="34a87-125">تقارير شائعة</span><span class="sxs-lookup"><span data-stu-id="34a87-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34a87-126">الوفاء باتفاقيات الخدمات</span><span class="sxs-lookup"><span data-stu-id="34a87-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="34a87-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">اتفاقيات الخدمات (نموذج)</a></span><span class="sxs-lookup"><span data-stu-id="34a87-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="34a87-128"><strong>هامش أمر الخدمة</strong></span><span class="sxs-lookup"><span data-stu-id="34a87-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34a87-129">التعامل مع استعلامات العميل</span><span class="sxs-lookup"><span data-stu-id="34a87-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="34a87-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">أوامر الخدمة (نموذج)</a></span><span class="sxs-lookup"><span data-stu-id="34a87-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="34a87-131"><strong>وصف العمل</strong></span><span class="sxs-lookup"><span data-stu-id="34a87-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="34a87-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">‏‏لوحة الإرسال (نموذج)</a></span><span class="sxs-lookup"><span data-stu-id="34a87-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="34a87-133"><strong>الحركة - الاشتراك</strong></span><span class="sxs-lookup"><span data-stu-id="34a87-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="34a87-134"><strong>حركات رسوم الاشتراك</strong></span><span class="sxs-lookup"><span data-stu-id="34a87-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="34a87-135">دمج إدارة خدمة</span><span class="sxs-lookup"><span data-stu-id="34a87-135">Integration of Service management</span></span>

<span data-ttu-id="34a87-136">يمكن أن تتكامل إداة الخدمات مع الوحدات النمطية التالية في Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="34a87-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="34a87-137">المبيعات والتسويق</span><span class="sxs-lookup"><span data-stu-id="34a87-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="34a87-138">الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="34a87-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


