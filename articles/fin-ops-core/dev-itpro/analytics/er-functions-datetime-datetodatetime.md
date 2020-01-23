---
title: وظيفة DATETODATETIME ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية DATETODATETIME (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916374"
---
# <a name="DATETODATETIME">وظيفة DATETODATETIME ER</a>

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `DATETODATETIME` قيمة *DateTime* يتم تحويلها من قيمة تاريخ مُعين إلى قيمة تاريخ/وقت بالتوقيت العالمي المنسق (توقيت جرينتش المتوسط \[GMT\]).

## <a name="syntax"></a>بناء الجملة

```
DATETODATETIME (date)
```

## <a name="arguments"></a>الوسائط

`date`: *التاريخ*

قيمة التاريخ التي تمثل التاريخ المُراد تحويله.

## <a name="return-values"></a>إرجاع القيم

*DateTime*

قيمة التاريخ/الوقت الناتجة.

## <a name="example-1"></a>مثال1

يُرجع `DATETODATETIME (CompInfo. 'getCurrentDate()')` تاريخ جلسة Microsoft Dynamics 365 Finance الحالية، 24 ديسمبر 2015، على الشكل التالي **12/24/2015 12:00:00 AM**.  في هذا المثال، **CompInfo** عبارة عن مصدر بيانات تقارير إلكترونية (ER) من النوع **Finance and Operations/جدول** ، ويشير إلى جدول CompanyInfo.

## <a name="example-2"></a>مثال2

يُرجع `DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` قيمة التاريخ/الوقت **11/12/2019 12:00:00 AM**. 

## <a name="additional-resources"></a>الموارد الإضافية

[دلات التاريخ والوقت](er-functions-category-datetime.md)
