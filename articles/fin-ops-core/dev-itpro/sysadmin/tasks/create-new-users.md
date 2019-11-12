---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570511"
---
# <a name="create-new-users"></a>إنشاء مستخدمين جدد

[!include [task guide banner](../../includes/task-guide-banner.md)]

المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>إقران مستخدم بترخيص (أنواع التراخيص الجديدة فقط)
بالنسبة إلى العملاء الموجودين على أحد أنواع الترخيص الجديدة التي تمت اضافتها في 2019 أكتوبر، يجب إقران المستخدمين بترخيص. يُضاف المستخدمون المرتبطون بترخيص بشكل تلقائي كمستخدمي نظام ليس لديهم أي أدوار في المرة الأولى التي يقومون فيها بتسجيل الدخول. يتلقى المستخدمون الذين لا يقترنون بترخيص رسالة تحذير.

بإمكان مسؤولي النظام [تعيين تراخيص إلى المستخدمين](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) في [مركز إدارة Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>إضافة مستخدم جديد
1. انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.
2. في جزء الإجراء، حدد **جديد**.
3. في الحقل **معرف المستخدم**، أدخل معرفًا فريدًا للمستخدم. يجب إدخال معرف مستخدم.  
4. في حقل **اسم المستخدم**، أدخل اسم المستخدم‏‎.  
5. في الحقل **المجال**، أدخل مجال المستخدم.  
6. في الحقل‏‎ **الاسم المستعار**، أدخل الاسم المستعار للمستخدم.  
7. في حقل **الشركة**، حدد الشركة المطلوبة. 
8. على علامة التبويب السريعة **أدوار المستخدمين**، حدد **تعيين أدوار** من أجل [تعيين مستخدمين إلى أدوار الأمان](assign-users-security-roles.md)
9. حدد **موافق**.
10. حدد **حفظ**.

## <a name="import-users"></a>استيراد المستخدمين
1. في جزء الإجراءات، حدد **استيراد المستخدمين‬**.
2. في القائمة، قم بوضع علامة للصف المحدد.
3. حدد **استيراد المستخدمين‬**.
4. حدد **إغلاق**.

