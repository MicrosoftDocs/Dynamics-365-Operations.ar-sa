---
title: TABLENAME2ID ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية TABLENAME2ID (ER).
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915799"
---
# <span data-ttu-id="90660-103"><a name="TABLENAME2ID">TABLENAME2ID ER وظيفة</a></span><span class="sxs-lookup"><span data-stu-id="90660-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90660-104">تُرجع الوظيفة `TABLENAME2ID` تمثيل رقمي لمُعرف الجدول لاسم الجدول المُحدد كقيمة *عدد صحيح*.</span><span class="sxs-lookup"><span data-stu-id="90660-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="90660-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="90660-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="90660-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="90660-106">Arguments</span></span>

<span data-ttu-id="90660-107">`text`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="90660-107">`text`: *String*</span></span>

<span data-ttu-id="90660-108">قيمة نصية تمثل اسم جدول صالح.</span><span class="sxs-lookup"><span data-stu-id="90660-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="90660-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="90660-109">Return values</span></span>

<span data-ttu-id="90660-110">*عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="90660-110">*Integer*</span></span>

<span data-ttu-id="90660-111">القيمة العددية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="90660-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="90660-112">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="90660-112">Usage notes</span></span>

<span data-ttu-id="90660-113">يُمكن أن ينتج عن تنفيذ هذه الوظيفة نتائج مختلفة في مثيلات مختلفة من  Microsoft Dynamics 365 Finance ، حتى إذا تم استخدام نفس اسم الشركة.</span><span class="sxs-lookup"><span data-stu-id="90660-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="90660-114">مثال</span><span class="sxs-lookup"><span data-stu-id="90660-114">Example</span></span>

<span data-ttu-id="90660-115">يُرجع التعبير `TABLENAME2ID ("Intrastat")` **1510**.</span><span class="sxs-lookup"><span data-stu-id="90660-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90660-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="90660-116">Additional resources</span></span>

[<span data-ttu-id="90660-117">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="90660-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
