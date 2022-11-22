---
title: إعداد مستأجر B2C في Commerce
description: يصف هذا المقال كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785117"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>إعداد مستأجر B2C في Commerce

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية إعداد مستأجري متاجرة بين عمل ومستهلك (B2C) في Azure Active Directory (Azure AD) لمصادقة موقع المستخدم في Dynamics 365 Commerce.

يقوم Dynamics 365 Commerce باستخدام Azure AD B2C لدعم بيانات اعتماد المستخدم وتدفقات المصادقة. بإمكان المستخدم التسجيل وتسجيل الدخول وإعادة تعيين كلمة المرور من خلال هذه التدفقات. يقوم Azure AD B2C بتخزين معلومات المصادقة الحساسة، مثل اسم المستخدم وكلمه المرور. سيقوم سجل المستخدم في مستأجر B2C بتخزين سجل حساب محلي B2C أو سجل موفر هوية اجتماعية B2C. سترتبط سجلات B2C هذه من جديد بسجل العميل في بيئة Commerce.

> [!WARNING] 
> سيُوقف Azure AD B2C عمليات سير عمل المستخدمين القدامى بحلول 1 أغسطس2021. لذلك، يجب أن تخطط لترحيل تدفقات المستخدم إلى الإصدار الجديد الموصى به. يوفر الإصدار الجديد تماثل ميزات وميزات جديده. يجب استخدام مكتبة الوحدات لإصدار Commerce رقم 10.0.15 أو إصدار أحدث مع عمليات سير عمل مستخدم B2C الموصى بها. لمزيد من المعلومات، راجع [عمليات سير عمل المستخدمين في Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > تأتي بيئات تقييم Commerce مع مستأجر Azure AD B2C المحمل مسبقًا لأغراض التوضيح. لا يلزم تحميل مستأجر Azure AD  B2Cالخاص بك باستخدام الخطوات التالية لبيئات التقييم.

> [!TIP]
> يمكنك حماية مستخدمي موقعك وتعزيز أمان مستأجري Azure AD B2Cمع حماية الهوية والوصول المشروط في Azure AD. لمراجعة القدرات المتاحة للمستأجرين في Azure AD من الفئة B2C Premium P1 وP2 المميزين، راجع [حماية الهوية والوصول المشروط إلى Azure AD ‏B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>متطلبات بيئة Dynamics الأساسية

قبل البدء، تأكد من أن بيئة Dynamics 365 Commerce وقناة التجارة الإلكترونية مكونة بشكل مناسب عن طريق تحقيق المتطلبات الأساسية التالية.

- قم بتعيين عمليات نقطة البيع **AllowAnonymousAccess** إلى "1" في المركز الرئيسي لـ Commerce:
    1. الانتقال إلى **عمليات نقطه البيع**.
    1. في شبكة العمليات، انقر بزر الماوس الأيمن وحدد **تخصيص**.
    1. حدد **إضافة حقل**.
    1. في قائمة الأعمدة المتوفرة، حدد عمود **AllowAnonymousAccess** لإضافته.
    1. حدد **تحديث**.
    1. بالنسبة للعملية **612** "إضافة عميل"، قم بتغيير **AllowAnonymousAccess** إلى "1."
    1. قم بتشغيل المهمة **1090 (السجلات)**.
- قم بتعيين السمة **يدوي** لحساب عميل التسلسل الرقمي إلى **لا** في المركز الرئيسي لـ Commerce:
    1. انتقل إلى **Retail وCommerce \> إعداد المراكز \> المعلمات \> معلمات الحسابات المدينة**.
    1. حدد **تسلسلات رقمية**.
    1. في صف **حساب العميل**، انقر نقرا مزدوجا فوق قيمة **كود التسلسل الرقمي**.
    1. في علامة التبويب السريعة **عام** للتسلسل الرقمي، قم بتعيين **يدوي** إلى **لا**.

بعد نشر بيئة Dynamics 365 Commerce الخاصة بك، يوصى أيضًا بـ [تهيئة البيانات الأولية](enable-configure-retail-functionality.md) في البيئة.

## <a name="next-steps"></a>الخطوات التالية

لمتابعة عملية إعداد مستأجر B2C في Commerce، تابع [إنشاء مستأجر B2C Azure AD موجود أو الارتباط به في Azure portal ](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>الموارد الإضافية

[إنشاء مستأجر B2C Azure AD موجود أو الارتباط به في Azure portal ](create-link-aad-b2c-tenant.md)

[إنشاء تطبيق B2C](create-b2c-app.md)

[إنشاء سياسات تدفق المستخدم](create-user-flow-policies.md)

[إضافة موفري الهوية الاجتماعية (اختياري)](add-social-identity-providers.md)

[تحديث Commerce headquarters بواسطة معلومات Azure AD B2C](update-hq-aad-b2c-info.md)

[تكوين مستأجر B2C في منشئ موقع Commerce](config-b2c-tenant-site-builder.md)

[معلومات B2C إضافية](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
