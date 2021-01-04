---
title: WHERE ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية WHERE (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cc47c5001cf456b1fc600b326f826ea3b8b43ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687040"
---
# <a name="where-er-function"></a><span data-ttu-id="853a4-103">WHERE ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="853a4-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="853a4-104">تُرجع الوظيفة `WHERE` القائمة المُحددة كقيمة *قائمة السجلات* بعد أن تمت تصفيتها وفقًا للشرط المُحدد.</span><span class="sxs-lookup"><span data-stu-id="853a4-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="853a4-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="853a4-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="853a4-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="853a4-106">Arguments</span></span>

<span data-ttu-id="853a4-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="853a4-107">`list`: *Record list*</span></span>

<span data-ttu-id="853a4-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="853a4-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="853a4-109">`condition`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="853a4-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="853a4-110">تعبير شرطي صالح يُستخدم لتصفية سجلات القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="853a4-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="853a4-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="853a4-111">Return values</span></span>

<span data-ttu-id="853a4-112">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="853a4-112">*Record list*</span></span>

<span data-ttu-id="853a4-113">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="853a4-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="853a4-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="853a4-114">Usage notes</span></span>

<span data-ttu-id="853a4-115">تختلف هذه الوظيفة عن وظيفة [FILTER](er-functions-list-filter.md) ، لأن يتم تطبيق الشرط المُحدد على أي من مصادر بيانات التقارير الإلكترونية (ER) لنوع *قائمة السجلات* الموجودة في الذاكرة.</span><span class="sxs-lookup"><span data-stu-id="853a4-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="853a4-116">إذا كانت هذه الوسيطات المكونة لهذه الوظيفة (`list` و`condition`) تسمح بترجمة هذا الطلب للاستدعاء المباشر لـ SQL، يتم طرح رسالة تحذيرية في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="853a4-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="853a4-117">تُعلم هذه الرسالة المستخدم أنه يُمكنه تحسين الأداء إذا تم استخدام الوظيفة [FILTER](er-functions-list-filter.md) بدلًا من `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="853a4-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="853a4-118">مثال1</span><span class="sxs-lookup"><span data-stu-id="853a4-118">Example 1</span></span>

<span data-ttu-id="853a4-119">إذا تم تكوين **Vendor** كمصدر بيانات تقارير إلكترونية يشير إلى جدول VendTable، يُرجع التعبير `WHERE (Vendors, Vendors.VendGroup = "40")` قائمة المورّدين التي تنتمي إلى مجموعة الموردين 40.</span><span class="sxs-lookup"><span data-stu-id="853a4-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="853a4-120">مثال2</span><span class="sxs-lookup"><span data-stu-id="853a4-120">Example 2</span></span>

<span data-ttu-id="853a4-121">إذا أدخلت مصدر البيانات **DS** من النوع *الحقل المحسوب* ، ويحتوي على التعبير `SPLIT ("A|B|C", "|")` ، يُرجع التعبير `WHERE( DS, DS.Value = "B")` قائمة بسجل واحد فقط يحتوي على النص **"B"** في حقل **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="853a4-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="853a4-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="853a4-122">Additional resources</span></span>

[<span data-ttu-id="853a4-123">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="853a4-123">List functions</span></span>](er-functions-category-list.md)
