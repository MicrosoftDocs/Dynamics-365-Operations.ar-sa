---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (23 يناير 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f97462f088fc1a3cb94f2a34204fc09f1cd66fb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460158"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-23-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent - Core HR‏ (23 يناير 2019)

**الإصدار 8.1.2121**

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Core HR.

## <a name="changes"></a>التغييرات

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>عدم عمل استيراد التعويض الثابت للموظفين عند إنشاء سجلات تعويض ثابت جديدة
تم إدخال تغيير على كيان التعويض الثابت للموظفين لاسترداد مستوى التعويض عند الاستيراد. قبل هذا الإصدار، كانت تظهر رسالة تشير إلى أن المستوى كان مطلوبًا.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>إزالة حقل "الحد الأدنى للرصيد" من مربع حوار "طلب إجازة"
تمت إزالة حقل **الحد الأدنى للرصيد** من مربع حوار **طلب إجازة**. يؤثر هذا التغيير على كافة المناطق التي يمكن فيها طلب زمن توقف.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>ترقية البيانات لمستويات التعويض التي لا تحدّث في جميع السيناريوهات
تم إدخال تغيير لتحديث مستوى التعويض في خطط التعويض الثابت. سيؤدي هذا التغيير إلى ملء مستوى التعويض على الخطط الثابتة للوظيفة المعينة للموظف.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>تتوفر معلومات المرتبات في صفحة "إدارة التغييرات" فقط عند تسجيل الدخول كمسؤول النظام
هذا التغيير يسمح للموظفين الذي يؤدون دور مسؤول المرتبات بالوصول إلى معلومات حول المرتبات‬ في صفحة **تغييرات المخطط الزمني > إدارة التغييرات** للمنصب.

### <a name="job-fields-default-to-positions"></a>تعيين قيم حقول الوظائف إلى المناصب بشكل افتراضي
عند تغيير الوظيفة في أحد المناصب، يتم تعيين قيم حقول الوظائف إلى المنصب بشكل افتراضي. سوف تظهر رسالة تنبيه توفر خيارًا يسمح بقبول القيم الافتراضية أو الاحتفاظ بالقيم الموجودة الخاصة بهذه الحقول.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>عدم ظهور فترة وضع الاختبار والتقويم للموظفين الذين سيتم تعيينهم في المستقبلي.
مع هذا التغيير، تمت إضافة الحقلين **فترة الاختبار** و **التقويم** إلى صفحة **إدارة التغييرات** للسماح بإدخال البيانات للموظفين السابقين واللاحقين.

### <a name="platform-update-23-for-finance-and-operations"></a>تحديث النظام الأساسي 23 لـ Finance and Operations
تم تضمين إصلاحات أخطاء ثانوية كجزء من تحديث النظام الأساسي 23 لـ Finance and Operations. للحصول على مزيد من المعلومات، راجع [ما الجديد أو المتغير في Dynamics 365 Finance and Operations platform update 23 (يناير 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
