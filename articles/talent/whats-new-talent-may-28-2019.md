---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (28‏ مايو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 29e941ddab1b2746ccd74d6e335fec7742d1391e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529598"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (28‏ مايو 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>قريبًا في Attract

### <a name="job-approvals-on-home-page"></a>موافقات الوظائف في الصفحة الرئيسية

تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات. يستطيع المعتمدون مراجعة موافقاتهم ضمن **المعينة لك**، التي تعرض معرف الوظيفة والعنوان والمعتمدين الآخرين والتاريخ المعين. يستطيع المستخدمين الذين يقومون بإرسال مهمة للاعتماد مراجعة الوظائف الخاصة بهم ضمن **طلبتها**، وهو ما يعرض المعتمدين الذين لا يزالوا يحتاجون إلى اعتماد الوظيفة التي تم إرسالها.

## <a name="changes-in-onboard"></a>التغييرات في Onboard
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2319.

### <a name="common-data-service-entity-support-for-custom-fields"></a>دعم كيان Common Data Service للحقول المخصصة

في إصدار الأسبوع هذا، تدعم كيانات Common Data Service التالية الآن المجالات المخصصة: تفاصيل معدل حساب الميزات، وبنذ إجازة تقويم العمل، والتوظيف.

### <a name="copy-position-now-includes-payroll-details"></a>نسخ المنصب يشمل الآن تفاصيل الرواتب
عند استخدام **نسخ المنصب** وتحديد كافة الخيارات، تكون معلومات تفاصيل الرواتب مضمنة الآن في معلومات النسخ. 

## <a name="in-preview-in-core-hr"></a>في المعاينة في Core HR

### <a name="restrict-the-leave-types-in-time-off-requests"></a>تقييد أنواع الإجازات في طلب أيام الإجازات

يمكن للمؤسسات تقديم العديد من الأنواع المختلفة من الإجازات إلى الموظفين. قد لا تكون بعض أنواع الإجازات هذه مناسبة للموظفين لطلب الحصول على إيام الإجازة وتتم إدارتها بواسطة الموارد البشرية (HR) بدلاً من ذلك. وباستخدام هذا الإصدار، يمكنك تكوين أنواع الإجازات التي يمكن للموظفين إرسال طلبات أيام الإجازة لها. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>صفحة جديدة للتحقق من صحة بيانات التدرج الهرمي للمناصب

بإمكان قسم الموارد البشرية (HR) والمسؤولين التحقق من صحة التدرج الهرمي الإداري لأي مراجع دائرية قد يتم استيرادها بشكل غير مقصود. يمكنك الوصول إلى هذه الصفحة الجديدة من **الإدارة التنظيمية > الارتباطات > المناصب > التحقق من صحة بيانات التدرج الهرمي للمناصب‬**.

### <a name="specify-reason-codes-on-leave-types"></a>تحديد أكواد الأسباب في أنواع الإجازات

قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة

قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلبات إجازة. قد يكون هذا الشرط موجودًا بسبب سياسة الشركة أو المتطلبات التنظيمية. يمكنك تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية

تؤدي القدرة على تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات ليس فقط إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين ولكنها تساعد أيضًا على ضمان منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) لتمكين موظفي الموارد البشرية من الاطلاع على الأسباب التي تكمن خلف أرصدة أيام الإجازات.


[!INCLUDE[footer-include](../includes/footer-banner.md)]