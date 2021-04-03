---
title: MOD_97 ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني MOD_97 (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 618cb2b101dd0b1c91b3b1538ef3f87c21e4a70a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563332"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="8e052-103">MOD_97 ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="8e052-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e052-104">تُرجع الوظيفة `MOD_97` قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD97، بناءً على أرقام رقم الفاتورة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="8e052-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e052-105">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="8e052-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="8e052-106">الوسائط</span><span class="sxs-lookup"><span data-stu-id="8e052-106">Arguments</span></span>

<span data-ttu-id="8e052-107">`invoice number digits`: *السلسلة*</span><span class="sxs-lookup"><span data-stu-id="8e052-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="8e052-108">قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="8e052-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="8e052-109">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="8e052-109">Return values</span></span>

<span data-ttu-id="8e052-110">*السلسلة*</span><span class="sxs-lookup"><span data-stu-id="8e052-110">*String*</span></span>

<span data-ttu-id="8e052-111">القيمة النصية الناتجة.</span><span class="sxs-lookup"><span data-stu-id="8e052-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8e052-112">مثال</span><span class="sxs-lookup"><span data-stu-id="8e052-112">Example</span></span>

<span data-ttu-id="8e052-113">يُرجع التعبير `MOD_97 ("VEND-200002")` **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="8e052-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e052-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8e052-114">Additional resources</span></span>

[<span data-ttu-id="8e052-115">دالات أخرى (خاصة بمجال الأعمال)</span><span class="sxs-lookup"><span data-stu-id="8e052-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]