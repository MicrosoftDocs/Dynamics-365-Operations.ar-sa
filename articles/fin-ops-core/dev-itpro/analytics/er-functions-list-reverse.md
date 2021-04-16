---
title: REVERSE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية REVERSE (ER).
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755194"
---
# <a name="reverse-er-function"></a><span data-ttu-id="1d7d7-103">REVERSE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="1d7d7-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d7d7-104">تُرجع الوظيفة `REVERSE` القائمة المُحددة كقيمة *قائمة التسجيلات* في ترتيب فرز معكوس.</span><span class="sxs-lookup"><span data-stu-id="1d7d7-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d7d7-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="1d7d7-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="1d7d7-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="1d7d7-106">Arguments</span></span>

<span data-ttu-id="1d7d7-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="1d7d7-107">`list`: *Record list*</span></span>

<span data-ttu-id="1d7d7-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="1d7d7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1d7d7-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="1d7d7-109">Return values</span></span>

<span data-ttu-id="1d7d7-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="1d7d7-110">*Record list*</span></span>

<span data-ttu-id="1d7d7-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="1d7d7-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="1d7d7-112">مثال1</span><span class="sxs-lookup"><span data-stu-id="1d7d7-112">Example 1</span></span>

<span data-ttu-id="1d7d7-113">إذا قمت بإدخال مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("C|B|A", "|")` ، يُرجع التعبير `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` القيمة النصية **"C"**.</span><span class="sxs-lookup"><span data-stu-id="1d7d7-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1d7d7-114">مثال2</span><span class="sxs-lookup"><span data-stu-id="1d7d7-114">Example 2</span></span>

<span data-ttu-id="1d7d7-115">عند تكوين **Vendor** كمصدر بيانات تقارير إلكترونية (ER) يشير إلى جدول VendTable، يُرجع التعبير `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` قائمة مورّدين تم فرزها حسب الاسم بترتيب تنازلي.</span><span class="sxs-lookup"><span data-stu-id="1d7d7-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d7d7-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1d7d7-116">Additional resources</span></span>

[<span data-ttu-id="1d7d7-117">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="1d7d7-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]