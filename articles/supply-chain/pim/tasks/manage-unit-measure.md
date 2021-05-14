---
title: إدارة وحدات القياس
description: يصف هذا الموضوع كيفية تحديد وحدة قياس، وتوفير ترجمات للوحدة ووصفها، وتحديد قواعد التحويل للوحدات ذات الصلة.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921331"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="8c9ba-103">إدارة وحدات القياس</span><span class="sxs-lookup"><span data-stu-id="8c9ba-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c9ba-104">يصف هذا الموضوع كيفية تحديد وحدة قياس، وتوفير ترجمات للوحدة ووصفها، وتحديد قواعد التحويل للوحدات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="8c9ba-105">فتح صفحة الوحدات</span><span class="sxs-lookup"><span data-stu-id="8c9ba-105">Open the Units page</span></span>

<span data-ttu-id="8c9ba-106">لإنشاء وحدات القياس المتوفرة في نظامك والعمل معها، انتقل إلى **إدارة المؤسسة \> الإعداد \> الوحدات \> الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="8c9ba-107">تصف الأقسام المتبقية من هذا الموضوع ما يمكنك القيام به في صفحة **الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="8c9ba-108">إنشاء الوحدات القياسية والتحويلات</span><span class="sxs-lookup"><span data-stu-id="8c9ba-108">Create standard units and conversions</span></span>

<span data-ttu-id="8c9ba-109">إذا كان نظامك لا يتضمن بالفعل وحدات القياس الأكثر استخدامًا للنظام المتري و/أو النظام المتعارف عليه في الولايات المتحدة (USCS)، فيمكن أن يساعدك معالج إعداد الوحدة في البدء بسرعة في تعريفات الوحدات الأساسية والتحويلات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="8c9ba-110">لإكمال المعالج، حدد **معالج إنشاء الوحدات** في جزء الإجراءات، ثم اتبع الإرشادات التي تظهر على الشاشة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="8c9ba-111">إنشاء وحدة قياس أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="8c9ba-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="8c9ba-112">لإنشاء وحده قياس أو تحريرها، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="8c9ba-113">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8c9ba-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="8c9ba-114">لتحرير وحده موجودة، حددها في جزء القائمة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="8c9ba-115">لإنشاء وحدة جديدة، حدد **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="8c9ba-116">في رأس السجل، عيِّن الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8c9ba-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="8c9ba-117">**الوحدة** – أدخل المعرف أو الرمز المراد استخدامه للإشارة إلى الوحدة في لغة النظام.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="8c9ba-118">ويكون هذا المعرف أو الرمز عاده اختصارا شائعا للوحدة، مثل *ea* لكل أو *cm* لسنتيمتر.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="8c9ba-119">**الوصف** – أدخل اسمًا وصفيًا للوحدة بلغة النظام.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="8c9ba-120">عاده ما يكون هذا الاسم هو الاسم الكامل للوحدة، مثل *كل من* أو *سنتيمتر*.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="8c9ba-121">في علامة التبويب السريعة **عام**، اضبط الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8c9ba-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="8c9ba-122">**فئة الوحدة** – حدد الخاصية التي تقيسها الوحدة (مثل الطول أو المساحة أو الكتلة أو الكمية).</span><span class="sxs-lookup"><span data-stu-id="8c9ba-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="8c9ba-123">**نظام الوحدات** – حدد نظام القياس الذي تنتمي إليه الوحدة ( *الوحدات المترية* أو *الوحدات العرفية للولايات المتحدة*).</span><span class="sxs-lookup"><span data-stu-id="8c9ba-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="8c9ba-124">**الوحدة الأساسية** – قم بتعيين هذا الخيار إلى *نعم* لاستخدام الوحدة الحالية كوحدة أساسيه لفئة الوحدة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="8c9ba-125">في هذه الحالة، ما عليك سوى تحديد عامل التحويل بين الوحدة الأساسية وكل وحدة إضافية في فئة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="8c9ba-126">يمكن للنظام بعد ذلك التحويل بين جميع الوحدات في فئة الوحدة هذه.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="8c9ba-127">لذلك، من الأسهل إعداد التحويلات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="8c9ba-128">على سبيل المثال، إذا كان الغالون هو الوحدة الأساسية لفئة وحدة *الحجم*، ما عليك سوى إعداد عوامل التحويل من كوارت إلى جالون ومن نصف لتر إلى جالون.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="8c9ba-129">ويمكن بعد ذلك للنظام أيضا التحويل من كوارت إلى بينت.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="8c9ba-130">يمكن ان يكون لديك وحده أساسيه واحده لكل فئة وحده.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="8c9ba-131">**وحدة النظام** – قم بتعيين هذا الخيار إلى *نعم* لاستخدام الوحدة الحالية كوحدة مفترضة لجميع القياسات غير المحددة في فئة الوحدة الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="8c9ba-132">على سبيل المثال، إذا كان الحقل المستخدم لإدخال كمية لا يسمح بتحديد وحدة (إذا لم يحدد المستخدم وحدة)، فسيستخدم النظام الوحدة التي تم تعيينها كوحدة نظام لفئة وحدة *الكمية*.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="8c9ba-133">يمكنك الحصول على وحدة نظام واحدة فقط لكل فئة وحدة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="8c9ba-134">**الدقة العشرية** – حدد عدد المنازل العشرية التي يجب تقريب القيم المحددة للوحدة الحالية أو المحولة إليها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="8c9ba-135">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="8c9ba-136">تعريف ترجمات الوحدة</span><span class="sxs-lookup"><span data-stu-id="8c9ba-136">Define unit translations</span></span>

