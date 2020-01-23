---
title: ORDERBY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ORDERBY (ER).
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916190"
---
# <span data-ttu-id="67d2f-103"><a name="ORDERBY">ORDERBY ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="67d2f-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67d2f-104">تُرجع الوظيفة `ORDERBY` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تم فرزها وفقًا للوسيطات المُحددة.</span><span class="sxs-lookup"><span data-stu-id="67d2f-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="67d2f-105">يمكن تعريف الوسيطات التالية كعبارات.</span><span class="sxs-lookup"><span data-stu-id="67d2f-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d2f-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="67d2f-106">Syntax</span></span>

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="67d2f-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="67d2f-107">Arguments</span></span>

<span data-ttu-id="67d2f-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="67d2f-108">`list`: *Record list*</span></span>

<span data-ttu-id="67d2f-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="67d2f-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="67d2f-110">`expression 1`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="67d2f-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="67d2f-111">المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها.</span><span class="sxs-lookup"><span data-stu-id="67d2f-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="67d2f-112">يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="67d2f-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="67d2f-113">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="67d2f-113">This argument is required.</span></span>

<span data-ttu-id="67d2f-114">`expression N`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="67d2f-114">`expression N`: *Field*</span></span>

<span data-ttu-id="67d2f-115">المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها.</span><span class="sxs-lookup"><span data-stu-id="67d2f-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="67d2f-116">يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="67d2f-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="67d2f-117">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="67d2f-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="67d2f-118">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="67d2f-118">Return values</span></span>

<span data-ttu-id="67d2f-119">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="67d2f-119">*Record list*</span></span>

<span data-ttu-id="67d2f-120">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="67d2f-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="67d2f-121">مثال1</span><span class="sxs-lookup"><span data-stu-id="67d2f-121">Example 1</span></span>

<span data-ttu-id="67d2f-122">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( ORDERBY( DS, DS. Value)).Value` القيمة النصية **"A"**.</span><span class="sxs-lookup"><span data-stu-id="67d2f-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="67d2f-123">مثال2</span><span class="sxs-lookup"><span data-stu-id="67d2f-123">Example 2</span></span>

<span data-ttu-id="67d2f-124">عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `ORDERBY (Vendors, Vendors.'name()')` قائمة مورّدين تم فرزها حسب الاسم بترتيب تصاعدي.</span><span class="sxs-lookup"><span data-stu-id="67d2f-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67d2f-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="67d2f-125">Additional resources</span></span>

[<span data-ttu-id="67d2f-126">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="67d2f-126">List functions</span></span>](er-functions-category-list.md)
