---
title: نوع البريد الإلكتروني لوجهة إعداد التقارير الإلكترونية
description: يوفر هذا الموضوع معلومات حول كيفية تكوين وجهة بريد إلكتروني لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745551"
---
# <a name="email-destination"></a>وجهة البريد الإلكتروني

[!include [banner](../includes/banner.md)]

يمكنك تكوين وجهة بريد إلكتروني لكل مكون "ملف" أو "مجلد" لتنسيق إعداد التقارير الإلكترونية (ER) التي يتم تكوينها لإنشاء مستندات صادرة. واستنادًا إلى إعداد الوجهة، يتم تسليم المستند المنشأ كمرفق لبريد إلكتروني.

عيّن الخيار **ممكّن**إلى **نعم** لإرسال ملف المخرجات بواسطة البريد الإلكتروني. وبعد تمكين هذا الخيار، يمكنك تحديد مستلمي البريد الإلكتروني وتحرير الموضوع ونص رسالة البريد الإلكتروني. يمكنك إعداد نصوص ثابتة لموضوع البريد الإلكتروني والنص، أو يمكنك استخدام [معادلات](er-formula-language.md) إعداد التقارير الإلكترونية لإنشاء نصوص البريد الإلكتروني بطريقة ديناميكية. 

يمكنك تكوين عناوين البريد الإلكتروني للتقارير الإلكترونية بطريقتين. يمكن إكمال التكوين بنفس طريقة إكمال ميزة إدارة الطباعة لها، أو يمكنك حل عنوان بريد إلكتروني باستخدام مرجع مباشر لتكوين إعداد التقارير الإلكترونية من خلال إحدى المعادلات.

[![تمكين وجهة البريد الإلكتروني](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>أنواع عناوين البريد الإلكتروني

عند تحديد **تحرير** في الحقول **إلى** أو **نسخة**، يظهر مربع الحوار **بريد إلكتروني إلى**. ثم يمكنك تحديد نوع عنوان البريد الإلكتروني المُراد استخدامه. يحظى حاليًا نوعا البريد الإلكتروني **البريد الإلكتروني للتكوين** و**إدارة الطباعة** بالدعم.

[![تحديد نوع البريد الإلكتروني](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>إدارة الطباعة

عند تحديد نوع البريد الإلكتروني **إدارة الطباعة"**، يمكنك إدخال عناوين بريد إلكتروني ثابتة في حقل **إلى**. 

[![تكوين عناوين البريد الكتروني الثابتة](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

لاستخدام عناوين بريد إلكتروني غير ثابتة، يجب تحديد نوع مصدر البريد الإلكتروني لوجهة ملف. القيم التالية مدعومة: **العميل**، **المورد**، **عميل متوقع**، **جهة اتصال**، **المنافس**، **العامل**، **مقدم الطلب**، **المورد المتوقع**، و **مورد غير مسموح به**. بعد تحديد نوع مصدر البريد إلكتروني، استخدم الزر الموجود بجوار حقل **حساب مصدر البريد الإلكتروني** لفتح نموذج **مصمم المعادلة**. يمكنك استخدام هذا النموذج لإرفاق معادلة إرجاع في وقت التشغيل **، حساب الطرف** لنوع المصدر المحدد من المستند الذي تمت معالجته إلى وجهة البريد الإلكتروني.

[![تكوين حساب مصدر البريد الإلكتروني](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

تتعلق المعادلات بتكوين إعداد التقارير الإلكترونية. في حقل **المعادلة** أدخل مرجعًا خاصًا بالمستند إلى طرف من نوع عميل أو مورّد. بدلاً من الكتابة، يمكنك العثور على عقدة مصدر البيانات التي تمثل حساب العميل أو المورّد، ثم حدد الزر **إضافة مصدر البيانات** لتحديث المعادلة. على سبيل المثال، إذا كنت تستخدم تكوين **نقل الائتمان ISO 20022**، فإن العقدة التي تمثل حساب المورّد هي `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

عند إدخال قيمة سلسلة، مثل `"DE-001"`، وحفظ إحدى المعادلات، سيتم إرسال بريد إلكتروني إلى شخص جهة الاتصال بالمورد، **DE-001**.


[![صفحة مصمم معادلة إعداد التقارير الإلكترونية](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![تكوين حساب سمات مصدر البريد الإلكتروني](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>البريد الإلكتروني في التكوين

استخدم هذا النوع من البريد الإلكتروني إذا كان التكوين الذي تستخدمه به عقدة في مصادر البيانات التي ترجع **عنوان بريد إلكتروني**. يمكنك استخدام مصادر البيانات والوظائف في مصمم المعادلة للحصول على عنوان بريد إلكتروني منسق بشكل صحيح. على سبيل المثال، إذا كنت تستخدم تكوين **نقل الائتمان ISO 20022**، فإن العقدة التي تمثل عنوان البريد الإلكتروني لشخص جهة الاتصال بالمورد هي `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![تكوين مصدر عنوان البريد الإلكتروني](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)
- [وجهات إعداد التقارير الإلكترونية (ER)‬](electronic-reporting-destinations.md)
- [مصمم المعادلات في التقارير الإلكترونية](general-electronic-reporting-formula-designer.md)
