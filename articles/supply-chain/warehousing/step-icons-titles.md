---
title: تعيين رموز وعناوين الخطوة لتطبيق الأجهزة المحمولة لـ Warehouse Management
description: يصف هذا الموضوع كيفية تعيين رموز وعناوين الخطوات لتدفقات المهام الجديدة أو المخصصة لتطبيق الأجهزة المحمولة لـ Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049354"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="34a6a-103">تعيين رموز وعناوين الخطوة لتطبيق الأجهزة المحمولة لـ Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="34a6a-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34a6a-104">يصف هذا الموضوع كيفية تعيين رموز وعناوين الخطوات لتدفقات المهام الجديدة أو المخصصة لتطبيق الأجهزة المحمولة لـ Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="34a6a-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="34a6a-105">توضح التوضيحات التالية كيفية ظهور رموز وعناوين الخطوات في تطبيق الأجهزة المحمولة لـ Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="34a6a-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="34a6a-106">![مثال على رمز خطوة وعنوان خطوة في تطبيق الأجهزة المحمولة لـ Warehouse Management](media/step-icon-example.png "مثال على رمز خطوة وعنوان خطوة في تطبيق الأجهزة المحمولة لـ Warehouse Management")</span><span class="sxs-lookup"><span data-stu-id="34a6a-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="34a6a-107">تشغيل هذه الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="34a6a-107">Turn on this feature in your system</span></span>

<span data-ttu-id="34a6a-108">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="34a6a-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="34a6a-109">بإمكان المسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="34a6a-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="34a6a-110">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="34a6a-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="34a6a-111">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="34a6a-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="34a6a-112">**اسم الميزة:** *إعدادات المستخدم والرموز وعناوين الخطوات لتطبيق المستودع الجديد*</span><span class="sxs-lookup"><span data-stu-id="34a6a-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="34a6a-113">معرفات الخطوات القياسية والفئات والرموز</span><span class="sxs-lookup"><span data-stu-id="34a6a-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="34a6a-114">يتم تعريف كل خطوة في تدفق المهام بمعرف خطوة، ويحتوي كل معرف خطوة على فئة خطوة مقابلة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="34a6a-115">يتم تحديد رمز الخطوة وعنوانها في كل فئة خطوة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="34a6a-116">معرفات الخطوات و فئات الخطوات</span><span class="sxs-lookup"><span data-stu-id="34a6a-116">Step IDs and step classes</span></span>

