---
title: منهج قاعدة إهلاك نصف السنة
description: يصف هذا الموضوع الأسلوب الذي تستخدمه الأصول الثابتة لحساب الإهلاك باستخدام قاعدة نصف السنة، والذي يحسب سته أشهر من الإهلاك خلال العامين الأول والأخير من وضع الأصل قيد الخدمة.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 6ec4c3a0bd86e15ee015fc2e2c49c92b035243b6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009283"
---
# <a name="half-year-depreciation-convention-methodology"></a>منهج قاعدة إهلاك نصف السنة

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا الموضوع الأسلوب المستخدم في الأصول الثابتة لحساب الإهلاك باستخدام قاعدة نصف السنة. تحسب قاعدة نصف السنة سته أشهر من الإهلاك خلال العامين الأول والأخير من وضع الأصل قيد الخدمة.‬ لمزيد من المعلومات حول قواعد الإهلاك، راجع [أساليب وقواعد الإهلاك](Fixed-asset-depreciation-conventions.md). 

عند استخدام قواعد الإهلاك من سته أشهر، يستخدم النظام سنة الاستحواذ أو سنة وضع الأصل قيد الخدمة، ثم يحسب خمس سنوات من الإهلاك اعتبارًا من ذلك العام، ثم يضيف ستة أشهر. لتوضيح هذه العملية، يمكنك افتراضي أصل تم الاستحواذ عليه بسعر 50,000، وتم وضعه قيد الخدمة في أبريل 2020. ويمكنك أن تفترض أيضًا أن عمر الخدمة لهذا الأصل هو خمس سنوات.

سوف تنتهي سنة الخدمة الأولى في ديسمبر 2020 ، مما يعني أن انتهاء خدمة الأصل من خمس سنوات ستكون في ديسمبر 2024. ستقوم قاعده إهلاك نصف السنة بإضافة ستة أشهر إلى عمر الأصل، مما يعني أن عمر الخدمة سينتهي في يونيو 2025. 

> الإهلاك السنوي 50,000/5 = 10,000 الإهلاك الشهري 10,000/12 = 833.33 <br>
> إهلاك السنة الأولى 10,000/2 = 5,000 والإهلاك الشهري التالي 5,000/9 = 555.56

   [![جدول الإهلاك لقاعدة إهلاك نصف السنة](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

توفر فترات الإهلاك الممتدة التي تضيفها قاعدة النصف سنة توزيعًا أكثر دقة للإهلاك. تمثل قاعدة الستة أشهر مصروفات الإهلاك بطريقة متساوية، الأمر الذي يعتبر مفيدًا لإعداد تقرير كشف الأرباح والخسائر.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]