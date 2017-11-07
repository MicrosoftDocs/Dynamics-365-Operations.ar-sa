---
title: "نظرة عامة على التسوية البنكية المتقدمة"
description: "تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33150777222faa97af7488c59ab13cb0fb9e8e2c
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

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
    -   قاعدة مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود الحركات البنكية في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition أثناء عملية التسوية. واستنادًا إلى ممارسة العمل الخاصة بك، يمكنك إعداد أكثر من قاعدة مطابقة لتحسين عملية التسوية وإجرائها تلقائيًا.‬

3.  تسوية الكشوف البنكية مع الحركات البنكية في Finance and Operations.
    -   قم بإنشاء دفاتر يومية التسوية ومطابقتها تلقائيًا.
    -   اعرض الكشوف البنكية والحركات البنكية في Finance and Operations جنبًا إلى جنب.
    -   وقم بترحيل الحركات البنكية في Finance and Operations تلقائياً إذا كانت تظهر في كشف بنكي ولكن لا تظهر في Finance and Operations.
    -   إنشاء كشف تسوية.






