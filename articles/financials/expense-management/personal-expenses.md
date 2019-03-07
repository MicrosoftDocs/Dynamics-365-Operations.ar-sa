---
title: النفقات الشخصية على تقرير نفقات
description: يشرح هذا الموضوع الأسلوبين المستخدمين لمعالجة المصروفات الشخصية للعامل في Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6b6c505e7dc5e6544658b00d9f59e6062353608
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "344882"
---
# <a name="personal-expenses-on-an-expense-report"></a>المصروفات الشخصية على تقرير المصروفات

[!include [banner](../includes/banner.md)]

أثناء السفر من أجل العمل، قد يقوم العامل أحيانًا باستخدام بطاقة الائتمان الخاصة بالشركة لسداد مصروفاته الشخصية. إذا لم تقم بتحديد آلية لمعالجة المصروفات الشخصية، فقد تتعطل عملية الموافقة على تقارير المصروفات عندما يُرسل العمال تقارير مصروفاتهم المفصلة. 

هناك أسلوبان لمعالجة المصروفات الشخصية للعامل في Microsoft Dynamics 365 for Finance and Operations.

- **مدفوع بواسطة الموظف** - لا تدفع مؤسستك مصروفاتك الشخصية التي تظهر على الفاتورة الخاصة ببطاقة ائتمان الشركة. بدلًا من ذلك، يقوم الموظف بإنشاء تقرير يعرض المصروفات الشخصية جنبًا إلى جنب مع مصروفات الشركة التي تم تحميلها على بطاقة ائتمان الشركة.
- **مدفوع بواسطة الشركة** - تدفع مؤسستك الفاتورة كاملة من خلال بطاقة ائتمان الشركة، ثم تقوم بخصم المصروفات الشخصية من حساب العامل.

يمكنك تحديد الطريقة التي تستخدمها مؤسستك على صفحة **محددات إدارة المصروفات**.
