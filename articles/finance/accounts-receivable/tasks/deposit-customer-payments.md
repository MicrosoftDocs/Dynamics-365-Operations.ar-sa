---
title: إيداع مدفوعات العميل
description: إيداع مدفوعات العميل.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 595d1b609ae83af8f1581caeff9ef7d3892a6207
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176270"
---
# <a name="deposit-customer-payments"></a>إيداع مدفوعات العميل

[!include [task guide banner](../../includes/task-guide-banner.md)]

إيداع مدفوعات العميل. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > المدفوعات > دفتر يومية المدفوعات‬**.
2. حدد **جديد**.
3. في حقل **الاسم**، حدد‏‎ **CustPay** في القائمة المنسدلة
4. حدد **البنود**.
5. في الحقل **الحساب**، حدد العميل الذي تقوم بتسجيل الدفعة له.
6. في الحقل **الدائن**، أدخل مبلغ الدفع. يمكنك اختيار ترك المبلغ فارغًا والسماح للنظام بحسابه عن طريق تحديد الفواتير التي تم دفعها.  
7. في حقل **مرجع الدفع**، اكتب قيمة. قد يكون مرجع الدفع رقم الشيك للدفعة التي تقوم بإدخاله. يكون مرجع الدفع مطلوبًا لتضمين الدفعة في إيصال إيداع.  
8. ضع علامة على المربع "استخدام إيصال إيداع‬". إذا كان يجب تضمين الدفع في الإيداع فيمكنك تغيير هذا الإعداد إلى "نعم".  
9. حدد **جديد**.
10. في الحقل **الحساب**، حدد العميل للدفعة التالية.
11. في الحقل **الدائن**، أدخل مبلغ الدفع.
12. في حقل **مرجع الدفع**، اكتب قيمة.
13. ضع علامة على المربع **استخدام إيصال إيداع‬**.
14. حدد **ترحيل**. يجب ترحيل المدفوعات قبل التمكن من إنشاء إيصال الإيداع. وهذا للتأكد من أن المدفوعات لا تتغير بعد إنشاء إيصال الإيداع.  
15. حدد **الوظائف**.
16. حدد **إيصال الإيداع**.
17. حدد **موافق**. يتم استخدام الصفحة الأولى لإنشاء إيصال الإيداع.  
18. حدد **موافق**. تتعلق الخطوة الثانية بطباعة إيصال الإيداع، ولكن هذه الخطوة غير مطلوبة.  