<span data-ttu-id="34a6a-117">يسرد الجدول التالي كل معرف خطوة متوفر حاليًا، وفئة الخطوة المقابلة له.</span><span class="sxs-lookup"><span data-stu-id="34a6a-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="34a6a-118">يتم استخدام اسم عنصر التحكم الخاص بحقل الإدخال الأساسي كمعرف للخطوة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="34a6a-119">للحصول على مثال يوضح كيفية استخدام معرفات الخطوات هذه وفئاتها، راجع تطبيق الأسلوب `WHSMobileAppStepInfoBuilder.stepId()` في [المثال: تعيين رموز وعناوين الخطوات للقسم تدفق مخصص](#example) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="34a6a-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="34a6a-120">معرف الخطوة</span><span class="sxs-lookup"><span data-stu-id="34a6a-120">Step ID</span></span> | <span data-ttu-id="34a6a-121">فئة الخطوة</span><span class="sxs-lookup"><span data-stu-id="34a6a-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="34a6a-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-122">BatchDisposition</span></span> | <span data-ttu-id="34a6a-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="34a6a-124">الناقل</span><span class="sxs-lookup"><span data-stu-id="34a6a-124">Carrier</span></span> | <span data-ttu-id="34a6a-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="34a6a-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="34a6a-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-126">CatchWeight</span></span> | <span data-ttu-id="34a6a-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="34a6a-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="34a6a-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="34a6a-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="34a6a-130">CatchWeightTag</span></span> | <span data-ttu-id="34a6a-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="34a6a-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="34a6a-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="34a6a-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="34a6a-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="34a6a-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="34a6a-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="34a6a-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="34a6a-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="34a6a-136">CheckDigit</span></span> | <span data-ttu-id="34a6a-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="34a6a-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="34a6a-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="34a6a-138">ClusterId</span></span> | <span data-ttu-id="34a6a-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="34a6a-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="34a6a-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="34a6a-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="34a6a-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="34a6a-142">ClusterPosition</span></span> | <span data-ttu-id="34a6a-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="34a6a-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="34a6a-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="34a6a-144">ConfigId</span></span> | <span data-ttu-id="34a6a-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="34a6a-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="34a6a-146">التأكيد</span><span class="sxs-lookup"><span data-stu-id="34a6a-146">Confirmation</span></span> | <span data-ttu-id="34a6a-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="34a6a-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="34a6a-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="34a6a-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="34a6a-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="34a6a-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="34a6a-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="34a6a-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="34a6a-154">ContainerType</span></span> | <span data-ttu-id="34a6a-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="34a6a-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="34a6a-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="34a6a-156">CountingReasonCode</span></span> | <span data-ttu-id="34a6a-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="34a6a-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="34a6a-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="34a6a-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="34a6a-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="34a6a-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="34a6a-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="34a6a-160">CycleCountQty1</span></span> | <span data-ttu-id="34a6a-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="34a6a-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="34a6a-162">CycleCountQty2</span></span> | <span data-ttu-id="34a6a-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="34a6a-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="34a6a-164">CycleCountQty3</span></span> | <span data-ttu-id="34a6a-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="34a6a-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="34a6a-166">CycleCountQty4</span></span> | <span data-ttu-id="34a6a-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="34a6a-168">الترتيب</span><span class="sxs-lookup"><span data-stu-id="34a6a-168">Disposition</span></span> | <span data-ttu-id="34a6a-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="34a6a-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="34a6a-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="34a6a-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="34a6a-172">DriverCheckInId</span></span> | <span data-ttu-id="34a6a-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="34a6a-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="34a6a-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="34a6a-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="34a6a-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="34a6a-176">DriverCheckOutId</span></span> | <span data-ttu-id="34a6a-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="34a6a-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="34a6a-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="34a6a-178">ExpDate</span></span> | <span data-ttu-id="34a6a-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="34a6a-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="34a6a-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-180">FromBatchDisposition</span></span> | <span data-ttu-id="34a6a-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="34a6a-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="34a6a-182">FromInventoryStatus</span></span> | <span data-ttu-id="34a6a-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="34a6a-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="34a6a-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-184">FullQty</span></span> | <span data-ttu-id="34a6a-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="34a6a-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-186">InboundPut</span></span> | <span data-ttu-id="34a6a-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="34a6a-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="34a6a-188">InventBatchId</span></span> | <span data-ttu-id="34a6a-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="34a6a-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="34a6a-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="34a6a-190">InventColorId</span></span> | <span data-ttu-id="34a6a-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="34a6a-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="34a6a-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-192">InventLocation</span></span> | <span data-ttu-id="34a6a-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="34a6a-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="34a6a-194">InventLocationId</span></span> | <span data-ttu-id="34a6a-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="34a6a-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="34a6a-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="34a6a-196">InventSerialId</span></span> | <span data-ttu-id="34a6a-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="34a6a-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="34a6a-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="34a6a-198">InventSizeId</span></span> | <span data-ttu-id="34a6a-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="34a6a-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="34a6a-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="34a6a-200">InventStatusId</span></span> | <span data-ttu-id="34a6a-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="34a6a-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="34a6a-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="34a6a-202">InventStyleId</span></span> | <span data-ttu-id="34a6a-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="34a6a-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="34a6a-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="34a6a-204">InventVersionId</span></span> | <span data-ttu-id="34a6a-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="34a6a-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="34a6a-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="34a6a-206">ItemId</span></span> | <span data-ttu-id="34a6a-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="34a6a-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="34a6a-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="34a6a-208">ITMContainerID</span></span> | <span data-ttu-id="34a6a-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="34a6a-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="34a6a-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="34a6a-210">ITMShipmentID</span></span> | <span data-ttu-id="34a6a-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="34a6a-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="34a6a-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="34a6a-212">KanbanCardId</span></span> | <span data-ttu-id="34a6a-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="34a6a-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="34a6a-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="34a6a-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="34a6a-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="34a6a-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="34a6a-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="34a6a-216">KanbanOrCardId</span></span> | <span data-ttu-id="34a6a-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="34a6a-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="34a6a-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-218">LicensePlateId</span></span> | <span data-ttu-id="34a6a-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="34a6a-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="34a6a-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="34a6a-220">LoadId</span></span> | <span data-ttu-id="34a6a-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="34a6a-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="34a6a-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="34a6a-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="34a6a-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="34a6a-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="34a6a-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-224">LocOrLP</span></span> | <span data-ttu-id="34a6a-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="34a6a-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="34a6a-226">LocOrLP_From</span></span> | <span data-ttu-id="34a6a-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="34a6a-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="34a6a-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="34a6a-228">LocOrLP_To</span></span> | <span data-ttu-id="34a6a-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="34a6a-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="34a6a-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="34a6a-230">LocOrLPCheck</span></span> | <span data-ttu-id="34a6a-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="34a6a-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="34a6a-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-232">LocVerification</span></span> | <span data-ttu-id="34a6a-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="34a6a-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="34a6a-234">LPAdjustIn</span></span> | <span data-ttu-id="34a6a-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="34a6a-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="34a6a-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-236">LPBreakChildLP</span></span> | <span data-ttu-id="34a6a-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="34a6a-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-238">LPBreakParentLP</span></span> | <span data-ttu-id="34a6a-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="34a6a-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-240">LPBuildChildLP</span></span> | <span data-ttu-id="34a6a-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="34a6a-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-242">LPBuildParentLP</span></span> | <span data-ttu-id="34a6a-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="34a6a-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-244">LPVerification</span></span> | <span data-ttu-id="34a6a-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="34a6a-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="34a6a-246">MergeContainerId</span></span> | <span data-ttu-id="34a6a-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="34a6a-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="34a6a-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-248">MixedLPLineNum</span></span> | <span data-ttu-id="34a6a-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="34a6a-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="34a6a-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="34a6a-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="34a6a-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="34a6a-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="34a6a-252">MovementConfirmCancel</span></span> | <span data-ttu-id="34a6a-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="34a6a-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="34a6a-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-254">NewCaptureWeight</span></span> | <span data-ttu-id="34a6a-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="34a6a-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-256">NewQty</span></span> | <span data-ttu-id="34a6a-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="34a6a-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="34a6a-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="34a6a-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="34a6a-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="34a6a-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-260">OutboundPut</span></span> | <span data-ttu-id="34a6a-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="34a6a-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-262">OutboundWeight</span></span> | <span data-ttu-id="34a6a-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="34a6a-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-264">OverridePutNewLocation</span></span> | <span data-ttu-id="34a6a-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="34a6a-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="34a6a-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="34a6a-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-268">POLineNum</span></span> | <span data-ttu-id="34a6a-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="34a6a-270">‏‫رقم أمر الشراء‬</span><span class="sxs-lookup"><span data-stu-id="34a6a-270">PONum</span></span> | <span data-ttu-id="34a6a-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="34a6a-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="34a6a-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="34a6a-272">PositionFull</span></span> | <span data-ttu-id="34a6a-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="34a6a-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="34a6a-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-274">PositionFullQty</span></span> | <span data-ttu-id="34a6a-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="34a6a-276">القوة</span><span class="sxs-lookup"><span data-stu-id="34a6a-276">Potency</span></span> | <span data-ttu-id="34a6a-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="34a6a-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="34a6a-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="34a6a-278">PrinterName</span></span> | <span data-ttu-id="34a6a-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="34a6a-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="34a6a-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="34a6a-280">ProdId</span></span> | <span data-ttu-id="34a6a-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="34a6a-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="34a6a-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="34a6a-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="34a6a-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-284">ProductConfirmation</span></span> | <span data-ttu-id="34a6a-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="34a6a-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="34a6a-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="34a6a-288">وضع</span><span class="sxs-lookup"><span data-stu-id="34a6a-288">Put</span></span> | <span data-ttu-id="34a6a-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="34a6a-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="34a6a-290">PutawayClusterId</span></span> | <span data-ttu-id="34a6a-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="34a6a-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="34a6a-292">الكمية</span><span class="sxs-lookup"><span data-stu-id="34a6a-292">Qty</span></span> | <span data-ttu-id="34a6a-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="34a6a-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="34a6a-294">QtyAdjust</span></span> | <span data-ttu-id="34a6a-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="34a6a-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="34a6a-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="34a6a-296">QtyShort</span></span> | <span data-ttu-id="34a6a-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="34a6a-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="34a6a-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="34a6a-298">QtyToConsume</span></span> | <span data-ttu-id="34a6a-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="34a6a-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="34a6a-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="34a6a-300">QtyToPick</span></span> | <span data-ttu-id="34a6a-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="34a6a-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="34a6a-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-302">QtyToPut</span></span> | <span data-ttu-id="34a6a-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="34a6a-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="34a6a-304">QtyToScrap</span></span> | <span data-ttu-id="34a6a-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="34a6a-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="34a6a-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-306">QtyVerification</span></span> | <span data-ttu-id="34a6a-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="34a6a-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="34a6a-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="34a6a-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="34a6a-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="34a6a-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="34a6a-310">ReasonString</span></span> | <span data-ttu-id="34a6a-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="34a6a-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="34a6a-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="34a6a-312">RecvLocationId</span></span> | <span data-ttu-id="34a6a-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="34a6a-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="34a6a-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="34a6a-314">RemoveContainerId</span></span> | <span data-ttu-id="34a6a-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="34a6a-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="34a6a-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="34a6a-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="34a6a-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="34a6a-318">RMANum</span></span> | <span data-ttu-id="34a6a-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="34a6a-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="34a6a-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="34a6a-320">ShortPickReason</span></span> | <span data-ttu-id="34a6a-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="34a6a-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="34a6a-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-322">SortConOrLP</span></span> | <span data-ttu-id="34a6a-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="34a6a-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-324">SortLicensePlateId</span></span> | <span data-ttu-id="34a6a-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="34a6a-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="34a6a-326">SortPositionId</span></span> | <span data-ttu-id="34a6a-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="34a6a-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="34a6a-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-328">SortVerification</span></span> | <span data-ttu-id="34a6a-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="34a6a-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="34a6a-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="34a6a-330">StartLocationId</span></span> | <span data-ttu-id="34a6a-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="34a6a-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="34a6a-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="34a6a-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="34a6a-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-334">TargetLicensePlateId</span></span> | <span data-ttu-id="34a6a-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="34a6a-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-336">TOLineNum</span></span> | <span data-ttu-id="34a6a-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="34a6a-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-338">ToLocation</span></span> | <span data-ttu-id="34a6a-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="34a6a-340">TONum</span><span class="sxs-lookup"><span data-stu-id="34a6a-340">TONum</span></span> | <span data-ttu-id="34a6a-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="34a6a-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="34a6a-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="34a6a-342">ToWarehouse</span></span> | <span data-ttu-id="34a6a-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="34a6a-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="34a6a-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="34a6a-344">TransportLoadId</span></span> | <span data-ttu-id="34a6a-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="34a6a-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="34a6a-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="34a6a-346">WaveLabelId</span></span> | <span data-ttu-id="34a6a-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="34a6a-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="34a6a-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-348">WaveLblQty</span></span> | <span data-ttu-id="34a6a-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="34a6a-350">الوزن</span><span class="sxs-lookup"><span data-stu-id="34a6a-350">Weight</span></span> | <span data-ttu-id="34a6a-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="34a6a-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="34a6a-352">WeightToConsume</span></span> | <span data-ttu-id="34a6a-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="34a6a-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="34a6a-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="34a6a-354">WHSAdjustmentType</span></span> | <span data-ttu-id="34a6a-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="34a6a-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="34a6a-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="34a6a-356">WHSReceivingException</span></span> | <span data-ttu-id="34a6a-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="34a6a-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="34a6a-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="34a6a-358">WHSWorkException</span></span> | <span data-ttu-id="34a6a-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="34a6a-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="34a6a-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="34a6a-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="34a6a-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="34a6a-362">WMSLocationId</span></span> | <span data-ttu-id="34a6a-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="34a6a-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="34a6a-364">WorkId</span></span> | <span data-ttu-id="34a6a-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="34a6a-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="34a6a-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="34a6a-366">WorkIdToCancel</span></span> | <span data-ttu-id="34a6a-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="34a6a-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="34a6a-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="34a6a-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="34a6a-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="34a6a-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="34a6a-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="34a6a-370">WorkPoolId</span></span> | <span data-ttu-id="34a6a-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="34a6a-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="34a6a-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="34a6a-372">ZoneId</span></span> | <span data-ttu-id="34a6a-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="34a6a-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="34a6a-374">رموز الخطوة المتوفرة</span><span class="sxs-lookup"><span data-stu-id="34a6a-374">Available step icons</span></span>

