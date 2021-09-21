---
title: لا يمكن حجز الصنف RM عند إصدار أمر إنتاج
description: 'عند إصدار أمر إنتاج، قد تتلقى الخطأ: "تعذر حجز الصنف RM بالكامل." تأكد من توفر الكمية بالكامل أو قم بحجز الأصناف يدوياً.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475499"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>لا يمكن حجز الصنف RM بالكامل عند إصدار أمر إنتاج

## <a name="symptoms"></a>العلامات

في حالة عدم توفر كافة أصناف بنود قائمة مكونات الصنف بشكل فعلي عند إصدار أمر إنتاج إلى مستودع، وتعيين السياسة **إصدار إلى المستودع** على *طلب حجز كامل*، ستتلقى رسالة الخطأ التالية:

> تعذر حجز الصنف RM بالكامل. تاكد من توفر الكمية بالكامل أو قم بحجز الأصناف يدويا إذا كان حقل الحجز في بند قائمة مكونات الصنف معينا علي "يدوي" أو "تم البدء". تعذر إصدار الأمر للمستودع نظرًا لتعذر حجز بعض المواد.

## <a name="resolution"></a>الحل

يتم هذا السلوك حسب التصميم ويعمل كما هو متوقع. لحل هذه المشكلة، اتبع الإرشادات الواردة في رسالة الخطأ: "تأكد من توفر الكمية بالكامل أو قم بحجز الأصناف يدوياً إذا تم تعيين حقل الحجز في بند شجرة مكونات الصنف على"يدوي" أو "تم البدء."
