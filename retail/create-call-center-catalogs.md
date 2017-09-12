---
title: "إنشاء كتالوج مركز الاتصالات"
description: "توفر هذه المقالة نظرة عامة على عملية إنشاء كتالوج‬ لمركز اتصالات."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 94ff6d74d4a11b3b04be6b69f85e778c3b45de92
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="create-a-call-center-catalog"></a><span data-ttu-id="87c60-103">إنشاء كتالوج مركز الاتصالات</span><span class="sxs-lookup"><span data-stu-id="87c60-103">Create a call center catalog</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="87c60-104">توفر هذه المقالة نظرة عامة على عملية إنشاء كتالوج‬ لمركز اتصالات.</span><span class="sxs-lookup"><span data-stu-id="87c60-104">This article provides an overview of the process for creating a catalog for a call center.</span></span> 

<span data-ttu-id="87c60-105">في مركز الاتصال، يمكنك استخدام كتالوجات منتجات لتحديد المنتجات التي تريد عرضها للعملاء.</span><span class="sxs-lookup"><span data-stu-id="87c60-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="87c60-106">عادة، تستخدم مراكز الاتصال الكتالوجات المطبوعة.</span><span class="sxs-lookup"><span data-stu-id="87c60-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="87c60-107">تتم معالجة تصميم وإنتاج الكتالوجات المطبوعة خارج Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="87c60-107">The design and production of a printed catalog is handled outside Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="87c60-108">ومع ذلك، يمكنك إنشاء وتخزين نموذج رقمي لكتالوج باستخدام نفس النماذج التي استخدمتها لإعداد كتالوجات البيع بالتجزئة على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="87c60-108">However, you can create and store a digital form of a catalog by using the same forms that you use to set up online retail catalogs.</span></span> <span data-ttu-id="87c60-109">قبل إنشاء كتالوج، يجب إعداد عمليات فرز المنتجات وتعيين عمليات الفرز إلى مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="87c60-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="87c60-110">يمكنك أيضا إضافة منتجات إلى الكتالوج من خلال تحديد المنتجات من عمليات الفرز هذه.</span><span class="sxs-lookup"><span data-stu-id="87c60-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="87c60-111">بعد إضافة المنتجات إلى الكتالوج واكتمال الكتالوج، يجب التحقق من صحة الكتالوج للتحقق من البيانات.</span><span class="sxs-lookup"><span data-stu-id="87c60-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="87c60-112">ثم يجب إرسال الكتالوج لمراجعته واعتماده.</span><span class="sxs-lookup"><span data-stu-id="87c60-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="87c60-113">وبعد الموافقة على الكتالوج، يمكن نشره.</span><span class="sxs-lookup"><span data-stu-id="87c60-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="87c60-114">عندما يتم إنشاء كتالوج مركز الاتصال، يمكنك أخذ لقطة من بيانات الكتالوج في الوقت الذي يتم نشر الكتالوج فيه.</span><span class="sxs-lookup"><span data-stu-id="87c60-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time when the catalog is published.</span></span> <span data-ttu-id="87c60-115">تتيح لك وظيفة اللقطة هذه الوصول إلى إصدار معين من الكتالوج حتى في حالة تغيير الكتالوج وتحديثه لاحقاً.</span><span class="sxs-lookup"><span data-stu-id="87c60-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="87c60-116">يمكن أيضا إعداد كتالوجات مركز الاتصال لتتضمن الميزات الاختيارية التالية.</span><span class="sxs-lookup"><span data-stu-id="87c60-116">Call center catalogs can also be set up to include the following optional features.</span></span>

-   <span data-ttu-id="87c60-117">**رموز المصدر** – الرموز المستخدمة لتعقب استجابة العملاء للمراسلات البريدية لكتالوج معين.</span><span class="sxs-lookup"><span data-stu-id="87c60-117">**Source codes** – Codes that are used to track the customer response to particular catalog mailings.</span></span>
-   <span data-ttu-id="87c60-118">**المنتجات المجانية** - المنتجات المضمنة في أمر العميل بدون تكلفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="87c60-118">**Free products** – Products that are included in a customer's order at no additional charge.</span></span> <span data-ttu-id="87c60-119">تتم إضافة هذه المنتجات إلى الأمر تلقائياً عند إدخال التعليمات البرمجية المصدر للكتالوج في الأمر.</span><span class="sxs-lookup"><span data-stu-id="87c60-119">These products are automatically added to the order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="87c60-120">**البرامج النصية** – النصوص التي يقوم عامل مركز الاتصال بقرائتها للعميل عند إنشاء أمر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="87c60-120">**Scripts** – Texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="87c60-121">يمكن أن تتضمن البرامج النصية التهاني أو اقتراحات الشراء.</span><span class="sxs-lookup"><span data-stu-id="87c60-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="87c60-122">**الأصناف الإضافية أو المكملة** - الأصناف التي يتم عرضها كاقتراح عند إضافة منتج معين إلى الأمر.</span><span class="sxs-lookup"><span data-stu-id="87c60-122">**Upsell or cross-sell items** - Items that are displayed as a suggestion when a specific product is added to the order.</span></span>

