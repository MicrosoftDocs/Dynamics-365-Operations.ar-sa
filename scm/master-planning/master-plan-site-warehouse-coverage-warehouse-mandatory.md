---
title: "التخطيط لتغطية الموقع والمستودع، إلزامية المستودع الرئيسي"
description: "يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. يُعد بُعد المستودع إلزاميًا."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>التخطيط لتغطية الموقع والمستودع، إلزامية المستودع الرئيسي

يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعدي الموقع والمستودع له للتغطية. يُعد بُعد المستودع إلزاميًا.

يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.
-   تم تعيين بُعد المستودع على إلزامي ويجب إدخاله في حركة الطلب.
-   تم تعيين الموقع وأبعاد المستودع لتخطيط التغطية. يمكن تعيين أبعاد الأخرى لتخطيط التغطية أيضًا. ولكن لا تتأثر هذه الأبعاد بوظيفة المواقع المتعددة.

يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي. تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:
-   The warehouse is set to **Manual**. انقر فوق **إدارة مخزون &gt;الإعداد &gt;تصنيف المخزون &gt;مستودعات**. وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **الدليل**.
-   تحديد تغطية الصنف. انقر فوق **إدارة معلومات المنتج &gt;منتجات&gt; المنتجات التي تم إصدارها**. حدد العنصر، ثم في جزء الإجراءات، على **خطة** ، انقر فوق **تغطية الصنف**.
-   تحديد علاقات إعادة الملء للمستودع. انقر فوق **إدارة مخزون &gt;الإعداد &gt;تصنيف المخزون &gt;مستودعات**. وفي علامة التبويب السريع **التخطيط الرئيسي**، راجع حقل **المستودع الرئيسي**.
-   يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان. انقر فوق **إدارة معلومات المنتج &gt;منتجات&gt; المنتجات التي تم إصدارها**. حدد العنصر، ثم في جزء الإجراءات، على **خطة** ، انقر فوق **إعدادات الأمر الافتراضية**. وفي نموذج **إعدادات الأوامر الافتراضية**، راجع **نوع الأمر الافتراضي**.

![طلب تغطية الموقع والمستودع، إلزاميًا](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>راجع أيضًا
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع، المستودع غير إلزامي](master-plan-site-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف](master-plan-bom-version-determined.md)


