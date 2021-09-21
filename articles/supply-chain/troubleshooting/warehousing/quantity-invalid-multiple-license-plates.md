---
title: الكمية غير صالحة لعمل الانتقاء بلوحات ترخيص متعددة
description: عند وجود عمل انتقاء يحتوي على لوحات ترخيص متعددة في موقع واحد، تصبح الكمية غير صالحة لوحدة ea. تحقق من صحة الحقول التالية.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475431"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>الكمية غير صالحة عند وجود عمل الانتقاء مع العديد من لوحات الترخيص في أحد المواقع

## <a name="symptoms"></a>العلامات

عند وجود عمل انتقاء يحتوي على لوحات ترخيص متعددة في موقع واحد، تصبح الكمية غير صالحة لوحدة *ea* وتستلم رسالة الخطأ التالية:

> الكمية غير صالحة للوحدة 1%.

## <a name="resolution"></a>الحل

تحقق من تعيين الحقلين **معرف مجموعه تسلسل الوحدات** و **تحويلات الوحدات** في متغير المنتج أو المنتج الذي تم إصداره بشكل صحيح.

لاحظ أنه تم تحسين رسالة الخطأ في الإصدار 10.0.15 لإظهار الكمية المتوقع (راجع [قاعدة المعارف 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). رسالة الخطأ الجديدة هي:

> الكمية غير صالحة. المتوقع %1 %2.
