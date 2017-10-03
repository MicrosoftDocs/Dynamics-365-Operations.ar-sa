--- 
title: "تسوية الشحن يدويًا"
description: "يوضح هذا الإجراء كيفية تسوية الشحن يدويًا."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 28de4c720cd771f476f379d925e9500e41482aa6
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="reconcile-freight-manually"></a>تسوية الشحن يدويًا

[!include[task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية تسوية الشحن يدويًا. عادة ما يتم ذلك عن طريق منسق نقل. يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.


## <a name="select-a-load-to-reconcile"></a>تحديد حمل عمل للتسوية
1. انتقل إلى إدارة النقل > التخطيط > منضدة عمل تخطيط الحِمل‬.
2. قم بإلغاء تحديد خانة الاختيار "إخفاء ما تم شحنه‬ وما تم استلامه‬". 
3. في القائمة، حدد الحمولة ذات معرف الحمل 00006.

## <a name="create-a-carrier-invoice"></a>إنشاء فاتورة شركة نقل
    * إذا قمت بتسوية الشحن يدويًا ولم تستلم فواتير الشركة تلقائيًا، فيمكنك إنشاء فاتورة استنادًا إلى فاتورة الشحن.  
1. انقر فوق "معلومات ذات صلة".
2. انقر فوق "تفاصيل فاتورة الشحن".
3. انقر فوق "إنشاء كمبيالة/فاتورة الشحن".
4. في الحقل "الفاتورة"، اكتب قيمة.
5. انقر فوق "موافق".

## <a name="reconcile-the-invoice"></a>تسوية الفاتورة
    * عند تسوية فاتورة الشركة وفاتورة الشحن، يتم ذلك كل بند بعد الآخر.  
1. انقر فوق "مطابقة فواتير الشحن والفواتير".
2. قم بتوسيع المقطع "تفاصيل الفاتورة".
3. قم بتوسيع المقطع "تفاصيل فاتورة الشحن غير المطابقة‬".
4. في القائمة، قم بوضع علامة للصف المحدد.
5. انقر فوق "مطابقة".
6. قم بتوسيع المقطع "تفاصيل فاتورة الشحن المطابقة‬".

## <a name="submit-the-invoice-for-approval"></a>تقديم الفاتورة للاعتماد
1. انقر فوق "إرسال" للموافقة.
2. قم بإغلاق الصفحة.
3. امسح تحديد خانة الاختيار "إخفاء الموافقة‬". 
4. انقر فوق "دفاتر يومية فاتورة المورّد".
5. انقر لمتابعة الارتباط الوارد في الحقل "رقم دفتر يومية المرجع‬".
6. انقر فوق البنود.


