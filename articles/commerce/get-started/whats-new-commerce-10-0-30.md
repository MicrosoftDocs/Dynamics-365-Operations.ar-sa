---
title: معاينة الإصدار 10.0.30 من Dynamics 365 Commerce (نوفمبر 2022)
description: تصف هذه المقالة الميزات الجديدة أو المتغيرة في 10.0.30. Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405538"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>معاينة الإصدار 10.0.30 من Dynamics 365 Commerce (نوفمبر 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا المقالا الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Commerce إصدار 10.0.30. رقم بنية هذا الإصدار هي 10.0.1362، وهو يتوفر وفق الجدول التالي:

- **معاينة الإصدار:** سبتمبر 2022
- **التوفر العام للإصدار (تحديث ذاتي):** أكتوبر 2022
- **التوفر العام للإصدار (تحديث تلقائي):** نوفمبر 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تمت إضافتها إلى البنية بعد نشر هذا الموضوع.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---------|------------------|----------------|--------------| 
| دعم العملاء.   | عليك الدردشة علي موقع تجاره الكترونيات باستخدام Power Virtual Agents بوت. | ستقوم هذه الميزة بمنح مستخدمي موقع التجارة الكترونيه اختيارا لاستخدام Power Virtual Agents بوت المحادثة لطلبات الدعم. | تم تمكينه بواسطة المسؤول/المتخذ للمستخدمين النهائيين |
| نتائج التحليلات  |  نقاط الرؤى التشغيلية لنقطه البيع (POS) لحسابك Application Insights. | [تسجيل الوصول في Application Insights](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  اشتراك تكنولوجيا الدخول الخاص ب Pro/developer   |
|  المدفوعات  | دعم طلب PayPal خارج فتره تخويل اليوم 29 يوم. | الحد الأقصى لفتره التخويل PayPal هو 29 يوما ، والذي يجب بعده إنشاء معرف التخويل والتفويض الجديد. وكبديل ، يقدم PayPal خيارا يمكن ان يتم فيه الرجوع إلى ترتيب PayPal كامر عام ، مما يسمح بالتفويضات والأسر المتعددة مقابل نفس معرف الأمر ، بدلا من إنشاء معرف تفويض جديد ومعرف الأمر في 29 يوما). | عند تكوين موصل دفع PayPal في Commerce headquarters، يتم أضافه الحقل **OrderIntent** ويمكن ان يحتوي علي قيمتين:<p><p>- **التخويل** -هذا التكوين هو الافتراضي (في حاله ترك الحقل فارغا ، **فان التخويل** سيعمل كاعداد افتراضي). تكوين **OrderIntent** إلى **Authorize** يرتبط بـ PayPal **تعليمات المعالجة** قيمة **NO_INSTRUCTION**. سيتم اعتماد الأمر مع PayPal ولا يمكن تعديل التخويل عند استخدام هذه القيمة.<p>- **حفظ** - عندما **OrderIntent** تم تعيين القيمة على **حفظ**, هذا يرتبط بـ PayPal **تعليمات المعالجة** قيمة **ORDER_SAVED_EXPLICITLY**. سيتم حفظ مراجع الأوامر في خدمه PayPal عند استخدام هذه القيمة.  |
| تسجيل الدخول في نقاط البيع  | [تمكين قدرات تشخيصات الخدمة الذاتية لتسجيل الدخول إلى نقطه البيع](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  توفر هذه الميزة إمكانيات تشخيص الخدمة الذاتية في نقطه البيع (POS) وCommerce headquarters للمساعدة في تخزين الموظفين والمديرين بسرعة لتحديد الأسباب الجذرية لمشكلات تسجيل الدخول إلى نقطه البيع وإصلاحها.<p><p>- تم تحسين رسائل الفشل التي تظهر على شاشة تسجيل الدخول في نقطة البيع لتوفير معلومات السبب الجذري الملموسة التي يمكن أن تساعد في تخزين الموظفين الذين يستخدمون نقاط البيع على فهم الخطأ الذي حدث حتى يتمكنوا من تنفيذ الإجراءات اللازمة لحل المشكلة.<p>أ **-تتوفر وظيفة تسجيل دخول** الاختبار في صفحه العاملين **في** Commerce headquarters بحيث يمكن لمديري المتجر الذين يقومون باعداد أجهزه retail pos محاكاة تسجيل الدخول بنقطه البيع. في حاله فشل تسجيل الدخول ، توفر هذه الوظيفة إرشادات استكشاف الأخطاء وإصلاحها قابله للتنفيذ حتى يتمكن المديرون من التحقق من التكوينات ذات الصلة والإصدارات الصحيحة والتحقق من صحة الإصلاحات.  | قيد التشغيل بشكل افتراضي |


## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن 10.0.30 Dynamics 365 Finance تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.30 من تطبيقات التمويل والعمليات](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من نسخة 10.0.30، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022](/dynamics365-release-plan/2022wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-features"></a>الميزات التي تمت إزالتها وإهمالها

توضح الميزات التي [تمت ازالتها أو إهمالها في Dynamics 365 Commerce](removed-deprecated-features-commerce.md) المقالة الميزات التي تمت ازالتها أو إهمالها للتجارة.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]