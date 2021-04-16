---
title: ارتباط تسجيل الدخول يقوم بإعادة التوجيه مرة أخرى إلى موقع التجارة الإلكترونية
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة قيام ارتباط تسجيل الدخول بإعادة التوجيه إلى موقع التجارة الإلكترونية بدلا من الانتقال إلى صفحة تسجيل الدخول.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ee2ac8636dad8d31719971b2cc17c8b923f07959
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801449"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>ارتباط تسجيل الدخول يقوم بإعادة التوجيه مرة أخرى إلى موقع التجارة الإلكترونية

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة قيام ارتباط تسجيل الدخول بإعادة التوجيه إلى موقع التجارة الإلكترونية بدلا من الانتقال إلى صفحة تسجيل الدخول.

## <a name="description"></a>الوصف

بعد تكوين مستأجر جديد لـ B2C في Microsoft Azure Active Directory (B2C لـ Azure AD) في منشئ مواقع Commerce، تتم إعادة توجيه المستخدمين الذين يقومون بتحديد ارتباط **تسجيل الدخول** مرة أخرى إلى الصفحة المنتقل إليها الرئيسية للتجارة الإلكترونية دون الانتقال إلى صفحه تسجيل الدخول.

## <a name="resolution"></a>الدقة

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>التأكد من تكوين عنوان URL للرد بشكل صحيح في تطبيق B2C لـ Azure AD

لتأكد من تكوين عنوان URL للرد بشكل صحيح في تطبيق B2C لـ Azure AD، اتبع الخطوات التالية.

1. انتقل إلى [مدخل Azure](https://portal.azure.com/).
1. حدد تطبيق B2C لـ Azure AD الذي قمت بإنشائه للوصول إلى الموقع الخاص بك.
1. حدد التطبيق الذي قمت بإنشائه أثناء إعداد B2C لـ Azure AD.
1. تحت **عنوان URL للرد**، تأكد من أن القائمة تتضمن إدخالات لكل من عنوان URL لمجال الموقع وعنوان URL الذي تم إنشاؤه بواسطة التجارة الإلكترونية، كما هو موضح في المثال الموجود في التوضيح التالي.

    ![إدخالات URL للرد الخاصة بـ B2C لـ Azure AD](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> يجب أن يكون كل من عنوان URL لمجال الموقع وعنوان URL المنشأ بواسطة التجارة الإلكترونية بتنسيق URL صالح لا يحتوي على خطوط مائلة سابقة أو لاحقة.

## <a name="additional-resources"></a>الموارد الإضافية

[تسجيل تطبيق ويب في B2C لـ Azure Active Directory ](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[إعداد مستأجر متاجرة عمل-مستهلك في Commerce](../set-up-b2c-tenant.md)
