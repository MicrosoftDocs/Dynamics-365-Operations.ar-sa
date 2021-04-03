---
title: 'وظيفة VALUE ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية VALUE (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 7cdaa302e757b54858e36c3716167593383d7071
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561436"
---
# <a name="value-er-function"></a>وظيفة VALUE ER 

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `VALUE` قيمة *حقيقية* التي يتم تحويلها من قيمة السلسلة المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
VALUE (text)
```

## <a name="arguments"></a>الوسائط

`text`: *السلسلة*

قيمة سلسلة يجب تحويلها إلى قيمة رقمية.

## <a name="return-values"></a>إرجاع القيم

*حقيقي*

القيمة العددية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يتم اعتبار الفواصل وأحرف النقطة (.) كفواصل عشرية، ويتم استخدام الواصلة البادئة (-) كعلامة سالب. يتم طرح استثناء في وقت التشغيل إذا كانت السلسلة المُحددة تحتوي على أحرف غير رقمية أخرى.

## <a name="example-1"></a>مثال1

يطرح التعبير `VALUE ("1 234,56")` استثناء.

## <a name="example-2"></a>مثال2

يُرجع التعبير `VALUE ("1234,56")` **1234.56**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تحويل النوع](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]