---
title: "التخطيط الرئيسي ووظائف المواقع المتعددة"
description: "يأخذ التخطيط الرئيسي إعدادات أبعاد مخزون المستودع والموقع في الاعتبار."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 19eeee753c15cf2670948ce2c615a112813c16ad
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-and-multisite-functionality"></a>التخطيط الرئيسي ووظائف المواقع المتعددة

يأخذ التخطيط الرئيسي إعدادات أبعاد مخزون المستودع والموقع في الاعتبار. 

بُعد الموقع إلزامي ويمكنك تعيين بُعد المستودع بحيث يكون إلزاميًا.

وعندما يكون البعد إلزاميًا، يجب إدخال قيمة البعد على كافة حركات المخزون. ولذلك، وخلال التخطيط الرئيسي، يكون الموقع والمستودع للطلب الأولي معروفين. ويكون بعد الموقع كذلك متوافقًا حتى لا تتغير قيمة الموقع أثناء عملية تحديد إجمالي المكونات المطلوبة للطلب منخفض المستوى.

وعندما لا يتم تعيين المستودع ليكون إلزاميًا، قد لا يُعرف من الطلب الأولي. ويجب أن يحدد محرك التخطيط المستودع الذي سيستخدمه بناءً على الإعدادات المحددة للصنف، والمستودعات الفردية، وكذلك تفاصيل بند الأمر.

توضح مقالات wiki التالية كيفية عمل محرك التخطيط، عند تحديد إعدادات مختلفة، لتحديد المستودع الذي سيتم استخدامه.

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع إلزامي](master-plan-site-coverage-warehouse-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع والمستودع، المستودع غير إلزامي](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - تغطية الموقع، المستودع غير إلزامي](master-plan-site-coverage-warehouse-not-mandatory.md)

[التخطيط الرئيسي - كيفية تحديد إصدار قائمة مكونات الصنف](master-plan-bom-version-determined.md)


