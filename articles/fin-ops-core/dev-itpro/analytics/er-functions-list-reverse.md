---
title: REVERSE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية REVERSE (ER).
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917225"
---
# <span data-ttu-id="edca4-103"><a name="REVERSE">REVERSE ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="edca4-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edca4-104">تُرجع الوظيفة `REVERSE` القائمة المُحددة كقيمة *قائمة التسجيلات* في ترتيب فرز معكوس.</span><span class="sxs-lookup"><span data-stu-id="edca4-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="edca4-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="edca4-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="edca4-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="edca4-106">Arguments</span></span>

<span data-ttu-id="edca4-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="edca4-107">`list`: *Record list*</span></span>

<span data-ttu-id="edca4-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="edca4-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="edca4-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="edca4-109">Return values</span></span>

<span data-ttu-id="edca4-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="edca4-110">*Record list*</span></span>

<span data-ttu-id="edca4-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="edca4-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="edca4-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="edca4-112">Example 1</span></span>

<span data-ttu-id="edca4-113">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` القيمة النصية **"C"**.</span><span class="sxs-lookup"><span data-stu-id="edca4-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="edca4-114">مثال2</span><span class="sxs-lookup"><span data-stu-id="edca4-114">Example 2</span></span>

<span data-ttu-id="edca4-115">عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` قائمة مورّدين تم فرزها حسب الاسم بترتيب تنازلي.</span><span class="sxs-lookup"><span data-stu-id="edca4-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edca4-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="edca4-116">Additional resources</span></span>

[<span data-ttu-id="edca4-117">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="edca4-117">List functions</span></span>](er-functions-category-list.md)
