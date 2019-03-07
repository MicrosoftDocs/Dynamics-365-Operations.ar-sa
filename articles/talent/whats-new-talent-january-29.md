---
title: ما الجديد أو المتغير في Dynamics 365 for Talent‏ (31‏ يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2019
ms.locfileid: "374724"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>ما الجديد أو المتغير في Dynamics 365 for Talent‏ (31‏ يناير 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 for Talent

**الإصدار 8.1.2128**

## <a name="core-hr-changes"></a>التغييرات الرئيسية Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>وقت الإجازة المأخوذ على بطاقة الأفراد لا يأخذ في الاعتبار تواريخ خطة الإجازة
بالنسبة إلى أولئك الأشخاص الذين ليس لديهم أي خطط للإجازة على سنة التقويم، تعرض الآن بطاقة **مأخوذ** الإجازات المأخوذة في سنة الإجازة المحددة بواسطة خطة. على سبيل المثال، إذا كانت فترة سنة الإجازة في المؤسسة تمتد من 1 يونيو إلى 30 مايو، وأخذ أحد الموظفين إجازة لمدة ثلاثة أيام في شهر ديسمبر، فستعرض البطاقة **مأخوذ** ثلاثة أيام في 15 يناير. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>مقادير الاستحقاق غير متطابقة مع أساس تاريخ المستوى
تمت إضافة خيارات جديدة إلى الإجازة أو الغياب (معلمات **الموارد البشرية**) لتمكين العملاء من تحديد الوقت الذي يكون فيه تاريخ أشهر خدمة الموظف ساري المفعول. بالنسبة إلى بعض المؤسسات، التاريخ هو نهاية الشهر، وقد يكون بداية الشهر التالي بالنسبة إلى البعض الآخر. على سبيل المثال، قد تمنح إحدى المؤسسات إجازة يوم 31 ديسمبر، في حين أن مؤسسة أخرى قد تمنح إجازة يوم 1 يناير. سيسمح لك هذا الخيار بتحديد وقت منح هذه الإجازة. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>إجراءات توظيف العاملين عالقة في الحالة "اكتمال سير العمل"
تم إدخال تغييرات لتصحيح مشكلة حيث انتهى عدد صغير من مهام سير العمل مع الحالة "اكتمال سير العمل". يجب أن تنتقل الآن مهام سير العمل الجديدة إلى الحالة "مكتمل" عند انتهاء سير العمل. وسيتم نقل مهام سير العمل في الحالة "اكتمال سير العمل" إلى الحالة "خطأ" للسماح بالتحديث أو الإزالة، إذا لزم الأمر. 
