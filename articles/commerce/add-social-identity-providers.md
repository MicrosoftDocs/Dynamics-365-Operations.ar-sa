---
title: إضافة موفري الهوية الاجتماعية
description: توضح هذه المقالة كيفية إضافة موفري الهويات الاجتماعية في Microsoft Azure. portal
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785206"
---
# <a name="add-social-identity-providers"></a>إضافة موفري الهوية الاجتماعية

[!include [banner](includes/banner.md)]

توضح هذه المقالة كيفية إضافة موفري الهويات الاجتماعية في Microsoft Azure. portal

يسمح موفرو الهوية الاجتماعية للمستخدمين باستخدام حساباتهم الاجتماعية للمصادقة. تعتبر إضافة مصادقة موفر الهوية الاجتماعية اختيارية في Dynamics 365 Commerce. 

إذا لم تتم إضافة مصادقة موفر الهوية الاجتماعية، ستكون ملفات تعريف Azure Active Directory (Azure AD) B2C الافتراضية ملفات التعريف الأساسية لقاعدة المستخدمين. سيقوم المستخدمون بتحديد اسم المستخدم (عنوان بريدهم الإلكتروني المفضل) وتعيين كلمة مرور. سيقوم Azure AD B2C بمصادقة المستخدمين بشكل مباشر. 

إذا تمت إضافة مصادقة موفر الهوية الاجتماعية واختار أحد المستخدمين أحد موفري الهوية الاجتماعية المعروضين، فسيتم مع ذلك إنشاء كيان في مستأجر Azure AD B2C. سيقوم Azure AD B2C عندئذٍ بمصادقة بيانات اعتماد المستخدم مع موفر الهوية الاجتماعية.

> [!NOTE]
> يؤدي تسجيل دخول الموفر إلى إنشاء سجل في مستأجر B2C، ولكن بتنسيق مختلف عن الحسابات المحلية لأنه سيقوم باستدعاء مرجع موفر الهوية الاجتماعية الخارجي للمصادقة. يمكن للمستخدم استخدام عنوان البريد الإلكتروني نفسه عبر موفري الهويات الاجتماعية، مما يعني أن اسم المستخدم للبريد الإلكتروني الذي تم استخدامه للمصادقة قد لا يكون فريدًا للمستخدم. سيفرض Azure AD B2C فقط وجود عنوان بريد إلكتروني فريد للمستخدمين على حسابات B2C المحلية.

قبل أن تتمكن من إضافة موفر هوية اجتماعية للمصادقة، يجب الانتقال إلى مدخل موفر الهوية وإعداد تطبيق موفر هوية كما هو موضح في وثائق Azure AD B2C. توجد أدناه قائمة بالارتباطات إلى الوثائق.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (مستأجر واحد)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [حساب Microsoft](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>إضافة موفر هوية اجتماعية وإعداده

> [!NOTE]
> إن إضافة موفري هوية اجتماعية هي خطوة اختيارية عند إعداد مستأجر (B2C) من شركة إلى مستهلك في Microsoft Dynamics 365 Commerce.

لإضافة موفر هوية اجتماعية وإعداده، اتبع الخطوات التالية.  

1. في مدخل Azure، انتقل إلى **موفرو الهوية**.
1. حدد **إضافة**. تظهر الشاشة **إضافة موفر هوية**.
1. ضمن **الاسم**، أدخل الاسم المطلوب عرضه للمستخدمين على شاشة تسجيل الدخول.
1. ضمن **نوع موفر الهوية**، حدد موفر هوية من القائمة.
1. حدد **موافق**.
1. حدد **إعداد موفر الهوية هذا** للوصول إلى شاشة **إعداد موفر الهوية الاجتماعية**.
1. ضمن **معرف العميل**، أدخل معرف العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.
1. ضمن **سر العميل**، أدخل سر العميل كما تم الحصول عليه من إعداد تطبيق موفر الهوية.
1. إرفاق سير عمل المستخدم لسياسات التسجيل وتسجيل الدخول:
1. انتقل إلى **Azure AD B2C – تدفقات المستخدم (السياسات) \> {سياسة التسجيل وتسجيل الدخول} \> موفرو الهوية**.
1. لإرفاق سياسة سير عمل المستخدم للتسجيل/تسجيل الدخول، حدد كل موفر هوية قمت بإعداده لحسابك. لاختبار هذه التدفقات، حدد **تشغيل تدفق المستخدم** لكل موفر هوية. ستعرض علامة تبويب جديدة صفحة تسجيل الدخول التي تعرض مربع تحديد موفر الهوية الجديد.

تظهر الصورة التالية أمثلة عن شاشات **إضافة موفر هوية** و **إعداد موفر الهوية الاجتماعية** في Azure AD B2C.

![إضافة موفر هوية اجتماعية إلى تطبيقك.](./media/B2CImage_14.png)

تعرض الصورة التالية مثالاً عن كيفية تحديد موفري الهوية في صفحة **موفرو هوية** Azure AD B2C.

![حدد كل موفر هوية اجتماعية لتمكينه لسياستك.](./media/B2CImage_16.png)

تعرض الصورة التالية مثالاً عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية.

> [!NOTE]
> إذا كنت تستخدم الصفحات المخصصة المضمنة في Commerce لتدفقات المستخدم الخاصة بك، فستحتاج الأزرار الخاصة بموفري الهوية الاجتماعية إلى إضافتها باستخدام ميزات القابلية للتوسعة في مكتبة وحدة Commerce. بالإضافة إلى ذلك، عند إعداد تطبيقاتك باستخدام موفر هوية اجتماعية محدد، قد يكون عنوان URL أو سلاسل التكوين في بعض الحالات حساسة لحالة الأحرف. راجع إرشادات الاتصال الخاصة بموفر الهوية الاجتماعية لمزيد من المعلومات.
 
![مثال عن شاشة تسجيل دخول افتراضية مع عرض زر تسجيل الدخول إلى موفر هوية اجتماعية.](./media/B2CImage_17.png)

## <a name="next-steps"></a>الخطوات التالية

لمتابعه عملية إعداد مستأجر B2C في Commerce، تابع [تحديث Commerce headquarters بمعلومات Azure AD B2Cالجديدة](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد مستأجر B2C في Commerce](set-up-b2c-tenant.md)

[إنشاء مستأجر B2C Azure AD موجود أو الارتباط به في Azure portal ](create-link-aad-b2c-tenant.md)

[إنشاء تطبيق B2C](create-b2c-app.md)

[إنشاء سياسات تدفق المستخدم](create-user-flow-policies.md)

[تحديث Commerce headquarters بواسطة معلومات Azure AD B2C](update-hq-aad-b2c-info.md)

[تكوين مستأجر B2C في منشئ موقع Commerce](config-b2c-tenant-site-builder.md)

[معلومات B2C إضافية](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
