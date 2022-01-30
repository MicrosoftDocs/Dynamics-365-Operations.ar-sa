---
title: إضافة أنواع مبالغ الدفعات
description: يشرح هذا الموضوع كيفية إعداد أنواع مبالغ الدفعات في تأجير الأصول.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 037afa458277a3a07bcb937c6ec4d961d0dd5ca9
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968314"
---
# <a name="add-payment-amount-types"></a>إضافة أنواع مبالغ الدفعات

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع كيفية إعداد أنواع مبالغ الدفعات في تأجير الأصول. وبهذه الطريقة، يمكنك تفصيل مبلغ دفعات الإيجار بدلاً من إضافة المبلغ الإجمالي في بنود جدول الدفع.

لإضافة أنواع مبالغ الدفعات، اتبع الخطوات التالية.

1. انتقل إلى **تأجير الأصول \> الإعداد \> أنواع مبالغ الدفعات**.
2. حدد **جديد**.
3. أدخل نوع الدفعة الجديد ووصفًا له.

> [!NOTE]
> بالنسبة لإعادة تقييم مؤشر IFRS 16، يجب عليك إنشاء نوع مبلغ دفعة واحد ووضع علامة عليه على أنه **مستخدم لإعادة تقييم مؤشر IFRS 16**. سيتم استخدام نوع مبلغ الدفعة هذا عند تشغيل عملية إعادة تقييم المؤشر مقابل دفتر IFRS 16، كما سيراعي التغييرات التي حدثت بسبب عملية إعادة تقييم المؤشر.
>
> عند تعيين الخيار **تصنيف الدفع** إلى **نعم**، إذا تم تشغيل إعادة تقييم المؤشر للمعيار IFRS 16، ولكن لا يوجد نوع دفعة للمعيار IFRS 16، فلن تكتمل العملية.

يمكن تمييز سجل واحد فقط على أنه **مستخدم لإعادة تقييم مؤشر IFRS16‬**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
