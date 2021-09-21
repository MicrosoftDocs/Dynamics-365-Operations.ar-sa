---
title: يتعذر إنشاء بند حمل عمل بسبب أبعاد المخزون غير الصالحة
description: عند محاولة إصدار أمر مبيعات إرجاع إلى المستودع، قد تتلقى خطأ بشأن أبعاد المخزون غير الصالحة. قم بإزالتها من بند الأمر.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475488"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>يتعذر إنشاء بند حمل عمل لأمر مبيعات الإرجاع بسبب أبعاد مخزون غير صالحة

## <a name="symptoms"></a>العلامات

عند محاولة إصدار أمر مبيعات إرجاع إلى المستودع، قد تستلم رسالة الخطأ التالية:

> لا يمكنك إنشاء بند تحميل لسطر الأمر هذا لأنه يحتوي علي ابعاد مخزون غير صالحه. لا يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد الموقع في التدرج الهرمي للحجز. تتيح أزاله الابعاد غير الصالحة من سطر الأمر.

## <a name="resolution"></a>الحل

لسوء الأسف ، لا يدعم المنتج معالجه التحميل لعمليه إرجاع المبيعات. التالي ، لا يمكن تحرير أمر الشراء المرتجع إلى المستودع.

في حركات أمر المبيعات، يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد **الموقع** في التدرج الهرمي للحجز. الحل هو أزاله الابعاد غير الصالحة من سطر الأمر.
