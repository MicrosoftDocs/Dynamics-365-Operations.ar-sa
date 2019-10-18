---
title: " تدقيق الفواتير والبيانات الأساسية في نظام الحسابات الدائنة "
description: عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6e8967fe4db67ff98fc7093792bdb82b73a33d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176172"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a> تدقيق الفواتير والبيانات الأساسية في نظام الحسابات الدائنة 

[!include [task guide banner](../../includes/task-guide-banner.md)]

عندما تتلقى فاتورة من مورّد للبضائع أو الخدمات على أمر شراء، قد تتطلب العمليات التجارية تلقي البضائع أو الخدمات قبل اعتماد الفاتورة للدفع. قبل أن تبدأ، تأكد من تحديد مفتاح تكوين مطابقة الفاتورة. 

في صفحة "محددات الحسابات الدائنة"، تأكد من تحديد الخيار "تمكين التحقق من صحة مطابقة الفاتورة‬"، ومن تعيين الحقل "ترحيل الفاتورة التي بها اختلافات إلى "طلب موافقة‬" ومن تعيين الحقل "سياسة مطابقة البند" إلى "سياسة المطابقة الثلاثية‬".

يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF. قد ينفذ دور مدير الحسابات الدائنة أو دور مدير الحسابات‬ هذه الخطوات.


## <a name="create-a-purchase-order"></a>إنشاء أمر شراء
1. انتقل إلى **كافة أوامر الشراء**.
2. انقر فوق **جديد**.
3. في حقل **حساب المورّد**، اكتب قيمة.
4. وانقر فوق **موافق**.
5. انقر فوق **إضافة بند**.
6. في حقل **رقم الصنف**، اكتب قيمة.
7. في جزء الإجراءات، انقر فوق **شراء‬**.
8. انقر فوق **تأكيد**.

## <a name="post-a-product-receipt"></a>ترحيل إيصال استلام المنتجات
1. في جزء الإجراءات، **انقر فوق استلام**.
2. انقر فوق **إيصال استلام المنتجات**.
3. في حقل **إيصال استلام المنتجات**، اكتب قيمة.
4. وانقر فوق **موافق**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>تسجيل فاتورة مورّد ومطابقتها مع إيصالات استلام المنتجات
1. في جزء الإجراءات، انقر فوق **فاتورة > فاتورة**.
2. في حقل **الرقم**، اكتب قيمة.
3. انقر فوق **افتراضي من: الكمية المطلوبة** لفتح مربع حوار الإسقاط.
4. في حقل **الكمية الافتراضية للبنود**، حدد خيارًا.
5. وانقر فوق **موافق**.
6. انقر فوق **نعم**.
7. انقر فوق **مطابقة إيصالات استلام المنتجات**.
8. وانقر فوق **موافق**.
9. في جزء الإجراءات، انقر فوق **مراجعة**.
10. انقر فوق **تفاصيل المطابقة**.
