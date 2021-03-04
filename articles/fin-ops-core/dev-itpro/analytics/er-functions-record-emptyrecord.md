---
title: 'وظيفة EMPTYRECORD ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية EMPTYRECORD (ER).
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684801"
---
# <a name="emptyrecord-er-function"></a>وظيفة EMPTYRECORD ER 

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `EMPTYRECORD` قيمة *حاوية (سجل)* فارغة لها نفس البنية كقائمة سجلات مُحددة أو سجل.

## <a name="syntax"></a>بناء الجملة

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة سجلات* أو *حاوية (سجل)*

مسار صالح لمصدر بيانات إما من النوع *قائمة السجلات* أو *حاوية (سجل)*.

## <a name="return-values"></a>إرجاع القيم

*حاوية (سجل)*

قيمة السجل الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

> [!NOTE] 
> سجل فارغ عبارة عن سجل تحتوي فيه جميع الحقول على قيمة فارغة. قيمة فارغة هي **0** (صفر) للأرقام، سلسلة فارغة للسلاسل، وهكذا.

## <a name="example"></a>مثال

يُرجع التعبير `EMPTYRECORD (SPLIT ("abc", 1))` سجل فارغ جديد له نفس بنية القائمة المُرتجعة بواسطة الوظيفة `SPLIT` . لمزيد من المعلومات، راجع [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف السجلات](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]