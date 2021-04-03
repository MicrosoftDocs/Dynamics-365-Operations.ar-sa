---
title: REVERSE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية REVERSE (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f76582bc8b752fe0322bee8917d8649ed1c024ba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567356"
---
# <a name="reverse-er-function"></a><span data-ttu-id="9c18f-103">REVERSE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="9c18f-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c18f-104">تُرجع الوظيفة `REVERSE` القائمة المُحددة كقيمة *قائمة التسجيلات* في ترتيب فرز معكوس.</span><span class="sxs-lookup"><span data-stu-id="9c18f-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c18f-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="9c18f-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="9c18f-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="9c18f-106">Arguments</span></span>

<span data-ttu-id="9c18f-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="9c18f-107">`list`: *Record list*</span></span>

<span data-ttu-id="9c18f-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="9c18f-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c18f-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="9c18f-109">Return values</span></span>

<span data-ttu-id="9c18f-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="9c18f-110">*Record list*</span></span>

<span data-ttu-id="9c18f-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="9c18f-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="9c18f-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="9c18f-112">Example 1</span></span>

<span data-ttu-id="9c18f-113">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` القيمة النصية **"C"**.</span><span class="sxs-lookup"><span data-stu-id="9c18f-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9c18f-114">مثال2</span><span class="sxs-lookup"><span data-stu-id="9c18f-114">Example 2</span></span>

<span data-ttu-id="9c18f-115">عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` قائمة مورّدين تم فرزها حسب الاسم بترتيب تنازلي.</span><span class="sxs-lookup"><span data-stu-id="9c18f-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c18f-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9c18f-116">Additional resources</span></span>

[<span data-ttu-id="9c18f-117">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="9c18f-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]