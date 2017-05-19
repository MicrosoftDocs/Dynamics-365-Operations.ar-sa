---
title: "نظرة عامة على التسوية البنكية المتقدمة"
description: "تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6977cb3b315a90b504fc6748d2a4d02854a9d5ef
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>نظرة عامة على التسوية البنكية المتقدمة

[!include[banner](../includes/banner.md)]


تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية.

تتيح لك ميزة تسوية البنكية المتقدمة استيراد كشوف الحسابات البنكية. ويمكن بعد ذلك تسوية كشف الحساب البنكي المستورد تلقائياً من داخل الحركات البنكية. فيما يلي الخطوات في تدفق التسوية البنكية المتقدمة.

1.  إعداد استيراد كشف الحساب البنكي.
    -   استيراد كشوف الحسابات البنكية من خلال إطار كيان البيانات.
    -   هناك ثلاثة تنسيقات نموذجية لكشف البنك مضمنة في: ISO20022، وBAI2، وMT940.
    -   يمكن توسيع الوظائف لأي تنسيق.

2.  قم بإعداد تسلسل رقمي لاستخدامه للتسوية البنكية المتقدمة، وحدد قواعد مطابقة التسوية البنكية.
    -   وقاعدة مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود الحركات البنكية في Microsoft Dynamics 365 for Operations أثناء عملية التسوية. واستنادًا إلى ممارسة العمل الخاصة بك، يمكنك إعداد أكثر من قاعدة مطابقة لتحسين عملية التسوية وإجرائها تلقائيًا.‬

3.  تسوية الكشوف البنكية مع الحركات البنكية في Dynamics 365 for Operations.
    -   قم بإنشاء دفاتر يومية التسوية ومطابقتها تلقائيًا.
    -   اعرض الكشوف البنكية والحركات البنكية في Dynamics 365 for Operations جنبًا إلى جنب.
    -   وقم بترحيل الحركات البنكية في Dynamics 365 for Operations تلقائياً إذا كانت تظهر في كشف بنكي ولكن لا تظهر في Dynamics 365 for Operations.
    -   إنشاء كشف تسوية.






