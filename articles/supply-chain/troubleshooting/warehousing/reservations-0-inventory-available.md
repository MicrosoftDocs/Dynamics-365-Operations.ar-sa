---
title: لا يمكن إجراء عمليات حجز مخزون نظراً لتوفر 0.00
description: تستلم رسالة خطأ مفادها أن النظام لا يمكنه إجراء عمليات حجز نظرا لتوفر 0.00 في المخزون. قد يكون سبب هذه المشكلة هو فتح العمل.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475503"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>لا يمكن للنظام إجراء عمليات حجز نظرا لتوفر 0.00 في المخزون

## <a name="symptoms"></a>العلامات

قد تحدث هذه المشكلة في حاله عدم تمكن النظام من تحديث كميه مخزون نظرا لعدم وجود حركات مخزون كافيه بالابعاد المحددة. سوف تتلقى رسالة الخطأ التالية:

> موقع الفعلي = %1، المستودع = %2، حاله المخزون = متاح، رقم المجموعة = %3، المالك = %4 : لا يمكن حجز %5 نظرا لتوفر 0.00 فقط في المخزون.

## <a name="resolution"></a>الحل

قد يكون سبب هذه المشكلة هو فتح العمل. قم اما بإكمال العمل أو الاستلام دون إنشاء العمل. تاكد من عدم قيام إيه حركات مخزون بالفعل بحجز الكمية. علي سبيل المثال ، قد تكون هذه الحركات أوامر جودة مفتوحة أو سجلات حظر المخزون أو أوامر المخرجات.
