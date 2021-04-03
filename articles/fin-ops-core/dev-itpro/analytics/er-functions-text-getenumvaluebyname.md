---
title: 'وظيفة GETENUMVALUEBYNAME ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني GETENUMVALUEBYNAME (ER).
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570580"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="3fd50-103">وظيفة GETENUMVALUEBYNAME ER</span><span class="sxs-lookup"><span data-stu-id="3fd50-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fd50-104">تبحث وظيفة `GETENUMVALUEBYNAME` عن قيمة *Enum* مُحددة في مصدر بيانات التعداد المُحدد باستخدام اسم التعداد المُحدد كقيمة *السلسلة* .</span><span class="sxs-lookup"><span data-stu-id="3fd50-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="3fd50-105">إذا تم العثور على قيمة *تعداد* ، تقوم الوظيفة بإرجاعها.</span><span class="sxs-lookup"><span data-stu-id="3fd50-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="3fd50-106">وإلا، تقوم الوظيفة بإرجاع قيمه التعداد **null**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd50-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="3fd50-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="3fd50-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="3fd50-108">Arguments</span></span>

<span data-ttu-id="3fd50-109">`enumeration data source path`: *تعداد*</span><span class="sxs-lookup"><span data-stu-id="3fd50-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="3fd50-110">مسار مرجع صالح لمصدر بيانات أحد أنواع التعداد التالية:</span><span class="sxs-lookup"><span data-stu-id="3fd50-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="3fd50-111">تعداد نموذج إعداد التقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="3fd50-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="3fd50-112">تعداد تنسيق إعداد التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="3fd50-112">ER format enumeration</span></span>
- <span data-ttu-id="3fd50-113">تعداد Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="3fd50-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="3fd50-114">`enumeration value text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="3fd50-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="3fd50-115">قيمة سلسلة تمثل اسم قيمة تعداد مُفرد.</span><span class="sxs-lookup"><span data-stu-id="3fd50-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="3fd50-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="3fd50-116">Return values</span></span>

<span data-ttu-id="3fd50-117">‏‫قابل للإبطال *Enum*</span><span class="sxs-lookup"><span data-stu-id="3fd50-117">Nullable *Enum*</span></span>

<span data-ttu-id="3fd50-118">قيمة التعداد الناتجة.</span><span class="sxs-lookup"><span data-stu-id="3fd50-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3fd50-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="3fd50-119">Usage notes</span></span>

<span data-ttu-id="3fd50-120">لا يتم طرح أي استثناء إذا لم يتم العثور على قيمة *Enum* باستخدام اسم قيمة التعداد المحدد كقيمة *سلسلة* .</span><span class="sxs-lookup"><span data-stu-id="3fd50-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="3fd50-121">مثال1</span><span class="sxs-lookup"><span data-stu-id="3fd50-121">Example 1</span></span>

<span data-ttu-id="3fd50-122">في الرسم التوضيحي التالي، يتم تقديم تعداد **ReportDirection** في نموذج بيانات.</span><span class="sxs-lookup"><span data-stu-id="3fd50-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="3fd50-123">لاحظ أنه يتم تحديد التسميات لقيم التعداد.</span><span class="sxs-lookup"><span data-stu-id="3fd50-123">Notice that labels are defined for the enumeration values.</span></span>

