---
title: إضافة الدعم إلى شبكة تسليم المحتوى (CDN)
description: يوضح هذا المقال كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة  Microsoft Dynamics 365 Commerce الخاصة بك.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2ed8f66d447e1d9e890c0885fd20e9b55c66ac0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855866"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>إضافة الدعم إلى شبكة تسليم المحتوى (CDN)

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية إضافة شبكة توصيل المحتوى (CDN) إلى بيئة  Microsoft Dynamics 365 Commerce الخاصة بك.

عندما تقوم بإعداد بيئة تجارة إلكترونية في Dynamics 365 Commerce، يُمكنك تكوينها للعمل مع خدمة CDN الخاصة بك. 

يُمكن تمكين مجالك المُخصص أثناء عملية التوفير لبيئة التجارة الإلكترونية الخاصة بك. وبدلًا من ذلك، يُمكن استخدام طلب خدمة لإعداده بعد اكتمال عملية التوفير. تقوم عملية توفير بيئة التجارة الإلكترونية بإنشاء اسم مضيف مرتبط بالبيئة. يكون لاسم هذا المضيف التنسيق التالي، حيث \<*e-commerce-tenant-name*\> هو اسم بيئتك:

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

يدعم اسم المضيف أو النقطة النهائية التي يتم إنشاؤها خلال عملية التوفير شهادة طبقة مآخذ التوصيل الآمنة (SSL) فقط لـ \*.commerce.dynamics.com.  ولا يدعم SSL للمجالات المُخصصة. وبالتالي، يجب عليك إنهاء SSL للمجالات المخصصة في CDN الخاصة بك وإعادة توجيه حركة النقل من CDN إلى اسم المضيف أو النقطة النهائية التي قام Commerce بإنشائها. 

بالإضافة إلى ذلك، يتم عرض *الإحصاءات* (إما JavaScript أو ملفات أوراق الأنماط المتتالية \[CSS\]) من Commerce من النقطة النهائية الذي قام Commerce بإنشاءها (\*.commerce.dynamics.com). يُمكن تخزين هذه الإحصائيات مؤقتًا فقط في حالة إذا تم وضع اسم المضيف أو نقطة النهاية التي قام Commerce بإنشائها بعد CDN.

## <a name="set-up-ssl"></a>إعداد SSL

بعد توفير بيئة Commerce الخاصة بك مع المجال المخصص الذي تم توفيره، أو بعد أن تقوم بتوفير مجال مخصص للبيئة الخاصة بك باستخدام طلب خدمة، تحتاج إلى العمل مع فريق إعداد Commerce للتخطيط لتغييرات DNS.

وكما سبق ذكره، يدعم اسم المضيف أو نقطة النهاية التي تم إنشائها شهادة SSL فقط لـ \*.commerce.dynamics.com.  ولا يدعم SSL للمجالات المُخصصة.

## <a name="cdn-services"></a>خدمات CDN

يُمكن استخدام أي خدمة من خدمات CDN مع بيئة Commerce. وفيما يلي مثالين:

- **Microsoft Azure Front Door Service** – حل Azure CDN. للمزيد من المعلومات حول Azure Front Door Service، راجع [وثائق Azure Front Door Service](/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – للمزيد من المعلومات، راجع [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>إعداد CDN

تتكون عملية إعداد CDN من الخطوات العامة التالية:

1. إضافة مضيف واجهة أمامية.
1. تكوين وعاء خلفي.
1. إعداد قواعد التوجيه.

### <a name="add-a-front-end-host"></a>إضافة مضيف واجهة أمامية

يُمكن استخدام أي خدمة من خدمات CDN، ولكن بالنسبة للمثال الموجود في هذا المقال، يتم استخدام Azure Front Door Service. 

للحصول على معلومات حول كيفية إعداد Azure Front Door Service، راجع [Quickstart: إنشاء Front Door لتطبيق الويب العمومي المتوفرة بشكل كبير](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>تكوين وعاء خلفي في Azure Front Door Service

لتكوين وعاء خلفي في Azure Front Door Service، اتبع الخطوات التالية.

1. أضف **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** إلى تجمع الخلفية كمضيف مخصص له رأس مضيف خلفي مماثل لـ **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.
1. تحت **موازنة التحميل**، اترك القيم الافتراضية.
1. تعطيل عمليات فحص السلامة لمجموعة الخلفية.

يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service مع إدخال اسم مضيف وعاء خلفي.

![إضافة مربع حوار وعاء خلفي.](./media/CDN_BackendPool.png)

يُبين الرسم التوضيحي التالي مربع الحوار **إضافة وعاء خلفي** في Azure Front Door Service مع قيم موازنة الحمل الافتراضي.

![إضافة مربع حوار وعاء خلفي يتبع.](./media/CDN_BackendPool_2.png)

> [!NOTE]
> تأكد من تعطيل **فحوصات السلامة** عند إعداد خدمة Azure Front Door لـ Commerce.


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


> [!WARNING]
> إذا كان المجال الذي ستستخدمه نشطًا ومباشرًا، فأنشئ تذكرة دعم من الإطار المتجانب **الدعم** في [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) للحصول على المساعدة لخطواتك التالية. للحصول على مزيد من المعلومات، راجع [الحصول على الدعم لتطبيقات التمويل والعمليات أو Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

إذا كان مجالك جديدًا وليس مجالاً مباشرًا موجودًا بشكل مسبق، فيمكنك إضافة مجال مخصص إلى تكوين Azure Front Door Service. سيؤدي ذلك إلى تمكين حركة مرور الويب لتوجيه موقعك عبر مثيل Azure Front Door. لإضافة مجال مخصص (على سبيل المثال، `www.fabrikam.com`)، يجب عليك تكوين اسم متعارف عليه (CNAME) للمجال.

يُبين الرسم التوضيحي التالي مربع الحوار **تكوين CNAME** في Azure Front Door Service.

![مربع حوار تكوين CNAME.](./media/CNAME_Configuration.png)

يُمكنك استخدام Azure Front Door Service لإدارة الشهادة، أو يُمكنك استخدام شهادتك الخاصة للمجال المخصص. 

يُبين الرسم التوضيحي التالي مربع الحوار **HTTP للمجال المخصص** في Azure Front Door Service.

![مربع حوار HTTP للمجال المخصص.](./media/Custom_Domain_HTTPS.png)

للحصول على إرشادات مفصلة حول إضافة مجال مخصص إلى Azure Front Door، راجع [إضافة مجال مخصص إلى Front Door](/azure/frontdoor/front-door-custom-domain).

يجب الآن تكوين CDN بشكل صحيح بحيث يُمكن استخدامه مع موقع Commerce الخاص بك.

## <a name="additional-resources"></a>الموارد الإضافية

[خيارات تنفيذ شبكة تسليم المحتويات](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]