<span data-ttu-id="87c60-123">يجب إعداد هذه الخيارات قبل اعتماد الكتالوج ونشره.</span><span class="sxs-lookup"><span data-stu-id="87c60-123">These options must be set up before the catalog is approved and published.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="87c60-124">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="87c60-124">Prerequisites</span></span>
<span data-ttu-id="87c60-125">يجب إكمال المهام التالية قبل البدء في:</span><span class="sxs-lookup"><span data-stu-id="87c60-125">The following tasks must be completed before you start:</span></span>

-   <span data-ttu-id="87c60-126">إعداد منتجات وعمليات فرز المنتجات.</span><span class="sxs-lookup"><span data-stu-id="87c60-126">Set up products and product assortments.</span></span>
-   <span data-ttu-id="87c60-127">إعداد منتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="87c60-127">Set up retail products.</span></span>
-   <span data-ttu-id="87c60-128">إعداد عملية فرز.</span><span class="sxs-lookup"><span data-stu-id="87c60-128">Set up an assortment.</span></span>
-   <span data-ttu-id="87c60-129">إنشاء مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="87c60-129">Create a call center.</span></span>
-   <span data-ttu-id="87c60-130">إعداد مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="87c60-130">Set up a call center.</span></span>
-   <span data-ttu-id="87c60-131">إضافة مركز اتصال لتدرج هرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="87c60-131">Add the call center to an organization hierarchy.</span></span>
-   <span data-ttu-id="87c60-132">إنشاء تدرجي هرمي للمؤسسة وتعديله.</span><span class="sxs-lookup"><span data-stu-id="87c60-132">Create or modify an organization hierarchy.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="87c60-133">إنشاء كتالوج</span><span class="sxs-lookup"><span data-stu-id="87c60-133">Create a catalog</span></span>
<span data-ttu-id="87c60-134">يجب أولاً إنشاء كتالوج، ثم إضافة منتجات إلى الكتالوج ثم مراجعة وتحديث السمات الخاصة بالمنتجات.</span><span class="sxs-lookup"><span data-stu-id="87c60-134">You must first create a catalog, add products to the catalog, and then review and update the attributes for the products.</span></span>

## <a name="validate-the-catalog"></a><span data-ttu-id="87c60-135">التحقق من صحة الكتالوج</span><span class="sxs-lookup"><span data-stu-id="87c60-135">Validate the catalog</span></span>
<span data-ttu-id="87c60-136">بعد الانتهاء من إعداد الكتالوج، يجب التحقق من صحته.</span><span class="sxs-lookup"><span data-stu-id="87c60-136">After you've finished setting up the catalog, you must validate it.</span></span> <span data-ttu-id="87c60-137">يتم من خلال هذه العملية التحقق من أن البيانات المطلوبة لسمات القناة وسمات المنتج كاملة وصحيحة، وأنه تم نشر الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="87c60-137">The validation process verifies that the data that is required for channel attributes and product attributes is complete and valid, and that the catalog can be published.</span></span>

## <a name="submit-the-catalog-for-review-and-approval"></a><span data-ttu-id="87c60-138">إرسال الكتالوج للمراجعة والاعتماد</span><span class="sxs-lookup"><span data-stu-id="87c60-138">Submit the catalog for review and approval</span></span>
<span data-ttu-id="87c60-139">بعد التحقق من صحة كتالوج، يمكنه إرساله للمراجعة والموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="87c60-139">After a catalog is validated, you can submit the catalog for review and approval.</span></span> <span data-ttu-id="87c60-140">يجب الموافقة على الكتالوج قبل نشره.</span><span class="sxs-lookup"><span data-stu-id="87c60-140">A catalog must be approved before it can be published.</span></span> <span data-ttu-id="87c60-141">يمكنك تكوين سير العمل حتى تتم الموافقة على الكتالوج تلقائيًا أو يجب الموافقة عليه يدويًا.</span><span class="sxs-lookup"><span data-stu-id="87c60-141">You can configure a workflow so that catalogs either are automatically approved or require manual approval.</span></span>

