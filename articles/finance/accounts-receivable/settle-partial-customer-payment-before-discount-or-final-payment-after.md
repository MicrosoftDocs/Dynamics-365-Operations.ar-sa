---
title: تسوية دفع جزئي لعميل قبل تاريخ الخصم بدفعة نهائية بعد تاريخ الخصم
description: تتناول هذه المقالة تأثير تسوية مدفوعات الفواتير للعملاء. يركز السيناريو على التأثيرات في دفتر الأستاذ الفرعي، وليس دفتر الأستاذ العام.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a71d0931445f3501f1b74f26c5eef583ab598b3c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188891"
---
# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>تسوية دفع جزئي لعميل قبل تاريخ الخصم بدفعة نهائية بعد تاريخ الخصم

[!include [banner](../includes/banner.md)]

تتناول هذه المقالة تأثير تسوية مدفوعات الفواتير للعملاء. يركز السيناريو على التأثيرات في دفتر الأستاذ الفرعي، وليس دفتر الأستاذ العام.

‏‫شركة الاتحاد للتصنيع تبيع السلع للعميل 4027. تقدم هذه الشركة خصمًا نقديًا بنسبة 1 في المائة، إذا تم دفع الفاتورة في غضون 14 يومًا.‬ ويجب دفع الفواتير في غضون 30 يومًا. كما تقدم شركة الاتحاد للتصنيع الخصومات النقدية في دفعات جزئية. وتوجد معلمات التسوية في صفحة **معلمات الحسابات المدينة**.

## <a name="invoice"></a>الفاتورة
في 25 حزيران/يونيو، يقوم جمال بإدخال وترحيل فاتورة بمبلغ 1,000.00 للعميل 4027. ويستطيع جمال عرض هذه الفاتورة من خلال استخدام الزر **الحركات** في صفحة **العملاء**.

| الإيصال   | نوع الحركة | التاريخ      | الفاتورة | المبلغ في خصم بعملة الحركة | المبلغ في الائتمان بعملة الحركة | الرصيد  | عملة |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | الفاتورة          | 6/25/2015 | 10020   | 1,000.00                             |                                       | 1,000.00 | دولار أمريكي      |

## <a name="partial-payment-before-the-cash-discount-date"></a>الدفعة الجزئية قبل تاريخ الخصم النقدي
في 2 تموز/يوليو، قام العميل 4027 بسداد دفعة جزئية بمبلغ 297.00 للفاتورة. الدفعة مؤهلة للحصول على خصم نقدي، لأن شركة الاتحاد للتصنيع تقدم خصومات نقدية على مدفوعات جزئية، ويتم إجراء الدفع الجزئي قبل تاريخ الخصم النقدي. ولذلك، يحصل العميل 4027 على خصم نقدي بمبلغ 3.00. ويسجل جمال الدفعة للعميل 4027 باستخدام دفتر يومية المدفوعات. ويقوم جمال فيما بعد بفتح صفحة **تسوية الحركات** حتى تتمكن من تمييز الفاتورة للتسوية.

| وضع علامة     | استخدام الخصم النقدي | الإيصال   | الحساب | التاريخ      | تاريخ الاستحقاق  | الفاتورة | المبلغ في خصم بعملة الحركة | عملة | المبلغ المراد تسويته |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| محدَد | عادي            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 1,000.00                             | دولار أمريكي      | 297.00           |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**. إذا لم تقم بتغيير قيمة **المبلغ المُراد تسويته** إلى **297.00**، فستختلف قيم مبلغ الخصم النقدي الذي يظهر. وعلى الرغم من ذلك، سيتم الحصول على مبلغ 3.00 عند ترحيل الدفعة، لأن التسوية تقوم تلقائياً بتعديل قيمة **المبلغ المُراد تسويته **بالنسبة لك.

|                              |           |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | 7/09/2015 |
| مبلغ الخصم النقدي         | 10.00     |
| استخدام الخصم النقدي            | عادي    |
| الخصم النقدي المستقطع          | 0.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | 3.00      |

يقوم جمال بترحيل هذه الدفعة. وتشتمل الفاتورة الآن على رصيد 700.00. يمكن للعميل رؤية الحركات التالية.

