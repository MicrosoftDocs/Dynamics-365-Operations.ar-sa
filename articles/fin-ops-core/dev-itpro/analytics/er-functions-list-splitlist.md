---
title: SPLITLIST ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLITLIST (ER).
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744781"
---
# <a name="splitlist-er-function"></a>SPLITLIST ER وظيفة

[!include [banner](../includes/banner.md)]

تقسم الوظيفة `SPLITLIST` القائمة المُحددة إلى قوائم فرعية (أو دفعات)، تحتوي كل واحدة منها على العدد المُحدد من السجلات. ثم يقوم بإرجاع النتيجة كقيمة *قائمة سجلات* جديدة التي تتكون من الدفعات.

## <a name="syntax"></a>بناء الجملة

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`number`: *عدد صحيح*

أقصى عدد للسجلات لكل دفعة.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تحتوي قائمة الدفعات التي تم إرجاعها على العناصر التالية:

 - **القيمة:** *القائمة*

    قائمة السجلات التي تخص الدفعة الحالية.

- **BatchNumber:** *عدد صحيح*

    عدد الدفعات الحالية في القائمة المُرتجعة.

## <a name="example"></a>مثال

في الرسم التوضيح التالي، يتم إنشاء مصدر بيانات **الخطوط** كقائمة سجلات تحتوي على ثلاث سجلات. يتم تقسيم هذه القائمة إلى دُفعات، يحتوي كل منها على ما يصل إلى سجلين.

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

يبين الرسم التوضيحي التالي تخطيط التنسيق المصمم. في تخطيط التنسيق هذا، يتم إنشاء عمليات الربط إلى مصدر بيانات **الخطوط** لإنشاء إخراج بتنسيق XML. يقدم هذا الإخراج عقدًا فردية لكل دُفعة والسجلات التي فيها.

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المصمم.

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)
