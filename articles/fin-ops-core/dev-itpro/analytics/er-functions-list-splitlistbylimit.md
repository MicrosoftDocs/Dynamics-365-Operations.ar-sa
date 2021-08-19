---
title: SPLITLISTBYLIMIT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLITLISTBYLIMIT (ER).
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 52351c131480119ce9fb98a75307ebf6026cb12b9977e8b4236d3a24ef6a140e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744424"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER وظيفة

[!include [banner](../includes/banner.md)]

تقسم الوظيفة `SPLITLISTBYLIMIT` القائمة المُحددة إلى قائمة جديدة من القوائم الفرعية (دفعات). يتم حساب عدد السجلات في كل دفعة بشكل ديناميكي. ثم تُرجع الوظيفة النتيجة كقيمة *قائمة سجلات* جديدة التي تتكون من الدفعات.

## <a name="syntax"></a>بناء الجملة

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>الوسائط

`list`: *قائمة السجلات*

مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.

`limit value`: *عدد صحيح* أو *حقيقي*

الحد الأقصى لقيمة الحد المستخدم لتقسيم القائمة الأصلية إلى دفعات.

`limit source`: *الحقل*

المسار الصالح لحقل من النوع *عدد صحيح* أو *حقيقي* في القائمة المُحددة. تُحدد قيمة هذا الحقل الخطوة التي يتم فيها زيادة إجمالي المجموع.

## <a name="return-values"></a>إرجاع القيم

*قائمة السجلات*

قائمة السجلات الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

تحتوي قائمة الدفعات التي تم إرجاعها على العناصر التالية:

- **القيمة**: *القائمة*

    قائمة السجلات التي تخص الدفعة الحالية.

- **BatchNumber**: *عدد صحيح*

    عدد الدفعات الحالية في القائمة المُرتجعة.

لا يتم تطبيق الحد على صنف واحد من القائمة الأصلية عندما يقوم مصدر الحد بتجاوز الحد المعرّف.

## <a name="example"></a>مثال

يوضح الرسم التوضيحي التالي تنسيق التقارير الإلكترونية (ER).

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

يبين الرسم التوضيحي التالي مصادر البيانات التي يتم استخدامها للتنسيق.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق. في هذه الحالة، الإخراج عبارة عن قائمة مسطحة بأصناف السلع.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

في الرسوم التوضيحية التالية، تم تعديل التنسيق نفسه بحيث يقدم قائمة أصناف السلع في دُفعات إذا كانت الدفعة الواحدة يجب أن تتضمن سلعًا ويجب ألا يتجاوز الوزن الإجمالي الحد 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المعدَّل.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> لا يتم تطبيق الحد على الصنف الأخير من القائمة الأصلية لأن القيمة (**11**) لمصدر الحد (**الوزن**) تتجاوز الحد المُعرف (**9**). لتجاهل القوائم الفرعية خلال إنشاء التقرير، استخدم إما وظيفة `WHERE` أو تعبير **مُمكّن** لعنصر التنسيق المناظر، عند الحاجة.

## <a name="additional-resources"></a>الموارد الإضافية

[دالات القائمة](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]