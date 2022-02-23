---
title: لا يستطيع مستخدمو Attract التقدم للوظائف من مدخل المهن
description: يشرح هذا الموضوع كيفية استكشاف مشكلة حيث يتعذر على مستخدمي Attract التقدم للوظائف من مدخل الوظائف.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460176"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>لا يستطيع مستخدمو Attract التقدم للوظائف من مدخل المهن

[!include [banner](includes/banner.md)]

## <a name="issue"></a>إصدار

لا يستطيع مستخدمو Attract التقدم للوظائف من مدخل الوظائف. عندما يحاولون التقدم لوظيفة تم إنشاؤها في Dynamics 365 Talent: Attract، يقوم المتصفح بتحميل الصفحة بشكل مستمر ولا يكمل الإجراء.

## <a name="cause"></a>السبب

تحدث هذه المشكلة عندما لا يكون لفريق Talent Relationship دور مستخدم Talent.

## <a name="resolution"></a>الدقة

قم بتعيين دور مستخدم Talent إلى فريق Talent Relationship.

1. سجل الدخول إلى [مركز إدارة Power Platform](https://admin.powerplatform.microsoft.com) باستخدام أيٍّ من بيانات اعتماد المسؤول التالية:

   - إدارة Dynamics 365
   - مسؤول عمومي
   - مسؤول Power Platform

2. في جزء التنقل، حدد **البيئات**، ثم حدد البيئة التي يتم فيها تعيين دور مستخدم Talent إلى فريق Talent Relationship.

   ![تحديد بيئة](./media/attract-troubleshoot-career-portal-select-environment.png)

3. في جزء **البيئات**، حدد **عنوان URL للبيئة** وقم بتسجيل الدخول إلى مدخل مسؤول البيئة (على سبيل المثال، https:<orgname>.crm.dynamics.com).

4. حدد **الإعدادات**، وحدد **النظام**، ثم حدد **الأمان**.

   ![الانتقال إلى الأمان](./media/attract-troubleshoot-career-portal-security.png)

5. حدد **Teams**.

   ![تحديد Teams](./media/attract-troubleshoot-career-portal-security-teams.png)

6. ابحث عن **فريق Talent Relationship** في مربع البحث، ثم حدد الفريق من نتائج البحث.

7. حدد **إدارة الأدوار** من الشريط.

8. في مربع الحوار **إدارة أدوار الفريق**، حدد **مستخدم Talent** من قائمة الأدوار المتاحة، ثم حدد **موافق** لتطبيق الدور.

   ![تطبيق الدور](./media/attract-troubleshoot-career-portal-apply-role.png)

9. اختبر تغييراتك:

   1. قم بتسجيل الدخول إلى مدخل الوظائف من نافذة مستعرض جديدة.
   2. تقدم للوظيفة من مدخل الوظائف. 