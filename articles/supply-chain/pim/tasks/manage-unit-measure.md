---
title: إدارة وحدة القياس
description: يوضح هذا الإجراء كيفية تحديد وحدة قياس وتقديم ترجمات للوحدة ووصفها وتعريف قواعد التحويل للوحدات ذات الصلة.
author: sorenva
manager: AnnBe
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f26b55f6e79200ac273fbb642c49998d8cd7e388
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147608"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="826b2-103">إدارة وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="826b2-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="826b2-104">يوضح هذا الإجراء كيفية تحديد وحدة قياس وتقديم ترجمات للوحدة ووصفها وتعريف قواعد التحويل للوحدات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="826b2-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="826b2-105">يمكنك استعراض هذا الإجراء باستخدام بيانات العرض التوضيحي أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="826b2-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="826b2-106">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة معلومات المنتج > صيانة المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="826b2-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="826b2-107">انقر فوق **الوحدات**.</span><span class="sxs-lookup"><span data-stu-id="826b2-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="826b2-108">إنشاء وحدة قياس</span><span class="sxs-lookup"><span data-stu-id="826b2-108">Create a unit of measure</span></span>
1. <span data-ttu-id="826b2-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="826b2-109">Click **New**.</span></span>
2. <span data-ttu-id="826b2-110">في الحقل **الوحدة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="826b2-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="826b2-111">أدخل المعرف أو الرمز لاستخدامه عند الإشارة إلى وحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="826b2-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="826b2-112">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="826b2-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="826b2-113">أدخل اسمًا وصفيًا لوحدة القياس في لغة النظام.</span><span class="sxs-lookup"><span data-stu-id="826b2-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="826b2-114">في الحقل **فئة الوحدة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="826b2-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="826b2-115">تحدد فئة الوحدة التجمع المنطقي، كالمنطقة أو الكتلة أو الكمية، الذي تشكل وحدة القياس جزءًا منه.</span><span class="sxs-lookup"><span data-stu-id="826b2-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="826b2-116">في حقل **الدقة العشرية‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="826b2-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="826b2-117">حدد عدد المنازل العشرية التي يجب تقريب وحدة القياس المحولة إليها عند اكتمال عملية حسابية لوحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="826b2-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="826b2-118">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="826b2-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="826b2-119">تعريف ترجمات الوحدة</span><span class="sxs-lookup"><span data-stu-id="826b2-119">Define unit translations</span></span>
1. <span data-ttu-id="826b2-120">في **جزء الإجراءات**، انقر فوق **نصوص الوحدات‬**.</span><span class="sxs-lookup"><span data-stu-id="826b2-120">On the **Action pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="826b2-121">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="826b2-121">Click **New**.</span></span> <span data-ttu-id="826b2-122">استخدم نص الوحدة لإنشاء ترجمة للمعرف أو رمز يمثل وحدة القياس لاستخدامها في المستندات الخارجية بلغات خاصة بالعميل أو المورّد.</span><span class="sxs-lookup"><span data-stu-id="826b2-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="826b2-123">في الحقل **اللغة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="826b2-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="826b2-124">في الحقل **النص**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="826b2-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="826b2-125">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="826b2-125">Click **Save**.</span></span>
6. <span data-ttu-id="826b2-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="826b2-126">Close the page.</span></span>
7. <span data-ttu-id="826b2-127">في **جزء الإجراءات**، انقر فوق **أوصاف الوحدات المترجمة‬‬**.</span><span class="sxs-lookup"><span data-stu-id="826b2-127">On the **Action pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="826b2-128">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="826b2-128">Click **New**.</span></span> <span data-ttu-id="826b2-129">حدد أوصافًا خاصة باللغة لوحدة القياس.</span><span class="sxs-lookup"><span data-stu-id="826b2-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="826b2-130">في الحقل **اللغة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="826b2-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="826b2-131">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="826b2-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="826b2-132">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="826b2-132">Click **Save**.</span></span>
12. <span data-ttu-id="826b2-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="826b2-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="826b2-134">تعريف قواعد تحويل الوحدة</span><span class="sxs-lookup"><span data-stu-id="826b2-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="826b2-135">في **جزء الإجراءات**، انقر فوق **تحويلات الوحدات‬‬**.</span><span class="sxs-lookup"><span data-stu-id="826b2-135">On the **Action pane**, click **Unit conversions**.</span></span> <span data-ttu-id="826b2-136">قم بتعريف قواعد لتحويل وحدة القياس إلى وحدات قياس أخرى في فئة الوحدة المحددة ومنها.</span><span class="sxs-lookup"><span data-stu-id="826b2-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="826b2-137">انقر فوق **جديد**  لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="826b2-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="826b2-138">في الحقل **المعامل‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="826b2-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="826b2-139">معامل التحويل بين وحدة "من" ووحدة "إلى".</span><span class="sxs-lookup"><span data-stu-id="826b2-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="826b2-140">على سبيل المثال، عامل التحويل من السنتيمتر إلى المتر هو 100 نظرًا لوجود 100 سنتيمتر بالمتر الواحد.</span><span class="sxs-lookup"><span data-stu-id="826b2-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="826b2-141">في الحقل **إلى وحدة‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="826b2-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="826b2-142">في الحقل **التقريب‬**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="826b2-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="826b2-143">حدد كيفية تقريب القيمة المحوّلة.</span><span class="sxs-lookup"><span data-stu-id="826b2-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="826b2-144">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="826b2-144">Click **OK**.</span></span>
7. <span data-ttu-id="826b2-145">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="826b2-145">Close the page.</span></span>

