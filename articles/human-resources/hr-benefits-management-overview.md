---
title: نظرة عامة على إدارة المزايا
description: نظرة عامة على ميزة معاينة إدارة المزايا في Dynamics 365 Human Resources. يمكنك تزويد موظفيك بخيارات المزايا الممتدة مع تجربة سهلة الاستخدام عبر الإنترنت.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029453"
---
# <a name="benefits-management-overview"></a>نظرة عامة على إدارة المزايا

[!include [banner](includes/preview-feature.md)]

لكي تظل قادرًا على المنافسة، ينبغي أن تقدم مجموعة ثرية من المزايا لجذب أفضل الموظفين والاحتفاظ بهم. بالإضافة إلى المزايا القياسية مثل التغطية الطبية وتغطية الأسنان، وقد ترغب أيضًا في تقديم خدمات موسعة مثل المساعدة في التبني وبرامج الترفيه وبدل الملابس. توفر لك ميزة معاينة إدارة المزايا في Microsoft Dynamics 365 Human Resources حلاً مرنًا يدعم مجموعة واسعة من خيارات المزايا. كما يتضمن Human Resources أيضًا تجربة سهلة الاستخدام للموظف التي تعرض عروضك.

- تتيح لك خطط المزايا المحسّنة إنشاء وإدارة خطط مزايا فريدة ودعم جداول معدلات الميزة المعقدة والمستويات المتداخلة. يمكنك بسهولة إنشاء برامج ميزة وحزم وقواعد التسجيل التلقائي لتجربة استخدام أسهل من جانب الموظف.

- تسمح لك برامج الائتمان المرنة التقسيم بالتناسب لدعم التقاعد والأحداث الحياتية الأخرى.

- وتضمن قواعد الاستحقاق الشاملة جعل المزايا الصحيحة متوفرة للموظفين المستحقين.

- يوفر تسجيل المزايا عبر الإنترنت تجربة سهلة لموظفيك.

- تتكامل معالجة الأحداث الحياتية المؤهلة مع الخدمة الذاتية للموظف، كما تدعم الأحداث الحياتية المستقبلية.

إذا كنت ترغب في الوصول إلى بيانات العرض التوضيحي‬، فستحتاج إلى إعادة نشر بيئة الحماية.

يمكنك تقديم ملاحظات مباشرة أو الإبلاغ عن المشكلات إلى: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>المشكلات المعروفة في إدارة المزايا

### <a name="eligibility-processing"></a>معالجة الاستحقاق

عند تشغيل الاستحقاق للمزايا التي تستخدم 1-5X الراتب، % من الراتب، ومبلغ تغطيه المبلغ ‏‫المبلغ الأساسي ، يتعين تعيين تاريخ **تفاصيل الميزة** لـ **تاريخ بدء الموظف** في **سجل التوظيف**. يجب عليك أيضًا تضمين **ساعات العمل** و **تكرار الدفع** و **مبلغ راتب المزايا السنوي**. إذا كان للعامل تعويض ثابت ، ادخل **ساعات العمل** و **تكرار الدفع**. سوف يتم حساب مبلغ الراتب السنوي. إذا كان الموظف براتب، فلن تحتاج إلى إدخال **ساعات العمل**. نوصي بإدخال التعويض الثابت أولًا، عند إنشاء عُمال جدد. لتحديث سجل تفاصيل الميزة، انتقل إلى **العامل > سجل العامل> تفاصيل التوظيف**. قم بتعديل التاريخ لتاريخ البدء الخاص بالعامل.

### <a name="employee-self-service"></a>خدمة الموظف الذاتية

لا يتم حساب مبلغ الموظف عند تحديث مبلغ التغطية للتأمين على الحياة. على سبيل المثال، عندما يتم عرض خطة تأمين على الحياة لأحد الموظفين، يُمكنهم تحديد ما يصل إلى 50.000 دولار في التغطية بتكلفة .36 دولار لكل 1.000 دولار من التغطية.  عندما يقوم الموظف بتحديث مبلغ التغطية، تظل التكلفة المرتبطة بالموظف بالقيمة صفر.

