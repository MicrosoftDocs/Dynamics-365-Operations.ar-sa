---
title: كيانات بيانات المنتج
description: يوفر هذا الموضوع معلومات حول الكيانات المختلفة التي يمكن استخدامها لاستيراد وتصدير بيانات المنتج.
author: cvocph
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 83191ea3d07ec9e2ed6261ee997e06b802ee7645
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935929"
---
# <a name="product-data-entities"></a><span data-ttu-id="a3e89-103">كيانات بيانات المنتج</span><span class="sxs-lookup"><span data-stu-id="a3e89-103">Product data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3e89-104">لاستيراد وتصدير بيانات المنتج، يجب عليك استخدام كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-104">To import and export product data, you must use data entities.</span></span> <span data-ttu-id="a3e89-105">يوفر الجدول التالي تفاصيل حول كيانات البيانات المتعلقة بالمنتج ويصف الغرض من كل منها.</span><span class="sxs-lookup"><span data-stu-id="a3e89-105">The following table provides details about the product-related data entities and describes the purpose of each.</span></span>

| <span data-ttu-id="a3e89-106">الكيان</span><span class="sxs-lookup"><span data-stu-id="a3e89-106">Entity</span></span> | <span data-ttu-id="a3e89-107">اسم شجرة مكونات البرنامج (AOT) (النوع)</span><span class="sxs-lookup"><span data-stu-id="a3e89-107">Application Object Tree (AOT) name (type)</span></span> | <span data-ttu-id="a3e89-108">الملاحظات</span><span class="sxs-lookup"><span data-stu-id="a3e89-108">Notes</span></span> |
|--------|-------------------------------------------|-------|
| <span data-ttu-id="a3e89-109">المنتجات V2</span><span class="sxs-lookup"><span data-stu-id="a3e89-109">Products V2</span></span> | <span data-ttu-id="a3e89-110">EcoResProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="a3e89-110">EcoResProductV2Entity</span></span> | <span data-ttu-id="a3e89-111">ويُستخدم هذا الكيان لاستيراد وتصدير المنتجات المتميزة والمنتجات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="a3e89-111">This entity is used to import and export shared products-distinct products and product masters.</span></span> <span data-ttu-id="a3e89-112">إنها تسمح للحصول على التحديثات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-112">It allows for updates.</span></span> <span data-ttu-id="a3e89-113">لا يدعم عمليات SQL المستندة إلى مجموعة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-113">It doesn't support set-based SQL operations.</span></span> <span data-ttu-id="a3e89-114">يتم تمكينه لبروتوكول البيانات المفتوحة (OData).</span><span class="sxs-lookup"><span data-stu-id="a3e89-114">It's enabled for Open Data Protocol (OData).</span></span> |
| <span data-ttu-id="a3e89-115">المنتجات الصادرة V2</span><span class="sxs-lookup"><span data-stu-id="a3e89-115">Released products V2</span></span> | <span data-ttu-id="a3e89-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="a3e89-116">EcoResReleasedProductV2Entity</span></span> | <span data-ttu-id="a3e89-117">ويُستخدم هذا الكيان لاستيراد وتصدير المنتجات الصادرة‬، المنتجات المتميزة والمنتجات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="a3e89-117">This entity is used to import and export released products-distinct products and product masters.</span></span> <span data-ttu-id="a3e89-118">إنها تسمح للحصول على التحديثات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-118">It allows for updates.</span></span> <span data-ttu-id="a3e89-119">يتطلب ان يتم إنشاء المنتج المشترك بالفعل.</span><span class="sxs-lookup"><span data-stu-id="a3e89-119">It requires that the shared product already be created.</span></span> <span data-ttu-id="a3e89-120">عند استيراد منتج جديد تم إصداره، يحدث إصدار للمنتج المشترك.</span><span class="sxs-lookup"><span data-stu-id="a3e89-120">When a new released product is imported, a release of the shared product occurs.</span></span> <span data-ttu-id="a3e89-121">وهناك أيضا كيانات منفصلة يمكن استخدامها لاستيراد وتصدير المنتجات الرئيسية التي تم إصدارها وإصدار متغيرات مميزه.</span><span class="sxs-lookup"><span data-stu-id="a3e89-121">There are also separate entities that can be used to import and export released product masters and released distinct variants.</span></span> <span data-ttu-id="a3e89-122">لا يعتمد هذا الكيان عمليات SQL المستندة إلى مجموعه أو عمليات الحذف.</span><span class="sxs-lookup"><span data-stu-id="a3e89-122">This entity doesn't support set-based SQL operations or delete operations.</span></span> <span data-ttu-id="a3e89-123">تم تمكينه ل OData.</span><span class="sxs-lookup"><span data-stu-id="a3e89-123">It's enabled for OData.</span></span> |
| <span data-ttu-id="a3e89-124">إنشاء المنتج الذي تم إصداره V2</span><span class="sxs-lookup"><span data-stu-id="a3e89-124">Released product creation V2</span></span> | <span data-ttu-id="a3e89-125">EcoResReleasedProductCreationV2Entity</span><span class="sxs-lookup"><span data-stu-id="a3e89-125">EcoResReleasedProductCreationV2Entity</span></span> | <span data-ttu-id="a3e89-126">يتم استخدام هذا الكيان لاستيراد المنتجات المشتركة والمنتجات التي تم إصدارها في خطوه واحدة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-126">This entity is used to import shared products and released products in one step.</span></span> <span data-ttu-id="a3e89-127">على الرغم من أنه يدعم الصادرات، إلا أن هذا الاستخدام غير مستحسن، لأن الغرض من الكيان هو إنشاء المنتج.</span><span class="sxs-lookup"><span data-stu-id="a3e89-127">Although it supports exports, that use isn't recommended, because the purpose of the entity is product creation.</span></span> <span data-ttu-id="a3e89-128">لا يدعم التحديثات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-128">It doesn't support updates.</span></span> <span data-ttu-id="a3e89-129">يدعم مجموعة محدودة من الحقول (الحقول المتوفرة في مربع حوار إنشاء المنتج).</span><span class="sxs-lookup"><span data-stu-id="a3e89-129">It supports a limited set of fields (fields that are available in the product creation dialog box).</span></span> <span data-ttu-id="a3e89-130">لا يدعم عمليات SQL المستندة إلى مجموعة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-130">It doesn't support set-based SQL operations.</span></span> <span data-ttu-id="a3e89-131">لا يتم كشفها من خلال OData.</span><span class="sxs-lookup"><span data-stu-id="a3e89-131">It isn't exposed through OData.</span></span> |
| <span data-ttu-id="a3e89-132">متغيرات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a3e89-132">Product variants</span></span> | <span data-ttu-id="a3e89-133">EcoResProductVariantEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-133">EcoResProductVariantEntity</span></span> | <span data-ttu-id="a3e89-134">يتم استخدام هذا الكيان لاستيراد وتصدير متغيرات المنتجات المشتركة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-134">This entity is used to import and export shared product variants.</span></span> <span data-ttu-id="a3e89-135">إنها تسمح للحصول على التحديثات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-135">It allows for updates.</span></span> <span data-ttu-id="a3e89-136">وهو يتطلب إنشاء قيم الابعاد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a3e89-136">It requires that dimension values already be created.</span></span> <span data-ttu-id="a3e89-137">مفتاح التكامل هو المنتج الرئيسي بالإضافة إلى أبعاد المنتج</span><span class="sxs-lookup"><span data-stu-id="a3e89-137">The integration key is the product master plus product dimensions.</span></span> <span data-ttu-id="a3e89-138">لا يدعم هذا الكيان عمليات SQL المستندة إلى مجموعة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-138">This entity doesn't support set-based SQL operations.</span></span> <span data-ttu-id="a3e89-139">تم تمكينه ل OData.</span><span class="sxs-lookup"><span data-stu-id="a3e89-139">It's enabled for OData.</span></span> <span data-ttu-id="a3e89-140">وهو يدعم عمليات الحذف.</span><span class="sxs-lookup"><span data-stu-id="a3e89-140">It supports delete operations.</span></span> <span data-ttu-id="a3e89-141">لا يمكن تمديده من خلال إضافة أبعاد المنتج الجديد.</span><span class="sxs-lookup"><span data-stu-id="a3e89-141">It can't be extended through the addition of new product dimensions.</span></span> |
| <span data-ttu-id="a3e89-142">متغيرات المنتجات حسب تعريف رقم المنتج</span><span class="sxs-lookup"><span data-stu-id="a3e89-142">Product variants by product number identification</span></span> | <span data-ttu-id="a3e89-143">EcoResProductNumberIdentifiedProductVariantEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-143">EcoResProductNumberIdentifiedProductVariantEntity</span></span> | <span data-ttu-id="a3e89-144">يتم استخدام هذا الكيان لاستيراد وتصدير متغيرات المنتجات المشتركة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-144">This entity is used to import and export shared product variants.</span></span> <span data-ttu-id="a3e89-145">إنها تسمح للحصول على التحديثات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-145">It allows for updates.</span></span> <span data-ttu-id="a3e89-146">وهو يتطلب إنشاء قيم الابعاد الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a3e89-146">It requires that dimension values already be created.</span></span> <span data-ttu-id="a3e89-147">مفتاح التكامل هو رقم المنتج (في حين أن مفتاح التكامل لكيان **متغيرات المنتج** هو المنتج الرئيسي بالإضافة إلى أبعاد المنتج).</span><span class="sxs-lookup"><span data-stu-id="a3e89-147">The integration key is the product number (whereas the integration key for the **Product variants** entity is the product master plus product dimensions).</span></span> |
| <span data-ttu-id="a3e89-148">متغيرات المنتج الذي تم إصداره</span><span class="sxs-lookup"><span data-stu-id="a3e89-148">Released product variants</span></span> | <span data-ttu-id="a3e89-149">EcoResReleasedProductVariantEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-149">EcoResReleasedProductVariantEntity</span></span> | <span data-ttu-id="a3e89-150">يتم استخدام هذا الكيان لاستيراد وتصدير متغيرات المنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="a3e89-150">This entity is used to import and export released product variants.</span></span> <span data-ttu-id="a3e89-151">إنها تسمح للحصول على التحديثات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-151">It allows for updates.</span></span> <span data-ttu-id="a3e89-152">يتطلب أن يتم إنشاء متغيرات المنتج المشتركة الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a3e89-152">It requires that shared product variants already be created.</span></span> <span data-ttu-id="a3e89-153">عند استيراد متغير منتج جديد تم إصداره، يحدث إصدار متغير للمنتج المشترك.</span><span class="sxs-lookup"><span data-stu-id="a3e89-153">When a new released product variant is imported, a release of the shared product variant occurs.</span></span> <span data-ttu-id="a3e89-154">لا يدعم هذا الكيان عمليات SQL المستندة إلى مجموعة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-154">This entity doesn't support set-based SQL operations.</span></span> <span data-ttu-id="a3e89-155">تم تمكينه ل OData.</span><span class="sxs-lookup"><span data-stu-id="a3e89-155">It's enabled for OData.</span></span> <span data-ttu-id="a3e89-156">على الرغم من أنه يدعم عمليات الحذف، إلا أن هذا الاستخدام يتسبب حاليًا في تلف البيانات نظرًا لوجود خطأ في النظام الأساسي الحالي.</span><span class="sxs-lookup"><span data-stu-id="a3e89-156">Although it supports delete operations, that use currently causes data corruption because of a bug in the current platform.</span></span> <span data-ttu-id="a3e89-157">لا يمكن تمديد هذا الكيان من خلال إضافة أبعاد جديدة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="a3e89-157">This entity can't be extended through the addition of new product dimensions.</span></span> |
| <span data-ttu-id="a3e89-158">متغيرات المنتجات الصادرة حسب تعريف رقم المنتج</span><span class="sxs-lookup"><span data-stu-id="a3e89-158">Released product variants by product number identification</span></span> | <span data-ttu-id="a3e89-159">EcoResProductNumberIdentifiedReleasedProductVariantEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-159">EcoResProductNumberIdentifiedReleasedProductVariantEntity</span></span> | <span data-ttu-id="a3e89-160">يشبه هذا الكيان كيان **متغيرات المنتج الذي تم إصداره‬** ، ولكن مفتاح التكامل هو رقم المنتج بدلاً من المنتج الرئيسي بالإضافة إلى أبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="a3e89-160">This entity resembles the **Released product variants** entity, but the integration key is the product number instead of the product master plus product dimensions.</span></span> <span data-ttu-id="a3e89-161">يمكن تمديده من خلال إضافة أبعاد المنتج الجديد.</span><span class="sxs-lookup"><span data-stu-id="a3e89-161">It can be extended through the addition of new product dimensions.</span></span> |
| <span data-ttu-id="a3e89-162">منتجات قابلة للبيع تم إصدارها</span><span class="sxs-lookup"><span data-stu-id="a3e89-162">Sellable released products</span></span> | <span data-ttu-id="a3e89-163">EcoResSellableReleasedProductEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-163">EcoResSellableReleasedProductEntity</span></span> | <span data-ttu-id="a3e89-164">يُستخدم هذا الكيان لتصدير المنتجات القابلة للبيع فقط.</span><span class="sxs-lookup"><span data-stu-id="a3e89-164">This entity is used to export only sellable products.</span></span> <span data-ttu-id="a3e89-165">المنتجات القابلة للبيع هي المنتجات التي تشتمل على المعلومات المطلوبة لكي يتم استخدامها في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-165">Sellable products are products that have the information that they require in order to be used in a sales order.</span></span> <span data-ttu-id="a3e89-166">تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.</span><span class="sxs-lookup"><span data-stu-id="a3e89-166">The same rules apply when a product is validated by using the **Validate** function on the **Released products** page.</span></span> |
| <span data-ttu-id="a3e89-167">المنتجات المميزة الصادرة‬ V2</span><span class="sxs-lookup"><span data-stu-id="a3e89-167">Released Distinct products V2</span></span> | <span data-ttu-id="a3e89-168">EcoResDistinctProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="a3e89-168">EcoResDistinctProductV2Entity</span></span> | <span data-ttu-id="a3e89-169">يُستخدم هذا الكيان لتصدير المنتجات المميزة.</span><span class="sxs-lookup"><span data-stu-id="a3e89-169">This entity is used to export distinct products.</span></span> <span data-ttu-id="a3e89-170">يمكن أن تكون هذه المنتجات المميزة منتجات ومنتجات فرعية ومتغيرات منتجات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-170">Those distinct products can be products, subtype products, and product variants.</span></span> |
| <span data-ttu-id="a3e89-171">أصول المنتجات التي تم إصدارها V2</span><span class="sxs-lookup"><span data-stu-id="a3e89-171">Released products masters V2</span></span> | <span data-ttu-id="a3e89-172">EcoResProductMasterV2Entity</span><span class="sxs-lookup"><span data-stu-id="a3e89-172">EcoResProductMasterV2Entity</span></span> | <span data-ttu-id="a3e89-173">يُستخدم هذا الكيان لاستيراد وتصدير أصول المنتجات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-173">This entity is used to import and export product masters.</span></span> <span data-ttu-id="a3e89-174">لم يتم تمكينه لإدارة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a3e89-174">It isn't enabled for data management.</span></span> |
| <span data-ttu-id="a3e89-175">الصنف - الرمز الشريطي</span><span class="sxs-lookup"><span data-stu-id="a3e89-175">Item - bar code</span></span> | <span data-ttu-id="a3e89-176">EcoResProductBarcodeEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-176">EcoResProductBarcodeEntity</span></span> | <span data-ttu-id="a3e89-177">يُستخدم هذا الكيان لتصدير المنتجات والأكواد الشريطية‬.</span><span class="sxs-lookup"><span data-stu-id="a3e89-177">This entity is used to export products and bar codes.</span></span> |
| <span data-ttu-id="a3e89-178">حالات دورة حياة المنتج</span><span class="sxs-lookup"><span data-stu-id="a3e89-178">Product lifecycle states</span></span> | <span data-ttu-id="a3e89-179">EcoResProductLifecycleSateEntity</span><span class="sxs-lookup"><span data-stu-id="a3e89-179">EcoResProductLifecycleSateEntity</span></span> | <span data-ttu-id="a3e89-180">يُستخدم هذا الكيان لاستيراد وتصدير حالات دورة حياة المنتج المختلفة التي يمكن تخصيصها لمنتج ما.</span><span class="sxs-lookup"><span data-stu-id="a3e89-180">This entity is used to import and export the different product lifecycle states that can be assigned to a product.</span></span> |

> [!NOTE]
> <span data-ttu-id="a3e89-181">يمكنك استخدام كيان بيانات **المنتجات التي تم إصدارها V2** لاستيراد المنتجات إلى النظام فقط إذا تم بالفعل إنشاء المنتج المشترك.</span><span class="sxs-lookup"><span data-stu-id="a3e89-181">You can use the **Released Products V2** data entity to import products into the system only if the shared product has already been created.</span></span> <span data-ttu-id="a3e89-182">وبخلاف ذلك، لاستيراد المنتجات إلى النظام، يجب عليك استخدام كيان بيانات **إنشاء المنتج** .</span><span class="sxs-lookup"><span data-stu-id="a3e89-182">Otherwise, to import products into the system, you must use the **Product creation** data entity.</span></span>