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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041367"
---
# <span data-ttu-id="97100-103"><a name="ISOCREDREF">ISOCREDREF ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="97100-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97100-104">تُرجع الوظيفة `ISOCREDREF` قيمة *سلسلة* تمثل مرجع دائن المنطقة العالمية للمواصفات (ISO)، استنادًا إلى الخامات الرقمية والرموز الأبجدية في رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="97100-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="97100-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="97100-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="97100-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="97100-106">Arguments</span></span>

<span data-ttu-id="97100-107">`invoice number digits`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="97100-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="97100-108">قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="97100-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="97100-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="97100-109">Return values</span></span>

<span data-ttu-id="97100-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="97100-110">*String*</span></span>

<span data-ttu-id="97100-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="97100-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97100-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="97100-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="97100-113">لإزالة الرموز من الحروف الأبجدية غير المتوافقة مع ISO، يجب ترجمة الوسيطة `invoice number digits` قبل أن يتم تمريرها إلى هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="97100-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="97100-114">مثال</span><span class="sxs-lookup"><span data-stu-id="97100-114">Example</span></span>

<span data-ttu-id="97100-115">يُرجع التعبير `ISOCredRef ("VEND-200002")` **"RF23VEND-200002"**. </span><span class="sxs-lookup"><span data-stu-id="97100-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97100-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="97100-116">Additional resources</span></span>

[<span data-ttu-id="97100-117">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="97100-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
