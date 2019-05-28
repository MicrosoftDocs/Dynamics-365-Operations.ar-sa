---
title: ما الجديد أو المتغير في Dynamics 365 for Talent Core HR‏ (15 نوفمبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b90d4230fe1e666aba4075670f6df206e8df7ce9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517255"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>ما الجديد أو المتغير في Dynamics 365 for Talent Core HR‏ (15 نوفمبر 2018)

[!include [banner](includes/banner.md)]

**الإصدار 8.1.2045**

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.

## <a name="other-changesfixes"></a>التغييرات/الإصلاحات الأخرى

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>تعذر تغيير الوضع الحالي للموظف إلى وضع مفتوح في المستقبل.

تم إجراء تغيير لتمكين عمليات نقل المنصب عندما يكون المنصب متاحًا في المستقبل فقط. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>لا يتم عرض المنصب عند إنشاء موظف جديد

تم إجراء تغيير لعرض جميع المناصب المفتوحة المتاحة لتعيينها عند توظيف موظف جديد في Talent. ويتضمن هذا المناصب المسجلة أو إذا كانت المناصب محجوزة في المستقبل. سوف تظهر المناصب الآن بشكل صحيح بناءً على تاريخ بداية الموظف. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>يتم عرض تاريخ الإنهاء بناءً على إعدادات المستخدم

تم إجراء تغيير على قائمة الموظفين السابقة على حساب أي مقاصات منطقة زمنية للمنطقة الزمنية المفضلة للموظفين عند عرض تاريخ الإنهاء.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>لا تقوم أصناف العمل التي تم تعيينها إلى ارتباطاتي بعرض المعلومات الصحيحة.

من خلال هذا التغيير، سوف يعرض التنقل إلى عناصر أصناف العمل الفردية في القائمة المعلومات الصحيحة للعنصر المحدد. تحدث هذه المشكلة فقط مع خيارات الأمان المتقدمة.


## <a name="known-issue"></a>مشكلات معروفة​

- **المشكلة**: عند إضافة مرفق جديد إلى عامل، يظهر الزران **جديد** و**تحرير** بلون رمادي. 
- **الحل البديل:** قبل فتح صفحة المرفق، تأكد من أن مربعات الحقائق في صفحة **العامل** مغلقة. إذا كانت مربعات الحقائق مغلقة عند تحميل صفحة **العامل**، سيتم تمكين زر المرفقات (سوف يتم إصلاح هذه المشكلة في التحديث التالي للنظام الأساسي.)
