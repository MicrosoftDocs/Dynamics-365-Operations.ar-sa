---
title: ارتباط تسجيل الدخول يقوم بإعادة التوجيه مرة أخرى إلى موقع التجارة الإلكترونية
description: يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة قيام ارتباط تسجيل الدخول بإعادة التوجيه إلى موقع التجارة الإلكترونية بدلا من الانتقال إلى صفحة تسجيل الدخول.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 0bc9c0afbd6b349d8565f9eea56e207eae179f65
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291445"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>ارتباط تسجيل الدخول يقوم بإعادة التوجيه مرة أخرى إلى موقع التجارة الإلكترونية

[!include [banner](../../includes/banner.md)]

يوفر هذا المقال إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة قيام ارتباط تسجيل الدخول بإعادة التوجيه إلى موقع التجارة الإلكترونية بدلا من الانتقال إلى صفحة تسجيل الدخول.

## <a name="description"></a>الوصف

بعد تكوين مستأجر جديد لـ B2C في Microsoft Azure Active Directory (B2C لـ Azure AD) في منشئ مواقع Commerce، تتم إعادة توجيه المستخدمين الذين يقومون بتحديد ارتباط **تسجيل الدخول** مرة أخرى إلى الصفحة المنتقل إليها الرئيسية للتجارة الإلكترونية دون الانتقال إلى صفحه تسجيل الدخول.

## <a name="resolution"></a>الدقة

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>التأكد من تكوين عنوان URL للرد بشكل صحيح في تطبيق B2C لـ Azure AD

لتأكد من تكوين عنوان URL للرد بشكل صحيح في تطبيق B2C لـ Azure AD، اتبع الخطوات التالية.

1. انتقل إلى [مدخل Azure](https://portal.azure.com/).
1. حدد تطبيق B2C لـ Azure AD الذي قمت بإنشائه للوصول إلى الموقع الخاص بك.
1. حدد التطبيق الذي قمت بإنشائه أثناء إعداد B2C لـ Azure AD.
1. تحت **عنوان URL للرد**، تأكد من أن القائمة تتضمن إدخالات لكل من عنوان URL لمجال الموقع وعنوان URL الذي تم إنشاؤه بواسطة التجارة الإلكترونية، كما هو موضح في المثال الموجود في التوضيح التالي.

    ![إدخالات URL للرد الخاصة بـ B2C لـ Azure AD.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> يجب أن يكون كل من عنوان URL لمجال الموقع وعنوان URL المنشأ بواسطة التجارة الإلكترونية بتنسيق URL صالح لا يحتوي على خطوط مائلة سابقة أو لاحقة.

## <a name="additional-resources"></a>الموارد الإضافية

[تسجيل تطبيق ويب في B2C لـ Azure Active Directory ](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[إعداد مستأجر متاجرة عمل-مستهلك في Commerce](../set-up-b2c-tenant.md)
