---
title: حاويات الشحن
description: يوضح هذا الموضوع كيفية إعداد حاويات الشحن للوحدة المنطقية التكلفة شاملة التفريغ.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833703"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="727d5-103">إعداد حاوية الشحن</span><span class="sxs-lookup"><span data-stu-id="727d5-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="727d5-104">يوضح هذا الموضوع كيفية إعداد حاويات الشحن لوحدة **التكلفة المستلمة**.</span><span class="sxs-lookup"><span data-stu-id="727d5-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="727d5-105">إعداد أنواع حاويات الشحن</span><span class="sxs-lookup"><span data-stu-id="727d5-105">Set up shipping container types</span></span>

<span data-ttu-id="727d5-106">تحدد أنواع حاويات الشحن أنواع حاويات الشحن المتاحة للاستخدام أثناء الشحن والرحلات.</span><span class="sxs-lookup"><span data-stu-id="727d5-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="727d5-107">للعمل مع أنواع حاويات الشحن، انتقل إلى **التكلفة المستلمة \> إعداد الحاويات \> أنواع حاويات الشحن**.</span><span class="sxs-lookup"><span data-stu-id="727d5-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="727d5-108">يمكنك عرض وإضافة وإزالة السجلات لأنواع الحاويات.</span><span class="sxs-lookup"><span data-stu-id="727d5-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="727d5-109">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="727d5-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="727d5-110">الحقل</span><span class="sxs-lookup"><span data-stu-id="727d5-110">Field</span></span> | <span data-ttu-id="727d5-111">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-111">Description</span></span> |
|---|---|
| <span data-ttu-id="727d5-112">نوع حاوية الشحن</span><span class="sxs-lookup"><span data-stu-id="727d5-112">Shipping container type</span></span> | <span data-ttu-id="727d5-113">أدخل اسم/رقم تعريف فريد لنوع حاوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="727d5-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-114">Description</span></span> | <span data-ttu-id="727d5-115">أدخل وصفًا لنوع حاوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="727d5-116">الحجم</span><span class="sxs-lookup"><span data-stu-id="727d5-116">Volume</span></span> | <span data-ttu-id="727d5-117">أدخل الحد الأقصى للحجم المسموح به في حاويات الشحن من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="727d5-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="727d5-118">الوزن</span><span class="sxs-lookup"><span data-stu-id="727d5-118">Weight</span></span> | <span data-ttu-id="727d5-119">أدخل الحد الأقصى للوزن المسموح به في حاويات الشحن من هذا النوع.</span><span class="sxs-lookup"><span data-stu-id="727d5-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="727d5-120">قابل للإرجاع</span><span class="sxs-lookup"><span data-stu-id="727d5-120">Returnable</span></span> | <span data-ttu-id="727d5-121">حدد ما إذا كان يمكن إرجاع حاويات الشحن من هذا النوع إلى المورد بعد استخدامها أثناء الرحلة.</span><span class="sxs-lookup"><span data-stu-id="727d5-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="727d5-122">إذا تم تعيين هذا الخيار إلى *نعم*، قد يتم تطبيق تكاليف إضافية لإعادة حاويات الشحن من هذا النوع إلى ميناء المنشأ.</span><span class="sxs-lookup"><span data-stu-id="727d5-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="727d5-123">إعداد حاويات الشحن</span><span class="sxs-lookup"><span data-stu-id="727d5-123">Set up shipping containers</span></span>

<span data-ttu-id="727d5-124">يمكنك استخدام سجلات حاويات الشحن لتحديد كل حاوية تستخدمها أثناء الرحلات.</span><span class="sxs-lookup"><span data-stu-id="727d5-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="727d5-125">عند إنشاء رحلة، يمكنك تحديد حاوية معينة لها في قائمة جميع سجلات حاويات الشحن التي حددتها هنا.</span><span class="sxs-lookup"><span data-stu-id="727d5-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="727d5-126">هذه الميزة مفيدة بشكل خاص إذا كانت شركتك تمتلك حاويات الشحن الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="727d5-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="727d5-127">لا يتعين عليك إدخال أرقام حاويات الشحن لحاويات الشحن التي سيتم استخدامها مرة واحدة فقط.</span><span class="sxs-lookup"><span data-stu-id="727d5-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="727d5-128">بدلاً من ذلك، يمكنك إضافة رقم حاوية الشحن عند إنشاء رحلة.</span><span class="sxs-lookup"><span data-stu-id="727d5-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="727d5-129">تستخدم سجلات حاويات الشحن فقط في التكلفة المستلمة.</span><span class="sxs-lookup"><span data-stu-id="727d5-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="727d5-130">إنها غير متوفرة في وحدة **إدارة النقل** القياسية (TMS).</span><span class="sxs-lookup"><span data-stu-id="727d5-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="727d5-131">للعمل مع حاويات الشحن، انتقل إلى **التكلفة المستلمة \> إعداد الحاويات \> حاويات الشحن**.</span><span class="sxs-lookup"><span data-stu-id="727d5-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="727d5-132">يمكنك عرض وإضافة وإزالة السجلات لحاويات الشحن الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="727d5-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="727d5-133">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="727d5-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="727d5-134">الحقل</span><span class="sxs-lookup"><span data-stu-id="727d5-134">Field</span></span> | <span data-ttu-id="727d5-135">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-135">Description</span></span> |
|---|---|
| <span data-ttu-id="727d5-136">حاوية الشحن</span><span class="sxs-lookup"><span data-stu-id="727d5-136">Shipping container</span></span> | <span data-ttu-id="727d5-137">أدخل اسم/رقم تعريف فريد لحاوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="727d5-138">نوع حاوية الشحن</span><span class="sxs-lookup"><span data-stu-id="727d5-138">Shipping container type</span></span> | <span data-ttu-id="727d5-139">حدد نوع حاوية الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-139">Select the type of shipping container.</span></span> <span data-ttu-id="727d5-140">لمزيد من المعلومات، راجع قسم [إعداد أنواع حاويات الشحن](#shipping-container-types) مبكرًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="727d5-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="727d5-141">إعداد حاوية الشحن اختياري.</span><span class="sxs-lookup"><span data-stu-id="727d5-141">The shipping container setup is optional.</span></span> <span data-ttu-id="727d5-142">عادةً، لن تستخدمه إلا إذا كانت شركتك تمتلك حاويات الشحن الخاصة بها أو غالبًا ما تعيد استخدام نفس حاويات الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="727d5-143">لم يتم حساب أرقام التحقق لأرقام حاويات الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="727d5-144">إعداد أنواع الوحدات</span><span class="sxs-lookup"><span data-stu-id="727d5-144">Set up unit types</span></span>

