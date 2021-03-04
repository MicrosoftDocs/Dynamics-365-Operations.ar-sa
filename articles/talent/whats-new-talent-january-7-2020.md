---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (7‏ يناير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460217"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (7‏ يناير 2020)

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2697. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>لا يمكن حذف العاملين الذين ليس لديهم سجلات توظيف - (386157)

يقوم هذا التغيير باضافه خيار حذف في نموذج **عمال بلا عمل**. يظهر العاملون في هذا النموذج في حاله عدم وجود فرص توظيف مستقبليه أو نشطه أو تاريخيه للعامل. في هذا الإصدار ، يتم تمكين الحذف فقط لمسؤولي النظام. ومع ذلك ، في الأسبوع التالي ، سيتم تحديث الأمان للسماح لكافة المستخدمين الذين لديهم دور مساعد الموارد بازاله الموظفين دون امبلويمينتس. يمكنك أيضا اجراء هذه التغييرات يدويا باتباع الخطوات التالية.

1. انتقل إلى **تكوين الأمان**.
2. في علامة التبويب **الامتيازات**، قم بتصفية قائمة **الامتيازات** إلى  **الاحتفاظ بالعمال**.
3. في عمود **المراجع**، حدد **عرض عناصر القائمة**.
4. في **عرض عناصر القائمة**، حدد **HcmWOrkersWithoutEmployment**.
5. يمكنك تعيين إذن **الحذف** لمنحه.
6. حدد علامة التبويب **الكائنات غير المنشورة**.
7. حدد **نشر الكل**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]