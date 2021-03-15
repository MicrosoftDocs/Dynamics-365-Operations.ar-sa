---
title: بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام ‏‫دفتر يومية الموافقة
description: يشرح هذا الموضوع كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f19c31a3ca20ad4b11e2529bdcb9db351c37f6c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971868"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>بيانات الفاتورة الرئيسية في الحسابات الدائنة باستخدام ‏‫دفتر يومية الموافقة

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيفية استخدام سجل الفواتير لإنشاء فواتير ثم استخدام دفتر يومية الموافقة لتحديث حسابات المصروفات.

## <a name="create-and-post-and-invoice"></a>إنشاء فاتورة وترحيلها
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > سجل الفواتير**.
2. حدد **جديد**.
3. حدد اسم سجل الفواتير الذي تريد استخدامه.
4. حدد **البنود‬** لفتح السجل وإدخال بنود المصروفات.
5. حدد موردًا. على سبيل المثال، أدخل أو حدد `US-104`.
6. في حقل **الفاتورة**، اكتب قيمة.
7. في حقل **الوصف**، اكتب قيمة.
8. في الحقل **دائن**، أدخل رقمًا.
9. في الحقل **معتمد بواسطة**، حدد معتمدًا من القائمة المنسدلة.
10. حدد **ترحيل**.

## <a name="approve-an-invoice"></a>الموافقة على فاتورة
1. في جزء التنقل، انتقل إلى **الوحدات النمطية > الحسابات الدائنة > الفواتير > الموافقة على الفاتورة**.
2. حدد **جديد**.
3. حدد اسم دفتر يومية الموافقة على الفواتير الذي تريد استخدامه.
4. حدد **البنود** لعرض صفحة حيث يمكنك تحديد الفواتير التي تريد الموافقة عليها.
5. حدد **البحث عن إيصالات** لعرض كافة الفواتير الجاهزة للموافقة عليها.
6. ضع علامة على الفاتورة التي قمت بإنشائها، ثم انقر فوق **تحديد**. يتم نقل الإيصالات التي حددتها أعلاه إلى هذه القائمة بعد تحديدها.  
7. حدد **موافق**.
8. حدد حقل **رقم الحساب** لإضافة حساب مصروفات للفاتورة.
9. أدخل رقم حساب، واضغط على علامة جدولة للخروج من الحقل. على سبيل المثال، أدخل `600120`.
10. حدد **ترحيل**.
11. حدد **الإيصال** لعرض الإدخالات التي تم ترحيلها. يتم عكس حساب "الفاتورة المعلقة للموافقة" واستبداله بحساب المصروفات الفعلية.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]