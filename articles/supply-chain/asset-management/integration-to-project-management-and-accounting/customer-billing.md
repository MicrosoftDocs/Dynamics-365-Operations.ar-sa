---
title: فوتره للصيانة علي أصول مملوكه للعملاء
description: يوضح هذا الموضوع كيفيه إنشاء ومعالجه وعمل الصيانة الخاصة بالمواد التي يتم القيام بها في الأصول الخاصة بالعملاء.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5532f1ce14239002022f487f227286efe10abf12
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813787"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="0a41c-103">فوتره للصيانة علي أصول مملوكه للعملاء</span><span class="sxs-lookup"><span data-stu-id="0a41c-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a41c-104">تتيح لك ميزه *الفوترة الخاصة بامر العمل* إنشاء ومعالجه وعمل الصيانة التي يتم القيام بها في الأصول التي يمتلكها العملاء.</span><span class="sxs-lookup"><span data-stu-id="0a41c-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="0a41c-105">تُمكّنك هذه الميزة من تنفيذ المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="0a41c-106">قم بتوصيل العملاء بالأصول الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="0a41c-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="0a41c-107">حدد عميلا وقم بعرض الأصول التي يملكها العميل عند إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="0a41c-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="0a41c-108">قم باعداد مشروع رئيسي لكل عميل.</span><span class="sxs-lookup"><span data-stu-id="0a41c-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="0a41c-109">قم بتسجيل الساعات والأصناف والمصروفات والرسوم مقابل أمر العمل، ثم قم بإنشاء مقترح فاتورة للعميل فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="0a41c-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="0a41c-110">بالاضافه إلى ذلك، توفر الميزة الوظائف التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="0a41c-111">يتم نسخ عقد المشروع من المشروع الرئيسي للعميل تلقائيا إلى مشروع أمر العمل ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="0a41c-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="0a41c-112">يمكن الآن لأداره الأصول استخدام نوع حركه مشروع *الرسوم* في كل من تنبؤات أمر العمل ودفاتر يوميه أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="0a41c-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="0a41c-113">تشغيل ميزة فوترة العميل</span><span class="sxs-lookup"><span data-stu-id="0a41c-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="0a41c-114">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="0a41c-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="0a41c-115">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="0a41c-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="0a41c-116">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="0a41c-117">**الوحدة النمطية:** *إدارة المشاريع ومحاسبتها*</span><span class="sxs-lookup"><span data-stu-id="0a41c-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="0a41c-118">**اسم الميزة:** *فوتره أمر العمل*</span><span class="sxs-lookup"><span data-stu-id="0a41c-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0a41c-119">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="0a41c-119">Example scenario</span></span>

