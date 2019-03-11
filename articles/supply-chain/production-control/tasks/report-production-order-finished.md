---
title: الإبلاغ عن انتهاء أمر إنتاج
description: يوضح هذا الإجراء كيفية الإبلاغ عن أمر إنتاج كمنتهٍ.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97e67ff51e4bc4533aeb2485c34cd5ec8a882bb6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "320479"
---
# <a name="report-a-production-order-as-finished"></a>الإبلاغ عن انتهاء أمر إنتاج

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية الإبلاغ عن أمر إنتاج كمنتهٍ. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا هو الإجراء السادس من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.


## <a name="report-a-production-order-as-finished"></a>الإبلاغ عن انتهاء أمر إنتاج
1. انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.
    * حدد أمر إنتاج يكون في الحالة "تم بدءه".  
2. في جزء "الإجراءات"، انقر فوق "أمر إنتاج".
3. انقر فوق تقرير كمنتهِ.
    * في هذه الصفحة، يمكنك تأكيد كمية المنتج المنتهي للإبلاغ عنها كمنتهية.  
4. انقر فوق علامة التبويب "عام".
5. عيّن "كمية البضائع" على "18".
6. عيّن "كمية الأخطاء" على "2".
7. في الحقل "سبب الخطأ"، حدد "المادة".
8. حدد خانات الاختيار "إنهاء الوظيفة" أو قم بإلغاء تحديدها.
9. حدد خانة الاختيار "قبول الخطأ" أو قم بإلغاء تحديدها.
10. انقر فوق "موافق".

## <a name="verify-the-report-as-finished-journal"></a>التحقق من دفتر يومية "الإبلاغ عنه كمنتهٍ".
1. في جزء "الإجراءات"، انقر فوق "عرض".
2. انقر فوق "تم الإبلاغ عنه كمنتهٍ".
3. في القائمة، قم بوضع علامة للصف المحدد.
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * تم ترحيل دفتر يومية التقرير كمنتهٍ. إذا أردت إجراء تعديلات على دفتر اليومية، يمكنك إنشاء دفتر يومية جديد يدويًا حيث يمكنك إجراء تغييرات.  

