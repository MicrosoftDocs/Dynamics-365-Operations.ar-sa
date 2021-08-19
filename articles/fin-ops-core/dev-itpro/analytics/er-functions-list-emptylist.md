---
title: EMPTYLIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني EMPTYLIST (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: fe2c72eddbb7f9227691ba29b19743c03aedfeb0d841e1a2466a159fa3afdf56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734782"
---
# <a name="emptylist-er-function"></a>EMPTYLIST ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `EMPTYLIST` قيمة *قائمة سجلات* فارغة باستخدام القائمة المُحددة كمصدر لبنية القائمة.

## <a name="syntax"></a>بناء الجملة

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `EMPTYLIST (SPLIT ("abc", 1))` قائمة فارغة جديدة لها نفس بنية القائمة المُرتجعة بواسطة وظيفة `SPLIT` المستخدمة.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]