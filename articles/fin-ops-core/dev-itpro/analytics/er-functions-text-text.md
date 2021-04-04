---
title: TEXT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني TEXT (ER).
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560051"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]