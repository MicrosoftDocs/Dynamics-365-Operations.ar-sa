---
title: لا يتم عرض أوامر الإنتاج في صفحة وضع العلامات
description: لا يتم عرض أوامر الإنتاج في صفحه وضع العلامات. يشرح هذا الموضوع تكوينات المنتجات الثلاثة غير المتوفرة لوضع العلامة.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475418"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>لا يتم عرض أوامر الإنتاج في صفحة وضع العلامات

## <a name="symptoms"></a>العلامات

عند العمل مع التصنيع المنفصل، لا تظهر بعض أوامر الإنتاج فى صفحة **وضع العلامات**.

## <a name="resolution"></a>الحل

لا تتوفر المنتجات التي لها التكوينات التالية لوضع العلامة. لذلك، لن يتم إظهارها في صفحه **وضع العلامات**:

- يتم تعريف المنتجات كمنتجات من نوع *وزن التعبئة*.
- ويتم تمكينها لعمليات المستودع المتقدمة.
- ويتم تكوينها ليتم التحكم فيها بواسطة مبدأ *التكلفة المعياري*.