<span data-ttu-id="34a6a-375">يتضمن النظام مجموعة من رموز الخطوة القياسية التي يمكنك استخدامها أيضًا للخطوات المخصصة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="34a6a-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="34a6a-376">لا يمكنك تحميل رموز الخطوات المخصصة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="34a6a-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="34a6a-377">وبالتالي، يجب عليك دائمًا تحديد أحد رموز الخطوة القياسية.</span><span class="sxs-lookup"><span data-stu-id="34a6a-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="34a6a-378">يعرض الجدول التالي كل رمز خطوة قياسية متوفر حاليًا، واسمه.</span><span class="sxs-lookup"><span data-stu-id="34a6a-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="حول رمز الخطوة"><br><span data-ttu-id="34a6a-380">حول</span><span class="sxs-lookup"><span data-stu-id="34a6a-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="إضافة لوحة ترخيص أو رمز خطوة صنف"><br><span data-ttu-id="34a6a-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="34a6a-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="رمز خطوة إرجاع الدفعة"><br><span data-ttu-id="34a6a-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="رمز خطوة الكاريرية"><br><span data-ttu-id="34a6a-386">الناقل</span><span class="sxs-lookup"><span data-stu-id="34a6a-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="رمز خطوة العلامة الخاصة بوزن التعبئة"><br><span data-ttu-id="34a6a-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="34a6a-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="رمز خطوة وزن علامة وزن التعبئة"><br><span data-ttu-id="34a6a-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="رمز خطوة رقم الفحص"><br><span data-ttu-id="34a6a-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="34a6a-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="رمز خطوة معرف الإيداع والسحب"><br><span data-ttu-id="34a6a-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="34a6a-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="رمز خطوة لوحة الترخيص التابعة"><br><span data-ttu-id="34a6a-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="رمز خطوة معرف نظام المجموعة"><br><span data-ttu-id="34a6a-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="34a6a-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="رمز خطوة موضع نظام المجموعة"><br><span data-ttu-id="34a6a-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="34a6a-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="رمز تكوين خطوة المعرف"><br><span data-ttu-id="34a6a-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="34a6a-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="رمز خطوة الحقل المكون"><br><span data-ttu-id="34a6a-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="34a6a-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="رمز خطوة التجميع أو لوحة الترخيص"><br><span data-ttu-id="34a6a-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="تجميع من رمز خطوة معرف لوح الترخيص"><br><span data-ttu-id="34a6a-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="34a6a-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="تجميع لرمز خطوة معرف لوح الترخيص"><br><span data-ttu-id="34a6a-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="34a6a-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="رمز خطوة نوع الحاوية"><br><span data-ttu-id="34a6a-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="34a6a-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="رمز خطوة الجرد"><br><span data-ttu-id="34a6a-414">الجرد</span><span class="sxs-lookup"><span data-stu-id="34a6a-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="رمز خطوة كود سبب الجرد"><br><span data-ttu-id="34a6a-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="34a6a-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="رمز خطوة كود بلد المنشأ"><br><span data-ttu-id="34a6a-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="34a6a-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="رمز خطوة الإرجاع"><br><span data-ttu-id="34a6a-420">الترتيب</span><span class="sxs-lookup"><span data-stu-id="34a6a-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="رمز خطوة الإكمال"><br><span data-ttu-id="34a6a-422">تم</span><span class="sxs-lookup"><span data-stu-id="34a6a-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="رمز خطوة تأكيد ‏‫تسجيل دخول السائق‬"><br><span data-ttu-id="34a6a-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="رمز خطوة معرف ‏‫تسجيل دخول السائق‬"><br><span data-ttu-id="34a6a-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="34a6a-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="رمز خطوة معرف ‏‫تسجيل خروج السائق‬"><br><span data-ttu-id="34a6a-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="34a6a-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="رمز خطوة تاريخ انتهاء الصلاحية"><br><span data-ttu-id="34a6a-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="34a6a-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="رمز خطوة الحقل"><br><span data-ttu-id="34a6a-432">الحقل</span><span class="sxs-lookup"><span data-stu-id="34a6a-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="رمز خطوة إرجاع من الدفعة"><br><span data-ttu-id="34a6a-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="34a6a-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="رمز خطوة حالة من المخزون"><br><span data-ttu-id="34a6a-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="34a6a-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="رمز خطوة سمة المعرف"><br><span data-ttu-id="34a6a-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="34a6a-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="رمز خطوة معرف دفعة المخزون"><br><span data-ttu-id="34a6a-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="34a6a-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="رمز خطوة معرف لون المخزون"><br><span data-ttu-id="34a6a-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="34a6a-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="رمز خطوة موقع المخزون"><br><span data-ttu-id="34a6a-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="رمز خطوة المعرف التسلسلي للمخزون"><br><span data-ttu-id="34a6a-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="34a6a-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="رمز خطوة معرف حجم المخزون"><br><span data-ttu-id="34a6a-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="34a6a-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="رمز خطوة معرف حالة المخزون"><br><span data-ttu-id="34a6a-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="34a6a-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="رمز خطوة معرف نمط المخزون"><br><span data-ttu-id="34a6a-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="34a6a-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="رمز خطوة معرفإصدار المخزون"><br><span data-ttu-id="34a6a-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="34a6a-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="رمز خطوة معرف الصنف"><br><span data-ttu-id="34a6a-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="34a6a-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="رمز خطوة معرف حاوية ITM"><br><span data-ttu-id="34a6a-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="34a6a-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="رمز خطوة معرف شحن ITM"><br><span data-ttu-id="34a6a-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="34a6a-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="رمز خطوة معرف بطاقة كانبان"><br><span data-ttu-id="34a6a-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="34a6a-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="رمز خطوة معرف بطاقة أو كانبان"><br><span data-ttu-id="34a6a-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="34a6a-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="رمز خطوة معرف لوحة الترخيص"><br><span data-ttu-id="34a6a-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="34a6a-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="رمز خطوة معرف الحمل"><br><span data-ttu-id="34a6a-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="34a6a-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="رمز ‏‫خطوة موضع لوحة ترخيص الموقع"><br><span data-ttu-id="34a6a-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="34a6a-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="رمز خطوة لوحة الترخيص أو موقع"><br><span data-ttu-id="34a6a-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="رمز خطوة فحص لوحة الترخيص أو موقع"><br><span data-ttu-id="34a6a-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="34a6a-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="رمز فحص لوحة الترخيص أو موقع من خطوة"><br><span data-ttu-id="34a6a-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="34a6a-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="رمز لوحة الترخيص أو موقع لخطوة"><br><span data-ttu-id="34a6a-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="34a6a-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="رمز خطوة عملية طويلة مكتملة"><br><span data-ttu-id="34a6a-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="34a6a-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="رمز خطوة لوحة الترخيص الأصلية لفاصل لوحة الترخيص"><br><span data-ttu-id="34a6a-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="رمز خطوة دمج معرف حاوية"><br><span data-ttu-id="34a6a-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="34a6a-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="رمز خطوة لوحة ترخيص مستخدم مختلطة"><br><span data-ttu-id="34a6a-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="رمز خطوة الوزن الخارجي"><br><span data-ttu-id="34a6a-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="34a6a-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="رمز خطوة المالك"><br><span data-ttu-id="34a6a-490">المالك</span><span class="sxs-lookup"><span data-stu-id="34a6a-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="رمز خطوة لوحة الترخيص الأصلية"><br><span data-ttu-id="34a6a-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="34a6a-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="الرجاء التأكيد على رمز الخطوة"><br><span data-ttu-id="34a6a-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="34a6a-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="رمز خطوة رقم بند أمر الشراء"><br><span data-ttu-id="34a6a-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="رمز خطوة رقم أمر الشراء"><br><span data-ttu-id="34a6a-498">‏‫رقم أمر الشراء‬</span><span class="sxs-lookup"><span data-stu-id="34a6a-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="رمز خطوة موضع كامل"><br><span data-ttu-id="34a6a-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="34a6a-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="رمز خطوة القوة"><br><span data-ttu-id="34a6a-502">القوة</span><span class="sxs-lookup"><span data-stu-id="34a6a-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="رمز خطوة اسم الطابعة"><br><span data-ttu-id="34a6a-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="34a6a-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="رمز خطوة معرف المنتج"><br><span data-ttu-id="34a6a-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="34a6a-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="رمز خطوة تأكيد المنتج"><br><span data-ttu-id="34a6a-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="وضع رمز الخطوة"><br><span data-ttu-id="34a6a-510">وضع</span><span class="sxs-lookup"><span data-stu-id="34a6a-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="رمز خطوة معرف نظام مجموعة التخزين"><br><span data-ttu-id="34a6a-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="34a6a-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="رمز خطوة الكمية"><br><span data-ttu-id="34a6a-514">الكمية</span><span class="sxs-lookup"><span data-stu-id="34a6a-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="تعديل الكمية في رمز الخطوة"><br><span data-ttu-id="34a6a-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="34a6a-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="رمز خطوة الكمية الصغيرة"><br><span data-ttu-id="34a6a-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="34a6a-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="رمز خطوة الكمية المطلوب استهلاكها"><br><span data-ttu-id="34a6a-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="34a6a-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="رمز خطوة الكمية المطلوب وضعها"><br><span data-ttu-id="34a6a-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="34a6a-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="رمز خطوة الكمية المطلوب تخريدها"><br><span data-ttu-id="34a6a-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="34a6a-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="رمز خطوة تأكيد الكمية"><br><span data-ttu-id="34a6a-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="34a6a-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="رمز خطوة الإبلاغ كوظيفة منتهية"><br><span data-ttu-id="34a6a-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="34a6a-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="رمز خطوة معرف موقع الاستلام"><br><span data-ttu-id="34a6a-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="34a6a-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="رمز خطوة إزالة معرف حاوية"><br><span data-ttu-id="34a6a-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="34a6a-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="رمز خطوة رقم RMA"><br><span data-ttu-id="34a6a-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="34a6a-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="رمز خطوة تحديد الأمر"><br><span data-ttu-id="34a6a-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="34a6a-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="رمز خطوة سبب انتقاء قصير"><br><span data-ttu-id="34a6a-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="34a6a-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="رمز خطوة معرف موضع الفرز"><br><span data-ttu-id="34a6a-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="34a6a-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="رمز خطوة معرف لوحة الترخيص الهدف"><br><span data-ttu-id="34a6a-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="رمز خطوة لرقم السطر"><br><span data-ttu-id="34a6a-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="رمز خطوة لموقع"><br><span data-ttu-id="34a6a-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="34a6a-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="رمز خطوة لرقم"><br><span data-ttu-id="34a6a-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="34a6a-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="رمز خطوة لمستودع"><br><span data-ttu-id="34a6a-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="34a6a-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="رمز خطوة معرف حمل النقل"><br><span data-ttu-id="34a6a-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="34a6a-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="رمز خطوة معرف دفعة المورد"><br><span data-ttu-id="34a6a-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="34a6a-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="رمز خطوة معرف تسمية الموجة"><br><span data-ttu-id="34a6a-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="34a6a-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="رمز خطوة كمية تسمية الموجة"><br><span data-ttu-id="34a6a-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="34a6a-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="رمز خطوة الوزن"><br><span data-ttu-id="34a6a-560">الوزن</span><span class="sxs-lookup"><span data-stu-id="34a6a-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="رمز خطوة الوزن المطلوب استهلاكه"><br><span data-ttu-id="34a6a-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="34a6a-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="رمز خطوة نوع تسوية WHS"><br><span data-ttu-id="34a6a-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="34a6a-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="رمز خطوة استثناء استلام WHS"><br><span data-ttu-id="34a6a-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="34a6a-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="رمز خطوة معرف موقع WMS"><br><span data-ttu-id="34a6a-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="34a6a-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="رمز خطوة معرف العمل"><br><span data-ttu-id="34a6a-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="34a6a-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="رمز خطوة إلغاء معرف العمل للإلغاء"><br><span data-ttu-id="34a6a-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="34a6a-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="رمز خطوة معرف لوحة ترخيص العمل"><br><span data-ttu-id="34a6a-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="34a6a-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="رمز خطوة نظام مجموعة تخزين معرف لوحة ترخيص العمل"><br><span data-ttu-id="34a6a-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="34a6a-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="رمز خطوة معرف وعاء العمل"><br><span data-ttu-id="34a6a-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="34a6a-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="رمز خطوة معرف المنطقة"><br><span data-ttu-id="34a6a-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="34a6a-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="34a6a-581">مثال: تعيين رموز وعناوين الخطوات لتدفق مخصص</span><span class="sxs-lookup"><span data-stu-id="34a6a-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="34a6a-582">يوضح هذا المثال كيفية إعداد رموز وعناوين الخطوات لتدفق مهمة مخصصة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="34a6a-583">يتم إنشاء السيناريو على مثال لتدفق مهمة مخصصة يتم تقديمها واستكشافها بمزيد من التفصيل في نشر المدونة التالي: [تخصيص تطبيق المستودع للأجهزة](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="34a6a-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="34a6a-584">يعمل تدفق المهام بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="34a6a-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="34a6a-585">ويقوم التطبيق بإظهار صفحة تطالب العامل بتقديم معرف حاوية (على سبيل المثال، عن طريق مسح كود شريطي).</span><span class="sxs-lookup"><span data-stu-id="34a6a-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="34a6a-586">إذا كان معرف الحاوية صالحًا، يقوم التطبيق بفتح صفحة جديدة تطالب العامل بالوزن.</span><span class="sxs-lookup"><span data-stu-id="34a6a-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="34a6a-587">(إذا كان معرف الحاوية غير صالح، يتم إرجاع العامل إلى الصفحة الأولى.)</span><span class="sxs-lookup"><span data-stu-id="34a6a-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="34a6a-588">عندما يدخل العامل وزن صالح، يقوم النظام بتخزين الوزن وإرجاع العامل إلى الصفحة الأولى.</span><span class="sxs-lookup"><span data-stu-id="34a6a-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="34a6a-589">يبين الرسم التوضيحي التالي تدفق هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="34a6a-590">![الرسم التخطيطي لسير المهمة](media/step-icons-example-task-flow.png "الرسم التخطيطي لسير المهمة")</span><span class="sxs-lookup"><span data-stu-id="34a6a-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="34a6a-591">إنشاء فئة خطوة لصفحة إدخال الحاوية</span><span class="sxs-lookup"><span data-stu-id="34a6a-591">Create a step class for the container input page</span></span>

<span data-ttu-id="34a6a-592">تتيح صفحة إدخال الحاوية فحص العامل أو إدخال معرف الحاوية.</span><span class="sxs-lookup"><span data-stu-id="34a6a-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="34a6a-593">![صفحة إدخال الحاوية](media/step-icons-example-container-input.png "صفحة إدخال الحاوية")</span><span class="sxs-lookup"><span data-stu-id="34a6a-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="34a6a-594">في الصفحة "إدخال الحاوية"، اسم عنصر التحكم الخاص بحقل الإدخال هو `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="34a6a-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="34a6a-595">نظرًا لأن اسم عنصر التحكم هذا ليس في [قائمة معرفات الخطوات](#step-ids-classes)، فلن تجد خطوة موجودة تستند إليه.</span><span class="sxs-lookup"><span data-stu-id="34a6a-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="34a6a-596">ولذلك، يجب عليك إنشاء فئة خطوة تمثل الخطوة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="34a6a-597">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="34a6a-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="34a6a-598">يتم تخزين معرف رمز الخطوة في عضو الفئة `defaultStepIcon`، ويتم تخزين عنوان الخطوة في عضو الفئة `defaultStepTitle`.</span><span class="sxs-lookup"><span data-stu-id="34a6a-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="34a6a-599">لتعيين رمز خطوة، قم بتعيين `defaultStepIcon` لأحد معرفات الرموز التي يتم سردها في القسم [رموز الخطوات المتوفرة](#step-icons) سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="34a6a-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="34a6a-600">استخدام رمز خطوة قياسية أو مخصصة وعنوان لإدخال الوزن</span><span class="sxs-lookup"><span data-stu-id="34a6a-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="34a6a-601">تتيح صفحة إدخال الوزن للعامل إدخال وزن.</span><span class="sxs-lookup"><span data-stu-id="34a6a-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="34a6a-602">![صفحة إدخال الوزن](media/step-icons-example-weight-input.png "صفحة إدخال الوزن")</span><span class="sxs-lookup"><span data-stu-id="34a6a-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="34a6a-603">في الصفحة إدخال الوزن، اسم عنصر التحكم الخاص بحقل الإدخال هو `Weight`، والموجود في [قائمة معرفات الخطوات](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="34a6a-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="34a6a-604">لذلك، إذا كان رمز وعنوان الخطوة اللذين يتم تعريفهما في الفئة `WHSMobileAppStepWeight` مقبولان بالنسبة إليك، فلن تحتاج إلى تغيير أي شيء لهذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="34a6a-605">ومع ذلك، إذا كنت تفضل استخدام رمز أو عنوان مختلف لهذه الخطوة، فإنه يمكنك منع إما الأسلوب `stepId()` أو الأسلوب `stepInfo()` في فئة المنشئ.</span><span class="sxs-lookup"><span data-stu-id="34a6a-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="34a6a-606">يحتوي كل تدفق مهام على منشئ معلومات الخطوة الخاص به.</span><span class="sxs-lookup"><span data-stu-id="34a6a-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="34a6a-607">منع أسلوب stepId()</span><span class="sxs-lookup"><span data-stu-id="34a6a-607">Override the stepId() method</span></span>

<span data-ttu-id="34a6a-608">يظهر المثال التالي طريقة واحدة يمكنك من خلالها تعديل فئة منشئ بواسطة منع الأسلوب `stepId()`.</span><span class="sxs-lookup"><span data-stu-id="34a6a-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="34a6a-609">ثم تقوم بعد ذلك بإنشاء فئة خطوة للخطوة `NewWeight`.</span><span class="sxs-lookup"><span data-stu-id="34a6a-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="34a6a-610">يجب أن يتشابه الرمز مع الرمز الخاص بالمثال `ContainerId` الذي تم إظهاره سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="34a6a-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="34a6a-611">منع أسلوب stepInfo()</span><span class="sxs-lookup"><span data-stu-id="34a6a-611">Override the stepInfo() method</span></span>

<span data-ttu-id="34a6a-612">يظهر المثال التالي طريقة واحدة يمكنك من خلالها تعديل فئة منشئ بواسطة منع الأسلوب `stepInfo()`.</span><span class="sxs-lookup"><span data-stu-id="34a6a-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="34a6a-613">قم بعد ذلك بإنشاء كائن `WHSMobileAppStepInfo`، وقم بتعيين الرمز و/أو العنوان مباشرة.</span><span class="sxs-lookup"><span data-stu-id="34a6a-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34a6a-614">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="34a6a-614">Additional resources</span></span>

- [<span data-ttu-id="34a6a-615">تثبيت تطبيق إدارة المستودع للأجهزة المحمولة والاتصال به</span><span class="sxs-lookup"><span data-stu-id="34a6a-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="34a6a-616">إعدادات مستخدم الجهاز المحمول</span><span class="sxs-lookup"><span data-stu-id="34a6a-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
