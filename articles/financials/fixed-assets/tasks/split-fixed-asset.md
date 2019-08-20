---
title: تقسيم أصل ثابت
description: سيقوم دليل المهمة هذا بتقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5fdc8a7b326daca1fc0f0962c69bb8fb1ff64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839703"
---
# <a name="split-a-fixed-asset"></a>تقسيم أصل ثابت

[!include [task guide banner](../../includes/task-guide-banner.md)]

سيقوم دليل المهمة هذا بتقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.  إنه يستخدم دور المحاسب وبيانات العرض التوضيحي USMF.‬


## <a name="create-a-new-fixed-asset"></a>إنشاء أصل ثابت جديد
1. انتقل إلى الأصول الثابتة > الأصول الثابتة > الأصول الثابتة.
2. انقر فوق "جديد".
3. في حقل "مجموعة الأصول الثابتة"، أدخل قيمة أو حددها.
4. لاحظ رقم الأصل الثابت لاستخدامه في عملية التقسيم لاحقًا.
5. في حقل "الاسم"، اكتب قيمة.
6. وقم بغلق النموذج.

## <a name="split-a-fixed-asset"></a>تقسيم أصل ثابت
1. في القائمة، ابحث عن الأصل الثابت المراد تقسيمه وحدده.
2. في القائمة، انقر فوق الارتباط في الصف المحدد.
3. انقر فوق "الدفاتر".
    * حدد الدفتر لتقسيمه إلى الأصل الجديد.  
4. انقر فوق "الوظائف".
5. انقر فوق "تقسيم أصل ثابت‬".
6. في حقل "إلى الأصل الثابت‬"، أدخل قيمة أو حددها.
7. في الحقل "إلى دفتر‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
8. في حقل "‏‫تاريخ الحركة"، أدخل تاريخًا.
9. في الحقل "النسبة‬"، أدخل رقمًا.
10. في الحقل "اسم دفتر اليومية"، أدخل قيمة أو حددها.
11. انقر فوق "موافق".

## <a name="post-the-journal-transaction"></a>ترحيل حركة دفتر اليومية
1. انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬.
2. في القائمة، حدد دفتر اليومية الذي تم إنشاؤه بواسطة عملية التقسيم.
3. انقر فوق البنود.
    * تحقق من بنود دفتر اليومية التي تم إنشاؤها.  يتم إنشاء حركة تسوية الاستحواذ للأصل الأولي لإنقاص القيمة بالنسبة المئوية المحددة أثناء عملية التقسيم.  يتم إنشاء حركة استحواذ للأصل الجديد بالمبلغ نفسه.  
4. انقر فوق "ترحيل".

