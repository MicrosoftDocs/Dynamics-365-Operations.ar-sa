---
title: نشر الوظائف في مواقع وظائف خارجية من Attract
description: يشرح هذا الموضوع كيفية استخدام Dynamics 365 for Talent - Attract لنشر الوظائف في مواقع توظيف خارجية.
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517247"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>نشر الوظائف في مواقع وظائف خارجية من Attract

[!include [banner](../includes/banner.md)]

تريد عرض المناصب المفتوحة أمام عدد أكبر عدد ممكن من المرشحين المؤهلين. تساعدك مواقع التوظيف مثل Broadbean في تحقيق هذا الهدف. يسمح لك الآن Microsoft Dynamics 365 Talent: Attract بنشر الوظائف في Broadbean، وتعمل Microsoft بشكل مستمر على تقديم عروض جديدة في هذا المجال.

## <a name="post-jobs-to-broadbean"></a>نشر وظائف في Broadbean

قبل أن تتمكن من نشر الوظائف في Broadbean، يجب عليك تكوين تكامل Broadbean.

> [!NOTE]
> - لنشر الوظائف في مواقع خارجية، يجب استخدام [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - هذه الميزة قيد المعاينة حاليًا. إذا أردت تجربتها، فيجب [تشغيلها في إعدادات إدارة Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>تكوين تكامل Broadbean

1. سجل دخولك إلى Attract كمسؤول.
2. حدد زر **الإعدادات** (رمز الترس) في الزاوية العلوية اليسرى من الصفحة، ثم حدد **مركز الإدارة**.
3. على علامة التبويب **إعدادات لوحة الوظائف**، في القسم **تمكين تكامل Broadbean**، قم بتشغيل التكامل.
4. اتصل بموقع Broadbean، وأدخل معلوماتك في **Username, Client ID, Encryption Token**.

> [!WARNING]
> تعتبر بيانات اعتمادك في Broadbean سرية وحساسة لحالة الأحرف. وبالتالي، يجب تخزينها ومشاركتها بطريقة مسؤولة. بإمكان أي شخص يؤدي دور المسؤول في Attract عرض بيانات الاعتماد هذه.

> [!NOTE]
> لا تشارك Microsoft كما لا يشارك Attract في إنشاء هذه القيم والمحافظة عليها. تقع على عاتقك مسؤولية تحديثها بشكل مستمر في Attract والعمل مع Broadbean على حل أي مشكلة تتعلق ببيانات اعتمادك.

### <a name="post-a-job-to-broadbean"></a>نشر وظيفة في Broadbean

بعد تشغيل Broadbean، بإمكان المسؤولين ومسؤولي التعيين نشر وظائف فيه. يجب أن يتوفر لديك عنوان URL لتقديم الطلب للوظيفة.

1. في Attract، افتح الوظيفة التي تريد نشرها في Broadbean.
2. في قسم **عمليات النشر**، حدد الزر **نشر الآن** الذي يتوافق مع Broadbean.
3. اتبع الإرشادات في نافذة Broadbean.

يقوم Attract بتمرير المعلومات التالية إلى Broadbean:

- معرف الطلب
- المسمى الوظيفي
- وصف الوظيفة
- موقع الوظيفة
- عنوان URL لتقديم الطلب
- معلومات مسؤول التعيين

بعد أن يكمل Broadbean عملية نشر الوظيفة بنجاح، يعرض القسم **عمليات النشر** للوظيفة في Attract حالة Broadbean **منشور**.

> [!NOTE]
> - يحتاج Broadbean إلى حقل **المجال**. تم تعيين هذا الحقل إلى **تكنولوجيا المعلومات**، بشكل افتراضي. ومع ذلك، يمكنك تغيير القيمة إلى المجال الصحيح في نافذة نشر الوظائف في Broadbean.
> - يحتاج Broadbean إلى بعض الوقت لإتمام نشر وظيفتك في جميع لوحات الوظائف التي حددتها. ولذلك، قد يحدث بعض التأخير قبل أن يتمكن Attract من توفير تحديث الحالة للوظيفة.

### <a name="view-a-broadbean-job-posting"></a>عرض منشور وظيفة في Broadbean

بعد نشر وظيفة في Broadbean، يمكنك عرضها من Attract.

1. في Attract، افتح الوظيفة التي تريد عرضها في Broadbean.
2. في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **عرض**.

يظهر منشور الوظيفة في Broadbean في نافذة جديدة.

### <a name="update-a-broadbean-job-posting"></a>تحديث منشور وظيفة في Broadbean

يمكنك تحديث منشور وظيفة في Broadbean باستخدام طريقتين.

1. في Attract، افتح الوظيفة التي تريد تحديثها.
2. في قسم **عمليات النشر**، حدد الزر **تحديث المنشور** الذي يتوافق مع Broadbean.
3. حرر المنشور في نافذة Broadbean.

–أو –

1. في Attract، افتح الوظيفة التي تريد عرضها في Broadbean.
2. في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **عرض**.
3. في نافذة Broadbean، حرر تفاصيل الوظيفة، ثم انشر الوظيفة من جديد. لا يطرأ أي تغيير على تفاصيل الوظيفة في Attract.

### <a name="remove-a-broadbean-job-posting"></a>إزالة منشور وظيفة في Broadbean

يمكنك إزالة منشور وظيفة من Broadbean كما تقتضي الحاجة.

1. في Attract، افتح الوظيفة التي تريد إزالتها.
2. في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **إزالة المنشور**.

بعد قيام Broadbean بإزالة الوظيفة، يتضمن عنصر Broadbean في Attract الزر **نشر الآن**. يشير وجود هذا الزر إلى أن إزالة الوظيفة وإلى إمكانية نشرها من جديد.

### <a name="troubleshoot-the-broadbean-integration"></a>استكشاف أخطاء تكامل Broadbean وإصلاحها

إذا كنت تواجه مشكلة ما في نشر وظيفة في Broadbean، فجرّب الخطوات التالية.

1. تأكد من أن بيانات اعتماد Broadbean التي أدخلتها في Attract صالحة وصحيحة.
2. إذا كانت بيانات الاعتماد صالحة وصحيحة، فاتصل بقسم [دعم Broadbean](https://www.broadbean.com/resources/support/).
3. إذا استمرت المشكلة، فاتصل بقسم [دعم Microsoft](./talent-support.md).
