---
title: استكشاف أخطاء معلومات المنتج وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع معلومات المنتج.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9db8e0081a0d47ec8d74680fe99a0934b99bb5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223352"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="e9a58-103">استكشاف أخطاء معلومات المنتج وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="e9a58-103">Troubleshoot product information</span></span>

<span data-ttu-id="e9a58-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="e9a58-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="e9a58-105">لا يمكنني حذف منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="e9a58-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-106">Issue description</span></span>

<span data-ttu-id="e9a58-107">يمكنك حذف منتج تم إصداره وجميع متغيراته فقط إذا لم يكن للمنتج الذي تم إصداره إيه حركات مرتبطة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-108">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-108">Issue resolution</span></span>

<span data-ttu-id="e9a58-109">اتبع الخطوات التالية لحذف منتج أو أصل منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="e9a58-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="e9a58-110">يستخدم لإغلاق كافة الحركات المفتوحة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="e9a58-111">تقليل المخزون إلى 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="e9a58-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="e9a58-112">اجراء اقفال المخزون.</span><span class="sxs-lookup"><span data-stu-id="e9a58-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="e9a58-113">قم بحذف كافة متغيرات المنتج لأصل المنتج الذي تريد حذفه.</span><span class="sxs-lookup"><span data-stu-id="e9a58-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="e9a58-114">هل يمكنني تغيير رقم الصنف الخاص بمنتج تم إصداره؟</span><span class="sxs-lookup"><span data-stu-id="e9a58-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="e9a58-115">في معظم الحالات ، لا يمكنك تحرير أرقام الأصناف للمنتجات التي تم إصدارها ، لان هذا التغيير سيتسبب في تلف البيانات.</span><span class="sxs-lookup"><span data-stu-id="e9a58-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="e9a58-116">يمكنك تحرير رقم الصنف فقط إذا كان من الضروري إصلاح تلف البيانات الذي حدث بسبب أعاده التسمية السابقة للمفتاح الأساسي لذلك المنتج الذي تم إصداره ، كما هو موضح في قائمه [ميزات Finance and Operations 10.0.0 التي تمت ازالتها أو إهمالها مع تحديث النظام الأساسي 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="e9a58-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="e9a58-117">إذا أردت ان تكون قادرا علي تحرير أرقام الأصناف للمنتجات الصادرة، [قم بالتصويت لهذه الفكرة في مدخل الأفكار](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="e9a58-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="e9a58-118">لا يتم إدخال قاعده التفريغ الافتراضية من المنتج في بند قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-119">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-119">Issue description</span></span>

<span data-ttu-id="e9a58-120">عند أضافه صنف إلى بند قائمة مكونات الصنف (BOM) ، لا يستخدم النظام معلومات قاعده التفريغ الافتراضية التي يتم اعدادها للصنف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="e9a58-121">بمعني آخر ، لا تظهر قاعده التفريغ من الصنف في صفحه **بند قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="e9a58-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-122">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-122">Issue resolution</span></span>

<span data-ttu-id="e9a58-123">إذا قمت بتحديد قاعده المسح في بند قائمة مكونات الصنف، سيتم تطبيقها علي بند قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="e9a58-124">ومع ذلك ، إذا كانت قاعده المسح فارغه ، أو إذا لم يتم تعيينها في بند قائمة مكونات الصنف، ستبقي قاعده التفريغ التي تم تعيينها في الصنف تنطبق علي بند شجره المواد ، حتى وان لم يكن ظاهرا في بند قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="e9a58-125">ولا يعمل المنطق الافتراضي لمنطق الميزات الأخرى في Microsoft Dynamics 365 Supply Chain Management بهذه الطريقة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="e9a58-126">ومع ذلك ، لا يمكن تغيير السلوك الحالي.</span><span class="sxs-lookup"><span data-stu-id="e9a58-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="e9a58-127">والا ، فقد يتم قطع بعض التخصيصات الموجودة التي تعتمد عليها.</span><span class="sxs-lookup"><span data-stu-id="e9a58-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="e9a58-128">يتيح النظام لي حفظ الأكواد الشريطية المكررة لأصناف مختلفه أو لنفس الصنف الذي يحتوي علي ابعاد مختلفه.</span><span class="sxs-lookup"><span data-stu-id="e9a58-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="e9a58-129">لا يفرض النظام حاليا الرموز الشريطية الفريدة ، ستكون أضافه هذا التقييد تغييرا في الفصل.</span><span class="sxs-lookup"><span data-stu-id="e9a58-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="e9a58-130">في الواقع ، لدي Microsoft دليل علي ان بعض عمليات تثبيت العميل الموجودة ستقطع بهذا التغيير.</span><span class="sxs-lookup"><span data-stu-id="e9a58-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="e9a58-131">ومع ذلك ، سنقوم بمراعاه تغيير أكبر في التصميم لتمكين هذه الميزة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="e9a58-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="e9a58-132">أتلقى رسالة الخطا التالية عند تحرير قوالب سجلات الأصناف: "تعذر إنشاء موقع المستودع" لان الصنف غير مخزن.</span><span class="sxs-lookup"><span data-stu-id="e9a58-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="e9a58-133">لأصناف المخزون ، يجب تحديد خيار المنتج المخزن في مجموعه نماذج الصنف المقترن. "</span><span class="sxs-lookup"><span data-stu-id="e9a58-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-134">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-134">Issue description</span></span>

<span data-ttu-id="e9a58-135">تحدث هذه المشكلة في حاله اتباع الخطوات التالية لمحاولة إنشاء قالب لصنف غير مخزن.</span><span class="sxs-lookup"><span data-stu-id="e9a58-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="e9a58-136">يستخدم هذا الزر في فتح منتج تم إصداره والذي لم يتم تخزينه.</span><span class="sxs-lookup"><span data-stu-id="e9a58-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="e9a58-137">في جزء "الإجراءات"، على علامة تبويب **خيارات**، حدد **معلومات السجل**.</span><span class="sxs-lookup"><span data-stu-id="e9a58-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="e9a58-138">في مربع الحوار **معلومات السجل**، حدد **قالب حسابات الشركة**.</span><span class="sxs-lookup"><span data-stu-id="e9a58-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="e9a58-139">في هذه الحالة، تتلقى رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="e9a58-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="e9a58-140">لا يمكن إنشاء موقع المستودع نظرا لان الصنف غير مخزن.</span><span class="sxs-lookup"><span data-stu-id="e9a58-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="e9a58-141">لأصناف المخزون ، يجب تحديد خيار المنتج المخزن في مجموعه نماذج الصنف المقترن.</span><span class="sxs-lookup"><span data-stu-id="e9a58-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-142">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-142">Issue resolution</span></span>

<span data-ttu-id="e9a58-143">وتتطلب عمليه إنشاء قوالب المنتجات منطقا إضافيا خاصا بمنتج إضافي.</span><span class="sxs-lookup"><span data-stu-id="e9a58-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="e9a58-144">لذلك ، لا يمكنك استخدام الزر **القالب حسابات الشركة** العامة لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="e9a58-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="e9a58-145">بدلاً، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="e9a58-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="e9a58-146">افتح منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="e9a58-146">Open a released product.</span></span>
1. <span data-ttu-id="e9a58-147">في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **جديد**‬، حدد **قالب \> إنشاء قالب مشترك**.</span><span class="sxs-lookup"><span data-stu-id="e9a58-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="e9a58-148">لا يتم إدخال نص التعليمات الافتراضي المضاف في سمات المنتج في منتج تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="e9a58-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="e9a58-149">لا يكون نص التعليمات والوصف المضافين في سمات المنتج مرئيا أو يتم إدخاله بشكل افتراضي في المنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="e9a58-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="e9a58-150">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="e9a58-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="e9a58-151">تختلف الكمية الافتراضية التي يتم إدخالها عند تسجيلها من قائمة مكونات الصنف وعند تسجيلها من إصدار قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-152">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-152">Issue description</span></span>

<span data-ttu-id="e9a58-153">بشكل افتراضي ، عند أضافه صنف إلى شجره مواد ، يتم تعيين الكمية إلى 1 بدلا من الكمية المحددة في الحقل **الحد الأدنى لكميه الأمر** في الصفحة **إعدادات الأمر الافتراضية** الخاصة بمنتج محدد.</span><span class="sxs-lookup"><span data-stu-id="e9a58-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="e9a58-154">ومع ذلك ، عند أضافه صنف من إصدار شجره المواد ، وتحديد الصنف والمتغير ، تقوم الكمية التي يتم إدخالها بشكل افتراضي بأخذ الحد الأدنى من الكمية التي يتم تعيينها في إعدادات الأمر الافتراضية للابعاد المحددة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-155">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-155">Issue resolution</span></span>

<span data-ttu-id="e9a58-156">هذا السلوك متوقع.</span><span class="sxs-lookup"><span data-stu-id="e9a58-156">This behavior is expected.</span></span> <span data-ttu-id="e9a58-157">ومع ذلك ، فان المنطق يختلف في قائمة مكونات الصنف وإصدار قائمة مكونات الصنف هو مشكله معروفه.</span><span class="sxs-lookup"><span data-stu-id="e9a58-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="e9a58-158">نيفرتلس ، فلن يتم تغيير هذا السلوك ، لان أحد التغييرات قد يؤثر علي عده سيناريوهات مختلفه للعملاء.</span><span class="sxs-lookup"><span data-stu-id="e9a58-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="e9a58-159">في تفاصيل المنتجات الصادرة ، لا يمكنني تغيير الصور المرفقة التي تم تحميلها من وحده بيانات مرفقات مستند المنتج.</span><span class="sxs-lookup"><span data-stu-id="e9a58-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-160">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-160">Issue description</span></span>

<span data-ttu-id="e9a58-161">يمكن ان تحدث هذه المشكلة عند إرفاق صوره بأحد الأصناف باستخدام كيان البيانات *مرفقات مستندات المنتج*.</span><span class="sxs-lookup"><span data-stu-id="e9a58-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="e9a58-162">وفي هذه الحالة ، يتم عرض صوره الصنف للصنف.</span><span class="sxs-lookup"><span data-stu-id="e9a58-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="e9a58-163">علي اي حال ، إذا قمت بتحديد **تغيير الصورة**، فانه لا يتم عرض اي شيء في قائمه الصور المحملة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="e9a58-164">بالاضافه إلى ذلك ، لا يتم إظهار إيه مرفقات للعنصر.</span><span class="sxs-lookup"><span data-stu-id="e9a58-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-165">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-165">Issue resolution</span></span>

<span data-ttu-id="e9a58-166">يقوم الكيان *EcoResProductDocumentAttachmentEntity* (*مرفقات مستند المنتج*) باستيراد مرفقات المستندات *للمنتجات* ولكن ليس *للمنتجات التي تم إصدارها*.</span><span class="sxs-lookup"><span data-stu-id="e9a58-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="e9a58-167">(تعرف المنتجات التي تم إصدارها أيضا باسم *الأصناف*.) لعرض مرفقات أحد الأصناف في الصفحة **تفاصيل المنتجات التي تم إصدارها**، يجب استخدام الكيان *EcoResReleasedProductDocumentAttachmentEntity* (*مرفقات مستندات المنتجات التي تم إصدارها*) بدلا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="e9a58-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="e9a58-168">يعرض الموصل Microsoft Flow رسالة الخطا التالية: "غير مسموح بالتحديث للحقل"'ProductNumber'".</span><span class="sxs-lookup"><span data-stu-id="e9a58-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-169">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-169">Issue description</span></span>

<span data-ttu-id="e9a58-170">تحدث هذه المشكلة إذا حاولت تحديث حقل **رقم المنتج** باستخدام كيان *المنتجات الصادرة* V2 وMicrosoft Flow.</span><span class="sxs-lookup"><span data-stu-id="e9a58-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-171">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-171">Issue resolution</span></span>

<span data-ttu-id="e9a58-172">هذا السلوك متوقع.</span><span class="sxs-lookup"><span data-stu-id="e9a58-172">This behavior is expected.</span></span> <span data-ttu-id="e9a58-173">تمت أزاله القدرة علي تحرير رقم المنتج لمنتج تم إصداره في Dynamics 365 Finance and Operations 10.0.0 مع تحديث النظام الأساسي 24 للمساعدة علي منع تلف البيانات.</span><span class="sxs-lookup"><span data-stu-id="e9a58-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="e9a58-174">في حالات استثنائية، يجب إصلاح تلف البيانات التي سببتها إعادة تسميه سابقه للمفتاح الأساسي لمنتج تم إصداره، فالرجاء الاتصال بدعم Microsoft لطلب الإزالة المؤقتة لهذا التقييد.</span><span class="sxs-lookup"><span data-stu-id="e9a58-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="e9a58-175">لا يمكنني إنشاء متغير منتج تم إصداره في كيان قانوني آخر.</span><span class="sxs-lookup"><span data-stu-id="e9a58-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-176">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-176">Issue description</span></span>

<span data-ttu-id="e9a58-177">إذا حاولت إصدار أصل منتج بدون متغيرات ، ثم قمت بإنشاء المتغيرات في كل كيان قانوني (الشركة) حسب الحاجة ، فلن تتمكن من إصدار المتغيرات باستخدام اقتراحات المتغير.</span><span class="sxs-lookup"><span data-stu-id="e9a58-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="e9a58-178">كما لن تتمكن من إنشاء المتغيرات يدويا.</span><span class="sxs-lookup"><span data-stu-id="e9a58-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-179">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-179">Issue resolution</span></span>

<span data-ttu-id="e9a58-180">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="e9a58-180">This behavior is by design.</span></span> <span data-ttu-id="e9a58-181">يتم الاحتفاظ بعلاقات أصل المنتج والابعاد التي يمكن الحصول عليها بالشكل الرئيسي في مستوي مشترك.</span><span class="sxs-lookup"><span data-stu-id="e9a58-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="e9a58-182">التالي ، لا يمكنك إنشاء الابعاد المتوفرة لأصل منتج مشترك في الكيان القانوني المحدد حيث يتم إصدار هذه الابعاد ثم تقوم باجراء نسخ متماثل للعملية في كل كيان قانوني حيث تكون الابعاد مطلوبه.</span><span class="sxs-lookup"><span data-stu-id="e9a58-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="e9a58-183">بدلا من ذلك ، يجب عليك تغيير عمليه الإصدار الخاصة بك لتلائم العملية التي تم تصميمها.</span><span class="sxs-lookup"><span data-stu-id="e9a58-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="e9a58-184">وفيما يلي عمليه إصدار المنتجات.</span><span class="sxs-lookup"><span data-stu-id="e9a58-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="e9a58-185">إنشاء أصل المنتج المشترك والابعاد التي يمكن إصدارها إلى الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="e9a58-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="e9a58-186">قم بإصدار المنتجات إلى الكيانات القانونية اما باستخدام اقتراحات متغيرة أو باضافه المجموعات التي يجب إصدارها يدويا.</span><span class="sxs-lookup"><span data-stu-id="e9a58-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="e9a58-187">وبدلا من ذلك ، يمكنك إنشاء المنتج الذي تم إصداره مباشره.</span><span class="sxs-lookup"><span data-stu-id="e9a58-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="e9a58-188">عند إصدار متغير في شركه أخرى ، أتلقى رسالة الخطا التالية: "تم بالفعل إنشاء متغير منتج بابعاد محدده."</span><span class="sxs-lookup"><span data-stu-id="e9a58-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e9a58-189">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-189">Issue description</span></span>

<span data-ttu-id="e9a58-190">في حاله إصدار متغير منتج بالفعل في شركه أ، ومحاولة إصداره في الشركة ب باستخدام الزر **جديد** في الصفحة **متغيرات المنتج الذي تم إصداره**، ستتلقى رسالة الخطا التالية:</span><span class="sxs-lookup"><span data-stu-id="e9a58-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="e9a58-191">تم بالفعل إنشاء متغير منتج ذي أبعاد محددة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e9a58-192">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="e9a58-192">Issue resolution</span></span>

<span data-ttu-id="e9a58-193">يقوم الزر **جديد** الموجود في الصفحة **متغيرات المنتج الذي تم إصداره** بإنشاء المتغير وإصداره في سياق الشركة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="e9a58-194">إذا كان المتغير قد تم إنشاؤه بالفعل ، فلا يمكنك استخدام الزر **جديد** لتحريره في شركه أخرى.</span><span class="sxs-lookup"><span data-stu-id="e9a58-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="e9a58-195">لإصلاح المشكلة ، افتح الصفحة **السجل الرئيسي للمنتج**، وحدد **إصدار المنتج** لإصدار المتغير الموجود في الشركة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="e9a58-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]