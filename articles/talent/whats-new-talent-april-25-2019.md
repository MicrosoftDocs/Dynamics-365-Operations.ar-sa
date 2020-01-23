---
title: ما الجديد أو المتغير في Dynamics 365 Talent (23 أبريل 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cbafea9063844dd3f19e5828ab37632e04591f18
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897870"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-23-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (23 أبريل 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2253. تشير الأرقام الموجودة بين أقواس إلى أرقام الدعم في Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>دعم كيان Common Data Service للحقول المخصصة
مع إصدار هذا الأسبوع، تدعم الكيانات التالية الحقول المخصصة: مستوى التعويض وخيار الميزة ونوع المهارة ومنطقة التعويض.

### <a name="additional-odata-entities-302992"></a>كيانات OData الإضافيه (302992)
الكيانات التالية مدعومة الآن في OData: الخبرة المهنية للعامل وتعليم العامل.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>مرفقات دفتر يومية الأداء للمدراء والموظفين (308248)
مع هذا الإصدار، أصبحت المرفقات متاحة الآن للمدراء والموظفين عند إنشاء إدخالات دفتر يومية الأداء وتحديثها.

### <a name="employee-rehire-flag-always-available-310047"></a>علامة إعادة توظيف الموظف متوفرة دائمًا (310047)
يتوفر الآن خيار إعادة توظيف الموظفين للتحديث خارج عملية الإنهاء. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>لا يمكن تغيير اسم **طريقة دفعي** (308815)
تم تمكين التخصيص للسماح بتغيير‏‎ تسمية **طريقة دفعي** في الخدمة الذاتية للموظف.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>لا يمكن حذف الأبعاد المالية في مقابل المنصب (293908)
يمكن الآن إزالة الأبعاد المالية عند طلب تغيير لمنصب موجود والأبعاد المالية عبر حدود الشركة. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>العميل غير قادر على إعادة نشر البيانات في Talent عند فتح البيانات من Excel‏ (302955)
يعمل هذا التغيير على تصحيح مشكلة في النشر عند استخدام جداول مرتبطة.

## <a name="in-preview"></a>قيد المعاينة

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>السماح بتعيين أكواد الأسباب على أنواع الإجازات
قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة
قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلب إجازة. قد يعود سبب ذلك إلى سياسة الشركة أو إلى متطلبات تنظيمية. يمكنك الآن تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية
يؤدي تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات ليس فقط إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين ولكنه يضمن أيضًا منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) للاطلاع على الأسباب التي تكمن خلف الأرصدة.

## <a name="coming-soon"></a>قريبًا

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>تحسينات في واجهة المستخدم للتحقق من وجود موظفين مكررين
مع هذا التغيير، يتم الكشف عن التكرارات عند إدخال حقول الأسماء، وتعرض الحالة عدد التكرارات التي تم العثور عليها. يمكنك تحديد الارتباط المتوفر لفتح صفحة جديدة لتقييم ما إذا كان يجب استخدام المطابقة التي تم الكشف عنها. لتجنب مقاطعة إدخال البيانات، لا يفتح نموذج التكرارات بشكل تلقائي.
## <a name="known-issues"></a>مشكلات معروفة

### <a name="email-support-for-alerts"></a>دعم البريد الإلكتروني للتنبيهات
في إصدار Platform update 26 لـ Finance and Operations بإمكان المستخدمين إنشاء قواعد تنبيه ترسل بشكل تلقائي إعلامات بالبريد الإلكتروني إلى جهات الاتصال عند تشغيل الإعلامات بواسطة حدث.
