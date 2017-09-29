--- 
title: "معالجة الخصومات للدفع"
description: "يوضح هذا الإجراء كيفية تحويل خصومات العميل المعتمدة التي تمت معالجتها لإشعارات دائنة."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 73bfc08115a9727cbdcbe9b37e1427e67341dbd8
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="process-rebates-for-payment"></a>معالجة الخصومات للدفع

[!include[task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية تحويل خصومات العميل المعتمدة التي تمت معالجتها لإشعارات دائنة. يمكن استخدام هذا الدليل في شركة العرض التقديمي USMF. الشرط المسبق لهذا الدليل هو وجود مطالبة واحدة أو أكثر من مطالبات الخصم في حالة"تمييز". إذا كنت تستخدم USMF، يجب عليك تشغيل الدليل "إنشاء خصومات العميل ومعالجتها" قبل تشغيل في هذا الدليل.


## <a name="convert-rebate-claims-to-credit-note"></a>تحويل مطالبات الخصم لإشعار دائن
1. انتقل إلى "جميع العملاء".
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
4. في جزء الإجراءات، انقر فوق "تحصيل".
5. انقر فوق "تسوية الحركات".
6. انقر فوق "الوظائف".
7. انقر فوق "برنامج الخصم".
    * تسرد صفحة الخصومات قائمة بمطالبات الخصم التي قمت بمعالجتها في منضدة عمل خصم العميل والتي تكون في حالة "التمييز".    
8. انقر فوق "تحرير".
    * قم بتعيين علامات الاختيار الموجودة في الحقل "تمييز" للمطالبات التي تريد تضمينها في إشعار الدائن.   
9. انقر فوق "الوظائف".
10. انقر فوق "إنشاء إشعار دائن".
    * تظهر رسالة لإعلامك بأنه قد تم ترحيل دفتر يومية (هذا هو دفتر يومية استهلاك الحسابات المدينة، كما هو محدد في صفحة معلمات الحسابات المدينة). يؤدي هذا لنقل مبلغ الالتزام الحقيقي (المبلغ الدائن) إلى رصيد العميل. ويعني هذا أنه تمت إضافة حساب العميل وخصم حساب استحقاق الخصم.  
11. قم بإغلاق الصفحة.
12. انقر فوق "إلغاء".
    * يؤدي هذا لتحديث الصفحة بحيث يمكنك أن ترى التحديثات.  
13. في جزء الإجراءات، انقر فوق "تحصيل".
14. انقر فوق "تسوية الحركات".
    * لاحظ أنه تمت إضافة حركة لمبلغ سالب لرصيد العميل، تمثل إجمالي مبلغ الخصم، دون مرجع فاتورة.   
15. انقر فوق "إلغاء".

