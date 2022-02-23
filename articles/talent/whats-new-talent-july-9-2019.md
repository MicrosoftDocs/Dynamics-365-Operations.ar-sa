---
title: ما الجديد والمتغير في Dynamics 365 Talent (9 يوليو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: feb39966d98fa7bde9a6bfad26b07fbd224da59b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528017"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>ما الجديد والمتغير في Dynamics 365 Talent (9 يوليو 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>قريبًا في Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>تظهر الموافقات على الوظائف في الصفحة الرئيسية

تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات. يستطيع المعتمدون مراجعة موافقاتهم ضمن **المعينة لك**، التي تعرض معرف الوظيفة والمسمى الوظيفي والمعتمدين الآخرين وتاريخ تعيين الوظيفة. يستطيع المستخدمين الذين يقومون بإرسال وظيفة للاعتماد مراجعة الوظائف الخاصة بهم ضمن **طلبتها**، التي تعرض المعتمدين الذين لا يزالوا يحتاجون إلى اعتماد الوظيفة التي تم إرسالها.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>تحديث النظام الأساسي 28 لـ Finance and Operations

للحصول على مزيد من التفاصيل حول تحديث النظام الأساسي 28 لـ Finance and Operations، راجع [ميزات المعاينة في تحديث النظام الأساسي 28 لـ Dynamics 365 Finance and Operations (يوليو 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>دعم الكيانات للحقول المخصصة في Common Data Service 

تدعم الكيانات التالية الحقول المخصصة: 

- **الخطة الثابتة للتعويض**
- **إعداد النقاط المرجعية للتعويض**
- **إعداد بند النقاط المرجعية للتعويض**
- **كود أرباح كشف الرواتب**
- **فترة الدفع**
- **حدث التعويض الثابت**
- **شبكة التعويض**

لعرض كافة الكيانات التي تم تحديثها في Talent:

1. حدد **إدارة النظام**، وحدد **الارتباطات**، ثم حدد **تكوين Common Data Service**.
2. حدد القائمة المنسدلة **اسم كيان CDS**. توجد جميع الكيانات المدرجة في الإصدار الأخير. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>إضافة حقل الاسم الكامل إلى كيان العامل في Common Data Service

تمت إضافة حقل **الاسم الكامل** إلى كيان **العامل**.

### <a name="full-time-equivalent-higher-than-10"></a>موظف بدوام الكامل أكبر من 1.0

يظهر تحذير الآن إذا تم إدخال قيمة أكبر من 1.0 لموظف بدوام كامل في أحد المناصب. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>توقف ظهور التحذير في صفحة العامل في حال عدم وجود توظيف ذي تاريخ مستقبلي

لن تتلقى بعد ذلك رسالة التي تشير إلى وجود توظيف مستقبلي عند الانتقال إلى صفحة **العامل** من قائمة **الموظفون المنتهية خدماتهم** في مساحة العمل **إدارة العاملين**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>تعذر حذف عملية أعمال في Talent

يمكنك الآن حذف عمليات الأعمال في مساحة عمل **عمليات الأعمال**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>لم يعد رصيد الإجازات يعرض صفرًا للخطط بدون استحقاقات عند استخدام الرصيد كفترة استحقاق

بإمكان الخطط التي تم إعدادها بدون استحقاقات أن تعرض الآن رصيدًا.

## <a name="in-preview"></a>قيد المعاينة

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>لا يتم تمكين ميزات المعاينة إلا في مثيلات بيئة الاختبار المعزول

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو **إنتاج** أو **بيئة اختبار معزولة**. تسمح أنواع مثيلات **بيئة اختبار معزولة** بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختبار المعزولة**، اتصل بـ [الدعم](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>تقييد أنواع الإجازات في طلب أيام الإجازات

يمكن للمؤسسات تقديم العديد من الأنواع المختلفة من الإجازات إلى الموظفين. ولكن، قد لا يكون مناسبًا للموظفين تقديم طلبات الإجازات لبعض أنواع الإجازات. قد تتم إدارة أنواع الإجازات هذه بواسطة الموارد البشرية بدلاً من ذلك. يمكنك في هذا الإصدار تكوين أنواع الإجازات التي يمكن للموظفين تقديم طلبات أيام الإجازة لها. 

## <a name="coming-soon-in-core-hr"></a>قريبًا من Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>عرض معلومات موسعة حول الأداء في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار المراجعات الجديدة التي يشارك موظفيهم في إدارتها. بالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة. 

### <a name="entities-supporting-custom-fields"></a>كيانات تدعم الحقول المخصصة

سيتم تمكين الكيانات التالية للحقول المخصصة في Common Data Service: 

- **نوع الإجازة**
- **الحساب البنكي للعامل**
- **تقويم العمل**
