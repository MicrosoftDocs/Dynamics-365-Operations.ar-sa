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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="343b0-103">يتم ترحيل استحقاق الشراء الذي له مبلغ صفر لإيصال استلام المنتجات بقيمة صفر</span><span class="sxs-lookup"><span data-stu-id="343b0-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="343b0-104">رقم KB: 4612588</span><span class="sxs-lookup"><span data-stu-id="343b0-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="343b0-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="343b0-105">Symptoms</span></span>

<span data-ttu-id="343b0-106">عند ترحيل إيصال استلام المنتجات الذي يحتوي على قيمة صفر، يقوم النظام بإنشاء ترحيل لاستحقاق الشراء حيث يكون المبلغ هو 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="343b0-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="343b0-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="343b0-107">Resolution</span></span>

<span data-ttu-id="343b0-108">وبشكل افتراضي، لعمليات ترحيل دفتر الأستاذ لنوع *الشراء، استحقاق*، يتم تعيين الحقل دائمًا `IsTransferredIndetail` على *الملخص* في حركات دفتر الأستاذ الفرعي.</span><span class="sxs-lookup"><span data-stu-id="343b0-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="343b0-109">وبالتالي، يقوم النظام بإنشاء إدخال الإيصال ذات الصلة حتى إذا كان المبلغ يساوي 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="343b0-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="343b0-110">لتخطي هذا النوع من الترحيل عندما يكون المبلغ 0 (صفر)، قم بتوسيع الطريقة `subledgerJournalizer.markDoNotTransferEntries` بحيث تتضمن `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`، كما هو موضح في المثال التالي.</span><span class="sxs-lookup"><span data-stu-id="343b0-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
