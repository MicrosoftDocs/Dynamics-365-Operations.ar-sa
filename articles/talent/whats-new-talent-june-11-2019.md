---
title: ما الجديد والمتغير في Dynamics 365 for Talent (11 يونيو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a1413ea43e852c78ede227b69c0f49c07944a872
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741603"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a>ما الجديد والمتغير في Dynamics 365 for Talent (11 يونيو 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="search-engine-optimization-for-job-posts"></a>تحسين محرك البحث لعمليات نشر المهام

بعد قيامك بتشغيل **تحسين محرك البحث** في Dynamics 365 for Talent: مركز الإدارة‬‏‫‬‏‫ في Attract، يقوم Attract بإعلام واجهة برمجة التطبيق (API) في فهرسة Google لتتبع صفحة الويب في حالة تنشيط وظيفة جديدة ونشرها أو تحديث وظيفة موجودة. وبهذه الطريقة، ستظهر الوظيفة في نتائج البحث في Google ومحركات البحث الأخرى.

وبالمثل، في حالة إلغاء نشر وظيفة، يقوم Attract بإعلام واجهة برمجة تطبيق الفهرسة ليتوقف ظهور الوظيفة التي تم إلغاء نشرها عن الظهور في نتائج البحث.

> [!NOTE]
> لا تحتوي متتبعات ارتباطات الويب علي إطار زمني معرف لتتبع ارتباطات صفحات الويب أو تحديث نتائج البحث.

## <a name="coming-soon-in-attract"></a>قريبًا في Attract

### <a name="job-approvals-appear-on-the-home-page"></a>تظهر الموافقات على الوظائف في الصفحة الرئيسية

تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات. يستطيع المعتمدون مراجعة موافقاتهم ضمن **المعينة لك**، التي تعرض معرف الوظيفة والمسمى الوظيفي والمعتمدين الآخرين وتاريخ تعيين الوظيفة. يستطيع المستخدمين الذين يقومون بإرسال وظيفة للاعتماد مراجعة الوظائف الخاصة بهم ضمن **طلبتها**، التي تعرض المعتمدين الذين لا يزالوا يحتاجون إلى اعتماد الوظيفة التي تم إرسالها.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 for Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2337.

### <a name="platform-update-27"></a>update 27 للنظام الأساسي

للحصول على مزيد من التفاصيل حول Platform update 27، راجع [ميزات المعاينة في Dynamics 365 for Finance and Operations platform update 27 (مايو 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>مساحة عمل إدارة الميزات في Talent

تتيح مساحة عمل **إدارة الميزات** في **إدارة النظام** عرض الميزات التي تم تسليمها في كل إصدار من الإصدارات وتمكينها وتعطيلها وجدولتها. بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل. ويمكنك استخدام مساحة عمل **إدارة الميزات** لتشغيلها وعرض الوثائق الخاصة بها.

### <a name="common-data-service-entity-support-for-custom-fields"></a>دعم كيان Common Data Service للحقول المخصصة

يدعم كيان إصدار الوكالة الآن الحقول المخصصة.

### <a name="new-common-data-service-entities"></a>كيانات Common Data Service جديدة

تمت إضافة كيان مجموعة المهام.

## <a name="in-preview"></a>قيد المعاينة

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>لن يتم تمكين ميزات المعاينة إلا في بيئات الاختبار المعزولة‬

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

عند توفير مثيل جديد من Talent‬، يمكنك الاشار إلى ما إذا كان نوع المثيل هو إنتاج أو ابيئة اختبار معزولة. يسمح نوع المثيل "بيئة اختبار معزولة" بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختبار المعزولة**، اتصل بـ [الدعم](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>تقييد أنواع الإجازات في طلب أيام الإجازات

يمكن للمؤسسات تقديم العديد من أنواع الإجازات إلى الموظفين. ولكن، قد لا يكون مناسبًا للموظفين تقديم طلبات الإجازات لبعض أنواع الإجازات. وقد تتم إدارة أنواع الإجازات هذه بواسطة الموارد البشرية (HR) بدلاً من ذلك. يمكنك في هذا الإصدار تكوين أنواع الإجازات التي يمكن للموظفين تقديم طلبات أيام الإجازة لها. 

## <a name="coming-soon-in-core-hr"></a>قريبًا من Core HR

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>عرض معلومات موسعة حول أداء التقارير في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار مراجعات جديدة. وبالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة.

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

سيتمكن الموظفون والمديرون وموظفي الموارد البشرية من طباعة مراجعة أداء الموظف.
