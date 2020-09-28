---
title: 'وظيفة FORMATELEMENTNAME ER '
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكتروني FORMATELEMENTNAME (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745623"
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
