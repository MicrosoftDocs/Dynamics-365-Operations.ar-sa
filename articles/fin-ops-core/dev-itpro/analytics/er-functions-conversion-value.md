---
title: 'وظيفة VALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية VALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042609"
---
# <span data-ttu-id="5d987-103"><a name="VALUE">وظيفة VALUE ER </a></span><span class="sxs-lookup"><span data-stu-id="5d987-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d987-104">تُرجع الوظيفة `VALUE` قيمة *حقيقية* التي يتم تحويلها من قيمة السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="5d987-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d987-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="5d987-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="5d987-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="5d987-106">Arguments</span></span>

<span data-ttu-id="5d987-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="5d987-107">`text`: *String*</span></span>

<span data-ttu-id="5d987-108">قيمة سلسلة يجب تحويلها إلى قيمة رقمية.</span><span class="sxs-lookup"><span data-stu-id="5d987-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d987-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="5d987-109">Return values</span></span>

<span data-ttu-id="5d987-110">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="5d987-110">*Real*</span></span>

<span data-ttu-id="5d987-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="5d987-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5d987-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="5d987-112">Usage notes</span></span>

<span data-ttu-id="5d987-113">يتم اعتبار الفواصل وأحرف النقطة (.) كفواصل عشرية، ويتم استخدام الواصلة البادئة (-) كعلامة سالب.</span><span class="sxs-lookup"><span data-stu-id="5d987-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="5d987-114">يتم طرح استثناء في وقت التشغيل إذا كانت السلسلة المُحددة تحتوي على أحرف غير رقمية أخرى.</span><span class="sxs-lookup"><span data-stu-id="5d987-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="5d987-115">مثال1</span><span class="sxs-lookup"><span data-stu-id="5d987-115">Example 1</span></span>

<span data-ttu-id="5d987-116">يطرح التعبير `VALUE ("1 234,56")` استثناء.</span><span class="sxs-lookup"><span data-stu-id="5d987-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="5d987-117">مثال2</span><span class="sxs-lookup"><span data-stu-id="5d987-117">Example 2</span></span>

<span data-ttu-id="5d987-118">يُرجع التعبير `VALUE ("1234,56")` **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="5d987-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d987-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5d987-119">Additional resources</span></span>

[<span data-ttu-id="5d987-120">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="5d987-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
