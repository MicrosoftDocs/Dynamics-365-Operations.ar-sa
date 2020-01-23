---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (13‏ مايو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab201e099a5075760c038d819759162682874a33
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896901"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-13-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (13‏ مايو 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="coming-soon-in-attract"></a>قريبًا في Attract

### <a name="job-approvals-on-home-page"></a>موافقات الوظائف في الصفحة الرئيسية

تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات. يستطيع المعتمدون مراجعة موافقاتهم ضمن **المعينة لك**، التي تعرض معرف الوظيفة والعنوان والمعتمدين الآخرين والتاريخ المعين. يستطيع المستخدمين الذين يقومون بإرسال مهمة للاعتماد مراجعة الوظائف الخاصة بهم ضمن **طلبتها**، وهو ما يعرض المعتمدين الذين لا يزالوا يحتاجون إلى اعتماد الوظيفة التي تم إرسالها.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2297. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>الإشارة إلى نوع المثيل عند تزويد Talent

عند تزويد مثيل Talent جديد، ستتمكن من الإشارة إلى ما إذا كان نوع المثيل هو **إنتاج** أو **بيئة اختبار معزولة**، مما يسمح بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختيار المعزولة**، يُرجى الاتصال بـ [الدعم](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.

### <a name="common-data-service-entity-support-for-custom-fields"></a>دعم كيان Common Data Service للحقول المخصصة

في إصدار الأسبوع هذا، تدعم كيانات Common Data Service  التالية الآن المجالات المخصصة: التوظيف، وتكرار حساب الميزات، ومعدل حساب الميزات، وإجازة تقويم العمل، ونوع التعريف.

### <a name="common-data-service-integration-page"></a>صفحة تكامل Common Data Service

يوفر هذا الإصدار خيارًا جديدًا في **إدارة النظام > الارتباطات> التكاملات > تكوين Common Data Service**. يسمح خيار تكوين **Common Data Service** للمسؤول أو مسؤول إدارة البيانات ببعض المرونة والرؤى في Common Data Service. باستخدام هذا الخيار، يمكنك تمكين تكامل Common Data Service باستخدام مثيل Talent أو تعطيله وعرض تفاصيل المزامنة بين مثيل Talent وCommon Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>استيراد بيانات الأداء مع تقييم الموظف النهائي (316710)

في هذا الإصدار، يمكنك استيراد بيانات تقييم الموظف التاريخية. يحتوي حقل **FinalEmployeeRatingId** الآن على إذن الكتابة.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>لا يمكن إنشاء عنوان العامل في Common Data Service ومزامنته باستخدام Talent (317555)

يتيح هذا التغيير إنشاء بيانات بيانات العنوان في Common Data Service لمزامنتها باستخدام Talent.

## <a name="in-preview"></a>قيد المعاينة

### <a name="new-page-to-validate-position-hierarchy-data"></a>صفحة جديدة للتحقق من صحة بيانات التدرج الهرمي للمناصب

بإمكان قسم الموارد البشرية (البشرية) والمسؤولين التحقق من صحة التدرج الهرمي الإداري لأي مراجع دائرية قد يتم استيرادها بشكل غير مقصود. يمكنك الوصول إلى هذه الصفحة الجديدة من **الإدارة التنظيمية > الارتباطات > المناصب > التحقق من صحة بيانات التدرج الهرمي للمناصب‬**.

### <a name="specify-reason-codes-on-leave-types"></a>تحديد أكواد الأسباب في أنواع الإجازات

قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة

قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلبات إجازة. قد يكون هذا الشرط موجودًا بسبب سياسة الشركة أو المتطلبات التنظيمية. يمكنك تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية

تؤدي القدرة على تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات ليس فقط إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين ولكنها تساعد أيضًا على ضمان منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) لتمكين موظفي الموارد البشرية من الاطلاع على الأسباب التي تكمن خلف أرصدة أيام الإجازات.
