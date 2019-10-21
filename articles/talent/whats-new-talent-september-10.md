---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR(10 سبتمبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
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
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 59cb0203422b7d81b5ca0077370fd9cbdb4a7f89
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010074"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-september-10-2018"></a>ما الجديد أو المتغير في Dynamics 365 Talent: Core HR‏ (10 سبتمبر 2018)

[!include [banner](includes/banner.md)]

**الإصدار 8.1.138.0**

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent: Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>السماح بوقت معين في اليوم في طلبات الإجازات (أنصاف الأيام)

إذا تم إعداد الإجازة والغياب بحيث يُرسل زمن التوقف بالأيام، يمكن الآن أيضًا تمكين تعريف نصف اليوم. وبعد ذلك، عندما يقوم المستخدمون بإرسال طلبات زمن التوقف،  يمكنهم تحديد إذا ما كان ذلك يعني قيامهم بطلب النصف الأول أو النصف الثاني من يوم الإجازة.

يتم إيقاف تشغيل هذا الخيار افتراضيًا. بالنسبة للموظفين الذين يطلبون النص الأول أو النصف الثاني من اليوم إجازة، يجب عليك تشغيل هذا الخيار في منطقة **الإجازة والغياب** لمُحددات الموارد البشرية.

امتياز الأمان لهذه الميزة هو الاحتفاظ بمحددات الموارد البشرية.

## <a name="validation-of-leave-and-absence-entries"></a>التحقق من إدخالات الإجازة والغياب

بناءً عل كيفية تكوين الإجازة، يتلقى الموظفون الذي يحاولون إرسال طلب إجازة أطول من يوم العمل الخاصة بهم، رسالة تحذير. بمعنى آخر، يتم تحذيرهم إذا حاولوا أخذ أكثر من يوم كامل إجازة في أي تاريخ محدد.

يتم دائمًا تشغيل ميزة التحقق من الصحة هذه. في أي وقت يتجاوز الموظف حد اليوم المُحدد، يتلقي تحذير في طلب الإجازة الخاصة به.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>حقول إضافية للعبارات الشرطية في مهام سير العمل.

تمت إضافة حقول إضافية إلى العبارات الشرطية وعناصر نائبة لمهام سير عمل متعددة في Core HR.

تمت إضافة الحقول التالية إلى عمليات سير عمل التعويض والإنهاء والنقل:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
-  TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- المهنة
- الاتحاد
- القسم
- PositionType
- CompLocation
- المسمى الوظيفي
- وظيفة
- JobType
- JobFamily
- JobFunction

تمت إضافة الحقول التالية إلى سير عمل المنصب:

- المهنة
- الاتحاد
- القسم
- PositionType
- CompLocation
- المسمى الوظيفي
- وظيفة
- JobType
- JobFamily
- JobFunction

تتوفر الحقول في العبارات الشرطية والعناصر النائبة لجميع المستخدمين الذين لديهم صلاحية الوصول لتكوين عمليات سير العمل المذكورة مسبقًا.

## <a name="navigation-to-attract-from-personnel-management"></a>الانتقال إلى Attract من إدارة الموظفين

في إدارة الموظفين، إذا لم يتم إعداد Attract، فمن ثم يوجه قسم**المرشحون المُراد توظيفهم** البدء باستخدام Attract بدلًا من عرض الرسالة "لم يتم العثور على أي شئ لعرضه هنا."

## <a name="other-changes"></a>التغييرات الأخرى

يشمل هذا الإصدار عددًا من إصلاحات الأخطاء الإضافية:

- عند توظيف مقاول، يجب ألا تتوافر علامة تبويب**التعويض** على صفحة الطلب/الإجراء.
- أثناء عملية إنهاء لطلب، لا يمكنك المتابعة حتى تحتوي كافة الحقول المطلوبة على بيانات.
- تمت معالجة مشاكل ترتيب الفرز وعرض التاريخ في تحليلات إدارة الموظفين.
