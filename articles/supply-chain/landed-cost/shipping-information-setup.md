---
title: إعداد معلومات الشحن
description: يوضح هذا الموضوع كيفية إعداد معلومات الشحن للوحدة المنطقية التكلفة شاملة التفريغ.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 74ac7e0eac545369eef1a48f0085c820a4728e75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833679"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="71c6d-103">إعداد معلومات الشحن</span><span class="sxs-lookup"><span data-stu-id="71c6d-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71c6d-104">يوضح هذا الموضوع كيفية إعداد معلومات الشحن لوحدة **التكلفة المستلمة**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="71c6d-105">وصف البضائع</span><span class="sxs-lookup"><span data-stu-id="71c6d-105">Description of goods</span></span>

<span data-ttu-id="71c6d-106">تساعد أوصاف البضائع في تحديد الرحلة أو حاوية الشحن أو سجل البضائع والبضائع الموجودة فيها.</span><span class="sxs-lookup"><span data-stu-id="71c6d-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="71c6d-107">يمكنك تحديد وصف للبضائع في رأس حاوية الشحن أو رأس السجل.</span><span class="sxs-lookup"><span data-stu-id="71c6d-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="71c6d-108">للعمل مع أوصاف البضائع، انتقل إلى **التكلفة المستلمة \> إعداد معلومات الشحن \> وصف البضائع**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="71c6d-109">هناك، يمكنك عرض السجلات وفتحها وإنشاؤها وحذفها لوصف البضائع.</span><span class="sxs-lookup"><span data-stu-id="71c6d-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="71c6d-110">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="71c6d-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="71c6d-111">الحقل</span><span class="sxs-lookup"><span data-stu-id="71c6d-111">Field</span></span> | <span data-ttu-id="71c6d-112">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-112">Description</span></span> |
|---|---|
| <span data-ttu-id="71c6d-113">وصف البضائع</span><span class="sxs-lookup"><span data-stu-id="71c6d-113">Description of goods</span></span> | <span data-ttu-id="71c6d-114">أدخل اسم/رقم تعريف فريد لنوع البضائع التي ستستخدم هذا الوصف.</span><span class="sxs-lookup"><span data-stu-id="71c6d-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="71c6d-115">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-115">Description</span></span> | <span data-ttu-id="71c6d-116">أدخل وصفًا لنوع البضائع في هذه الفئة.</span><span class="sxs-lookup"><span data-stu-id="71c6d-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="71c6d-117">البواخر</span><span class="sxs-lookup"><span data-stu-id="71c6d-117">Vessels</span></span>

<span data-ttu-id="71c6d-118">السفينة هي الاسم الفريد للسفينة أو السفينة التي تستخدمها شركة أو وكالة شحن.</span><span class="sxs-lookup"><span data-stu-id="71c6d-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="71c6d-119">عند إنشاء رحلة، يجب عليك دائمًا إما اختيار سفينة أو الدخول إليها.</span><span class="sxs-lookup"><span data-stu-id="71c6d-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="71c6d-120">إذا كنت تستخدم نفس السفن غالبًا، فيمكنك جعل إنشاء رحلة جديدة أسرع وأسهل من خلال إنشاء سجل سفينة لكل منها، مما يتيح للمستخدمين تحديد السفينة من قائمة بدلاً من إدخال الاسم أو الرقم يدويًا لكل منهما الوقت.</span><span class="sxs-lookup"><span data-stu-id="71c6d-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="71c6d-121">للعمل مع السفن، انتقل إلى **التكلفة المستلمة \> إعداد معلومات الشحن \> السفن**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="71c6d-122">هناك، يمكنك عرض السجلات الخاصة بالسفن وفتحها وإنشائها وحذفها.</span><span class="sxs-lookup"><span data-stu-id="71c6d-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="71c6d-123">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="71c6d-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="71c6d-124">الحقل</span><span class="sxs-lookup"><span data-stu-id="71c6d-124">Field</span></span> | <span data-ttu-id="71c6d-125">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-125">Description</span></span> |
|---|---|
| <span data-ttu-id="71c6d-126">الباخرة</span><span class="sxs-lookup"><span data-stu-id="71c6d-126">Vessel</span></span> | <span data-ttu-id="71c6d-127">أدخل اسمًا/رقمًا تعريفيًا فريدًا للسفينة التي سيتم استخدامها لنقل البضائع في الرحلة.</span><span class="sxs-lookup"><span data-stu-id="71c6d-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="71c6d-128">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-128">Description</span></span> | <span data-ttu-id="71c6d-129">أدخل وصفًا للسفينة.</span><span class="sxs-lookup"><span data-stu-id="71c6d-129">Enter a description of the vessel.</span></span> <span data-ttu-id="71c6d-130">عادةً ما يحدد هذا الوصف اسم السفينة وشركة الشحن/المندوب.</span><span class="sxs-lookup"><span data-stu-id="71c6d-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="71c6d-131">وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="71c6d-131">Mode of delivery</span></span> | <span data-ttu-id="71c6d-132">حدد طريقة التسليم التي تستخدمها السفينة (مثل _الجو_ أو _المحيط_ أو _القطار_).</span><span class="sxs-lookup"><span data-stu-id="71c6d-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="71c6d-133">المصدّر‬ون</span><span class="sxs-lookup"><span data-stu-id="71c6d-133">Exporters</span></span>

