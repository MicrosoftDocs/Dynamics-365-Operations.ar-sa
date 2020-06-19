---
title: نظرة عامة
description: في Dynamics 365 Human Resources، توفر مساحة عمل الإجازة والغياب اطار عمل مرنًا لإنشاء خطط إجازة جديدة وعمليات سير عمل لإدارة الطلبات وصفحة خدمه ذاتية بديهية للموظفين لطلب الإجازات.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428957"
---
# <a name="overview"></a>نظرة عامة

يساعدك Dynamics 365 Human Resources في توفير ميزات أجازه رائعه للعاملين. توفر مساحة عمل **الإجازة والغياب** اطارا مرنا لإنشاء خطط مغادره جديده ومهام سير عمل لأداره الطلبات وصفحه خدمه ذاتية بديهية للموظفين لطلب زمن توقف. تساعد التحليلات المؤسسة على قياس أرصدة الإجازات ومراقبتها واستخدامها لخطط إجازتك.

## <a name="set-up-leave-and-absence"></a>إعداد الإجازة والغياب

قبل أن تتمكن من إنشاء خطط الإجازات لموظفيك، يجب إجراء خطوات إعداد قليله:

- [تكوين مُحددات الإجازة والغياب](hr-leave-and-absence-parameters.md)
- [إنشاء تقويم مواعيد العمل](hr-leave-and-absence-working-time-calendar.md)
- [إنشاء سير عمل طلب إجازة](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>لإنشاء خطط إجازات وإدارتها

قبل إنشاء خطط الإجازات للعاملين، يتعين عليك إنشاء أنواع غياب وإجازات. بعد إنشاء خطة الإجازة، يمكنك تسجيل العمال في الخطة. يمكنك أيضا تشغيل عمليه الاستحقاق وإنشاء التنبيهات وعرض التحليلات الخاصة بخططك.

- [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md)
- [إنشاء خطة إجازة وغياب](hr-leave-and-absence-plans.md)
- [تعيين عمال لخطة إجازة](hr-leave-and-absence-enroll.md)
- [خطط استحقاق الإجازات والغياب](hr-leave-and-absence-accrue.md)
- [عرض تحليلات للإجازة والغياب](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>طلب زمن التوقف وأداره الطلبات

ويمكن للموظفين إرسال طلبات زمن التوقف وأدارتها في مساحة عمل **الخدمة الذاتية للموظفين**.

- [طلب إجازة](hr-employee-self-service-request-time-off.md)
- [إدارة طلبات الإجازة والغياب](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>المشاكل المعروفة المتعلقة بالإجازة والغياب

### <a name="rounding-precision"></a>دقة التقريب

لا يمكنك تعيين **دقة التقريب** عند تعيين **نوع التقريب**. يمكنك تعيين **دقه التقريب** فقط باستخدام كيان **نوع الإجازة والغياب**. 

1. من **أنواع الإجازة والغياب**، حدد **فتح في Excel** لفتح كيان **نوع الإجازة والغياب**.

2. بعد أن يتم فتح الملف وتمكينه، حدد **تصميم**.

3. في الجدول **نوع الإجازة والغياب**، حدد خيار القلم المراد تحريره.

4. حدد **RoundingPrecision** و**RoundingType**، ثم حدد **إضافة** للإضافة إلى قائمة الحقول.

5. حدد **تحديث**، ثم حدد **تم**.

6. أدخل أو حدد **نوع التقريب** لكل نوع من أنواع الإجازات إذا لم يتم تعيينه بعد. 

7. أدخل **دقة التقريب** للأنواع المناسبة.

8. حدد **نشر** لدفع التغييرات إلى Human Resources..

## <a name="leave-and-absence-preview-features"></a>ميزات مُعاينة الإجازة والغياب

يمكنك تجربه ميزات جديده لمراجعه الإجازة والغياب في بيئة **وضع الحماية**. للحصول على معلومات حول تشغيل ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

تتضمن ميزات المعاينة:

- **استحقاق الإجازات لكل شركة أو خطة‬** - يمكنك تشغيل عملية الاستحقاق إما لجميع الشركات أو لشركة واحدة. يمكنك أيضًا تشغيل عملية الاستحقاق لخطة غياب وإجازة معينة لشركة معينة. 

- **شراء إجازة** - يمكنك تمكين وإنشاء سياسات شراء الإجازات للموظفين لتقديم طلبات شراء. بإمكان الموظفين تقديم طلبات الشراء وتحديث أرصدتهم بشكل تلقائي لإظهار الطلب.  

- **إضافة مرفقات إلى طلبات الإجازة المعتمدة** - يمكنك إضافة مرفق إلى طلب الإجازة الذي تم تمت الموافقة عليه. 

