---
title: أوامر العمل والأصول الثابتة
description: يشرح هذا الموضوع أوامر العمل والأصول الثابتة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875477"
---
# <a name="work-orders-and-fixed-assets"></a>أوامر العمل والأصول الثابتة


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


في إدارة الأصول، يمكن ربط الأصول بالأصول الثابتة، ويمكن إنشاء أوامر عمل لهذه الأصول. إذا استخدمت هذه الوظيفة، يمكنك الحصول على نظرة عامة كاملة على الأصول الثابتة ومشاريع الاستثمار ذات الصلة والتكاليف المسجلة على مشاريع الاستثمار في الوحدة النمطية **إدارة المشاريع ومحاسبتها** والوحدة النمطية **الأصول الثابتة** في Dynamics 365 for Finance and Operations.

>[!NOTE]
>يتم ملء حقل **رقم الأصل الثابت** فقط في مشروع وظيفة أمر العمل في حالة تحديد النوع "استثمار" كنوع المشروع في مشروع وظيفة أمر العمل.

![الشكل 1](media/24-work-orders.png)

يصف الإجراء التالي العلاقة بين الأصول وأوامر العمل ومشاريع وظائف أمر العمل والأصول الثابتة.

1. تقوم بإنشاء أصل تربطه بأصل ثابت، كما هو موضح في الشكل أدناه.

![الشكل 2](media/25-work-orders.png)

2. عند إعداد أنواع أوامر العمل (**إدارة الأصول** > **الإعداد** > **أوامر العمل** > **أنواع أوامر العمل**)، تنشئ نوع أمر عمل للتعامل مع الاستثمارات. راجع أيضًا [أنواع أوامر العمل](../setup-for-work-orders/work-order-types.md).

![الشكل 3](media/26-work-orders.png)

3. عندما تقوم بإعداد مجموعات مشاريع أوامر العمل (**إدارة الأصول** > **الإعداد** > **أوامر العمل** >  **إعداد المشروع** > الارتباط **مجموعة المشاريع**)، تنشئ علاقة بين نوع أمر العمل المستخدم للاستثمارات ومجموعة المشاريع التي تم إنشاؤها للاستثمارات في الوحدة النمطية **إدارة المشاريع ومحاسبتها** (**إدارة المشاريع ومحاسبتها** > **الإعداد** > **الترحيل** > **مجموعات المشاريع**).

![الشكل 4](media/27-work-orders.png)

4. عندما تنشئ أمر عمل يتعلق بكائن الأصل الثابت، فأنت تحدد نوع أمر العمل المستخدم للتعامل مع الاستثمارات، على سبيل المثال، "استثمار".

5. عند إنشاء أمر العمل، يتم عرض نوع أمر العمل المرتبط في **جميع أوامر العمل‬‏‫**.

![الشكل 5](media/28-work-orders.png)

6. عند إنشاء أمر العمل، يتم إنشاء المشروع المرتبط بأمر العمل في **إدارة المشاريع ومحاسبتها** > **جميع المشاريع**. يمكنك الاطلاع على المعلومات ذات الصلة بالمشروع من خلال النقر فوق الارتباط **معرف المشروع**  على أمر العمل (في **إدارة الأصول**، افتح أمر العمل في طريقة عرض التفاصيل > علامة التبويب السريعة **تفاصيل البنود** > علامة التبويب السريعة **عام** > الحقل **معرف المشروع**).

![الشكل 6](media/29-work-orders.png)

7. في **الأصول الثابتة**، يمكنك الاطلاع على نظرة عامة على المشاريع المقترنة بأصل ثابت (**الأصول الثابتة** > **الأصول الثابتة** > **الأصول الثابتة** > انقر فوق الأصل الثابت في حقل **رقم الأصل الثابت** > استعرض المحتويات في الجزء **معلومات ذات الصلة** > قسم **المشروعات المقترنة‬**).
