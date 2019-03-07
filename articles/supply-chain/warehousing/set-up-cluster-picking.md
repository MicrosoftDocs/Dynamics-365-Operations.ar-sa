---
title: إعداد انتقاء نظام المجموعة
description: يصف هذا الموضوع كيفية إعداد انتقاء نظام مجموعة وكيفية تطبيق تأكيد الصنف بانتقاء نظام المجموعة.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7adec850cfb473b0bfc9536dcb1ef1cfd74129a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "364087"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="1e9f9-103">إعداد انتقاء نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="1e9f9-103">Set up cluster picking</span></span>

<span data-ttu-id="1e9f9-104">يصف هذا الموضوع كيفية تمكين العاملين من استخدام الأجهزة المحمولة الخاصة بهم لتجميع عمل الانتقاء في نظم مجموعات، حيث يمكنهم انتقاء الأصناف من موقع واحد لأوامر عمل متعددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="1e9f9-105">وهذا ما يسمى *انتقاء نظام المجموعة*.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="1e9f9-106">حول انتقاء نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="1e9f9-106">About cluster picking</span></span>

<span data-ttu-id="1e9f9-107">بعد إصدار أوامر العمل إلى المستودع، يمكن للعامل استخدام جهاز محمول لتعيين الأوامر لنظام مجموعة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="1e9f9-108">ينظم نظام المجموعة عمل الانتقاء للعامل.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="1e9f9-109">عند تعيين أمر عمل لنظام مجموعة، يجب على العامل استخدام انتقاء نظام المجموعة لتنفيذ عمل الانتقاء للأمر.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="1e9f9-110">لا يمكن للعامل استخدام أساليب انتقاء أخرى.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="1e9f9-111">إذا تم تعيين أمر عمل لنظام مجموعة عن طريق الخطأ، فيجب على العامل إيقاف نظام المجموعة ثم إعادة إنشائه.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="1e9f9-112">وإذا لزم الأمر، يمكن للعامل تمرير نظام مجموعة إلى عامل آخر.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="1e9f9-113">يؤدي هذا إلى تغيير حالة نظام المجموعة إلى تم الاجتياز.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="1e9f9-114">عندما يستخدم العامل جهازًا محمولاً للإشارة إلى اكتمال عمل الانتقاء والاستبعاد، يجب تأكيد الشحنة أو حمل العمل في عميل Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="1e9f9-115">إعداد انتقاء نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="1e9f9-115">Set up cluster picking</span></span>

<span data-ttu-id="1e9f9-116">لتمكين انتقاء نظام المجموعة، يجب إعداد ما يلي:</span><span class="sxs-lookup"><span data-stu-id="1e9f9-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="1e9f9-117">**ملفات تعريف نظام المجموعة** – تحديد ما إذا كان سيتم تلقائيًا إنشاء معرفات نظام المجموعة، وعدد المواضع المستخدمة، ومتى يمكن إيقاف نظم المجموعات، وكيفية التسلسل والتحقق من عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="1e9f9-118">**قوالب العمل** – تحديد كيفية إنشاء عمل الانتقاء لانتقاء نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="1e9f9-119">**توجيهات الموقع‬** – تحديد من أين يمكن انتقاء الأصناف وأين يمكن وضعها.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="1e9f9-120">**‏‫أصناف قائمة الجهاز المحمول‬** – تكوين عنصر قائمة للجهاز المحمول لاستخدام العمل الموجود الذي يتم توجيهه بواسطة انتقاء نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="1e9f9-121">ثم يجب عليك إضافة عنصر قائمة إلى قائمة الجهاز المحمول حتى يتم عرضه على الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="1e9f9-122">**محددات إدارة المستودعات‬** – تحديد التسلسل الرقمي لاستخدامه إذا كنت تريد إنشاء معرفات لنظام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="1e9f9-123">إعداد ملف تعريف نظام المجموعة</span><span class="sxs-lookup"><span data-stu-id="1e9f9-123">Set up a cluster profile</span></span>

