---
title: يتم ترحيل استحقاق الشراء الذي له مبلغ صفر لإيصال استلام المنتجات بقيمة صفر
description: عند ترحيل إيصال استلام المنتجات الذي يحتوي على قيمة صفر، يقوم النظام بإنشاء ترحيل لاستحقاق الشراء حيث يكون المبلغ هو 0 (صفر).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026251"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>يتم ترحيل استحقاق الشراء الذي له مبلغ صفر لإيصال استلام المنتجات بقيمة صفر

رقم KB: 4612588

## <a name="symptoms"></a>العلامات

عند ترحيل إيصال استلام المنتجات الذي يحتوي على قيمة صفر، يقوم النظام بإنشاء ترحيل لاستحقاق الشراء حيث يكون المبلغ هو 0 (صفر).

## <a name="resolution"></a>الدقة

وبشكل افتراضي، لعمليات ترحيل دفتر الأستاذ لنوع *الشراء، استحقاق*، يتم تعيين الحقل دائمًا `IsTransferredIndetail` على *الملخص* في حركات دفتر الأستاذ الفرعي. وبالتالي، يقوم النظام بإنشاء إدخال الإيصال ذات الصلة حتى إذا كان المبلغ يساوي 0 (صفر).

لتخطي هذا النوع من الترحيل عندما يكون المبلغ 0 (صفر)، قم بتوسيع الطريقة `subledgerJournalizer.markDoNotTransferEntries` بحيث تتضمن `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`، كما هو موضح في المثال التالي.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
