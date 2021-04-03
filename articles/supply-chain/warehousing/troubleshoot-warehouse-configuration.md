---
title: استكشاف أخطاء تكوين المستودع وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء تكوين Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1fe285f05e5f1ddcb7bd206290b9954cbdaffc75
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487087"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="0fafb-103">استكشاف أخطاء تكوين المستودع وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="0fafb-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fafb-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء تكوين Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0fafb-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="0fafb-105">أتلقى رسالة الخطا التالية: "لوحه الترخيص أو الموقع غير صحيح."</span><span class="sxs-lookup"><span data-stu-id="0fafb-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-106">Issue description</span></span>

<span data-ttu-id="0fafb-107">تظهر رسالة الخطا هذه عند مسح معرف لوحه الترخيص أو الموقع.</span><span class="sxs-lookup"><span data-stu-id="0fafb-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-108">Issue resolution</span></span>

<span data-ttu-id="0fafb-109">تاكد من ان معرف لوح الترخيص غير محجوز بواسطة شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="0fafb-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="0fafb-110">وتستخدم هذه المشكلة لتحدث عندما يكون أحد المستخدمين الذي قام بفحصه في تطبيق المستودع هو موقع صالح ومعرف لوحه ترخيص صالح.</span><span class="sxs-lookup"><span data-stu-id="0fafb-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="0fafb-111">ومع ذلك ، تم حل هذه المشكلة في الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="0fafb-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="0fafb-112">أتلقى رسالة الخطا التالية: "يجب تحديد لوحه الترخيص لهذا الموقع."</span><span class="sxs-lookup"><span data-stu-id="0fafb-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-113">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-113">Issue description</span></span>

<span data-ttu-id="0fafb-114">تظهر رسالة الخطا هذه إذا قمت بإنشاء أمر تحويل باستخدام مستودع ممكن لأداره المستودعات المتقدمة (WMS) ، ثم بعد اكتمال العمل ، فانك تحاول تاكيد الشحن.</span><span class="sxs-lookup"><span data-stu-id="0fafb-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-115">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-115">Issue resolution</span></span>

<span data-ttu-id="0fafb-116">حقل **موقع الاستلام الافتراضي** فارغ لمخزن بضاعة بالطريق للمستودع "من".</span><span class="sxs-lookup"><span data-stu-id="0fafb-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="0fafb-117">لحل هذه المشكلة ، حدد موقع استلام افتراضي في مخزن البضاعة بالطريق.</span><span class="sxs-lookup"><span data-stu-id="0fafb-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="0fafb-118">تاكد من ان هذا الموقع هو لوحه الترخيص – التي يتم التحكم بها.</span><span class="sxs-lookup"><span data-stu-id="0fafb-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="0fafb-119">أتلقى رسالة الخطا التالية: "لا يمكنك إنشاء بند قالب عمل لتغيير حاله المخزون لان نوع العمل غير صالح.</span><span class="sxs-lookup"><span data-stu-id="0fafb-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="0fafb-120">حدد نوع عمل مختلف."</span><span class="sxs-lookup"><span data-stu-id="0fafb-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-121">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-121">Issue description</span></span>

<span data-ttu-id="0fafb-122">بالنسبة لقالب عمل، لا يمكنك تحديد *تغيير حاله المخزون* في العمود **نوع العمل** الخاص بقسم **تفاصيل قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-123">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-123">Issue resolution</span></span>

<span data-ttu-id="0fafb-124">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="0fafb-124">This behavior is by design.</span></span> <span data-ttu-id="0fafb-125">يتم استخدام نوع العمل *تغيير حاله المخزون* فقط من قبل عمليات النظام.</span><span class="sxs-lookup"><span data-stu-id="0fafb-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="0fafb-126">لا يمكن تكوينها.</span><span class="sxs-lookup"><span data-stu-id="0fafb-126">It can't be configured.</span></span> <span data-ttu-id="0fafb-127">ونظرا لان قائمه أنواع العمل قد تم إصلاحها علي انها قائمه تعداد ، لا يمكن تصفيه الإدخالات الاضافيه خارج القائمة المنسدلة **نوع العمل**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="0fafb-128">أتلقى رسالة الخطا التالية: "الكمية غير صالحة للوحدة 1%."</span><span class="sxs-lookup"><span data-stu-id="0fafb-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-129">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-129">Issue description</span></span>

