---
title: Regulatory Configuration Service
description: يقدم هذا الموضوع نظرة عامة حول إمكانيات Regulatory Configuration Service (RCS) ويشرح كيفية الوصول إلى الخدمة.
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 4ee68b691bba7f3314b5278b0bcc26504c1583335914a1e7c645abd5303f02c6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012003"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

إن Regulatory Configuration Service (RCS) عبارة عن مصمم مستقل وخدمة إدارة دورة حياة لوظيفة عولمة بدون كود/كود منخفض. تسمح RCS للمساهمين في العولمة بتمديد وتخصيص مناطق العولمة الرئيسية للضرائب والفوترة الإلكترونية والتقارير التنظيمية والبنود ومستندات العمل من دون الحاجة إلى مشاركة المطورين. يجعل أسلوب العولمة هذا بدون كود/كود منخفض العولمة أكثر سهولة وسرعة وأكثر فعالية من حيث التكلفة للإنشاء أو التمديد.

توفر ميزة RCS القدرات التالية:

- دعم لكافة الوظائف التي يتم توفيرها بواسطة إعداد التقارير الإلكترونية (ER).
- أحد المتطلبات الأساسية لتكوين الخدمات الصغيرة الجديدة للعولمة.
- دعم الفوترة الإلكترونية. لمزيد من المعلومات، راجع [الفوترة الإلكترونية‎](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- دعم حساب الضريبة. لمزيد من المعلومات، راجع [خدمة الضريبة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- دعم وظيفة ميزات العولمة الجديدة التي تبسط إدارة دورة الحياة لميزات متعددة المكونات وتوفر قدرة إضافية لتكوين الإجراءات وإعداد معلمات الميزات. لمزيد من المعلومات، راجع  [Regulatory Configuration Service – إدارة ميزات العولمة المبسطة لخدمات العولمة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- دعم عمليات النشر والتخزين والمشاركة المركزية للتكوينات المخصصة في المستودع العمومي لتبسيط إدارة التكوين المبسطة من دون الحاجة إلى استخدام Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>الوصول إلى RCS

يمكنك التسجيل في RCS أو تسجيل الدخول إليها في [صفحة Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![التسجيل في/تسجيل الدخول إلى RCS.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

في صفحة **Regulatory Configuration Service**، راجع ووافق على الشروط والأحكام الإضافية لاستخدام الخدمة، ثم حدد أحد الأزرار التالية:

- **التسجيل** إذا كنت تستخدم الخدمة للمرة الأولى، وكنت تستخدم عنوان بريد إلكتروني للعمل لتزويد مؤسستك ببيئة خدمة
- **تسجيل الدخول** إذا سبق لك التسجيل في الخدمة، وأردت الوصول إلى بيئة مؤسستك

> [!NOTE] 
> بعد الاشتراك، نوصي بإضافة مستخدم SysAdmin إضافية إلى بيئة RCS. سيتم توفير هذا المستخدم كمسؤول مشارك للبيئة. وهذا يساعد على توفير الاستقرار للوصول إلى بيئة RCS، كما دور SysAdmin لإدارة المستخدمين لتلك البيئة. يمكنك إضافة مستخدمين باستخدام **مساحة عمل RCS > إدارة النظام**.

## <a name="regional-availability"></a>التوافر الإقليمي

تتوفر خدمة RCS بشكل عام في المناطق التالية:

- الولايات المتحدة
- الهند
- فرنسا
- أوروبا

للحصول على قائمه كامله بالمناطق، راجع [Dynamics 365 وPower Platform: التوافر وموقع البيانات واللغة والترجمة](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="rcs-default-company"></a>الشركة الافتراضية RCS

تتم مشاركة وظيفة وقت التصميم المستخدمة في RCS عبر كافة الشركات. لا توجد وظيفة خاصة بالشركة. وبالتالي، نُوصي باستخدام شركة واحدة، **DAT**، مع بيئة RCS الخاصة بك.

ومع ذلك، في بعض السيناريوهات، قد تحتاج إلى جعل تنسيقات التقارير الإلكترونية تستخدم المعلمات المرتبطة بكيان قانوني محدد. في هذه السيناريوهات هذه فقط، يجب استخدام مبدل الشركة الافتراضي. على سبيل المثال، راجع [تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة لكل كيان قانوني](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>وثائق RCS ذات الصلة

لمزيد من المعلومات حول المكونات ذات الصلة، راجع الموضوعات التالية:

- **RCS:**

    - [إنشاء تكوينات ER في RCS وتحميلها إلى المستودع العمومي](rcs-global-repo-upload.md)

- **المستودع العمومي:**

    - [إنشاء تكوين التقارير الإلكترونية وتحميله إلى المستودع العمومي](rcs-global-repo-upload.md)
    - [مشاركة التكوين في المستودع العمومي](rcs-global-repo-share-configuration.md)
    - [التصفية المحسنة في المستودع العمومي](enhanced-filtering-global-repo.md)
    - [تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [إيقاف التكوينات في المستودع العمومي](discontinuing-configurations-rcs-global-repo.md)
    - [إهلاك تخزين Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)](rcs-lcs-repo-dep-faq.md)

- **ميزة العولمة:**

    - [Regulatory Configuration Service (RCS) - ميزة العولمة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>استكشاف أخطاء التسجيل في RCS وإصلاحها

عندما تقوم بالتسجيل في RCS من صفحة الخدمة، قد تواجه مشكلة مرتبطة بـ Azure Active Directory (Azure AD). تشير رسالة الخطأ التي تظهر إلى أنه تم إيقاف تشغيل التسجيل في RCS حاليًا ويجب تشغيل التسجيل قبل أن تتمكن من إكمال عملية التسجيل.

![رسالة خطأ التسجيل في RCS.](media/01_RCSSignUpError.jpg)

تحدث هذه المشكلة بسبب أنك محظور من التسجيل للاشتراكات المخصصة، ويجب تمكين الخاصية `AllowAdHocSubscriptions` في المستأجر الخاص بك. 

- إذا قام قسم تكنولوجيا المعلومات الخاص بك بإدارة مستأجري Azure لمؤسسك، فاتصل بذلك القسم للإبلاغ عن المشكلة.
- إذا كنت مسؤولاً عن إدارة مستأجري Azure، فيمكنك إصلاح المشكلات باتباع الخطوات الموجودة في [ما التسجيل بالخدمة الذاتية لـ Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
