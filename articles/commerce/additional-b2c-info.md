---
title: معلومات B2C إضافية
description: يقدم هذا المقال معلومات إضافية حول كيفية تعيين مستأجر بين العمل والمستهلك (B2C) في Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785205"
---
# <a name="additional-b2c-information"></a>معلومات B2C إضافية

[!include [banner](includes/banner.md)]

يقدم هذا المقال معلومات إضافية حول كيفية تعيين مستأجر بين العمل والمستهلك (B2C) في Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>ترحيل العملاء

إذا كنت ترغب في ترحيل سجلات العملاء من نظام موفر الهوية السابق، فيرجى العمل مع فريق Dynamics 365 Commerce لمراجعة احتياجات ترحيل العملاء.

للحصول على وثائق Azure AD B2C إضافة حول ترحيل العملاء، راجع [ترحيل العملاء إلى Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>سياسات مخصصة

للحصول على معلومات إضافية حول تخصيص تفاعلات وتدفقات سياسة Azure AD B2C بما يتجاوز ما تقدمه سياسات B2C القياسية، راجع [السياسات المخصصة في Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>المسؤول الثانوي

يمكن إضافة حساب مسؤول ثانوي اختياري في قسم **المستخدمون** في مستأجر B2C. قد يكون هذا الحساب مباشرًا أو عامًا. إذا أردت مشاركة حساب عبر موارد الفريق، يمكن أيضًا إنشاء حساب عام. بسبب حساسية البيانات المخزنة في Azure AD B2C، يجب مراقبة حساب عام عن كثب وفق ممارسات الأمان الخاصة بشركتك.

### <a name="set-up-a-custom-sign-in-domain"></a>إعداد مجال تسجيل دخول مخصص

يسمح لك Azure AD B2C بإعداد مجال تسجيل دخول مخصص لمستأجر Azure AD B2C. للحصول على الإرشادات، راجع [تمكين المجالات المخصصة لـ Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

إذا كنت تستخدم مجالاً مخصصًا لتسجيل الدخول، فيجب إدخال المجال في منشئ الموقع في Commerce.

لإدخال مجال تسجيل دخول مخصص في منشئ الموقع، اتبع الخطوات التالية.

1. في الركن العلوي الأيسر من منشئ الموقع، حدد مبدل الموقع، ثم حدد **إدارة المواقع**.
1. في جزء التنقل الأيسر، حدد **إعدادات المستأجر \> إعداد مصادق الموقع**.
1. في القسم **ملفات تعريف مصادقة الموقع**، حدد **إدارة**.
1. في القائمة المنبثقة إلى اليسار، حدد الزر **تحرير** (رمز القلم) بجانب ملف تعريف مصادقة الموقع الذي تريد إدخال مجال مخصص له.
1. في مربع الحوار **تحرير ملف تعريف مصادق الموقع**، ضمن **مجال مخصص لتسجيل الدخول**، أدخل مجالك المخصص لتسجيل الدخول (على سبيل المثال، 'login.fabrikam.com').

> [!WARNING]
> عند التحديث إلى مجال مخصص لمستأجر Azure AD B2C ، يؤثر التغيير على تفاصيل جهة إصدار المستأجر للرمز المميز المُنشأ. ستتضمن عندئذٍ تفاصيل جهة إصدار المجال المخصص بدلاً من المجال الافتراضي الذي يوفره Azure AD B2C. يقوم تكوين **جهة إصدار** مختلفة في Commerce headquarters (**البيع بالتجزئة والتجارة \> إعداد Headquarters \> المعلمات \> معلمات التجارة المشتركة‬ \> موفرو الهوية**) بتغيير تفاعل النظام مع مستخدمي الموقع، مما قد يؤدي إلى إنشاء سجل جديد للعميل إذا كان المستخدم يقوم بالمصادقة مقابل جهة الإصدار الجديدة. يجب اختبار أي تغييرات في المجال المخصص بدقة قبل التبديل إلى المجال المخصص في بيئة Azure AD B2C مباشرة.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد مستأجر B2C في Commerce](set-up-b2c-tenant.md)

[إنشاء مستأجر B2C Azure AD موجود أو الارتباط به في Azure portal ](create-link-aad-b2c-tenant.md)

[إنشاء تطبيق B2C](create-b2c-app.md)

[إنشاء سياسات تدفق المستخدم](create-user-flow-policies.md)

[إضافة موفري الهوية الاجتماعية (اختياري)](add-social-identity-providers.md)

[تحديث Commerce headquarters بواسطة معلومات Azure AD B2C](update-hq-aad-b2c-info.md)

[تكوين مستأجر B2C في منشئ موقع Commerce](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
