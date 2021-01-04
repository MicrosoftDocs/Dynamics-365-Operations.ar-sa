---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679830"
---
# <a name="create-new-users"></a>إنشاء مستخدمين جدد

[!include [banner](../../includes/banner.md)]

المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>إقران مستخدم بترخيص (أنواع التراخيص الجديدة فقط)
بالنسبة إلى العملاء الموجودين على أحد أنواع الترخيص الجديدة التي تمت اضافتها في 2019 أكتوبر، يجب إقران المستخدمين بترخيص. يُضاف المستخدمون المرتبطون بترخيص بشكل تلقائي كمستخدمي نظام ليس لديهم أي أدوار في المرة الأولى التي يقومون فيها بتسجيل الدخول.

بإمكان مسؤولي النظام [تعيين تراخيص إلى المستخدمين](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) في [مركز إدارة Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>إقران مستخدم خارجي بترخيص (أنواع التراخيص الجديدة فقط)
يحتاج المستخدمون الخارجيون للمستأجر الذي تم نشر البيئة فيه إلى تمثيلهم في دليل المستأجر المضيف (Azure Active Directory (Azure AD)) حتى يمكن تعيين تراخيص لهم. يجب إضافة هؤلاء المستخدمين الخارجيين إلى المستأجر في Azure AD كمستخدمين ضيوف ثم تعيين التراخيص المناسبة لهم. لمزيد من المعلومات، راجع [إضافة مستخدمي تعاون B2B Azure Active Directory في مدخل Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>إضافة مستخدم جديد
1. انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.
2. في جزء الإجراء، حدد **جديد**.
3. في الحقل **معرف المستخدم**، أدخل معرفًا فريدًا للمستخدم. يجب إدخال معرف مستخدم.  
4. في حقل **اسم المستخدم**، أدخل اسم المستخدم‏‎.  
5. في الحقل **المجال**، أدخل مجال المستخدم.  
6. في الحقل‏‎ **الاسم المستعار**، أدخل الاسم المستعار للمستخدم.  
7. في حقل **الشركة**، حدد الشركة المطلوبة. 
8. في علامة التبويب السريعة **أدوار المستخدمين**، حدد **تعيين أدوار** لتعيين مستخدمين إلى أدوار الأمان لمزيد من المعلومات، راجع ‏‫[تعيين مستخدمين إلى أدوار أمان‬](assign-users-security-roles.md).
9. حدد **موافق**.
10. حدد **حفظ**.

## <a name="import-users"></a>استيراد المستخدمين
1. انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.
2. في جزء الإجراءات، حدد **استيراد المستخدمين‬**.
3. في القائمة، قم بوضع علامة للصف المحدد.
4. حدد **استيراد المستخدمين‬**.
5. حدد **إغلاق**.

