---
title: ما الجديد أو المتغير في Dynamics 365 Talent (14 فبراير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32f3bab38233833498ed566fa1558a023b3bc0dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460220"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (14 فبراير 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:

## <a name="changes-in-onboarding"></a>التغييرات في Onboarding
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية أخرى:
 
## <a name="changes-in-core-hr"></a>التغييرات في Core HR 
**الإصدار 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>لا يصدّر الكيان التعويض الثابت للموظفين جميع السجلات
نتيجة هذا التغيير، يقوم الآن كيان **التعويض الثابت للموظفين** بتصدير جميع السجلات. ويمكن استخدام الكيان لإنشاء وتحديث سجلات التعويض الثابت الموجودة للموظفين. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>لا يراعي تاريخ انتهاء التوظيف إعدادات المنطقة الزمنية المفضلة للموظف
تراعي الآن تواريخ انتهاء التوظيف المنطقة الزمنية المفضلة للمستخدم عند إنشاء أو إنهاء توظيف مع شركة.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>تظهر عناوين المملكة المتحدة في صفحة التحليلات كعناوين سويسرية
في هذا الإصدار، تم إجراء تغيير لتصحيح الترتيب الخاطئ في العناوين في التقرير "عدد الموظفين بالموقع" في **إدارة الأفراد**.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>عدم تعبئة كود الإنهاء في سجل تعيين منصب العامل‬ عند إنهاء المنصب
تم إجراء تغيير على كود "سبب الإنهاء" الافتراضي عند إنهاء تعيين المناصب للموظفين.

### <a name="new-entity-created-for-job-compensation-levels"></a>إنشاء كيان جديد لمستويات تعويض الوظيفة
تم إنشاء إطار عمل جديد لإدارة البيانات (DMF). يوفر الكيان العنصر اللازمة لإنشاء وتحديث مستويات التعويض وقيم السوق ومعلومات الاستطلاع لكل وظيفة معرّفة في النظام.


[!INCLUDE[footer-include](../includes/footer-banner.md)]