<span data-ttu-id="727d5-145">تقوم أنواع الوحدات بإنشاء مجموعات إضافية وطرق تحديد لحاويات الشحن.</span><span class="sxs-lookup"><span data-stu-id="727d5-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="727d5-146">يستخدم نوع الوحدة عادةً لتحديد نوع الحاوية التي يتم تعبئة البضائع فيها، مثل المنصات أو البراميل.</span><span class="sxs-lookup"><span data-stu-id="727d5-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="727d5-147">يمكنك تحديد نوع الوحدة عند إعداد حاوية في صفحة **كل حاويات الشحن**.</span><span class="sxs-lookup"><span data-stu-id="727d5-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="727d5-148">يتم استخدام أنواع الوحدات فقط في التكلفة المستلمة.</span><span class="sxs-lookup"><span data-stu-id="727d5-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="727d5-149">إنها غير متوفرة في إدارة النقل (TMS).</span><span class="sxs-lookup"><span data-stu-id="727d5-149">They aren't available in TMS.</span></span>

<span data-ttu-id="727d5-150">للعمل مع أنواع الوحدات، انتقل إلى **التكلفة المستلمة \> إعداد الحاويات \> أنواع الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="727d5-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="727d5-151">يمكنك عرض وإضافة وإزالة السجلات لأنواع الوحدات.</span><span class="sxs-lookup"><span data-stu-id="727d5-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="727d5-152">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="727d5-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="727d5-153">الحقل</span><span class="sxs-lookup"><span data-stu-id="727d5-153">Field</span></span> | <span data-ttu-id="727d5-154">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-154">Description</span></span> |
|---|---|
| <span data-ttu-id="727d5-155">نوع الوحدة</span><span class="sxs-lookup"><span data-stu-id="727d5-155">Unit type</span></span> | <span data-ttu-id="727d5-156">أدخل اسم/رقم تعريف فريد لنوع الوحدة.</span><span class="sxs-lookup"><span data-stu-id="727d5-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="727d5-157">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-157">Description</span></span> | <span data-ttu-id="727d5-158">يتيح إدخال وصف لكود نوع الوحدة.</span><span class="sxs-lookup"><span data-stu-id="727d5-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="727d5-159">إعداد أنواع التبريد</span><span class="sxs-lookup"><span data-stu-id="727d5-159">Set up refrigeration types</span></span>

<span data-ttu-id="727d5-160">تقوم أنواع التبريد بإنشاء مجموعات إضافية وطرق تحديد لحاويات الشحن (عادة الحاويات المبردة).</span><span class="sxs-lookup"><span data-stu-id="727d5-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="727d5-161">يمكنك تحديد نوع التبريد عند إعداد حاوية في صفحة **كل حاويات الشحن**.</span><span class="sxs-lookup"><span data-stu-id="727d5-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="727d5-162">للعمل مع أنواع التبريد، انتقل إلى **التكلفة المستلمة \> إعداد الحاويات \> أنواع التبريد**.</span><span class="sxs-lookup"><span data-stu-id="727d5-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="727d5-163">يمكنك عرض وإضافة وإزالة السجلات لأنواع التبريد.</span><span class="sxs-lookup"><span data-stu-id="727d5-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="727d5-164">يصف الجدول التالي الحقول المتوفرة لكل سجل.</span><span class="sxs-lookup"><span data-stu-id="727d5-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="727d5-165">الحقل</span><span class="sxs-lookup"><span data-stu-id="727d5-165">Field</span></span> | <span data-ttu-id="727d5-166">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-166">Description</span></span> |
|---|---|
| <span data-ttu-id="727d5-167">نوع التبريد</span><span class="sxs-lookup"><span data-stu-id="727d5-167">Refrigeration type</span></span> | <span data-ttu-id="727d5-168">أدخل اسم/رقم تعريف فريد لنوع التبريد.</span><span class="sxs-lookup"><span data-stu-id="727d5-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="727d5-169">الوصف</span><span class="sxs-lookup"><span data-stu-id="727d5-169">Description</span></span> | <span data-ttu-id="727d5-170">أدخل وصفًا لنوع التبريد.</span><span class="sxs-lookup"><span data-stu-id="727d5-170">Enter a description of the refrigeration type.</span></span> |
