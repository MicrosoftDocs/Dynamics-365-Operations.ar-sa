---
title: استكشاف أخطاء الإصدار الجزئي والشحنات الجزئية وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات الإصدار الجزئية والشحنات الجزئية في Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263218"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>استكشاف أخطاء الإصدار الجزئي والشحنات الجزئية وإصلاحها

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إصلاح المشكلات الشائعة التي قد تواجهها أثناء العمل مع عمليات الإصدار الجزئية والشحنات الجزئية في Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>وتظل حاله إصدار أمر المبيعات قد تم إصدارها جزئيا حتى بعد ان تتم فوتره أمر المبيعات.

### <a name="issue-description"></a>وصف المشكلة

أمر المبيعات هو أمر تسليم ، ولكن صنف واحد أو أكثر له له وضع تسليم مختلف. بعد فوتره الأمر ، يبقي له حاله إصدار تم *إصدارها جزئيا*.

علي سبيل المثال ، يكون لأمر التوريد صنفين: أحدهما بالنسبة للتسليم والاخر للالتقاط. تم اجراء التسليم والتقاط. ولذلك ، تمت فوتره كلا البندين. ومع ذلك ، لا تزال حاله الإصدار ظاهره علي انها تم *إصدارها جزئيا*، وهي مضلله.

### <a name="issue-resolution"></a>حل المشكلة

تنطبق حاله الإصدار فقط علي بنود الأمر التي يتم فيها تمكين الأصناف لأداره المستودعات. لذلك تبقي حاله الإصدار تم *إصدارها جزئيا* في هذا السيناريو. قامت Microsoft بتقييم هذه المشكلة وقامت بتحديد انها قيد ميزه. ويمكن أضافه ملحق كجزء من كشف التعبئة وعمليه الفوترة لتحديث حاله الإصدار.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]