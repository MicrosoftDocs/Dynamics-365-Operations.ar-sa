---
title: ALLITEMSQUERY ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ALLITEMSQUERY (ER).
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
ms.openlocfilehash: ed21252fbbe3d4adad106625062e10e3de712bb0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687734"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="ae401-103">ALLITEMSQUERY ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="ae401-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae401-104">تعمل الوظيفة `ALLITEMSQUERY` كاستعلام SQL مُنضم.</span><span class="sxs-lookup"><span data-stu-id="ae401-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="ae401-105">يقوم بإرجاع قيمة قيمة *قائمة السجلات* المٌسطحة التي تتكون من قائمة السجلات التي تمثل كافة العناصر التي تتطابق مع المسار المُحدد.</span><span class="sxs-lookup"><span data-stu-id="ae401-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae401-106">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="ae401-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="ae401-107">الوسائط</span><span class="sxs-lookup"><span data-stu-id="ae401-107">Arguments</span></span>

<span data-ttu-id="ae401-108">`path`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="ae401-108">`path`: *Record list*</span></span>

<span data-ttu-id="ae401-109">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="ae401-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="ae401-110">يجب أن يحتوي على علاقة واحدة على الأقل.</span><span class="sxs-lookup"><span data-stu-id="ae401-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="ae401-111">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="ae401-111">Return values</span></span>

<span data-ttu-id="ae401-112">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="ae401-112">*Record list*</span></span>

<span data-ttu-id="ae401-113">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="ae401-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ae401-114">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="ae401-114">Usage notes</span></span>

<span data-ttu-id="ae401-115">يجب تعريف المسار المُحدد كمسار مصدر بيانات صالح لعنصر مصدر بيانات لنوع بيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="ae401-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="ae401-116">يجب أن يحتوي أيضًا على علاقة واحدة على الأقل.</span><span class="sxs-lookup"><span data-stu-id="ae401-116">It must also contain at least one relation.</span></span> <span data-ttu-id="ae401-117">يجب أن تُظهر عناصر البيانات مثل *سلسلة* المسار و *التاريخ* خطأ في وقت التصميم في منشئ تعبير التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="ae401-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="ae401-118">عند تطبيق هذه وظيفة على مصادر البيانات من نوع بيانات *قائمة السجلات* التي تشير إلى كائن تطبيق يُمكن استدعائه مباشرة باستخدام SQL (على سبيل المثال، جدول أو كيان أو استعلام)، يتم تشغيله كاستعلام SQL مُنضم.</span><span class="sxs-lookup"><span data-stu-id="ae401-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="ae401-119">وإلا، يتم تشغيله في الذاكرة كوظيفة [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="ae401-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="ae401-120">مثال</span><span class="sxs-lookup"><span data-stu-id="ae401-120">Example</span></span>

<span data-ttu-id="ae401-121">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="ae401-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="ae401-122">مصدر بيانات **CustInv** من النوع *سجلات الجدول* الذي يُشير إلى جدول CustInvoiceTable. </span><span class="sxs-lookup"><span data-stu-id="ae401-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="ae401-123">مصدر بيانات **FilteredInv** من النوع *الحقل المحسوب* الذي يحتوي على التعبير `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="ae401-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="ae401-124">مصدر بيانات **JourLines** من النوع *الحقل المحسوب* الذي يحتوي على التعبير `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="ae401-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="ae401-125">عندما تقوم بتشغيل تعيين نموذج لطلب مصدر البيانات **JourLines**، فإنه يتم تشغيل عبارة SQL التالية:</span><span class="sxs-lookup"><span data-stu-id="ae401-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="ae401-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ae401-126">Additional resources</span></span>

[<span data-ttu-id="ae401-127">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="ae401-127">List functions</span></span>](er-functions-category-list.md)
