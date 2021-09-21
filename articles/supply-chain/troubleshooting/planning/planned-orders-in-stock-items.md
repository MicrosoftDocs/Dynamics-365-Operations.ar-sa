---
title: يتم إنشاء الأوامر المخططة للمخزون المضمن مع أوامر الإنتاج
description: ويتم إنشاء الأوامر المخططة على الرغم من وجود أصناف في أوامر المخزون والإنتاج متوفرة بالفعل لها
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475521"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>يتم إنشاء الأوامر المخططة للمخزون المضمن مع أوامر الإنتاج

## <a name="symptoms"></a>العلامات

يتم إنشاء الأوامر المخططة على الرغم من وجود أصناف في أوامر المخزون والإنتاج متوفرة بالفعل لها.

## <a name="resolution"></a>الحل

قد تتمكن من حل هذه المشكلة عن طريق زيادة قيمه **الأيام الموجبة** للمجموعات ذات الصلة في صفحه **مجموعه التغطية**. سيؤدي هذا التغيير إلى تحديد ما إذا كان من الممكن استخدام المخزون الفعلي للطلب ام لا. وبعد ذلك لن يتم إنشاء أمر مخطط جديد للأصناف الموجودة بالمخزن.
