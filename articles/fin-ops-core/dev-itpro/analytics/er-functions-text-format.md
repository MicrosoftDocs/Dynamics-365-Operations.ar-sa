---
title: وظيفة FORMAT ER
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية FORMAT (ER).
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
ms.openlocfilehash: 8b347a7209ee543f6bd687c2864203eb632d6a4a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688403"
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
> - **للتسميات من موارد في تطبيق Microsoft Dynamics 365 Finance:** **\@X**، حيث **X** هو معرف التسمية في شجرة مكونات البرنامج (AOT)
> - **للتسميات المقيمة في تكوينات ER:** **@"GER_LABEL:X"** ، حيث **X** هو معرف التسمية في تكوين ER.

## <a name="additional-resources"></a>الموارد الإضافية

[الدالات النصية](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]