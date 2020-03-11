---
title: وظيفة GUIDVALUE ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية GUIDVALUE.
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041138"
---
# <span data-ttu-id="51ed6-103"><a name="GUIDVALUE">وظيفة GUIDVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="51ed6-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51ed6-104">تقوم وظيفة `GUIDVALUE` بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.</span><span class="sxs-lookup"><span data-stu-id="51ed6-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ed6-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="51ed6-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="51ed6-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="51ed6-106">Arguments</span></span>

<span data-ttu-id="51ed6-107">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="51ed6-107">`input`: *String*</span></span>

<span data-ttu-id="51ed6-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="51ed6-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="51ed6-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="51ed6-109">Return values</span></span>

<span data-ttu-id="51ed6-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="51ed6-110">*GUID*</span></span>

<span data-ttu-id="51ed6-111">قيمه المعرف الفريد (GUID) الناتجة عالميًا.</span><span class="sxs-lookup"><span data-stu-id="51ed6-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="51ed6-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="51ed6-112">Usage notes</span></span>

<span data-ttu-id="51ed6-113">لإجراء تحويل في الاتجاه المعاكس (أي لتحويل المدخلات المحددة من نوع بيانات *GUID* إلى عنصر بيانات من نوع البيانات *سلسلة*)، يمكنك استخدام وظيفة [النص](er-functions-text-text.md) .</span><span class="sxs-lookup"><span data-stu-id="51ed6-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="51ed6-114">مثال</span><span class="sxs-lookup"><span data-stu-id="51ed6-114">Example</span></span>

<span data-ttu-id="51ed6-115">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="51ed6-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="51ed6-116">مصدر بيانات **myID** الخاص بنوع *الحقل المحسوب* الذي يحتوي على التعبير `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="51ed6-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="51ed6-117">مصدر بيانات **المستخدمين** من النوع *سجلات الجدول* الذي يُشير إلى جدول UserInfo.</span><span class="sxs-lookup"><span data-stu-id="51ed6-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="51ed6-118">يمكنك بعد ذلك استخدام تعبير مثل `FILTER (Users, Users.objectId = myID)` لتصفيه جدول معلومات المستخدم بواسطة الحقل **‎objectId‎** من نوع بيانات *GUID*.</span><span class="sxs-lookup"><span data-stu-id="51ed6-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51ed6-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="51ed6-119">Additional resources</span></span>

[<span data-ttu-id="51ed6-120">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="51ed6-120">Text functions</span></span>](er-functions-category-text.md)
