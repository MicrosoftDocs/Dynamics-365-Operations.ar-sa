---
title: بقاء حالة الأمر صادر جزئياً بعد أن تتم فوترته
description: في بعض الحالات تظل حالة أمر المبيعات صادر جزئياً، حتى بعد أن تتم فوتره الأمر. تشرح هذه الصفحة لماذا يحدث ذلك والحلول الممكنة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475482"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>بقاء حالة الأمر صادر جزئياً حتى بعد أن تتم فوترة أمر المبيعات

## <a name="symptoms"></a>العلامات

أمر المبيعات هو أمر تسليم ، ولكن صنف واحد أو أكثر له له وضع تسليم مختلف. بعد فوتره الأمر ، يبقي له حاله إصدار تم *إصدارها جزئيا*.

علي سبيل المثال ، يكون لأمر التوريد صنفين: أحدهما بالنسبة للتسليم والاخر للالتقاط. تم اجراء التسليم والتقاط. ولذلك ، تمت فوتره كلا البندين. ومع ذلك ، لا تزال حاله الإصدار ظاهره علي انها تم *إصدارها جزئيا*، وهي مضلله.

## <a name="workaround"></a>حل بديل

تنطبق حاله الإصدار فقط علي بنود الأمر التي يتم فيها تمكين الأصناف لأداره المستودعات. لذلك تبقي حاله الإصدار تم *إصدارها جزئيا* في هذا السيناريو. قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. ويمكن أضافه ملحق كجزء من كشف التعبئة وعمليه الفوترة لتحديث حاله الإصدار.
