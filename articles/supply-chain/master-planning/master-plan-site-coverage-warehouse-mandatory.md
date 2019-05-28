---
title: التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي
description: يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية. يُعد المستودع بُعدًا إلزاميًا.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f61c142fff73fdeeca573cca3f54e654511af1e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556402"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية. يُعد المستودع بُعدًا إلزاميًا.

يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب. لا يمكن تعديل هذا الإعداد.
-   تم تعيين بُعد المستودع على إلزامي ويجب إدخاله في حركة الطلب.
-   تعيين بُعد الموقع لتخطيط التغطية. ويمكن تعيين أبعاد أخرى لتخطيط التغطية أيضًا. ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.
-   عدم تعيين بُعد المستودع لتخطيط التغطية. ولذلك يتم تجميع العرض والطلب حسب الموقع، وربما حسب الأبعاد الأخرى المخططة في التغطية أيضا.

يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي. تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:
-   تحديد تغطية الصنف. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم انقر فوق **خطة &gt; تغطية الصنف**.
-   تحديد علاقات إعادة الملء للمستودع. انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**. وفي علامة التبويب **التخطيط الرئيسي**، راجع مجموعة حقل **المستودع الرئيسي**.
-   يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم انقر فوق **خطة &gt; إعدادات الأوامر الافتراضية**. وفي نموذج **إعدادات الأوامر الافتراضية**، راجع **نوع الأمر الافتراضي**.

![طلب مستودع تغطية الموقع إلزاميًا](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>الموارد الإضافية
--------

[التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع. المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف](master-plan-bom-version-determined.md)



