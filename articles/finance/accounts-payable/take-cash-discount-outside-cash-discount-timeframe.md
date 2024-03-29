---
title: الحصول على خصم نقدي خارج فترة الخصم النقدي
description: توفر هذه المقالة سيناريوهين يظهران كيف يمكن أخذ خصم نقدي حتى لو تم إجراء الدفع خارج فترة الخصم النقدي.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26b1eb5e542acf7496d1a0cf7196716a5de75e4e
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780432"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>الحصول على خصم نقدي خارج فترة الخصم النقدي

[!include [banner](../includes/banner.md)]

توفر هذه المقالة سيناريوهين يظهران كيف يمكن أخذ خصم نقدي حتى لو تم إجراء الدفع خارج فترة الخصم النقدي.

في 28 حزيران/يونيو، تقوم فوزية بإنشاء فاتورة بمبلغ 2,000.00 للمورد 3052. وتشمل الفاتورة خصمًا نقديًا قدره 1 في المائة، إذا تم دفع الفاتورة في غضون 14 يومًا.‬

## <a name="use-cash-discount-option--always"></a>استخدم خيار الخصم النقدي = دوماً
تقوم فوزية بإنشاء دفعة في الأول من يوليو، بعد تاريخ الخصم. وتقوم فوزية بفتح صفحة **تسوية الحركات** لعرض الحركات التي يمكن تسويتها. 

وتقوم فوزية بتمييز فاتورة الدفع. لم يتم الحصول على أي خصم نقدي، لأن الدفع بعد تاريخ الخصم. ‏‫ومع ذلك، أعطى المورد فوزية موافقة لإدخال الخصم النقدي على أية حال. ولذلك، تقوم فوزية بتغيير القيمة في حقل **استخدام الخصم النقدي** إلى **دوماً**.

| وضع علامة     | استخدام الخصم النقدي | الإيصال   | الحساب | تاريخ الخصم النقدي | تاريخ الاستحقاق  | الفاتورة | المبلغ بعملة الحركة | عملة | المبلغ المراد تسويته |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| محدد | دائمًا            | Inv-10030 | 3052    | بتاريخ 6/28/2020          | بتاريخ 7/12/2020 | 10030   | -2,000.00                      | دولار أمريكي      | -1,980.00        |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات**.

| الحقل                        | قيمة     |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | بتاريخ 7/12/2020 |
| مبلغ الخصم النقدي         | -20.00    |
| استخدام الخصم النقدي            | دائمًا    |
| الخصم النقدي المستقطع          | 0.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | -20.00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>التاريخ المستخدم لحساب الخصومات = التاريخ المحدد
إذا تم ترحيل الفاتورة والدفع على حد سواء، فإنه لا يزال يمكن الحصول على الخصم النقدي عند تسوية الحركات في صفحة **تسوية الحركات**. وتقوم فوزية بتغيير القيمة في حقل **التاريخ المطلوب استخدامه لحساب الخصومات** إلى **التاريخ المحدد**. وتقوم فيما بعد بإدخال تاريخ 28 يونيو، في فترة الخصم النقدي للفاتورة. ويتم استخدام هذا التاريخ لحساب خصم نقدي للحركة. وفي صفحة **تسوية الحركات المفتوحة** تشاهد فوزية الخصم الكامل بمبلغ 20.00 يظهر بشكل افتراضي، يعرض بند الفاتورة المبلغ المراد تسويته بمبلغ 1,980.00.

| وضع علامة          | استخدام الخصم النقدي | الإيصال   | الحساب | تاريخ الخصم النقدي | تاريخ الاستحقاق  | الفاتورة | المبلغ بعملة الحركة | عملة | المبلغ المراد تسويته |
|--------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| المحددة والمميزة | عادي    | Inv-10030 | 3052    | بتاريخ 6/28/2020         | بتاريخ 7/12/2020 | 10030   | -2,000.00                      | دولار أمريكي      | -1,980.00        |
| محدد                 | عادي    | APP-10030 | 3052    | بتاريخ 15/7/2020          | بتاريخ 15/7/2020 |         | 500.00                         | دولار أمريكي      | 500.00           |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**. مبلغ الخصم الذي يتم الحصول عليه هو 20.00، لأن مبلغ المراد تسويته للفاتورة هو المبلغ الافتراضي 1,980.00.

| الحقل                        | قيمة     |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | بتاريخ 7/12/2020 |
| مبلغ الخصم النقدي         | -20.00    |
| استخدام الخصم النقدي            | عادي    |
| الخصم النقدي المستقطع          | 0.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | -20.00    |

تقوم فوزية بتحديث القيمة في حقل **المبلغ المُراد تسويته** إلى **500.00**. ويتم حساب القيمة في حقل **مبلغ الخصم النقدي المراد الحصول عليه** بمبلغ **5.05**.

| وضع علامة                     | استخدام الخصم النقدي | الإيصال   | الحساب | التاريخ      | تاريخ الاستحقاق  | الفاتورة | المبلغ بعملة الحركة | عملة | المبلغ المراد تسويته |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| المحددة والمميزة | عادي            | Inv-10030 | 3052    | بتاريخ 6/28/2020 | بتاريخ 7/12/2020 | 10030   | 2,000.00                       | دولار أمريكي      | -500.00          |
| محدد                 | عادي            | APP-10030 | 3052    | بتاريخ 15/7/2020 | بتاريخ 15/7/2020 |         | 500.00                         | دولار أمريكي      | 500.00           |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات المفتوحة**. والقيمة في حقل **مبلغ الخصم النقدي المراد الحصول عليه** هو **5.05**، لأن المبلغ المراد تسويته للفاتورة تم تغييره إلى مبلغ الدفع 500.00.

| الحقل                        | قيمة     |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | بتاريخ 7/12/2020 |
| مبلغ الخصم النقدي         | -20.00    |
| استخدام الخصم النقدي            | عادي    |
| الخصم النقدي المستقطع          | 0.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | -5.05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