<span data-ttu-id="0fafb-130">الكمية غير صالحه لوحده *ea* عند وجود عمل انتقاء يحتوي علي لوحات ترخيص متعددة في موقع واحد.</span><span class="sxs-lookup"><span data-stu-id="0fafb-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-131">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-131">Issue resolution</span></span>

<span data-ttu-id="0fafb-132">تحقق من تعيين الحقلين **معرف مجموعه تسلسل الوحدات** و **تحويلات الوحدات** في متغير المنتج أو المنتج الذي تم إصداره بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="0fafb-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="0fafb-133">لاحظ انه تم تحسين رسالة الخطا في 10.0.15 الإصدار (راجع [قاعدة المعارف 4581627 ](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="0fafb-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="0fafb-134">رسالة الخطا الجديدة هي ، "الكمية غير صالحه.</span><span class="sxs-lookup"><span data-stu-id="0fafb-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="0fafb-135">المتوقع %1 %2."</span><span class="sxs-lookup"><span data-stu-id="0fafb-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="0fafb-136">في موجات الموقع التي يضع فيها عمل التوريد ، لا يقوم خيار المضاعفة SKU بتقييم الإجراءات الموجهة متعددة المواقع.</span><span class="sxs-lookup"><span data-stu-id="0fafb-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-137">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-137">Issue description</span></span>

<span data-ttu-id="0fafb-138">لا يقوم موجه المواقع الخاصة بنوع أمر عمل *أوامر المبيعات* ونوع العمل *تخزين* بتقييم الإجراءات الموجهة متعددة المواقع عند تحديد الخيار **SKU متعددة**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="0fafb-139">يتم تقييم الاجراء الخاص بالتوجيه في الموقع الأول فقط.</span><span class="sxs-lookup"><span data-stu-id="0fafb-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-140">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-140">Issue resolution</span></span>

