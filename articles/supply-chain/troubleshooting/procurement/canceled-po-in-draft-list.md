---
title: تظهر أوامر الشراء الملغية في قائمه المسودة في مساحة العمل
description: تظهر أوامر الشراء الملغاة في قائمة مسودة في مساحة عمل تجهيز أمر الشراء
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
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475494"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>تظهر أوامر الشراء الملغية في قائمه المسودة في مساحة العمل

## <a name="symptoms"></a>العلامات

بعد إلغاء أوامر الشراء التي كانت في الحالة *مؤكد*، يستمر ظهور أوامر الشراء الملغاة في قائمة أوامر الشراء في حالة المسودة في مساحة عمل **تجهيز أمر الشراء**.

## <a name="resolution"></a>الحل

تحدث هذه المشكلة فقط مع أوامر الشراء التي تخضع لإدارة التغييرات. وهي تحدث لأن الإلغاء يُعتبر كتغيير يجب الموافقة عليه. يمكن إجراء الموافقة بشكل تلقائي بواسطة النظام. وبالتالي، تقضي العملية بأن يتم إرسال أمر الشراء الملغى إلى سير عمل الموافقة بحيث يمكنه الانتقال إلى الحالة *موافق عليه*. وفي هذه المرحلة، سيتوقف ظهور أمر الشراء في قائمة أوامر الشراء بحالة المسودة في مساحة عمل **تجهيز أمر الشراء**.
