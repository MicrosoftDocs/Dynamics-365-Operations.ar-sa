---
title: مدخل العميل للنظرة العامة على Dynamics 365 Supply Chain Management (تحتوي على الفيديو)
description: يقدم هذا المقال مدخل العميل، ويقدم شرحًا يتعلق بالجهات التي يمكنها استخدامه وكيفية عمله.
author: Henrikan
ms.date: 06/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7f34acd78966cc9f26242653e9d0d16fdf22e0b2
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103819"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>نظرة عامة على مدخل العميل في Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]


## <a name="what-is-the-customer-portal"></a>ما هو مدخل العميل؟

تعتمد أنظمة سلسلة التوريد الحديثة على التكامل. وهي تتطلب أن يكون المخزون وطلبات العملاء وأقسام المبيعات كلها متكاملة بدلاً من أن تقيم في مستودعات منفصلة. يساعد مدخل العميل الشركات التي تستخدم Microsoft Dynamics 365 Supply Chain Management على تحسين هذا التكامل وإطلاع العملاء على جميع المعلومات بشكل فعال ومستمر.

إن مدخل العميل هو قالب [مداخل Power Apps](/powerapps/maker/portals/overview) يسمح للشركات بإنشاء موقع ويب لمعاملات الشركات (B2B) للسيناريوهات ذات الصلة بمعالجة أوامر المبيعات. يستخدم القالب [الكتابة المزدوجة](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md) وSupply Chain Management ومداخل Power Apps لتمكين عملاء المؤسسة الخارجية من عرض وإنشاء البيانات من بيئة Dynamics 365 الخاصة بالشركة.

يحتوي قالب مدخل العميل على كافة إمكانيات التخصيص التي توفرها ميزة مداخل Power Apps. ويمكن تعديل القالب بسهولة لتمثيل العلامة التجارية الخاصة بالشركة وإضافة المزيد من الوظائف وتغيير تجربة المستخدم. يمكن تعديل كافة الوظائف التي يقدمها القالب حسب الحاجة.

> [!IMPORTANT]
> من غير المتوقع أن يكون القالب قادرًا على العمل بحد ذاته. فهو يعمل فقط كأداة تمكين للعملاء الراغبين في إنشاء موقع خارجي على الويب لتمكين عملاء المؤسسة المشاركة مع البيانات من Supply Chain Management.

> [!NOTE]
> تتوجه وثائق مدخل العميل للمسؤولين والمخصصين والعاملين في مؤسسات تكامل الأنظمة الذين سيعملون على إعداد مدخل العميل لتثبيت Supply Chain Management. وهي تستخدم مصطلحات _العميل_ و _المستخدم_ لوصف الأشخاص الذين هم من عملاء المؤسسة التي تقوم بتشغيل Supply Chain Management والذين سيستخدمون المدخل النهائي بحد ذاته.

## <a name="video"></a>الفيديو

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

تم تضمين الفيديو [نظرة عامة حول قالب مدخل العميل في Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (يظهر أعلاه) في [قائمة تشغيل التمويل والعمليات](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) المتوفرة على YouTube.

## <a name="who-should-use-it"></a>من هي الجهات التي يمكنها استخدامه؟

تم تصميم مدخل العميل للشركات التي تقوم بتشغيل Supply Chain Management وتتميز بالمواصفات التالية:

- تريد بناء موقع خارجي للإعلام عن معلومات معالجة الأوامر (مثل حالة الأمر أو معلومات الحساب) مباشرةً من نظام Supply Chain Management إلى عملاء مؤسستهم.
- إنها بصدد الانتقال من Dynamics AX 2012 إلى Supply Chain Management وسبق لها استخدام في [مدخل الخدمة الذاتية للعميل في AX 2012](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

الأنواع التالية من المؤسسات **ليست** من المرشحين الجيدين لتنفيذ مدخل العميل:

- الشركات التي ترغب في إنشاء موقع ويب للعملاء غير التابعين لمؤسسات. يجب على هذه الشركات التفكير في إنشاء [موقع ويب للتجارة الإلكترونية في Dynamics 365 Commerce](../../commerce/create-ecommerce-site.md).
- الشركات التي تستخدم موقع ويب لمداخل Power Apps لغرض مشابه. لن تحصل هذه الشركات على أي مزايا إضافية من مدخل العميل. يتم تسليم مدخل العميل كقالب يعمل كدليل ونقطة بداية للعملاء الذين يرغبون في "وصل النقاط" بين الكتابة المزدوجة وSupply Chain Management ومداخل Power Apps. إذا سبق لك إعداد موقع ويب يخدم هذا الغرض، فقد لا تستفيد كثيرًا من استخدام قالب مدخل العميل لإعادة تزويد موقع الويب هذا.

## <a name="how-does-it-work"></a>كيف يعمل؟

تم توفير مدخل العميل كقالب مداخل Power Apps. وهو يتوقف على الكتابة المزدوجة ومداخل Power Apps.

[إن مداخل Power Apps](/powerapps/maker/portals/overview) عبارة عن ميزه تتيح للمستخدمين إنشاء موقع خارجي يستطيع الأشخاص من خارج المؤسسة تسجيل الدخول اليه. لإنشاء المداخل، تحتاج إلى تعليمات برمجية قليلة أو لا تحتاجها إطلاقًا. يعد مدخل العميل واحدًا من ضمن [قوالب مداخل Dynamics 365](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) المتعددة المتوفرة من Microsoft.

[الكتابة المزدوجة](/powerapps/maker/portals/overview) هي بنية أساسية جاهزة توفر تفاعلاً قريبًا من الوقت الفعلي بين تطبيقات مشاركة العميل وتطبيقات التمويل والعمليات. وتوفر الكتابة المزدوجة دمجًا ثنائي الاتجاه بين تطبيقات التمويل والعمليات وMicrosoft Dataverse. وهي بالتالي توفر تجربة متكاملة للمستخدم عبر التطبيقات. يعتمد مدخل العميل على الجداول التي تتم مزامنتها مع الكتابة المزدوجة. قبل التمكن من إظهار البيانات من Supply Chain Management في مدخل العميل، يجب تمكين الكتابة المزدوجة لكافة الجداول المناسبة.

![تبعيات مدخل العميل.](media/customer-portal-elements.png "تبعيات مدخل العميل")

يعمل مدخل العميل كنقطة بداية للمؤسسات التي ترغب في استخدام مداخل Power Apps لإنشاء موقع ويب خارجي يستخدم البيانات من تثبيت Supply Chain Management. وهو يساعد المؤسسات على توصيل الكتابة المزدوجة وSupply Chain Management ومداخل Power Apps.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
