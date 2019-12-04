---
title: إعداد تكامل LinkedIn مع Attract
description: يشرح هذا الموضوع كيفيه تكوين تكامل LinkedIn لـ Microsoft Dynamics 365 Talent - Attract كي تتمكن من نشر الوظائف بسهولة في LinkedIn من Attract، مما يسمح لمسؤولي التعيين بمزامنة معلومات التعيين لديهم مع ملف تعريف المرشح في LinkedIn.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833174"
---
# <a name="set-up-linkedin-integration-with-attract"></a>إعداد تكامل LinkedIn مع Attract

[!include [banner](includes/banner.md)]

ساعد مسؤولي التعيين ومدراء التوظيف على جذب أهم المواهب من خلال تكوين تكامل LinkedIn مع Microsoft Dynamics 365 Talent: Attract:. يسمح لك Attract بنشر الوظائف مباشره في LinkedIn، أكبر شركة احترافية في العالم.‬

تعتبر الوظائف التي تنشرها في LinkedIn عبر Attract عروض وظائف محدودة وهي متوفر لشركتك من دون أي تكلفة إضافية. تتوفر إدخالات عروض الوظائف هذه فقط من خلال شركاء برنامج LinkedIn مثل Attract. وهي لا تظهر في لوحة **المهن** في صفحة LinkedIn الخاصة بشركتك، لأن الإدخالات المدفوعة وحدها تظهر هناك. ومع ذلك، فهي تظهر عندما يستعرض المرشحون المحتملون كافة الوظائف المتوفرة. تظهر أيضًا عروض الوظائف المحدودة في عمليات البحث عن الوظائف في LinkedIn.

يوفر Attract طريقتين للتكامل مع LinkedIn لمساعدتك في البحث عن المرشحين من موقع الوظائف الرائج هذا:

- نشر الوظائف من Attract في LinkedIn
- نقل المرشحين من LinkedIn إلى Attract

