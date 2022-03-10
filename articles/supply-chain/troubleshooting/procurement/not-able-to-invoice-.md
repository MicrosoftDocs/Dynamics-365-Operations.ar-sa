---
title: لا يمكن فوترة أمر مبيعات مخصص للعملاء
description: لم يعد بإمكانك فوترة أمر المبيعات الأصلي وأمر الشراء للتسليم المباشر الأصلي بعد تمكين الخيار ترحيل الفاتورة تلقائيًا.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756741"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>لا يمكن فوترة أمر مبيعات مخصص للعملاء

رقم KB: 4611793

## <a name="symptoms"></a>العلامات

لم يعد بإمكانك فوترة أمر المبيعات الأصلي وأمر الشراء للتسليم المباشر الأصلي بعد تمكين الخيار **ترحيل الفاتورة تلقائيًا** على الصفحة **بين شركات شقيقة** لمورد.

## <a name="resolution"></a>الدقة

يتم التحكم في سلوك المزامنة الخاص بفواتير أمر التسليم بين الشركات الشقيقة والتسليم المباشر وفرضه بواسطة المعلمات الموضحة في [إعداد المحددات لترحيل أمر بين الشركات الشقيقة](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

بعد تعيين تلك المعلمات، يجب أن تقوم بفوترة أمر مبيعات بين الشركات الشقيقة أولاً. سيتم بعد ذلك مزامنة أوامر المبيعات وأوامر الشراء الأصلية.
