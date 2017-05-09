---
title: "تسوية دفعة جزئية لعميل لديه خصومات في الإشعارات الدائنة"
description: "ترشدك هذه المقالة من خلال سيناريو حيث تم أخذ خصم نقدي على إشعار دائن عندما تضمنت الفاتورة الأصلية أيضًا خصمًا نقديًا."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: e43bcea67d9c408c93258f9b64565560b59fbb88
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>تسوية دفعة جزئية لعميل لديه خصومات في الإشعارات الدائنة

[!include[banner](../includes/banner.md)]


ترشدك هذه المقالة من خلال سيناريو حيث تم أخذ خصم نقدي على إشعار دائن عندما تضمنت الفاتورة الأصلية أيضًا خصمًا نقديًا. 

تسمح شركة الاتحاد للتصنيع للعملاء بأخذ الخصومات النقدية على مدفوعات جزئية وأيضًا على الإشعارات الدائنة (مذكرات الائتمان). ويمكن الحصول على خصم نقدي على إشعار دائن عندما يتم إصدار إشعار دائن لفاتورة يحصل فيها العميل على خصم نقدي. وبدلاً من توفير ائتمان للمبلغ بالكامل، يمكن ائتمان رصيد العميل لمبلغ يستبعد نسبة الخصم النقدي التي يحصل عليها العميل. وتوجد معلمات التسوية في صفحة **معلمات الحسابات المدينة**.

## <a name="invoice-and-credit-note"></a>الفاتورة والإشعار الدائن
لدى العميل 4035 فاتورة بمبلغ 1,000.00 وإشعار دائن بمبلغ 100.00. ويحتوي كل مستند على خصم بنسبة 1 في المائة إذا كان الدفع في غضون 14 يومًا. يستطيع جمال عرض هذه المعلومات في صفحة **حركات العميل**.

| الإيصال    | نوع الحركة | التاريخ      | الفاتورة  | المبلغ في خصم بعملة الحركة | المبلغ في الائتمان بعملة الحركة | الرصيد  | عملة |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | الفاتورة          | 6/28/2015 | 10050    | 1,000.00                             |                                       | 1,000.00 | دولار أمريكي      |
| CCRN-10050 | الإشعار الدائن      | 6/28/2015 | CR-10050 |                                      | 100.00                                | 100.00-  | دولار أمريكي      |

## <a name="settle-a-credit-note-with-an-invoice"></a>تسوية إشعار دائن مع فاتورة
من صفحة **حركات العميل**، يفتح جمال صفحة **تسوية الحركات**. ويمكنه استخدام صفحة **تسوية الحركات** لتسوية الفاتورة والإشعار الدائن. وكجزء من عملية التسوية، يشاهد تواريخ ومبالغ الخصم النقدي. ويقوم بتمييز هاتين الوثيقتين، ثم النقر فوق **ترحيل** لتسوية الحركات. يوجد خصم بمبلغ -1.00 على إشعار دائن، لأن شركة الاتحاد للتصنيع تسمح بالخصومات على الإشعارات الدائنة.

| وضع علامة     | استخدام الخصم النقدي | الإيصال    | الحساب | التاريخ      | تاريخ الاستحقاق  | الفاتورة  | المبلغ بعملة الحركة | عملة | المبلغ المراد تسويته |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| محدَد | عادي            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1,000.00                       | دولار أمريكي      | 990.00           |
| محدَد | عادي            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | 100.00-                        | دولار أمريكي      | -99.00           |

تظهر معلومات الخصم أسفل صفحة **تسوية الحركات**.

|                              |           |
|------------------------------|-----------|
| تاريخ الخصم النقدي           | 7/12/2015 |
| مبلغ الخصم النقدي         | -1.00     |
| استخدام الخصم النقدي            | عادي    |
| الخصم النقدي المستقطع          | 0.00      |
| مبلغ الخصم النقدي المطلوب استقطاعه | -1.00     |

التسوية ستكون 100.00، وسوف تشمل دفعة بمبلغ 99.00 وخصمًا بمبلغ 1.00.



