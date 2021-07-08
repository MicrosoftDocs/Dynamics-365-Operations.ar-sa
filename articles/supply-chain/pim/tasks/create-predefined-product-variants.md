---
title: إنشاء متغيرات المنتج المعرفة مسبقًا
description: يتناول هذا الإجراء إنشاء متغيرات المنتجات لأصل المنتج باستخدام مجموعات أبعاد المنتجات.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270470"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="8e936-103">متغيرات المنتج المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="8e936-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="8e936-104">سيناريو مثال: إنشاء متغيرات المنتج المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="8e936-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="8e936-105">يوضح سيناريو المثال هذا كيفية إنشاء متغيرات المنتج لأصل منتج باستخدام مجموعات من أبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="8e936-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="8e936-106">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="8e936-106">Make demo data available</span></span>

<span data-ttu-id="8e936-107">لمتابعة هذا السيناريو باستخدام القيم المقترحة هنا ، يجب أن يكون لديك بيانات الإصدار التجريبي مثبتة ، ويجب عليك تحديد الكيان القانوني لـ *USMF*.</span><span class="sxs-lookup"><span data-stu-id="8e936-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="8e936-108">الخطوة 1: إنشاء أصل منتج</span><span class="sxs-lookup"><span data-stu-id="8e936-108">Step 1: Create a product master</span></span>

<span data-ttu-id="8e936-109">لإنشاء أصل منتج:</span><span class="sxs-lookup"><span data-stu-id="8e936-109">To create a product master:</span></span>

1. <span data-ttu-id="8e936-110">انتقل إلى **إدارة معلومات المنتج‬ > المنتجات > أصول المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="8e936-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="8e936-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8e936-111">Select **New**.</span></span>
1. <span data-ttu-id="8e936-112">إذا لم يعرض حقل **رقم المنتج** رقمًا بالفعل، فأدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="8e936-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="8e936-113">هذا مطلوب فقط إذا لم يتم تعيين تسلسل رقمي لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="8e936-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="8e936-114">أدخل اسمًا في حقل **اسم المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8e936-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="8e936-115">في حقل **مجموعة أبعاد المنتجات**، حدد مجموعة أبعاد المنتج *SizeCol* (الحجم واللون).</span><span class="sxs-lookup"><span data-stu-id="8e936-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="8e936-116">حدد **موافق** لإنشاء المنتج الرئيسي الجديد وفتحه.</span><span class="sxs-lookup"><span data-stu-id="8e936-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="8e936-117">الخطوة 2: إضافة أبعاد المنتجات</span><span class="sxs-lookup"><span data-stu-id="8e936-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="8e936-118">يوضح هذا المثال كيفية إدخال أبعاد المنتجات يدويًا.</span><span class="sxs-lookup"><span data-stu-id="8e936-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="8e936-119">يمكنك كذلك اختيار تحديد الحجم أو اللون أو مجموعة النمط التي تتضمن قيم بُعد المنتج الذي تريد استخدامه.</span><span class="sxs-lookup"><span data-stu-id="8e936-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="8e936-120">لإضافة أبعاد المنتجات:</span><span class="sxs-lookup"><span data-stu-id="8e936-120">To add product dimensions:</span></span>