بالنسبة لخطة الميزة التي لا تسمح إلا بتحديد واحد من نوع الخطة، يتلقى المستخدم خطأ إذا حاول التنازل عن الخطة بعد تحديدها. علي سبيل المثال ، يحدد المستخدم خطه طبية ويضعها في سلة التسوق الخاصة به. ثم يُحدد المستخدم **تنازل** لخطة طبية أخرى. سوف يتلقى المستخدم خطأ.

## <a name="enable-benefits-management"></a>تمكين إدارة المزايا

تُعد إدارة المزايا ميزة معاينة، وهي متوفرة فقط في بيئات **الحماية‬** . توضح هذه المقالات كيفية تشغيل ميزات المعاينة في Human Rescources. كما أنها تحدد المزايا الموجودة في Human Resources والتي تستبدلها إدارة المزايا أو تقوم بتعطيلها بمجرد تشغيل إدارة المزايا.

- [إدارة الميزات](hr-admin-manage-features.md)
- [ميزة المعاينة: إدارة المزايا](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>تكوين إدارة المزايا

قبل أن تتمكن من إنشاء خطط المزايا للموظفين، تحتاج إلى تكوين خيارات للخطط.

- [تعيين معلمات إدارة المزايا](hr-benefits-setup-parameters.md)
- [تكوين قواعد الاهلية وخياراتها](hr-benefits-setup-eligibility-rules.md)
- [تكوين خيارات أهلية جهة الاتصال الشخصية](hr-benefits-setup-contact-eligibility-options.md)
- [إنشاء خيارات تغطية](hr-benefits-setup-coverage-options.md)
- [إعداد تكرارات الدفع](hr-benefits-setup-payment-frequencies.md)
- [تكوين أنواع الأحداث الحياتية](hr-benefits-setup-life-event-types.md)
- [إنشاء أنواع الخطة](hr-benefits-setup-plan-types.md)
- [إعداد أكواد السبب](hr-benefits-setup-reason-codes.md)
- [إعداد أكواد الطبقات](hr-benefits-setup-tier-codes.md)
- [تكوين المعدلات](hr-benefits-setup-rates.md)
- [تكوين الخصومات](hr-benefits-setup-deductions.md)
- [تكوين أيام الانتظار](hr-benefits-setup-waiting-days.md)
- [تكوين فترات الانتظار](hr-benefits-setup-waiting-periods.md)
- [إعداد قواعد التقريب](hr-benefits-setup-rounding-rules.md)
- [إنشاء فئات التوظيف](hr-benefits-setup-employment-categories.md)
- [إعداد أنواع التوظيف](hr-benefits-setup-employment-types.md)
- [تكوين خدمة الموظف الذاتية](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>إنشاء خطط المزايا

توضح هذه المقالات كيفية إنشاء خطط المزايا، بما في ذلك الحزم وبرامج الائتمان المرنة.

- [إعداد خطط المزايا](hr-benefits-plans-setup.md)
- [إنشاء خطط المزايا الخاصة بالعامل](hr-benefits-plans-worker.md)
- [إعداد برامج الائتمان المرنة](hr-benefits-plans-flex-credit-programs.md)
- [تكوين الأحداث الحياتية المستقبلية](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>معالجة خطط المزايا

تحتاج إلى معالجة بعض تغييراتك لجعلها نشطة.

- [معالجة أهلية التسجيل‬](hr-benefits-process-enrollment-eligibility.md)
- [معالجة الأحداث الحياتية](hr-benefits-process-life-events.md)
- [معالجة تغييرات الأحداث الحياتية](hr-benefits-process-life-event-changes.md)
- [‏‫معالجة أهلية الحدث الحياتي‬](hr-benefits-process-life-event-eligibility.md)
- [معالجة تغييرات المعدل](hr-benefits-process-rate-changes.md)

