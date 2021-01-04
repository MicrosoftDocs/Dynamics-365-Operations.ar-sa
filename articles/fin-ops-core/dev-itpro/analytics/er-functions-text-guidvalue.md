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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685937"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="55251-103">وظيفة GUIDVALUE ER</span><span class="sxs-lookup"><span data-stu-id="55251-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55251-104">تقوم وظيفة `GUIDVALUE` بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.</span><span class="sxs-lookup"><span data-stu-id="55251-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="55251-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="55251-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="55251-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="55251-106">Arguments</span></span>

<span data-ttu-id="55251-107">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="55251-107">`input`: *String*</span></span>

<span data-ttu-id="55251-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="55251-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="55251-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="55251-109">Return values</span></span>

<span data-ttu-id="55251-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="55251-110">*GUID*</span></span>

<span data-ttu-id="55251-111">قيمه المعرف الفريد (GUID) الناتجة عالميًا.</span><span class="sxs-lookup"><span data-stu-id="55251-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="55251-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="55251-112">Usage notes</span></span>

<span data-ttu-id="55251-113">لإجراء تحويل في الاتجاه المعاكس (أي لتحويل المدخلات المحددة من نوع بيانات *GUID* إلى عنصر بيانات من نوع البيانات *سلسلة*)، يمكنك استخدام وظيفة [النص](er-functions-text-text.md) .</span><span class="sxs-lookup"><span data-stu-id="55251-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="55251-114">مثال</span><span class="sxs-lookup"><span data-stu-id="55251-114">Example</span></span>

<span data-ttu-id="55251-115">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="55251-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="55251-116">مصدر بيانات **myID** الخاص بنوع *الحقل المحسوب* الذي يحتوي على التعبير `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="55251-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="55251-117">مصدر بيانات **المستخدمين** من النوع *سجلات الجدول* الذي يُشير إلى جدول UserInfo.</span><span class="sxs-lookup"><span data-stu-id="55251-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="55251-118">يمكنك بعد ذلك استخدام تعبير مثل `FILTER (Users, Users.objectId = myID)` لتصفيه جدول معلومات المستخدم بواسطة الحقل **‎objectId‎** من نوع بيانات *GUID*.</span><span class="sxs-lookup"><span data-stu-id="55251-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55251-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="55251-119">Additional resources</span></span>

[<span data-ttu-id="55251-120">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="55251-120">Text functions</span></span>](er-functions-category-text.md)
