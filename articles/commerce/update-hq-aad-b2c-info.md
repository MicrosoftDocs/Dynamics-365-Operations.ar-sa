---
title: تحديث Commerce headquarters بواسطة معلومات Azure AD B2C جديدة
description: توضح هذه المقالة كيفية تحديث Microsoft Dynamics 365 Commerce headquartersبالمعلومات الجديدة Azure Active Directory (Azure AD) الخاصة بالشركة إلى المستهلك (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785218"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>تحديث Commerce headquarters بواسطة معلومات Azure AD B2C جديدة

[!include [banner](includes/banner.md)]

توضح هذه المقالة كيفية تحديث Microsoft Dynamics 365 Commerce headquartersبالمعلومات الجديدة Azure Active Directory (Azure AD) الخاصة بالشركة إلى المستهلك (B2C).

بعد إكمال خطوات تزويد Azure AD B2C أعلاه، يجب تسجيل تطبيق Azure AD B2C في بيئتك في Dynamics 365 Commerce.

لتحديث المقر الرئيسي بمعلومات Azure AD B2C الجديدة، اتبع هذه الخطوات.

1. في Commerce، انتقل إلى **معلمات Commerce المشتركة** وحدد **موفرو الهوية** في القائمة اليسرى
1. ضمن **موفرو الهوية**، قم بما يلي:
    1. في مربع **المُصدر** أدخل سلسة مُصدر موفر الهوية. للعثور على سلسلة المُصدر، راجع [الحصول على سلسلة المُصدر لإعداد المركز الرئيسي](#obtain-issuer-string-for-headquarters-setup) أدناه.
    1. في مربع **الاسم** أدخل اسمًا لسجل المصدر.
    1. في مربع **النوع** أدخل **Azure AD B2C (id_token)**.
1. ضمن **الأطراف المعتمِدة**، مع تحديد عنصر موفر هوية B2C أعلاه، قم بما يلي:
    1. في مربع **ClientID** أدخل رقم تطبيق B2C الخاص بك، والذي يمكنك العثور عليه في مربع **رقم التطبيق** في صفحة خصائص تطبيق B2C الخاص بك.
    1. في مربع **النوع** أدخل **عام**.
    1. في مربع **نوع المستخدم** أدخل **عميل**.
1. في جزء الإجراءات، حدد **حفظ**.
1. في مربع البحث في Commerce، ابحث عن **جدول التوزيع**
1. في قائمة التنقل اليسرة من صفحة **جداول التوزيع** حدد الوظيفة **1110 تكوين عمومي**.
1. في جزء الإجراءات، حدد **تشغيل الآن**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>الحصول على سلسلة المُصدر لإعداد المركز الرئيسي

للحصول على عنوان URL لسلسلة مُصدر موفر الهوية، اتبع الخطوات التالية.

1. في صفحة Azure AD B2C الخاصة بمدخل Azure، انتقل إلى سير عمل مستخدم **تسجيل الاشتراك وتسجيل الدخول**.
1. حدد **تخطيطات الصفحات** في قائمه التنقل إلى اليسار، ضمن **اسم التخطيط** حدد **صفحة تسجيل الاشتراك أو تسجيل الدخول الموحد**، ثم حدد **تشغيل سير عمل المستخدم**.
1. تأكد من تعيين تطبيقك إلى تطبيق Azure AD B2C المقصود الذي تم إنشاؤه أعلاه، ثم حدد ارتباط سير عمل المستخدم الذي يظهر ضمن رأس **تشغيل سير عمل المستخدم** الذي يتضمن ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (لا تحدد **تشغيل تدفق المستخدم**.) ستفتح علامة تبويب جديدة وتعرض بيانات تعريف للسياسة لتجميع سلسلة المُصدر.
1. في صفحة بيانات التعريف المعروضة في علامة تبويب المستعرض، انسخ سلسلة مُصدر موفر الهوية (قيمة **المُصدر** التي تبدأ بـ "https://" وتنتهي بـ "/v2.0/" ) والتي تبدو مماثلة للمثال التالي.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**أو**: لإنشاء نفس عنوان URL لبيانات التعريف يدويا، قم باجراء الخطوات التالية.

1. قم بإنشاء عنوان URL لعنوان بيانات التعريف بالتنسيق التالي باستخدام سياسة ومستأجر B2C: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - مثال: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. أدخل عنوان URL لعنوان بيانات التعريف في شريط العناوين في المستعرض.
1. في بيانات التعريف، انسخ عنوان URL لمصدر موفر الهوية (قيمة **"المصدر"**).
    - مثال: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>الخطوات التالية

لمتابعة عملية إعداد مستاجر B2C في Commerce، تابع [تكوين مستاجر B2C في منشئ مواقع Commerce .](config-b2c-tenant-site-builder.md)

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد مستأجر B2C في Commerce](set-up-b2c-tenant.md)

[إنشاء مستأجر B2C Azure AD موجود أو الارتباط به في Azure portal ](create-link-aad-b2c-tenant.md)

[إنشاء تطبيق B2C](create-b2c-app.md)

[إنشاء سياسات تدفق المستخدم](create-user-flow-policies.md)

[إضافة موفري الهوية الاجتماعية (اختياري)](add-social-identity-providers.md)

[تكوين مستأجر B2C في منشئ موقع Commerce](config-b2c-tenant-site-builder.md)

[معلومات B2C إضافية](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
