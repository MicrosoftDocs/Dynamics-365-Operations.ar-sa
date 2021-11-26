---
title: استكشاف مشاكل إعداد Finance Insights وإصلاحها
description: يسرد هذا الموضوع المشاكل التي قد تحدث عند استخدام قدرات Finance Insights. كما يشرح كيفية إصلاح هذه المشاكل.
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: f3cac30a66ff3a74a7f67c11dd9fa14af79d10af
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752606"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>استكشاف مشاكل إعداد Finance Insights وإصلاحها

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يسرد هذا الموضوع المشاكل التي قد تحدث عند استخدام قدرات Finance Insights. كما يشرح كيفية إصلاح هذه المشاكل.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>العرض: لماذا لا يمكنني تعيين عمود وجهة قالب تكامل البيانات لمعلومات الدفع الخاصة بالعميل؟

### <a name="resolution"></a>القرار

ربما تستخدم قالبًا تابعًا لإصدار سابق. قبل إطلاق الإصدار 10.0.17، قام عملاء الإصدار الأولي بتكوين قالب تكامل البيانات (DI) في **نتائج معلومات الدفع الخاصة بالعميل (CDS إلى Fin and Ops)** باستخدام الكيان **نتيجة توقع الدفع (إصدار أولي)**. بعد الترقية إلى 10.0.17 والإصدارات اللاحقة، يجب عليك استخدام قالب DI في **نتائج معلومات الدفع الخاصة بالعميل (CDS إلى Fin and Ops 10.0.17 والإصدارات اللاحقة)** لإكمال التعيين. قد لا تتمكن من تعيين العمود الوجهة لقالب DI حتى يتم تحديث قائمة كيانات إدارة البيانات وظهور الكيان **نتيجة توقع الدفع**. لتحديث قائمة الكيانات وإظهار نتيجة توقع الدفع، ستقوم بإكمال الخطوات في كل من Microsoft Dynamics 365 Finance وDataverse (يُعرف سابقًا باسم مدخل مسؤول Common Data Service \[CDS\]l).

### <a name="in-finance"></a>في Finance

اتبع هذه الخطوات في Finance بعد الترقية.

1. اذهب إلى **إدارة النظام \> مساحات العمل \> إدارة البيانات**.
2. في مساحة عمل **إدارة البيانات**، حدد الإطار المتجانب **معلمات إطار العمل**.
3. في الصفحة **معلمات إطار العمل لاستيراد/تصدير البيانات**، حدد **إعدادات الكيان**، ثم حدد **تحديث قائمة الكيانات**.
4. قم بإغلاق الصفحة **معلمات إطار العمل لاستيراد/تصدير البيانات**.
5. في مساحة عمل **إدارة بيانات**، حدد تجانب **كيانات البيانات**.
6. ابحث عن "نتيجة توقع الدفع". تحقق من أن كيان **نتيجة توقع الدفع** ليس الإصدار الأولي. ينتهي اسم الإصدار الأولي بـ "(إصدار أولي)." إذا رأيت فقط الإصدار الأولي للكيان، فاتصل بدعم Microsoft.

### <a name="in-dataverse"></a>في Dataverse

اتبع الخطوات التالية في [Power Platform admin center](https://admin.powerplatform.microsoft.com/environments) لتحديث مشاريع تكامل البيانات.

1. إذا كنت تستخدم إصدارًا أوليًا من Finance Insights، فعليك إزالة المشروع DI المرتبط بالقالب **نتائج معلومات الدفع الخاصة بالعميل (CDS لـ Fin وOps)‬**.
2. اتبع الخطوات في [إنشاء مشروع تكامل البيانات](create-data-integrate-project.md). استخدم القالب **نتائج معلومات الدفع الخاصة بالعميل (CDS إلى Fin and Ops 10.0.17 والإصدارات اللاحقة)**.

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>العَرَض: عندما أحاول فتح AI Builder باستخدام الارتباطات الموجودة في صفحة إعداد توقعات دفع العميل، فلماذا أتلقى رسالة الخطأ التالية: "عذرًا، حدث انقطاع في الاتصال"؟

### <a name="resolution"></a>القرار

يجب أن يكون لدى مستخدمي Dynamics 365 Finance حساب مستخدم Microsoft Power Apps للبيئة، ويجب أن يكون لحساب المستخدم دور مخصص النظام. يمكن لمسؤول نظام Microsoft Power Apps إنشاء حساب المستخدم وتعيين الدور. يمكنك بعد ذلك الانتقال إلى <https://make.preview.powerapps.com/>، وتسجيل الدخول باستخدام حساب المستخدم هذا، وجرب الروابط مرة أخرى.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>العرض: لماذا لا تظهر علامة التبويب التوقع النقدي في مساحة عمل "تقدير التدفقات النقدية‬" أي بيانات؟

### <a name="resolution"></a>القرار

يجب إعداد وظيفة تقدير التدفقات النقدية‬ في "إدارة النقد والبنوك‬" و"تقديرات التدفقات النقدية‬" في Finance Insights ويجب تمكينها لتصحيح البيانات بشكل صحيح في مساحة العمل **تقدير التدفقات النقدية‬**.

عليك أولاً إعداد وتمكين تقدير التدفقات النقدية وحسابات السيولة. لمزيد من المعلومات، راجع [‏‫تقدير التدفقات النقدية](../cash-bank-management/cash-flow-forecasting.md). إذا تم إكمال هذا الإعداد، ولكنك لم تتمكن من رؤية النتائج التي تتوقعها، فراجع [استكشاف أخطاء إعداد تقدير التدفقات النقدية وإصلاحها](../cash-bank-management/cash-flow-forecasting-tsg.md) لمزيد من المعلومات.

بعد ذلك، تأكد من تمكين ميزة تقديرات التدفقات النقدية‬ في Finance insights (**إدارة النقد والبنوك‬ \> الإعداد \> Finance Insights \> تقديرات التدفقات النقدية**) ومن استكمال تدريب نموذج AI model. إذا لم يتم إكمال التدريب، فحدد **التنبؤ الآن** لبدء عملية التدريب على النماذج.
