---
title: نظره عامه علي حل Invoice capture
description: توفر هذه المقالة معلومات حول حل Invoice capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691120"
---
# <a name="invoice-capture-solution"></a>حل Invoice capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يقدم هذا المقال معلومات حول حل Invoice capture الذي يقوم بإنشاء فواتير المورد من صور الفواتير الرقمية تلقائيا.

تقوم الاداره الحسابات الدائنة (AP) باداره الفواتير الخاصة بالبضائع والخدمات التي يتم استلامها ومعالجتها. يتحقق محاسب الوصول إلى البيانات الموجودة في فواتير المورد للأسباب التالية:

- لتجنب المجهود الإضافي إذا كانت التسويات أو التصحيحات مطلوبه اثناء اقفال الفترة
- لدفع فواتير المورد بطريقه في الوقت المناسب ومنع الخسائر المالية بسبب الخطا أو الاحتيال

وقد تم استخدام التعرف البصري علي الحرف (OCR) بشكل واسع بواسطة صناعات مختلفه في السنوات الماضية. وهذا الأمر شائع الآن لإظهار النصوص المطبوعة ، بحيث يمكن تحريرها الكترونيا والبحث فيها وتخزينها بشكل أكثر كومباكتلي وعرضها عبر الإنترنت. يمكن استخدام النص الرقمي في العمليات اليه مثل الحوسبة المعروفة والترجمة اليه وتحويل النص إلى كلام والبيانات الاساسيه وجمع النص.

قامت تقنيه تطوير المعلومات الزائفة (الذكاء الاصطناعي) بتمكين حلول OCR الحديثة لقراءه تنسيقات فواتير مختلفه من موردين مختلفين بدون الحاجة إلى تدخل بشريه للغاية. تقوم المزيد من الشركات بالتعرف علي امكانيه حفظ الجهد وتحسين الدقة من خلال معالجه الفواتير من خلال التنفيذ التلقائي بدلا من اجراء المعالجة اليدوية.

## <a name="system-landscape"></a>النظام الأفقي

يبين الرسم التوضيحي التالي المكونات الرئيسية والخطوات في حل Invoice capture.

[![المكونات والخطوات في حل Invoice capture.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>الأدوار المطلوبة

يعرض الجدول التالي الأدوار المطلوبة لاعداد حل Invoice capture واستخدامه.

| دور          | الإجراءات | الأنظمة | اسم AOT للدور |
|---------------|---------|---------|-----------|
| مسؤول | <ul><li>قم بإعداد البيئات في Microsoft Power Platform.</li><li>نشر الحلول في Microsoft Power Platform.</li><li>قم باعداد الاتصالات بين Dynamics 365 و AI Builder.</li><li>إعداد Azure Data Lake Storage المواقع.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>مسؤول Dynamics 365</li><li>مسؤول Power Platform</li><li>مالك بيانات تخزين البيانات الثنائية الكبيرة</li></ul> |
| الذكاء الاصطناعي maker      | <ul><li>صيانة التدفقات.</li><li>إنشاء نماذج الذكاء الاصطناعية مخصصه.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>صناعات مرتكز</li></ul> |
| موظف AP      | <ul><li>مراجعه الإجراءات الموجودة في المنطقة التدريج لفاتورة المورد والقيام بها.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>دور موظف جديد لنقطه الوصول في Power Platform</li></ul> |
| موظف AP      | <ul><li>تنفيذ العمليات اليومية كموظف AP.</li><li>انتقل إلى منطقه تقسيم فاتورة المورد.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>موظف الحسابات الدائنة</li></ul> |
  
لمزيد من المعلومات حول تثبيت Invoice capture ، راجع [تثبيت التقاط](../accounts-payable/install-invoice-capture.md) الفواتير.  
