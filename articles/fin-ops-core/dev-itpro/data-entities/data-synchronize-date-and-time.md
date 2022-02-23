---
title: مزامنة التاريخ والوقت في مهام الاستيراد
description: استخدم مناطق زمنيه UTC في استيراد المهام لتجنب المشكلات التي تتعلق بتحويلات المنطقة الزمنيه.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798709"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>مزامنة التاريخ والوقت في مهام الاستيراد

[!include [banner](../includes/banner.md)]

من المهم تعيين المنطقة الزمنيه لمهمة الاستيراد الخاصة بك إلى التوقيت العالمي المتفق عليه (UTC). قد تري تواريخ وأوقات غير متوقعه في البيانات المستوردة إذا كنت تستخدم اعدادا مختلفا. وبدون الاعداد الصحيح، تقوم عمليه الاستيراد بتحويل تاريخ UTC إلى التنسيق المحلي، ثم تقوم إعدادات النظام بتحويله مره أخرى.

يتسبب هذا التحويل الثنائي علي التسبب في تغيير التواريخ بين التطبيقات. علي سبيل المثال، قد يتسبب التحويل الثنائي في ان يكون تاريخ بدء الموظف مختلفا بين Dynamics 365 Human Resources وDynamics 365 Finance بسبب الاختلافات في المناطق الزمنيه المحلية. ويؤدي تعيين مهمة الاستيراد إلى UTC إلى حل هذه المشكلة.

1. في Dynamics 365 Finance and Operations، حدد **أداره البيانات**.

2. حدد **استيراد** المشاريع، ثم حدد المشروع.

3. ضمن **تنسيق** التاريخ المصدر ، حدد **CSV-Unicode**.

   [![تغيير تنسيق التاريخ المصدر إلى UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. تغيير **المنطقة الزمنيه** إلى **منطقه التوقيت العالمي المتفق عليها**، وتغيير **اللغة** إلى **En-US**.


