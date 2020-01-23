---
title: TEXT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TEXT (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c26d0c4c8c6290bd2dbb10a288bbd59941a8d98e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915546"
---
# <span data-ttu-id="2492d-103"><a name="TEXT">TEXT ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="2492d-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2492d-104">تُرجع وظيفة `TEXT` الرقم المُحدد كقيمة *سلسلة* بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي.</span><span class="sxs-lookup"><span data-stu-id="2492d-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="2492d-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="2492d-105">Syntax</span></span>

```
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="2492d-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="2492d-106">Arguments</span></span>

<span data-ttu-id="2492d-107">`number`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="2492d-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="2492d-108">رقم يجب تحويله إلى سلسلة نصية.</span><span class="sxs-lookup"><span data-stu-id="2492d-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="2492d-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="2492d-109">Return values</span></span>

<span data-ttu-id="2492d-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="2492d-110">*String*</span></span>

<span data-ttu-id="2492d-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="2492d-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2492d-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="2492d-112">Usage notes</span></span>

<span data-ttu-id="2492d-113">بالنسبة إلى القيم من النوع *الحقيقي*، تتحدد سلسلة التحويل بمنزلتين عشريتين.</span><span class="sxs-lookup"><span data-stu-id="2492d-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="2492d-114">مثال</span><span class="sxs-lookup"><span data-stu-id="2492d-114">Example</span></span>

<span data-ttu-id="2492d-115">إذا كانت إعدادات الخادم المحلية لمثيل Microsoft Dynamics 365 Finance معرفة على الشكل **EN-US**، يُرجع التعبير `TEXT (NOW ())` تاريخ جلسة عمل التطبيق الحالية، 17 ديسمبر 2015، على شكل السلسلة النصية **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="2492d-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="2492d-116">يُرجع التعبير `TEXT (1/3)` **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="2492d-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2492d-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="2492d-117">Additional resources</span></span>

[<span data-ttu-id="2492d-118">الدالات النصية</span><span class="sxs-lookup"><span data-stu-id="2492d-118">Text functions</span></span>](er-functions-category-text.md)
