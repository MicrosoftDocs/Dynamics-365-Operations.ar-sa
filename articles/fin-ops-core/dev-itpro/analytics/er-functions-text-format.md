---
title: وظيفة FORMAT ER
description: توفر هذه المقالة معلومات عن كيفية استخدام وظيفة إعداد التقارير الإلكترونية FORMAT‏ (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: a7eb3d4a4c72e8faf40d28a724cda5ba7d7e8a47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285988"
---
# <a name="format-er-function"></a>وظيفة FORMAT ER

[!include [banner](../includes/banner.md)]

تُرجع الوظيفة `FORMAT` السلسلة المُحددة كقيمة *سلسلة* بعد أن تم تنسيقها باستبدال أي تواجد من **%N** بالوسيطة *N*.

## <a name="syntax"></a>بناء الجملة

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>الوسائط

`string`: *السلسلة*

مرجع إلى مصدر البيانات من نوع *السلسلة* التي يجب تنسيقها. هذه الوسيطة مطلوبة.

`argument 1`: *السلسلة*

الوسيطة الأولى، المستخدمة لاستبدال مرات حدوث **%1**. هذه الوسيطة مطلوبة.

`argument N`: *السلسلة*

الوسيطة *N* ، المستخدمة لاستبدال مرات الحدوث من **%2** و **%3** وغيرها. هذه الوسائط الإضافية اختيارية.

## <a name="return-values"></a>إرجاع القيم

*السلسلة*

القيمة النصية الناتجة.

## <a name="usage-notes"></a>ملاحظات الاستخدام

إذا لم يتم توفير وسيطة لمعلمة، فسيتم إرجاع المعلمة على الشكل **"% N"** في السلسلة. بالنسبة إلى القيم من النوع *الحقيقي*، تتحدد سلسلة التحويل الافتراضية بمنزلتين عشريتين.

## <a name="example"></a>مثال

في الرسم التوضيحي التالي، يُرجع مصدر البيانات **PaymentModel** قائمة سجلات العُملاء باستخدام مكون **العميل**. يقوم بإرجاع قيمة تاريخ المُعالجة باستخدام الحقل **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

في تنسيق التقارير الإلكترونية (ER) المصمم لإنشاء ملف إلكتروني لعملاء معينين، يتم تحديد **PaymentModel** كمصدر بيانات ويتحكم بسير العملية. عند إيقاف عميل محدد للتاريخ عندما تتم معالجة التقرير، يتم طرح استثناء لإبلاغ المستخدم.  باستطاعة المعادلة المصممة لنوع التحكم بالمعالجة هذا استخدام الموارد التالية:

- تسمية SYS70894، التي تتضمن النص التالي:

    - **للغة الإنجليزية-الولايات المتحدة:** "Nothing to print"
    - **للغة الألمانية:** "Nichts zu drucken"

- تسمية SYS18389، التي تتضمن النص التالي:

    - **بالنسبة إلى اللغة EN-US:** يتم وقف "العميل %1 لـ %2.
    - **بالنسبة للغة الألمانية:** "الدائن%1wird für %2 gesperrt." 

هذا هو التعبير التي يمكن تصميمه.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

إذا تمت معالجة تقرير العميل **Litware Retail** في 17 ديسمبر 2015 بالثقافة **الإنجليزية-الولايات المتحدة** واللغة **الإنجليزية-الولايات المتحدة** فإن هذه المعادلة سترجع النص التالي الذي يمكن تقديمه كرسالة استثناء:

*لا توجد عناصر لطباعتها. العميل Litware Retail موقوف للتاريخ 12/17/2015‎*.

إذا تمت معالجة التقرير نفسه لعميل **Litware Retail** في 17 ديسمبر 2015، بالثقافة **الألمانية** واللغة **الألمانية**، فإن هذه المعادلة ترجع النص التالي الذي يستخدم تنسيق تاريخ آخر:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> يتم تطبيق بناء الجملة التالي في معادلات التقارير الإلكترونية للتسميات:
>
> - **للتسميات من الموارد في تطبيق 365‎ Finance Microsoft Dynamics:** **\@X**، حيث **X** هو معرف التسمية في شجرة مكونات البرنامج (AOT)
> - **للتسميات المقيمة في تكوينات ER:** **@"GER_LABEL:X"** ، حيث **X** هو معرف التسمية في تكوين ER.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
