---
title: إلغاء باقي التسليم نقل أمر الشراء إلى حالة مؤكدة
description: إذا تم إلغاء كمية متبقية من التسليم على أمر شراء تم فيه تشغيل إدارة التغييرات، ينتقل أمر الشراء إلى الحالة "مؤكد"
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475484"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>إلغاء باقي التسليم نقل أمر الشراء إلى حالة مؤكدة

## <a name="symptoms"></a>العلامات

بالنسبة لأمر شراء يخضع لإدارة التغييرات، إذا كان التغيير الوحيد المطلوب إلغاء كمية متبقية من التسليم على بند أو أكثر، فسينتقل أمر الشراء بشكل مباشر إلى الحالة *مؤكد* عندما يكون موافقًا عليه، ولن يتم إنشاء دفتر يومية.

## <a name="resolution"></a>الحل

لا يؤثر إلغاء الكمية المتبقية من التسليم على محتويات دفتر يومية التأكيد. يجب استخدام هذه الوظيفة عند استلام البند بشكل جزئي، ويجب إلغاء جودة الكمية المتبقية في خطوة المعالجة بعد تأكيد أمر الشراء مع المورّد.

إذا كان يجب أني ينعكس ذلك على تأكيد أمر الشراء، فيجب تعديل الكمية في بند أمر الشراء حتى يكون التأكيد مطلوبًا. بدلاً من ذلك، إذا لم يتم استلام أي شيء على البند، فيمكن إزالة الكمية. في هذه الحالة، ستكون إعادة التأكيد مطلوبة.
