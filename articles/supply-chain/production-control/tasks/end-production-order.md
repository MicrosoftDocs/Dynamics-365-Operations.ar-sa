---
title: "إنهاء أمر إنتاج"
description: "يوضح هذا الإجراء كيفية إنهاء أمر إنتاج."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 1cc586f804a072ca5499c73ecdf7d37778cbf067
ms.contentlocale: ar-sa
ms.lasthandoff: 02/06/2018

---
# <a name="end-a-production-order"></a>إنهاء أمر إنتاج

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنهاء أمر إنتاج. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. هذا هو الإجراء النهائي من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.


## <a name="end-a-production-order"></a>إنهاء أمر إنتاج
1. انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.
    * حدد أمر إنتاج يكون في الحالة "تم الإبلاغ عنه كمنتهٍ".  
2. في جزء "الإجراءات"، انقر فوق "أمر إنتاج".
3. انقر فوق "إنهاء".
    * في هذه الصفحة، يمكنك تأكيد رغبتك في إنهاء أمر الإنتاج.  
4. انقر فوق علامة التبويب "عام".
5. في حقل "التاريخ"، أدخل تاريخًا.
6. في الحقل "أسلوب الخردة"، حدد "تخصيص".
    * عند تحديد طريقة التخصيص، تتم إضافة التكاليف من مواد الخردة إلى البضائع المنتهية.  
7. انقر فوق "موافق".

## <a name="validate-calculation-results"></a>التحقق من صحة نتائج الحساب
1. في جزء الإجراءات، انقر فوق "إدارة التكاليف‬".
2. انقر فوق "عرض مقارنة التكلفة".
    * بعد إنهاء أمر الإنتاج، يمكنك مقارنة سعر التكلفة المقدر مقابل سعر التكلفة المحقق للحصول على نظرة عامة حول نسب الفرق في الإنتاج.  

