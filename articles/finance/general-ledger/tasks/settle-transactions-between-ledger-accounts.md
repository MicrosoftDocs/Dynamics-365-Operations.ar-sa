---
title: تسوية الحركات بين حسابات دفتر الأستاذ
description: يوضح هذا الإجراء كيفية تسوية الحركات بين حسابات دفتر الأستاذ أو إلغاء إحدى تسويات دفتر الأستاذ.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994405"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="279a0-103">تسوية الحركات بين حسابات دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="279a0-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="279a0-104">يوضح هذا الإجراء كيفية تسوية الحركات بين حسابات دفتر الأستاذ أو إلغاء إحدى تسويات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="279a0-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="279a0-105">ويستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="279a0-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="279a0-106">تسوية الحركة بين حسابات دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="279a0-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="279a0-107">انتقل إلى دفتر الأستاذ العام > المهام الدورية > تسويات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="279a0-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="279a0-108">في القائمة، ابحث عن الحركة التي ترغب في تسويتها.</span><span class="sxs-lookup"><span data-stu-id="279a0-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="279a0-109">يجب أن يكون رصيد المبلغ أكبر من الصفر.</span><span class="sxs-lookup"><span data-stu-id="279a0-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="279a0-110">انقر فوق تضمين.</span><span class="sxs-lookup"><span data-stu-id="279a0-110">Click Include.</span></span>
4. <span data-ttu-id="279a0-111">انقر فوق "قبول".</span><span class="sxs-lookup"><span data-stu-id="279a0-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="279a0-112">إلغاء تسوية دفتر الأستاذ</span><span class="sxs-lookup"><span data-stu-id="279a0-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="279a0-113">انتقل إلى دفتر الأستاذ العام > الاستعلامات والتقارير > ميزان المراجعة.</span><span class="sxs-lookup"><span data-stu-id="279a0-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="279a0-114">انقر فوق "المعلمات" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="279a0-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="279a0-115">انقر فوق تحديث.</span><span class="sxs-lookup"><span data-stu-id="279a0-115">Click Update.</span></span>
4. <span data-ttu-id="279a0-116">في القائمة، ابحث عن الحساب الذي يحتوي على الحركة التي تمت تسويتها.</span><span class="sxs-lookup"><span data-stu-id="279a0-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="279a0-117">انقر فوق "جميع الحركات".</span><span class="sxs-lookup"><span data-stu-id="279a0-117">Click All transactions.</span></span>
6. <span data-ttu-id="279a0-118">استخدم عامل تصفية للبحث عن الحركة في القائمة بسهولة.</span><span class="sxs-lookup"><span data-stu-id="279a0-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="279a0-119">انقر فوق "تسويات دفتر الأستاذ".</span><span class="sxs-lookup"><span data-stu-id="279a0-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="279a0-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="279a0-120">In the list, mark the selected row.</span></span>

