---
title: إعداد صفحات مخصصه لعمليات تسجيل دخول المستخدمين
description: يوضح هذا الموضوع كيفية إنشاء صفحات مخصصة في Microsoft Dynamics 365 Commerce التي تقوم بمعالجة عمليات تسجيل الدخول المخصصة لمستخدمي مستأجري ميزة عمل-مستهلك (B2C) في Azure Active Directory (Azure AD).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a55da9683c43ac75109fd256e481b02a4d565914
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970068"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>إعداد صفحات مخصصه لعمليات تسجيل دخول المستخدمين


[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية إنشاء صفحات مخصصة في Microsoft Dynamics 365 Commerce التي تقوم بمعالجة عمليات تسجيل الدخول المخصصة لمستخدمي مستأجري ميزة عمل-مستهلك (B2C) في Azure Active Directory (Azure AD).

## <a name="overview"></a>نظرة عامة

لاستخدام الصفحات المخصصة المؤلفة في Dynamics 365 Commerce لمعالجة تدفقات تسجيل دخول المستخدم، ويجب إعداد سياسات Azure AD التي سيتم الرجوع إليها في بيئة التجارة. يمكنك تكوين سياسات "تسجيل الاشتراك وتسجيل الدخول،" وسياسات تطبيق B2C Azure AD لخصائص "تحرير ملف التعريف" و"إعادة تعيين كلمه المرور" باستخدام تطبيق Azure AD B2C. ويمكن بعد ذلك الرجوع إلى مستأجر Azure AD B2C وأسماء السياسات أثناء عملية التوفير التي تمت لبيئة التجارة باستخدام Microsoft Dynamics Lifecycle Services (LCS).

يمكن إنشاء صفحات التجارة المخصصة باستخدام تسجيل الدخول، أو التسجيل الاشتراك، أو تحرير ملف تعريف الحساب، أو الوحدة النمطية لإعادة تعيين كلمه المرور. بعد ذلك، يجب الرجوع إلى عناوين URL للصفحة التي يتم نشرها لهذه الصفحات المخصصة في تكوينات سياسة Azure AD B2Cفي مدخل Azure.

## <a name="set-up-b2c-policies"></a>إعداد سياسات B2C

بعد إعداد مستأجر Azure AD B2C وربطه ببيئة التجارة الخاصة بك، انتقل إلى صفحة **Azure AD B2C** في مدخل Azure، ثم في القائمة، ضمن **السياسات**، حدد **تدفقات المستخدم (السياسات)**.

![أمر تدفقات المستخدم (السياسات) في القائمة](./media/B2C_CustomPage_PoliciesMenu.png)

يمكنك الآن تكوين تدفقات تسجيل الدخول لمستخدم "تسجيل الاشتراك وتسجيل الدخول" و "تحرير ملف التعريف" و "إعادة تعيين كلمة المرور".

### <a name="configure-the-sign-up-and-sign-in-policy"></a>تكوين سياسة "تسجيل الاشتراك وتسجيل الدخول"

لتكوين سياسة "تسجيل الاشتراك وتسجيل الدخول"، اتبع الخطوات التالية.

1. حدد **تدفق مستخدم جديد**، ثم في علامة التبويب **الموصي به** ، حدد سياسة **تسجيل الاشتراك وتسجيل الدخول** .
1. أدخل اسمًا للسياسة (على سبيل المثال، **B2C\_1\_1** تسجيل الاشتراك وتسجيل الدخول).
1. في المقطع **موفري الهوية** ، حدد موفرو الهوية المراد استخدامهم للسياسة. يجب تحديد على الأقل **تسجيل الاشتراك بالبريد الإلكتروني** .
1. في العمود **سمة التجميع** ، حدد خانات الاختيار لـ **عنوان البريد الكتروني**،و **الاسم المحدد**، و **اللقب**.
1. في العمود **إرجاع مطالبة** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني**، و **الاسم المحدد**، و **موفر الهوية**، و **اللقب**، و **معرف الكائن الخاص بالمستخدم**.

    ![تحديد السمات والمطالبات](./media/B2C_SignInSignUp_Attributes.png)

1. حدد **موافق** لإنشاء السياسة.
1. انقر نقرا مزدوجًا فوق اسم السياسة الجديدة، ثم في جزء التنقل ،حدد **خصائص**.
1. قم بتعيين خيار **تمكين JavaScript لتخطيط الصفحة (معاينة)** إلى **تشغيل**.

    ![صفحه الخصائص للسياسة الجديدة](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> سيتم الإشارة إلى اسم السياسة بشكل كامل في بيئة التجارة. (سوف يتم تضمين البادئة **B2C\_1\_** في المرجع.) ولا يمكن إعادة تسمية السياسة بعد إنشائها. إذا كنت تستبدل سياسة موجودة لبيئة التجارة الخاصة بك، فيمكنك حذف السياسة الأصلية وإنشاء سياسة جديدة لها نفس الاسم. وبدلاً من ذلك، إذا تم توفير البيئة بالفعل، فيمكنك توفير اسم السياسة الجديدة من خلال طلب خدمة.

سوف تعود إلى هذه السياسة لإنهاء الإعداد بعد إنشاء الصفحات المخصصة. والآن، قم بإغلاق السياسة للعودة إلى صفحة **تدفقات المستخدم (السياسات)** في مدخل Azure.

### <a name="configure-the-profile-editing-policy"></a>تكوين سياسة "تحرير ملف التعريف"

لتكوين سياسة "تحرير ملف التعريف"، اتبع هذه الخطوات.

1. حدد **تدفق مستخدم جديد**، ثم في علامة التبويب **مستحسن** ، حدد سياسة **تحرير ملف التعريف** .
1. ادخل اسمًا للسياسة (على سبيل المثال، **B2C\_1\_EditProfile**).
1. في المقطع **موفري الهوية** ، حدد موفرو الهوية المراد استخدامهم للسياسة. يجب تحديد **تسجيل الدخول للحساب المحلي** كحد أدني.
1. في العمود **سمة التجميع** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني** و **اللقب**.
1. في العمود **إرجاع مطالبة** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني**، و **الاسم المحدد**، و **موفر الهوية**، و **اللقب**، و **معرف الكائن الخاص بالمستخدم**.
1. حدد **موافق** لإنشاء السياسة.
1. انقر نقرا مزدوجًا فوق اسم السياسة الجديدة، ثم في جزء التنقل ،حدد **خصائص**.
1. قم بتعيين خيار **تمكين JavaScript لتخطيط الصفحة (معاينة)** إلى **تشغيل**.

سوف تعود إلى هذه السياسة لإنهاء الإعداد بعد إنشاء الصفحات المخصصة. والآن، قم بإغلاق السياسة للعودة إلى صفحة **تدفقات المستخدم (السياسات)** في مدخل Azure.

### <a name="configure-the-password-reset-policy"></a>تكوين سياسة "إعادة تعيين كلمه المرور"

لتكوين سياسة "إعادة تعيين كلمة المرور"، اتبع هذه الخطوات.

1. حدد **تدفق مستخدم جديد**، ثم في علامة التبويب **معاينة** ، حدد سياسة **إعادة تعيين كلمة المرور الإصدار 1.1** .

    ![سياسة إعادة تعيين كلمة المرور في الإصدار 1.1 في علامة التبويب مُعاينة](./media/B2C_ForgetPassword_Menu.png)

1. أدخل اسمًا للسياسة (على سبيل المثال، **B2C\_1\_ForgetPassword**).
1. في القسم **موفرو الهوية** ، حدد **إعادة تعيين كلمة المرور باستخدام عنوان البريد الكتروني**.
1. في العمود **إرجاع مطالبة** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني**، و **الاسم المحدد**، و **اللقب**، و **معرف الكائن الخاص بالمستخدم**.

    ![المطالبات المحددة](./media/B2C_ForgetPassword_Attributes.png)

1. حدد **موافق** لإنشاء السياسة.
1. انقر نقرا مزدوجًا فوق اسم السياسة الجديدة، ثم في جزء التنقل ،حدد **خصائص**.
1. قم بتعيين خيار **تمكين JavaScript لتخطيط الصفحة (معاينة)** إلى **تشغيل**.

سوف تعود إلى هذه السياسة لإنهاء الإعداد بعد إنشاء الصفحات المخصصة. والآن، قم بإغلاق السياسة للعودة إلى صفحة **تدفقات المستخدم (السياسات)** في مدخل Azure.

## <a name="build-the-custom-pages"></a>إنشاء صفحات مخصصة

لإنشاء الصفحات المخصصة للتعامل مع وظائف تسجيل الدخول الخاصة بالمستخدم، اتبع الخطوات التالية.

1. في أدوات التأليف الخاصة بـ Commerce، انتقل إلى الموقع الخاص بك.
1. بناء القوالب الخمسة والصفحات الخمسة التالية:

    - قالب وصفحة **تسجيل الدخول** التي تستخدم الوحدة النمطية تسجيل الدخول.
    - قالب وصفحة **تسجيل الاشتراك** التي تستخدم الوحدة النمطية تسجيل الاشتراك.
    - قالب وصفحة **إعادة تعيين كلمة المرور** والتي تستخدم الوحدة النمطية إعادة تعيين كلمة المرور.
    - قالب وصفحة **التحقق من إعادة تعيين كلمة المرور** والتي تستخدم الوحدة النمطية التحقق من إعادة تعيين كلمة المرور.
    - قالب وصفحة **تحرير ملف التعريف** التي تستخدم الوحدة النمطية تحرير ملف تعريف الحساب.

عند إنشاء الصفحات، اتبع الإرشادات التالية:

- لكل صفحة أو وحدة نمطية، استخدم التخطيط والنمط الأكثر ملائمة لمتطلبات أعمالك.
- انشر كافة الصفحات وعناوين URL التي يجب استخدامها في إعداد Azure AD B2C.
- بعد نشر الصفحات وعناوين URL، قم بتجميع عناوين URL التي يجب استخدامها لتكوينات سياسة Azure AD B2C. تتم إضافة اللاحقة **?preloadscripts=true** إلى كل عنوان URL عند استخدامه.

> [!IMPORTANT]
> لا تعيد استخدام العناوين والتذييلات العامة التي لها ارتباطات نسبية. ونظرًا لاستضافة هذه الصفحات في المجال Azure AD B2C عند استخدامها، يجب فقط استخدام عناوين URL المطلقة لكافة الارتباطات.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>تكوين سياسات Azure AD B2C باستخدام معلومات صفحة مخصصة 

في مدخل Azure، ارجع إلى الصفحة **Azure AD B2C** ، ثم في القائمة، تحت **السياسات**، حدد **تدفقات المستخدم (السياسات)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>تحديث سياسة "تسجيل الاشتراك وتسجيل الدخول" باستخدام معلومات الصفحة المخصصة

لتحديث سياسة "تسجيل الاشتراك وتسجيل الدخول" باستخدام معلومات الصفحة المخصصة، اتبع الخطوات التالية.

1. في سياسة **تسجيل الاشتراك وتسجيل الدخول** التي قمت بتكوينها سابقًا، في جزء التنقل ، حدد **تخطيطات الصفحة**.
1. حدد تخطيط صفحة **تسجيل الاشتراك وتسجيل الدخول** .
1. قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.
1. في الحقل **URI للصفحة المخصصة** ، ادخل عنوان URL لتسجيل الدخول الكامل. ضمن اللاحقة **?preloadscripts=true** . على سبيل المثال، أدخل ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.
1. حدد تخطيط **صفحة تسجيل الدخول بالحساب المحلي** .
1. قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.
1. في الحقل **عنوان URI للصفحة المخصصة** ، ادخل عنوان URL للتسجيل الكامل للدخول. ضمن اللاحقة **?preloadscripts=true** . على سبيل المثال، أدخل ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.
1. في القسم **سمات المستخدم** ، اتبع الخطوات التالية:

    1. بالنسبة **لعنوان البريد الكتروني**، و **الاسم المحدد**، وسمات **اللقب** ، حدد **لا** في الحقل **يتطلب إجراء عملية تحقق**.
    1. بالنسبة لـ **الاسم المحدد** وسمات **اللقب** ، حدد **لا** في الحقل **اختياري** .

    ![تكوين سياسة صفحة تسجيل الدخول بالحساب المحلي](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>تحديث سياسة "تحرير ملف التعريف" باستخدام معلومات الصفحة المخصصة

لتحديث سياسة "تحرير ملف التعريف" باستخدام معلومات الصفحة المخصصة، اتبع الخطوات التالية.

1. في سياسة **تحرير ملف التعريف** الذي قمت بتكوينه سابقًا، في جزء التنقل، حدد **تخطيطات الصفحة**.
1. حدد تخطيط **صفحة تحرير ملف التعريف** .
1. قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.
1. في الحقل **عنوان URI للصفحة المخصصة** ، أدخل عنوان URL الكامل لتعديل الملف الشخصي. ضمن اللاحقة **?preloadscripts=true** . على سبيل المثال، أدخل ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.
1. في القسم **سمات المستخدم** ، اتبع الخطوات التالية:

    1. بالنسبة لـ **عنوان البريد الكتروني**، وسمات **الاسم المحدد** ، حدد **لا** في الحقل **يتطلب إجراء عملية تحقق** .
    1. بالنسبة لـ **الاسم المحدد** وسمات **اللقب** ، حدد **لا** في الحقل **اختياري** .

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>تحديث سياسة "إعادة تعيين كلمة المرور" باستخدام معلومات الصفحة المخصصة

لتحديث سياسة "إعادة تعيين كلمة المرور" باستخدام معلومات الصفحة المخصصة، اتبع الخطوات التالية.

1. في سياسة **إعادة تعيين كلمة المرور** الذي قمت بتكوينه سابقًا، في جزء التنقل، حدد **تخطيطات الصفحة**.
1. حدد تخطيط **صفحة كلمة المرور الجديدة** .
1. قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.
1. في الحقل **عنوان URI للصفحة المخصصة** ، أدخل عنوان URL الكامل لإعادة تعيين كلمة المرور. ضمن اللاحقة **?preloadscripts=true** . على سبيل المثال، أدخل ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.
1. حدد تخطيط **صفحة التحقق من الحساب** .
1. قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.
1. في الحقل **عنوان URI للصفحة المخصصة** ، أدخل عنوان URL الكامل لإعادة التحقق من كلمة المرور. ضمن اللاحقة **?preloadscripts=true** . على سبيل المثال، أدخل ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>تخصيص السلاسل النصية الافتراضية للتسميات والأوصاف

في مكتبة الوحدات النمطية، تتم تعبئة وحدات تسجيل الدخول النمطية مسبقًا باستخدام سلاسل نصية افتراضية للتسميات والأوصاف. يمكنك تخصيص هذه السلاسل في مجموعه تطوير البرامج (SDK) عن طريق تحديث القيم الموجودة في ملف global.json الخاص بتسجيل الدخول في الوحدة النمطية.

على سبيل المثال، يكون النص الافتراضي لارتباط كلمة المرور المنسية هو **كلمه المرور المنسية؟**. فيما يلي يظهر النص الافتراضي في صفحة تسجيل الدخول.

![النص الافتراضي لارتباط كلمة المرور المنسية في صفحة تسجيل الدخول](./media/B2C_SignUp_ModuleFace.png)

ومع ذلك، في ملف global.json للوحدة النمطية لتسجيل الدخول إلى مكتبة الوحدات النمطية، يمكنك تحرير النص إلى **هل نسيت كلمة المرور؟**، كما هو مبين في التوضيح التالي.

![تم تحديث نص الارتباط في ملف global.json الخاص بالوحدة النمطية تسجيل الدخول](./media/B2C_CustomizingStringsForModule.png)

بعد تحديث ملف global.json ونشر التغييرات، يظهر نص الارتباط الجديد في الوحدة النمطية تسجيل الدخول في كل من Commerce وصفحة تسجيل الدخول المباشر.

## <a name="additional-resources"></a>الموارد الإضافية

[تكوين اسم مجالك](configure-your-domain-name.md)

[نشر مستأجر التجارة الإلكترونية الجديد](deploy-ecommerce-site.md)

[إنشاء موقع تجارة إلكترونية](create-ecommerce-site.md)

[إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت](associate-site-online-store.md)

[إدارة ملفات robots.txt](manage-robots-txt-files.md)

[تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع](upload-bulk-redirects.md)

[إعداد مستأجر B2C في Commerce](set-up-B2C-tenant.md)

[تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce](configure-multi-B2C-tenants.md)

[إضافة الدعم إلى شبكة تسليم المحتوى (CDN)](add-cdn-support.md)

[تمكين اكتشاف المتجر استنادًا إلى الموقع](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]