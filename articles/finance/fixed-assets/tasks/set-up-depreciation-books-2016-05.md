---
title: إعداد دفاتر الإهلاك (مايو 2016)
description: سيقوم دليل المهمة هذا بإنشاء دفتر إهلاك جديد ويقرنه بمجموعة أصول ثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186890"
---
# <a name="set-up-depreciation-books-may-2016"></a>إعداد دفاتر الإهلاك (مايو 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

سيقوم دليل المهمة هذا بإنشاء دفتر إهلاك جديد ويقرنه بمجموعة أصول ثابتة.  إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.


## <a name="create-a-depreciation-book"></a>إنشاء دفتر إهلاك
1. انتقل إلى الأصول الثابتة > إعداد > دفاتر الإهلاك.
2. انقر فوق "جديد".
3. في الحقل "دفتر الإهلاك"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. حدد خانة الاختيار "حساب الإهلاك‬" أو قم بإلغاء تحديدها.
6. في الحقل "ملف تعريف الإهلاك"، انقر فوق زر القائمة المنسدلة لفتح البحث.
7. في القائمة، ابحث عن ملف تعريف الإهلاك المطلوب وحدده.
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
9. في الحقل "ملف تعريف الإهلاك البديل"، انقر فوق زر القائمة المنسدلة لفتح البحث.
10. في القائمة، حدد ملف تعريف الإهلاك المطلوب.
11. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * حدد ملف تعريف الإهلاك الاستثنائي‬ لاستخدامه في إهلاك إضافي لأصل ما في ظروف غير عادية. على سبيل المثال، قد تستخدم هذا الملف لتسجيل الإهلاك الناتج عن كارثة طبيعية.  
12. حدد خانة الاختيار "إنشاء تسويات الإهلاك التي لها تسويات أساسية‬" أو قم بإلغاء تحديدها.
13. في الحقل "التقويم"، انقر فوق زر القائمة المنسدلة لفتح البحث.
14. في القائمة، انقر فوق الارتباط في الصف المحدد.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>إقران دفتر الإهلاك بمجموعة أصول ثابتة
1. انقر فوق "مجموعات الأصول الثابتة".
2. في الحقل "مجموعة الأصول الثابتة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. في الحقل "قواعد الإهلاك‬‬"، حدد خيارًا.
6. في الحقل "مدة الخدمة‬"، أدخل رقمًا.
    * لاحظ أنه يتم حساب قيمة الحقل "فترات الإهلاك" بعد تعيين مدة الخدمة.  
