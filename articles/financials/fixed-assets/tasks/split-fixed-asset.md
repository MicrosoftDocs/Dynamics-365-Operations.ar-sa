---
title: تقسيم أصل ثابت
description: يشرح هذا الموضوع كيفية تقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867573"
---
# <a name="split-a-fixed-asset"></a>تقسيم أصل ثابت

[!include [task guide banner](../../includes/task-guide-banner.md)]

يشرح هذا الموضوع كيفية تقسيم نسبة مئوية من دفتر الأصول إلى دفتر أصول جديد. إنه يستخدم دور المحاسب وبيانات العرض التوضيحي USMF.‬


## <a name="create-a-new-fixed-asset"></a>إنشاء أصل ثابت جديد
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الأصول الثابتة > الأصول الثابتة‬**.
2. حدد **جديد**.
3. في حقل **مجموعة الأصول الثابتة**، أدخل قيمة أو حددها. لاحظ رقم الأصل الثابت لاستخدامه في عملية التقسيم لاحقًا.  
4. في الحقل **الاسم**، اكتب قيمة.
5. وقم بغلق النموذج.

## <a name="split-a-fixed-asset"></a>تقسيم أصل ثابت
1. في القائمة، ابحث عن الارتباط إلى الأصل الثابت المراد تقسيمه وحدده.
2. حدد **الدفاتر**. حدد الدفتر لتقسيمه إلى الأصل الجديد.  
3. حدد **الوظائف**.
4. حدد **تقسيم الأصل الثابت**.
5. في حقل **إلى الأصل الثابت**، أدخل قيمة أو حددها.
6. في الحقل **إلى دفتر‬**، حدد زر القائمة المنسدلة لفتح البحث.
7. في حقل **‏‫تاريخ الحركة**، أدخل تاريخًا.
8. في الحقل **النسبة‬ المئوية**، أدخل رقمًا.
9. في الحقل **اسم دفتر اليومية**، أدخل قيمة أو حددها.
10. حدد **موافق**.

## <a name="post-the-journal-transaction"></a>ترحيل حركة دفتر اليومية
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬**.
2. في القائمة، حدد دفتر اليومية الذي تم إنشاؤه بواسطة عملية التقسيم.
3. حدد **البنود**.

    - تحقق من بنود دفتر اليومية التي تم إنشاؤها.  
    - يتم إنشاء حركة تسوية الاستحواذ للأصل الأولي لإنقاص القيمة بالنسبة المئوية المحددة أثناء عملية التقسيم.  
    - يتم إنشاء حركة استحواذ للأصل الجديد بالمبلغ نفسه.  

4. حدد **ترحيل**.

