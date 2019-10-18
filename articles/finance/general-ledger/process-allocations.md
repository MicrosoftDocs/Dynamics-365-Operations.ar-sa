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
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf889169357ea0598a3fe24b09a6eb565209b9c0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186338"
---
# <a name="process-allocations"></a><span data-ttu-id="46dfd-105">توزيعات العمليات</span><span class="sxs-lookup"><span data-stu-id="46dfd-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46dfd-106">توفر هذه المقالة معلومات حول عمليات التخصيص والخيارات الخاصة بمعالجتها، وكيف يمكن استخدامها في تخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="46dfd-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="46dfd-107">تستخدم عمليات التخصيص لتوزيع مبالغ عبر مجموعات متعددة من حسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="46dfd-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="46dfd-108">وهي تساعد على ضمان تحميل النفقات أو الإيرادات للكائن الصحيح في المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="46dfd-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="46dfd-109">تدعم الإمكانيات التالية هذه العملية:</span><span class="sxs-lookup"><span data-stu-id="46dfd-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="46dfd-110">قم يدويًا بتوزيع مبالغ الحركات باستخدام إجراء التقسيم في التوزيعات المحاسبية، أو عن طريق تطبيق القوالب الافتراضية للأبعاد المالية على مستند.</span><span class="sxs-lookup"><span data-stu-id="46dfd-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="46dfd-111">ولمزيد من المعلومات، راجع [التوزيعات المحاسبية.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="46dfd-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="46dfd-112">قم تلقائيًا بتوزيع مبالغ الحركات استناداً إلى مدة التوزيع المحددة في حساب رئيسي فردي.</span><span class="sxs-lookup"><span data-stu-id="46dfd-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="46dfd-113">وسيتم إنشاء إدخالات حساب التوزيع لكل دفتر يومية استناداً إلى حساب دفتر أستاذ الوجهة والنسبة المئوية حيث يفي إدخال المحاسبة بالمعايير المحددة باعتبارها حساب دفتر الأستاذ المصدر.</span><span class="sxs-lookup"><span data-stu-id="46dfd-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="46dfd-114">قم تلقائيًا بتوزيع أرصدة دفتر الأستاذ أو المبالغ الثابتة استناداً إلى قواعد توزيع دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="46dfd-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="46dfd-115">تتم معالجة قواعد توزيع دفتر الأستاذ على أساس دوري باستخدام دفاتر يومية التوزيع.</span><span class="sxs-lookup"><span data-stu-id="46dfd-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="46dfd-116">التوزيعات في تخطيط الموازنة</span><span class="sxs-lookup"><span data-stu-id="46dfd-116">Allocations in budget planning</span></span>

<span data-ttu-id="46dfd-117">يمكن استخدام قواعد توزيع دفتر الأستاذ لخطط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="46dfd-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="46dfd-118">عند استخدام قواعد توزيع دفتر الأستاذ في تخطيط الموازنة، تعمل قواعد التوزيع بنفس الطريقة المتبعة في دفتر الأستاذ، ولكن تأتي البيانات المصدر والبيانات الوجهة من خطة الموازنة.</span><span class="sxs-lookup"><span data-stu-id="46dfd-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="46dfd-119">يمكنك تحديد قواعد توزيع دفتر الأستاذ لاستخدامها بخطط الموازنة يدويًا.</span><span class="sxs-lookup"><span data-stu-id="46dfd-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="46dfd-120">بدلاً من ذلك، يمكنك استخدام جدول توزيع يتم تشغيله كجزء من عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="46dfd-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="46dfd-121">يمكنك استخدام قواعد توزيع دفتر الأستاذ بين الشركات الشقيقة لتخطيط الموازنة.</span><span class="sxs-lookup"><span data-stu-id="46dfd-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>





