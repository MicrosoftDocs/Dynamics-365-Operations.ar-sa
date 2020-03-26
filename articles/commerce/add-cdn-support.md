---
title: إضافة الدعم إلى شبكة تسليم المحتوى (CDN)
description: يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.
author: brianshook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 23ac9d8844c2a8ae20bd316c40078319601a3a4d
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096715"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>إضافة الدعم إلى شبكة تسليم المحتوى (CDN)


[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة Microsoft Dynamics 365 Commerce الخاصة بك.

## <a name="overview"></a>نظرة عامة

عندما تقوم بإعادة بيئة تجارة إلكترونية في Dynamics 365 Commerce، يُمكنك تكوينه للعمل مع خدمة CDN الخاصة بك. 

يُمكن تمكين مجالك المُخصص أثناء عملية التوفير لبيئة التجارة الإلكترونية الخاصة بك. وبدلًا من ذلك، يُمكن استخدام طلب خدمة لإعداده بعد اكتمال عملية التوفير. تقوم عملية توفير بيئة التجارة الإلكترونية بإنشاء اسم مضيف مرتبط بالبيئة. يكون لاسم هذا المضيف التنسيق التالي، حيث يكون *e-commerce-tenant-name* هو اسم البيئة الخاصة بك: 

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

يدعم اسم المضيف أو النقطة النهائية التي يتم إنشاؤها خلال عملية التوفير شهادة طبقة مآخذ التوصيل الآمنة (SSL) فقط لـ \*.commerce.dynamics.com.  ولا يدعم SSL للمجالات المُخصصة. وبالتالي، يجب عليك إنهاء SSL للمجالات المخصصة في CDN الخاصة بك وإعادة توجيه حركة النقل من CDN إلى اسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها. 

بالإضافة إلى ذلك، يتم عرض *الإحصاءات* (إما JavaScript أو ملفات أوراق الأنماط المتتالية \[CSS\]) من Commerce من النقطة النهائية الذي قام Commerce بإنشاءها (\*.commerce.dynamics.com). يُمكن تخزين هذه الإحصائيات مؤقتًا فقط في حالة إذا تم وضع اسم المضيف أو نقطة النهاية التي قام Commerce بإنشائها بعد CDN.

## <a name="set-up-ssl"></a>إعداد نظام إدارة الأوامر الموزعة (SSL)

وللمساعدة في ضمان إعداد SSL، وأنه قد تم تخزين الإحصائيات مؤقتًا، يجب عليك تكوين CDN الخاص بك بحيث يكون مقترنًا باسم المضيف الذي قام Commerce بإنشاءه للبيئة الخاصة بك. كما يجب عليك أيضًا تخزين الأنماط التالية للإحصائيات مؤقتًا فقط: 

/\_msdyn365/\_scnr/\*

بعد توفير بيئة Commerce الخاصة بك مع المجال المخصص الذي تم توفيره، أو بعد أن تقوم بتوفير مجال مخصص للبيئة الخاصة بك باستخدام طلب خدمة، قم بالإشارة إلى مجالك المخصص لاسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها.

وكما سبق ذكره، يدعم اسم المضيف أو نقطة النهاية التي تم إنشائها شهادة SSL فقط لـ \*.commerce.dynamics.com.  ولا يدعم SSL للمجالات المُخصصة.

## <a name="cdn-services"></a>خدمات CDN

يُمكن استخدام أي خدمة من خدمات CDN مع بيئة Commerce. وفيما يلي مثالين:

- **Microsoft Azure Front Door Service** – حل Azure CDN. للمزيد من المعلومات حول Azure Front Door Service، راجع [وثائق Azure Front Door Service](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – للمزيد من المعلومات، راجع [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>إعداد CDN

تتكون عملية إعداد CDN من الخطوات العامة التالية:

1. إضافة مضيف واجهة أمامية.
1. قم بتكوين مجموعة النهاية الخلفية.
1. إعداد القواعد للتوجيه والتخزين المؤقت.

### <a name="add-a-front-end-host"></a>إضافة مضيف واجهة أمامية

يُمكن استخدام أي خدمة من خدمات CDN، ولكن بالنسبة للمثال الموجود في هذا الموضوع، يتم استخدام Azure Front Door Service. 

للحصول على معلومات حول كيفية إعداد Azure Front Door Service، راجع [Quickstart: إنشاء Front Door لتطبيق الويب العمومي المتوفرة بشكل كبير](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>تكوين وعاء خلفي في Azure Front Door Service 

لتكوين وعاء خلفي في Azure Front Door Service، اتبع الخطوات التالية. 

1. إضافة **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** للوعاء الخلفي كمضيف مخصص له عنوان مضيف خلفي فارغ.
1. ضمن **فحوصات الصحة**، في حقل **المسار** ، ادخل **/keepalive**. 
1. في حقل **الفواصل الزمنية (ثوان)** ، ادخل **255**.
1. تحت **موازنة التحميل**، اترك القيم الافتراضية.

يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service. 

![إضافة مربع حوار وعاء خلفي](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>إعداد القواعد في Azure Front Door Service

لإعداد قاعدة التوجيه في Azure Front Door Service، اتبع الخطوات التالية. 

1. إضافة قاعدة التوجيه.
1. في الحقل **الاسم** ، أدخل **‏افتراضي**.
1. في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.
1. في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.
1. تحت **النماذج المطلوب مطابقتها**، في الحقل العلوي، ادخل **/\***.
1. تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.
1. في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. 
1. في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**. 
1. قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.
1. قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.

لإعداد قاعدة التخزين المؤقت في Azure Front Door Service، اتبع الخطوات التالية.

1. إضافة قاعدة التخزين المؤقت.
1. في الحقل **الاسم** ، أدخل **‏الإحصائيات**.
1. في حقل **البروتوكول المقبول** ، حدد **HTTP وHTTPS**.
1. في حقل **مضيفو الواجهة الأمامية** ، ادخل **dynamics-ecom-tenant-name.azurefd.net**.
1. تحت **النماذج المطلوب مطابقتها** ، في الحقل العلوي، **/\_msdyn365/\_scnr/\***.
1. تحت **تفاصيل التوجيه**، قم بتعيين خيار **نوع التوجيه** إلى **للأمام**.
1. في حقل **الوعاء الخلفي** ،حدد **ecom-backend**. 
1. في مجموعة حقل **بروتوكول إعادة التوجيه** ،حدد خيار **مطابقة الطلب**.
1. قم بتعيين خيار **إعادة كتابة عنوان URL** إلى **مُعطل**.
1. قم بتعيين خيار **التخزين المؤقت** إلى **مُعطل**.
1. في حقل **سلوك التخزين المؤقت لسلسلة الاستعلام** ،حدد **تخزين مؤقت لكل عنوان URL فريد**.
1. في مجموعة حقل **الضغط الديناميكي** ،حدد خيار **مُمكّن**.

يُبين الرسم التوضيحي التالي مربع الحوار **إضافة قاعدة** في Azure Front Door Service.

![إضافة مربع حوار قاعدة](./media/CDN_CachingRule.png)

بعد أن يتم نشر هذا التكوين الأولي، يجب عليك إضافة مجالك المخصص إلى التكوين الخاص بـ Azure Front Door Service. لإضافة مجال مخصص (على سبيل المثال، `www.fabrikam.com`)، يجب عليك تكوين اسم متعارف عليه (CNAME) للمجال.

يُبين الرسم التوضيحي التالي مربع الحوار **تكوين CNAME** في Azure Front Door Service.

![مربع حوار تكوين CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> إذا كان المجال الذي سوف تستخدمه نشطًا ومباشرًا بالفعل، اتصل بالدعم لتمكين هذا المجال مع Azure Front Door Service لإعداد اختبار.

يُمكنك استخدام Azure Front Door Service لإدارة الشهادة، أو يُمكنك استخدام شهادتك الخاصة للمجال المخصص. 

يُبين الرسم التوضيحي التالي مربع الحوار **HTTP للمجال المخصص** في Azure Front Door Service.

![مربع حوار HTTP للمجال المخصص](./media/Custom_Domain_HTTPS.png)

يجب الآن تكوين CDN بشكل صحيح بحيث يُمكن استخدامه مع موقع Commerce الخاص بك.

## <a name="additional-resources"></a>الموارد الإضافية

[تكوين اسم مجالك](configure-your-domain-name.md)

[نشر موقع تجارة إلكترونية جديد](deploy-ecommerce-site.md)

[إعداد قناة متجر عبر الإنترنت](online-stores.md)

[إنشاء موقع تجارة إلكترونية](create-ecommerce-site.md)

[إقران موقع عبر الإنترنت بقناة](associate-site-online-store.md)

[إدارة ملفات robots.txt](manage-robots-txt-files.md)

[تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع](upload-bulk-redirects.md)

[إعداد مستأجر B2C في Commerce](set-up-B2C-tenant.md)

[إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين](custom-pages-user-logins.md)

[تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce](configure-multi-B2C-tenants.md)

[تمكين اكتشاف المتجر استنادًا إلى الموقع](enable-store-detection.md)
