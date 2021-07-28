---
title: الرسائل الإلكترونية
description: يوفر هذا الموضوع نظرة عامة حول المراسلات الإلكترونية في Microsoft Dynamics 365 Finance بالإضافة إلى معلومات الإعداد.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 339e0c811a70ca6b722d8967c2df103500578664
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433709"
---
# <a name="electronic-messaging"></a>المراسلة الإلكترونية

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع نظرة عامة ومعلومات الإعداد لوظائف **الرسائل الإلكترونية** (EM).

مؤخرًا، طبقت الحكومات والسلطات التشريعية للعديد من البلدان والمناطق في جميع أنحاء العالم متطلبات إعداد التقارير للشركات المٌسجّلة في تلك البلدان أو المناطق. ويتمثل الغرض من هذه المتطلبات في تمكين البيانات التي يتم الحصول عليها من تلك الشركات في تنسيق إلكتروني، مباشرةً من النظم التي يتم فيها حساب هذه البيانات وتخزينها ومعالجتها.

تدعم وظيفة الرسائل الإلكترونية في Microsoft Dynamics 365 Finance العمليات المختلفة للتشغيل الإلكتروني المتبادل بين Finance والنظم التي تقدمها الحكومات والسلطات التشريعية لإعداد التقارير وإرسالها واستلام المعلومات الرسمية.

تتكامل وظيفة الرسائل الإلكترونية (EM) مع وحدة **إعداد التقارير الإلكترونية** (ER). ويمكنك إعداد تنسيقات ER للرسائل الإلكترونية. للحصول على مزيد من التفاصيل، راجع [إعداد التقارير الإلكترونية (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>المفاهيم الأساسية لوظيفة EM

تستند وظيفة EM إلى الكيانات التالية:

- **الرسالة الإلكترونية** – تقرير أو إعلان يجب رفعه أو إرساله داخلياً، مثل تقرير يتم إرساله إلى مكتب الضرائب.
- **عناصر الرسائل الإلكترونية** -السجلات التي يجب تضمينها في الرسالة التي يتم الإبلاغ عنها.
- **معالجة الرسائل الإلكترونية** – سلسلة من الإجراءات يجب تشغيلها لجمع البيانات المطلوبة وإنشاء التقارير وتخزين البيانات في مخزن البيانات الثنائية كبيرة الحجم في Azure وإرسال تقارير من خارج النظام والحصول على الاستجابات من خارج النظام وتحديث قاعدة البيانات بناءً على المعلومات المستلمة. بإمكان الإجراءات الموجودة في السلسلة أن تكون مرتبطة أو غير مرتبطة.

يبين الرسم التوضيحي التالي تدفق بيانات لـ EM.

![تدفق بيانات الرسائل الإلكترونية.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>وحدات السيناريو المعتمدة في وظيفة EM

تدعم وظيفة EM السيناريوهات التالية:

- الإنشاء اليدوي لرسائل وتقارير تستند إلى تنسيقات تصدير ER مرتبطة من مختلف الأنواع. وتشمل هذه الأنواع Microsoft Excel وXML وJavaScript Object Notation (JSON) وPDF والنص وMicrosoft Word.
- الإنشاء والمعالجة التلقائية للرسائل التي تستند إلى المعلومات المطلوبة والتي تم استلامها من هيئة ما باستخدام تنسيق ER مقترن للاستيراد.
- تجميع المعلومات ومعالجتها من مصدر بيانات كعناصر للرسالة. مصدر البيانات هو جدول Finance.
- تخزين معلومات إضافية وتقييم قيم مختلفة عن طريق استدعاء فئات قابلة للتنفيذ مُعرفة بشكل خاص فيما يتعلق بالرسائل أو عناصر الرسائل.
- تجميع المعلومات المُجمّعة في عناصر الرسالة، وتقسيم هذه المعلومات بالرسالة وإنشاء تقارير في تنسيقات تصدير ER مقترنة.
- إرسال التقارير التي تم إنشاؤها إلى خدمة ويب باستخدام معلومات الأمان المُخزنة في Azure Key Vault.
- تلقي استجابة من خدمة الويب وتفسير الاستجابة وتحديث البيانات في Finance حسب الحاجة.
- تخزين جميع التقارير التي تم إنشاؤها ومراجعتها.
- تخزين ومراجعة جميع معلومات السجل المرتبطة بالإجراءات التي يتم تشغيلها لرسالة أو عنصر رسالة.
- التحكم في المعالجة من خلال العديد من حالات الرسائل المختلفة وحالات عناصر الرسالة

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>الميزات التنظيمية الخاصة بكل بلد مدعومة بوظيفة EM

يوفر الجدول التالي معلومات حول بعض الميزات التنظيمية الخاصة بكل بلد التي تدعمها وظيفة EM.

| الدولة     | اسم الميزة | ميزة تسجيل تجريبي |
|-------------|--------------|------------------------|
| إسبانيا       | [توفير فوري للمعلومات المتعلقة بضريبة القيمة المضافة (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| هنغاريا‬     | [نظام الفوترة عبر الإنترنت](../localizations/emea-hun-online-invoicing.md) | |
| المملكة المتحدة | [رقمنة الضرائب (MTD) – إرسال كشف حساب ضريبة القيمة المضافة](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: الضريبة الرقمية في المملكة المتحدة - إقرار ضريبة القيمة المضافة في Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| لتوانيا   | [تقارير i.SAF](../localizations/emea-ltu-isaf.md) | |
| بولندا      | [إقرار ضريبة القيمة المضافة مع السجلات (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: سجلات تدقيق SAF/JPK VAT](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| هولندا | [إقرار ضريبة القيمة المضافة لهولندا](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| جمهورية التشيك | [إقرار ضريبة القيمة المضافة](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| البرازيل      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| روسيا      | [إقرار ضريبة القيمة المضافة](../localizations/rus-vat-declaration.md) | |
| روسيا      | [التقارير المحاسبية بتنسيق إلكتروني](../localizations/rus-accounting-reporting.md) | |
| روسيا      | [إقرار ضريبة الربح](../localizations/rus-profit-tax-declaration.md) | |
| روسيا      | [إقرار الضرائب المقدّرة](../localizations/rus-assessed-tax-declaration.md) | |
| روسيا      | [إقرار ضريبة النقل](../localizations/rus-transport-tax-declaration.md) | |
| روسيا      | [إقرار ضريبة الأراضي‬](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

