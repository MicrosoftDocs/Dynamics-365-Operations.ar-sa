---
title: متطلبات صنف أمر الخدمة‬
description: يوضح هذا المقال متطلبات صنف أمر الخدمة.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 376cda6bbe1800611e6f24c347b9035469a30a14
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015161"
---
# <a name="service-order-item-requirements"></a>متطلبات صنف أمر الخدمة‬

[!include [banner](../includes/banner.md)]

يمكنك إنشاء أمر خدمة لتعقب وإدارة الخدمات التي توفرها للعملاء. إذا كنت تحتاج إلى حجز أصناف محددة لأمر خدمة، يمكنك إنشاء متطلبات صنف مخزون لها. يمكن استهلاك متطلبات صنف مباشرة من المخزون أو يمكن بدء أمر إنتاج للصنف.

باستخدام متطلب صنف بدلا من حركة صنف، يمكنك تخطيط التسليم قبل الاستخدام الفعلي للصنف، وإنشاء أمر شراء، وتضمين الصنف في إطار عمل الاتفاقية التجارية، وتضمين متطلب الصنف في تخطيط الإنتاج.

تتم معالجة متطلبات الصنف لأوامر الخدمة من خلال مشروع. لإنشاء متطلب صنف في أمر خدمة، يجب أن يتم إلحاق أمر الخدمة بمشروع.

حالما يتم إنشاء متطلب صنف لأمر خدمة، يمكن عرضه من **المشروع** في أمر الخدمة الفردي أو من خلال النموذج **أمر المبيعات**.

## <a name="view-an-item-requirement-from-a-service-order"></a>عرض متطلب صنف من أمر الخدمة

1. انتقل إلى **إدارة الخدمة** \> **أوامر الخدمات** \> **أوامر الخدمات**.
1. حدد **إرسال**، ثم حدد **متطلب صنف** لفتح النموذج **متطلبات الأصناف**.
1. حدد علامة التبويب **المشروع**، ثم حدد الحقل **أمر الخدمة** لعرض أوامر الخدمة لمتطلب الصنف.

## <a name="delete-service-orders-with-item-requirements"></a>حذف أوامر الخدمة التي بها متطلبات صنف

إذا تم إنشاء متطلب صنف في أمر الخدمة، فلا يمكنك إلغاء أمر الخدمة. يجب حذف متطلب الصنف لكي يمكنك حذف أمر الخدمة.

1. انتقل إلى **إدارة الخدمة** \> **أوامر الخدمات** \> **أوامر الخدمات**.
1. حدد **إرسال**، ثم حدد **متطلب صنف** لفتح النموذج **متطلبات الأصناف**. يسرد هذا النموذج متطلبات الصنف التي تم إنشاؤها في أمر الخدمة.
1. حدد متطلب الصنف المطلوب حذفه، ثم حدد **حذف**.

–أو –

1. انتقل إلى **إدارة المشاريع والمحاسبة** \> **المشاريع** \> **كافة المشاريع**.
1. قم بفتح المشروع الموجود به أمر الخدمة الذي تم إنشاء متطلب صنف به.
1. في نموذج **المشاريع**، في الجزء الأيسر، حدد **متطلبات الأصناف**. النموذج **متطلبات الأصناف** يسرد متطلبات الصنف التي تم إقرانها بالمشروع الذي تم تحديده.
1. حدد متطلب الصنف المطلوب حذفه، ثم حدد **حذف**.

## <a name="see-also"></a>راجع أيضًا

[متطلبات الصنف (نموذج)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]