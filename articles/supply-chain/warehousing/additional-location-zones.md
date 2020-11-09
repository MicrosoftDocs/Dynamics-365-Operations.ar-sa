---
title: مناطق المواقع الإضافية
description: يوفر هذا الموضوع نظرة عامة على مناطق المواقع الجديدة التي تمت اضافتها إلى Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016280"
---
# <a name="additional-location-zones"></a><span data-ttu-id="28a61-103">مناطق المواقع الإضافية</span><span class="sxs-lookup"><span data-stu-id="28a61-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28a61-104">تتوفر ثلاثة حقول مناطق جديدة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="28a61-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="28a61-105">ويمكن لمديري المستودع استخدامهما لتحديد المؤسسات أو التخطيطات الإضافية للمستودع.</span><span class="sxs-lookup"><span data-stu-id="28a61-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="28a61-106">يمكن تعيين حقول المنطقة الجديدة إما يدويًا أو باستخدام معالج **إعداد الموقع**.</span><span class="sxs-lookup"><span data-stu-id="28a61-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="28a61-107">ويمكن استخدامها في أي استعلام أو تصفية تستخدم جدول المواقع.</span><span class="sxs-lookup"><span data-stu-id="28a61-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="28a61-108">لا يتطلب الأمر أي إعداد إضافي لاستخدام حقول المنطقة.</span><span class="sxs-lookup"><span data-stu-id="28a61-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="28a61-109">تشغيل ميزة منطقة الموقع الإضافية</span><span class="sxs-lookup"><span data-stu-id="28a61-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="28a61-110">قبل أن تتمكن من استخدام ميزة *منطقة الموقع الإضافية* ، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="28a61-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="28a61-111">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="28a61-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="28a61-112">في مساحة عمل **إدارة الميزات** ، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="28a61-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="28a61-113">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="28a61-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="28a61-114">**اسم الميزة:** *منطقة الموقع الإضافية*</span><span class="sxs-lookup"><span data-stu-id="28a61-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="28a61-115">استخدام مناطق الموقع</span><span class="sxs-lookup"><span data-stu-id="28a61-115">Use location zones</span></span>

1. <span data-ttu-id="28a61-116">انتقل إلى **إدارة المستودع \> الإعداد \> المستودع \> معالج إعداد الموقع**.</span><span class="sxs-lookup"><span data-stu-id="28a61-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="28a61-117">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="28a61-117">Set the following values:</span></span>

    - <span data-ttu-id="28a61-118">في حقل **المستودع** ، حدد _62_.</span><span class="sxs-lookup"><span data-stu-id="28a61-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="28a61-119">في الحقل **معرف المنطقة** ، حدد _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="28a61-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="28a61-120">في الحقل **المنطقة الإضافية 1** ، حدد _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="28a61-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="28a61-121">في الحقل **المنطقة الإضافية 2** ، حدد _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="28a61-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="28a61-122">في الحقل **معرف ملف تعريف الموقع** ، حدد _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="28a61-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="28a61-123">حدد سطر **الأرضية**.</span><span class="sxs-lookup"><span data-stu-id="28a61-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="28a61-124">في الحقل **‏من رقم** ، أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="28a61-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="28a61-125">في الحقل **‏إلى رقم** ، أدخل _3_.</span><span class="sxs-lookup"><span data-stu-id="28a61-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="28a61-126">حدد سطر **الممر**.</span><span class="sxs-lookup"><span data-stu-id="28a61-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="28a61-127">في الحقل **‏من رقم** ، أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="28a61-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="28a61-128">في الحقل **‏إلى رقم** ، أدخل _5_.</span><span class="sxs-lookup"><span data-stu-id="28a61-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="28a61-129">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="28a61-129">Select **Create**.</span></span>
8. <span data-ttu-id="28a61-130">سوف تتلقى رسائل تشير إلى إضافة مواقع جديدة.</span><span class="sxs-lookup"><span data-stu-id="28a61-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="28a61-131">حدد زر **إظهار الرسائل** لعرض الرسائل.</span><span class="sxs-lookup"><span data-stu-id="28a61-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="28a61-132">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="28a61-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="28a61-133">تظهر المواقع الجديدة في القائمة، وتتوفر كافة حقول المنطقة (وهي حقل المنطقة الموجود وحقول المنطقة الإضافية الجديدة).</span><span class="sxs-lookup"><span data-stu-id="28a61-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
