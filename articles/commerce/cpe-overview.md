---
title: نظرة عامة على بيئة تقييم Dynamics 365 Commerce
description: يقدم هذا الموضوع نظرة عامة على بيئة تقييم Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f225db13fba91ce78287adfda9c6d084dea20af33e62287f517e51cc5a296352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752502"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>نظرة عامة على بيئة تقييم Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على بيئة تقييم Microsoft Dynamics 365 Commerce.

> [!NOTE]
> لا تتوفر بيئات تقييم Commerce بشكل عام، ويتم منحها للشركاء والعملاء على أساس كل طلب. لمزيد من المعلومات، اتصل بجهة اتصال شريك Microsoft.

بيئة تقييم Commerce هي بيئة اختيارية شاملة لـ Dynamics 365 Commerce تتيح للشركاء والعملاء المحتملين تجربة منتج Commerce.

يتم تكوين بيئات التقييم مسبقًا بشكل جزئي لتقليل الخطوات التالية للتوفير المطلوبة.

بصرف النظر عن بعض القيود البسيطة التي لا تؤثر على الميزات أو الوظائف، توفر بيئة تقييم Commerce تجربة Commerce بالكامل، ويمكن للعملاء وشركاء التنفيذ استخدامها لتقييم المنتج وتقديم الملاحظات وإجراء تحليل الملاءمة/الفروق.

## <a name="limitations-of-the-commerce-evaluation-environment"></a>قيود بيئة تقييم Commerce

على الرغم من توفير بيئة تقييم Commerce مجموعة كاملة من ميزات Commerce ووظائفها، إلا أن هناك بعض القيود الثانوية:

- على الرغم من عدم احتواء بيئة تقييم Commerce نفسها على قيود جغرافية، إلا أنه لا ينبغي توفير مكونات البيئة، مثل Retail Cloud Scale Unit (RCSU) وتطبيقات التجارة الإلكترونية، إلا في الولايات المتحدة.
- يوجد حد زمني لاستخدام بيئة تقييم Commerce بقيمة 30 يومًا من تاريخ توفير التجارة الإلكترونية.
- لا يمكن نشر بيئة تقييم Commerce وتهيئتها بنجاح إلا في بيئة تستخدم مخطط العرض التوضيحي، حيث يتم نشر جميع مكونات البيئة في جهاز ظاهري واحد (VM) مُستضاف في سحابة. والقيد الرئيسي للمخطط هو عدد المستخدمين المتزامنين الذين يمكن أن تدعمهم البيئة.

## <a name="get-started"></a>بدء الاستخدام

لتوفير بيئة تقييم Commerce، راجع [توفير بيئة تقييم Commerce](provisioning-guide.md)

## <a name="additional-resources"></a>الموارد الإضافية

[توفير بيئة تقييم Dynamics 365 Commerce](provisioning-guide.md)

[تكوين بيئة تقييم Dynamics 365 Commerce](cpe-post-provisioning.md)

[تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce](cpe-bopis.md)

[تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce](cpe-optional-features.md)

[الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
