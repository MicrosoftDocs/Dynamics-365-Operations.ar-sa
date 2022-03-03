---
title: يتعذر إنشاء بند حمل عمل بسبب أبعاد المخزون غير الصالحة
description: عند محاولة إصدار أمر مبيعات إرجاع إلى المستودع، قد تتلقى خطأ بشأن أبعاد المخزون غير الصالحة. قم بإزالتها من بند الأمر.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119202"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>يتعذر إنشاء بند حمل عمل لأمر مبيعات الإرجاع بسبب أبعاد مخزون غير صالحة

## <a name="symptoms"></a>العلامات

عند محاولة إصدار أمر مبيعات إرجاع إلى المستودع، قد تستلم رسالة الخطأ التالية:

> لا يمكنك إنشاء بند تحميل لسطر الأمر هذا لأنه يحتوي علي ابعاد مخزون غير صالحه. لا يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد الموقع في التدرج الهرمي للحجز. تتيح أزاله الابعاد غير الصالحة من سطر الأمر.

## <a name="resolution"></a>الحل

لسوء الأسف ، لا يدعم المنتج معالجه التحميل لعمليه إرجاع المبيعات. التالي ، لا يمكن تحرير أمر الشراء المرتجع إلى المستودع.

في حركات أمر المبيعات، يمكنك الاشاره إلى ابعاد المخزون الموجودة أسفل بعد **الموقع** في التدرج الهرمي للحجز. الحل هو أزاله الابعاد غير الصالحة من سطر الأمر.
