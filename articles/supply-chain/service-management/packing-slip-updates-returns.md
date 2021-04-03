---
title: تحديثات كشف التعبئة للمرتجعات
description: قبل استلام الأصناف المرتجعة في المخزون، يجب تحديث كشف التعبئة الخاص بالأمر الذي تنتمي إليه هذا الأصناف.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87dfad2247c84f8e85074739cfff4a2d1b9f8567
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259687"
---
# <a name="packing-slip-updates-for-returns"></a>تحديثات كشف التعبئة للمرتجعات  

[!include [banner](../includes/banner.md)]


قبل استلام الأصناف المرتجعة في المخزون، يجب تحديث كشف التعبئة الخاص بالأمر الذي تنتمي إليه هذا الأصناف. ويشبه التحديث إلى الحركة المالية عملية تحديث الفاتورة، وتعد عملية تحديث كشف التعبئة التحديث المادي لسجل المخزون؛ ما يعني أنه يحول التكاليف إلى المخزون. عندما يتعلق الأمر بالمرتجعات، يتم تنفيذ الخطوات التي تم تعيينها لإجراء الإرجاع أثناء تحديث إيصال التعبئة.

يمكن معالجة تحديث كشف التعبئة في دفتر يومية وصول الصنف أو في أمر الإرجاع.

وفي إطار عملية ترحيل كشف التعبئة، يمكن ربط رقم مرجع كشف التعبئة من مستندات الشحن الخاصة بالعميل مع بنود الأمر. يعتبر هذا الاقتران اختياريًا وكمرجع فقط. ولا ينشئ أية تحديثات خاصة بالحركات‬.

إذا لم تصل كافة الأصناف المرتجعة المتوقعة، فيجب عليك تضمين الكمية التي تم استلامها في تحديث كشف التعبئة فقط. ودع الأصناف المتبقية على الأمر حتى تصل باقي شحنة المرتجعات.

إذا تم إرسال صنف مرة أخرى من الفحص إلى قسم الشحن والاستلام، كما يكون الأمر عندما لا يعلم المفتش أين يقوم بتخزين الصنف في المخزون، عندئذٍ يجب تحديث كشف التعبئة المقابل وذلك للتسجيل الصحيح والعمل على كود الترتيب الذي يتم تحديده كنتيجة للفحص.

عندما تقوم بتحديث كشف تعبئة لصنف مرتجع من اتفاقية مبيعات، يتم تحديث التزام اتفاقية المبيعات لهذا الصنف تلقائياً ليعكس التغيير في الكمية أو المبلغ. 

## <a name="see-also"></a>راجع أيضًا

[إجراء تحديثات الفاتورة للمرتجعات](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]