---
title: إنشاء حالة دورة حياة منتج افتراضية
description: يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج افتراضية بالإضافة إلى كيفية إقران الحالة الافتراضية مع المنتجات الصادرة.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16f604d5e06859b15c6f610e7a5c822ef2089ea3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966895"
---
# <a name="create-a-default-product-lifecycle-state"></a>إنشاء حالة دورة حياة منتج افتراضية

[!include [banner](../../includes/banner.md)]

يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج افتراضية بالإضافة إلى كيفية إقران الحالة الافتراضية مع المنتجات الصادرة.


## <a name="create-a-default-lifecycle-state"></a>إنشاء حالة دورة حياة افتراضية
1. انتقل إلى إدارة معلومات المنتج > الإعداد > حالة دورة حياة المنتج.
2. انقر فوق "جديد".
3. في حقل "الحالة"، اكتب قيمة.
4. حدد "نعم" في حقل "الإعداد الافتراضي عند إصدار منتج لكيان قانوني‬".‬
5. في وصف الحقل، اكتب قيمة.
6. حدد "لا" في حقل "نشط للتخطيط‬".

> [!NOTE]
> إذا لم يكن من الضروري تضمين منتج جديد صادر في التخطيط الرئيسي‬‏‫، فحدد "لا". أما إذا كان يجب تضمينه في التخطيط الرئيسي، فاترك عنصر التحكم معينًا إلى قيمته الافتراضية "نعم".  

## <a name="create-a-new-released-product"></a>إنشاء منتج جديد صادر
1. قم بإغلاق الصفحة.
2. انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.
3. انقر فوق "جديد".
4. في الحقل "رقم المنتج"، اكتب قيمة.
5. في الحقل "اسم المنتج"، اكتب قيمة.
6. في الحقل "اسم البحث‬"، اكتب قيمة.
7. في الحقل "مجموعة النموذج"، أدخل قيمة أو حددها.
8. في حقل "مجموعة الصنف"، أدخل قيمة أو حددها.
9. في الحقل "مجموعة بُعد التخزين"، أدخل قيمة أو حددها.
10. في الحقل "مجموعة بُعد التعقب"، أدخل قيمة أو حددها.
11. انقر فوق "موافق".

> [!NOTE]
> دورة حياة المنتج الافتراضية عبارة عن تعريف عمومي.  

## <a name="change-the-product-to-an-active-state"></a>تغيير المنتج إلى حالة نشطة
1. في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.

> [!NOTE]
> لنفترض أنك قمت بإعداد حالة نشطة، يمكنك الآن تحديد الحالة النشطة للسماح بأن يتم استخدام المنتج في الحساب على مستوى التخطيط الرئيسي وقائمة مكونات الصنف. من الواضح أن هذا الأمر يعتبر منطقيًا إذا كانت جميع تفاصيل المنتج المطلوبة للتخطيط المتناسق محددة.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]