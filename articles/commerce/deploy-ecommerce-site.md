---
title: نشر مستأجر التجارة الإلكترونية الجديد
description: يصف هذا الموضوع كيفية نشر مستأجر التجارة الإلكترونية الجديد باستخدام Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697441"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>نشر مستأجر التجارة الإلكترونية الجديد

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

يصف هذا الموضوع كيفية نشر موقع تجارة إلكترونية جديد باستخدام Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>نظرة عامة
    
تعتبر Microsoft Dynamics Lifecycle Services مساحة عمل تعاونيه قائمة على السحابة ويمكن للشركاء والعملاء استخدامها لإدارة المشاريع والبيئات الخاصة بهم، وعرض أحدث المعلومات حول منتجات Microsoft Dynamics والميزات، وإنشاء حوادث الدعم وتعقبها واستعراضها. تتكامل ميزات إدارة التجارة الإلكترونية في LCS.

لمعرفه المزيد عن LCS، راجع [دليل مستخدم Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>البدء

قبل أن تتمكن من تهيئة التجارة الإلكترونية، يجب تهيئة مشروع، وبيئة، و Retail Cloud Scale Unit (RCSU). للقيام بعملية التهيئة في LCS ، يجب أن يكون لديك أذونات إما لمالك المشروع أو دور مُدير البيئة. يتم دعم مخططات بيئة الإنتاج وبيئة الاختبار المعزولة.

لمزيد من المعلومات حول البيئات، راجع [تخطيط البيئة](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). لمزيد من المعلومات حول RCSU، راجع [تهيئة Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>تهيئة التجارة الإلكترونية

استخدم هذا الاجراء لتهيئة ميزة التجارة الإلكترونية في بيئة موجودة.

قبل البدء، تأكد من أن لديك المعلومات المطلوبة التالية:

- RCSU المستخدمة.
- مجموعه أمان Microsoft Azure Active Directory التي سيتم استخدامها لمسؤولي النظام بالتجارة الإلكترونية.
- مجموعه أمان Microsoft Azure Active Directory التي سيتم استخدامها للتصنيفات ومراجعات الوسطاء.
- المجالات التي سوف يتم إقرانها بالبيئة.

بالإضافة إلى ذلك، يمكنك جمع المعلومات الاختيارية التالية:

- معلومات Azure AD العمل-المستهلك (B2C) :

    - اسم المستأجر.
    - معرّف العميل.
    - تسجيل الدخول إلى المجال المخصص.
    - عنوان URL الخاص بالرد.
    - معرف سياسة تسجيل الاشتراك وتسجيل الدخول.
    - إعادة تعيين مُعرف سياسة كلمة المرور.
    - تحرير معرف سياسة ملف التعريف.

[!NOTE]
يمكن إضافة هذه المعلومات في وقت لاحق، من خلال طلب خدمة.

بعد تجميع المعلومات المطلوبة، اتبع الخطوات التالية لتهيئه التجارة الإلكترونية.

1. سجل الدخول إلى [LCS](https://lcs.dynamics.com).
1. افتح المشروع الذي يحتوي علي البيئة التي ترغب في تهيئة التجارة الإلكترونية فيها.
1. في قسم **البيئات** ، حدد البيئة.
1. تحت **ميزات البيئة**، حدد ارتباط **إدارة Retail** .
1. في علامة التبويب **التجارة الإلكترونية** ، حدد **إعداد**. سوف يظهر مربع حوار، حيث يجب عليك إدخال المعلومات المطلوب توفيرها.
1. قم بملء المعلومات المطلوبة، ثم انتقل إلى الصفحة التالية.
1. ‏‫يمكنك في الصفحة التالية ملء المعلومات المطلوبة، ثم ارسل النموذج. يتم إرجاعك إلى علامة تبويب **التجارة الإلكترونية** ، حيث ستشاهد انه قد تم بدء التهيئة.
1. لعرض حالة التهيئة ، قم **بالتحديث** أو الرجوع إلى علامة تبويب **التجارة الإلكترونية** لاحقا.
    
عند تهيئة التجارة الإلكترونية من LCS، يقوم النظام بتوفير العديد من المكونات المطلوبة للتجارة الإلكترونية وربطها بالبيئة. بعد الانتهاء من التوفير، يتم تحديث علامة التبويب **التجارة الإلكترونية** في صفحة **إدارة Retail** لتعكس التوفير. وتعرض الصفحة أحدث عمليات نشر التخصيص وحالة أي عمليات نشر أخرى جارية. ويتضمن أيضا ارتباطات إلى موقع التجارة الإلكترونية وأداة إدارة موقع التجارة الإلكترونية (أداة التأليف).

## <a name="access-the-authoring-environment"></a>الوصول إلى بيئة التأليف

للوصول إلى بيئة التأليف، انتقل إلى علامة التبويب **التجارة الإلكترونية** في صفحة **إدارة Retail** . هناك، سوف تجد ارتباطات لموقع التجارة الإلكترونية الخاصة بك وأداة إدارة المواقع.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على المتجر على الإنترنت](online-store-overview.md)

[إنشاء موقع تجارة إلكترونية](create-ecommerce-site.md)

[إقران موقع عبر الإنترنت بقناة](associate-site-online-store.md)

[تكوين اسم مجالك](configure-your-domain-name.md)

[إضافة الدعم إلى شبكة تسليم المحتوى (CDN)](add-cdn-support.md)

[تمكين اكتشاف المتجر استنادًا إلى الموقع](enable-store-detection.md)

[إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين](custom-pages-user-logins.md)
