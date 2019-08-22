---
title: حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى (فبراير 2016)
description: يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ أحادية المستوى يوجد أساسها في كشف التكاليف.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1968703c7e9662b5cccdb71d049010bb4bd4534
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836494"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>حساب قائمة مكونات الصنف باستخدام هيكل أحادي المستوى (فبراير 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية حساب تكلفة المنتج النهائي باستخدام عملية تحديد إجمالي المكونات المطلوبة‬ أحادية المستوى يوجد أساسها في كشف التكاليف. إنها المهمة السادسة في سلسلة حسابات قائمة مكونات الصنف. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USMF.‬

1. انتقل إلى "المنتجات الصادرة‬".
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد المنتج BOM_1.  
3. في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".
4. انقر فوق "سعر الصنف".
5. انقر فوق "حساب تكلفة الصنف".
    * قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.  
6. في الحقل "إصدار محاسبة التكاليف"، انقر فوق زر القائمة المنسدلة لفتح البحث.
    * بالنسبة إلى هذا العرض التوضيحي، حدد 10. هذا هو إصدار محاسبة التكاليف نفسه المستخدم لإضافة سعر التكلفة إلى المكونات.  
7. انقر فوق "موافق".
8. انقر فوق "عرض تفاصيل الحساب"ز
    * قد تحتاج إلى النقر فوق علامة القطع (...) لرؤية هذا الخيار في القائمة العلوية.    إليك تركيب التكلفة:  •    يشتق 10 من ITEM_A، و10 من ITEM_B, 10 من BOM_2. وفي هذه الحالة لا توجد تفاصيل لـ BOM_2 حيث تم إدخالها كتكلفة معيارية من 10 لكن ذلك لم يتم من خلال الحساب.  •  يشتق 7 من وقت الإعداد، وهو تكلفة ثابتة، ويشتق 7 إضافي من عملية وقت التشغيل (العملية).  •   هناك أيضًا مبالغ أخرى تتطابق مع التكاليف غير المباشرة.  
9. @SysTaskRecorder:_RequestClose

