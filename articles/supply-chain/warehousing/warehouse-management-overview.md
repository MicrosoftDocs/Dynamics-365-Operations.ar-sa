---
title: نظرة عامة على إدارة المستودعات
description: استخدام إدارة المستودع لمراقبة وجعل عمليات المستودع تلقائية.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c900ef715b62484c1fb6576b7f0c97cdea4e4284
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865126"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="45d37-103">نظرة عامة على إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="45d37-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45d37-104">تسمح الوحدة النمطية "إدارة المستودعات" في Dynamics 365 for Finance and Operations بإدارة عمليات المستودعات في مجالات التصنيع والتوزيع وشركات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="45d37-104">The Warehouse management module for Dynamics 365 for Finance and Operations lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="45d37-105">تحتوي هذه الميزة على نطاق واسع من الميزات لدعم منشأة المستودع على المستوى الأمثل، في أي وقت.</span><span class="sxs-lookup"><span data-stu-id="45d37-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="45d37-106">تتكامل إدارة المستودعات بشكل تام مع العمليات التجارية الأخرى في Finance and Operations مثل النقل والتصنيع ومراقبة الجودة والشراء والتحويل والمبيعات والمرتجعات.</span><span class="sxs-lookup"><span data-stu-id="45d37-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="45d37-107">بدء الاستخدام</span><span class="sxs-lookup"><span data-stu-id="45d37-107">Get started</span></span>
<span data-ttu-id="45d37-108">للشروع في العمل مع إدارة المستودعات، يجب عليك إكمال عملية إعداد محددات المستودعات العامة لدعم العمليات التجارية لشركتك.</span><span class="sxs-lookup"><span data-stu-id="45d37-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="45d37-109">انتقل إلى الصفحة **محددات إدارة المستودعات** ضمن **إدارة المستودعات** > **الإعداد** لإعداد محددات المستودعات العامة.</span><span class="sxs-lookup"><span data-stu-id="45d37-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="45d37-110">يجب عليك تكوين المكونات لمهام سير عمل المستودع الواردة والصادرة وفقًا لمتطلبات العمل.</span><span class="sxs-lookup"><span data-stu-id="45d37-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="45d37-111">وأهم المكونات التي يجب عليك تكوينها هي قوالب الموجات، وقوالب العمل، وأوعية العمل، وتوجيهات المواقع.</span><span class="sxs-lookup"><span data-stu-id="45d37-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="45d37-112">تكوين المستودع</span><span class="sxs-lookup"><span data-stu-id="45d37-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="45d37-113">مراقبة عمل المستودع باستخدام قوالب العمل والتوجيهات المتعلقة بالموقع</span><span class="sxs-lookup"><span data-stu-id="45d37-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="45d37-114">إعداد الأجهزة المحمولة لعمل المستودع</span><span class="sxs-lookup"><span data-stu-id="45d37-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="45d37-115">إعداد توجيه موقع لتخزين أمر الشراء</span><span class="sxs-lookup"><span data-stu-id="45d37-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="45d37-116">إعداد قالب عمل لأوامر الشراء</span><span class="sxs-lookup"><span data-stu-id="45d37-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="45d37-117">عمليات إدارة المستودعات</span><span class="sxs-lookup"><span data-stu-id="45d37-117">Warehouse management processes</span></span>
- <span data-ttu-id="45d37-118">دعم متكامل للمستندات المصدر لأوامر المبيعات والمرتجعات‬ وأوامر التحويل وأوامر الإنتاج وكانبان</span><span class="sxs-lookup"><span data-stu-id="45d37-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="45d37-119">دعم مرن لعمليات سير عمل المواد الصادرة والواردة</span><span class="sxs-lookup"><span data-stu-id="45d37-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="45d37-120">التكامل الكامل مع عروض التصنيع والنقل</span><span class="sxs-lookup"><span data-stu-id="45d37-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="45d37-121">التحكم الكامل في حدود مخزون الموقع‬ ومقاييس الحجم في الموقع‬</span><span class="sxs-lookup"><span data-stu-id="45d37-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="45d37-122">خصائص المخزون التي تتحكم فيها حالة المخزون</span><span class="sxs-lookup"><span data-stu-id="45d37-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="45d37-123">دعم الدُفعة الكاملة والصنف التسلسلي</span><span class="sxs-lookup"><span data-stu-id="45d37-123">Full batch and serial item support</span></span>
- <span data-ttu-id="45d37-124">قدرات استلام أصناف مختلفة</span><span class="sxs-lookup"><span data-stu-id="45d37-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="45d37-125">استراتيجيات انتقاء متعددة</span><span class="sxs-lookup"><span data-stu-id="45d37-125">Multiple picking strategies</span></span>
- <span data-ttu-id="45d37-126">دعم جاهز للجيل التالي من الماسحات الضوئية للأكواد الشريطية</span><span class="sxs-lookup"><span data-stu-id="45d37-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="45d37-127">أنواع البالتات/الحاويات لعمليات المستودع</span><span class="sxs-lookup"><span data-stu-id="45d37-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="45d37-128">إمكانيات جرد متقدمة</span><span class="sxs-lookup"><span data-stu-id="45d37-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="45d37-129">طباعة الملصقات وتوجيه الملصقات مع دعم Zebra ZPL</span><span class="sxs-lookup"><span data-stu-id="45d37-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="45d37-130">تكامل المعلومات المهنية‬ في‬ Power BI</span><span class="sxs-lookup"><span data-stu-id="45d37-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="45d37-131">حركة المخزون اليدوية والتلقائية</span><span class="sxs-lookup"><span data-stu-id="45d37-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="45d37-132">مراقبة الجودة المتكاملة بشكل تام (QMS)</span><span class="sxs-lookup"><span data-stu-id="45d37-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="45d37-133">إمكانية تعقب كاملة لمعالجة المواد من قبل العاملين</span><span class="sxs-lookup"><span data-stu-id="45d37-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="45d37-134">معالجة الموجة الصادرة</span><span class="sxs-lookup"><span data-stu-id="45d37-134">Outbound wave processing</span></span>
- <span data-ttu-id="45d37-135">دعم التعبئة اليدوية والتعبئة التلقائية في حاويات</span><span class="sxs-lookup"><span data-stu-id="45d37-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="45d37-136">انتقاء نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="45d37-136">Cluster picking</span></span>
- <span data-ttu-id="45d37-137">توزيع بضائع بسيط</span><span class="sxs-lookup"><span data-stu-id="45d37-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45d37-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="45d37-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="45d37-139">ما الجديد وقيد التطوير</span><span class="sxs-lookup"><span data-stu-id="45d37-139">What's new and in development</span></span>
<span data-ttu-id="45d37-140">انتقل إلى [خارطة طريق Microsoft Dynamics 365](https://roadmap.dynamics.com/) للاطلاع على الميزات الجديدة التي تم إصدارها والميزات الجديدة قيد التطوير.</span><span class="sxs-lookup"><span data-stu-id="45d37-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="45d37-141">المدونات</span><span class="sxs-lookup"><span data-stu-id="45d37-141">Blogs</span></span>
<span data-ttu-id="45d37-142">يمكنك العثور على آراء وأخبار ومعلومات أخرى حول إدارة المستودعات وحلول أخرى في [مدونة Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="45d37-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

