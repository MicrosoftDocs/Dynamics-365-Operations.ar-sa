---
title: خيارات تنفيذ شبكة تسليم المحتويات
description: يراجع هذا الموضوع الخيارات المختلفة لتطبيق شبكة تسليم المحتوى (CDN) التي يمكن استخدامها مع بيئات Microsoft Dynamics 365 Commerce. تتضمن هذه الخيارات المثيلات الأصلية المقدمة من Commerce لـ Azure Front Door والمثيلات المملوكة للعملاء الخاصة بـ Azure Front Door
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f6e8fb2baf85be0eaecfffcc7ec6cbb457c3bb04
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021880"
---
# <a name="content-delivery-network-implementation-options"></a>خيارات تنفيذ شبكة تسليم المحتويات

[!include [banner](includes/banner.md)]

يراجع هذا الموضوع الخيارات المختلفة لتطبيق شبكة تسليم المحتوى (CDN) التي يمكن استخدامها مع بيئات Microsoft Dynamics 365 Commerce. تتضمن هذه الخيارات المثيلات الأصلية المقدمة من Commerce لـ Azure Front Door والمثيلات المملوكة للعملاء الخاصة بـ Azure Front Door

يتوفر لدي عملاء Commerce العديد من الخيارات عندما يفكرون في أي خدمة CDN يمكن استخدامها مع بيئة Commerce الخاصة بهم. تم إصدار Commerce مع دعم أساسي من Azure Front Door التي تغطي متطلبات المضيف الأساسية والمخصصة للمجال. بالنسبة للشركات التي ترغب في مزيد من التحكم وإمكانات أمان أكثر تحديدا، مثل جدار حماية تطبيق ويب (WAF)، قد يكون أفضل خيار هو استخدام المثيل الذي يملكه العميل من Azure Front Door أو CDN خارجية.

يمكن استخدام خيارات التنفيذ الثلاثة التالية لـ CDN مع بيئات Commerce:

- مثيل Azure Front Door الذي يوفره Commerce.
- المثيل المملوك للعميل من Azure Front Door (لمزيد من التحكم وميزات الأمان الإضافية)
- خدمة CDN الخارجية

تقدم كافة خيارات تنفيذ CDN الثلاثة فقط محتوي HTML ديناميكي من المجالات المخصصة. تعالج Commerce تلقائيًا كافة JavaScript وصور أوراق الأنماط المتتالية (CSS) والصور والفيديو والمحتوي الثابت الآخر من خدمات CDN التي تديرها Microsoft. يحدد الخيار الذي تختاره إمكانات التشغيل وإمكانات التحكم وإمكانات الأمان الإضافية المتوفرة.

يعرض الشكل التوضيحي التالي نظرة عامة على بنية Commerce.

![نظرة عامة حول بنية Commerce](media/Commerce_CDN-Option_ComparisonModels.png)