![القيم المتوفرة لقائمة تعداد نموذج البيانات](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="3fd50-125">يبين الرسم التوضيحي التالي هذه التفاصيل:</span><span class="sxs-lookup"><span data-stu-id="3fd50-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="3fd50-126">يتم تكوين مصدر البيانات **$Direction** في تقرير التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="3fd50-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="3fd50-127">يتم تكوين مصدر البيانات هذا استنادًا إلى تعداد نموذج **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="3fd50-128">تم تصميم التعبير `$IsArrivals` ليستخدم مصدر بيانات **$Direction** المستند إلى تعداد النموذج تعداد النموذج كمعلمة لهذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="3fd50-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="3fd50-129">قيمة تعبير المقارنة هذا هي **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-129">The value of this comparison expression is **TRUE**.</span></span>

![مثال عن تعداد نموذج بيانات](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="3fd50-131">مثال2</span><span class="sxs-lookup"><span data-stu-id="3fd50-131">Example 2</span></span>

<span data-ttu-id="3fd50-132">تسمح لك الدالتان `GETENUMVALUEBYNAME` و[`LISTOFFIELDS`](er-functions-list-listoffields.md) بإحضار قيم وتسميات التعدادات المعتمدة كقيم نصية.</span><span class="sxs-lookup"><span data-stu-id="3fd50-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="3fd50-133">(التعدادات المعتمدة هي تعدادات التطبيق وتعدادات نموذج البيانات وتعدادات التنسيق.)</span><span class="sxs-lookup"><span data-stu-id="3fd50-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="3fd50-134">في الرسم التوضيحي التالي، يتم تقديم مصدر البيانات **TransType** في تعيين نموذج.</span><span class="sxs-lookup"><span data-stu-id="3fd50-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="3fd50-135">يُشير مصدر البيانات هذا إلى تعداد تطبيق **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![مصدر بيانات لتعيين النموذج الذي يشير إلى تعداد التطبيق](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="3fd50-137">يبين الرسم التوضيحي التالي مصدر البيانات **TransTypeList** المكوّن في تعيين نموذج.</span><span class="sxs-lookup"><span data-stu-id="3fd50-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="3fd50-138">يتم تكوين مصدر البيانات هذا استنادًا إلى تعداد تطبيق **TransType**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="3fd50-139">تُستخدم الدالة `LISTOFFIELDS` لإرجاع كافة قيم التعداد كقائمة سجلات تحتوي على حقول.</span><span class="sxs-lookup"><span data-stu-id="3fd50-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="3fd50-140">بهذه الطريقة، يتم عرض تفاصيل كل قيمة من قيم التعداد.</span><span class="sxs-lookup"><span data-stu-id="3fd50-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="3fd50-141">تم تكوين الحقل **EnumValue** لمصدر البيانات **TransTypeList** باستخدام التعبير `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="3fd50-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="3fd50-142">يرجع هذا الحقل قيمة التعداد لكل سجل في هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="3fd50-142">This field returns an enumeration value for every record in this list.</span></span>

![مصدر بيانات لتعيين النموذج الذي يرجع كافة قيم التعداد لتعداد محدد كقائمة بالسجلات](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="3fd50-144">يبين الرسم التوضيحي التالي مصدر البيانات **VendTrans** المكوّن في تعيين نموذج.</span><span class="sxs-lookup"><span data-stu-id="3fd50-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="3fd50-145">يقوم مصدر البيانات هذا بإرجاع سجلات حركات المورّد من جدول تطبيق **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="3fd50-146">يتم تحديد نوع دفتر الأستاذ لكل حركة بواسطة قيمة الحقل **TransType**.</span><span class="sxs-lookup"><span data-stu-id="3fd50-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="3fd50-147">تم تكوين الحقل **TransTypeTitle** لمصدر البيانات **VendTrans** باستخدام التعبير `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="3fd50-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="3fd50-148">يقوم هذا الحقل بإرجاع تسمية قيمة التعداد الخاصة بالحركة الحالية كنص، إذا كانت قيمة التعداد هذه متوفرة.</span><span class="sxs-lookup"><span data-stu-id="3fd50-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="3fd50-149">وإلا، فسيقوم بإرجاع قيمة سلسلة فارغة.</span><span class="sxs-lookup"><span data-stu-id="3fd50-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="3fd50-150">يرتبط الحقل **TransTypeTitle** بحقل **LedgerType** لنموذج بيانات يمكّن استخدام هذه المعلومات في كل تنسيقات التقارير الإلكترونية التي تستخدم نموذج البيانات كمصدر بيانات.</span><span class="sxs-lookup"><span data-stu-id="3fd50-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![مصدر بيانات لتعيين النموذج الذي يُرجع حركات المورّد](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="3fd50-152">يبين الرسم التوضيحي التالي كيف يمكنك استخدام [مصحح أخطاء مصدر البيانات](er-debug-data-sources.md) لاختبار تعيين النموذج المكوّن.</span><span class="sxs-lookup"><span data-stu-id="3fd50-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![استخدام مصحح أخطاء مصدر البيانات لاختبار تعيين النموذج المكوّن](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="3fd50-154">يعرض حقل **LedgerType** لنموذج بيانات تسمية أنواع الحركات كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="3fd50-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="3fd50-155">إذا كنت تخطط لاستخدام هذه الطريقة كمية كبيره من بيانات الحركات، فيجب مراعاة أداء التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="3fd50-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="3fd50-156">لمزيد من المعلومات، راجع [تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="3fd50-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fd50-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3fd50-157">Additional resources</span></span>

[<span data-ttu-id="3fd50-158">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="3fd50-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="3fd50-159">تتبع تنفيذ تنسيقات التقارير الإلكترونية لاستكشاف مشكلات الأداء وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="3fd50-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="3fd50-160">LISTOFFIELDS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="3fd50-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="3fd50-161">FIRSTORNULL ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="3fd50-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="3fd50-162">WHERE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="3fd50-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]