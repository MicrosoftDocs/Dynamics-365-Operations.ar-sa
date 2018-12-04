--- 
title: "تعيين حالة دورة حياة منتج لأصل منتج صادر"
description: "يُظهر هذا الإجراء كيفية تعيين حالة دورة حياة منتج إلى أصل منتج صادر ومتغيراته."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: f476c1b2585ce0b5b67cd0d91684c86f7d3bda36
ms.contentlocale: ar-sa
ms.lasthandoff: 02/08/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>تعيين حالة دورة حياة منتج لأصل منتج صادر

[!include [task guide banner](../../includes/task-guide-banner.md)]

يُظهر هذا الإجراء كيفية تعيين حالة دورة حياة منتج إلى أصل منتج صادر ومتغيراته. المتطلبات الأساسية: يجب أولاً تشغيل دليل المهام "إنشاء حالة دورة حياة منتج جديدة" للتأكد من أن لديك حالة دورة حياة منتج واحدة على الأقل تم إنشاؤها قبل تشغيل دليل المهام هذا.


## <a name="find-a-released-product-master"></a>البحث عن أصل منتج صادر
1. انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.

> [!NOTE]
> أصل المنتج يتضمن أصل المنتج للنوع الفرعي للمنتج.  

## <a name="update-the-lifecycle-state"></a>تحديث حالة دورة الحياة
1. انقر فوق "تحرير".
2. في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.
3. انقر فوق "حفظ".
4. انقر فوق نعم.

> [!NOTE]
> إذا تم تحديد "نعم"، فسيتم أيضًا تحديث كافة متغيرات المنتجات الصادرة ذات الحالة الأصلية نفسها لأصل المنتج الصادر إلى حالة دورة حياة المنتج الجديدة. أما إذا تم تحديد "لا"، فستحافظ كافة المتغيرات على حالتها الفعلية. لن يتم تحديث المتغيرات ذات حالة دورة حياة منتج مختلفة عن أصل المنتج الصادر.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>التحقق من حالة دورة الحياة للمتغيرات
1. انقر فوق "متغيرات المنتج الذي تم إصداره".

> [!NOTE]
> لاحظ أن كافة المتغيرات قد ورثت حالة دورة الحياة المحددة من أصل المنتج الصادر.  

2. في القائمة، قم بوضع علامة للصف المحدد.
3. في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.


