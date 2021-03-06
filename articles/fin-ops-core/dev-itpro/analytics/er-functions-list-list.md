---
title: LIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية LIST (ER).
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
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683077"
---
# <a name="list-er-function"></a>LIST ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `LIST` قيمة *قائمة سجلات* جديدة تتكون من قائمة سجلات جديدة تم إنشاءها من الوسيطات المُحددة.

## <a name="syntax"></a>بناء الجملة

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>الوسائط

`record 1`: *حاوية (سجل)*

مرجع إلى مصدر البيانات من نوع بيانات *السجل*. هذه الوسيطة مطلوبة.

`record N`: *حاوية (سجل)*

مرجع إلى مصدر البيانات من نوع بيانات *السجل*. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تحتوي بنية القائمة التي تم إنشائها فقط على الحقول التي يتم عرضها في البنية لكل سجل مذكور في الوسيطات.

## <a name="example"></a>مثال

قم بإدخال مصدر البيانات **السجل 1** من النوع *الحاوية*. يحتوي مصدر البيانات هذا على الحقول المتداخلة من النوع *الحقل المحسوب*:

- **الرمز:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *السلسلة*.
- **المقدار:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *الحقيقي*.

يُمكنك بعدها إدخال مصدر البيانات **السجل 2** من نوع *الحاوية*. يحتوي مصدر البيانات هذا على الحقول المتداخلة من النوع *الحقل المحسوب*:

- **المقدار:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *الحقيقي*.
- **IsValid:** يحتوي هذا الحقل على تعبيرًا يُرجع قيمة من النوع *المنطقي*.

في هذه الحالة، يُرجع التعبير `LIST('Record 1', 'Record 2')` قائمة جديدة تحتوي على سجلين. تتكون بنية هذه القائمة من حقل **مبلغ** واحد من النوع *الحقيقي* ، لأن هذا الحقل هو الحقل الوحيد الذي يتم عرضه في كل وسطية من الوظيفة التي تم استدعاءها.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]