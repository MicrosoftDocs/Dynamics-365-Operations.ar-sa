---
title: أوامر المستودعات لوحدات نطاق السحابة والحافة
description: يوفر هذا الموضوع معلومات حول قدره أمر المستودع التي يتم استخدامها كجزء من حمل العمل لوحده قياس المستودعات.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105690"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="cdded-103">أوامر المستودعات لوحدات نطاق السحابة والحافة</span><span class="sxs-lookup"><span data-stu-id="cdded-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="cdded-104">لا يتم دعم كافة وظائف الاعمال بشكل كامل في المعاينة العامة عند استخدام أحمال عمل وحدات قياس.</span><span class="sxs-lookup"><span data-stu-id="cdded-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="cdded-105">إذا كنت تستخدم وحدات قياس، تاكد من استخدام العمليات التي يصفها هذا الموضوع بوضوح كما هو مدعوم.</span><span class="sxs-lookup"><span data-stu-id="cdded-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="cdded-106">ما هي أوامر المستودع؟</span><span class="sxs-lookup"><span data-stu-id="cdded-106">What are warehouse orders?</span></span>

<span data-ttu-id="cdded-107">*أوامر المستودع* هي نوع من الأوامر التي تم إنشاؤها لدعم عمليات نشر مستودع وحده القياس والمقياس.</span><span class="sxs-lookup"><span data-stu-id="cdded-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="cdded-108">وتتيح لك امكانيه استلام المخزون عند تشغيل حمل عمل المستودع علي وحده قياس.</span><span class="sxs-lookup"><span data-stu-id="cdded-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="cdded-109">ويتم استخدامها حاليا مع أوامر الشراء.</span><span class="sxs-lookup"><span data-stu-id="cdded-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="cdded-110">يتم استخدام أوامر المستودع كجزء من معالجه أداره المستودع، كما هو الحال عند استخدام تطبيق المستودع لتسجيل المخزون الفعلي الفعلي اثناء معالجه أمر الشراء الوارد.</span><span class="sxs-lookup"><span data-stu-id="cdded-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="cdded-111">يتم إنشاء أوامر المستودع كجزء من عمليه *الإصدار إلى المستودع* المتوفرة لأوامر الشراء التي تحدد مستودع وحده القياس والأصناف التي تم تمكينها لاستخدام عمليات أداره المستودع.</span><span class="sxs-lookup"><span data-stu-id="cdded-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdded-112">تتوفر أوامر المستودع فقط في عمليات النشر التي تستخدم [أحمال العمليات لأداره المستودع لوحدات مقياس السحابة والحافة](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="cdded-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="cdded-113">إنشاء أمر المستودع</span><span class="sxs-lookup"><span data-stu-id="cdded-113">Create a warehouse order</span></span>

<span data-ttu-id="cdded-114">لإنشاء أمر المستودع، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cdded-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="cdded-115">سجل الدخول إلى مثيل Microsoft Dynamics 365 Supply Chain Management الذي يعمل في المركز.</span><span class="sxs-lookup"><span data-stu-id="cdded-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="cdded-116">(يجب بدء العمليه *الإصدار إلى المستودع* اثناء تسجيل الدخول في لوحه الوصل.)</span><span class="sxs-lookup"><span data-stu-id="cdded-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="cdded-117">انتقل إلى **التدبير والتوريد \> أوامر الشراء \> كل أوامر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="cdded-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="cdded-118">في جزء الإجراءات، ضمن علامة التبويب **المستودع**، في مجموعة **الإجراءات**، حدد **إصدار إلى المستودع‬**.</span><span class="sxs-lookup"><span data-stu-id="cdded-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="cdded-119">لعرض بنود أمر المستودع المرتبطة، افتح أمر الشراء ذا الصلة ، وحدد بندا في القسم **بنود أمر الشراء**، ثم في شريط الادوات، حدد **المستودع \> بنود أمر المستودع**.</span><span class="sxs-lookup"><span data-stu-id="cdded-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="cdded-120">لعرض كافة البنود، انتقل إلى **أداره المستودعات \> استعلامات وتقارير \>بنود أمر المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="cdded-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="cdded-121">إلغاء أمر المستودع</span><span class="sxs-lookup"><span data-stu-id="cdded-121">Cancel a warehouse order</span></span>

<span data-ttu-id="cdded-122">كجزء من عمليه *إصدار إلى المستودع*، يتم ربط حركات مخزون أمر الشراء بأوامر المستودع والتي يتم تامينها من التحديث بواسطة لوحه الوصل.</span><span class="sxs-lookup"><span data-stu-id="cdded-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="cdded-123">إذا قمت بالإصدار إلى المستودع عن طريق الخطا، أو إذا كان لديك بعض الأسباب الأخرى للغاء إنشاء بنود أمر المستودع، فانه يمكنك طلب إلغاء بنود أمر المستودع.</span><span class="sxs-lookup"><span data-stu-id="cdded-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="cdded-124">لإلغاء بنود أمر المستودع، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cdded-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="cdded-125">سجل الدخول إلى مثيل Supply Chain Management الذي يعمل في المركز.</span><span class="sxs-lookup"><span data-stu-id="cdded-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="cdded-126">انتقل إلى **أداره المستودعات \> استعلامات وتقارير \>بنود أمر المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="cdded-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="cdded-127">حدد البند المناسب.</span><span class="sxs-lookup"><span data-stu-id="cdded-127">Select the relevant line.</span></span>
1. <span data-ttu-id="cdded-128">في جزء الاجراء ، حدد **إلغاء بنود أمر المستودع**.</span><span class="sxs-lookup"><span data-stu-id="cdded-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="cdded-129">سيتم رفض طلب إلغاء البنود لآيه بنود معلقه بالفعل إلغاء أو التي تتم معالجتها بشكل نشط في مستودع يقوم بتشغيل حمل العمل علي وحده قياس.</span><span class="sxs-lookup"><span data-stu-id="cdded-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="cdded-130">مراقبة أمر المستودع</span><span class="sxs-lookup"><span data-stu-id="cdded-130">Monitor a warehouse order</span></span>

<span data-ttu-id="cdded-131">في طريقه العرض **بنود أمر المستودع**، يمكنك مراقبه تقدم الاستلام الوارد عن طريق مراجعه القيم في العمود **الكمية المتبقية للاستلام**.</span><span class="sxs-lookup"><span data-stu-id="cdded-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="cdded-132">لعرض التفاصيل المتعلقة بالعمل الذي تم إنجازه باستخدام تطبيق المستودع، اتبع أحدي هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cdded-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="cdded-133">انتقل إلى **أداره المستودعات \> استعلامات وتقارير \> بنود أمر المستودع**، واستخدم عامل التصفية للعثور علي البنود التي تبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="cdded-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="cdded-134">انتقل إلى **التدبير وتحديد الموارد \> أوامر الشراء \> كافة أوامر الشراء**، وافتح أمر الشراء ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="cdded-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="cdded-135">في قسم **بنود أمر الشراء**، حدد بندا واحدا أو أكثر، ثم في شريط الادوات، حدد **مستودع \> إدخالات إيصال المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="cdded-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
