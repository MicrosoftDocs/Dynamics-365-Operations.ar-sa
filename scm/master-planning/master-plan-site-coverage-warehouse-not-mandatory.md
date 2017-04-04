---
title: "التخطيط لتغطية الموقع والمستودع ليس إلزامياً الرئيسي"
description: "يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية."
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 28607f0fc8db99c9fc8e96b4514763b8cf589dd8
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>التخطيط لتغطية الموقع والمستودع ليس إلزامياً الرئيسي

يصف هذا الموضوع كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية.

يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.
-   عدم تعيين بُعد المستودع على إلزامي. فقد يكون المستودع معروفًا، لكنه غير مستخدم في حساب التخططي الرئيسي.
-   تعيين بُعد الموقع لتخطيط التغطية.
-   عدم تعيين بُعد المستودع لتخطيط التغطية. ولذلك يتم تجميع العرض والطلب حسب الموقع، وربما حسب الأبعاد الأخرى المخططة في التغطية أيضا.

يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي. تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:
-   تحديد تغطية الصنف. انقر فوق **إدارة معلومات المنتج &gt;منتجات&gt; المنتجات التي تم إصدارها**. حدد العنصر ومن ثم انقر فوق **خطة &gt;تغطية الصنف**.
-   تحديد علاقات إعادة الملء للمستودع. انقر فوق **إدارة مخزون &gt;الإعداد &gt;تصنيف المخزون &gt;مستودعات**. وفي علامة التبويب **التخطيط الرئيسي**، راجع مجموعة حقل **المستودع الرئيسي**.
-   يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان. انقر فوق **إدارة معلومات المنتج &gt;منتجات&gt; المنتجات التي تم إصدارها**. حدد العنصر ومن ثم انقر فوق **خطة &gt;إعدادات الأمر الافتراضية**. وفي نموذج **إعدادات الأوامر الافتراضية**، راجع حقل **نوع الأمر الافتراضي**.

![طلب مستودع تغطية الموقع ليس إلزاميًا    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>راجع أيضًا
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي-كيف يتم تحديد إصدار شجرة المواد](master-plan-bom-version-determined.md)


