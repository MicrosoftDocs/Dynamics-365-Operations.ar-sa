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
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915684"
---
# <span data-ttu-id="83255-103"><a name="GUIDVALUE">وظيفة GUIDVALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="83255-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83255-104">تقوم وظيفة `GUIDVALUE` بتحويل الإدخال المُحدد لنوع *السلسلة* إلى عنصر بيانات من النوع *GUID*.</span><span class="sxs-lookup"><span data-stu-id="83255-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="83255-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="83255-105">Syntax</span></span>

```
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="83255-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="83255-106">Arguments</span></span>

<span data-ttu-id="83255-107">`input`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="83255-107">`input`: *String*</span></span>

<span data-ttu-id="83255-108">المسار الصالح لمصدر البيانات من نوع *السلسلة*.</span><span class="sxs-lookup"><span data-stu-id="83255-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="83255-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="83255-109">Return values</span></span>

<span data-ttu-id="83255-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="83255-110">*GUID*</span></span>

<span data-ttu-id="83255-111">قيمه المعرف الفريد (GUID) الناتجة عالميًا.</span><span class="sxs-lookup"><span data-stu-id="83255-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="83255-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="83255-112">Usage notes</span></span>

<span data-ttu-id="83255-113">لإجراء تحويل في الاتجاه المعاكس (أي لتحويل المدخلات المحددة من نوع بيانات *GUID* إلى عنصر بيانات من نوع البيانات *سلسلة*)، يمكنك استخدام وظيفة [النص](er-functions-text-text.md) .</span><span class="sxs-lookup"><span data-stu-id="83255-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="83255-114">مثال</span><span class="sxs-lookup"><span data-stu-id="83255-114">Example</span></span>

<span data-ttu-id="83255-115">أنت تحدد مصادر البيانات التالية في تعيين نموذج:</span><span class="sxs-lookup"><span data-stu-id="83255-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="83255-116">مصدر بيانات **myID** الخاص بنوع *الحقل المحسوب* الذي يحتوي على التعبير `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="83255-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="83255-117">مصدر بيانات **المستخدمين** من النوع *سجلات الجدول* الذي يُشير إلى جدول UserInfo.</span><span class="sxs-lookup"><span data-stu-id="83255-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="83255-118">يمكنك بعد ذلك استخدام تعبير مثل `FILTER (Users, Users.objectId = myID)` لتصفيه جدول معلومات المستخدم بواسطة الحقل **‎objectId‎** من نوع بيانات *GUID*.</span><span class="sxs-lookup"><span data-stu-id="83255-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83255-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="83255-119">Additional resources</span></span>

[<span data-ttu-id="83255-120">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="83255-120">Text functions</span></span>](er-functions-category-text.md)
