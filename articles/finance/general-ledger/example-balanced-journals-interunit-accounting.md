---
title: دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات
description: توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a926adcc631ec286f37796713466eb0144494c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818382"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="792c4-103">دفاتر اليومية التي تمت موازنتها للمحاسبة بين الوحدات</span><span class="sxs-lookup"><span data-stu-id="792c4-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="792c4-104">توضح هذه المقالة كيفية موازنة دفتر اليومية بشكل تلقائي عند تحديد بعد مالي للموازنة في صفحة دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="792c4-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="792c4-105">وإذا لم تتم موازنة الإدخالات المحاسبية على مستوى قيم البُعد المالي، يتم إنشاء إدخالات محاسبية إضافية تلقائيًا لموازنة دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="792c4-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="792c4-106">وتستخدم إدخالات الحساب هذه نوعي الترحيل **بين الوحدات - المدين** و **بين الوحدات - الدائن** في صفحة **حسابات للحركات التلقائية** لتحديد الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="792c4-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="792c4-107">على سبيل المثال، تم تحديد وحدة الأعمال، التي هي الجزء الثاني من حساب دفتر الأستاذ، بوصفها البعد المالي للموازنة، والقيود المحاسبية التالية على وشك أن يتم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="792c4-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| <span data-ttu-id="792c4-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="792c4-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="792c4-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="792c4-109">100.00 DR</span></span> |
| <span data-ttu-id="792c4-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="792c4-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="792c4-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="792c4-111">100.00 DR</span></span> |
| <span data-ttu-id="792c4-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="792c4-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="792c4-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="792c4-113">200.00 CR</span></span> |

<span data-ttu-id="792c4-114">وفي هذه الحالة، تم تحديد الأرصدة التالية:</span><span class="sxs-lookup"><span data-stu-id="792c4-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="792c4-115">لوحدة الأعمال MSP‏ = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="792c4-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="792c4-116">لوحدة الأعمال NY‏ = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="792c4-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="792c4-117">ولذلك، يتم إنشاء الإدخالات المحاسبية التالية تلقائيًا لموازنة هذا الإدخال على مستوى قيم البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="792c4-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| <span data-ttu-id="792c4-118">(المدين بين الوحدات) – MSP‏ – OU\_256</span><span class="sxs-lookup"><span data-stu-id="792c4-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="792c4-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="792c4-119">100.00 DR</span></span> |
| <span data-ttu-id="792c4-120">(الدائن بين الوحدات) – NY‏ – OU\_249</span><span class="sxs-lookup"><span data-stu-id="792c4-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="792c4-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="792c4-121">100.00 CR</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]