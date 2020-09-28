---
title: TEXT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TEXT (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743678"
---
# <a name="text-er-function"></a>TEXT ER وظيفة

[!include [banner](../includes/banner.md)]

تُرجع وظيفة `TEXT` الرقم المُحدد كقيمة *سلسلة* بعد أن يتم تحويله إلى سلسلة نصية يتم تنسيقها وفقًا لإعدادات الخادم المحلية لمثيل التطبيق الحالي.

## <a name="syntax"></a>بناء الجملة

```vb
TEXT (number)
```

## <a name="arguments"></a>الوسائط

`number`: *عدد صحيح* أو *حقيقي*

رقم يجب تحويله إلى سلسلة نصية.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

بالنسبة إلى القيم من النوع *الحقيقي*، تتحدد سلسلة التحويل بمنزلتين عشريتين.

## <a name="example"></a>مثال

إذا كانت إعدادات الخادم المحلية لمثيل Microsoft Dynamics 365 Finance معرفة على الشكل **EN-US**، يُرجع التعبير `TEXT (NOW ())` تاريخ جلسة عمل التطبيق الحالية، 17 ديسمبر 2015، على شكل السلسلة النصية **"12/17/2015 07:59:23 AM"**. يُرجع التعبير `TEXT (1/3)` **"0.33"**.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)
