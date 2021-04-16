---
title: ORDERBY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية ORDERBY (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753182"
---
# <a name="orderby-er-function"></a><span data-ttu-id="14dea-103">ORDERBY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="14dea-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14dea-104">تُرجع الوظيفة `ORDERBY` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تم فرزها وفقًا للوسيطات المُحددة.</span><span class="sxs-lookup"><span data-stu-id="14dea-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="14dea-105">يمكن تعريف الوسيطات التالية كعبارات.</span><span class="sxs-lookup"><span data-stu-id="14dea-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="14dea-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="14dea-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="14dea-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="14dea-107">Arguments</span></span>

<span data-ttu-id="14dea-108">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="14dea-108">`list`: *Record list*</span></span>

<span data-ttu-id="14dea-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="14dea-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="14dea-110">`expression 1`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="14dea-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="14dea-111">المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها.</span><span class="sxs-lookup"><span data-stu-id="14dea-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="14dea-112">يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="14dea-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="14dea-113">هذه الوسيطة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="14dea-113">This argument is required.</span></span>

<span data-ttu-id="14dea-114">`expression N`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="14dea-114">`expression N`: *Field*</span></span>

<span data-ttu-id="14dea-115">المسار الصالح لحقل مصدر البيانات المُشار إليه بواسطة الوسطية `list` للوظيفة التي تم استدعائها.</span><span class="sxs-lookup"><span data-stu-id="14dea-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="14dea-116">يجب ملء الحقل المُشار إليه من نوع البيانات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="14dea-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="14dea-117">هذه الوسائط الإضافية اختيارية.</span><span class="sxs-lookup"><span data-stu-id="14dea-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="14dea-118">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="14dea-118">Return values</span></span>

<span data-ttu-id="14dea-119">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="14dea-119">*Record list*</span></span>

<span data-ttu-id="14dea-120">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="14dea-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="14dea-121">مثال1</span><span class="sxs-lookup"><span data-stu-id="14dea-121">Example 1</span></span>

<span data-ttu-id="14dea-122">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( ORDERBY( DS, DS. Value)).Value` القيمة النصية **"A"**.</span><span class="sxs-lookup"><span data-stu-id="14dea-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="14dea-123">مثال2</span><span class="sxs-lookup"><span data-stu-id="14dea-123">Example 2</span></span>

<span data-ttu-id="14dea-124">عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `ORDERBY (Vendors, Vendors.'name()')` قائمة مورّدين تم فرزها حسب الاسم بترتيب تصاعدي.</span><span class="sxs-lookup"><span data-stu-id="14dea-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14dea-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="14dea-125">Additional resources</span></span>

[<span data-ttu-id="14dea-126">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="14dea-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]