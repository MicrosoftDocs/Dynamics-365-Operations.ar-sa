---
title: إنشاء عمل انتقاء فور إصدار حمل العمل
description: إذا كان يجب إنشاء العمل فورا عند إصدار الحمل ، يجب ان تقوم بتكوين قالب الموجه وفقا لذلك. ترشدك هذه الصفحة عبر الخطوات.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475490"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>لا يتم إنشاء عمل انتقاء فور إصدار التحميل الصادر

## <a name="symptoms"></a>العلامات

يمكنك إنشاء حمل عمل صادر باستخدام أمر مبيعات أو تحويل وإصدار حمل العمل إلى المستودع. مع ذلك، تلاحظ أنه لم يتم إنشاء عمل انتقاء بعد.

## <a name="resolution"></a>الحل

إذا كان يجب إنشاء العمل فورا عند إصدار الحمل ، يجب ان تقوم بتكوين قالب الموجه وفقا لذلك. في قالب الموجه ، قم بتعيين الخيارات التالية إلى *نعم*:

- جعل إنشاء الموجة تلقائيًا
- معالجة الموجة عند الإصدار إلى المستودع
- جعل تحرير الموجة تلقائيًا
