---
title: يحدث خطأ عند تحديد الموقع أثناء تسجيل قائمة الانتقاء
description: يحدث خطأ عند تحديد الموقع أثناء تسجيل قائمة الانتقاء.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef34b4fdcc572c56319f6cbf4913d822d8857595
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474954"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>يحدث خطأ عند تحديد الموقع أثناء تسجيل قائمة الانتقاء

رقم KB: 4613106

## <a name="symptoms"></a>العلامات

تحدث هذه المشكلة في حالة تكوين النظام الخاص بك لحجز أوامر المبيعات تلقائيًا. إذا حاولت تحديد موقع لبند تسجيل قائمة الانتقاء، فإنك تتلقي رسالة الخطأ التالية عند استخدام عمليات الحجز لإدارة المستودع (WMS):

> لا يمكن تحديث الكمية بالأبعاد الجديدة

قد تحدث هذه المشكلة نظرًا لعدم وجود مخزون فعلي كافي في موقع محدد.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم.

في السيناريوهات التي تستخدم فيها عملية الحجز على مستوى المستودع، إذا لم يتم حجز المخزون الفعلي على كافة مستويات أبعاد المخزون، ولم يكن لديك مخزون فعلي كاف في موقع محدد، فإننا نوصي باستخدام عملية الحجز اليدوي من بند الانتقاء. ويمكنك بعد ذلك استخدام الوظيفة *حجز دفعة* لتوزيع الحجوزات الأدنى، مثل الموقع، لكافة الكميات الفعلية المتاحة.
