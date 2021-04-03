---
title: COUNT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني COUNT (ER).
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567882"
---
# <a name="count-er-function"></a>COUNT ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `COUNT` قيمة *عدد صحيح* تمثل عدد السجلات في القائمة المحددة، إذا لم تكن القائمة فارغة. إذا كانت القائمة فارغة، تُرجع هذه وظيفة القيمة **0** (صفر).

## <a name="syntax"></a>بناء الجملة

```vb
COUNT (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

## <a name="return-values"></a>إرجاع القيم

*عدد صحيح*

القيمة العددية الناتجة.

## <a name="example"></a>مثال

يُرجع التعبير `COUNT (SPLIT("abcd" , 3))` **2** ، لأن وظيفة `SPLIT` المستخدمة في هذا المثال تقوم بإنشاء قائمة تتكون من سجلين.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]