<span data-ttu-id="8c9ba-137">لتعريف الترجمات للمعرف أو الرمز ووصف وحدة القياس، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="8c9ba-138">إنشاء أو تحديد الوحدة لإنشاء ترجمات لها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="8c9ba-139">في جزء الإجراءات، حدد **نصوص الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="8c9ba-140">سوف تظهر صفحة **نصوص الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="8c9ba-141">تستخدم هذه الصفحة لتعريف الترجمات للمعرف أو الرمز للوحدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="8c9ba-142">يمكن بعد ذلك استخدام هذه الترجمات في المستندات الخارجية باللغات الخاصة بالعميل أو الخاصة بالمورد.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="8c9ba-143">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8c9ba-144">في حقل **اللغة**، حدد اللغة التي تريد ترجمة معرف الوحدة أو الرمز إليها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="8c9ba-145">في حقل **النص**، أدخل ترجمة معرف الوحدة أو الرمز في اللغة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="8c9ba-146">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8c9ba-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-147">Close the page.</span></span>
1. <span data-ttu-id="8c9ba-148">في **جزء الإجراءات**، حدد **أوصاف الوحدات المترجمة‬‬**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="8c9ba-149">تظهر صفحة **أوصاف الوحدات المترجمة**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="8c9ba-150">تستخدم هذه الصفحة لتعريف الأوصاف الخاصة باللغة للوحدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="8c9ba-151">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8c9ba-152">في حقل **اللغة**، حدد اللغة التي تريد ترجمة وصف الوحدة إليها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="8c9ba-153">في حقل **الوصف**، أدخل ترجمة وصف الوحدة باللغة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="8c9ba-154">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8c9ba-155">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="8c9ba-156">تعريف قواعد تحويل الوحدة</span><span class="sxs-lookup"><span data-stu-id="8c9ba-156">Define unit conversion rules</span></span>

<span data-ttu-id="8c9ba-157">لتحديد قواعد التحويلات بين وحدات القياس، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="8c9ba-158">إنشاء أو تحديد الوحدة لتحديد قواعد التحويل لها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="8c9ba-159">في جزء الإجراءات، حدد **تحويلات الوحدة**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="8c9ba-160">تظهر صفحة **تحويلات الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="8c9ba-161">تستخدم هذه الصفحة لتعريف قواعد تحويل الوحدة المحددة إلى ومن الوحدات الأخرى في فئة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="8c9ba-162">حدد إحدى علامات التبويب التالية، بناءً على نوع التحويل الذي تريد إعداده:</span><span class="sxs-lookup"><span data-stu-id="8c9ba-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="8c9ba-163">**التحويلات القياسية** – قم بإعداد قواعد التحويل القياسية لجميع المنتجات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="8c9ba-164">**التحويلات بين الفئات** – قم بإعداد قواعد التحويل الخاصة بالمنتج للوحدات في نفس فئة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="8c9ba-165">**التحويلات بين الفئات** – قم بإعداد قواعد التحويل الخاصة بالمنتج للوحدات عبر فئات الوحدات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="8c9ba-166">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8c9ba-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="8c9ba-167">لإنشاء تحويل جديد، حدد **جديد** في شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="8c9ba-168">لتحرير تحويل موجود، حدد التحويل في الشبكة، ثم حدد **تحرير** في شريط الأدوات.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="8c9ba-169">في مربع حوار القائمة المنسدلة الذي يظهر، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8c9ba-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="8c9ba-170">**المنتج** - حدد المنتج المحدد الذي ينطبق عليه التحويل.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="8c9ba-171">يتوفر هذا الحقل فقط لعمليات التحويل بين الفئات والفئات الداخلية.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="8c9ba-172">**تخطيط المعادلة** – اترك هذا الحقل معينًا إلى *بسيط* لتحديد تحويل بسيط له عامل واحد.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="8c9ba-173">قم بتعيينه إلى *متقدم* لإعداد معادلة أكثر تعقيدًا.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="8c9ba-174">يختلف تنسيق المعادلات المتقدمة حسب فئة الوحدة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="8c9ba-175">**من الوحدة** – يعرض هذا الحقل الوحدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="8c9ba-176">عادة، يجب ألا يتم تغيير القيمة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-176">Usually, you should not change the value.</span></span> <span data-ttu-id="8c9ba-177">(إذا قمت بتغيير القيمة، يجب عليك فتح صفحة **تحويلات الوحدات** للوحدة المحددة لعرض التحويل الجديد بعد حفظه.)</span><span class="sxs-lookup"><span data-stu-id="8c9ba-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="8c9ba-178">**إلى الوحدة** – حدد الوحدة التي سيتم التحويل إليها.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="8c9ba-179">**التقريب** – حدد كيفية تقريب الكسور بناءً على قيمة **الدقة العشرية** للوحدة المحددة (*إلى الأقرب*، أو *لأعلى*، أو *لأسفل*).</span><span class="sxs-lookup"><span data-stu-id="8c9ba-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="8c9ba-180">**معادلة التحويل** – استخدم الحقول المتبقية في أعلى مربع حوار القائمة المنسدلة لتحديد صيغة التحويل بين الوحدتين.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="8c9ba-181">تختلف الحقول المتاحة، بناءً على فئة الوحدة وتخطيط الصيغة الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="8c9ba-182">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-182">Select **OK**.</span></span>
1. <span data-ttu-id="8c9ba-183">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="8c9ba-184">يمكنك أيضًا إعداد تحويلات الوحدات لكل متغير منتج.</span><span class="sxs-lookup"><span data-stu-id="8c9ba-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="8c9ba-185">لمزيد من المعلومات، راجع [تحويل وحدة القياس لكل متغير منتج](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="8c9ba-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
