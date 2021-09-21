---
title: حدث خطأ في مسار الشهادة عند الترقية أو الترحيل إلى WMS
description: إذا أظهر التطبيق خطأ "ربط الثقة لمسار الشهادة غير موجود" عند الترقية أو الترحيل إلى WMS، فإن هذه الصفحة توفر معلومات حول كيفية إصلاح المشكلة.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475446"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>لم يتم العثور على ربط الثقة لمسار الشهادة عند التحديث والترحيل إلى WMS

## <a name="symptoms"></a>العلامات

عند الترقية أو الترحيل إلى إدارة المستودعات المتقدمة (WMS)، قد يعرض تطبيق Warehouse Management رسالة الخطأ التالية:

> java.security.cert.certPathValidatorException: رابط الثقة لمسار الشهادة غير موجود.

## <a name="cause"></a>السبب

يحدث ذلك بسبب عدم اعتماد الشهادات الموقعة ذاتياً على Android8 + في البيئات المحلية.

## <a name="resolution"></a>الحل

استخدم المرجع المصدق (العام) الخارجي (CA). يتوفر إصلاح لهذه المشكلة في الإصدار 1.9.0.0 من تطبيق Warehouse Management. لمزيد من المعلومات حول هذه المشكلة وكيفية إصلاحها، راجع [ربط الثقة لمسار الشهادة غير موجود عند اعداد اتصال التطبيق](certification-path-app-connection-error.md).
