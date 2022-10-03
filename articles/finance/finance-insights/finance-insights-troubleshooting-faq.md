---
title: استكشاف مشاكل إعداد Finance Insights وإصلاحها
description: توضح هذه المقالة المشاكل التي قد تحدث عند استخدام قدرات Finance Insights. كما يشرح كيفية إصلاح هذه المشاكل.
author: panolte
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 331c714663d212471b72f1558e6183452ef7f394
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573158"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>استكشاف مشاكل إعداد Finance Insights وإصلاحها

[!include [banner](../includes/banner.md)]

توضح هذه المقالة المشاكل التي قد تحدث عند استخدام قدرات Finance Insights. كما يشرح كيفية إصلاح هذه المشاكل.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>العرض: لماذا لا يمكنني تعيين عمود وجهة قالب تكامل البيانات لمعلومات الدفع الخاصة بالعميل؟

### <a name="resolution"></a>القرار

ربما تستخدم قالبًا تابعًا لإصدار سابق. قبل إطلاق الإصدار 10.0.17، قام عملاء الإصدار الأولي بتكوين قالب تكامل البيانات (DI) في **نتائج معلومات الدفع الخاصة بالعميل (CDS إلى Fin and Ops)** باستخدام الكيان **نتيجة توقع الدفع (إصدار أولي)**. بعد الترقية إلى 10.0.17 والإصدارات اللاحقة، يجب عليك استخدام قالب DI في **نتائج معلومات الدفع الخاصة بالعميل (CDS إلى Fin and Ops 10.0.17 والإصدارات اللاحقة)** لإكمال التعيين. قد لا تتمكن من تعيين العمود الوجهة لقالب DI حتى يتم تحديث قائمة كيانات إدارة البيانات وظهور الكيان **نتيجة توقع الدفع**. لتحديث قائمة الكيانات وإظهار نتيجة توقع الدفع، ستقوم بإكمال الخطوات في كل من Microsoft Dynamics 365 Finance وDataverse (يُعرف سابقًا باسم مدخل مسؤول Common Data Service \[CDS\]).

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

## <a name="symptom-why-isnt-the-install-a-new-add-in-button-visible-in-microsoft-dynamics-lifecycle-services"></a>العَرَضْ‬: لماذا لا يكون الزر تثبيت وظيفة إضافية مرئيًا في Microsoft Dynamics Lifecycle Services؟

### <a name="resolution"></a>القرار

أولاً، تحقق من أنه يتم تعيين الدور **مدير البيئة** أو **مالك المشروع** إلى المستخدم في الحقل **دور أمان المشروع** في Microsoft Dynamics Lifecycle Services (LCS). يتطلب تثبيت الوظائف الإضافية الجديدة وجود دور واحد من أدوار أمان المشروع هذه.

إذا تم تعيين دور أمان المشروع الصحيح إليك، فقد تحتاج إلى تحديث نافذة المستعرض الخاصة بك لرؤية الزر **تثبيت وظيفة إضافية جديدة**.

## <a name="symptom-the-finance-insights-add-in-doesnt-seem-to-be-installing-why-is-that"></a>العَرَضْ‬: لا يبدو أنه قد تم تثبيت الوظيفة الإضافية في Finance insights. ما سبب ذلك؟

### <a name="resolution"></a>القرار

يجب إكمال الخطوات التالية.

- تحقق من أنه لديك حق الوصول بصفة **مسؤول النظام** و **مخصص النظام** في مركز إدارة Power Portal.
- تحقق من أنه يتم تطبيق ترخيص Dynamics 365 Finance أو الترخيص المكافئ على المستخدم الذي يقوم بتثبيت الوظيفة الإضافية.
- تحقق من أنه يتم تسجيل تطبيق Azure AD التالي في Azure AD: 

    | استمارة التقديم                  | معرف التطبيق           |
    | ---------------------------- | ---------------- |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 | 
  
    للتحقق من تسجيل التطبيق في Azure AD ، تحقق من **قائمه كافة التطبيقات**. لمزيد من التفاصيل ، راجع [عرض تطبيقات المؤسسة](/azure/active-directory/manage-apps/view-applications-portal).
  
    إذا لم يكن التطبيق مسجلا في Azure AD ، اتصل بالدعم.

