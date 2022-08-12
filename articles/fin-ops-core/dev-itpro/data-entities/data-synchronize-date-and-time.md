---
title: مزامنة التاريخ والوقت في مهام الاستيراد
description: استخدم مناطق زمنيه UTC في استيراد المهام لتجنب المشكلات التي تتعلق بتحويلات المنطقة الزمنيه.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8faa7b73349c48d3a02b685546b47c4969c6027
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109421"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>مزامنة التاريخ والوقت في مهام الاستيراد

[!include [banner](../includes/banner.md)]

من المهم تعيين المنطقة الزمنيه لمهمة الاستيراد الخاصة بك إلى التوقيت العالمي المتفق عليه (UTC). قد تري تواريخ وأوقات غير متوقعه في البيانات المستوردة إذا كنت تستخدم اعدادا مختلفا. وبدون الاعداد الصحيح، تقوم عمليه الاستيراد بتحويل تاريخ UTC إلى التنسيق المحلي، ثم تقوم إعدادات النظام بتحويله مره أخرى.

يتسبب هذا التحويل الثنائي علي التسبب في تغيير التواريخ بين التطبيقات. علي سبيل المثال، قد يتسبب التحويل الثنائي في ان يكون تاريخ بدء الموظف مختلفا بين Dynamics 365 Human Resources وDynamics 365 Finance بسبب الاختلافات في المناطق الزمنية المحلية. ويؤدي تعيين مهمة الاستيراد إلى UTC إلى حل هذه المشكلة.

1. في Dynamics 365 Finance and Operations، حدد **إدارة البيانات**.

2. حدد **استيراد** المشاريع، ثم حدد المشروع.

3. ضمن **تنسيق** التاريخ المصدر ، حدد **CSV-Unicode**.

   [![تغيير تنسيق التاريخ المصدر إلى UTC.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. تغيير **المنطقة الزمنيه** إلى **منطقه التوقيت العالمي المتفق عليها**، وتغيير **اللغة** إلى **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

