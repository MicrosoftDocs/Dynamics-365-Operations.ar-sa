---
title: إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي
description: يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج جديدة تستثني المنتجات من الحساب على مستوى التخطيط الرئيسي وقائمة مكونات الصنف.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 156972cdbf4ffb02b01b00972cc83d003d941378
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "326344"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>إنشاء حالة دورة حياة منتج لاستبعاد المنتجات من التخطيط الرئيسي

[!include [task guide banner](../../includes/task-guide-banner.md)]

يُظهر هذا الإجراء كيفية إنشاء حالة دورة حياة منتج جديدة تستثني المنتجات من الحساب على مستوى التخطيط الرئيسي وقائمة مكونات الصنف.


## <a name="create-an-obsolete-state"></a>إنشاء حالة قديمة
1. انتقل إلى إدارة معلومات المنتج > الإعداد > حالة دورة حياة المنتج.
2. انقر فوق "جديد".
3. في حقل "الحالة"، اكتب قيمة.
4. حدد "لا" في حقل "نشط للتخطيط‬".
5. في وصف الحقل، اكتب قيمة.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>إقران الحالة القديمة بمنتج صادر
1. قم بإغلاق الصفحة.
2. انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.
3. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على حقل "اسم البحث" بقيمة "M00".
4. انقر فوق "تحرير".
5. في القائمة، قم بوضع علامة للصف المحدد.
6. في الحقل "حالة دورة حياة المنتج"، أدخل قيمة أو حددها.

