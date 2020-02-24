---
title: ترحيل الدفعات والمبيعات على الإنترنت
description: يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf7f72be22539271649aa7f5541735b3d24dab66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021464"
---
# <a name="posting-of-online-sales-and-payments"></a>ترحيل الدفعات والمبيعات على الإنترنت

[!include[task guide banner](../includes/task-guide-banner.md)]

يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت.

إن ترحيل المبيعات والمدفوعات عبر الإنترنت عبارة عن عملية من مرحلتين.

- سحب بيانات حركه التجارة عبر الإنترنت إلى HQ.
- مزامنة الأوامر لإنشاء أوامر بيع في HQ.

يمكن سحب بيانات حركه عبر الإنترنت إما عن طريق تشغيل الوظيفة P يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.

### <a name="manually-running-the-p-job"></a>تشغيل الوظيفة P يدويًا

1. انتقل إلى كافة مساحات العمل > تكنولوجيات المعلومات للبيع بالتجزئة والتجارة.
2. انقر فوق جدول التوزيع.
3. حدد P-0001.
4. اضبط مجموعات قواعد بيانات القنوات، إذا كان ذلك مطلوبًا.
5. انقر فوق تشغيل الآن.
6. انقر فوق نعم.

### <a name="scheduling-a-recurring-p-job"></a>جدولة وظيفة P متكررة

1. انتقل إلى كافة مساحات العمل > تكنولوجيات المعلومات للبيع بالتجزئة والتجارة.
2. انقر فوق جدول التوزيع.
3. حدد P-0001.
4. انقر فوق "إنشاء وظيفة دفعية".
5. انقر فوق "تشغيل في الخلفية".
5. مكّن "معالجة الدُفعات".
6. انقر فوق "تكرار".
7. حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".
8. في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق. يكون هذا عادةً 5-10.
9. انقر فوق موافق.
10. انقر فوق موافق.

يمكن مزامنة الأوامر إما عن طريق تشغيل وظيفة "مزامنة الأوامر" يدويًا أو عن طريق إنشاء وظيفة دفعية متكررة.

### <a name="manually-running-order-synchronization"></a>تشغيل مزامنة الأوامر يدويًا 

اتبع هذه الخطوات لتشغيل وظيفة "مزامنة الأوامر" يدويًا مرة واحدة.

1. انتقل إلى كافة مساحات العمل > ماليات المتاجر.
2. انقر فوق مزامنة الأوامر.
3. في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "المتاجر حسب المنطقة".
    * حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.  
    * انقر فوق السهم لإضافة التحديد الخاص بك.  
4. انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".
5. تعطيل معالجة الدُفعات
6. انقر فوق "تكرار".
7. حدد الخيار "انتهاء بعد"
8. في الحقل "انتهاء بعد"، أدخل 1.
9. انقر فوق موافق.
10. انقر فوق موافق.

### <a name="scheduling-recurring-order-synchronization"></a>جدولة مزامنة الأوامر المتكررة

يتناول هذا الإجراء تكوين وظيفة دفعية متكررة وتشغيلها لإنشاء أوامر الشراء والمدفوعات لحركات المتجر على الإنترنت. ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.

1. انتقل إلى كافة مساحات العمل > ماليات المتاجر.
2. انقر فوق مزامنة الأوامر.
3. في حقل "‏‫التدرج الهرمي للمؤسسات‬"، حدد "المتاجر حسب المنطقة".
    * حدد إما متجر معين على الإنترنت أو حدد عقدة إذا أردت إنشاء وظيفة دفعية لمجموعة من المتاجر.  
    * انقر فوق السهم لإضافة التحديد الخاص بك.  
4. انقر فوق علامة التبويب "‏‫تشغيل في الخلفية".
5. تمكين معالجة الدُفعات
6. انقر فوق "تكرار".
7. حدد الخيار "‏‫لا يوجد تاريخ انتهاء‬".
8. في حقل "الجرد"، أدخل الفاصل بين عمليات التشغيل بالدقائق. يكون هذا عادةً 2-20
9. انقر فوق موافق.
10. انقر فوق موافق.

## <a name="data-entities-involved-in-the-process"></a>كيانات البيانات المشمولة في العملية

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
