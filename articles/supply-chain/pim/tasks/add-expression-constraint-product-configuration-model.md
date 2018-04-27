--- 
title: "إضافة قيد تعبير إلى نموذج تكوين منتج"
description: "يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>إضافة قيد تعبير إلى نموذج تكوين منتج

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج. ويُظهر كيفية إصدار أمر رسمي بوجوب يجب تطبيق حماية الزاوية على مكبر صوت إذا قام المستخدم بتحديد شبكة أمامية معدنية. يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.


## <a name="create-an-expression-constraint"></a>قم بإنشاء قيد تعبير
1. انقر فوق "تعريف نموذج متغير المنتج"ز
2. انقر فوق "نماذج تكوين المنتجات".
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * يستخدم هذا المثال نموذج مكبر الصوت المتطور.  
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. قم بتوسيع القسم "القيود".
6. وانقر فوق إضافة.
7. انقر فوق "إنشاء".
8. في حقل "الاسم"، اكتب قيمة.

## <a name="enter-expression"></a>إدخال تعبير
1. انقر فوق "تحرير التعبير".
    * إذا قمت بإلغاء تأمين واجهة المستخدم في تسجيل المهمة في هذه المرحلة، يمكنك استخدام IntelliSense وقائمة من الرموز لإنشاء تعبير القيد.  
2. في الحقل "ConstraintBody"، أدخل "Implies[FrontGrill=="Metal", CornerProtection]".
    * يوضح منطق التعبير هذا: إذا كانت الشبكة الأمامية معدنية، فيجب تحديد خيار حماية الزاوية.  
3. انقر فوق "التحقق من الصحة‬".
    * يتم تشغيل دالة التحقق من الصحة من خلال تعبير القيد وتتحقق من وجود أخطاء في بناء الجملة.  
4. انقر فوق "إغلاق".
5. انقر فوق "موافق".


