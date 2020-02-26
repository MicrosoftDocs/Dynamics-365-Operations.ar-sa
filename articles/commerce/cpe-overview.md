---
title: نظرة عامة على بيئة معاينة Dynamics 365 Commerce
description: يقدم هذا الموضوع نظرة عامة على بيئة معاينة Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024673"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a>نظرة عامة على بيئة معاينة Dynamics 365 Commerce


[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على بيئة معاينة Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

بيئة معاينة التجارة هي بيئة معاينة شاملة لـ Dynamics 365 Commerce تتيح للعملاء المحتملين تجربة منتج التجارة قبل صدوره بشكل عام للجمهور.

بصرف النظر عن بعض القيود البسيطة التي لا تؤثر على الميزات أو الوظائف، توفر بيئة معاينة التجارة تجربة التجارة الكاملة، ويمكن استخدامها من قبل العملاء وشركاء التنفيذ لتقييم المنتج ، وتقديم الملاحظات ، وتحليل الملاءمة / الفجوة.

## <a name="limitations-of-the-commerce-preview-environment"></a>قيود بيئة معاينة التجارة

على الرغم من أن بيئة معاينة التجارة توفر مجموعة كاملة من ميزات ووظائف التجارة، إلا أن هناك بعض القيود الثانوية:

- على الرغم من أن بيئة معاينة التجارة نفسها لا تحتوي على قيود جغرافية، إلا أنه لا يمكن توفير مكونات البيئة، مثل Retail Cloud Scale Unit (RCSU) وتطبيقات التجارة الإلكترونية، إلا في الولايات المتحدة.
- يقتصر استخدام بيئة المعاينة التجارية على مهلة 30 يومًا من تاريخ توفير التجارة الإلكترونية.
- يمكن نشر بيئة معاينة التجارة بنجاح وتهيئتها فقط في بيئة تستخدم طوبولوجيا العرض التوضيحي، حيث يتم نشر جميع مكونات البيئة في جهاز ظاهري واحد (VM). القيد الرئيسي لمخطط الجهاز الظاهري OneBox هو عدد المستخدمين المتزامنين الذين يمكن أن تدعمهم بيئة المعاينة.
- لا يمكن تقييم بيئة معاينة التجارة إلا إلى أن يكون التوافر العام (GA) لمنتج التجارة. ستكون البيئات التجريبية الجديدة متاحة بعد التوافر العام.

## <a name="get-started"></a>البدء

لتوفير بيئة معاينة التجارة، راجع [توفير بيئة معاينة التجارة](provisioning-guide.md)

## <a name="additional-resources"></a>الموارد الإضافية

[تشغيل بيئة معاينة Dynamics 365 Commerce](provisioning-guide.md)

[تكوين بيئة معاينة Dynamics 365 Commerce](cpe-post-provisioning.md)

[تكوين ميزات اختيارية لبيئة معاينة Dynamics 365 Commerce](cpe-optional-features.md)

[الأسئلة المتداولة حول بيئة معاينة Dynamics 365 Commerce](cpe-faq.md)