<span data-ttu-id="0fafb-141">تمت أضافه ميزه جديده، *تقييم كافة الإجراءات لتوجيهات المواقع SKU المتعددة*، في الإصدار 10.0.15 (راجع [قاعدة المعارف 4579866 ](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="0fafb-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="0fafb-142">هذه الميزة تقيم كافة الإجراءات لموجهات مواقع SKU متعددة.</span><span class="sxs-lookup"><span data-stu-id="0fafb-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="0fafb-143">إذا تطلبت هذه الميزة ، فاستخدم [أداره الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="0fafb-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="0fafb-144">لا يمكنني استخدام تطبيق المستودع لاجراء انتقاء جزئي.</span><span class="sxs-lookup"><span data-stu-id="0fafb-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-145">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-145">Issue description</span></span>

<span data-ttu-id="0fafb-146">بالنسبة لأوامر التوريد والتحويل ، لا يمكنك تخطي الأصناف واجراء انتقاء جزئي.</span><span class="sxs-lookup"><span data-stu-id="0fafb-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-147">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-147">Issue resolution</span></span>

<span data-ttu-id="0fafb-148">في الصفحة **عناصر قائمه الجهاز المحمول**، لكل عنصر قائمه تم اعداده لمعالجه أوامر المبيعات أو أوامر التحويل، قم بتعيين خيار **السماح بتقسيم العمل** في علامة التبويب السريعة **عام** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="0fafb-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="0fafb-149">كيف يمكنني اجراء تغيير في حاله المخزون للعمل الجزئي للكمية؟</span><span class="sxs-lookup"><span data-stu-id="0fafb-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-150">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-150">Issue description</span></span>

<span data-ttu-id="0fafb-151">الرغبة في القيام بتغيير في حاله المخزون لكميه جزئيه من المجموعة.</span><span class="sxs-lookup"><span data-stu-id="0fafb-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-152">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-152">Issue resolution</span></span>

<span data-ttu-id="0fafb-153">لتمكين العاملين من اجراء هذا التغيير ، يمكنك إنشاء عنصر قائمه لتطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="0fafb-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="0fafb-154">في صفحة **عناصر قائمة الجهاز المحمول**، أنشئ عناصر قائمة لأحد الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="0fafb-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="0fafb-155">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="0fafb-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="0fafb-156">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="0fafb-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="0fafb-157">**عملية إنشاء العمل:** *الحركة*</span><span class="sxs-lookup"><span data-stu-id="0fafb-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="0fafb-158">**عرض حالة المخزون:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="0fafb-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="0fafb-159">يمكنك تعيين حقول أخرى في الصفحة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="0fafb-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="0fafb-160">لا يمنع ملف تعريف إدارة الإرساء لملف تعريف الموقع أنواع المخزون من الاختلاط.</span><span class="sxs-lookup"><span data-stu-id="0fafb-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="0fafb-161">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-161">Issue description</span></span>

<span data-ttu-id="0fafb-162">أنت تستخدم *سياسات دمج الشحنات*.</span><span class="sxs-lookup"><span data-stu-id="0fafb-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="0fafb-163">لقد قمت بإعداد *ملف تعريف إدارة المستودع* لـ *ملف تعريف الموقع*، ولكن عند إنشاء العمل، يتم خلط أنواع المخزون في الموقع النهائي.</span><span class="sxs-lookup"><span data-stu-id="0fafb-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0fafb-164">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="0fafb-164">Issue resolution</span></span>

<span data-ttu-id="0fafb-165">تتطلب ملفات تعريف إدارة المستودعات تقسيم العمل مقدمًا.</span><span class="sxs-lookup"><span data-stu-id="0fafb-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="0fafb-166">بمعنى آخر، يتوقع ملف تعريف إدارة المستودعات ألا يكون لرأس العمل مواقع وضع متعددة.</span><span class="sxs-lookup"><span data-stu-id="0fafb-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="0fafb-167">لكي يتمكن ملف تعريف إدارة المستودعات من إدارة خلط المخزون بشكل فعال، يجب إعداد فاصل رأس العمل.</span><span class="sxs-lookup"><span data-stu-id="0fafb-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="0fafb-168">في هذا المثال، تم تكوين ملف تعريف إدارة المستودعات الخاص بنا بحيث يتم تعيين **أنواع المخزون التي لا يجب خلطها** إلى *معرف الشحنة*، وسنقوم بإعداد فاصل رأس عمل له:</span><span class="sxs-lookup"><span data-stu-id="0fafb-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="0fafb-169">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="0fafb-170">حدد **نوع أمر العمل** لتحريره (على سبيل المثال، *أوامر الشراء*).</span><span class="sxs-lookup"><span data-stu-id="0fafb-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="0fafb-171">حدد قالب العمل المُراد تحريره.</span><span class="sxs-lookup"><span data-stu-id="0fafb-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="0fafb-172">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="0fafb-173">افتح علامة التبويب **فرز** وأضف صفًا بالإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0fafb-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="0fafb-174">**الجدول** - *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0fafb-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="0fafb-175">**الجدول المشتق** - *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0fafb-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="0fafb-176">**الحقل** - *معرف الشحنة*</span><span class="sxs-lookup"><span data-stu-id="0fafb-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="0fafb-177">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-177">Select **OK**.</span></span>
1. <span data-ttu-id="0fafb-178">قم بالرجوع إلى صفحة **قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="0fafb-179">في جزء الإجراءات، حدد **فواصل رأس العمل**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="0fafb-180">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0fafb-181">حدد خانه الاختيار المقترنة بـ **اسم الحقل** *معرف الشحنة*.</span><span class="sxs-lookup"><span data-stu-id="0fafb-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="0fafb-182">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0fafb-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
