---
title: ALLITEMS ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ALLITEMS (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559214"
---
# <a name="allitems-er-function"></a><span data-ttu-id="9e4dd-103">ALLITEMS ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="9e4dd-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e4dd-104">تعمل وظيفة `ALLITEMS` كمجموعة في الذاكرة وتُرجع قيمة *قائمة سجلات* مُدمجة جديدة كقائمة من السجلات التي تمثل كافة العناصر التي تتطابق مع المسار المُحدد.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e4dd-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="9e4dd-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="9e4dd-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="9e4dd-106">Arguments</span></span>

<span data-ttu-id="9e4dd-107">`path`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="9e4dd-107">`path`: *Record list*</span></span>

<span data-ttu-id="9e4dd-108">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e4dd-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="9e4dd-109">Return values</span></span>

<span data-ttu-id="9e4dd-110">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="9e4dd-110">*Record list*</span></span>

<span data-ttu-id="9e4dd-111">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9e4dd-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="9e4dd-112">Usage notes</span></span>

<span data-ttu-id="9e4dd-113">يجب تحديد المسار كمسار مصدر بيانات صالح لعنصر مصدر بيانات لنوع بيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="9e4dd-114">يجب أن تُظهر عناصر البيانات مثل سلسلة المسار والتاريخ خطأ في وقت التصميم في منشئ تعبير التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="9e4dd-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="9e4dd-115">لا نوصي باستخدام هذه وظيفة لمصادر البيانات التعاملية التي قد تحتوي على مقدار كبير من البيانات.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="9e4dd-116">بدلًا من ذلك، ضع في اعتبارك استخدام وظيفة [ALLTEMSQUERY](er-functions-list-allitemsquery.md). </span><span class="sxs-lookup"><span data-stu-id="9e4dd-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="9e4dd-117">مثال1</span><span class="sxs-lookup"><span data-stu-id="9e4dd-117">Example 1</span></span>

<span data-ttu-id="9e4dd-118">إذا قمت بإدخال `SPLIT("abcdef" , 2)` كمصدر بيانات **DS**، يُرجع التعبير `COUNT( ALLITEMS (DS))` **3**.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9e4dd-119">مثال2</span><span class="sxs-lookup"><span data-stu-id="9e4dd-119">Example 2</span></span>

<span data-ttu-id="9e4dd-120">إذا قمت بإدخال **Vend** كمصدر بيانات لنوع البيانات *قائمة السجلات* التي تشير إلى جدول تطبيق VendTable، يُرجع التعبير `ALLITEMS (Vend.'<Relations'.ContactPerson)` قائمة سجلات مُسطحة تحتوي على بنية جدول **ContactPerson** وتحتوي على كافة جهات الاتصال التي يُمكن الوصول إليها باستخدام العلاقة **ContactPerson.ContactForParty == VendTable.Party**، والمتاحة لجميع الموردين من جدول الموردين المرجعي.</span><span class="sxs-lookup"><span data-stu-id="9e4dd-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e4dd-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9e4dd-121">Additional resources</span></span>

[<span data-ttu-id="9e4dd-122">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="9e4dd-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]