---
title: ما الجديد أو المتغير في Dynamics 365 Talent (20 أغسطس 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9ab26ba80ea53b4138c3aaa60f93815af64987d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460250"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-august-20-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (20 أغسطس 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="simplified-apply-experience-for-candidates"></a>تجربة مبسطة لتقديم طلبات التوظيف للمرشحين 

تتوفر الآن تجربة مبسطة لتقديم طلبات التوظيف للمرشحين في المعاينة العامة. عند تمكينها، سيتمكن المرشحون من تقديم طلب الحصول على وظيفة ما باستخدام سيرتهم الذاتية، أو باستخدام **التقدم بطلب عبر LinkedIn** (في حال تمكينه) أو باستخدام استمارة التقديم الموجودة. ومع هذه التغييرات، باستطاعة المرشحين إرسال استمارة تقديم للحصول على الوظيفة مع القليل من الحقول التي تحتاج إلى إدخال يدوي. للحصول على معلومات حول كيفية تمكين هذه الميزة، راجع [الوصول إلى ميزات المعاينة في Microsoft Dynamics 365 Talent](./access-preview-feature.md#enable-or-disable-preview-features).

### <a name="view-rejection-comments-as-part-of-application-activity"></a>عرض تعليقات الرفض كجزء من نشاط استمارة التقديم

تظهر الآن أسباب وتعليقات على علامة التبويب **النشاط** التابعة للمرشح. يمكنك أيضًا التمييز بين استمارات التقديم المفتوحة وتلك المغلقة.  

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Core HR. تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2429.

### <a name="in-preview"></a>قيد المعاينة

#### <a name="streamlined-employee-entry-and-navigation"></a>إدخال الموظفين والتنقل المبسط

تتوفر هذه الوظيفة الآن في بيئات الاختبار المعزولة. لتشغيل هذه الميزة، انتقل إلى **إدارة النظام > الارتباطات > الإعداد > محددات النظام‬ > ميزات المعاينة‬**. حدد **نموذج العامل المحسن والتنقل‬**. سيؤدي ذلك إلى تمكين هذه التغييرات لكافة المستخدمين. يمكنك إيقاف تشغيل هذا الخيار في اي وقت.

لمزيد من المعلومات، راجع [إدخال الموظفين والتنقل المبسط‬](./streamlined-employee-entry.md).

#### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>لا يتم تمكين ميزات المعاينة إلا في مثيلات بيئة الاختبار المعزول

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو إنتاج أو بيئة اختبار معزولة. تسمح أنواع مثيلات بيئة اختبار معزولة بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل الإنتاج. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل بيئة الاختبار المعزولة، اتصل بـ الدعم لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](./provisioning-talent.md).

#### <a name="view-extended-information-for-performance-in-manager-self-service"></a>عرض معلومات موسعة حول الأداء في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار مراجعات جديدة. بالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة.

### <a name="coming-soon"></a>قريبًا

#### <a name="platform-update-29-for-finance-and-operations"></a>تحديث النظام الأساسي 29 لـ Finance and Operations

للحصول على مزيد من التفاصيل حول تحديث النظام الأساسي 29 لـ Finance and Operations، راجع [ميزات المعاينة Dynamics 365 Finance and Operations تحديث النظام الأساسي 29 (أكتوبر 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
