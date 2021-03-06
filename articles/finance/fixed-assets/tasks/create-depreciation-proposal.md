---
title: إنشاء مقترح الإهلاك
description: يصف هذا الموضوع كيفية عمل مقترحات دُفعة الإهلاك ويشرح كيفية اقتراح إهلاك الأصول الثابتة.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3d62e982d26afbec7ac04dd80592a73f4a3286f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968887"
---
# <a name="create-a-depreciation-proposal"></a>إنشاء مقترح الإهلاك

[!include [banner](../../includes/banner.md)]

يصف هذا الموضوع كيفية عمل مقترحات دُفعة الإهلاك ويشرح كيفية اقتراح إهلاك الأصول الثابتة. تستخدم هذه المهمة شركة العرض التوضيحي USMF ودور المحاسب.


## <a name="create-a-depreciation-proposal"></a>إنشاء مقترح الإهلاك
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > إنشاء مقترح الإهلاك‬‬**.
2. في الحقل **اسم دفتر اليومية‬**، حدد خيارًا من القائمة المنسدلة.
3. في الحقل **إلى تاريخ**، أدخل تاريخًا.

    - حدد الخيار **تلخيص الإهلاك** لتلخيص عمليات الإهلاك الشهرية في بند واحد بدفتر اليومية.  
    - على سبيل المثال، إذا كانت قيمة "إلى تاريخ" 31 مارس 2015، يتم إنشاء الوصف التالي: "الإهلاك منذ 31 يناير 2015." يتم عندئذٍ تعيين حقل **التاريخ** في بنود دفتر اليومية المقترحة إلى 31 مارس 2015.  
    - يمكن تصفية مقترح الإهلاك حسب الأصول أو مجموعة الأصول أو معايير أخرى باستخدام خيار **التصفية**.  
    - عندما تستخدم النموذج **إنشاء مقترحات استحواذ أو إهلاك للأصول الثابتة‬**، يمكنك اقتراح الإهلاك بدفعات. يوصى بهذا الإجراء للمقترحات الكبيرة التي ستستخدم المزيد من موارد النظام. إذا حددت خيار الدُفعة، فيمكنك الاستمرار في إكمال مهام أخرى خلال هذه الفترة. عند اقتراح الإهلاك بهذه الطريقة، يتم حساب الإهلاك لنماذج القيمة للأصول الثابتة.  

4. حدد **إنشاء دفتر اليومية**.

## <a name="review-depreciation-entries"></a>مراجعة إدخالات الإهلاك
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. حدد **البنود**.
4. حدد **ترحيل**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]