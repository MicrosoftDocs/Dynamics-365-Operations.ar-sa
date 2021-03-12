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
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993993"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="ce9ac-103">استكشاف أخطاء تكوين المستودع وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="ce9ac-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce9ac-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء تكوين Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="ce9ac-105">أتلقى رسالة الخطا التالية: "لوحه الترخيص أو الموقع غير صحيح."</span><span class="sxs-lookup"><span data-stu-id="ce9ac-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-106">Issue description</span></span>

<span data-ttu-id="ce9ac-107">تظهر رسالة الخطا هذه عند مسح معرف لوحه الترخيص أو الموقع.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-108">Issue resolution</span></span>

<span data-ttu-id="ce9ac-109">تاكد من ان معرف لوح الترخيص غير محجوز بواسطة شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="ce9ac-110">وتستخدم هذه المشكلة لتحدث عندما يكون أحد المستخدمين الذي قام بفحصه في تطبيق المستودع هو موقع صالح ومعرف لوحه ترخيص صالح.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="ce9ac-111">ومع ذلك ، تم حل هذه المشكلة في الإصدار 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="ce9ac-112">أتلقى رسالة الخطا التالية: "يجب تحديد لوحه الترخيص لهذا الموقع."</span><span class="sxs-lookup"><span data-stu-id="ce9ac-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-113">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-113">Issue description</span></span>

<span data-ttu-id="ce9ac-114">تظهر رسالة الخطا هذه إذا قمت بإنشاء أمر تحويل باستخدام مستودع ممكن لأداره المستودعات المتقدمة (WMS) ، ثم بعد اكتمال العمل ، فانك تحاول تاكيد الشحن.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-115">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-115">Issue resolution</span></span>

<span data-ttu-id="ce9ac-116">حقل **موقع الاستلام الافتراضي** فارغ لمخزن بضاعة بالطريق للمستودع "من".</span><span class="sxs-lookup"><span data-stu-id="ce9ac-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="ce9ac-117">لحل هذه المشكلة ، حدد موقع استلام افتراضي في مخزن البضاعة بالطريق.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="ce9ac-118">تاكد من ان هذا الموقع هو لوحه الترخيص – التي يتم التحكم بها.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="ce9ac-119">أتلقى رسالة الخطا التالية: "لا يمكنك إنشاء بند قالب عمل لتغيير حاله المخزون لان نوع العمل غير صالح.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="ce9ac-120">حدد نوع عمل مختلف."</span><span class="sxs-lookup"><span data-stu-id="ce9ac-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-121">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-121">Issue description</span></span>

<span data-ttu-id="ce9ac-122">بالنسبة لقالب عمل، لا يمكنك تحديد *تغيير حاله المخزون* في العمود **نوع العمل** الخاص بقسم **تفاصيل قالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-123">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-123">Issue resolution</span></span>

<span data-ttu-id="ce9ac-124">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-124">This behavior is by design.</span></span> <span data-ttu-id="ce9ac-125">يتم استخدام نوع العمل *تغيير حاله المخزون* فقط من قبل عمليات النظام.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="ce9ac-126">لا يمكن تكوينها.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-126">It can't be configured.</span></span> <span data-ttu-id="ce9ac-127">ونظرا لان قائمه أنواع العمل قد تم إصلاحها علي انها قائمه تعداد ، لا يمكن تصفيه الإدخالات الاضافيه خارج القائمة المنسدلة **نوع العمل**.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="ce9ac-128">أتلقى رسالة الخطا التالية: "الكمية غير صالحة للوحدة 1%."</span><span class="sxs-lookup"><span data-stu-id="ce9ac-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-129">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-129">Issue description</span></span>

<span data-ttu-id="ce9ac-130">الكمية غير صالحه لوحده *ea* عند وجود عمل انتقاء يحتوي علي لوحات ترخيص متعددة في موقع واحد.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-131">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-131">Issue resolution</span></span>

