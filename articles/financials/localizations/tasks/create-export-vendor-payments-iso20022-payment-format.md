--- 
title: "إنشاء وتصدير دفعات المورّد باستخدام تنسيق الدفع ISO20022"
description: "يوضح هذا الإجراء كيفية إنشاء بنود الدفع في دفتر يومية دفع المورّد وإنشاء ملف دفع المورّد باستخدام مثال تحوي الائتمان ISO2022."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>إنشاء وتصدير دفعات المورّد باستخدام تنسيق الدفع ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء بنود الدفع في دفتر يومية دفع المورّد وإنشاء ملف دفع المورّد باستخدام مثال تحوي الائتمان ISO2022. 

شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.

هذا هو الإجراء الخامس من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="create-payment-lines"></a>إنشاء بنود الدفع
1. انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.
2. انقر فوق "جديد".
3. في القائمة، قم بوضع علامة للصف المحدد.
4. في الحقل "الاسم"، أدخل قيمة أو حددها.
5. انقر فوق البنود.
6. انقر فوق "مقترح الدفع".
7. انقر فوق "إنشاء مقترح دفع".
8. وسّع المقطع "السجلات المطلوب تضمينها‬".
9. انقر فوق "عامل التصفية".
10. في القائمة، حدد الصف الخاص بجدول "المورّدون" وحقل "حساب المورّد".
11. في الحقل "المعايير‬"، أدخل قيمة أو حددها.
    * يمكنك تطبيق أي معايير لتحديد حركات المورّد للدفع، لهذا لمثال استخدم DE-001 كحساب مورّد.  
12. انقر فوق "موافق".
13. انقر فوق "موافق".
14. انقر فوق "إنشاء مدفوعات".

## <a name="generate-an-iso20022-payment-file"></a>إنشاء ملف دفع ISO20022


