---
title: وظيفة FORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FORMAT (ER).
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
ms.openlocfilehash: 3f3e8e5f6676c26b8d604ed950470463f04c0473
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743869"
---
# <a name="format-er-function"></a><span data-ttu-id="6a36e-103">وظيفة FORMAT ER</span><span class="sxs-lookup"><span data-stu-id="6a36e-103">FORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a36e-104">تُرجع الوظيفة `FORMAT` السلسلة المُحددة كقيمة *سلسلة* بعد أن تم تنسيقها باستبدال أي تواجد من **%N** بالوسيطة *N*.</span><span class="sxs-lookup"><span data-stu-id="6a36e-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a36e-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="6a36e-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="6a36e-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="6a36e-106">Arguments</span></span>

<span data-ttu-id="6a36e-107">`string`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="6a36e-107">`string`: *String*</span></span>

<span data-ttu-id="6a36e-108">مرجع إلى مصدر البيانات من نوع *السلسلة* التي يجب تنسيقها.</span><span class="sxs-lookup"><span data-stu-id="6a36e-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="6a36e-109">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a36e-109">This argument is required.</span></span>

<span data-ttu-id="6a36e-110">`argument 1`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="6a36e-110">`argument 1`: *String*</span></span>

<span data-ttu-id="6a36e-111">الوسيطة الأولى، المستخدمة لاستبدال مرات حدوث **%1**.</span><span class="sxs-lookup"><span data-stu-id="6a36e-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="6a36e-112">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a36e-112">This argument is required.</span></span>

<span data-ttu-id="6a36e-113">`argument N`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="6a36e-113">`argument N`: *String*</span></span>

<span data-ttu-id="6a36e-114">الوسيطة *N* ، المستخدمة لاستبدال مرات الحدوث من **%2** و **%3** وغيرها.</span><span class="sxs-lookup"><span data-stu-id="6a36e-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="6a36e-115">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="6a36e-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6a36e-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="6a36e-116">Return values</span></span>

<span data-ttu-id="6a36e-117">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="6a36e-117">*String*</span></span>

<span data-ttu-id="6a36e-118">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="6a36e-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6a36e-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="6a36e-119">Usage notes</span></span>

<span data-ttu-id="6a36e-120">إذا لم يتم توفير وسيطة لمعلمة، فسيتم إرجاع المعلمة على الشكل **"% N"** في السلسلة.</span><span class="sxs-lookup"><span data-stu-id="6a36e-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="6a36e-121">بالنسبة إلى القيم من النوع *الحقيقي*، تتحدد سلسلة التحويل الافتراضية بمنزلتين عشريتين.</span><span class="sxs-lookup"><span data-stu-id="6a36e-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="6a36e-122">مثال</span><span class="sxs-lookup"><span data-stu-id="6a36e-122">Example</span></span>

<span data-ttu-id="6a36e-123">في الرسم التوضيحي التالي، يُرجع مصدر البيانات **PaymentModel** قائمة سجلات العُملاء باستخدام مكون **العميل**.</span><span class="sxs-lookup"><span data-stu-id="6a36e-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="6a36e-124">يقوم بإرجاع قيمة تاريخ المُعالجة باستخدام الحقل **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6a36e-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="6a36e-125">في تنسيق التقارير الإلكترونية (ER) المصمم لإنشاء ملف إلكتروني لعملاء معينين، يتم تحديد **PaymentModel** كمصدر بيانات ويتحكم بسير العملية.</span><span class="sxs-lookup"><span data-stu-id="6a36e-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="6a36e-126">عند إيقاف عميل محدد للتاريخ عندما تتم معالجة التقرير، يتم طرح استثناء لإبلاغ المستخدم. </span><span class="sxs-lookup"><span data-stu-id="6a36e-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="6a36e-127">باستطاعة المعادلة المصممة لنوع التحكم بالمعالجة هذا استخدام الموارد التالية:</span><span class="sxs-lookup"><span data-stu-id="6a36e-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="6a36e-128">تسمية SYS70894، التي تتضمن النص التالي:</span><span class="sxs-lookup"><span data-stu-id="6a36e-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="6a36e-129">**للغة الإنجليزية-الولايات المتحدة:** "Nothing to print"</span><span class="sxs-lookup"><span data-stu-id="6a36e-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="6a36e-130">**للغة الألمانية:** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="6a36e-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="6a36e-131">تسمية SYS18389، التي تتضمن النص التالي:</span><span class="sxs-lookup"><span data-stu-id="6a36e-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="6a36e-132">**بالنسبة إلى اللغة EN-US:** يتم وقف "العميل %1 لـ %2.</span><span class="sxs-lookup"><span data-stu-id="6a36e-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="6a36e-133">**بالنسبة للغة الألمانية:** "الدائن%1wird für %2 gesperrt." </span><span class="sxs-lookup"><span data-stu-id="6a36e-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="6a36e-134">هذا هو التعبير التي يمكن تصميمه.</span><span class="sxs-lookup"><span data-stu-id="6a36e-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="6a36e-135">إذا تمت معالجة تقرير العميل **Litware Retail** في 17 ديسمبر 2015 بالثقافة **الإنجليزية-الولايات المتحدة** واللغة **الإنجليزية-الولايات المتحدة** فإن هذه المعادلة سترجع النص التالي الذي يمكن تقديمه كرسالة استثناء:</span><span class="sxs-lookup"><span data-stu-id="6a36e-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="6a36e-136">*لا توجد عناصر لطباعتها. العميل Litware Retail موقوف للتاريخ 12/17/2015‎*.</span><span class="sxs-lookup"><span data-stu-id="6a36e-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="6a36e-137">إذا تمت معالجة التقرير نفسه لعميل**Litware Retail** في 17 ديسمبر 2015، بالثقافة **الألمانية** واللغة **الألمانية**، فإن هذه المعادلة ترجع النص التالي الذي يستخدم تنسيق تاريخ آخر:</span><span class="sxs-lookup"><span data-stu-id="6a36e-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="6a36e-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="6a36e-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="6a36e-139">يتم تطبيق بناء الجملة التالي في معادلات التقارير الإلكترونية للتسميات:</span><span class="sxs-lookup"><span data-stu-id="6a36e-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="6a36e-140">**للتسميات من موارد في تطبيق Microsoft Dynamics 365 Finance:** **\@X**، حيث **X** هو معرف التسمية في شجرة مكونات البرنامج (AOT)</span><span class="sxs-lookup"><span data-stu-id="6a36e-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="6a36e-141">**للتسميات المقيمة في تكوينات ER:** **@"GER_LABEL:X"** ، حيث **X** هو معرف التسمية في تكوين ER.</span><span class="sxs-lookup"><span data-stu-id="6a36e-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a36e-142">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a36e-142">Additional resources</span></span>

[<span data-ttu-id="6a36e-143">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="6a36e-143">Text functions</span></span>](er-functions-category-text.md)
