---
title: حدوث خطأ عند تغيير الحالة من الإعلام كمنتهي إلى النهاية
description: قد تستلم خطأ عند تغيير حالة أمر الإنتاج من الإعلام كمنتهي إلى النهاية. توضح هذه الصفحة كيفية تقليل المشكلة.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475478"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>حدث خطأ عند تغيير حالة أمر الإنتاج من الإعلام كمنتهي إلى النهاية

## <a name="symptoms"></a>العلامات

عند تغيير حالة أمر الإنتاج من تم الاعلام عنه كمنته حتى النهاية، تستلم إحدى رسائل الخطأ التالية:

> تعارض في التحديث. لا تتطابق التكلفة المعيارية مع قيمه المخزون المالي بعد التحديث.

> حدث خطا فادح في الدالة InventCostMovement.checkVariance.

## <a name="cause"></a>السبب

تحدث هذه المشكلة نتيجة لتغيير البيانات الاساسيه بواسطة عمليه أخرى. ستحاول العملية تحديث البيانات حتى خمس مرات. في حالة استمرار وجود التعارض بعد خمس محاولات، ستتلقى إحدى رسائل الخطأ المذكورة أعلاه:

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. لتقليل المشكلة ، استانف مهمة المجموعة. انتهاء تشغيله.

إذا فشلت مهمة المجموعة بشكل متناسق بعد استئنافها ، فتحقق من توافق دقه التقريب للعملة الافتراضية لدفتر الأستاذ مع التقريب الذي يتم تطبيقه علي القيم الموجودة في الجدول InventSum. إذا تم تغيير دقة التقريب إلى قيمة غير متوافقة، فمن المحتمل أنه يجب عليك تغييرها مرة أخرى إلى قيمة متوافقة. ابحث عن **ModifiedDateTime**. في هذه الحالة ، عاده ما توضح القيمة ان دقه التقريب قد تغيرت مؤخرا.
