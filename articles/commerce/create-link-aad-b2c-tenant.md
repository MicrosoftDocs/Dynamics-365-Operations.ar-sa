---
title: إنشاء مستأجر Azure AD B2C موجود في مدخل Azure أو الارتباط به
description: توضح هذه المقالة كيفية إنشاء مستأجر أو ارتباط موجود في Azure Active Directory (Azure AD) الخاصة بالعمل والمستهلك في بوابة Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785208"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>إنشاء مستأجر Azure AD B2C موجود في مدخل Azure أو الارتباط به

[!include [banner](includes/banner.md)]

توضح هذه المقالة كيفية إنشاء مستأجر أو ارتباط في Azure Active Directory (Azure AD) الخاصة بالعمل والمستهلك (B2C) في Microsoft Azure portal. ولمزيد من المعلومات، راجع [البرنامج التعليمي: إنشاء Azure Active Directory مستأجر B2C](/azure/active-directory-b2c/tutorial-create-tenant).

لإنشاء مستاجر Azure AD B2C موجود أو لربطه في Azure portal، اتبع الخطوات التالية.

1. سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).
1. من قائمة مدخل Azure، حدد **إنشاء مورد**. احرص على استخدام الاشتراك والدليل الذي سيتم توصيله ببيئة Commerce.

    ![إنشاء مورد في مدخل Azure.](./media/B2CImage_1.png)

1. انتقل إلى **الهوية \> Azure Active Directory B2C**.
1. عند وصولك إلى صفحة **إنشاء مستأجر B2C جديد أو الارتباط بمستأجر موجود**، استخدم أحد الخيارات أدناه الأكثر ملاءمة لاحتياجات شركتك:

    - **إنشاء مستأجر Azure AD B2C جديد**: استخدم هذا الخيار لإنشاء مستأجر Azure AD B2C جديد.
        1. حدد **إنشاء مستأجر Azure AD B2C جديد**.
        1. ضمن **اسم المؤسسة**، أدخل اسم المؤسسة.
        1. ضمن **اسم المجال الأولي**، أدخل اسم المجال الأولي‏‎.
        1. في **البلد أو المنطقة**، حدد البلد أو المنطقة.
        1. حدد **إنشاء** لإنشاء المستأجر.

     ![إنشاء مستأجر Azure AD جديد.](./media/B2CImage_2.png)

     - **ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**: استخدم هذا الخيار إذا كان لديك مستأجر Azure AD B2C تريد الارتباط به.
        1. حدد **ربط مستأجر Azure AD B2C موجود باشتراكي في Azure**.
        1. في **مستأجر Azure AD B2C**، حدد مستأجر B2C المناسب. إذا ظهرت الرسالة "لم يتم العثور على مستأجري B2C مؤهلين" في مربع التحديد، فهذا يعني عدم وجود مستأجر B2C مؤهل ويجب إنشاء واحد جديد.
        1. في **مجموعة الموارد**، حدد **إنشاء جديد**. أدخل **اسم** مجموعة الموارد التي ستحتوي على المستأجر، وحدد، **موقع مجموعة الموارد**، ثم حدد **إنشاء**.

    ![ربط مستأجر Azure AD B2C موجود باشتراك Azure.](./media/B2CImage_3.png)

1. بعد إنشاء دليل Azure AD B2C الجديد (قد يستغرق هذا الأمر لحظات قليلة)، سيظهر ارتباط إلى الدليل الجديد على لوحة المعلومات. سيوجهك هذا الارتباط إلى صفحة "مرحباً بك في Azure Active Directory B2C".

    ![ارتباط إلى دليل Azure AD Directory جديد](./media/B2CImage_4.png)

> [!NOTE]
> إذا كانت لديك اشتراكات متعددة داخل حساب Azure أو قمت بإعداد مستأجر B2C بدون إنشاء ارتباط إلى اشتراك نشط، سيقوم شعار **استكشاف الأخطاء وإصلاحها** بتوجيهك لربط المستأجر باشتراك. حدد رسالة استكشاف الأخطاء وإصلاحها واتبع الإرشادات لحل مشكلة الاشتراك.

تبين الصورة التالية مثالاً عن شعار **استكشاف الأخطاء وإصلاحها في Azure AD B2C**.

![تحذير يشير إلى عدم وجود اشتراك نشط لدى الدليل.](./media/B2CImage_5.png)

## <a name="next-steps"></a>الخطوات التالية

لمتابعة عملية إعداد مستأجر B2C في Commerce، تابع [إنشاء تطبيق B2C](create-b2c-app.md).

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد مستأجر B2C في Commerce](set-up-b2c-tenant.md)

[إنشاء تطبيق B2C](create-b2c-app.md)

[إنشاء سياسات تدفق المستخدم](create-user-flow-policies.md)

[إضافة موفري الهوية الاجتماعية (اختياري)](add-social-identity-providers.md)

[تحديث Commerce headquarters بواسطة معلومات Azure AD B2C](update-hq-aad-b2c-info.md)

[تكوين مستأجر B2C في منشئ موقع Commerce](config-b2c-tenant-site-builder.md)

[معلومات B2C إضافية](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
