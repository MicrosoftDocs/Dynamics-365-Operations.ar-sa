---
title: السيناريوهات المدعومة لإعداد الكتابة المزدوجة
description: يصف هذا الموضوع السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706242"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>السيناريوهات المدعومة لإعداد الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة Finance and Operations وبيئة Common Data Service.

+ توفر **بيئة Finance and Operations** النظام الأساسي لـ **تطبيقات Finance and Operations** (على سبيل المثال Microsoft Dynamics 365 Finance و Dynamics 365 Supply Chain Management وDynamics 365 Retail).
+ توفر **بيئة Common Data Service** النظام الأساسي **للتطبيقات المستندة إلى نموذج في Dynamics 365** ‏(Dynamics 365 Sales وDynamics 365 Customer Service وDynamics 365 Field Service Dynamics 365 Marketing وDynamics 365 Project Service Automation).

>[!IMPORTANT]
>يدعم Human Resources في Finance and Operations  اتصالات الكتابة المزدوجة، ولكن لا يدعمها تطبيق Dynamics 365 Human Resources.

تختلف آلية الإعداد باختلاف اشتراكك وبيئتك.

+ بالنسبة إلى المثيلات الجديدة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS). إذا كان لديك ترخيص Microsoft Power Platform، فستحل على بيئة Common Data Service جديدة، إذا لم يكن لدى المستأجر بيئة.
+ بالنسبة إلى المثيلات الموجودة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة Finance and Operations.

سيناريوهات الإعداد التالية مدعومة:

+ [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج](#new-new)
+ [مثيل جديد لتطبيق Finance and Operations ومثيل موجود لتطبيق مستند إلى نموذج](#new-existing)
+ [مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل جديد لتطبيق مستند إلى نموذج](#new-demo-new)
+ [مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل موجود لتطبيق مستند إلى نموذج](#new-demo-existing)
+ [مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق مستند إلى نموذج](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md). عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:

- يتم تزويد بيئة Finance and Operations جديدة فارغة.
- يتم تزويد مثيل جديد وفارغ من تطبيق يستند إلى نموذج، حيث تم تثبيت حل CRM الأساسي.
- يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.
- يتم تمكين خرائط الكيانات للمزامنة المباشرة.

عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>مثيل جديد لتطبيق Finance and Operations ومثيل موجود لتطبيق مستند إلى نموذج

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل موجود لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md). عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:

- يتم تزويد بيئة Finance and Operations جديدة فارغة.
- يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.
- يتم تمكين خرائط الكيانات للمزامنة المباشرة.

عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.

لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.

1. أنشئ شركة جديدة في تطبيق Finance and Operations.
2. أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.
3. [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.

لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>مثيل جديد لتطبيق Finance and Operations يتضمن بيانات عرض توضيحي ومثيل جديد لتطبيق مستند إلى نموذج

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل جديد لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج‬](#new-new) في قسم سابق من هذا الموضوع. عند اكتمال إعداد الاتصال، إذا أردت مزامنة بيانات العرض التوضيحي مع التطبيق المستند إلى نموذج، اتبع الخطوات التالية.

1. افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>مثيل جديد لتطبيق Finance and Operations يتضمن بيانات عرض توضيحي ومثيل موجود لتطبيق مستند إلى نموذج

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل موجود لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج‬](#new-existing) في قسم سابق من هذا الموضوع. عند اكتمال إعداد الاتصال، إذا أردت مزامنة بيانات العرض التوضيحي مع التطبيق المستند إلى نموذج، اتبع الخطوات التالية.

1. افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.

1. أنشئ شركة جديدة في تطبيق Finance and Operations.
2. أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.
3. [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.

لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق مستند إلى نموذج

يحدث إعداد اتصال الكتابة المزدوجة بين مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق يستند إلى نموذج في Dynamics 365 في بيئة Finance and Operation.

1. قم بإعداد الاتصال من تطبيق Finance and Operations.
2. لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬

لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.