<span data-ttu-id="0a41c-120">لمعرفه كيفيه عمل هذه الميزة، قم بالعمل من خلال سيناريو المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="0a41c-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="0a41c-121">للعمل بهذا السيناريو باستخدام السجلات والقيم النموذجية المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) القياسية.</span><span class="sxs-lookup"><span data-stu-id="0a41c-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="0a41c-122">يجب تحديد الكيان القانوني **USMF** قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="0a41c-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="0a41c-123">يمكنك أيضًا استخدام هذا السيناريو كإرشاد لاستخدام الميزة عند العمل في نظام إنتاج.</span><span class="sxs-lookup"><span data-stu-id="0a41c-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="0a41c-124">مع ذلك، في هذه الحالة، يجب استبدال القيم الخاصة بك، وقد تفقد بعض أنواع السجلات المطلوبة التي توفرها بيانات العرض التوضيحي القياسية.</span><span class="sxs-lookup"><span data-stu-id="0a41c-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="0a41c-125">الخطوة 1: إنشاء عقد مشروع جديد للعميل</span><span class="sxs-lookup"><span data-stu-id="0a41c-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="0a41c-126">انتقل إلى **إدارة المشاريع والمحاسبة \> المشاريع \> عقود المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="0a41c-127">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a41c-128">في مربع حوار **عقد مشروع جديد**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0a41c-129">**الاسم:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="0a41c-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="0a41c-130">**نوع التمويل:** *العميل*</span><span class="sxs-lookup"><span data-stu-id="0a41c-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="0a41c-131">**مصدر التمويل:** *US-013* ( *Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="0a41c-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="0a41c-132">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="0a41c-133">الخطوة 2: إنشاء مشروع رئيسي جديد للعميل</span><span class="sxs-lookup"><span data-stu-id="0a41c-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="0a41c-134">سيتم استخدام المشروع الرئيسي الذي تقوم بإنشاءه هنا عند إنشاء أوامر العمل الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="0a41c-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="0a41c-135">انتقل **إلى إدارة المشاريع والمحاسبة \> المشاريع \> كافة المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="0a41c-136">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a41c-137">في مربع الحوار **مشروع جديد**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0a41c-138">**نوع المشروع:** *الوقت والمواد‬*</span><span class="sxs-lookup"><span data-stu-id="0a41c-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="0a41c-139">**اسم المشروع:** *أوامر عمل Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="0a41c-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="0a41c-140">**مجموعة المشروع:** *TM*</span><span class="sxs-lookup"><span data-stu-id="0a41c-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="0a41c-141">**معرف عقد المشروع:** *Pelican Wholesales* (العقد الذي قمت بإنشاءه سابقا)</span><span class="sxs-lookup"><span data-stu-id="0a41c-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="0a41c-142">**تاريخ البدء:** حدد تاريخ اليوم.</span><span class="sxs-lookup"><span data-stu-id="0a41c-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="0a41c-143">حدد **إنشاء المشروع**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-143">Select **Create project**.</span></span>
1. <span data-ttu-id="0a41c-144">يفتح المشروع الجديد.</span><span class="sxs-lookup"><span data-stu-id="0a41c-144">The new project is opened.</span></span> <span data-ttu-id="0a41c-145">دوِّن ملاحظة بقيمة **مُعرف المشروع**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="0a41c-146">سيتعين عليك إدخالها في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="0a41c-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="0a41c-147">الخطوة 3: إنشاء نوع أمر عمل جديد في أداره الأصول</span><span class="sxs-lookup"><span data-stu-id="0a41c-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="0a41c-148">انتقل إلى **إدارة الأصول \> الإعداد \> أوامر العمل \> أنواع أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="0a41c-149">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a41c-150">تتم إضافة سجل جديد إلى القائمة.</span><span class="sxs-lookup"><span data-stu-id="0a41c-150">A new record is added to the list.</span></span> <span data-ttu-id="0a41c-151">قم بتعيين القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="0a41c-151">Set the following values for it:</span></span>

    - <span data-ttu-id="0a41c-152">**نوع أمر العمل:** *الخدمة*</span><span class="sxs-lookup"><span data-stu-id="0a41c-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="0a41c-153">**الاسم:** *أوامر عمل الخدمة*</span><span class="sxs-lookup"><span data-stu-id="0a41c-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="0a41c-154">**حالة دورة حياة أمر العمل:** *قياسي*</span><span class="sxs-lookup"><span data-stu-id="0a41c-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="0a41c-155">الخطوة 4: ربط حساب العميل بالمشروع الرئيسي</span><span class="sxs-lookup"><span data-stu-id="0a41c-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="0a41c-156">يجب الآن ربط حساب العميل بالمشروع الرئيسي في اعداد المشروع في أداره الأصول.</span><span class="sxs-lookup"><span data-stu-id="0a41c-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="0a41c-157">انتقل إلى **إدارة الأصول \> الإعداد \> أوامر العمل \> إعداد المشروع**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="0a41c-158">في علامة التبويب **المشروع الرئيسي**، حدد **إضافة** لإضافة سطر.</span><span class="sxs-lookup"><span data-stu-id="0a41c-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="0a41c-159">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0a41c-160">**حساب العميل:** *US-013* ( *Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="0a41c-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="0a41c-161">**معرف المشروع:** ادخل معرف المشروع الذي قمت بتسجيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="0a41c-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="0a41c-162">الخطوة 5: ربط مجموعه المشروع والنوع بمشروع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="0a41c-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="0a41c-163">يجب ان تظل في **صفحه اعداد المشروع** (**أداره الأصول \> اعداد \> أوامر العمل \> إعداد المشروع**).</span><span class="sxs-lookup"><span data-stu-id="0a41c-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="0a41c-164">في علامة التبويب **مجموعة المشروعات**، حدد **إضافة** لإضافة سطر.</span><span class="sxs-lookup"><span data-stu-id="0a41c-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="0a41c-165">في البند الجديد، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="0a41c-166">**نوع أمر العمل:** *خدمه* (نوع أمر العمل الذي قمت بإنشاءه سابقا)</span><span class="sxs-lookup"><span data-stu-id="0a41c-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="0a41c-167">**مجموعة المشروع:** *TM*</span><span class="sxs-lookup"><span data-stu-id="0a41c-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="0a41c-168">يتم دائما توارث عقد المشروع في مشروع أمر العمل من المشروع الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="0a41c-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="0a41c-169">الخطوة 6: ربط أصل بمعرف العميل</span><span class="sxs-lookup"><span data-stu-id="0a41c-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="0a41c-170">انتقل إلى **إدارة الأصول \> الأصول \> تنشيط الأصول**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="0a41c-171">في الحقل **عامل التصفية**، ادخل الخيار *VE-102*، ثم حدد للتصفية حسب **الأصل**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="0a41c-172">حدد الأصل لفتح إعداداته.</span><span class="sxs-lookup"><span data-stu-id="0a41c-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="0a41c-173">في علامة التبويب السريعة **العميل**، قم بتعيين حقل **حساب العميل** إلى *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="0a41c-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="0a41c-174">يتم تحديث حقل **الاسم** تلقائيا إلى *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="0a41c-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="0a41c-175">الخطوة 7: إنشاء نوع أمر عمل جديد في الأصل</span><span class="sxs-lookup"><span data-stu-id="0a41c-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="0a41c-176">انتقل إلى **إدارة الأصول \> أوامر العمل \>تنشيط أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="0a41c-177">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a41c-178">في مربع الحوار **إنشاء أمر العمل**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a41c-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="0a41c-179">**نوع أمر العمل:** *الخدمة*</span><span class="sxs-lookup"><span data-stu-id="0a41c-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="0a41c-180">**الوصف:** *إصلاح الشاحنة*</span><span class="sxs-lookup"><span data-stu-id="0a41c-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="0a41c-181">**حساب العميل:** *US-013* ( *Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="0a41c-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="0a41c-182">**الأصل:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="0a41c-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="0a41c-183">يعرض البحث الأصول المرتبطة بحساب العميل المحدد فقط.</span><span class="sxs-lookup"><span data-stu-id="0a41c-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="0a41c-184">**نوع مهمة الصيانة:** *إصلاح*</span><span class="sxs-lookup"><span data-stu-id="0a41c-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="0a41c-185">**التجارة:** *ميكانيكي*</span><span class="sxs-lookup"><span data-stu-id="0a41c-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="0a41c-186">**مستوى الخدمة:** *4*</span><span class="sxs-lookup"><span data-stu-id="0a41c-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="0a41c-187">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="0a41c-188">الخطوة 8: مراجعه أمر العمل والبدء في العمل عليه</span><span class="sxs-lookup"><span data-stu-id="0a41c-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="0a41c-189">في هذا المقطع ، ستعمل علي ترتيب العمل الذي قمت بإنشاءه في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="0a41c-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="0a41c-190">اتبع الخطوات التالية للتحقق من ان المشروع الرئيسي هو مشروع *أمر العمل Pelican wholesales*:</span><span class="sxs-lookup"><span data-stu-id="0a41c-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="0a41c-191">في القسم **مهام الصيانة لأمر العمل**، حدد بندا.</span><span class="sxs-lookup"><span data-stu-id="0a41c-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="0a41c-192">في علامة التبويب السريعة **تفاصيل السطر**، افحص قيمه **معرف المشروع**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="0a41c-193">يجب ان يكون رقم الواصلة في النموذج *\<Parent-Project-ID\>-\<Project-ID\>*</span><span class="sxs-lookup"><span data-stu-id="0a41c-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="0a41c-194">هذه القيمة عبارة عن ارتباط.</span><span class="sxs-lookup"><span data-stu-id="0a41c-194">This value is a link.</span></span>
    1. <span data-ttu-id="0a41c-195">حدد ارتباط معرف المشروع لفتح الصفحة التي يمكنك من خلالها عرض المشروع الرئيسي وأسماء المشاريع.</span><span class="sxs-lookup"><span data-stu-id="0a41c-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="0a41c-196">في جزء الإجراءات، ضمن علامة التبويب **أمر العمل**، في مجموعة **‏حالة دورة الحياة**، حدد **تحديث حالة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="0a41c-197">في مربع الحوار **تحديث حاله أمر العمل** ، في العمود **تحديد**، حدد خانه الاختيار للصف الذي تم فيه تعيين حقل **حاله دوره الحياة** إلى قيد *التقدم*.</span><span class="sxs-lookup"><span data-stu-id="0a41c-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="0a41c-198">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-198">Select **OK**.</span></span>
1. <span data-ttu-id="0a41c-199">في مربع الحوار **حاله دوره الحياة: قيد التقدم**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="0a41c-200">الخطوة 9: ترحيل الساعات التي تم قضاؤها في أمر العمل وإنشاء مقترح فاتورة جديد</span><span class="sxs-lookup"><span data-stu-id="0a41c-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="0a41c-201">في هذا المقطع ، ستواصل ترتيب العمل الذي قمت عملت فيه في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="0a41c-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="0a41c-202">في جزء الإجراءات, على علامة التبويب **أمر العمل**، في المجموعة **المشروع**، حدد **دفاتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="0a41c-203">تظهر الصفحة **دفاتر يوميه أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="0a41c-204">يمكنك هنا تسجيل الوقت الذي استغرقته في أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="0a41c-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="0a41c-205">على علامة التبويب السريعة **الساعات** ، حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="0a41c-206">في بند جديد، قم بتعيين **حقل الساعات** إلى *4*.</span><span class="sxs-lookup"><span data-stu-id="0a41c-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="0a41c-207">في جزء الإجراءات، حدد **دفاتر يومية الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="0a41c-208">قم بإغلاق الصفحة **دفاتر يوميه أمر العمل** للرجوع إلى أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="0a41c-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="0a41c-209">في جزء "الإجراءات"، على علامة تبويب **الفوترة**، حدد **مقترح الفاتورة الجديدة‬**.</span><span class="sxs-lookup"><span data-stu-id="0a41c-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="0a41c-210">في مربع الحوار **إنشاء مقترح فاتورة**، في القسم **حركات المشروع**، حدد خانه الاختيار **تحديد** لكل بند ترغب في فوترته.</span><span class="sxs-lookup"><span data-stu-id="0a41c-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="0a41c-211">حدد **موافق** لإغلاق مربع الحوار وعرض مقترح الفاتورة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="0a41c-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]