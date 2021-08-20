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
ms.openlocfilehash: da5905fb7ed1e890c85e891843379aa07de3279bd8972d6fc57136aa703c9ea4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762784"
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