لمزيد من المعلومات حول كيفية إعداد مثيل لـ Azure Front Door لموقع Commerce الخاصة بك، راجع [إضافة دعم CDN](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>استخدام مثيل Azure Front Door الذي يوفره Commerce

يسرد الجدول التالي مزايا وعيوب استخدام مثيل Azure Front Door الذي توفره Commerce لإدارة نقاط نهاية المحتوى.

| المزايا | العيوب |
|------|------|
| <ul><li>يتم تضمين المثيل في تكلفة Commerce.</li><li>ونظرا لأن المثيل تتم إدارته بواسطة فريق Commerce، ستتكون الصيانة المطلوبة أقل، كما توجد خطوات إعداد مشتركة.</li><li>تتميز البنية المستضافة على Azure بأنها قابلية لتغيير الحجم وآمنة وموثوق بها.</li><li>تتطلب شهادة طبقة مآخذ التوصيل الآمنه (SSL) الإعداد لمرة واحدة ويتم تجديدها تلقائيًا.</li><li>يراقب فريق Commerce المثيل بحثًا عن الأخطاء والأمور غير العادية.</li></ul> | <ul><li>لا يتم دعم جدار حماية WAF.</li><li>لا توجد تخصيصات أو عمليات ضبط محددة للإعدادات.</li><li>يعتمد المثيل على فريق Commerce في إجراء التحديثات أو التغييرات.</li><li>يلزم وجود مثيل Azure Front Door منفصل لمجالات apex، ويلزم إجراء عمل إضافي لدمج مجالات apex مع Azure DNS.</li><li>لا يتم توفير أي بيانات تتبع استخدام حول الاستجابات في الثانية (RPS) أو معدل الخطأ للعميل.</li></ul> |

يبين الرسم التوضيحي التالي بنية مثيل Azure Front Door الذي يوفره Commerce.

![مثيل Azure Front Door الذي يوفره Commerce](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>استخدام مثيل Azure Front Door المملوك للعميل

يسرد الجدول التالي مزايا وعيوب استخدام مثيل Azure Front Door المملوك للعميل لإدارة نقاط نهاية المحتوى.

| المزايا | العيوب |
|------|------|
| <ul><li>الإعداد أمن ويسهل إدارته.</li><li>تتميز البنية المستضافة على Azure بأنها قابلية لتغيير الحجم وآمنة وموثوق بها.</li><li>يسمح المثيل بتكامل جدار حماية WAF وعناصر تحكم قاعدة الدرجات المتعددة للأمان الأفضل الذي يتم ضبطه خصيصًا للموقع الخاص بك.</li><li>يسمح المثيل بالتحكم الدقيق بشهادات SSL (المملوكة للعميل والمدارة بواسطة Azure Front Door) وربط المجال.</li><li>يقدم المثيل حل مجال apex إذا كان مقترنًا مباشرة بخدمة Azure DNS.</li><li>يتم توفير بيانات تتبع الاستخدام والتنبيه.</li><li>تتطلب شهادة SSL الإعداد لمرة واحدة ويتم تجديدها تلقائيًا.</li></ul> | <ul><li>تتم إدارة المثيل ذاتيًا.</li><li>مطلوب زيادة المعرفة الأولية.</li></ul> |

يبين الرسم التوضيحي التالي البنية الأساسية لـ Commerce التي تشمل مثيل Azure Front Door المملوك للعميل.

![البنية الأساسية لـ Commerce التي تشمل مثيل Azure Front Door المملوك للعميل.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>استخدام خدمة CDN الخارجية

يسرد الجدول التالي المزايا والعيوب الخاصة باستخدام خدمة CDN الخارجية لإدارة نقاط نهاية المحتوى.

| المزايا | العيوب |
|------|------|
| <ul><li>يكون هذا الخيار مفيدًا في حالة استضافه المجال الموجود بالفعل على خدمة CDN خارجية.</li><li>قد يكون لخدمات CDN المنافسة (على سبيل المثال، Akamai) إمكانات WAF أفضل.</li></ul> | <ul><li>يلزم وجود عقد منفصل وتكلفة إضافية.</li><li>قد تتكبد خدمة SSL تكاليف إضافية.</li><li>نظرًا لأن الخدمة منفصلة عن بنيه سحابة Azure، يجب إدارة البنية الأساسية الإضافية.</li><li>قد تتطلب الخدمة استثمارات طويلة الوقت في نقطة النهاية وإعداد الأمان.</li><li>الخدمة مدارة ذاتيًا.</li><li>الخدمة مراقبة ذاتيًا.</li></ul> |

يبين الرسم التوضيحي التالي البنية الأساسية لـ Commerce التي تشتمل على خدمة CDN خارجية.

![البنية الأساسية لـ Commerce التي تشتمل على خدمه CDN خارجية](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة الدعم إلى شبكة تسليم المحتوى (CDN)](add-cdn-support.md)