1. <span data-ttu-id="8e936-121">مع بقاء المنتج الرئيسي الجديد مفتوحًا، حدد **أبعاد المنتج** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="8e936-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="8e936-122">افتح علامة التبويب **الحجم**، وحدد **جديد** على شريط الأدوات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="8e936-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="8e936-123">قم بإجراء الإعدادات التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="8e936-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="8e936-124">**الحجم:** حدد قيمة حجم.</span><span class="sxs-lookup"><span data-stu-id="8e936-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="8e936-125">**الاسم‏‎**: أدخل اسمًا للحجم.</span><span class="sxs-lookup"><span data-stu-id="8e936-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="8e936-126">حدد **جديد** على شريط الأدوات وأضف حجمًا ثانيًا إلى الشبكة باستخدام **حجم** و **اسم** جديدين.</span><span class="sxs-lookup"><span data-stu-id="8e936-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="8e936-127">افتح علامة التبويب **الألوان**، وحدد **جديد** على شريط الأدوات لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="8e936-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="8e936-128">قم بإجراء الإعدادات التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="8e936-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="8e936-129">**اللون:** حدد قيمة لون.</span><span class="sxs-lookup"><span data-stu-id="8e936-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="8e936-130">**الاسم:‏‎** أدخل اسمًا للون.</span><span class="sxs-lookup"><span data-stu-id="8e936-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="8e936-131">حدد **جديد** على شريط الأدوات وأضف لونًا ثانيًا إلى الشبكة باستخدام **لون** و **اسم** جديدين.</span><span class="sxs-lookup"><span data-stu-id="8e936-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="8e936-132">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8e936-132">Select **Save**.</span></span>
1. <span data-ttu-id="8e936-133">أغلق الصفحة للعودة إلى منتجك الرئيسي الجديد.</span><span class="sxs-lookup"><span data-stu-id="8e936-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="8e936-134">الخطوة 3: إنشاء متغيرات المنتج</span><span class="sxs-lookup"><span data-stu-id="8e936-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="8e936-135">يصف هذا القسم كيفية إنشاء متغيرات المنتج عند عدم تمكين ميزة *تحسينات صفحة اقتراحات المتغير*.</span><span class="sxs-lookup"><span data-stu-id="8e936-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="8e936-136">راجع القسم التالي للحصول على تفاصيل حول كيفية إنشاء متغيرات المنتج عندما تكون هذه الميزة متاحة.</span><span class="sxs-lookup"><span data-stu-id="8e936-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="8e936-137">لإنشاء متغيرات المنتج:</span><span class="sxs-lookup"><span data-stu-id="8e936-137">To generate product variants:</span></span>

1. <span data-ttu-id="8e936-138">مع بقاء المنتج الرئيسي الجديد مفتوحًا، حدد **متغيرات المنتج** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="8e936-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="8e936-139">في جزء الإجراءات، حدد **اقتراحات المتغيرات**.</span><span class="sxs-lookup"><span data-stu-id="8e936-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="8e936-140">يُنشئ النظام قائمة بجميع التركيبات الممكنة للأحجام والألوان التي حددتها للمنتج.</span><span class="sxs-lookup"><span data-stu-id="8e936-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="8e936-141">حدد **تحديد الكل** على شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="8e936-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="8e936-142">في هذا المثال ، حدد جميع المتغيرات المحتملة.</span><span class="sxs-lookup"><span data-stu-id="8e936-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="8e936-143">إذا كنت تريد فقط استخدام مجموعة فرعية من مجموعات أبعاد المنتج الممكنة ، فحدد فقط خانات الاختيار المطلوبة حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8e936-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="8e936-144">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="8e936-144">Select **Create**.</span></span>
1. <span data-ttu-id="8e936-145">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8e936-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="8e936-146">اقتراحات المتغيرات المحسَّنة</span><span class="sxs-lookup"><span data-stu-id="8e936-146">Improved variant suggestions</span></span>

