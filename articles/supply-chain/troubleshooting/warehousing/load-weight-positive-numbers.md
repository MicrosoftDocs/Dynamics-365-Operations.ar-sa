---
title: يمكن أن يحتوي وزن حمل العمل على أرقام موجبة فقط
description: عند معالجة العمل بين المواقع، قد تتلقي خطأ يتعلق بوزن حمل العمل ويتم إلغاء التحديث الخاص بك. اتبع هذه الخطوات لإصلاح المشكلة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475460"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>حدث خطأ في وزن التحميل وتم إلغاء التحديث عند معالجة العمل بين المواقع

## <a name="symptoms"></a>العلامات

في حالة وجود عمل مفتوح عند معالجة العمل من مواقع التعبئة إلى مواقع التقسيم، أو من المواقع المرحلية إلى مواقع اللإرساء، قد تستلم الخطأ التالي:

> يمكن أن يحتوي 'وزن حمل العمل' (=-%1) للمجال على أرقام موجبة فقط. تم إلغاء التحديث.

## <a name="resolution"></a>الحل

لحل هذه المشكلة ، انتقل إلى **إدار النظام \> المهام الدورية \> قاعدة البيانات \> فحص الاتساق**، ثم قم بتشغيل عمليه **فحص اتساق وزن الحمولة للمستودع**.
