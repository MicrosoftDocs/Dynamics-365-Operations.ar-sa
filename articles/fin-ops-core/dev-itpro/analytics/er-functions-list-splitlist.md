---
title: SPLITLIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLITLIST (ER).
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745559"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="2481d-103">SPLITLIST ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="2481d-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2481d-104">تقسم الوظيفة `SPLITLIST` القائمة المُحددة إلى قوائم فرعية (أو دفعات)، تحتوي كل واحدة منها على العدد المُحدد من السجلات.</span><span class="sxs-lookup"><span data-stu-id="2481d-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="2481d-105">ثم يقوم بإرجاع النتيجة كقيمة *قائمة سجلات* جديدة التي تتكون من الدفعات.</span><span class="sxs-lookup"><span data-stu-id="2481d-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="2481d-106">بناء الجملة 1</span><span class="sxs-lookup"><span data-stu-id="2481d-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="2481d-107">بناء الجملة 2</span><span class="sxs-lookup"><span data-stu-id="2481d-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="2481d-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2481d-108">Arguments</span></span>

<span data-ttu-id="2481d-109">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="2481d-109">`list`: *Record list*</span></span>

<span data-ttu-id="2481d-110">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="2481d-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="2481d-111">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="2481d-111">`number`: *Integer*</span></span>

<span data-ttu-id="2481d-112">أقصى عدد للسجلات لكل دفعة.</span><span class="sxs-lookup"><span data-stu-id="2481d-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="2481d-113">`on-demand reading flag`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="2481d-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="2481d-114">*قيمة منطقية* القيمة التي تحدد ما إذا كان يجب إنشاء عناصر القوائم الفرعية عند الطلب.</span><span class="sxs-lookup"><span data-stu-id="2481d-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="2481d-115">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2481d-115">Return values</span></span>

<span data-ttu-id="2481d-116">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="2481d-116">*Record list*</span></span>

<span data-ttu-id="2481d-117">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2481d-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2481d-118">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="2481d-118">Usage notes</span></span>

<span data-ttu-id="2481d-119">تحتوي قائمة الدفعات التي تم إرجاعها على العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="2481d-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="2481d-120">**القيمة:** *القائمة*</span><span class="sxs-lookup"><span data-stu-id="2481d-120">**Value:** *List*</span></span>

    <span data-ttu-id="2481d-121">قائمة السجلات التي تخص الدفعة الحالية.</span><span class="sxs-lookup"><span data-stu-id="2481d-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="2481d-122">**BatchNumber:** *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="2481d-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="2481d-123">عدد الدفعات الحالية في القائمة المُرتجعة.</span><span class="sxs-lookup"><span data-stu-id="2481d-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="2481d-124">عند تعيين علامة القراءة عند الطلب على **True**، يتم إنشاء القوائم الفرعية عند الطلب مما يسمح بتقليل استهلاك الذاكرة ولكن قد يتسبب في تدهور الأداء إذا لم يتم استخدام العناصر بشكل تسلسلي.</span><span class="sxs-lookup"><span data-stu-id="2481d-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="2481d-125">مثال</span><span class="sxs-lookup"><span data-stu-id="2481d-125">Example</span></span>

<span data-ttu-id="2481d-126">في الرسم التوضيح التالي، يتم إنشاء مصدر بيانات **الخطوط** كقائمة سجلات تحتوي على ثلاث سجلات.</span><span class="sxs-lookup"><span data-stu-id="2481d-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="2481d-127">يتم تقسيم هذه القائمة إلى دُفعات، يحتوي كل منها على ما يصل إلى سجلين.</span><span class="sxs-lookup"><span data-stu-id="2481d-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="2481d-128">يبين الرسم التوضيحي التالي تخطيط التنسيق المصمم.</span><span class="sxs-lookup"><span data-stu-id="2481d-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="2481d-129">في تخطيط التنسيق هذا، يتم إنشاء عمليات الربط إلى مصدر بيانات **الخطوط** لإنشاء إخراج بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="2481d-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="2481d-130">يقدم هذا الإخراج عقدًا فردية لكل دُفعة والسجلات التي فيها.</span><span class="sxs-lookup"><span data-stu-id="2481d-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="2481d-131">يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.</span><span class="sxs-lookup"><span data-stu-id="2481d-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="2481d-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2481d-132">Additional resources</span></span>

[<span data-ttu-id="2481d-133">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="2481d-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
