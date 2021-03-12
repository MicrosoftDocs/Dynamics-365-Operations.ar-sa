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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 662725edf5bf8d95be038f7c989b73d8d05fa0df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996416"
---
# <a name="additional-location-zones"></a><span data-ttu-id="5a845-103">مناطق المواقع الإضافية</span><span class="sxs-lookup"><span data-stu-id="5a845-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a845-104">تتوفر ثلاثة حقول مناطق جديدة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5a845-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5a845-105">ويمكن لمديري المستودع استخدامهما لتحديد المؤسسات أو التخطيطات الإضافية للمستودع.</span><span class="sxs-lookup"><span data-stu-id="5a845-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="5a845-106">يمكن تعيين حقول المنطقة الجديدة إما يدويًا أو باستخدام معالج **إعداد الموقع**.</span><span class="sxs-lookup"><span data-stu-id="5a845-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="5a845-107">ويمكن استخدامها في أي استعلام أو تصفية تستخدم جدول المواقع.</span><span class="sxs-lookup"><span data-stu-id="5a845-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="5a845-108">لا يتطلب الأمر أي إعداد إضافي لاستخدام حقول المنطقة.</span><span class="sxs-lookup"><span data-stu-id="5a845-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="5a845-109">تشغيل ميزة منطقة الموقع الإضافية</span><span class="sxs-lookup"><span data-stu-id="5a845-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="5a845-110">قبل أن تتمكن من استخدام ميزة *منطقة الموقع الإضافية*، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5a845-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="5a845-111">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="5a845-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5a845-112">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="5a845-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5a845-113">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="5a845-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5a845-114">**اسم الميزة:** *منطقة الموقع الإضافية*</span><span class="sxs-lookup"><span data-stu-id="5a845-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="5a845-115">استخدام مناطق الموقع</span><span class="sxs-lookup"><span data-stu-id="5a845-115">Use location zones</span></span>

1. <span data-ttu-id="5a845-116">انتقل إلى **إدارة المستودع \> الإعداد \> المستودع \> معالج إعداد الموقع**.</span><span class="sxs-lookup"><span data-stu-id="5a845-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="5a845-117">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="5a845-117">Set the following values:</span></span>

    - <span data-ttu-id="5a845-118">في حقل **المستودع**، حدد _62_.</span><span class="sxs-lookup"><span data-stu-id="5a845-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="5a845-119">في الحقل **معرف المنطقة**، حدد _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="5a845-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="5a845-120">في الحقل **المنطقة الإضافية 1**، حدد _PICKZONE1_.</span><span class="sxs-lookup"><span data-stu-id="5a845-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="5a845-121">في الحقل **المنطقة الإضافية 2**، حدد _WEBSHOP1_.</span><span class="sxs-lookup"><span data-stu-id="5a845-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="5a845-122">في الحقل **معرف ملف تعريف الموقع**، حدد _FLOOR_.</span><span class="sxs-lookup"><span data-stu-id="5a845-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="5a845-123">حدد سطر **الأرضية**.</span><span class="sxs-lookup"><span data-stu-id="5a845-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="5a845-124">في الحقل **‏من رقم**، أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="5a845-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="5a845-125">في الحقل **‏إلى رقم**، أدخل _3_.</span><span class="sxs-lookup"><span data-stu-id="5a845-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="5a845-126">حدد سطر **الممر**.</span><span class="sxs-lookup"><span data-stu-id="5a845-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="5a845-127">في الحقل **‏من رقم**، أدخل _1_.</span><span class="sxs-lookup"><span data-stu-id="5a845-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="5a845-128">في الحقل **‏إلى رقم**، أدخل _5_.</span><span class="sxs-lookup"><span data-stu-id="5a845-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="5a845-129">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="5a845-129">Select **Create**.</span></span>
8. <span data-ttu-id="5a845-130">سوف تتلقى رسائل تشير إلى إضافة مواقع جديدة.</span><span class="sxs-lookup"><span data-stu-id="5a845-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="5a845-131">حدد زر **إظهار الرسائل** لعرض الرسائل.</span><span class="sxs-lookup"><span data-stu-id="5a845-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="5a845-132">انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**.</span><span class="sxs-lookup"><span data-stu-id="5a845-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="5a845-133">تظهر المواقع الجديدة في القائمة، وتتوفر كافة حقول المنطقة (وهي حقل المنطقة الموجود وحقول المنطقة الإضافية الجديدة).</span><span class="sxs-lookup"><span data-stu-id="5a845-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
