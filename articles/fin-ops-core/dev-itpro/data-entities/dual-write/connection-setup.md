---
title: إرشادات حول كيفية إعداد الكتابة المزدوجة
description: يصف هذا الموضوع السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088496"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>إرشادات حول كيفية إعداد الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة Finance and Operations وبيئة Common Data Service.

+ توفر **بيئة Finance and Operations** النظام الأساسي لـ **تطبيقات Finance and Operations** (على سبيل المثال Microsoft Dynamics 365 Finance و Dynamics 365 Supply Chain Management وDynamics 365 Retail).
+ توفر **بيئة Common Data Service** النظام الأساسي لـ **تطبيقات customer engagement** (Dynamics 365 Sales و Dynamics 365 Customer Service و Dynamics 365 Field Service و Dynamics 365 Marketing و Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>يدعم Human Resources في Finance and Operations  اتصالات الكتابة المزدوجة، ولكن لا يدعمها تطبيق Dynamics 365 Human Resources.

تختلف آلية الإعداد باختلاف اشتراكك وبيئتك.

+ بالنسبة إلى المثيلات الجديدة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS). إذا كان لديك ترخيص Power Platform، فستحل على بيئة Common Data Service جديدة، إذا لم يكن لدى المستأجر بيئة.
+ بالنسبة إلى المثيلات الموجودة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة Finance and Operations.

قبل بدء الكتابة الثنائية لكيان ما، يمكنك تشغيل مزامنة أولية لمعالجة البيانات الموجودة على جانبي تطبيقات Finance and Operations وتطبيقات customer engagement. يمكنك تخطي المزامنة الأولية إذا لم تكن بحاجة إلى مزامنة البيانات بين البيئتين.

تتيح المزامنة الأولية إمكانية نسخ البيانات الموجودة من تطبيق واحد إلى آخر بشكل ثنائي الاتجاه. هناك عدة سيناريوهات إعداد مختلفة استنادًا إلى البيئات التي لديك بالفعل ونوع البيانات الموجودة في البيئات.

سيناريوهات الإعداد التالية مدعومة:

+ [مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement جديد](#new-new)
+ [مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement حالي](#new-existing)
+ [مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل جديد لتطبيق customer engagement](#new-data-new)
+ [مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل موجود لتطبيق customer engagement حالي](#new-data-existing)
+ [مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement جديد](#existing-new)
+ [مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement حالي](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement جديد

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق customer engagement، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md). عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:

- يتم تزويد بيئة Finance and Operations جديدة فارغة.
- يتم تزويد مثيل جديد وفارغ من تطبيق customer engagement، حيث تم تثبيت حل CRM الأساسي.
- يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.
- يتم تمكين خرائط الكيانات للمزامنة المباشرة.

عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement حالي

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق customer engagement حالي، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md). عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:

- يتم تزويد بيئة Finance and Operations جديدة فارغة.
- يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.
- يتم تمكين خرائط الكيانات للمزامنة المباشرة.

عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.

لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.

1. أنشئ شركة جديدة في تطبيق Finance and Operations.
2. أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.
3. [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.
4. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>مثيل تطبيق Finance and Operations جديد ويحتوي على بيانات ومثيل تطبيق customer engagement جديد

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل جديد لتطبيق customer engagement، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق customer engagement‬](#new-new) في قسم سابق من هذا الموضوع. عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.

1. افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>مثيل تطبيق Finance and Operations جديد يحتوي على بيانات ومثيل تطبيق customer engagement حالي

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل حالي لتطبيق customer engagement، اتبع الخطوات الموجودة في [مثيل لتطبيق Finance and Operations ومثيل حالي لتطبيق customer engagement‬](#new-existing) في قسم سابق من هذا الموضوع. عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.

1. افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.

1. أنشئ شركة جديدة في تطبيق Finance and Operations.
2. أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.
3. [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.
4. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement جديد

يحدث إعداد اتصال الكتابة المزدوجة بين مثيل حالي لتطبيق Finance and Operations ومثيل جديد لتطبيق customer engagement في بيئة Finance and Operation.

1. [قم بإعداد الاتصال من تطبيق Finance and Operations ](enable-dual-write.md).
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement حالي

يحدث إعداد اتصال الكتابة المزدوجة بين مثيل حالي لتطبيق Finance and Operations ومثيل حالي لتطبيق customer engagement في بيئة Finance and Operation.

1. قم بإعداد الاتصال من تطبيق Finance and Operations.
2. لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬
3. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.

للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).

## <a name="example"></a>مثال

على سبيل المثال، راجع [تمكين Customers الإصدار 3—تعيين كيان جهات الاتصال](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

للحصول على أسلوب بديل يستند إلى وحدات تخزين البيانات في كل كيان التي يجب تشغيل المزامنة الأولية بها، راجع [اعتبارات المزامنة الأولية](initial-sync-guidance.md).
