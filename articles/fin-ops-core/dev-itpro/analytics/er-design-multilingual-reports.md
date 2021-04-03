---
title: تصميم تقارير متعددة اللغات في التقارير الإلكترونية
description: يشرح هذا الموضوع كيف يمكنك استخدام تسميات التقارير الإلكترونية (ER) لتصميم تقارير متعددة اللغات وإنشاءها.
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e765b450f626abb3dee4a70419176568eeb62d7e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562060"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a><span data-ttu-id="d8910-103">تصميم تقارير متعددة اللغات في التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d8910-103">Design multilingual reports in Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="d8910-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d8910-104">Overview</span></span>

<span data-ttu-id="d8910-105">بصفتك مستخدم شركة، يمكنك استخدام إطار العمل [التقارير الإلكترونية (ER)](general-electronic-reporting.md) لتكوين تنسيقات المستندات الصادرة التي يجب إنشائها وفقًا للمتطلبات القانونية لمختلف البلدان أو المناطق.</span><span class="sxs-lookup"><span data-stu-id="d8910-105">As a business user, you can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to configure formats for outbound documents that must be generated in accordance with the legal requirements of various countries or regions.</span></span> <span data-ttu-id="d8910-106">وعندما تطلب هذه المتطلبات إنشاء المستندات الصادرة بلغات مختلفة لبلدان أو مناطق مختلفة، فإنه يمكنك تكوين [تنسيق ER](general-electronic-reporting.md#FormatComponentOutbound) واحد يحتوي على موارد حسب اللغة.</span><span class="sxs-lookup"><span data-stu-id="d8910-106">When these requirements demand that outbound documents be generated in different languages for different countries or regions, you can configure a single ER [format](general-electronic-reporting.md#FormatComponentOutbound) that contains language-dependent resources.</span></span> <span data-ttu-id="d8910-107">وبهذه الطريقة، يمكنك إعادة استخدام التنسيق لإنشاء مستندات صادرة لبلدان أو مناطق مختلفة.</span><span class="sxs-lookup"><span data-stu-id="d8910-107">In that way, you can reuse the format to generate outbound documents for various countries or regions.</span></span> <span data-ttu-id="d8910-108">قد تحتاج أيضًا إلى استخدام تنسيق ER واحد لإنشاء مستند صادر بلغات مختلفة للعملاء المقابلين أو الموردين أو الشركات التابعة أو أية أطراف أخرى.</span><span class="sxs-lookup"><span data-stu-id="d8910-108">You might also want to use a single ER format to generate an outbound document in different languages for corresponding customers, vendors, subsidiaries, or any other parties.</span></span>

<span data-ttu-id="d8910-109">يمكنك تكوين نماذج البيانات الخاصة بـ ER وتعيينات النماذج كمصادر البيانات لتنسيقات ER المكونة لتحديد تدفق البيانات الذي يحدد البيانات التطبيق التي يتم وضعها في المستندات المنشاة.</span><span class="sxs-lookup"><span data-stu-id="d8910-109">You can configure ER data models and model mappings as the data sources of configured ER formats to define the data flow that specifies what application data is put into generated documents.</span></span> <span data-ttu-id="d8910-110">باعتبارك موفر [تكوين  ER](general-electronic-reporting.md#Provider)، فإنه يمكنك  [نشر](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) [نماذج البيانات](general-electronic-reporting.md#data-model-and-model-mapping-components) و [تعيينات النماذج](general-electronic-reporting.md#data-model-and-model-mapping-components) و  [التنسيقات](general-electronic-reporting.md#FormatComponentOutbound) المكونة كمكونات لحل ER لإنشاء مستندات صادرة معينة.</span><span class="sxs-lookup"><span data-stu-id="d8910-110">As an ER configuration [provider](general-electronic-reporting.md#Provider), you can [publish](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) configured [data models](general-electronic-reporting.md#data-model-and-model-mapping-components), [model mappings](general-electronic-reporting.md#data-model-and-model-mapping-components), and [formats](general-electronic-reporting.md#FormatComponentOutbound) as components of an ER solution to generate specific outbound documents.</span></span> <span data-ttu-id="d8910-111">يمكنك أيضًا السماح للعملاء [بتحميل](general-electronic-reporting-manage-configuration-lifecycle.md) الحل المنشور الخاص بـ ER بحيث يمكن استخدامه وتخصيصه.</span><span class="sxs-lookup"><span data-stu-id="d8910-111">You can also allow customers to [upload](general-electronic-reporting-manage-configuration-lifecycle.md) the published ER solution so that it can be used and customized.</span></span> <span data-ttu-id="d8910-112">إذا كنت تتوقع أن العملاء قد يتحدثون بلغات أخرى، فإنه يمكنك تكوين مكونات ER بحيث تحتوي علي موارد معتمدة على اللغة.</span><span class="sxs-lookup"><span data-stu-id="d8910-112">If you expect that customers might speak other languages, you can configure the ER components so that they contain language-dependent resources.</span></span> <span data-ttu-id="d8910-113">وبهذه الطريقة، يمكن تقديم محتوى مكون ER القابل للتحرير بلغة المستخدم المفضلة للعميل في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="d8910-113">In that way, the content of an editable ER component can be presented in a customer's user-preferred language at design time.</span></span>

<span data-ttu-id="d8910-114">يمكنك تكوين موارد تعتمد على اللغة باسم تسميات ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-114">You can configure language-dependent resources as ER labels.</span></span> <span data-ttu-id="d8910-115">ثم يمكنك استخدام تلك التسميات لتكوين مكونات ER للأغراض التالية:</span><span class="sxs-lookup"><span data-stu-id="d8910-115">You can then use those labels to configure ER components for the following purposes:</span></span>

- <span data-ttu-id="d8910-116">في وقت التصميم:</span><span class="sxs-lookup"><span data-stu-id="d8910-116">At design time:</span></span>

    - <span data-ttu-id="d8910-117">تقديم محتوى مكونات ER التي تم تكوينها باللغة المفضلة للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-117">Present the content of configured ER components in the user-preferred language.</span></span>

- <span data-ttu-id="d8910-118">في وقت التشغيل:</span><span class="sxs-lookup"><span data-stu-id="d8910-118">At runtime:</span></span>

    - <span data-ttu-id="d8910-119">قم بإنشاء محتوى يعتمد على اللغة للمستندات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="d8910-119">Generate language-dependent content for outbound documents.</span></span>
    - <span data-ttu-id="d8910-120">قم بتوفير رسائل تحذير ورسائل خطأ باللغة المفضلة للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-120">Provide warning and error messages in the user-preferred language.</span></span>
    - <span data-ttu-id="d8910-121">طالب بالحقول المطلوبة باللغة المفضلة للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-121">Prompt for required fields in the user-preferred language.</span></span>

<span data-ttu-id="d8910-122">يمكن تكوين تسميات ER في كل [تكوين ER](general-electronic-reporting.md#Configuration) يحتوي على مكونات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="d8910-122">ER labels can be configured in every ER [configuration](general-electronic-reporting.md#Configuration) that contains different components.</span></span> <span data-ttu-id="d8910-123">يمكن الاحتفاظ بالتسميات بشكل مستقل عن المنطق المكون لنماذج بيانات ER وتعيينات نموذج ER ومكونات التنسيق الخاصة بنموذج ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-123">The labels can be maintained independently of the configured logic of ER data models, ER model mappings, and ER format components.</span></span>

<span data-ttu-id="d8910-124">يتم تعريف كل تسمية ER بواسطة معرف فريد في نطاق تكوين ER الذي يحتفظ بتلك التسمية.</span><span class="sxs-lookup"><span data-stu-id="d8910-124">Every ER label is identified by an ID that is unique in the scope of the ER configuration that holds that label.</span></span> <span data-ttu-id="d8910-125">يمكن أن تحتوي كل تسمية على نص تسمية لكل لغة معتمدة في المثيل الحالي لـ Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d8910-125">Every label can contain label text for every language that is supported in the current instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="d8910-126">تتضمن هذه اللغات المعتمدة لغات التخصيصات المنشورة.</span><span class="sxs-lookup"><span data-stu-id="d8910-126">These supported languages include the languages of deployed customizations.</span></span>

## <a name="entry"></a><span data-ttu-id="d8910-127">الإدخال</span><span class="sxs-lookup"><span data-stu-id="d8910-127">Entry</span></span>

<span data-ttu-id="d8910-128">عند تصميم نموذج بيانات ER أو تعيين نموذج ER أو تنسيق ER، فإنه يتم عرض الخيار **ترجمة** كلما حددت حقلاً قد يحتوي على السياق القابل للترجمة.</span><span class="sxs-lookup"><span data-stu-id="d8910-128">When you design an ER data model, an ER model mapping, or an ER format, the **Translate** option is shown whenever you select a field that might contain the translatable context.</span></span> <span data-ttu-id="d8910-129">عند تحديد هذا الخيار، فإنه يمكنك ربط الحقل المحدد بتسمية ER في **جزء** <a name="TextTranslationPane">ترجمة النص</a>.</span><span class="sxs-lookup"><span data-stu-id="d8910-129">When you select this option, you can link the selected field to an ER label on the **Text translation** <a name="TextTranslationPane">pane</a>.</span></span> <span data-ttu-id="d8910-130">يمكنك تحديد تسمية ER موجودة أو يمكنك إضافة تسمية ER جديدة إذا لم تكن متوفرة حتى الآن.</span><span class="sxs-lookup"><span data-stu-id="d8910-130">You can select an existing ER label, or you can add a new ER label if it isn't available yet.</span></span> <span data-ttu-id="d8910-131">عند تحديد أو إضافة تسمية ER، فإنه يمكنك إضافة نص مرتبط إلى كل لغة مدعومة في مثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="d8910-131">When you select or add an ER label, you can add related text for every language that is supported in the current Finance instance.</span></span>

<span data-ttu-id="d8910-132">يبين الرسم التوضيحي التالي كيفية إجراء هذه الترجمة في نموذج بيانات ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-132">The following illustration shows how this translation is done in an editable ER data model.</span></span> <span data-ttu-id="d8910-133">في هذا المثال، تتم ترجمة سمة **الوصف** للحقل **PurchaseOrder** القابل للتحرير **لنموذج الفاتورة** القابل للتحرير باللغة الألمانية في النمسا (DE-AT) واليابانية (JA).</span><span class="sxs-lookup"><span data-stu-id="d8910-133">In this example, the **Description** attribute of the **PurchaseOrder** field for the editable **Invoice model** is translated into the Austrian German (DE-AT) and Japanese (JA) languages.</span></span>

![توفير ترجمة لتسمية ER في مصمم نموذج بيانات ER](./media/er-multilingual-labels-refer.png)

<span data-ttu-id="d8910-135">يمكن ترجمة نص التسمية فقط للتسميات الموجودة في مكون ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-135">Only label text for labels that reside in an editable ER component can be translated.</span></span> <span data-ttu-id="d8910-136">على سبيل المثال، إذا قمت بتحديد **ترجمة** لسمة التسمية لمصدر بيانات تعيين نموذج ER، ثم بعد ذلك قمت بتحديد تسمية ER الموجودة في نموذج بيانات ER الأصلي، ستشاهد محتوى التسمية ولكن لا يمكنك تغييره.</span><span class="sxs-lookup"><span data-stu-id="d8910-136">For example, if you select **Translate** for the label attribute of an ER model mapping data source, and you then select an ER label that resides in the parent ER data model, you will see the content of the label, but you can't change it.</span></span> <span data-ttu-id="d8910-137">في هذه الحالات، لا يتوفر الحقل **النص المترجم**، كما هو مبين في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="d8910-137">In these cases, the **Translated text** field is unavailable, as shown in the following illustration.</span></span>

![مراجعة الترجمة المقدمة لتسمية ER في مصمم تعيين نموذج بيانات ER](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> <span data-ttu-id="d8910-139">يتعذر عليك استخدام المصممين لحذف التسمية التي تم إدخالها في أحد مكونات ER القابلة للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-139">You can't use the designers to delete label that has been entered in an editable ER component.</span></span>

## <a name="scope"></a><span data-ttu-id="d8910-140">النطاق</span><span class="sxs-lookup"><span data-stu-id="d8910-140">Scope</span></span>

<span data-ttu-id="d8910-141">يمكن الإشارة إلى تسميات ER في العديد من السمات القابلة للترجمة الخاصة بمكونات ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-141">ER labels can be referred to in several translatable attributes of ER components.</span></span>

### <a name="data-model-component"></a><span data-ttu-id="d8910-142">مكون نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="d8910-142">Data model component</span></span>

<span data-ttu-id="d8910-143">عند تكوين نموذج بيانات ER، فإنه يمكنك إضافة تسميات ER إليه.</span><span class="sxs-lookup"><span data-stu-id="d8910-143">When you configure an ER data model, you can add ER labels for it.</span></span> <span data-ttu-id="d8910-144">يمكن ربط السمتين **التسمية** و **الوصف** لعنصر النموذج وكل حقل نموذج وكل <a id="LinkModelEnum"></a>قيمة تعداد النموذج بتسمية ER تتم إضافتها إلى نموذج بيانات ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-144">**Label** and **Description** attributes of the model item, every model's field, and every <a id="LinkModelEnum"></a>model enumeration value can be linked to an ER label that is added to the ER data model.</span></span>

![توفير ترجمة لسمة الوصف في مصمم نموذج بيانات ER](./media/er-multilingual-labels-refer.png)

<span data-ttu-id="d8910-146">عند تكوين نموذج بيانات ER بهذه الطريقة، فإنه يتم تقديم المحتوى الخاص به إلى مستخدمي مصمم نموذج بيانات ER باللغة المفضلة لكل مستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-146">When an ER data model is configured in this way, its content will be presented to users of the ER data model designer in each user's preferred language.</span></span> <span data-ttu-id="d8910-147">وبالتالي، يتم تبسيط صيانة النموذج.</span><span class="sxs-lookup"><span data-stu-id="d8910-147">Therefore, model maintenance is simplified.</span></span> <span data-ttu-id="d8910-148">تظهر الرسوم التوضيحية التالية كيفية عمل هذه الوظيفة للمستخدمين الذين يقومون بتعيين اللغتين الألمانية (النمسا) واليابانية كلغة مفضلة لهم.</span><span class="sxs-lookup"><span data-stu-id="d8910-148">The following illustrations show how this functionality works for users who have DE-AT and JA set as their preferred language.</span></span>

![تخطيط مصمم نموذج بيانات التقارير الإلكترونية لمستخدم قام بتعيين الألمانية (النمسا) باعتبارها اللغة المفضلة](./media/er-multilingual-labels-refer-de.png)

![تخطيط مصمم نموذج بيانات ER لمستخدم قام بتعيين اليابانية باعتبارها اللغة المفضلة](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a><span data-ttu-id="d8910-151">مكون تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="d8910-151">Model mapping component</span></span>

<span data-ttu-id="d8910-152">نظرًا لأن تعيين نموذج ER يستند إلى نموذج بيانات ER، تظهر تسميات عناصر نموذج البيانات التي يتم الرجوع إليها باللغة المفضلة للمستخدم في مصمم تعيين النموذج.</span><span class="sxs-lookup"><span data-stu-id="d8910-152">Because the ER model mapping is based on an ER data model, the labels of the data model elements that are referred to are appeared in the user's preferred language in the model mapping designer.</span></span> <span data-ttu-id="d8910-153">يبين الرسم التوضيحي التالي كيفية شرح معنى الحقل **PurchaseOrder** في تعيين النموذج القابل للتحرير باستخدام تسمية السمة **الوصف** التي تمت إضافتها إلى نموذج البيانات المكون.</span><span class="sxs-lookup"><span data-stu-id="d8910-153">The following illustration shows how the meaning of the **PurchaseOrder** field is explained in the editable model mapping by using the label of the **Description** attribute that has been added to the configured data model.</span></span> <span data-ttu-id="d8910-154">لاحظ أنه تم تقديم هذه التسمية باللغة المفضلة للمستخدم (الألمانية (النمسا) في هذا المثال).</span><span class="sxs-lookup"><span data-stu-id="d8910-154">Notice that this label is presented in the user's preferred language (DE-AT in this example).</span></span>

![تخطيط مصمم تعيين نموذج بيانات ER لمستخدم قام بتعيين الألمانية (النمسا) باعتبارها اللغة المفضلة](./media/er-multilingual-labels-show-mapping.png)

<span data-ttu-id="d8910-156">عندما يتم تكوين السمة **التسمية** لمصدر البيانات **معلمات إدخال المستخدم** على أنها مرتبطة بالتسمية ER، فإنه يتم تقديم حقل المعلمة الذي يتطابق مع مصدر البيانات هذا في مربع حوار المستخدم في وقت التشغيل إلى المستخدمين باللغة المفضلة.</span><span class="sxs-lookup"><span data-stu-id="d8910-156">When the **Label** attribute of the **User input parameter** data source is configured as linked to an ER label, the parameter field that corresponds to this data source is presented in the user dialog box at runtime to users in their preferred language.</span></span>

### <a name="format-component"></a><span data-ttu-id="d8910-157">مكون التنسيق</span><span class="sxs-lookup"><span data-stu-id="d8910-157">Format component</span></span>

<span data-ttu-id="d8910-158">عند تكوين تنسيق ER، فإنه يمكنك إضافة تسميات ER إليه.</span><span class="sxs-lookup"><span data-stu-id="d8910-158">When you configure an ER format, you can add ER labels for it.</span></span> <span data-ttu-id="d8910-159">يمكن ربط السمتين **التسمية** و **نص التعليمات** لكل مصدر بيانات تم تكوينه بتسمية ER تتم إضافته إلى التنسيق إلى ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-159">The **Label** and **Help text** attributes of every configured data source can be linked to an ER label that is added to the ER format.</span></span> <span data-ttu-id="d8910-160">كذلك، يمكن ربط السمتين **التسمية** و **الوصف** لكل قيمة تعداد التنسيق <a id="LinkFormatEnum"></a>بالتسمية ER التي يمكن الوصول إليها من التنسيق ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-160">The **Label** and **Description** attributes of every <a id="LinkFormatEnum"></a>format enumeration value can be also linked to an ER label that is accessible from the editable ER format.</span></span>

> [!NOTE]
> <span data-ttu-id="d8910-161">يمكنك أيضًا ربط هذه السمات بتسمية ER نموذج بيانات ER الاصلي بحيث يتم إعادة استخدام تسميات النموذج في كل تنسيق ER يتم تكوينه لنموذج بيانات ER هذا.</span><span class="sxs-lookup"><span data-stu-id="d8910-161">You can also link these attributes to an ER label of the parent ER data model that reuses the model's labels in every ER format that is configured for this ER data model.</span></span>

<span data-ttu-id="d8910-162">عند تكوين تنسيق ER بهذه الطريقة، فإنه يتم تقديم محتوى التنسيق إلى مستخدمي مصمم عملية ER باللغة المفضلة لكل مستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-162">When an ER format is configured in this way, the content of the format will be presented to users of the ER Operation designer in each user's preferred language.</span></span> <span data-ttu-id="d8910-163">وبالتالي، يتم تبسيط صيانة التنسيق وتحليل المنطق المكون.</span><span class="sxs-lookup"><span data-stu-id="d8910-163">Therefore, format maintenance and analysis of the configured logic are simplified.</span></span>

<span data-ttu-id="d8910-164">نظرًا لأن تنسيق ER يستند إلى نموذج بيانات ER، يتم تقديم التسميات التي يتم الرجوع إليها في عناصر نموذج البيانات في مصمم تنسيق ER باللغة المفضلة للمستخدم .</span><span class="sxs-lookup"><span data-stu-id="d8910-164">Because an ER format is based on an ER data model, the labels that are referred to in the data model elements are presented in the ER format designer in the user-preferred language.</span></span>

<span data-ttu-id="d8910-165">عندما يتم ربط السمة **التسمية** لمصدر البيانات **معلمات إدخال المستخدم** بتسمية ER، فإنه يتم تقديم الحقل الذي يتطابق مع المعلمة في مربع حوار المستخدم في وقت التشغيل إلى المستخدم كما هو مطالب.</span><span class="sxs-lookup"><span data-stu-id="d8910-165">When the **Label** attribute of the **User input parameter** data source is linked to an ER label, the field that corresponds to the parameter in the user dialog box at runtime is presented to the user as a prompt.</span></span> <span data-ttu-id="d8910-166">تظهر الرسوم التوضيحية التالية كيف يمكنك ربط السمة **تسمية** لمصدر البيانات **معلمة إدخال المستخدم** في وقت التصميم بتسمية ER، بحيث تتم مطالبة المستخدمين بالمعلمة بلغات مختلفة مفضلة للمستخدم (موضحة باللغة الإنجليزية "الولايات المتحدة" واللغة الألمانية "النمسا") في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d8910-166">The following illustrations show how you can link the **Label** attribute of the **User input parameter** data source at design time to an ER label, so that users are prompted for the parameter in different user-preferred languages (shown for English United States (EN-US) and DE-AT languages) at runtime.</span></span>

![توفير ترجمة سمات معلمة إدخال المستخدم في مصمم عمليات ER](./media/er-multilingual-labels-refer-format.png)

![معالجة دفع مورد ER في وقت التشغيل للغة الإنجليزية -الولايات المتحدة المفضلة للمستخدم](./media/er-multilingual-labels-show-runtime-en.png)

![معالجة دفع مورد ER في وقت التشغيل للغة الألمانية -النمسا المفضلة للمستخدم](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a><span data-ttu-id="d8910-170">تعبيرات</span><span class="sxs-lookup"><span data-stu-id="d8910-170">Expressions</span></span>

<span data-ttu-id="d8910-171">لاستخدام التسمية في [تعبير](er-formula-language.md) ER، فإنه يجب عليك استخدام بناء الجملة **@"GER\_LABEL:X"**، حيث تشير البادئة **@** إلى أن المعامل يرجع إلى تسمية، وتشير **GER\_LABEL** إلى أنه يتم تضمين تسمية ER، وأن  **X** هو معرف تسمية ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-171">To use a label in an ER [expression](er-formula-language.md), you must use the syntax **@"GER\_LABEL:X"**, where the prefix **@** indicates that the operand refers to a label, **GER\_LABEL** indicates that an ER label is involved, and **X** is the ER label ID.</span></span>

![تكوين تعبير ER يحتوي على مرجع إلى تسمية ER في مصمم صيغة ER](./media/er-multilingual-labels-expression1.png)

<span data-ttu-id="d8910-173">للإشارة إلى تسمية نظام (تطبيق)، استخدم بناء الجملة **@"X"**، حيث تشير البادئة **@** إلى أن العامل يشير إلى تسمية و **X** هو معرف تسمية النظام.</span><span class="sxs-lookup"><span data-stu-id="d8910-173">To refer to a system (application) label, use the syntax **@"X"**, where the prefix **@** indicates that the operand refers to a label, and **X** is the system label ID.</span></span>

![تكوين تعبير ER يحتوي على مرجع إلى تسمية التطبيق في مصمم صيغة ER](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a><span data-ttu-id="d8910-175">تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="d8910-175">Model mapping</span></span>

<span data-ttu-id="d8910-176">يمكن تكوين تعبير لتعيين نموذج ER باستخدام تسمية.</span><span class="sxs-lookup"><span data-stu-id="d8910-176">An expression of an ER model mapping can be configured by using a label.</span></span> <span data-ttu-id="d8910-177">عند استدعاء هذا التعيين بواسطة تنسيق ER الذي يتم تشغيله لإنشاء مستند صادر، يتضمن سياق التنفيذ رمز لغة.</span><span class="sxs-lookup"><span data-stu-id="d8910-177">When this mapping is called by an ER format that is run to generate an outbound document, the context of the execution includes a language code.</span></span> <span data-ttu-id="d8910-178">سيتم ملء تسمية التعبير المكون بنص التسمية الذي تم تكوينه للغة الخاصة بذلك السياق.</span><span class="sxs-lookup"><span data-stu-id="d8910-178">A configured expression label will be filled in with the label text that has been configured for the language of that context.</span></span>

<span data-ttu-id="d8910-179">إذا لم تكن للتسمية المشار إليها ترجمة للغة سياق تنفيذ التنسيق الذي يستدعي تعيين النموذج، فإنه يتم استخدام نص التسمية باللغة الإنجليزية - الولايات المتحدة بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="d8910-179">If a referenced label has no translation for the language of the format execution context that calls the model mapping, the label text in the EN-US language is used instead.</span></span>

#### <a name="format"></a><span data-ttu-id="d8910-180">التنسيق</span><span class="sxs-lookup"><span data-stu-id="d8910-180">Format</span></span>

<span data-ttu-id="d8910-181">يمكن تكوين تعبير ER لتنسيق ER باستخدام تسميات.</span><span class="sxs-lookup"><span data-stu-id="d8910-181">An ER expression of an ER format can be configured by using labels.</span></span> <span data-ttu-id="d8910-182">عند تشغيل هذا التنسيق لإنشاء مستند صادر، يتضمن سياق التنفيذ رمز لغة.</span><span class="sxs-lookup"><span data-stu-id="d8910-182">When this format is run to generate an outbound document, the context of the execution includes a language code.</span></span> <span data-ttu-id="d8910-183">سيتم ملء تسمية التعبير المكون بنص التسمية الذي تم تكوينه للغة الخاصة بذلك السياق.</span><span class="sxs-lookup"><span data-stu-id="d8910-183">A configured expression label will be filled in with the label text that has been configured for the language of that context.</span></span>

![توفير ترجمة لتسمية ER الخاصة بتعبير ER القابل للتحرير في مصمم معادلة ER](./media/er-multilingual-labels-refer-in-expression.png)

![عينة من ربط البيانات التي تشير إلى تسمية ER في مصمم عملية ER](./media/er-multilingual-labels-refer-in-binding.png)

<span data-ttu-id="d8910-186">يمكنك تكوين المكون **FILE** لتنسيق ER لإنشاء التقرير باللغة المفضلة للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-186">You can configure the **FILE** component of an ER format to generate the report in the user's preferred language.</span></span>

![إعداد المكون FILE في مصمم عملية ER لإنشاء التقرير باللغة المفضلة للمستخدم](./media/er-multilingual-labels-language-context-user.png)

<span data-ttu-id="d8910-188">إذا قمت بتكوين تنسيق ER بهذه الطريقة، فإنه يتم إنشاء التقرير باستخدام النص المطابق لتسميات ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-188">If you configure an ER format in this way, the report is generated by using the corresponding text of the ER labels.</span></span> <span data-ttu-id="d8910-189">تظهر الرسوم التوضيحية التالية أمثلة على التقارير الخاصة بلغتي المستخدم الإنجليزية - الولايات المتحدة والألمانية - النمسا.</span><span class="sxs-lookup"><span data-stu-id="d8910-189">The following illustrations show examples of reports for the EN-US and DE-AT user languages.</span></span>

![معاينة التقرير الذي تم إنشاؤه باللغة المفضلة للمستخدم الإنجليزية - الولايات المتحدة](./media/er-multilingual-labels-report-preview-en.png)

![معاينة التقرير الذي تم إنشاؤه باللغة المفضلة للمستخدم الألمانية - النمسا](./media/er-multilingual-labels-report-preview-de.png)

<span data-ttu-id="d8910-192">إذا لم تكن للتسمية المشار إليها ترجمة للغة سياق تنفيذ التنسيق، فإنه يتم استخدام نص التسمية باللغة الإنجليزية - الولايات المتحدة بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="d8910-192">If a referenced label has no translation for the language of the format execution context, the label text in the EN-US language is used instead.</span></span>

## <a name="language"></a><span data-ttu-id="d8910-193">اللغة</span><span class="sxs-lookup"><span data-stu-id="d8910-193">Language</span></span>

<span data-ttu-id="d8910-194">يدعم ER طرقًا مختلفة لتحديد لغة لتقرير تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="d8910-194">ER supports different ways to specify a language for a generated report.</span></span> <span data-ttu-id="d8910-195">في الحقل **تفضيلات اللغة** في علامة التبويب **التنسيق**، فإنه يمكنك تحديد القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="d8910-195">In the **Language preferences** field on the **Format** tab, you can select the following values:</span></span>

- <span data-ttu-id="d8910-196">**تفضيل الشركة** – إنشاء تقرير باللغة التي تحددها شركة.</span><span class="sxs-lookup"><span data-stu-id="d8910-196">**Company preference** – Generate a report in a company-specified language.</span></span>

    ![تحديد في مصمم عمليات ER اللغة المفضلة للشركة كلغة التقرير الذي تم إنشاؤه](./media/er-multilingual-labels-language-context-company.png)

- <span data-ttu-id="d8910-198">**تفضيل المستخدم** – إنشاء تقرير باللغة المفضلة للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-198">**User preference** – Generate a report in the user's preferred language.</span></span>
- <span data-ttu-id="d8910-199">**معرف بشكل صريح** – قم بإنشاء تقرير باللغة التي يتم تحديدها في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="d8910-199">**Explicitly defined** – Generate a report in a language that is specified at design time.</span></span>

    ![تحديد في مصمم عمليات ER اللغة محددة وقت التصميم كلغة التقرير الذي تم إنشاؤه](./media/er-multilingual-labels-language-context-fixed.png)

- <span data-ttu-id="d8910-201">**محدد في وقت التشغيل** – قم بإنشاء تقرير باللغة التي يتم تحديدها في وقت التشغيل.</span><span class="sxs-lookup"><span data-stu-id="d8910-201">**Defined at run-time** – Generate a report in a language that is specified at runtime.</span></span> <span data-ttu-id="d8910-202">إذا قمت بتحديد هذه القيمة، في الحقل **اللغة**، قم بتكوين تعبير ER يقوم بإرجاع كود اللغة للغة، مثل لغة العميل المطابق.</span><span class="sxs-lookup"><span data-stu-id="d8910-202">If you select this value, in the **Language** field, configure an ER expression that returns the language code for the language, such as the language of the corresponding customer.</span></span>

    ![تحديد في مصمم عمليات ER اللغة محددة وقت التشغيل كلغة التقرير الذي تم إنشاؤه](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="translation"></a><span data-ttu-id="d8910-204">الترجمة</span><span class="sxs-lookup"><span data-stu-id="d8910-204">Translation</span></span>

<span data-ttu-id="d8910-205">يمكنك إضافة تسميات ER المطلوبة إلى مكون ER قابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-205">You can add required ER labels to an editable ER component.</span></span> <span data-ttu-id="d8910-206">عند إضافة تسمية ER، يمكن ترجمتها بطريقتين: يدويًا وتلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="d8910-206">When an ER label is added, it can be translated in two ways: manually and automatically.</span></span>

### <a name="manual-translation"></a><span data-ttu-id="d8910-207">ترجمة يدوية</span><span class="sxs-lookup"><span data-stu-id="d8910-207">Manual translation</span></span>

<span data-ttu-id="d8910-208">عند إضافة تسمية ER في **الجزء** [ترجمة النص](#TextTranslationPane)، فإنه يمكنك ترجمتها يدويًا إلى كافة اللغات التي يتم دعمها في المثيل المالي الحالي.</span><span class="sxs-lookup"><span data-stu-id="d8910-208">When you add an ER label on the **Text translation** [pane](#TextTranslationPane), you can manually translate it into all languages that are supported in the current Finance instance.</span></span> <span data-ttu-id="d8910-209">يمكنك تحديد اللغة المفضلة في الحقل **اللغة** في القسم **لغة النظام** أو **لغة المستخدم**، أدخل النص المناسب في الحقل **النص المترجم**، ثم قم بتحديد **ترجمة**</span><span class="sxs-lookup"><span data-stu-id="d8910-209">You can select the preferred language in the **Language** field in the **System language** or **User language** section, enter the appropriate text in the corresponding **Translated text** field, and then select **Translate**.</span></span> <span data-ttu-id="d8910-210">يجب تكرار هذه العملية لكل لغة مطلوبة وكل تسمية تقوم بإضافتها.</span><span class="sxs-lookup"><span data-stu-id="d8910-210">This process must be repeated for every required language and every label that you add.</span></span>

### <a name="automatic-translation"></a><span data-ttu-id="d8910-211">ترجمة تلقائية</span><span class="sxs-lookup"><span data-stu-id="d8910-211">Automatic translation</span></span>

<span data-ttu-id="d8910-212">يتم إجراء تكوين مكون ER في إصدار المسودة الخاص بتكوين ER الذي يقع فيه مكون ER القابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-212">Configuration of an ER component is done in the draft version of the ER configuration that the editable ER component resides in.</span></span>

![صفحة تكوينات ER التي تقدم الوصول إلى إصدار التكوين في حالة المسودة](./media/er-multilingual-labels-configurations.png)

<span data-ttu-id="d8910-214">كما هو موضح سابقًا في هذا الموضوع، يمكنك إضافة تسميات ER المطلوبة إلى مكون ER قابل للتحرير.</span><span class="sxs-lookup"><span data-stu-id="d8910-214">As described earlier in this topic, you can add required ER labels to an editable ER component.</span></span> <span data-ttu-id="d8910-215">وبهذه الطريقة، يمكنك تحديد نص تسميات ER باللغة الإنجليزية - الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="d8910-215">In this way, you can specify the text of the ER labels in the EN-US language.</span></span> <span data-ttu-id="d8910-216">ثم يمكنك تصدير تسميات مكون ER باستخدام وظيفة ER المضمنة.</span><span class="sxs-lookup"><span data-stu-id="d8910-216">You can then export the labels of the ER component by using the built-in ER function.</span></span> <span data-ttu-id="d8910-217">حدد إصدار المسودة لتكوين ER الذي يحتوي على مكونات ER القابلة للتحرير، ثم حدد **تبادل \> تصدير التسميات**.</span><span class="sxs-lookup"><span data-stu-id="d8910-217">Select the draft version of an ER configuration that contains the editable ER component, and then select **Exchange \> Export labels**.</span></span>

![صفحة تكوينات ER مما يسمح بتصدير تسميات ER من إصدار التكوين المحدد](./media/er-multilingual-labels-export.png)

<span data-ttu-id="d8910-219">يمكنك تصدير إما كافة التسميات أو التسميات للغة واحدة قمت بتحديدها في بداية التصدير.</span><span class="sxs-lookup"><span data-stu-id="d8910-219">You can export either all labels or the labels for a single language that you specify at the beginning of export.</span></span> <span data-ttu-id="d8910-220">يتم تصدير التسميات كملف مضغوط يحتوي على ملفات XML.</span><span class="sxs-lookup"><span data-stu-id="d8910-220">Labels are exported as a zip file that contains XML files.</span></span> <span data-ttu-id="d8910-221">يحتوي كل ملف XML على تسميات للغة واحدة.</span><span class="sxs-lookup"><span data-stu-id="d8910-221">Every XML file contains labels for a single language.</span></span>

![عينة من الملف المصدر الذي يحتوي على تسميات ER للغة الألمانية - النمسا](./media/er-multilingual-labels-in-xml.png)

<span data-ttu-id="d8910-223">يتم استخدام هذا التنسيق للترجمة التلقائية للتسميات بواسطة خدمات الترجمة الخارجية مثل [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d8910-223">This format is used for automatic translation of labels by  external translation services such as [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md).</span></span> <span data-ttu-id="d8910-224">عند تلقي التسميات المترجمة، فإنه يمكنك استيرادها مرة أخرى إلى إصدار المسودة الخاص بتكوين ER الذي يحتوي على مكونات ER التي تملك هذه التسميات.</span><span class="sxs-lookup"><span data-stu-id="d8910-224">When you receive the translated labels, you can import them back into the draft version of an ER configuration that contains the ER components that own those labels.</span></span> <span data-ttu-id="d8910-225">حدد إصدار المسودة لتكوين ER الذي يحتوي على مكونات ER القابلة للتحرير، وحدد **تبادل \> تحميل التسميات**.</span><span class="sxs-lookup"><span data-stu-id="d8910-225">Select the draft version of an ER configuration that contains the editable ER component, and select **Exchange \> Load labels**.</span></span>

![صفحة تكوينات ER مما يسمح باستيراد تسميات ER إلى إصدار التكوين المحدد](./media/er-multilingual-labels-load.png)

<span data-ttu-id="d8910-227">سيتم استيراد التسميات المترجمة إلى تكوين ER المحدد.</span><span class="sxs-lookup"><span data-stu-id="d8910-227">Translated labels will be imported into the selected ER configuration.</span></span> <span data-ttu-id="d8910-228">يتم استبدال التسميات المترجمة الموجودة في تكوين ER هذا.</span><span class="sxs-lookup"><span data-stu-id="d8910-228">Translated labels that exist in this ER configuration are replaced.</span></span> <span data-ttu-id="d8910-229">إذا كانت أية تسمية مترجمة مفقودة في تكوين ER، فإنه يتم إلحاقها.</span><span class="sxs-lookup"><span data-stu-id="d8910-229">If any translated label is missing in the ER configuration, it's appended.</span></span>

## <a name="lifecycle"></a><span data-ttu-id="d8910-230">Lifecycle</span><span class="sxs-lookup"><span data-stu-id="d8910-230">Lifecycle</span></span>

<span data-ttu-id="d8910-231">يتم الاحتفاظ بتسميات مكون ER التي يمكن تحريرها، مع المحتوي الآخر للمكون، في الإصدار المناسب من تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-231">Labels of an ER component that can be edited are kept, together with other content for the component, in the appropriate version of an ER configuration.</span></span>

<span data-ttu-id="d8910-232">ويمكن الإشارة إلى تسميات مكون ER الأساسي في إصدار مشتق من مكون ER الذي قمت بإنشاءه لتقديم التعديلات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="d8910-232">Labels of a base ER component can be referred to in a derived version of the ER component that you create to introduce your modifications.</span></span>

<span data-ttu-id="d8910-233">يتحكم إصدار ER في تعيين التسمية إلى أي سمة في مكون ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-233">ER versioning controls label assignment to any attribute in an ER component.</span></span> <span data-ttu-id="d8910-234">يتم تسجيل التغييرات التي يتم إجراؤها على تعيين التسمية في قائمة التغييرات (دلتا) الخاصة بمكون ER قابل للتحرير والذي تم إنشاؤه كإصدار مشتق من مكون ER المقدم.</span><span class="sxs-lookup"><span data-stu-id="d8910-234">Changes to the label assignment are recorded in the list of changes (delta) of an editable ER component that has been created as a derived version of the provided ER component.</span></span> <span data-ttu-id="d8910-235">سيتم التحقق من صحة هذه التغييرات عندما تتم إعادة تعيين الإصدار المشتق إلى إصدار أساسي جديد.</span><span class="sxs-lookup"><span data-stu-id="d8910-235">These changes will be validated when a derived version is rebased to a new base version.</span></span>

## <a name="functions"></a><span data-ttu-id="d8910-236">الوظائف</span><span class="sxs-lookup"><span data-stu-id="d8910-236">Functions</span></span>

<span data-ttu-id="d8910-237">يمكن لوظيفة ER [LISTOFFIELDS](er-functions-list-listoffields.md) المضمنة الوصول إلى تسميات ER التي تم تكوينها لبعض عناصر ER.</span><span class="sxs-lookup"><span data-stu-id="d8910-237">The built-in [LISTOFFIELDS](er-functions-list-listoffields.md) ER function can access ER labels that have been configured for some items of ER components.</span></span>

<span data-ttu-id="d8910-238">وكما هو موضح سابقًا في هذا الموضوع، فإنه يمكن ربط السمتين **التسمية** و **الوصف** لكل قيمة تعداد ER [النموذج](#LinkModelEnum) أو [التنسيق](#LinkFormatEnum) بتسمية ER يمكن الوصول إليها في مكون ER المناسب.</span><span class="sxs-lookup"><span data-stu-id="d8910-238">As described earlier in this topic, the **Label** and **Description** attributes of every [model](#LinkModelEnum) or [format](#LinkFormatEnum) ER enumeration's value can be linked to an ER label that is accessible in the appropriate ER component.</span></span> <span data-ttu-id="d8910-239">يمكنك تكوين تعبير ER حيث تقوم باستدعاء الوظيفة **LISTOFFIELDS** باستخدام تعداد ER كوسيطة.</span><span class="sxs-lookup"><span data-stu-id="d8910-239">You can configure an ER expression where you call the **LISTOFFIELDS** function by using the ER enumeration as an argument.</span></span> <span data-ttu-id="d8910-240">يقوم هذا التعبير بإرجاع قائمة تحتوي على سجل لكل قيمة في قائمة تعداد ER تم تعريفها كوسيطة لهذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="d8910-240">This expression returns a list that contains a record for every value of an ER enumeration that has been defined as an argument of this function.</span></span> <span data-ttu-id="d8910-241">يحتوي كل سجل على القيمة الخاصة بتسمية ER المرتبطة بقيمة تعداد ER:</span><span class="sxs-lookup"><span data-stu-id="d8910-241">Every record contains the value of an ER label that is linked to an ER enumeration value:</span></span>

- <span data-ttu-id="d8910-242">يتم تخزين قيمة تسمية ER المرتبطة بسمات **التسمية** في الحقل **التسمية** للسجل الذي تم إرجاعه.</span><span class="sxs-lookup"><span data-stu-id="d8910-242">The value of an ER label that is linked to the **Label** attributes is stored in the **Label** field of the returned record.</span></span>
- <span data-ttu-id="d8910-243">يتم تخزين قيمة تسمية ER المرتبطة بسمات **الوصف** في الحقل **الوصف** للسجل الذي تم إرجاعه.</span><span class="sxs-lookup"><span data-stu-id="d8910-243">The value of an ER label that is linked to the **Description** attributes is stored in the **Description** field of the returned record.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8910-244">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d8910-244">Additional resources</span></span>

- [<span data-ttu-id="d8910-245">نظرة عامة حول التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d8910-245">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d8910-246">وظائف التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="d8910-246">Electronic Reporting functions</span></span>](er-formula-language.md#functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]