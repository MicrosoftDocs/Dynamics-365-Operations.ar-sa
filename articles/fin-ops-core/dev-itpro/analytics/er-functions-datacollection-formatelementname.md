---
title: وظيفة FORMATELEMENTNAME ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية FORMATELEMENTNAME‏ (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0a733c3c70cede6395b3d7454d82ce4d999e7e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851969"
---
# <a name="formatelementname-er-function"></a>وظيفة FORMATELEMENTNAME ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `FORMATELEMENTNAME` قيمة *السلسلة* التي تمثل اسم عنصر تنسيق التقارير الإلكترونية (ER) الحالي.

## <a name="syntax"></a>بناء الجملة

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

يُمكن استدعاء هذه الوظيفة في تعبيرات ER التي تم تكوينها لخصائص **اسم مفتاح البيانات المُجمّعة** و **قيمة مفتاح البيانات المُجمعة** لمكون تنسيق ER من مجموعة **النص** الموجودة الموجودة ضمن مكون **ملف\\شائع** حيث يتم تشغيل خيار **تجميع تفاصيل المُخرجات**.

## <a name="example"></a>مثال

لمزيد من المعلومات حول كيفية استخدام هذه الوظيفة، راجع دليل المهام [التقارير الإلكترونية - استخدام بيانات مخرجات التنسيق لعمليات الجرد والتجميع](tasks/er-format-counting-summing-1.md) جزء من عملية الأعمال **اكتساب/تطوير خدمة تكنولوجيا المعلومات/مكونات الحلول**.

## <a name="additional-resources"></a>الموارد الإضافية

[وظائف تجميع البيانات](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]