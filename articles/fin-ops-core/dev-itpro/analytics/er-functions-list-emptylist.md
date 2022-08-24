---
title: EMPTYLIST ER وظيفة
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكتروني EMPTYLIST‏ (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5fd14456a615d5dc6fb565f4bed523db5432c871
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268105"
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
