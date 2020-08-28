---
title: دالة إعداد التقارير الإلكترونية LISTDISTINCT
description: يوفر هذا الموضوع معلومات حول كيفية استخدام دالة إعداد التقارير الإلكترونية LISTDISTINCT.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 791038981e88d0f52026bfb17d2d1fa381f28c46
ms.sourcegitcommit: 41e165482b9bff4175c0e3b224dbeead13461956
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/11/2020
ms.locfileid: "3687997"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="ff217-103">دالة إعداد التقارير الإلكترونية LISTDISTINCT</span><span class="sxs-lookup"><span data-stu-id="ff217-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ff217-104">تقوم الدالة `LISTDISTINCT` بحساب التعبير المحدد كمحدد لكل سجل من القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="ff217-105">وتقوم بإرجاع قيمة *قائمة سجلات* جديدة تحتوي على سجل مفرد لكل قيمة محدد فريدة.</span><span class="sxs-lookup"><span data-stu-id="ff217-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff217-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ff217-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="ff217-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ff217-107">Arguments</span></span>

<span data-ttu-id="ff217-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="ff217-108">`list`: *Record list*</span></span>

<span data-ttu-id="ff217-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="ff217-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ff217-110">`selector`: *نوع البيانات الأساسي*</span><span class="sxs-lookup"><span data-stu-id="ff217-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="ff217-111">تعبير صالح يتم استخدامه لحساب قيمة محدد لكل سجل في القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="ff217-112">أنواع البيانات التالية مدعومة لهذه المعلمة:</span><span class="sxs-lookup"><span data-stu-id="ff217-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="ff217-113">منطقي</span><span class="sxs-lookup"><span data-stu-id="ff217-113">Boolean</span></span>
- <span data-ttu-id="ff217-114">التاريخ</span><span class="sxs-lookup"><span data-stu-id="ff217-114">Date</span></span>
- <span data-ttu-id="ff217-115">التاريخ/الوقت</span><span class="sxs-lookup"><span data-stu-id="ff217-115">DateTime</span></span>
- <span data-ttu-id="ff217-116">Guid</span><span class="sxs-lookup"><span data-stu-id="ff217-116">GUID</span></span>
- <span data-ttu-id="ff217-117">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="ff217-117">Integer</span></span>
- <span data-ttu-id="ff217-118">Int64</span><span class="sxs-lookup"><span data-stu-id="ff217-118">Int64</span></span>
- <span data-ttu-id="ff217-119">حقيقي</span><span class="sxs-lookup"><span data-stu-id="ff217-119">Real</span></span>
- <span data-ttu-id="ff217-120">السلسلة</span><span class="sxs-lookup"><span data-stu-id="ff217-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="ff217-121">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ff217-121">Return values</span></span>

<span data-ttu-id="ff217-122">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="ff217-122">*Record list*</span></span>

<span data-ttu-id="ff217-123">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ff217-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ff217-124">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ff217-124">Usage notes</span></span>

<span data-ttu-id="ff217-125">بنية القائمة التي تم إنشاؤها تتطابق مع بنية القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="ff217-126">قد يتم حساب نفس قيمة المحدد لسجلات متعددة في القائمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="ff217-127">في هذه الحالة، تكون قيم الحقول الخاصة بالسجل المقابل في القائمة التي تم إنشاؤها مساوية لقيم السجل الأول من القائمة المحددة التي يتم حساب قيمة المحدد لها.</span><span class="sxs-lookup"><span data-stu-id="ff217-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="ff217-128">يتم تنفيذ هذه الوظيفة على مصدر بيانات [إعداد التقارير الإلكترونية](general-electronic-reporting.md) لنوع *قائمة السجلات* الموجود في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="ff217-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="ff217-129">يمكن أيضًا استخدام مصدر البيانات **GROUPBY** لإنشاء قائمة بالسجلات التي يتم من خلالها حساب المحدد الذي يتضمن قيمًا مميزة.</span><span class="sxs-lookup"><span data-stu-id="ff217-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="ff217-130">ومع ذلك، من منظور الأداء واستهلاك الذاكرة، من الأفضل استخدام الدالة `LISTDISTINCT` بدلاً من مصدر البيانات **GROUPBY‎**، لأن تنفيذ الوظيفة يتم في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="ff217-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="ff217-131">مثال</span><span class="sxs-lookup"><span data-stu-id="ff217-131">Example</span></span>

<span data-ttu-id="ff217-132">يوضح المثال التالي كيفية الحصول علي قائمة بأرقام حسابات العملاء الفريدة التي تم إصدار فاتورة مبيعات أو فاتورة مشروع واحدة عل الأقل خلال فترة محددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="ff217-133">أدخل مصدر البيانات **SalesInvoice** للنوع `Record list` الذي يشير إلى جدول التطبيق **CustInvoiceJour** ويصفي فواتير المبيعات لفترات محددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="ff217-134">يقوم الحقل `InvoiceAccount` لمصدر البيانات هذا بإرجاع رقم الحساب الخاص بعميل تمت فوترته.</span><span class="sxs-lookup"><span data-stu-id="ff217-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="ff217-135">أدخل مصدر البيانات **ProjectInvoice** للنوع `Record list` الذي يشير إلى جدول التطبيق **ProjInvoiceJour** ويصفي فواتير المشاريع لفترات محددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="ff217-136">يقوم الحقل `InvoiceAccount` لمصدر البيانات هذا بإرجاع رقم الحساب الخاص بعميل تمت فوترته.</span><span class="sxs-lookup"><span data-stu-id="ff217-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="ff217-137">قم بتكوين مصدر البيانات **AllInvoices** من النوع `Calculated field` الذي يحتوي على التعبير `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="ff217-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="ff217-138">يقوم مصدر البيانات هذا بإرجاع القائمة المرتبطة لفواتير المبيعات وفواتير المشروع.</span><span class="sxs-lookup"><span data-stu-id="ff217-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="ff217-139">قم بتكوين مصدر البيانات **InvoicedCustomer** من النوع `Record list` الذي يحتوي على التعبير `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="ff217-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="ff217-140">يقوم مصدر البيانات هذا بإرجاع قائمة جديدة تحتوي على سجل مفرد لكل عميل فريد تمت فوترته خلال الفترة المحددة.</span><span class="sxs-lookup"><span data-stu-id="ff217-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="ff217-141">يحتوي الحقل `InvoiceAccount` الخاص بهذه القائمة على رقم حساب عميل.</span><span class="sxs-lookup"><span data-stu-id="ff217-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff217-142">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ff217-142">Additional resources</span></span>

[<span data-ttu-id="ff217-143">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="ff217-143">List functions</span></span>](er-functions-category-list.md)
