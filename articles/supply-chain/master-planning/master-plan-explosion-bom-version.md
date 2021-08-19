---
title: تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬
description: توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55b94bca10441a3757715e02b23f11b2f11650939b6fdcbbf978f896b414d016
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729473"
---
# <a name="explosion-of-a-bom-version"></a>تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬

[!include [banner](../includes/banner.md)]

توضح هذه المقالة سيناريو التخطيط الرئيسي الذي يتضمن تحديد إجمالي المكونات المطلوبة‬ لإصدار قائمة مكونات الصنف‬.

تؤدي عملية تحديد إجمالي المكونات المطلوبة لطلب خاص إصدار قائمة مكونات الصنف إلى إنشاء طلب لكل صنف بند في قائمة مكونات الصنف في موقع محدد وربما في مستودع محدد. وفي قائمة مكونات الصنف الخاصة بأحد المواقع، يمكن تحديد مستودع خاص لكل بند في قائمة مكونات الصنف. بالإضافة إلى ذلك، تحدد إعدادات بُعد الصنف بالنسبة لكل بند في قائمة مكونات الصنف ما إذا كان المستودع مطلوبًا أم لا. وبدوره يصبح هذا الطلب الناتج لكل صنف بند في قائمة مكونات الصنف نقطة البدء لتحديد إجمالي المكونات المطلوبة للطلب الإضافي. يتضمن سيناريو التخطيط الرئيسي هذا الشروط التالية:

-   بُعد الموقع إلزامي، ويجب إدخاله في حركة الطلب.
-   بُعد الموقع متناسق. لذلك فالموقع للطلب من المستوى الأدنى هو نفس الموقع في حركة الطلب المبدئي.

يوضح الرسم التخطيطي التالي الكيفية التي تتم بها عملية تحديد إجمالي المكونات المطلوبة لطلب التخطيط الرئيسي. ![طلب عملية تحديد إجمالي المكونات المطلوبة باستخدام إصدار قائمة مكونات الصف.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>الموارد الإضافية

[تحديد إصدار BOM](master-plan-bom-version-determined.md)

[نظرة عامة على التخطيط الرئيسي ووظائف المواقع المتعددة](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]