<span data-ttu-id="8e936-147">تعمل ميزة *تحسينات صفحة اقتراحات المتغيرات* على تحسين صفحة **اقتراحات المتغيرات** لمعالجة مشكلات الأداء وقابلية الاستخدام للشركات التي لديها عدد كبير من مجموعات أبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="8e936-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="8e936-148">تجعل العملية المحسّنة لاختيار قيم أبعاد المنتج التي يتم من أجلها إنشاء اقتراحات متغيرة من الأسرع والأسهل تحديد مجموعة متغيرات المنتج ذات الصلة وإصدارها.</span><span class="sxs-lookup"><span data-stu-id="8e936-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="8e936-149">تتم إضافة التحسينات التالية بواسطة هذه الميزة:</span><span class="sxs-lookup"><span data-stu-id="8e936-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="8e936-150">**تأجيل إنشاء اقتراحات المتغيرات:** لم تعد صفحة **اقتراحات المتغيرات** تعرض الاقتراحات عند فتحها لأول مرة.</span><span class="sxs-lookup"><span data-stu-id="8e936-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="8e936-151">بدلاً من ذلك ، يجب أن تختار صراحة القيم التي ستحتاج إليها ثم تحدد زر **اقتراح** لإنشاء التركيبات.</span><span class="sxs-lookup"><span data-stu-id="8e936-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="8e936-152">هذا يجعل العملية أكثر وضوحا وتفاعلية.</span><span class="sxs-lookup"><span data-stu-id="8e936-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="8e936-153">**تحديد قيم الأبعاد:** عندما يكون لديك العديد من قيم الأبعاد ، فأنت مهتم عادةً بإنشاء اقتراحات متغيرات تتضمن القليل منها فقط (على سبيل المثال عند تقديم مجموعة جديدة من الألوان أو الأنماط).</span><span class="sxs-lookup"><span data-stu-id="8e936-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="8e936-154">باستخدام التصميم المحسّن ، يمكنك تحديد قيم الأبعاد التي تريد إنشاء اقتراحات متغيرات المنتج لها.</span><span class="sxs-lookup"><span data-stu-id="8e936-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="8e936-155">هذا يزيد بشكل كبير من أهمية المتغيرات المقترحة ويحسن أداء النظام وإنتاجية المستخدم.</span><span class="sxs-lookup"><span data-stu-id="8e936-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="8e936-156">تشغيل ميزة تحسينات صفحة اقتراحات المتغيرات</span><span class="sxs-lookup"><span data-stu-id="8e936-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="8e936-157">قبل أن تتمكن من استخدام ميزة *تحسينات صفحة اقتراحات المتغيرات*، يجب تشغيلها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8e936-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="8e936-158">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="8e936-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="8e936-159">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="8e936-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="8e936-160">**الوحدة النمطية** *إدارة معلومات المنتج*</span><span class="sxs-lookup"><span data-stu-id="8e936-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="8e936-161">**اسم الميزة:** *تحسينات صفحة اقتراحات المتغيرات*</span><span class="sxs-lookup"><span data-stu-id="8e936-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="8e936-162">العمل مع اقتراحات المتغيرات المحسنة</span><span class="sxs-lookup"><span data-stu-id="8e936-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="8e936-163">لإنشاء اقتراحات متغيرات المنتجات عند تمكين ميزة *تحسينات صفحة اقتراحات المتغيرات*:</span><span class="sxs-lookup"><span data-stu-id="8e936-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="8e936-164">افتح أو أنشئ أصل منتج وأضف أبعاد المنتج المطلوبة إليه ، كما هو موضح في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="8e936-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="8e936-165">مع فتح المنتج الرئيسي الجديد، حدد **متغيرات المنتج** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="8e936-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="8e936-166">في جزء الإجراءات، حدد **اقتراحات المتغيرات**.</span><span class="sxs-lookup"><span data-stu-id="8e936-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="8e936-167">حدد القيم التي تريد استخدامها لكل بعد من الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="8e936-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="8e936-168">في شريط الأدوات العلوي، حدد **اقتراح**.</span><span class="sxs-lookup"><span data-stu-id="8e936-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="8e936-169">يُنشئ النظام قائمة بجميع التركيبات الممكنة للأحجام والألوان التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="8e936-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="8e936-170">في علامة التبويب السريع **المتغيرات المقترحة**، حدد خانة الاختيار لكل تركيبة أبعاد منتج تريد استخدامها أو حدد **تحديد الكل** على شريط الأدوات لتحديدها كلها.</span><span class="sxs-lookup"><span data-stu-id="8e936-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="8e936-171">حدد **إنشاء** لإضافة المتغيرات إلى أصل المنتج الحالي.</span><span class="sxs-lookup"><span data-stu-id="8e936-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