## <a name="optional-add-source-codes-free-products-and-scripts"></a><span data-ttu-id="87c60-142">اختياري: إضافة التعليمات البرمجية المصدر والمنتجات المجانية والبرامج النصية</span><span class="sxs-lookup"><span data-stu-id="87c60-142">Optional: Add source codes, free products, and scripts</span></span>
<span data-ttu-id="87c60-143">يمكنك أيضًا إضافة الأصناف التالية إلى كتالوج مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="87c60-143">You can also add the following items to a call center catalog.</span></span> <span data-ttu-id="87c60-144">هذه الأصناف اختيارية.</span><span class="sxs-lookup"><span data-stu-id="87c60-144">These items are optional.</span></span>

-   <span data-ttu-id="87c60-145">**الأكواد المصدر** يمكن استخدامها من قِبل الشركات التي تقدم الكتالوجات المطبوعة لتعقب استجابة العملاء لكتالوجات معينة.</span><span class="sxs-lookup"><span data-stu-id="87c60-145">**Source codes** can be used by companies that provide printed catalogs to track the customer response to particular catalogs.</span></span> <span data-ttu-id="87c60-146">غالبًا ما تطبع أكواد المصدر على الجزء الخلفي من الكتالوج ويتم إدخالها في أمر المبيعات عندما يقوم العميل بعملية شراء.</span><span class="sxs-lookup"><span data-stu-id="87c60-146">Source codes are often printed on the back of a catalog and are entered into the sales order when a customer makes a purchase.</span></span> <span data-ttu-id="87c60-147">ولإضافة كود مصدر إلى الكتالوج، يجب أولاً إنشاء سوق هدف.</span><span class="sxs-lookup"><span data-stu-id="87c60-147">To add a source code to the catalog, you must first create a target market.</span></span> <span data-ttu-id="87c60-148">ويتم تعيين السوق الهدف عادةً إلى قائمة المراسلات المملوكة أو المستأجرة.‬</span><span class="sxs-lookup"><span data-stu-id="87c60-148">The target market is usually mapped to an owned or rented mailing list.</span></span>
-   <span data-ttu-id="87c60-149">**المنتجات المجانية** عبارة عن أصناف ترويجية يتم تضمينها بدون مقابل في أمر العميل عند الرجوع إلى الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="87c60-149">**Free products** are promotional items that are included free of charge with the customer's order when the catalog is referenced.</span></span>
-   <span data-ttu-id="87c60-150">**البرامج النصية** يمكن استخدامها لتوجيه تفاعلات العامل مع العملاء في سياق كتالوج أو منتج في كتالوج.</span><span class="sxs-lookup"><span data-stu-id="87c60-150">**Scripts** can be used to guide the worker's interactions with customers in the context of a catalog or a product within a catalog.</span></span>

## <a name="publish-the-catalog"></a><span data-ttu-id="87c60-151">نشر الكتالوج</span><span class="sxs-lookup"><span data-stu-id="87c60-151">Publish the catalog</span></span>
<span data-ttu-id="87c60-152">إذا قمت بنشر الكتالوج لمركز الاتصالات، فإنك ستقوم بذلك بإنهاء معلومات المنتج في الكتالوج.</span><span class="sxs-lookup"><span data-stu-id="87c60-152">By publishing a catalog for a call center, you finalize the product information in the catalog.</span></span> <span data-ttu-id="87c60-153">المنشور أيضا يشير إلى أن الكتالوج جاهز لأي إجراءات إضافية تريد تنفيذها.</span><span class="sxs-lookup"><span data-stu-id="87c60-153">Publication also indicates that the catalog is ready for any additional actions that you want to perform.</span></span> <span data-ttu-id="87c60-154">على سبيل المثال، يمكنك إنشاء كتالوج مطبوع.</span><span class="sxs-lookup"><span data-stu-id="87c60-154">For example, you can create a printed catalog.</span></span> <span data-ttu-id="87c60-155">يمكنك نشر كتالوجاتك يدوياً، أو يمكنك استخدام معالجة دُفعة للنشر استنادا إلى أحد الجداول.</span><span class="sxs-lookup"><span data-stu-id="87c60-155">You can publish your catalogs manually, or you can use a batch process to publish according to a schedule.</span></span> <span data-ttu-id="87c60-156">قبل نشر كتالوج، يجب التحقق من صحة الكتالوج والموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="87c60-156">Before you can publish a catalog, the catalog must be validated and approved.</span></span> <span data-ttu-id="87c60-157">لتغيير الكتالوج بعد أن تم نشره، يمكنك سحب الكتالوج، ثم يمكنك إعادة نشره.</span><span class="sxs-lookup"><span data-stu-id="87c60-157">To change the catalog after it's published, you can retract the catalog and then republish it.</span></span>




