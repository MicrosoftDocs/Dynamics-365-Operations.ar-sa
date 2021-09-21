---
title: لا تعكس أوامر الشراء إعدادات اللغة الخاصة بالكيان القانوني
description: يظهر اسم المنتج في أمر الشراء بلغة النظام بدلاً من اللغة التي تم تعيينها للكيان القانوني حيث تم إنشاء أمر الشراء
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475461"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>لا تعكس أوامر الشراء إعدادات اللغة الخاصة بالكيان القانوني


## <a name="symptoms"></a>العلامات

يظهر اسم المنتج في أمر الشراء بلغة النظام بدلاً من اللغة التي تم تعيينها للكيان القانوني حيث تم إنشاء أمر الشراء.

## <a name="reproduce-the-issue"></a>إعادة إنتاج المشكلة

يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.

1. قم بتعيين لغة النظام إلى *EN-US* (US English).
1. تأكد من وجود منتج حيث تتم المحافظة على اللغتين *EN-US* و *DE* (German) للترجمات واسم المنتج.
1. قم بتغيير لغة الكيان القانوني إلى *DE*.
1. في الكيان القانوني حيث تم تعيين *DE‎* كلغة، أنشئ أمر شراء يتضمن المنتج.
1. لاحظ استمرار ظهور اسم المنتج باللغة US English (لغة النظام).

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. على أوامر الشراء، يظهر المنتج دائمًا بلغة النظام. يتم استخدام لغة أمر الشراء عند إنشاء دفتر يومية التأكيد.
