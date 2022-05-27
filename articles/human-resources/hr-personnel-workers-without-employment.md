---
title: العاملون بدون توظيف
description: يظهر العمال الذين ليس لديهم عمل مستقبلي أو نشط أو تاريخي مع مؤسستك في صفحة العمال بدون توظيف.
author: twheeloc
ms.date: 11/03/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3b2d5d470e780c708941fd3d08eae1a042b4c03
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689792"
---
# <a name="workers-without-employment"></a>العاملون بدون توظيف


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يظهر العمال الذين ليس لديهم عمل مستقبلي أو نشط أو تاريخي مع مؤسستك في صفحة **عمال بدون عمل**. يمكن أن يظهر العمال من هذا النوع عند استيراد عمال ليس لديهم سجل توظيف، أو عندما تحذف توظيف عامل عبر **العمال \> تاريخ التوظيف**.

بشكل افتراضي، تتوفر صفحة **العمال بدون عمل** للأدوار التالية:

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

   [![قائمة تصفية الامتيازات.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. في عمود **المراجع**، حدد **عرض عناصر القائمة**.

4. في **عرض عناصر القائمة**، حدد **HcmWorkersWithoutEmployment**.

   [![تحديد نموذج.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. قم بتعيين إذن **حذف** إلى **منح**.

6. حدد علامة التبويب **الكائنات غير المنشورة**.

7. حدد **نشر الكل**.

   [![نشر التغييرات.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
