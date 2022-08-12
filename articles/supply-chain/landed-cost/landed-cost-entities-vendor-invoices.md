---
title: كيانات فاتورة المورّد
description: يوفر هذا المقال معلومات حول كيانات فاتورة المورد، والتي تتيح تكوين أكواد أنواع التكلفة للتكاليف الداخلية أو التكاليف المشتقة خارجيًا.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f0371cf9862afaf3bc43a44def725c420e9aaf56
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166732"
---
# <a name="vendor-invoice-entities"></a>كيانات فواتير الموردين

[!include [banner](../includes/banner.md)]

تتيح وحدة **التكلفة شاملة التفريغ** تكوين أكواد نوع التكلفة للتكاليف الداخلية أو التكاليف المشتقة خارجيًا. إذا كانت التكلفة خارج نطاق الأعمال، فمن المتوقع أن تصدر فاتورة من مزود الخدمة. تتم معالجة هذه الفاتورة كدفتر يومية للفواتير يمكن ربطها برحلة، ويمكن توزيع قيمة الفاتورة عبر تكلفة واحدة أو أكثر للرحلة.

تعمل كيانات فاتورة المورد على تمكين تخصيص قيمة بند دفتر اليومية عبر تكلفة واحدة أو أكثر للرحلة التي تشترك في رمز نوع التكلفة نفسه.

يمكن تخصيص التكلفة فقط في حالة وجود بنود دفتر يومية الفاتورة وبنود دفتر يومية الفاتورة.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>تخصيصات تكاليف رحلات الموردين (ITMLedgerJournalCostLinesVoyagesEntity)

يتيح كيان بيانات تخصيصات تكلفة رحلة المورد تخصيص بند فاتورة المورد عبر تكلفة واحدة أو أكثر يتم تطبيقها على منطقة تكلفة الرحلة. هذه الوظيفة مدعومة من قِبل كيان `ITMLedgerJournalCostLinesVoyagesEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| المبلغ الموزّع | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | لا | لا |
| رقم بند حركة التكلفة | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم بند دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **نعم** | لا |
| الرحلة البحرية | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>مخصصات تكاليف حاوية شحن المورد (ITMLedgerJournalCostLinesContainersEntity)

يتيح كيان بيانات تخصيصات تكلفة حاوية شحن المورد تخصيص بند فاتورة المورد عبر تكلفة واحدة أو أكثر يتم تطبيقها على منطقة تكلفة حاوية الشحن. هذه الوظيفة مدعومة من قِبل كيان `ITMLedgerJournalCostLinesContainersEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| المبلغ الموزّع | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | لا | لا |
| حاوية الشحن | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |
| رقم بند حركة التكلفة | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم بند دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **نعم** | لا |
| الرحلة البحرية | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>تخصيصات تكاليف حافظات أوراق الموردين (ITMLedgerJournalCostLinesFoliosEntity)

يتيح كيان بيانات تخصيصات تكلفة حافظة ورق المورد تخصيص بند فاتورة المورد عبر تكلفة واحدة أو أكثر يتم تطبيقها على منطقة تكلفة حافظة الورق. هذه الوظيفة مدعومة من قِبل كيان `ITMLedgerJournalCostLinesFoliosEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| المبلغ الموزّع | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | لا | لا |
| رقم بند حركة التكلفة | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |
| حافظة الأوراق | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |
| رقم بند دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **نعم** | لا |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>تخصيصات تكاليف أوامر شراء الموردين (ITMLedgerJournalCostLinesPurchTableEntity)

يتيح كيان بيانات تخصيصات تكلفة أمر شراء المورد تخصيص بند فاتورة المورد عبر تكلفة واحدة أو أكثر يتم تطبيقها على منطقة تكلفة أمر الشراء. هذه الوظيفة مدعومة من قِبل كيان `ITMLedgerJournalCostLinesPurchTableEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| المبلغ الموزّع | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | لا | لا |
| رقم بند حركة التكلفة | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم بند دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **نعم** | لا |
| أمر شراء | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>تخصيصات تكاليف أصناف الموردين (ITMLedgerJournalCostLinesPurchLineEntity)

