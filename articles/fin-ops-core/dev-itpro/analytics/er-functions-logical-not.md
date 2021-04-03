---
title: NOT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني NOT (ER).
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565870"
---
# <a name="not-er-function"></a>NOT ER وظيفة

[!include [banner](../includes/banner.md)]

ترجع الوظيفة `NOT` القيمة المنطقية المعكوسة للشرط المُحدد كقيمة *منطقية*.

## <a name="syntax"></a>بناء الجملة

```vb
NOT (condition)
```

## <a name="arguments"></a>الوسائط

`condition`: *منطقي*

تعبير شرطي صالح يجب عكسه.

## <a name="return-values"></a>إرجاع القيم

*منطقي*

القيمة *المنطقية* الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `NOT (TRUE)` **FALSE**.

## <a name="additional-resources"></a>الموارد الإضافية

[الوظائف المنطقية](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]