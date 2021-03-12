---
title: نظرة عامة على بيئة تقييم Dynamics 365 Commerce
description: يقدم هذا الموضوع نظرة عامة على بيئة تقييم Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000940"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a>نظرة عامة على بيئة تقييم Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على بيئة تقييم Microsoft Dynamics 365 Commerce.

> [!NOTE]
> لا تتوفر بيئات تقييم Commerce بشكل عام، ويتم منحها للشركاء والعملاء على أساس كل طلب. لمزيد من المعلومات، اتصل بجهة اتصال شريك Microsoft.

## <a name="overview"></a>نظرة عامة

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
