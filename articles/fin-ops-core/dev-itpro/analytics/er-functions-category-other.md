---
title: قائمة وظائف التقارير الإلكترونية في فئة خاصة بمجال الأعمال
description: توفر هذه المقالة معلومات عن الوظائف الخاصة بمجال الأعمال المعتمدة في التقارير الإلكترونية (ER).
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
ms.openlocfilehash: d9df826dcc0b672977d4d8af1feb985ab9a0ab7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879938"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>قائمة وظائف التقارير الإلكترونية في فئة خاصة بمجال الأعمال

[!include [banner](../includes/banner.md)]

يمكن استخدام الوظائف الخاصة بمجال إعداد التقارير الإلكترونية (ER) لتنفيذ العمليات الحسابية وطلبات الوصول إلى البيانات الخاصة بتنفيذ 365‎ Finance Microsoft Dynamics. توفر هذه المقالة ملخصًا لهذه الوظائف.

## <a name="list-of-supported-functions"></a>قائمة الوظائف المدعومة

| الوظيفة| ‏‏الوصف |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | تُرجع هذه الوظيفة قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD10، بناءً على أرقام رقم الفاتورة المُحددة. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | تُرجع هذه الوظيفة قيمة *سلسلة* تمثل مُعرف بعد مالي واحد مأخوذ من السلسلة المُحددة. تعرض السلسلة المُحددة كافة الأبعاد كقائمة مُعرفات مفصولة بفاصلة. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | تُرجع هذه الوظيفة قيمة *حقيقية* تمثل نتيجة تحويل المبلغ المالي المحدد من العملة المصدر المحددة إلى العملة الهدف المحددة باستخدام إعدادات الشركة المُحددة في التاريخ المُحدد. |
| [CurCredRef](er-functions-other-curcredref.md) | تُرجع هذه الوظيفة قيمة *سلسلة* تُمثل مرجع دائن، بناءً على أرقام رقم الفاتورة المُحددة. |
| [FA_Balance](er-functions-other-fabalance.md) | تُرجع هذه الوظيفة قيمة *حاوية (سجل)* تتكون من بيانات لرصيد الأصل الثابت لعنصر الأصل الثابت المُحدد وكود نموذج القيمة وسنة إعداد التقرير وتاريخ إعداد التقرير. |
| [FA_Sum](er-functions-other-fasum.md) | تُرجع هذه الوظيفة قيمة *حاوية (سجل)* تتكون من بيانات لمبالغ الأصول الثابتة لعنصر الأصل الثابت المُحدد وكود نموذج القيمة والفترات المرتبطة بالتواريخ. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل كود الكيان القانوني (الشركة) الذي يقوم مستخدم بتسجيل الدخول فيه حاليًا. |
| [ISOCredRef](er-functions-other-isocredref.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل مرجع دائن المنطقة العالمية للمواصفات (ISO)، استنادًا إلى الخامات الرقمية والرموز الأبجدية في رقم الفاتورة المُحددة. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | تُرجع هذه الوظيفة قيمة *منطقية* **TRUE** إذا كانت السلسلة المُحددة تمثل رقم حساب مصرفي دولي (IBAN) صالح. وبخلاف ذلك، تُرجع قيمة *منطقية* لـ **FALSE**. |
| [Mod_97](er-functions-other-mod97.md) | تُرجع هذه الوظيفة قيمة *سلسلة* تُمثل مرجع دائن كتعبير MOD97، بناءً على أرقام رقم الفاتورة المُحددة. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | تُرجع هذه الوظيفة قيمة *السلسلة* التي تمثل القيمة الجديدة التي تم إنشاؤها للتسلسل الرقمي، استنادًا إلى التسلسل الرقمي المُحدد والنطاق ومُعرف النطاق. يساوي مُعرف النطاق كود الشركة الذي يتم توفيره بواسطة السياق الذي يتم تشغيل تنسيق إعداد التقارير الإلكترونية ضمنه. |
| [RoundAmount](er-functions-other-roundamount.md) | تُرجع هذه الوظيفة قيمة *حقيقة* تمثل نتيجة تقريب المبلغ المُحدد إلى الرقم المُحدد من منازل عشرية وفقًا لقاعدة التقريب المُحددة. |
| [TableName2ID](er-functions-other-tablename2id.md) | تُرجع هذه الوظيفة تمثيل رقمي لمُعرف الجدول لاسم الجدول المُحدد كقيمة *عدد صحيح*. |

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة حول التقارير الإلكترونية](general-electronic-reporting.md)

[مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)

[لغة تركيبة التقارير الإلكترونية](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]