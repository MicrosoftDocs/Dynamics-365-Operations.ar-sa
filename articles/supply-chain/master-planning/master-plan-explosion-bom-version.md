---
title: تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬
description: توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbdfc169365cb73e13383b11efcd8983aef4bbca
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815308"
---
# <a name="explosion-of-a-bom-version"></a>تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬

[!include [banner](../includes/banner.md)]

توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.

تؤدي عملية تحديد إجمالي المكونات المطلوبة لطلب خاص إصدار قائمة مكونات الصنف إلى إنشاء طلب لكل صنف بند في قائمة مكونات الصنف في موقع محدد وربما في مستودع محدد. وفي قائمة مكونات الصنف الخاصة بأحد المواقع، يمكن تحديد مستودع خاص لكل بند في قائمة مكونات الصنف. بالإضافة إلى ذلك، تحدد إعدادات بُعد الصنف بالنسبة لكل بند في قائمة مكونات الصنف ما إذا كان المستودع مطلوبًا أم لا. وبدوره يصبح هذا الطلب الناتج لكل صنف بند في قائمة مكونات الصنف نقطة البدء لتحديد إجمالي المكونات المطلوبة للطلب الإضافي. يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   بُعد الموقع إلزامي، ويجب إدخاله في حركة الطلب.
-   بُعد الموقع متناسق. لذلك فالموقع للطلب من المستوى الأدنى هو نفس الموقع في حركة الطلب المبدئي.

يوضح الرسم التخطيطي التالي الكيفية التي تتم بها عملية تحديد إجمالي المكونات المطلوبة لطلب التخطيط الرئيسي. ![طلب عملية تحديد إجمالي المكونات المطلوبة باستخدام إصدار شجرة المواد](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>الموارد الإضافية
--------

[تحديد إصدار BOM](master-plan-bom-version-determined.md)

[نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)