## <a name="symptom-error-we-didnt-find-any-data-for-the-selected-filter-range-please-select-a-different-filter-range-and-try-again"></a>العَرَض‬‏‫: خطأ، "لم نعثر على أي بيانات لنطاق عامل التصفية المحدد. الرجاء تحديد نطاق تصفية آخر والمحاولة مره أخرى." 

### <a name="resolution"></a>القرار

تحقق من إعداد موحد البيانات للتأكد من أنه يعمل كما هو متوقع ويحدّث البيانات من AI Builder إلى Finance.  
لمزيد من المعلومات، راجع [إنشاء مشروع تكامل البيانات](../finance-insights/create-data-integrate-project.md).

## <a name="symptom-customer-payment-prediction-training-failed-and-the-ai-builder-error-states-prediction-should-have-only-2-distinct-outcome-values-to-train-the-model-map-to-two-outcomes-and-retrain-training-report-issue-isnotminrequireddistinctnonnullvalues"></a>العَرَضْ‬‬‏‫: فشل تدريب توقع دفع العميل وحالات خطأ AI Builder، "يجب أن يحتوي التنبؤ على قيمتين ناتجتين مميزتين فقط لتدريب النموذج. قم بالتعيين إلى النتائج وأعد التدريب"، "مشكلة في تقرير التدريب: IsNotMinRequiredDistinctNonNullValues".

### <a name="resolution"></a>القرار

يشير هذا الخطأ إلى عدم وجود حركات قديمة كافية في السنهة الأخيرة تمثل كل فئة ورد وصفها في الفئات **في الوقت المحدد‬** و **متأخر** و **متأخر‏‎ جدًا**. لحل هذا الخطأ، قم بتعديل فتره الحركة **المتأخرة جدًا**. إذا لم يساعد تعديل فترة الحركة **المتأخرة جدًا** على إصلاح الخطأ، فإن الخيار **توقعات دفع العميل‬** ليس الحل الأفضل لأنه يحتاج إلى بيانات في كل فئة لأغراض التدريب.

لمزيد من المعلومات حول كيفية تعديل الفئات **في الوقت المحدد** و **متأخر** و **متأخر جدًا**، راجع [تمكين توقعات دفع العميل‬](../finance-insights/enable-cust-paymnt-prediction.md).

## <a name="symptom-model-training-failed"></a>العَرَض‬‬‏‫: فشل تدريب النموذج

### <a name="resolution"></a>القرار

يحتاج تدريب نموذج **تقدير التدفقات النقدية‬** إلى بيانات تحتوي على 100 حركة أو أكثر تمتد عبر أكثر من سنة. من المستحسن أن يكون لديك سنتين من البيانات على الأقل مع أكثر من 1000 حركة.

تتطلب الميزة **توقعات دفع العميل‬** أكثر من 100 حركة في الأشهر الستة إلى التسعة السابقة. بإمكان الحركات أن تتضمن فواتير النص الحر وأوامر المبيعات ومدفوعات العميل. يجب نشر هذه البيانات من خلال الإعدادات **في الوقت المناسب** و **متأخر** و **متأخر جدًا** المحددة في صفحة **التكوين**.    

تتطلب ميزة **مقترح الموازنة** ثلاث سنوات كحد أدنى من الموازنة أو البيانات الفعلية. يستخدم هذا الحل من ثلاث إلى عشر سنوات من البيانات في التوقعات. ستحصل على نتائج أفضل إذا كانت الفترة تزيد عن ثلاث سنوات. وتعمل البيانات نفسها بشكل أفضل عندما يكون هناك اختلاف في القيم. إذا كانت البيانات تحتوي علي كافة البيانات الثابتة، مثل مصروفات الإيجار، فقد يفشل التدريب لأن نقص التباين لا يتطلب الذكاء الاصطناعي لتوقع المبالغ.

## <a name="symptom-error-message-states-that-the-table-with-name-msdyn_paypredpredictionresultentities-does-not-exist-the-remote-server-returned-an-error-404-not-found"></a>العَرَضْ‬: تفيد رسالة الخطأ بأن "الجدول المسمى 'msdyn_paypredpredictionresultentities' غير موجود أرجع الخادم البعيد الخطأ: (404) غير موجود... "

### <a name="resolution"></a>القرار

وصلت البيئة إلى الحد الأقصى لجدول خدمات Data Lake. لمزيد من المعلومات عن الحد، راجع قسم **تمكين تغييرات البيانات في وقت قريب من الوقت الحقيقي** من مقالة [التصدير إلى Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/Azure-Data-Lake-GA-version-overview.md).
