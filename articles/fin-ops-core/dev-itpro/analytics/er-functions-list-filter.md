---
title: FILTER ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FILTER (ER).
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
ms.openlocfilehash: 55fa3d4ad4427e2a45f7c5fce679c50a91c40b6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679428"
---
# <a name="filter-er-function"></a><span data-ttu-id="a8d03-103">FILTER ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="a8d03-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8d03-104">تٌرجع وظيفة `FILTER` القائمة المُحددة كقيمة *قائمة سجلات* بعد تغيير الاستعلام بحيث تتم تصفيتها للشرط المُحدد.</span><span class="sxs-lookup"><span data-stu-id="a8d03-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d03-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="a8d03-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="a8d03-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="a8d03-106">Arguments</span></span>

<span data-ttu-id="a8d03-107">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="a8d03-107">`list`: *Record list*</span></span>

<span data-ttu-id="a8d03-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="a8d03-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a8d03-109">`condition`: *منطقي*</span><span class="sxs-lookup"><span data-stu-id="a8d03-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="a8d03-110">تعبير شرطي صالح يُستخدم لتصفية سجلات القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="a8d03-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="a8d03-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="a8d03-111">Return values</span></span>

<span data-ttu-id="a8d03-112">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="a8d03-112">*Record list*</span></span>

<span data-ttu-id="a8d03-113">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="a8d03-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a8d03-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="a8d03-114">Usage notes</span></span>

<span data-ttu-id="a8d03-115">تختلف هذه وظيفة عن وظيفة [WHERE](er-functions-list-where.md) لأنه يتم تطبيق الشرط المحدد على أي من مصادر بيانات التقارير الإلكترونية (ER) لنوع *سجلات الجداول* على مستوى قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a8d03-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="a8d03-116">يمكن تحديد القائمة والشرط باستخدام الجداول والعلاقات.</span><span class="sxs-lookup"><span data-stu-id="a8d03-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="a8d03-117">إذا لم تسمح أحد الوسيطتين أو كليهما المكونة لهذه الوظيفة (`list` و`condition`) بترجمة هذا الطلب للاستدعاء المباشر لـ SQL، يتم طرح استثناء في وقت التصميم.</span><span class="sxs-lookup"><span data-stu-id="a8d03-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="a8d03-118">يُعلم هذا الاستثناء المستخدم أنه إما `list` أو `condition` لا يُمكن استخدامهم للاستعلام عن قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="a8d03-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="a8d03-119">مثال1</span><span class="sxs-lookup"><span data-stu-id="a8d03-119">Example 1</span></span>

<span data-ttu-id="a8d03-120">إذا تم تكوين **Vendor** كمصدر بيانات تقارير إلكترونية يشير إلى جدول VendTable، يُرجع التعبير `FILTER (Vendors, Vendors.VendGroup = "40")` قائمة المورّدين التي تنتمي إلى مجموعة الموردين 40.</span><span class="sxs-lookup"><span data-stu-id="a8d03-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="a8d03-121">مثال2</span><span class="sxs-lookup"><span data-stu-id="a8d03-121">Example 2</span></span>

<span data-ttu-id="a8d03-122">إذا تم تكوين **المورّد** كمصدر بيانات التقارير الإلكترونية (ER) يُشير إلى جدول VendTable، وإذا تم تكوين **parmVendorBankGroup** كمصدر بيانات التقارير الإلكترونية (ER) يُرجع قيمة نوع بيانات *السلسلة*، يُرجع التعبير `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` قائمة حسابات المورّدين الذين ينتمون إلى مجموعة بنكية مُحددة.</span><span class="sxs-lookup"><span data-stu-id="a8d03-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="a8d03-123">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="a8d03-123">Example 3</span></span>

<span data-ttu-id="a8d03-124">يُمكنك إدخال مصدر بيانات **DS** من النوع *الحقل المحسوب* ، الذي يحتوي على التعبير `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="a8d03-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="a8d03-125">ثم قم بإدخال تعبير آخر، `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="a8d03-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="a8d03-126">عندما تحاول حفظ هذا التعبير في مصم تركيبة التقارير الإلكترونية ER، يتم طرح الاستثناء التالي: "خطأ التحقق من الصحة: تعبير القائمة للوظيفة FILTER غير قابل للاستعلام."</span><span class="sxs-lookup"><span data-stu-id="a8d03-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8d03-127">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a8d03-127">Additional resources</span></span>

[<span data-ttu-id="a8d03-128">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="a8d03-128">List functions</span></span>](er-functions-category-list.md)
