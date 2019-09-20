---
title: ما الجديد أو المتغير في Dynamics 365 for Talent (14 مارس 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ee8e076174acba8e706991f3086d6299a10945ec
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742483"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-14-2019"></a>ما الجديد أو المتغير في Dynamics 365 for Talent (14 مارس 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:

## <a name="changes-in-onboarding"></a>التغييرات في Onboarding
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
**الإصدار 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>إدارة الأداء لا تعمل في كافة السيناريوهات عند استخدام أدوار الأمان المكررة
تسمح التغييرات التي تم إجراؤها في هذا الإصدار بتمكين سيناريوهات إدارة الأداء عند استخدام الأدوار الجاهزة أو المكررة.

### <a name="mass-assign-checklists-to-workers"></a>تعيين قوائم الاختيار إلى العاملين بشكل مجمع
مع هذا التغيير، يمكنك الآن تحديد عدة موظفين وتعيين قائمة اختيار واحدة أو أكثر إلى هؤلاء الموظفين بشكل مجمع. 

### <a name="platform-update-24"></a>update 24 للنظام الأساسي
للحصول على تفاصيل إضافية حول Platform update 24، راجع [الميزات الجديدة أو المتغيرة في Finance and Operations platform update 24 (مارس 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). تتضمن التغييرات الهامة في platform 24 ما يلي: 

- تم تمكين التنبيهات في Talent.
- يتحاذى الآن شريط التنقل المحدث مع رأس Office.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>تحديث موقع المكتب يبدّل السياق إلى أعلى قائمة العاملين
مع الإصدار الحالي، لم يعد تغيير موقع المكتب يبدّل موقع سياق العامل الذي تعرضه عند تعيين موقع مكتب.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>لا يظهر تاريخ انتهاء تعيين المنصب بشكل صحيح على إجراءات توظيف العامل ونقله
تظهر الآن تواريخ انتهاء تعيين المنصب بشكل صحيح استنادًا إلى المنطقة الزمنية المفضلة لدى المستخدم عند استخدام الإجراءات.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>لا يسمح كيان وظيفة Common Data Service بتحديث حقلي نوع الوظيفة ومهمة الوظيفة
تتزامن الآن كيانات Common Data Service بشكل صحيح عند تحديثها باستخدام Common Data Service.

## <a name="coming-soon"></a>قريبًا

###  <a name="advanced-compensation-security-fixed-and-variable"></a>أمان التعويض المتقدم (التعويض الثابت والمتغير)
في الكثير من المؤسسات، قد يتوفر لدى مدراء التعويضات والمزايا حق الوصول إلى سجلات تعويض معينة فقط. وقد تكون هذه السجلات مخصصة للمدراء التنفيذيين أو الموظفين الإقليميين. مع هذا التغيير، سيتمكن قسم الموارد البشرية من إدارة خطط التعويض لمجموعات مختلفة من الموظفين في المؤسسة والمحافظة عليها. يمكن تعيين أدوار أمان إلى خطط التعويض الثابت والمتغير التي تحدد حق الوصول إلى الخطط وبيانات الموظفين ذات الصلة بها، على سبيل المثال، معلومات حول الرواتب أو سجلات المكافآت. وحدها الأدوار التي تم منح حق الوصول لها يمكنها معالجة التعويض لهؤلاء الموظفون.

###  <a name="email-support-for-alerts"></a>دعم البريد الإلكتروني للتنبيهات
مع إصدار Platform update 24، بإمكان المستخدمين إنشاء قواعد تنبيه ترسل بشكل تلقائي إعلامات بالبريد الإلكتروني إلى جهات الاتصال عند تشغيلها بواسطة حدث.

### <a name="duplicate-employee-check-interface-changes"></a>عمليات التحقق من الموظفين المكررين: تغييرات واجهة المستخدم
مع هذا التغيير، يتم الكشف عن التكرارات عند إدخال حقول الأسماء، وتعرض الحالة عدد التكرارات التي تم العثور عليها. يمكنك تحديد الارتباط المتوفر لفتح صفحة جديدة لتقييم ما إذا كان يجب استخدام المطابقة التي تم الكشف عنها. لا يفتح نموذج التكرارات بشكل تلقائي لتجنب مقاطعة إدخال البيانات.
