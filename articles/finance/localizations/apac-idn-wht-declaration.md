---
title: تقرير ضريبة الخصم لإندونيسيا
description: يشرح هذا الموضوع كيفية تكوين وإنشاء تقرير ضريبة الخصم لإندونيسيا.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6cf2f9240ea747054578c52343af34b15c250f38
ms.sourcegitcommit: f51e74ee9162fe2b63c6ce236e514840795acfe1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943651"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>تقرير ضريبة الخصم لإندونيسيا (ID-00005)

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية إعداد وإنشاء ملف ضريبة الخصم PPH الذي تستخدمه الكيانات القانونية في إندونيسيا للإبلاغ عن حركات الخصم في تطبيق e-Bupot.

تحدد مصلحة الضرائب الإندونيسية (DGT) أن رواد الأعمال الخاضعين للضريبة (PKP) المسجلين في KPP Pratama باعتبارهم حاملي الضرائب/محصلي ضريبة الدخل (PPh) المادة 23 و/أو المادة 26 يجب أن يقدموا تقريرًا إلكترونيًا عن إقرار ضريبة الدخل المادتين 23 و26 باستخدام تطبيق e-Bupot. 

- **المادة 23** – يتضمن التقرير جميع معاملات الاقتطاع الضريبي من البائعين حيث يكون رمز البلد / المنطقة الخاص بالعنوان الأساسي هو رمز إندونيسيا.
- **المادة 26** – يتضمن التقرير جميع معاملات الاقتطاع الضريبي من البائعين حيث لا يكون رمز البلد / المنطقة الخاص بالعنوان الأساسي هو رمز إندونيسيا.

## <a name="prerequisites"></a>المتطلبات الأساسية

- يجب أن يكون العنوان الرئيسي للكيان القانوني في إندونيسيا.
- في مساحة عمل **إدارة الميزات**، يجب تمكين ميزة **ضريبة الخصم العمومية**. لمزيد من المعلومات حول كيفية تمكين الميزات، راجع [نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="download-electronic-reporting-configurations"></a>تنزيل تكوينات إعداد التقارير الإلكترونية

يعتمد إنشاء ملف الاستيراد على تكوينات التقارير الإلكترونية (ER). لمزيد من المعلومات حول إمكانات ومفاهيم التقارير القابلة للتكوين، راجع [إعداد التقارير الإلكترونية](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

بالنسبة لبيئات اختبار قبول الإنتاج والمستخدم (UAT)، اتبع التعليمات الموجودة في[تنزيل تكوينات إعداد التقارير الإلكترونية من Lifecycle Services‬‏‫](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

لإنشاء ملف الاستيراد، قم بتحميل التكوينات التالية من المستودع:

- **نموذج الإقرار الضريبي .version.93.xml** أو إصدار أحدث
- **نموذج الإقرار الضريبي mapping.version.93.153.xml** أو إصدار أحدث
- **ما استيراد مخطط WHT PPh (المعرف).الإصدار 93.14** أو إصدار أحدث

## <a name="set-up-general-ledger-parameters"></a>إعداد معلمات دفتر الأستاذ العام

1. انتقل إلى **الضريبة** \> **الإعداد** \> **معلمات دفتر الأستاذ العام**.
2. في علامة التبويب **ضريبة الخصم**، في الحقل **تعيين تنسيق إقرار ضريبة الخصم**، حدد **استيراد مخطط WHT PPh (معرف)**. 
3. انتقل إلى **الضريبة** \> **الإعداد** \> **ضريبة الخصم** \> **أنواع إيرادات ضريبة الخصم** لإعداد نوع إيرادات ضريبة خصم **Kode Bukti Potong** ثم قم بتعيين الرموز لمجموعات ضرائب الخصم على العناصر ذات الصلة. الرموز مطلوبة لإنشاء ملف التكامل باستخدام تطبيق e-Bupot. 

## <a name="generate-the-withholding-import-file"></a>إنشاء ملف استيراد الخصم

تعتمد عملية إعداد وإنشاء ملف e-Bupot لفترة محددة على حركات ضريبة الاستقطاع التي تم ترحيلها أثناء وظيفة التسوية أو ضريبة ما بعد الدفع.

اتبع هذه الخطوات لإنشاء الملف.

1. انتقل إلى **الضريبة** \> **الإقرارات** \> **ضريبة الخصم** \> **PPH ملف الاستيراد e-bupot 23 و26**.
2. حدد تاريخ "من" و"إلى" للتقرير، ثم حدد فترة التسوية.
3. أدخل تاريخ الحركة، ثم حدد **موافق**.
4. حدد اللغة. تمت ترجمة جميع التقارير إلى اللغة الإنجليزية الأمريكية (**en-us**) واللغة الإندونيسية (**id**).
5. حدد نوع الأعمال ثم أدخل الشيك وأرقام المستندات. 
6. تحقق مما إذا كان التقرير قد تم توقيعه من قِبل المدير. تم الإبلاغ عن هذه المعلومات في الملف. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]