يمكنك تكوين الخيارات في علامة التبويب **تكامل LinkedIn** في مركز الإدارة. لفتح مركز الإدارة، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> لاستخدام تكامل LinkedIn Recruiter مع Attract، تحتاج إلى [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) بالإضافة إلى [تراخيص LinkedIn Recruiter](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). لمزيد من المعلومات، راجع [أي إصدار من Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

إذا واجهت مشكلة ما في نشر الوظائف في LinkedIn، راجع [استكشاف أخطاء التكامل وإصلاحها مع LinkedIn‏‎ وMicrosoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).

للحصول على معلومات حول طرق أخرى لنشر الوظائف في LinkedIn، راجع [الأسئلة المتداولة حول تكامل Attract مع LinkedIn](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>تكوين نشر الوظائف في LinkedIn

قبل ان تتمكن من نشر الوظائف من Attract في LinkedIn، تحتاج إلى [معرّف شركة في LinkedIn](https://aka.ms/findID). يتكوّن معرّف الشركة في LinkedIn من سلسلة من الأرقام التي تعرف شركتك في LinkedIn بشكل فريد. لمزيد من المعلومات، راجع [ربط معرّف شركتك في LinkedIn بلوحة وظائف LinkedIn - الأسئلة المتداولة](https://aka.ms/findID).

يرسل Attract موجزًا لعمليات نشر الوظائف في LinkedIn، وتتحقق LinkedIn من الموجز مرة واحدة في اليوم تقريبًا. قد يستغرق نشر الوظائف في الموقع حوالي 48 ساعة.

تظهر إعلانات الوظائف المنشورة على LinkedIn في موقع LinkedIn المباشر. لا توجد لدى LinkedIn بيئة اختبار لنشر إعلانات الوظائف. لذلك، تأكد من عدم نشر أي وظائف اختبارية عن طريق الخطأ. 

1. في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**. بدلاً من ذلك، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.
2. حدد علامة التبويب **تكامل LinkedIn**.
3. ضمن **اسم الشركة**، أدخل اسم شركتك، وضمن **معرّف الشركة**، أدخل معرّف شركتك في LinkedIn. تأكد من تطابق اسم الشركة مع الاسم الذي يظهر في صفحة شركتك على LinkedIn. لمزيد من المعلومات حول معرّفات الشركات في LinkedIn، راجع [ربط معرّف شركتك في LinkedIn بلوحة وظائف LinkedIn - الأسئلة المتداولة](https://www.linkedin.com/help/linkedin/answer/98972).

    إذا احتجت إلى تغيير أي معلومات خاصة بمؤسستك، فراجع [تغيير عنوان مؤسستك وجهة الاتصال التقنية فيها والمزيد](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). وإذا بقيت تواجه بعض المشاكل، فاتصل بقسم [دعم LinkedIn](https://www.linkedin.com/help/linkedin).

4. حدد **حفظ**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>إعداد LinkedIn Recruiter مع Attract 

للسماح لمسؤولي التعيين بالبحث عن الوظائف من خلال LinkedIn Recruiter، يجب تكوين التكامل مع LinkedIn Recruiter في Attract. لإكمال عملية التكوين، ستحتاج إلى العمل مع المستخدم الذي يؤدي دور المسؤول في عقد LinkedIn Recruiter الخاص بمؤسستك.

1. في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**. بدلاً من ذلك، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.
2. حدد علامة التبويب **تكامل LinkedIn**.

    [![طريقة عرض مسؤول Attract لبدء تكامل LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. حدد **اتصال** لبدء الإعداد. سيتم إرشادك من خلال عملية تسجيل الدخول إلى LinkedIn.
4. إذا كان لديك مقاعد في عقود LinkedIn متعددة، فحدد العقد الذي تريد توصيله بنظام Attract. إذا كان لديك مقعد في عقد LinkedIn واحد فقط، فيمكنك تخطي هذه الخطوة.
5. ضمن **Recruiter System Connect (RSC)**، حدد **طلب‏‎**.

    [![طريقة عرض مسؤول Attract لطلب تكامل LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. من المفترض أن يظهر إعداد **Recruiter System Connect (RSC)** الآن على الشكل **الشريك جاهز‬‏‫**. إذا رأيت **إعلام الشريك** على هذه الصفحة، فانتظر بضع ثوان، وحدد **إعلام الشريك**، ثم قم بتحديث الصفحة. يجب أن يظهر الإعداد الآن على الشكل **الشريك جاهز**.

    [![طريقة عرض المسؤول في Attract للإشارة إلى استكمال الطلبات من جانب Attract](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. لإكمال الخطوات التالية، تحتاج إلى امتيازات المسؤول على عقد LinkedIn Recruiter.

    1. سجل دخولك إلى LinkedIn باستخدام حساب المسؤول، ثم حدد **LinkedIn Recruiter**في الجزء العلوي الأيسر. 
    2. في قائمة **المزيد** في أعلى الشاشة، حدد **إعدادات المسؤول**، ثم حدد علامة التبويب **ATS**.
    3. لتمكين التصدير بنقرة واحدة لعقد واحد فقط، قم بتشغيل الخيار **الوصول على مستوي العقد (لكل مقعد على هذا العقد)**. لتمكينه للشركة بكاملها، قم بتشغيل الخيار **الوصول على مستوى الشركة‬‏‫ (لكل عقد في شركتك)**.

    [![تشغيل تكامل Attract من طريقة عرض مسؤول LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

8. في مركز إدارة Attract، حدد علامة التبويب **تكامل LinkedIn**. من المفترض أن يظهر الآن الإعداد **Recruiter System Connect (RSC)** على الشكل **ممكّن**.

    [![اكتمال تكامل LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>إعداد "التقدم بطلب عبر LinkedIn" في Attract

يمكنك السماح للمرشحين بتقديم طلبات للحصول على وظائفك باستخدام ملفات تعريفهم في LinkedIn. لمزيد من المعلومات حول إعداد "التقدم بطلب عبر LinkedIn، راجع [قوة LinkedIn في كل مكان: التقدم بطلب عبر LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

هذه الميزة قيد المعاينة حاليًا. قبل اتباع هذه الخطوات، تأكد من تمكين "التقدم بطلب عبر LinkedIn". لمزيد من المعلومات حول كيفية تمكين ميزات المعاينة، راجع [الوصول إلى ميزات المعاينة في Microsoft Dynamics 365 Talent](./access-preview-feature.md).

1. في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**. بدلاً من ذلك، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.
2. حدد علامة التبويب **تكامل LinkedIn**.

    [![طريقة عرض مسؤول Attract لبدء تكامل LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. إلى جانب **التقدم بطلب عبر LinkedIn**، حدد **اتصال** لبدء الإعداد. سيتم إرشادك عبر الجزء المتبقي من العملية مع LinkedIn.

## <a name="see-also"></a>راجع أيضًا

[الأسئلة المتداولة حول تكامل Attract مع LinkedIn](./attract-linkedin-faq.md)

[نشر الوظائف في مواقع مهن خارجية من Attract](./posting-jobs-external.md)

[بحث عن المرشحين باستخدام LinkedIn Recruiter في Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[إنشاء الوظائف والموافقة عليها ونشرها في Attract](./creating-jobs-attract.md)

[استكشاف أخطاء التكامل وإصلاحها مع LinkedIn وMicrosoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)
