---
title: SPLITLIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLITLIST (ER).
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
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744781"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="bf405-103">SPLITLIST ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="bf405-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf405-104">تقسم الوظيفة `SPLITLIST` القائمة المُحددة إلى قوائم فرعية (أو دفعات)، تحتوي كل واحدة منها على العدد المُحدد من السجلات.</span><span class="sxs-lookup"><span data-stu-id="bf405-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="bf405-105">ثم يقوم بإرجاع النتيجة كقيمة *قائمة سجلات* جديدة التي تتكون من الدفعات.</span><span class="sxs-lookup"><span data-stu-id="bf405-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf405-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="bf405-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="bf405-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="bf405-107">Arguments</span></span>

<span data-ttu-id="bf405-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="bf405-108">`list`: *Record list*</span></span>

<span data-ttu-id="bf405-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="bf405-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="bf405-110">`number`: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="bf405-110">`number`: *Integer*</span></span>

<span data-ttu-id="bf405-111">أقصى عدد للسجلات لكل دفعة.</span><span class="sxs-lookup"><span data-stu-id="bf405-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="bf405-112">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="bf405-112">Return values</span></span>

<span data-ttu-id="bf405-113">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="bf405-113">*Record list*</span></span>

<span data-ttu-id="bf405-114">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="bf405-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bf405-115">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="bf405-115">Usage notes</span></span>

<span data-ttu-id="bf405-116">تحتوي قائمة الدفعات التي تم إرجاعها على العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="bf405-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="bf405-117">**القيمة:** *القائمة*</span><span class="sxs-lookup"><span data-stu-id="bf405-117">**Value:** *List*</span></span>

    <span data-ttu-id="bf405-118">قائمة السجلات التي تخص الدفعة الحالية.</span><span class="sxs-lookup"><span data-stu-id="bf405-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="bf405-119">**BatchNumber:** *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="bf405-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="bf405-120">عدد الدفعات الحالية في القائمة المُرتجعة.</span><span class="sxs-lookup"><span data-stu-id="bf405-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="bf405-121">مثال</span><span class="sxs-lookup"><span data-stu-id="bf405-121">Example</span></span>

<span data-ttu-id="bf405-122">في الرسم التوضيح التالي، يتم إنشاء مصدر بيانات **الخطوط** كقائمة سجلات تحتوي على ثلاث سجلات.</span><span class="sxs-lookup"><span data-stu-id="bf405-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="bf405-123">يتم تقسيم هذه القائمة إلى دُفعات، يحتوي كل منها على ما يصل إلى سجلين.</span><span class="sxs-lookup"><span data-stu-id="bf405-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="bf405-124">يبين الرسم التوضيحي التالي تخطيط التنسيق المصمم.</span><span class="sxs-lookup"><span data-stu-id="bf405-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="bf405-125">في تخطيط التنسيق هذا، يتم إنشاء عمليات الربط إلى مصدر بيانات **الخطوط** لإنشاء إخراج بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="bf405-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="bf405-126">يقدم هذا الإخراج عقدًا فردية لكل دُفعة والسجلات التي فيها.</span><span class="sxs-lookup"><span data-stu-id="bf405-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="bf405-127">يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.</span><span class="sxs-lookup"><span data-stu-id="bf405-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="bf405-128">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bf405-128">Additional resources</span></span>

[<span data-ttu-id="bf405-129">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="bf405-129">List functions</span></span>](er-functions-category-list.md)