<span data-ttu-id="ce9ac-132">تحقق من تعيين الحقلين **معرف مجموعه تسلسل الوحدات** و **تحويلات الوحدات** في متغير المنتج أو المنتج الذي تم إصداره بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="ce9ac-133">لاحظ انه تم تحسين رسالة الخطا في 10.0.15 الإصدار (راجع [قاعدة المعارف 4581627 ](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="ce9ac-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="ce9ac-134">رسالة الخطا الجديدة هي ، "الكمية غير صالحه.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="ce9ac-135">المتوقع %1 %2."</span><span class="sxs-lookup"><span data-stu-id="ce9ac-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="ce9ac-136">في موجات الموقع التي يضع فيها عمل التوريد ، لا يقوم خيار المضاعفة SKU بتقييم الإجراءات الموجهة متعددة المواقع.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-137">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-137">Issue description</span></span>

<span data-ttu-id="ce9ac-138">لا يقوم موجه المواقع الخاصة بنوع أمر عمل *أوامر المبيعات* ونوع العمل *تخزين* بتقييم الإجراءات الموجهة متعددة المواقع عند تحديد الخيار **SKU متعددة**.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="ce9ac-139">يتم تقييم الاجراء الخاص بالتوجيه في الموقع الأول فقط.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-140">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-140">Issue resolution</span></span>

<span data-ttu-id="ce9ac-141">تمت أضافه ميزه جديده، *تقييم كافة الإجراءات لتوجيهات المواقع SKU المتعددة*، في الإصدار 10.0.15 (راجع [قاعدة المعارف 4579866 ](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="ce9ac-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="ce9ac-142">هذه الميزة تقيم كافة الإجراءات لموجهات مواقع SKU متعددة.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="ce9ac-143">إذا تطلبت هذه الميزة ، فاستخدم [أداره الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="ce9ac-144">لا يمكنني استخدام تطبيق المستودع لاجراء انتقاء جزئي.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-145">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-145">Issue description</span></span>

<span data-ttu-id="ce9ac-146">بالنسبة لأوامر التوريد والتحويل ، لا يمكنك تخطي الأصناف واجراء انتقاء جزئي.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-147">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-147">Issue resolution</span></span>

<span data-ttu-id="ce9ac-148">في الصفحة **عناصر قائمه الجهاز المحمول**، لكل عنصر قائمه تم اعداده لمعالجه أوامر المبيعات أو أوامر التحويل، قم بتعيين خيار **السماح بتقسيم العمل** في علامة التبويب السريعة **عام** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="ce9ac-149">كيف يمكنني اجراء تغيير في حاله المخزون للعمل الجزئي للكمية؟</span><span class="sxs-lookup"><span data-stu-id="ce9ac-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="ce9ac-150">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-150">Issue description</span></span>

<span data-ttu-id="ce9ac-151">الرغبة في القيام بتغيير في حاله المخزون لكميه جزئيه من المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ce9ac-152">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce9ac-152">Issue resolution</span></span>

<span data-ttu-id="ce9ac-153">لتمكين العاملين من اجراء هذا التغيير ، يمكنك إنشاء عنصر قائمه لتطبيق المستودع.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="ce9ac-154">في صفحة **عناصر قائمة الجهاز المحمول**، أنشئ عناصر قائمة لأحد الطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="ce9ac-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="ce9ac-155">**الوضع:** *العمل*</span><span class="sxs-lookup"><span data-stu-id="ce9ac-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="ce9ac-156">**استخدام العمل الموجود:** *لا*</span><span class="sxs-lookup"><span data-stu-id="ce9ac-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="ce9ac-157">**عملية إنشاء العمل:** *الحركة*</span><span class="sxs-lookup"><span data-stu-id="ce9ac-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="ce9ac-158">**عرض حالة المخزون:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="ce9ac-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="ce9ac-159">يمكنك تعيين حقول أخرى في الصفحة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="ce9ac-159">You can set other fields on the page as you require.</span></span>