يتيح كيان بيانات تخصيصات تكلفة صنف المورد تخصيص بند فاتورة المورد عبر تكلفة واحدة أو أكثر يتم تطبيقها على منطقة تكلفة الصنف. تغطي منطقة تكلفة الصنف التكاليف في بند أمر الشراء. هذه الوظيفة مدعومة من قِبل كيان `ITMLedgerJournalCostLinesPurchLineEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| المبلغ الموزّع | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | لا | لا |
| رقم بند حركة التكلفة | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم بند دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **نعم** | لا |
| أمر شراء | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |
| رقم بند أمر الشراء | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>تخصيصات تكاليف بنود أوامر تحويل الموردين (ITMLedgerJournalCostLinesTransferLineEntity)

يتيح كيان بيانات تخصيصات تكاليف بنود أوامر تحويل الموردين تخصيص بند فاتورة المورد عبر تكلفة واحدة أو أكثر يتم تطبيقها على منطقة تكاليف بنود التحويل. هذه الوظيفة مدعومة من قِبل كيان `ITMLedgerJournalCostLinesTransferLineEntity`. يسرد الجدول التالي الحقول والتعيينات التي تشكل هذا الكيان.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| المبلغ الموزّع | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | لا | لا |
| رقم بند حركة التكلفة | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم بند دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **نعم** | لا |
| رقم دفتر اليومية | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **نعم** | لا |
| أمر التحويل | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **نعم** | لا |
| رقم بند أمر التحويل | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **نعم** | لا |

### <a name="reference-table"></a>جدول المراجع

ترتبط بنود تكاليف الرحلات ارتباطًا مباشرًا بسجل حركات التكلفة. يتضمن هذا السجل قيمة **معرّف الجدول المرجعي**. هذه القيمة فريدة لكل منطقة تكلفة (الرحلة، وحاوية الشحن، وما إلى ذلك). عند الإشارة إلى أرقام جدول محددة للبيانات التي تم إنشاؤها باستخدام كيانات البيانات، يتم تقسيم الكيانات بناءً على قيم **معرّف الجدول المرجعي**.

قيم الجدول المرجعي (`RefTableId`) ونوع الحركة (`TransType`) ضمنية في اختيار إما كيان بند شراء تكلفة الأرض أو بند تحويل التكلفة شاملة التفريغ.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>بنود دفتر يومية فاتورة المورد (VendorInvoiceJournalLineEntity)

قبل تخصيص قيمة بند دفتر اليومية لتكلفة واحدة أو أكثر في وحدة **التكلفة شاملة التفريغ**، يجب أن يكون بند دفتر اليومية مرتبطًا بمنطقة التكلفة. لدعم هذه الوظيفة، تضيف وحدة **التكلفة شاملة التفريغ** بعض الحقول الجديدة إلى جدول بنود دفتر اليومية (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>تمت إضافة الحقول إلى كيان بند دفتر يومية فاتورة المورد

يسرد الجدول التالي الحقول التي تضيفها وحدة **التكلفة شاملة التفريغ** إلى كيان بند دفتر يومية فاتورة المورد (`VendorInvoiceJournalLineEntity`). تُمكّن هذه الحقول النظام من إنشاء بنود دفتر اليومية وتخصيص التكاليف مقابلها.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| منطقة التكلفة | LedgerJournalTrans.ITMCostArea | الفترة | لا | لا |
| كود نوع التكلفة | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | لا | لا |

### <a name="mainoffset-account"></a>الحساب المقابل/الرئيسي

يتم تحديد الحساب المقابل/الرئيسي لبند دفتر يومية الفاتورة المرتبط برحلة التكلفة شاملة التفريغ بواسطة رمز نوع التكلفة. عندما يتم تضمين رمز نوع التكلفة في بند دفتر يومية الفاتورة، فسيتم استخدام الحساب المقابل للرمز إما كحساب رئيسي أو حساب مقابل، اعتمادًا على السيناريو:

- **دفتر اليومية ذو البند الواحد** – إذا تم تحديد حساب رئيسي (بمعنى آخر، حساب المورد)، وتم توفير رمز نوع التكلفة، فسيتم إدخال قيمة الحساب المقابل لكود نوع التكلفة هذا في الحساب المقابل.
- **دفتر يومية ذو البنود المتعددة** – إذا تم تحديد حساب رئيسي، وتم توفير رمز نوع التكلفة، فسيتم إدخال قيمة حساب المقاصة لرمز نوع التكلفة هذا في الحساب الرئيسي. لن يشير بند دفتر اليومية الذي يمنح المورّد إلى رمز نوع التكلفة.

## <a name="sequencing"></a>التسلسل

بسبب التبعيات بين جداول بنود دفتر اليومية ودفتر اليومية، يجب إنشاء سجل الرحلة أولاً. لا يمكن إنشاء بنود الرحلات إلا بعد إنشاء الرحلة وحاوية الشحن وحاويات الأوراق.

لتخصيص فاتورة رحلة، يجب على النظام معالجة الكيانات بالترتيب التالي:

1. رأس دفتر يومية الفواتير (`VendInvoiceJournalHeaderEntity`)
1. بند دفتر يومية الفاتورة (`VendInvoiceJournalLineEntity`)
1. تخصيصات التكلفة شاملة التفريغ (`ITMLedgerJournalEntities`)
