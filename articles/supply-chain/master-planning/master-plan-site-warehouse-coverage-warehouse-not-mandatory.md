---
title: "التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع غير إلزامي"
description: "يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. بُعد المستودع غير إلزامي."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ec5150abd297a7c00ac180db581adb30bef65b3f
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع غير إلزامي

[!include[banner](../includes/banner.md)]


يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. بُعد المستودع غير إلزامي.

يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب. لا يمكن تعديل هذا الإعداد.
-   عدم تعيين بُعد المستودع على إلزامي. فقد يكون المستودع معروفًا، لكنه غير مستخدم في حساب التخططي الرئيسي.
-   تم تعيين الموقع وأبعاد المستودع لتخطيط التغطية. يمكن تعيين أبعاد الأخرى لتخطيط التغطية أيضًا. ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.

يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي. تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:
-   تم تعيين المستودع إلى يدوي. انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**. وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **الدليل**.
-   تحديد تغطية الصنف. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة**، انقر فوق **تغطية الصنف**.
-   تحديد علاقات إعادة الملء للمستودع. انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**. وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **المستودع الرئيسي**.
-   يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم في جزء الإجراءات، في علامة التبويب **خطة**، انقر فوق **إعدادات الأوامر الافتراضية**. وفي نموذج **إعدادات الأوامر الافتراضية**، راجع **نوع الأمر الافتراضي**.

![طلب الموقع والمستودع، ليس المستودع](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>راجع أيضًا
--------

[التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع، المستودع غير إلزامي](master-plan-site-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف](master-plan-bom-version-determined.md)




