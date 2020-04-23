---
title: استلام لوحة الترخيص‬ عبر تطبيق المستودع للأجهزة المحمولة
description: يوضح هذا الموضوع كيفية إعداد تطبيق المستودع للأجهزة المحمولة‬ لدعم استخدام عملية استلام لوحة الترخيص لاستلام المخزون الفعلي.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261298"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="441ce-103">استلام لوحة الترخيص‬ عبر تطبيق المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="441ce-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="441ce-104">يوضح هذا الموضوع كيفية إعداد تطبيق المستودع للأجهزة المحمولة‬ بحيث يدعم استخدام عملية استلام لوحة الترخيص لاستلام المخزون الفعلي.</span><span class="sxs-lookup"><span data-stu-id="441ce-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="441ce-105">يمكنك استخدام هذه الوظيفة لتسجيل استلام المخزون الوارد المرتبط بإشعار شحن مسبق (ASN) بسرعة.</span><span class="sxs-lookup"><span data-stu-id="441ce-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="441ce-106">ينشئ النظام بشكل تلقائي إشعار ASN عند استخدام عمليات إدارة المستودعات لشحن أمر تحويل.</span><span class="sxs-lookup"><span data-stu-id="441ce-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="441ce-107">بالنسبة إلى عملية أمر الشراء، يمكن تسجيل ASN يدويًا أو يمكن استيراده تلقائيًا باستخدام عمليات كيان بيانات ASN الواردة.</span><span class="sxs-lookup"><span data-stu-id="441ce-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="441ce-108">ترتبط بيانات ASN بالأحمال والشحنات عبر *بنى التعبئة*، حيث يمكن ان تحتوي البالتات (لوحات الترخيص الرئيسية) على حالات (لوحات الترخيص المتداخلة).</span><span class="sxs-lookup"><span data-stu-id="441ce-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="441ce-109">لتخفيض عدد حركات المخزون عند استخدام بنيات التعبئة التي تحتوي على لوحات ترخيص متداخلة، يقوم النظام بتسجيل المخزون الفعلي الموجود علي لوحة الترخيص الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="441ce-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="441ce-110">لتشغيل حركة المخزون الفعلي من لوحة الترخيص الأصلية إلى لوحات الترخيص المتداخلة، استنادًا إلى بيانات بنيه التعبئة، يجب أن يوفر الجهاز المحمول عنصر قائمة يستند إلى عملية إنشاء العمل *تعبئة لألواح الترخيص المتداخلة*.</span><span class="sxs-lookup"><span data-stu-id="441ce-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="441ce-111">إظهار صفحة ملخص الاستلام أو تخطيها</span><span class="sxs-lookup"><span data-stu-id="441ce-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="441ce-112">يمكنك استخدام الميزة *التحكم في عرض صفحة ملخص الاستلام على الأجهزة المحمولة* للاستفادة من سير مهام إضافي مفصل في تطبيق المستودع كجزء من عملية استلام لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="441ce-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="441ce-113">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="441ce-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="441ce-114">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="441ce-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="441ce-115">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="441ce-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="441ce-116">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="441ce-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="441ce-117">**اسم الميزة:** *التحكم في عرض صفحة ملخص الاستلام على الأجهزة المحمولة*</span><span class="sxs-lookup"><span data-stu-id="441ce-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="441ce-118">عند تشغيل هذه الميزة، ستوفر عناصر قائمة الجهاز المحمول لاستلام لوحة الترخيص‬ أو استلام ‏‫لوحة الترخيص‬ وتخزينها‬ الإعداد **عرض صفحة ملخص الاستلام**.</span><span class="sxs-lookup"><span data-stu-id="441ce-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="441ce-119">يتضمن هذا الإعداد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="441ce-119">This setting has the following options:</span></span>

- <span data-ttu-id="441ce-120">**عرض ملخص مفصل** – أثناء استلام لوحة الترخيص، سيرى العاملون صفحة إضافية تعرض معلومات ASN الكاملة.</span><span class="sxs-lookup"><span data-stu-id="441ce-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="441ce-121">**تخطي الملخص** – لن يتمكن العاملون من رؤية معلومات ASN الكاملة.</span><span class="sxs-lookup"><span data-stu-id="441ce-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="441ce-122">ولن يتمكن عمال المستودعات أيضًا من تعيين رمز الإرجاع أو إضافة استثناءات أثناء عملية الاستلام.</span><span class="sxs-lookup"><span data-stu-id="441ce-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="441ce-123">منع استخدام لوحات الترخيص المشحونة في أمر التحويل في المستودعات غير المستودع الوجهة.</span><span class="sxs-lookup"><span data-stu-id="441ce-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="441ce-124">لا يمكن استخدام عملية استلام لوحة الترخيص إذا احتوى إشعار ASN على معرف لوحة ترخيص موجود ولديه بيانات فعلية في موقع مستودع آخر غير موقع المستودع حيث يحدث تسجيل لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="441ce-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="441ce-125">بالنسبة إلى سيناريوهات أمر التحويل التي لا يتعقب فيها مستودع البضاعة بالطريق ألواح الترخيص (وبالتالي لا يتعقب أيضًا المخزون الفعلي لكل لوحة ترخيص)، يمكنك استخدام الميزة *منع استخدام لوحات الترخيص المشحونة في أمر التحويل في مستودعات أخرى غير المستودع الوجهة.‬* لمنع التحديثات الفعلية لألواح الترخيص بالطريق.</span><span class="sxs-lookup"><span data-stu-id="441ce-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="441ce-126">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="441ce-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="441ce-127">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="441ce-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="441ce-128">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="441ce-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="441ce-129">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="441ce-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="441ce-130">**اسم الميزة:** *منع استخدام لوحات الترخيص المشحونة في أمر التحويل في مستودعات أخرى غير المستودع الوجهة*</span><span class="sxs-lookup"><span data-stu-id="441ce-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="441ce-131">لإدارة الوظائف عندما تكون هذه الميزة متوفرة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="441ce-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="441ce-132">انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="441ce-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="441ce-133">على علامة التبويب **عام**، على علامة التبويب السريعة **ألواح الترخيص**، قم بتعيين الحقل **سياسة لوحة ترخيص مستودع البضاعة بالطريق** إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="441ce-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="441ce-134">**السماح بإعادة استخدام لوحة ترخيص غير متعقبة** – يعمل النظام بنفس الطريقة التي يعمل بها عندما لا تكون الميزة *منع استخدام لوحات الترخيص المشحونة في أمر التحويل في مستودعات أخرى غير المستودع الوجهة* متوفرة.</span><span class="sxs-lookup"><span data-stu-id="441ce-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="441ce-135">هذه القيمة هي الإعداد الافتراضي عندما تقوم بتنشيط الميزة للمرة الأولى.</span><span class="sxs-lookup"><span data-stu-id="441ce-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="441ce-136">**منع إعادة استخدام لوحة الترخيص غير المتعقبة** – سوف يسمح فقط التحديثات المتاحة ذات الصلة بلوحة ترخيص مشحونة في المستودع الوجهة حتى يتم استلام أمر التحويل.</span><span class="sxs-lookup"><span data-stu-id="441ce-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="441ce-137">مزيد من المعلومات</span><span class="sxs-lookup"><span data-stu-id="441ce-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="441ce-138">لمزيد من المعلومات حول عناصر قائمة الجهاز المحمول، راجع [إعداد الأجهزة المحمولة لعمل المستودع](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="441ce-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
