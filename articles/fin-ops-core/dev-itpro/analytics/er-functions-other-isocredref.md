---
title: ISOCREDREF ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني ISOCREDREF (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744085"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="8379c-103">ISOCREDREF ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="8379c-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8379c-104">تُرجع الوظيفة `ISOCREDREF` قيمة *سلسلة* تمثل مرجع دائن المنطقة العالمية للمواصفات (ISO)، استنادًا إلى الخامات الرقمية والرموز الأبجدية في رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="8379c-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8379c-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="8379c-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8379c-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="8379c-106">Arguments</span></span>

<span data-ttu-id="8379c-107">`invoice number digits`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="8379c-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8379c-108">قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8379c-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8379c-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="8379c-109">Return values</span></span>

<span data-ttu-id="8379c-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="8379c-110">*String*</span></span>

<span data-ttu-id="8379c-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="8379c-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8379c-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="8379c-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="8379c-113">لإزالة الرموز من الحروف الأبجدية غير المتوافقة مع ISO، يجب ترجمة الوسيطة `invoice number digits` قبل أن يتم تمريرها إلى هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="8379c-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="8379c-114">مثال</span><span class="sxs-lookup"><span data-stu-id="8379c-114">Example</span></span>

<span data-ttu-id="8379c-115">يُرجع التعبير `ISOCredRef ("VEND-200002")` **"RF23VEND-200002"**. </span><span class="sxs-lookup"><span data-stu-id="8379c-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8379c-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8379c-116">Additional resources</span></span>

[<span data-ttu-id="8379c-117">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="8379c-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
