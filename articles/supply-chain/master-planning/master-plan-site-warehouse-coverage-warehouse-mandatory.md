---
title: التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع إلزامي
description: يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. يُعد بُعد المستودع إلزاميًا.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41530a10eba71716a07e593d6d93e35fecd83b34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989733"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع إلزامي

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. يُعد بُعد المستودع إلزاميًا.

يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.
-   تم تعيين بُعد المستودع على إلزامي ويجب إدخاله في حركة الطلب.
-   تم تعيين الموقع وأبعاد المستودع لتخطيط التغطية. يمكن تعيين أبعاد الأخرى لتخطيط التغطية أيضًا. ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.

يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي. تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:
-   تم تعيين المستودع إلى **يدوي‏‎**. انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**. وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **الدليل**.
-   تحديد تغطية الصنف. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة**، انقر فوق **تغطية الصنف**.
-   تحديد علاقات إعادة الملء للمستودع. انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**. وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **المستودع الرئيسي**.
-   يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة**، انقر فوق **إعدادات الأوامر الافتراضية**. وفي نموذج **إعدادات الأوامر الافتراضية**، راجع **نوع الأمر الافتراضي**.

![طلب تغطية الموقع والمستودع، إلزاميًا](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>الموارد الإضافية
--------

[نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)

[التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي](master-plan-site-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع غير إلزامي](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[تحديد إصدار BOM](master-plan-bom-version-determined.md)



