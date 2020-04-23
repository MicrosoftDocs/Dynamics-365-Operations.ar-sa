---
title: نظرة عامة على إدارة المزايا
description: نظرة عامة على ميزة إدارة المزايا في Dynamics 365 Human Resources. يمكنك تزويد موظفيك بخيارات المزايا الممتدة مع تجربة سهلة الاستخدام عبر الإنترنت.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 91a4425b4f020f90843bb3b0b280b7ee28463670
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230144"
---
# <a name="benefits-management-overview"></a>نظرة عامة على إدارة المزايا

لكي تظل قادرًا على المنافسة، ينبغي أن تقدم مجموعة ثرية من المزايا لجذب أفضل الموظفين والاحتفاظ بهم. بالإضافة إلى المزايا القياسية مثل التغطية الطبية وتغطية الأسنان، وقد ترغب أيضًا في تقديم خدمات موسعة مثل المساعدة في التبني وبرامج الترفيه وبدل الملابس. توفر لك ميزة إدارة المزايا في Microsoft Dynamics 365 Human Resources حلاً مرنًا يدعم مجموعة واسعة من خيارات المزايا. كما يتضمن Human Resources أيضًا تجربة سهلة الاستخدام للموظف التي تعرض عروضك.

- تتيح لك خطط المزايا المحسّنة إنشاء وإدارة خطط مزايا فريدة ودعم جداول معدلات الميزة المعقدة والمستويات المتداخلة. يمكنك بسهولة إنشاء برامج ميزة وحزم وقواعد التسجيل التلقائي لتجربة استخدام أسهل من جانب الموظف.

- تسمح لك برامج الائتمان المرنة التقسيم بالتناسب لدعم التقاعد والأحداث الحياتية الأخرى.

- وتضمن قواعد الاستحقاق الشاملة جعل المزايا الصحيحة متوفرة للموظفين المستحقين.

- يوفر تسجيل المزايا عبر الإنترنت تجربة سهلة لموظفيك.

- تدعم معالجة أحداث الحياة المؤهلة أحداث الحياة المستقبلية.

إذا كنت ترغب في الوصول إلى بيانات العرض التوضيحي‬، فستحتاج إلى إعادة نشر بيئة الحماية.

## <a name="benefits-management-known-issues"></a>المشكلات المعروفة في إدارة المزايا

### <a name="flex-credit-programs"></a>برامج الائتمان المرنة

لا تظهر قيمة الائتمان الإجمالية المحددة لبرنامج ائتمان مرن‬ في نموذج **خطط المزايا الخاصة بالعامل**. كذلك الأمر، إذا قمت بتعيين برنامج ائتمان كي تكون له قاعدة تناسب بقيمة **بلا**، ستحصل على خطأ في نموذج **خطط المزايا الخاصة بالعامل‬‏‫** عند تحديد الخطط وتأكيدها.

## <a name="enable-benefits-management"></a>تمكين إدارة المزايا

توضح هذه المقالة كيفية تشغيل ميزات Human Resources. كما أنها تحدد المزايا الموجودة في Human Resources والتي تستبدلها إدارة المزايا أو تقوم بتعطيلها بمجرد تشغيل إدارة المزايا.

> [!IMPORTANT]
> بعد تمكين إدارة المزايا في بيئة **الإنتاج**، لا يمكنك تعطيلها. نوصي بتمكين إدارة المزايا واختبارها في **بيئة اختبار معزولة** قبل تمكينها في بيئة **الإنتاج**. توجد اختلافات كبيرة بين وظيفة المزايا القديمة ووظيفة إدارة المزايا الجديدة التي تتطلب عملية إعداد إضافية ويجب اختبارها قبل وضعها في بيئة الإنتاج.

- [إدارة الميزات](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>تكوين معلومات الموظفين

قبل تسجيل الموظفين في المزايا، يجب تقديم المعلومات المطلوبة. يجب أن تسجل موظفًا في **خطة تعويض ثابت** في تاريخ بدئها، ويجب أن تحدد **تكرار دفع المزايا** في **تفاصيل التوظيف** على نموذج **العامل**.

عند إنشاء خطة مزايا تستخدم الأسعار التي تعتمد على الجنس أو العمر، يجب إدخال تاريخ ميلاد الموظف وجنسه لحساب تكلفة المزايا.

## <a name="configure-benefits-management"></a>تكوين إدارة المزايا

قبل أن تتمكن من إنشاء خطط المزايا للموظفين، تحتاج إلى تكوين خيارات للخطط.

- [تعيين معلمات إدارة المزايا](hr-benefits-setup-parameters.md)
- [تكوين قواعد الاهلية وخياراتها](hr-benefits-setup-eligibility-rules.md)
- [تكوين خيارات أهلية جهة الاتصال الشخصية](hr-benefits-setup-contact-eligibility-options.md)
- [إنشاء خيارات تغطية](hr-benefits-setup-coverage-options.md)
- [إعداد تكرارات المدفوعات](hr-benefits-setup-payment-frequencies.md)
- [تكوين أنواع أحداث الحياة](hr-benefits-setup-life-event-types.md)
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
- [إعداد برامج الائتمان المرنة](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>معالجة خطط المزايا

تحتاج إلى معالجة بعض تغييراتك لجعلها نشطة.

- [معالجة أهلية التسجيل‬](hr-benefits-process-enrollment-eligibility.md)
- [معالجة الأحداث الحياتية](hr-benefits-process-life-events.md)
- [معالجة تغييرات الأحداث الحياتية](hr-benefits-process-life-event-changes.md)
- [‏‫معالجة أهلية الحدث الحياتي‬](hr-benefits-process-life-event-eligibility.md)
- [معالجة تغييرات المعدل](hr-benefits-process-rate-changes.md)

