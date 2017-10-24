---
title: "دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات"
description: "توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="76b1b-103">دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات</span><span class="sxs-lookup"><span data-stu-id="76b1b-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="76b1b-104">توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="76b1b-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="76b1b-105">وإذا لم تتم موازنة الإدخالات المحاسبية على مستوى قيم البُعد المالي، يتم إنشاء إدخالات محاسبية إضافية تلقائيًا لموازنة دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="76b1b-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="76b1b-106">وتستخدم إدخالات الحساب هذه نوعي الترحيل **بين الوحدات - المدين** و**بين الوحدات - الدائن** في صفحة **حسابات للحركات التلقائية** لتحديد الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="76b1b-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="76b1b-107">على سبيل المثال، تم تحديد الفرع، الذي هو الجزء الثاني من حساب دفتر الأستاذ، بوصفه البعد المالي للموازنة، والقيود المحاسبية التالية على وشك أن يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="76b1b-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="76b1b-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="76b1b-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="76b1b-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="76b1b-109">100.00 DR</span></span> |
| <span data-ttu-id="76b1b-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="76b1b-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="76b1b-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="76b1b-111">100.00 DR</span></span> |
| <span data-ttu-id="76b1b-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="76b1b-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="76b1b-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="76b1b-113">200.00 CR</span></span> |

<span data-ttu-id="76b1b-114">وفي هذه الحالة، تم تحديد الأرصدة التالية:</span><span class="sxs-lookup"><span data-stu-id="76b1b-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="76b1b-115">بالنسبة لفرع الرياض = 100.00 ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="76b1b-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="76b1b-116">بالنسبة لفرع نيويورك = 100.00 دولار</span><span class="sxs-lookup"><span data-stu-id="76b1b-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="76b1b-117">ولذلك، يتم إنشاء الإدخالات المحاسبية التالية تلقائيًا لموازنة هذا الإدخال على مستوى قيم البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="76b1b-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="76b1b-118">(المدين بين الوحدات) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="76b1b-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="76b1b-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="76b1b-119">100.00 DR</span></span> |
| <span data-ttu-id="76b1b-120">(الدائن بين الوحدات) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="76b1b-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="76b1b-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="76b1b-121">100.00 CR</span></span> |






