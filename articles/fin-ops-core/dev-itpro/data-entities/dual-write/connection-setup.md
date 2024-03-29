---
title: إرشادات حول إعداد الكتابة المزدوجة
description: تصف هذه المقالة السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289733"
---
# <a name="guidance-for-dual-write-setup"></a>إرشادات حول إعداد الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة التمويل والعمليات وبيئة Dataverse.

+ توفر **بيئة التمويل والعمليات** النظام الأساسي **لتطبيقات التمويل والعمليات** (على سبيل المثال، Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Commerce وDynamics 365 Human Resources).
+ توفر **بيئة Dataverse** النظام الأساسي **لتطبيقات customer engagement** ‏(Dynamics 365 Sales وDynamics 365 Customer Service وDynamics 365 column Service وDynamics 365 Marketing وDynamics 365 Project Service Automation).


> [!IMPORTANT]
> تدعم الوحدة النمطية الموارد البشرية في Dynamics 365 Finance اتصالات الكتابة المزدوجة، ولكن لا يدعمها تطبيق Dynamics 365 Human Resources .

تختلف آلية الإعداد باختلاف اشتراكك وبيئتك:

+ بالنسبة إلى المثيلات الجديدة لتطبيقات التمويل والعمليات، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS). إذا كان لديك ترخيص Microsoft Power Platform، فستحل على بيئة Dataverse جديدة، إذا لم يكن لدى المستأجر بيئة.
+ بالنسبة إلى المثيلات الموجودة لتطبيقات التمويل والعمليات، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة التمويل والعمليات.

قبل بدء الكتابة المزدوجة على كيان ما، يمكنك تشغيل مزامنة أولية لمعالجة البيانات الموجودة على الجانبين: تطبيقات التمويل والعمليات وتطبيقات مشاركة العميل. يمكنك تخطي المزامنة الأولية إذا لم تكن بحاجة إلى مزامنة البيانات بين البيئتين.

تتيح المزامنة الأولية إمكانية نسخ البيانات الموجودة من تطبيق واحد إلى آخر بشكل ثنائي الاتجاه. هناك العديد من سيناريوهات الإعداد، بناءً على البيئات التي لديك بالفعل ونوع البيانات الموجودة فيها.

سيناريوهات الإعداد التالية مدعومة:

+ [مثيل جديد لتطبيقات التمويل والعمليات ومثيل جديد لتطبيق مشاركة العميل](#new-new)
+ [مثيل جديد لتطبيقات التمويل والعمليات ومثيل موجود لتطبيق مشاركة العميل](#new-existing)
+ [مثيل جديد لتطبيقات التمويل والعمليات يحتوي على بيانات ومثيل جديد لتطبيق مشاركة العميل](#new-data-new)
+ [مثيل جديد لتطبيق التمويل والعمليات يحتوي على بيانات ومثيل موجود لتطبيق مشاركة العميل](#new-data-existing)
+ [مثيل موجود لتطبيق التمويل والعمليات ومثيل جديد لتطبيق مشاركة العميل](#existing-new)
+ [مثيل موجود لتطبيق التمويل والعمليات ومثيل موجود لتطبيق مشاركة العميل](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>مثيل جديد لتطبيق التمويل والعمليات ومثيل جديد لتطبيق مشاركة العميل

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق التمويل والعمليات لا يحتوي على بيانات ومثيل جديد لتطبيق مشاركة العميل، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md). عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:

- يتم تزويد بيئة جديدة وفارغة في التمويل والعمليات.
- يتم تزويد مثيل جديد وفارغ من تطبيق customer engagement، حيث تم تثبيت حل CRM الأساسي.
- يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.
- يتم تمكين خرائط الجداول للمزامنة المباشرة.

عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>مثيل جديد لتطبيق التمويل والعمليات ومثيل موجود لتطبيق مشاركة العميل

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق التمويل والعمليات لا يحتوي على بيانات ومثيل موجود لتطبيق مشاركة العميل، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md). عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:

- يتم تزويد بيئة جديدة وفارغة في التمويل والعمليات.
- يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.
- يتم تمكين خرائط الجداول للمزامنة المباشرة.

عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.

لمزامنة بيانات Dataverse الموجودة مع تطبيق التمويل والعمليات، اتبع الخطوات التالية.

1. أنشئ شركة جديدة في تطبيق التمويل والعمليات.
2. أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.
3. [قم بتمهيد](bootstrap-company-data.md) بيانات Dataverse باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.
4. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.

للحصول على روابط لمثال لذلك وطريقة بديلة، راجع قسم [المثال](#example) لاحقًا في هذه المقالة.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>مثيل جديد لتطبيق التمويل والعمليات يحتوي على بيانات ومثيل جديد لتطبيق مشاركة العميل

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق التمويل والعمليات الذي يحتوي على بيانات ومثيل جديد لتطبيق مشاركة العميل، اتبع الخطوات الموجودة في [قسم مثيل جديد لتطبيق التمويل والعمليات ومثيل جديد لتطبيق مشاركة العميل](#new-new) سابقًا من هذه المقالة. عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.

1. افتح تطبيق التمويل والعمليات من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.

للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>مثيل جديد لتطبيق التمويل والعمليات يحتوي على بيانات ومثيل موجود لتطبيق مشاركة العميل

لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق التمويل والعمليات الذي يحتوي على بيانات ومثيل موجود لتطبيق مشاركة العميل، اتبع الخطوات الموجودة في [تطبيق مثيل جديد لتطبيق التمويل والعمليات ومثيل موجود لتطبيق مشاركة العميل](#new-existing) سابقًا في هذه المقالة. عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.

1. افتح تطبيق التمويل والعمليات من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.

لمزامنة بيانات Dataverse الموجودة مع تطبيق التمويل والعمليات، اتبع الخطوات التالية.

1. أنشئ شركة جديدة في تطبيق التمويل والعمليات.
2. أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.
3. [قم بتمهيد](bootstrap-company-data.md) بيانات Dataverse باستخدام كود شركة ISO المكون من ثلاثة أحرف.
4. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.

للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>مثيل موجود لتطبيق التمويل والعمليات ومثيل جديد لتطبيق مشاركة العميل

يحدث إعداد اتصال الكتابة المزدوجة بين مثيل موجود لتطبيق التمويل والعمليات ومثيل جديد لتطبيق مشاركة العميل في بيئة التمويل والعمليات.

1. [إعداد الاتصال من تطبيق التمويل والعمليات](enable-dual-write.md).
2. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.

للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>مثيل موجود لتطبيق التمويل والعمليات ومثيل موجود لتطبيق مشاركة العميل

يحدث إعداد اتصال الكتابة المزدوجة بين مثيل موجود لتطبيق التمويل والعمليات ومثيل موجود لتطبيق مشاركة العميل في بيئة التمويل والعمليات.

1. [إعداد الاتصال من تطبيق التمويل والعمليات](enable-dual-write.md).
2. لمزامنة بيانات Dataverse الموجودة مع تطبيق التمويل والعمليات، يمكنك [تمهيد](bootstrap-company-data.md) بيانات Dataverse باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬
3. قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.

للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).

## <a name="example"></a>مثال

على سبيل المثال، راجع [تمكين Customers الإصدار 3—تعيين جدول جهات الاتصال](enable-entity-map.md#enable-table-map)

للحصول على أسلوب بديل يستند إلى وحدات تخزين البيانات في كل كيان التي يجب تشغيل المزامنة الأولية بها، راجع [اعتبارات المزامنة الأولية](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
