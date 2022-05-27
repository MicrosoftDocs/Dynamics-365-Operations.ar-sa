---
title: لم يتم إنشاء الإيصال
description: يوفر هذا الموضوع معلومات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعد عندما يجب إنشاء قسيمة ولكن لا.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eb45b79fa710699cfa267e7c6359ba3ce761d62d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693216"
---
# <a name="voucher-isnt-generated"></a>لم يتم إنشاء الإيصال

[!include [banner](../includes/banner.md)]

إذا كان يجب إنشاء إيصال، لا تعرض صفحة **حركات الإيصالات** أي إيصالات، اتبع الخطوات الواردة في الأقسام التالية كما هو مطلوب لاستكشاف هذه المشكلة وإصلاحها.

[![صفحة حركات الإيصال التي لا تحتوي على قسائم.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>فحص إمكانية تطبيق الضرائب

1. انتقل إلى **الضريبة** \> **المهام الدورية** \> **لم يتم نقل إدخالات دفتر يومية الأستاذ الفرعي**.
2. إذا كان هناك سجل دفتر يومية، فحدده، ثم حدد **نقل الآن**.

    [![زر التحويل الآن في صفحة إدخالات دفتر يومية الأستاذ الفرعي التي لم يتم نقلها بعد.](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. افتح صفحة **حركات الإيصالات** مرة أخرى لمعرفة ما إذا كان قد تم إنشاء الإيصال أو لا.

## <a name="determine-whether-customization-exists"></a>حدد ما إذا كان التخصيص موجودًا

إذا كنت قد أكملت الخطوات الواردة في القسم السابق ولكنك لم تجد أي مشكلة، فحدد ما إذا كان التخصيص موجودًا أم لا. في حاله عدم وجود تخصيص، قم بإنشاء طلب خدمه Microsoft لمزيد من الدعم.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
