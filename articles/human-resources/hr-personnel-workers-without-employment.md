---
title: العاملون بدون توظيف
description: يظهر العمال الذين ليس لديهم عمل مستقبلي أو نشط أو تاريخي مع مؤسستك في نموذج العمال بدون عمل.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051703"
---
# <a name="workers-without-employment"></a>العاملون بدون توظيف

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يظهر العمال الذين ليس لديهم عمل مستقبلي أو نشط أو تاريخي مع مؤسستك في نموذج **العمال بدون عمل**. يمكن أن يظهر العمال بهذه الحالة عند استيراد عمال ليس لديهم سجل توظيف ، أو عند حذف توظيف عامل من خلال **العمال > سجل التوظيف**.

بشكل افتراضي ، يتوفر نموذج **العمال بدون عمل** للأدوار التالية.

- مساعد الموارد البشرية
- مدير الموارد البشرية
- مسؤول التعيين
- مدير التعويض والميزات
- مسؤول المرتبات
- مدير المرتبات
- مدير التدريب

في قائمة **العمال بدون عمل**، يمكنك حذف الأفراد المدرجين. بشكل افتراضي ، يتم منح هذا الامتياز لدور مساعد الموارد البشرية. يمكنك منح هذا الامتياز للأدوار الأخرى من خلال الخطوات التالية:

1. حدد **إدارة النظام**، ثم حدد علامة التبويب **تكوين الأمان**.

2. في علامة التبويب **الامتيازات**، قم بتصفية قائمة **الامتيازات** إلى  **الاحتفاظ بالعمال**.

   [![قائمة تصفية الامتيازات](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. في عمود **المراجع**، حدد **عرض عناصر القائمة**.

4. في **عرض عناصر القائمة**، حدد **HcmWorkersWithoutEmployment**.

   [![تحديد نموذج](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. قم بتعيين إذن **حذف** إلى **منح**.

6. حدد علامة التبويب **الكائنات غير المنشورة**.

7. حدد **نشر الكل**.

   [![نشر التغييرات](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]