---
title: بطاقات ولاء العملاء ونقاط المكافآت
description: يصف هذا الموضوع تكامل البيانات حول بطاقات ولاء العملاء ونقاط المكافأة في الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747977"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>بطاقات ولاء العملاء ونقاط المكافآت

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تعمل الشركات على تصنيف العملاء وتوفير خدمات معقدة، استنادًا إلى أنماط تسوق وانفاق العميل. على سبيل المثال، يشتمل Dynamics 365 Commerce على البنية الأساسية والوظائف لتسهيل ومعالجة بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت والتسعير المستند إلى الولاء وخبرات الشراء المستندة إلى المكافآت. عند مزامنة بيانات حول بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت في Commerce مع Dataverse، فإن تطبيقات Customer Engagement يمكنها استخدام هذه البيانات. على سبيل المثال، يستطيع مستخدمو Dynamics 365 Customer Service استخدام البيانات لتوفير نفس الخدمات المعقدة من خلال مركز المساعدة.

## <a name="templates"></a>القوالب

| تطبيقات Finance and Operations | التطبيقات المستندة إلى نموذج في Dynamics 365 | ‏‏الوصف |
|-----------------------------|-----------------------------------|-------------|
| بطاقة الولاء                | msdyn\_loyaltycards               | يقوم هذا القالب بمزامنة معلومات بطاقات ولاء العملاء. |
| نقاط مكافآت الولاء       | msdyn\_loyaltyrewardpoints        | يقوم هذا القالب بمزامنة معلومات نقاط مكافآت العملاء. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]