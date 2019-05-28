---
title: نظرة عامة على التسوية البنكية المتقدمة
description: تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c6cec76ebc8328f221ecb6c30ae93716bd9bfe9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546491"
---
# <a name="advanced-bank-reconciliation-overview"></a>نظرة عامة على التسوية البنكية المتقدمة

[!include [banner](../includes/banner.md)]

تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية.

تتيح لك ميزة تسوية البنكية المتقدمة استيراد كشوف الحسابات البنكية. ويمكن بعد ذلك تسوية كشف الحساب البنكي المستورد تلقائياً من داخل الحركات البنكية. فيما يلي الخطوات في تدفق التسوية البنكية المتقدمة.

1.  إعداد استيراد كشف الحساب البنكي.
    -   استيراد كشوف الحسابات البنكية من خلال إطار كيان البيانات.
    -   هناك ثلاثة تنسيقات نموذجية لكشف البنك مضمنة في: ISO20022، وBAI2، وMT940.
    -   يمكن توسيع الوظائف لأي تنسيق.

2.  قم بإعداد تسلسل رقمي لاستخدامه للتسوية البنكية المتقدمة، وحدد قواعد مطابقة التسوية البنكية.
    -   قاعدة مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود الحركة البنكية في Microsoft Dynamics 365 for Finance and Operations أثناء عملية التسوية. واستنادًا إلى ممارسة العمل الخاصة بك، يمكنك إعداد أكثر من قاعدة مطابقة لتحسين عملية التسوية وإجرائها تلقائيًا.‬

3.  تسوية الكشوف البنكية مع الحركات البنكية في Finance and Operations.
    -   قم بإنشاء دفاتر يومية التسوية ومطابقتها تلقائيًا.
    -   اعرض الكشوف البنكية والحركات البنكية في Finance and Operations جنبًا إلى جنب.
    -   وقم بترحيل الحركات البنكية في Finance and Operations تلقائياً إذا كانت تظهر في كشف بنكي ولكن لا تظهر في Finance and Operations.
    -   إنشاء كشف تسوية.





