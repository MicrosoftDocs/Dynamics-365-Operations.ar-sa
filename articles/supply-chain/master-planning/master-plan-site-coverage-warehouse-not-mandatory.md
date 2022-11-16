---
title: التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي
description: يصف هذا المقال كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b03bd1970aa7a2f3276186a0a9f8c2cd2880956
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741139"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي

[!include [banner](../includes/banner.md)]

يصف هذا المقال كيف يتم التخطيط لصنف تم تعيين بُعد الموقع له للتغطية.

يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   تم تعيين بُعد الموقع إلى إلزامي، ويجب إدخاله في حركة الطلب.
-   عدم تعيين بُعد المستودع على إلزامي. فقد يكون المستودع معروفًا، لكنه غير مستخدم في حساب التخططي الرئيسي.
-   تعيين بُعد الموقع لتخطيط التغطية.
-   عدم تعيين بُعد المستودع لتخطيط التغطية. ولذلك يتم تجميع العرض والطلب حسب الموقع، وربما حسب الأبعاد الأخرى المخططة في التغطية أيضا.

يوضح الرسم التالي كيفية تقدم التخطيط الرئيسي. تكون المحددات المشار إليها في الرسم ومواقعها كما يلي:
-   تحديد تغطية الصنف. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم انقر فوق **خطة &gt; تغطية الصنف**.
-   تحديد علاقات إعادة الملء للمستودع. انقر فوق **إدارة المخزون &gt; الإعداد &gt; تصنيف المخزون &gt; المستودعات**. وفي علامة التبويب **التخطيط الرئيسي**، راجع مجموعة حقل **المستودع الرئيسي**.
-   يتم تعيين نوع الأمر الافتراضي للإنتاج أو أمر الشراء أو كانبان. انقر فوق **إدارة معلومات المنتج &gt; المنتجات&gt; المنتجات الصادرة**. حدد الصنف، ثم انقر فوق **خطة &gt; إعدادات الأوامر الافتراضية**. وفي نموذج **إعدادات الأوامر الافتراضية**، راجع حقل **نوع الأمر الافتراضي**.

![طلب مستودع تغطية الموقع ليس إلزاميًا.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)
- [التخطيط الرئيسي لتغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)
- [التخطيط الرئيسي لتغطية الموقع، المستودع إلزامي](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [التخطيط الرئيسي لتغطية الموقع، المستودع غير إلزامي](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [تحديد إصدار BOM](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]