| الإيصال    | نوع الحركة | التاريخ      | الفاتورة | المبلغ في خصم بعملة الحركة | المبلغ في الائتمان بعملة الحركة | الرصيد | عملة |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | الفاتورة          | 6/25/2015 | 10020   | 1,000.00                             |                                       | 700.00  | دولار أمريكي      |
| ARP-10020  |  الدفع         | 7/1/2015  |         |                                      | 297.00                                | 0.00    | دولار أمريكي      |
| DISC-10020 |  الخصم النقدي   | 7/1/2015  |         |                                      | 3.00                                  | 0.00    | دولار أمريكي      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>الدفعة المتبقية بعد تاريخ الخصم النقدي
في 11 يوليو، الذي يكون بعد فترة الخصم، يدفع العميل 4027 بقية هذه الفاتورة. وفي صفحة **تسوية الحركات**، لا يتم عرض أي مبلغ خصم في حقل **الخصم النقدي المقدر**، والقيمة في حقل **مبلغ الخصم النقدي** هي **0.00**. وعندما يدفع العميل 4027 مبلغ 700.00 المتبقي، لا يتم الحصول على أي خصم إضافي.

| وضع علامة     | استخدام الخصم النقدي | الإيصال   | الحساب | التاريخ      | تاريخ الاستحقاق  | الفاتورة | المبلغ في خصم بعملة الحركة | عملة | المبلغ المراد تسويته |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| محدَد | عادي            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 700.00                               | دولار أمريكي      | 700.00           |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**.

|                              |           |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | 7/09/2015 |
| مبلغ الخصم النقدي         | 0.00      |
| استخدام الخصم النقدي            | عادي    |
| الخصم النقدي المستقطع          | 3.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | 0.00      |

إذا قام جمال بتغيير القيمة في حقل **استخدام الخصم النقدي** إلى **دوماً**، يتم تجاوز إعداد **حساب الخصومات النقدية للمدفوعات الجزئية**، ويتم الحصول على الخصم النقدي. ويتغير مبلغ الدفعة إلى 693.00، ويساوي الخصم النقدي مبلغ 7.00 المتبقي.

| وضع علامة     | استخدام الخصم النقدي | الإيصال   | الحساب | التاريخ      | تاريخ الاستحقاق  | الفاتورة | المبلغ في خصم بعملة الحركة | المبلغ في الائتمان بعملة الحركة | عملة | المبلغ المراد تسويته |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| محدَد | دائمًا            | FTI-10020 | 4027    | 6/25/2015 | 7/25/2015 | 10020   | 700.00                               |                                       | دولار أمريكي      | 693.00           |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**.

|                              |           |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | 7/09/2015 |
| مبلغ الخصم النقدي         | 7.00      |
| استخدام الخصم النقدي            | دائمًا    |
| الخصم النقدي المستقطع          | 3.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | 7.00      |

يقوم جمال بتغيير القيمة في حقل **استخدام الخصم النقدي** مرة أخرى إلى **عادي**، لأنه لا يترك هذا العميل يحصل على الخصم النقدي المتبقي بمبلغ 7.00. ثم يقوم جمال بترحيل الدفعة. وعندما يفتح جمال صفحة **حركات العميل**، ترى أن الفاتورة بها رصيد 0.00. كما يرى أن هناك دفعتان. الدفعة المفتوحة بمبلغ 297.00 وبها خصم نقدي بمبلغ 3.00، والدفعة الأخرى بمبلغ 700.00.

| الإيصال    | نوع الحركة | التاريخ      | الفاتورة | المبلغ في خصم بعملة الحركة | المبلغ في الائتمان بعملة الحركة | الرصيد | عملة |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | الفاتورة          | 6/25/2015 | 10020   | 1,000.00                             |                                       | 0.00    | دولار أمريكي      |
| ARP-10020  |                  | 7/1/2015  |         |                                      | 297.00                                | 0.00    | دولار أمريكي      |
| DISC-10020 |                  | 7/1/2015  |         |                                      | 3.00                                  | 0.00    | دولار أمريكي      |
| ARP-10021  |                  | 7/11/2015 |         |                                      | 700.00                                | 0.00    | دولار أمريكي      |




