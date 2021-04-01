---
title: توزيعات العمليات
description: توفر هذه المقالة معلومات حول عمليات التخصيص والخيارات الخاصة بمعالجتها في Dynamics 365 FinanceMicrosoft، وكيف يمكن استخدامها في تخطيط الموازنة. تستخدم عمليات التخصيص لتوزيع مبالغ عبر مجموعات متعددة من حسابات دفتر الأستاذ. وهي تساعد على ضمان تحميل النفقات أو الإيرادات للكائن الصحيح في المحاسبة.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13496e764f907201a23f0dd6772ee22efffb250
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204968"
---
# <a name="process-allocations"></a><span data-ttu-id="eca56-105">توزيعات العمليات</span><span class="sxs-lookup"><span data-stu-id="eca56-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eca56-106">توفر هذه المقالة معلومات حول عمليات التخصيص والخيارات الخاصة بمعالجتها، وكيف يمكن استخدامها في تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="eca56-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="eca56-107">تستخدم عمليات التخصيص لتوزيع مبالغ عبر مجموعات متعددة من حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="eca56-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="eca56-108">وهي تساعد على ضمان تحميل النفقات أو الإيرادات للكائن الصحيح في المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="eca56-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="eca56-109">تدعم الإمكانيات التالية هذه العملية:</span><span class="sxs-lookup"><span data-stu-id="eca56-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="eca56-110">قم يدويًا بتوزيع مبالغ الحركات باستخدام إجراء التقسيم في التوزيعات المحاسبية، أو عن طريق تطبيق القوالب الافتراضية للأبعاد المالية على مستند.</span><span class="sxs-lookup"><span data-stu-id="eca56-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="eca56-111">ولمزيد من المعلومات، راجع [التوزيعات المحاسبية](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="eca56-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="eca56-112">قم تلقائيًا بتوزيع مبالغ الحركات استناداً إلى مدة التوزيع المحددة في حساب رئيسي فردي.</span><span class="sxs-lookup"><span data-stu-id="eca56-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="eca56-113">وسيتم إنشاء إدخالات حساب التوزيع لكل دفتر يومية استناداً إلى حساب دفتر أستاذ الوجهة والنسبة المئوية حيث يفي إدخال المحاسبة بالمعايير المحددة باعتبارها حساب دفتر الأستاذ المصدر.</span><span class="sxs-lookup"><span data-stu-id="eca56-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="eca56-114">لمزيد من المعلومات، راجع [شروط التوزيع على حساب رئيسي](../general-ledger/main-account-allocation-terms.md).</span><span class="sxs-lookup"><span data-stu-id="eca56-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="eca56-115">قم تلقائيًا بتوزيع أرصدة دفتر الأستاذ أو المبالغ الثابتة استناداً إلى قواعد توزيع دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="eca56-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="eca56-116">تتم معالجة قواعد توزيع دفتر الأستاذ على أساس دوري باستخدام دفاتر يومية التوزيع.</span><span class="sxs-lookup"><span data-stu-id="eca56-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="eca56-117">لمزيد من المعلومات، راجع [قواعد التوزيع](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="eca56-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="eca56-118">التوزيعات في تخطيط الموازنة</span><span class="sxs-lookup"><span data-stu-id="eca56-118">Allocations in budget planning</span></span>

<span data-ttu-id="eca56-119">يمكن استخدام قواعد توزيع دفتر الأستاذ لخطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="eca56-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="eca56-120">عند استخدام قواعد توزيع دفتر الأستاذ في تخطيط الموازنة، تعمل قواعد التوزيع بنفس الطريقة المتبعة في دفتر الأستاذ، ولكن تأتي البيانات المصدر والبيانات الوجهة من خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="eca56-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="eca56-121">يمكنك تحديد قواعد توزيع دفتر الأستاذ لاستخدامها بخطط الموازنة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="eca56-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="eca56-122">بدلاً من ذلك، يمكنك استخدام جدول توزيع يتم تشغيله كجزء من عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="eca56-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="eca56-123">يمكنك استخدام قواعد توزيع دفتر الأستاذ بين الشركات الشقيقة لتخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="eca56-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]