<span data-ttu-id="71c6d-134">يحدد كل سجل مُصدِّر مورِّدًا أو مُصدِّرًا يمكن تعريفه على أنه المورد لرحلة ما.</span><span class="sxs-lookup"><span data-stu-id="71c6d-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="71c6d-135">يمكن أن يرتبط المصدر برحلة ما ويستخدم للإبلاغ.</span><span class="sxs-lookup"><span data-stu-id="71c6d-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="71c6d-136">للعمل مع المصدرين، انتقل إلى **التكلفة المستلمة \> إعداد معلومات الشحن \> المصدرين**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="71c6d-137">هناك، يمكنك عرض السجلات الخاصة بالمصدرين وفتحها وإنشائها وحذفها.</span><span class="sxs-lookup"><span data-stu-id="71c6d-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="71c6d-138">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="71c6d-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="71c6d-139">الحقل</span><span class="sxs-lookup"><span data-stu-id="71c6d-139">Field</span></span> | <span data-ttu-id="71c6d-140">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-140">Description</span></span> |
|---|---|
| <span data-ttu-id="71c6d-141">المصدّر‬</span><span class="sxs-lookup"><span data-stu-id="71c6d-141">Exporter</span></span> | <span data-ttu-id="71c6d-142">أدخل اسمًا/رقمًا تعريفيًا فريدًا لمصدر البضائع التي يتم نقلها في رحلة.</span><span class="sxs-lookup"><span data-stu-id="71c6d-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="71c6d-143">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-143">Description</span></span> | <span data-ttu-id="71c6d-144">أدخل وصفًا للمُصدر.</span><span class="sxs-lookup"><span data-stu-id="71c6d-144">Enter a description of the exporter.</span></span> <span data-ttu-id="71c6d-145">عادةً ما يحدد هذا الوصف الاسم الكامل لشركة/وكيل الشحن.</span><span class="sxs-lookup"><span data-stu-id="71c6d-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="71c6d-146">أكواد السلع</span><span class="sxs-lookup"><span data-stu-id="71c6d-146">Commodity codes</span></span>

<span data-ttu-id="71c6d-147">أنت تستخدم رموز البضائع للمساعدة في تحديد الجمارك وحساب معدلات الرسوم على البضائع في رحلة.</span><span class="sxs-lookup"><span data-stu-id="71c6d-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="71c6d-148">يمكنك تحديد أكواد السلع في صفحة **المنتجات التي تم إصدارها**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="71c6d-149">للعمل مع أكواد السلع، انتقل إلى **التكلفة المستلمة \> إعداد معلومات الشحن \> رموز السلع**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="71c6d-150">هناك، يمكنك عرض السجلات الخاصة بأكواد السلع وفتحها وإنشائها وحذفها.</span><span class="sxs-lookup"><span data-stu-id="71c6d-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="71c6d-151">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="71c6d-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="71c6d-152">الحقل</span><span class="sxs-lookup"><span data-stu-id="71c6d-152">Field</span></span> | <span data-ttu-id="71c6d-153">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-153">Description</span></span> |
|---|---|
| <span data-ttu-id="71c6d-154">كود السلعة</span><span class="sxs-lookup"><span data-stu-id="71c6d-154">Commodity code</span></span> | <span data-ttu-id="71c6d-155">أدخل رمزًا فريدًا لهذا النوع من السلع.</span><span class="sxs-lookup"><span data-stu-id="71c6d-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="71c6d-156">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-156">Description</span></span> | <span data-ttu-id="71c6d-157">يتيح إدخال وصف لكود نوع السلع.</span><span class="sxs-lookup"><span data-stu-id="71c6d-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="71c6d-158">وصف الجمارك</span><span class="sxs-lookup"><span data-stu-id="71c6d-158">Customs description</span></span>

<span data-ttu-id="71c6d-159">تساعد الأوصاف الجمركية في تحديد البضائع للأغراض الجمركية.</span><span class="sxs-lookup"><span data-stu-id="71c6d-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="71c6d-160">يمكنك تحديد وصف الجمارك في صفحة **المنتجات الصادرة** أو في بنود أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="71c6d-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="71c6d-161">للعمل مع الأوصاف الجمركية، انتقل إلى **التكلفة المستلمة \> إعداد معلومات الشحن \> وصف الجمارك**.</span><span class="sxs-lookup"><span data-stu-id="71c6d-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="71c6d-162">هناك، يمكنك عرض السجلات وفتحها وإنشاؤها وحذفها للأوصاف الجمركية.</span><span class="sxs-lookup"><span data-stu-id="71c6d-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="71c6d-163">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="71c6d-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="71c6d-164">الحقل</span><span class="sxs-lookup"><span data-stu-id="71c6d-164">Field</span></span> | <span data-ttu-id="71c6d-165">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-165">Description</span></span> |
|---|---|
| <span data-ttu-id="71c6d-166">وصف الجمارك</span><span class="sxs-lookup"><span data-stu-id="71c6d-166">Customs description</span></span> | <span data-ttu-id="71c6d-167">أدخل رمزًا فريدًا لهذا النوع من تصنيف الجمارك.</span><span class="sxs-lookup"><span data-stu-id="71c6d-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="71c6d-168">غالبًا ما يكون هذا الرمز هو الوصف الرسمي الذي توفره سلطة الجمارك للوصف والقيمة النوعية للبضائع.</span><span class="sxs-lookup"><span data-stu-id="71c6d-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="71c6d-169">الوصف</span><span class="sxs-lookup"><span data-stu-id="71c6d-169">Description</span></span> | <span data-ttu-id="71c6d-170">أدخل وصفًا لتصنيف الجمارك.</span><span class="sxs-lookup"><span data-stu-id="71c6d-170">Enter a description of the customs classification.</span></span> |