<span data-ttu-id="1e9f9-124">لإعداد ملف تعريف نظام المجموعة، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="1e9f9-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="1e9f9-125">انقر فوق **إدارة المستودعات**\>**الإعداد**\>**الجهاز المحمول**\>**ملفات تعريف نظام المجموعة**.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="1e9f9-126">انقر فوق **جديد** لإنشاء ملف تعريف جديد.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="1e9f9-127">انقر فوق **إنشاء نظام مجموعة**، وضمن **فرز نظام المجموعة**، انقر فوق **جديد** لإعداد معايير الفرز لنظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="1e9f9-128">تتحكم معايير الفرز في الترتيب الذي سيقوم العامل على أساسه تنفيذ عمل الانتقاء.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="1e9f9-129">يمكنك إضافة أي عدد من المعايير حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="1e9f9-130">في حقل **رقم التسلسل**، قم بإدخال رقم لتحديد الترتيب الذي ستتم به معالجة معايير الفرز.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="1e9f9-131">في **اسم الحقل**، حدد الحقل الذي سيحدد الفرز.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="1e9f9-132">على سبيل المثال، إذا قمت بتحديد الحقل **WMSLocationId**، فسيتم تصنيف العمل حسب الموقع.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="1e9f9-133">في حقل **الفرز**، حدد أحد الخيارات التالية.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="1e9f9-134">**خيار**</span><span class="sxs-lookup"><span data-stu-id="1e9f9-134">**Option**</span></span>     | <span data-ttu-id="1e9f9-135">**الوصف**</span><span class="sxs-lookup"><span data-stu-id="1e9f9-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9f9-136">**تصاعدي**</span><span class="sxs-lookup"><span data-stu-id="1e9f9-136">**Ascending**</span></span>  | <span data-ttu-id="1e9f9-137">يتم تعيين تسلسل عمل الانتقاء في ترتيب تصاعدي استنادًا إلى معايير الفرز.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="1e9f9-138">على سبيل المثال، إذا استخدمت الحقل **WMSLocationId** بمثابة معايير الفرز، وكانت معرفات الموقع الخاصة بك هي 1 و2 و3 و4، فستقوم بالانتقاء من الموقع 4 أولاً.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="1e9f9-139">**تنازلي**</span><span class="sxs-lookup"><span data-stu-id="1e9f9-139">**Descending**</span></span> | <span data-ttu-id="1e9f9-140">يتم تعيين تسلسل عمل الانتقاء في ترتيب تنازلي استنادًا إلى معايير الفرز.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="1e9f9-141">على سبيل المثال، إذا استخدمت الحقل **WMSLocationId** بمثابة معايير الفرز، وكانت معرفات الموقع الخاصة بك هي 1 و2 و3 و4، فستقوم بالانتقاء من الموقع 1 أولاً.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="1e9f9-142">تأكيد الأصناف</span><span class="sxs-lookup"><span data-stu-id="1e9f9-142">Item confirmation</span></span>

<span data-ttu-id="1e9f9-143">عند تطبيق انتقاء نظام المجموعة، يُعد تأكيد الصنف أمرًا هامًا للتحقق من الأصناف التي تمت إضافتها إلى نظم المجموعات.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="1e9f9-144">يمكنك التحقق من الأصناف في انتقاء نظام المجموعة خلال عملية انتقاء نظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="1e9f9-145">يستند الإعداد على إعداد الرمز الشريطي للمنتج.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="1e9f9-146">إعداد التحقق من الصنف مع انتقاء نظام مجموعة</span><span class="sxs-lookup"><span data-stu-id="1e9f9-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="1e9f9-147">في عنصر قائمة جهاز محمول، قم بفتح نموذج الإعداد من تأكيد العمل: **إدارة المستودعات** \> **إدارة المستودعات** \> **الإعداد** \> **جهاز محمول** \> **عناصر قائمة الجهاز المحمول**.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="1e9f9-148">من عنصر قائمة الجهاز المحمول، قم بفتح **إعداد تأكيد العمل**.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="1e9f9-149">يسمح لك الخيار **تأكيد المنتج** بالتحقق من كل جزء من المخزون من خلال الهاتف المحمول عند مسحه ضوئيًا.</span><span class="sxs-lookup"><span data-stu-id="1e9f9-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
