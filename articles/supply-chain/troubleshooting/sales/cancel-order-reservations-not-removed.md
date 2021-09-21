---
title: لا يمكن إزالة عمليات الحجز عند إلغاء أمر
description: لا يمكنك إلغاء أمر المبيعات حتى يتم إلغاء العمل المقترن بهذا الأمر وعكسه. للقيام بذلك، اتبع الخطوات الثلاثة هذه.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475483"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>لا يمكن إزالة عمليات الحجز عند إلغاء أمر

## <a name="symptoms"></a>العلامات

إذا كان العمل مقترناً بأمر مبيعات وحاولت إلغاء ذلك الأمر، ستظهر لك رسالة الخطأ التالية:

> لا يمكن إزالة الحجوزات نظرًا لوجود عمل منشأ يعتمد على الحجوزات.

لا يمكنك إلغاء أمر المبيعات حتى يتم إلغاء العمل وعكسه. ينطبق هذا المتطلب حتى لون كان العمل المرتبط  بأمر  المبيعات مغلقا.

## <a name="resolution"></a>الحل

لإصلاح هذه المشكلة، اتبع هذه الخطوات:

1. قم بإلغاء العمل وضع المخزون مرة أخرى في الموقع المطلوب. انتقل إلى حمل العمل ذي الصلة لأمر المبيعات، وحدد **تقليل الكمية المنتقاة‬‏‫** على بند حمل العمل أو **إلغاء العمل** على جزء الإجراءات.

    أصبحت حالة العمل الآن *مُلغى*، ويتم إنشاء ومعالجة حركة المخزون الجديدة بشكل تلقائي لإعادة وضع المخزون في الموقع الذي ورد وصفه عند الإلغاء.

2. احذف حمل العمل. يتم أيضًا حذف الشحنة.

3. ينبغي الآن أن تكون قادرًا على الانتقال إلى أمر المبيعات وإلغائه.
