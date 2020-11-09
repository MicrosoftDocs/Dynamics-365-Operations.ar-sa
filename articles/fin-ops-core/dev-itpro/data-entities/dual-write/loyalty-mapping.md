---
title: بطاقات ولاء العملاء ونقاط المكافآت
description: يصف هذا الموضوع تكامل البيانات حول بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998003"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>بطاقات ولاء العملاء ونقاط المكافآت

[!include [banner](../../includes/banner.md)]



تعمل الشركات على تصنيف العملاء وتوفير خدمات معقدة، استنادًا إلى أنماط تسوق وانفاق العميل. في مجموعة تطبيقات Microsoft Dynamics 365 ، لدى Dynamics 365 Commerce البنية الأساسية والوظائف لتسهيل ومعالجة بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت والتسعير المستند إلى الولاء وخبرات الشراء المستندة إلى المكافآت. عند مزامنة بيانات حول بطاقات الولاء الخاصة بالعملاء ونقاط المكافآت في Commerce مع Common Data service، فإن التطبيقات المستندة إلى النماذج في Dynamics 365 يمكنها استخدام هذه البيانات. على سبيل المثال، يستطيع مستخدمو Dynamics 365 Customer Service استخدام البيانات لتوفير نفس الخدمات المعقدة من خلال مركز المساعدة.

## <a name="templates"></a>القوالب

| تطبيقات Finance and Operations | التطبيقات المستندة إلى نموذج في Dynamics 365 | ‏‏الوصف |
|-----------------------------|-----------------------------------|-------------|
| بطاقة الولاء                | msdyn\_loyaltycards               | يقوم هذا القالب بمزامنة معلومات بطاقات ولاء العملاء. |
| نقاط مكافآت الولاء       | msdyn\_loyaltyrewardpoints        | يقوم هذا القالب بمزامنة معلومات نقاط مكافآت العملاء. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
