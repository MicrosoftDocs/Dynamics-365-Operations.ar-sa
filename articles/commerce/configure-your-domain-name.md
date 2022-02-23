---
title: تكوين اسم مجالك
description: يوضح هذا الموضوع كيفية تكوين اسم مجال لموقع التجارة الإلكترونية Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ac1b0c8baaddd6ca62cc49657fff364df21c14f2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517102"
---
# <a name="configure-your-domain-name"></a>تكوين اسم مجالك


[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية تكوين اسم مجال لموقع التجارة الإلكترونية Microsoft Dynamics 365. 

## <a name="add-domains-during-e-commerce-initialization"></a>إضافة المجالات أثناء تهيئة التجارة الإلكترونية

لربط المجالات ببيئة التجارة الإلكترونية لـ Dynamics 365 Commerce الخاصة بك، قم بتهيئة التجارة الإلكترونية كما هو موضح في [نشر مستأجر تجارة إلكترونية جديد‬](deploy-ecommerce-site.md). أثناء التهيئة، يُطلب منك تقديم المعلومات التي سيتم استخدامها لتوفير بيئة التجارة الإلكترونية الخاصة بك. في حقل **أسماء الأجهزة المضيفة المدعومة** ، أضف جميع المجالات التي تخطط لاستخدامها مع هذه البيئة. يجب الفصل بين المجالات المتعددة بفاصلة منقوطة. وبهذه الطريقة، يتم تكوين المجالات في جميع مكونات التجارة الإلكترونية المطلوبة، وتكون جاهزة للاستخدام عند تبديل حركة المرور من شبكة تسليم المحتوى (CDN) أو خادم الويب وتوجيهها إلى الأطراف الأمامية للتجارة الإلكترونية.

## <a name="add-domains-after-e-commerce-initialization"></a>إضافة المجالات بعد تهيئة التجارة الإلكترونية

لربط المجالات الجديدة ببيئة التجارة الإلكترونية الخاصة بك بعد تهيئة التجارة الإلكترونية، يجب عليك تقديم طلب خدمة.

## <a name="additional-resources"></a>الموارد الإضافية

[نشر مستأجر التجارة الإلكترونية الجديد](deploy-ecommerce-site.md)

[إنشاء موقع تجارة إلكترونية](create-ecommerce-site.md)

[إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت](associate-site-online-store.md)

[إدارة ملفات robots.txt](manage-robots-txt-files.md)

[تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع](upload-bulk-redirects.md)

[إعداد مستأجر B2C في Commerce](set-up-B2C-tenant.md)

[إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين](custom-pages-user-logins.md)

[تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce](configure-multi-B2C-tenants.md)

[إضافة الدعم إلى شبكة تسليم المحتوى (CDN)](add-cdn-support.md)

[تمكين اكتشاف المتجر استنادًا إلى الموقع](enable-store-detection.md)
