---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (31‏ يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
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
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6dcdb37ba7a423e54a641c1d123f563a59648d46
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010304"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (31‏ يناير 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

**الإصدار 8.1.2128**

## <a name="core-hr-changes"></a>التغييرات الرئيسية Core HR

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>وقت الإجازة المأخوذ على بطاقة الأفراد لا يأخذ في الاعتبار تواريخ خطة الإجازة
بالنسبة إلى أولئك الأشخاص الذين ليس لديهم أي خطط للإجازة على سنة التقويم، تعرض الآن بطاقة **مأخوذ** الإجازات المأخوذة في سنة الإجازة المحددة بواسطة خطة. على سبيل المثال، إذا كانت فترة سنة الإجازة في المؤسسة تمتد من 1 يونيو إلى 30 مايو، وأخذ أحد الموظفين إجازة لمدة ثلاثة أيام في شهر ديسمبر، فستعرض البطاقة **مأخوذ** ثلاثة أيام في 15 يناير. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>مقادير الاستحقاق غير متطابقة مع أساس تاريخ المستوى
تمت إضافة خيارات جديدة إلى الإجازة أو الغياب (معلمات **الموارد البشرية**) لتمكين العملاء من تحديد الوقت الذي يكون فيه تاريخ أشهر خدمة الموظف ساري المفعول. بالنسبة إلى بعض المؤسسات، التاريخ هو نهاية الشهر، وقد يكون بداية الشهر التالي بالنسبة إلى البعض الآخر. على سبيل المثال، قد تمنح إحدى المؤسسات إجازة يوم 31 ديسمبر، في حين أن مؤسسة أخرى قد تمنح إجازة يوم 1 يناير. سيسمح لك هذا الخيار بتحديد وقت منح هذه الإجازة. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>إجراءات توظيف العاملين عالقة في الحالة "اكتمال سير العمل"
تم إدخال تغييرات لتصحيح مشكلة حيث انتهى عدد صغير من مهام سير العمل مع الحالة "اكتمال سير العمل". يجب أن تنتقل الآن مهام سير العمل الجديدة إلى الحالة "مكتمل" عند انتهاء سير العمل. وسيتم نقل مهام سير العمل في الحالة "اكتمال سير العمل" إلى الحالة "خطأ" للسماح بالتحديث أو الإزالة، إذا لزم الأمر. 
