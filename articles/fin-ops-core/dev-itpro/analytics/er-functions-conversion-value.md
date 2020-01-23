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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917616"
---
# <span data-ttu-id="54d50-103"><a name="VALUE">وظيفة VALUE ER </a></span><span class="sxs-lookup"><span data-stu-id="54d50-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54d50-104">تُرجع الوظيفة `VALUE` قيمة *حقيقية* التي يتم تحويلها من قيمة السلسلة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="54d50-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d50-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="54d50-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="54d50-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="54d50-106">Arguments</span></span>

<span data-ttu-id="54d50-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="54d50-107">`text`: *String*</span></span>

<span data-ttu-id="54d50-108">قيمة سلسلة يجب تحويلها إلى قيمة رقمية.</span><span class="sxs-lookup"><span data-stu-id="54d50-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="54d50-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="54d50-109">Return values</span></span>

<span data-ttu-id="54d50-110">*حقيقي*</span><span class="sxs-lookup"><span data-stu-id="54d50-110">*Real*</span></span>

<span data-ttu-id="54d50-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="54d50-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="54d50-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="54d50-112">Usage notes</span></span>

<span data-ttu-id="54d50-113">يتم اعتبار الفواصل وأحرف النقطة (.) كفواصل عشرية، ويتم استخدام الواصلة البادئة (-) كعلامة سالب.</span><span class="sxs-lookup"><span data-stu-id="54d50-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="54d50-114">يتم طرح استثناء في وقت التشغيل إذا كانت السلسلة المُحددة تحتوي على أحرف غير رقمية أخرى.</span><span class="sxs-lookup"><span data-stu-id="54d50-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="54d50-115">مثال1</span><span class="sxs-lookup"><span data-stu-id="54d50-115">Example 1</span></span>

<span data-ttu-id="54d50-116">يطرح التعبير `VALUE ("1 234,56")` استثناء.</span><span class="sxs-lookup"><span data-stu-id="54d50-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="54d50-117">مثال2</span><span class="sxs-lookup"><span data-stu-id="54d50-117">Example 2</span></span>

<span data-ttu-id="54d50-118">يُرجع التعبير `VALUE ("1234,56")` **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="54d50-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54d50-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="54d50-119">Additional resources</span></span>

[<span data-ttu-id="54d50-120">وظائف تحويل النوع</span><span class="sxs-lookup"><span data-stu-id="54d50-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
