---
title: تسوية شيك بتاريخ لاحق لمورد
description: قم بتسوية الشيك الذي تم إصداره بتاريخ لاحق إلى المورد عند قيام البنك بتسوية حركة الشيك بعد أن يصبح الشيك متأخرًا وتتم تسويته من قبل البنك.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08cf4ec805e632470ef778f31beb87597e0ca096
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976181"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>تسوية شيك بتاريخ لاحق لمورد

[!include [banner](../../includes/banner.md)]

قم بتسوية الشيك الذي تم إصداره بتاريخ لاحق إلى المورد عند قيام البنك بتسوية حركة الشيك بعد أن يصبح الشيك متأخرًا وتتم تسويته من قبل البنك. 

قم باستكمال الإجراءات التالية قبل البدء في هذا الإجراء.

1) إعداد شيكات بتاريخ لاحق

2) تسجيل شيك بتاريخ لاحق لمورد وترحيله



ويتمثل دور هذا الإجراء في أمين الخزانة. يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى الحسابات الدائنة > المدفوعات > ‏‫شيكات الموردين بتواريخ لاحقة.
2. انقر فوق "تسوية".
3. انقر فوق "تسوية إدخالات التسوية".
    * قم بتسوية حساب المورد لحركة الشيك.  
4. قم بإغلاق الصفحة.
5. انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.
6. في حقل "إظهار"، حدد "الكل".
7. حدد خانة اختيار "إظهار العناصر التي أنشاها المستخدم فقط" أو قم بإلغاء تحديدها.
8. في القائمة، قم بوضع علامة للصف المحدد.
9. انقر فوق البنود.
10. انقر فوق "الإيصال".
11. قم بإغلاق الصفحة.

