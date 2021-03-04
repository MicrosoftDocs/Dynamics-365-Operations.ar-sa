---
title: ما الجديد أو المتغير في Dynamics 365 Talent (7 فبراير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
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
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 002dcd8253a0ab753ac9002e7027441db6d0b858
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460230"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (7 فبراير 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="interview-scheduling-enhancements"></a>تحسينات في جدولة المقابلات
تم إدخال تحسينات على تجربة جدولة المقابلات الشاملة. يمكنك الآن رؤية إمكانية توافر التقويم لمرشح داخلي واستخدام تقويم المرشح الداخلي لتقديم توصيات تتعلق بالجدولة. للحصول على مزيد من المعلومات، راجع [جدولة المقابلات والملاحظات‬](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>نشر إعلانات الوظائف في LinkedIn- إصلاح مشكلة عدم تطابق الشركة
تم إصلاح مشكلة حيث كانت إعلانات الوظائف المنشورة في LinkedIn تم تظهر تحت اسم الشركة غير الصحيح. للحصول على مزيد من المعلومات، راجع [إنشاء الوظائف والموافقة عليها ونشرها في Attract‬](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>عرض عنوان URL لموقع الوظائف في إعدادات المسؤول
يظهر الآن عنوان URL للصفحة الرئيسية لموقع الوظائف في **إعدادات المسؤول** ضمن **إدارة موقع الوظائف‬**.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

**الإصدار 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>دعم مستويات تعويض مختلفة مستويات على الوظائف
يسمح هذا التغيير بتحديد مستوى تعويض واحد أو أكثر على الوظيفة، مما يسمح بنطاقات تعويضات ثابتة للموظفين قد تختلف بين الخطط عند استخدام الوظيفة نفسها. 

على سبيل المثال:    
*الوظيفة* - *مستويات التعويض المقترنة* لمدير الحساب: B1 وB2 - يتضمن الآن كل مستوى مجموعة قيم محددة. B1 = الحد الأدنى 50,000، الحد الأوسط 60,000، الحد الأقصى 75,000 وB2 = الحد الأدنى 65,000، الحد الأوسط 74,000، الحد الأقصى 85,000. عند إنشاء تعويض ثابت للموظفين، استنادًا إلى قواعد الأهلية المحددة، بإمكان كل خطة ثابتة أن تشير الآن إلى الوظيفة نفسها وإلى مستويات مختلفة على الوظيفة. يسمح هذا الأمر بتعريف الخطط في مناطق/شركات مختلفة وبأن تشير إلى الوظيفة نفسها ولكن مع نطاقات مختلفة من دون تكرار الوظائف لأخذ هذه الاختلافات في الاعتبار.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>تمت إضافة حقل مستوى التعويض إلى كيان التعويض الثابت للموظفين 
تم تحديث كيان التعويض الثابت للموظفين، في هذا التحديث، بحيث يتضمن الحقل **مستوى التعويض**. تسّهل هذه الإضافة تحديث خطط التعويض الثابت للموظفين. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>تحديث مجموعة الوظائف عند تحديث وإنشاء مناصب جديدة
عند تغيير الوظيفة في أحد المناصب، سيستند إعداد **مجموعة الوظائف** الآن إلى الوظيفة المحددة بشكل افتراضي.

### <a name="performance-improvements-when-rendering-workspaces"></a>تحسينات الأداء عند عرض مساحات العمل
سيتم الآن تحميل علامات تبويب "التحليلات" في مساحات العمل فقط عند الوصول إلى هذه الصفحات. سيظهر مؤشر أثناء العرض الأولي للصفحة في الزاوية العلوية اليمنى من الصفحة.


[!INCLUDE[footer-include](../includes/footer-banner.md)]