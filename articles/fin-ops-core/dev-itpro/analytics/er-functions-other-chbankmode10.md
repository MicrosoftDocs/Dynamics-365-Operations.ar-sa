---
title: CH_BANK_MOD_10 ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية CH_BANK_MOD_10 (ER).
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915868"
---
# <a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER وظيفة</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `CH_BANK_MOD_10` قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD10، بناءً على أرقام رقم الفاتورة المُحددة.

## <a name="syntax"></a>بناء الجملة

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>الوسائط

`invoice number digits`: *السلسلة*

قيمة نصية تمثل الأرقام الخاصة برقم الفاتورة.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `CH_BANK_MOD_10 ("VEND-200002")` **3**.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات أخرى (خاصة بمجال الأعمال)](er-functions-category-other.md)
