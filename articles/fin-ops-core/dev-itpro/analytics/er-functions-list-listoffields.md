---
title: LISTOFFIELDS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LISTOFFIELDS (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041988"
---
# <span data-ttu-id="c7dbc-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="c7dbc-103"><a name="LISTOFFIELDS">LISTOFFIELDS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7dbc-104">تُرجع الوظيفة `LISTOFFIELDS` قيمة *قائمة السجل* التي تم إنشاؤها بناءً على بنية الوسيطة المُحددة للنوع *التعداد* أو *الحاوية (السجل)*.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c7dbc-105">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="c7dbc-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="c7dbc-106">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="c7dbc-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="c7dbc-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="c7dbc-107">Arguments</span></span>

<span data-ttu-id="c7dbc-108">`path`: مرجع مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="c7dbc-108">`path`: Data source reference</span></span>

<span data-ttu-id="c7dbc-109">مسار مرجع صالح لمصدر بيانات أحد أنواع البيانات التالية:</span><span class="sxs-lookup"><span data-stu-id="c7dbc-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="c7dbc-110">تعداد النموذج</span><span class="sxs-lookup"><span data-stu-id="c7dbc-110">Model enumeration</span></span>
- <span data-ttu-id="c7dbc-111">تعداد التنسيق</span><span class="sxs-lookup"><span data-stu-id="c7dbc-111">Format enumeration</span></span>
- <span data-ttu-id="c7dbc-112">تعدادات التطبيق</span><span class="sxs-lookup"><span data-stu-id="c7dbc-112">Application enumeration</span></span>
- <span data-ttu-id="c7dbc-113">حاوية (سجل)</span><span class="sxs-lookup"><span data-stu-id="c7dbc-113">Container (record)</span></span>

<span data-ttu-id="c7dbc-114">`language`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="c7dbc-114">`language`: *String*</span></span>

<span data-ttu-id="c7dbc-115">النص الذي يمثل رمز لغة.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7dbc-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="c7dbc-116">Return values</span></span>

<span data-ttu-id="c7dbc-117">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="c7dbc-117">*Record list*</span></span>

<span data-ttu-id="c7dbc-118">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c7dbc-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="c7dbc-119">Usage notes</span></span>

<span data-ttu-id="c7dbc-120">تتكون القائمة التي تم إنشاؤها من السجلات التي تحتوي على الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="c7dbc-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="c7dbc-121">**الاسم** (نوع بيانات *السلسلة* )</span><span class="sxs-lookup"><span data-stu-id="c7dbc-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="c7dbc-122">**التسمية** (نوع بيانات *السلسلة* )</span><span class="sxs-lookup"><span data-stu-id="c7dbc-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="c7dbc-123">**الوصف** (نوع بيانات *السلسلة* )</span><span class="sxs-lookup"><span data-stu-id="c7dbc-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="c7dbc-124">**IsTranslated** (نوع البيانات *منطقي* )</span><span class="sxs-lookup"><span data-stu-id="c7dbc-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="c7dbc-125">إذا كانت الوسيطة `path` تشير إلى مصدر بيانات من النوع *الحاوية (سجل)* ، لكل حقل من سجل الحاوية المشار إليه، تتم إضافة سجل جديد إلى القائمة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="c7dbc-126">بالنسبة لكل سجل يتم إنشاؤه، يُرجع حقل **الاسم** اسم حقل سجل الحاوية المشار إليه الذي تم إنشاء السجل الحالي له.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="c7dbc-127">إذا كانت الوسيطة `path` تشير إلى مصدر بيانات واحد من أنواع  *التعداد*، لكل قيمة تعداد من التعداد المشار إليه، تتم إضافة سجل جديد إلى القائمة التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="c7dbc-128">بالنسبة لكل سجل تم إنشاؤه، يُرجع حقل **الاسم** قيمة التعداد المشار إليه الذي تم إنشاء السجل الحالي له، ويرجع حقل **الوصف** وصف التعداد، ويُرجع حقل **التسمية** تسمية هذا التعداد.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="c7dbc-129">في وقت التشغيل، عند استخدام بناء الجملة 1، يجب أن تُرجع الحقول **التسمية** و **الوصف** القيم التي تستند إلى إعدادات اللغة الخاصة بتنسيق التقارير الإلكترونية (ER) قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="c7dbc-130">إذا كانت التسميات والأوصاف الخاصة باللغة المطلوبة متوفرة، تُرجع الحقول **التسمية** و**الوصف** القيم التي تستند إلى تلك اللغة، ويُرجع حقل **IsTranslated** **True**.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="c7dbc-131">إذا لم تكن التسميات والأوصاف للغة المطلوبة متاحة، تُرجع حقول **التسمية** و**الوصف** القيم التي تستند إلى لغة **EN-US** الافتراضية، ويُرجع الحقل **IsTranslated** **False**.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="c7dbc-132">في وقت التشغيل، عند استخدام بناء الجملة 2، يجب أن تُرجع الحقول **التسمية** و **الوصف** القيم التي تستند إلى اللغة المُحددة كوسيطة ثانية للوظيفة التي تم استدعاءها.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="c7dbc-133">إذا كانت التسميات والأوصاف الخاصة باللغة المطلوبة متوفرة، تُرجع الحقول **التسمية** و**الوصف** القيم التي تستند إلى تلك اللغة، ويُرجع حقل **IsTranslated** **True**.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="c7dbc-134">إذا لم تكن التسميات والأوصاف للغة المطلوبة متاحة، تُرجع حقول **التسمية** و**الوصف** القيم التي تستند إلى لغة **EN-US** ، ويُرجع الحقل **IsTranslated** **False**.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="c7dbc-135">مثال1</span><span class="sxs-lookup"><span data-stu-id="c7dbc-135">Example 1</span></span>

<span data-ttu-id="c7dbc-136">في الرسم التوضيحي التالي، يتم تقديم تعداد في نموذج بيانات التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="c7dbc-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="c7dbc-137">يبين الرسم التوضيحي التالي هذه التفاصيل:</span><span class="sxs-lookup"><span data-stu-id="c7dbc-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="c7dbc-138">يتم إدراج تعداد النموذج في تقرير كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="c7dbc-139">يستخدم تعبير التقارير الإلكترونية تعداد النموذج كمعلمة لوظيفة `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="c7dbc-140">يتم إدراج مصدر بيانات نوع *قائمة السجلات* في تقرير باستخدام تعبير التقارير الإلكترونية الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="c7dbc-141">يوضح المثال التالي عناصر تنسيق التقارير الإلكترونية المرتبطة بمصدر البيانات من نوع *قائمة السجلات* الذي تم إنشاؤها باستخدام وظيفة `LISTOFFIELDS`.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="c7dbc-142">يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="c7dbc-143">تتم تعبئة النص المترجم للتسميات والأوصاف في إخراج تنسيق التقارير الإلكترونية وفقًا لإعدادات اللغة التي تم تكوينها لعناصر تنسيق **الملف** و**المجلد** الأصلي.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="c7dbc-144">مثال2</span><span class="sxs-lookup"><span data-stu-id="c7dbc-144">Example 2</span></span>

<span data-ttu-id="c7dbc-145">سوف تستخدم نوع مصدر البيانات *الحقل المحسوب* لتكوين مصادر البيانات **enumType\_de** و **enumType\_ deCH** لتعداد نموذج بيانات **enumType**: </span><span class="sxs-lookup"><span data-stu-id="c7dbc-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="c7dbc-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="c7dbc-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="c7dbc-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="c7dbc-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="c7dbc-148">في هذه الحالة، يمكنك استخدام التعبير التالي للحصول على تسمية لقيمة التعداد بالألمانية السويسرية، في حالة توفر الترجمة.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="c7dbc-149">إذا لم تتوفر ترجمة اللغة الألمانية (سويسرا)، فستكون التسمية باللغة الألمانية.</span><span class="sxs-lookup"><span data-stu-id="c7dbc-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="c7dbc-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c7dbc-150">Additional resources</span></span>

[<span data-ttu-id="c7dbc-151">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="c7dbc-151">List functions</span></span>](er-functions-category-list.md)
