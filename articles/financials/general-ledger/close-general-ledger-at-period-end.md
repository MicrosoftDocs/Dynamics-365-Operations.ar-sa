---
title: "إقفال دفتر الأستاذ العام في نهاية الفترة"
description: "يوضح هذا الموضوع المهام التي يتم إكمالها عادةً عند تنفيذ إقفال فترة لدفتر الأستاذ العام."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5643a06cb23eedd7c8676ad48be2ad2e78cdfc9b
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="6ec57-103">إقفال دفتر الأستاذ العام في نهاية الفترة</span><span class="sxs-lookup"><span data-stu-id="6ec57-103">Close the general ledger at period end</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ec57-104">يوضح هذا الموضوع المهام التي يتم إكمالها عادةً عند تنفيذ إقفال فترة لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="6ec57-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="6ec57-105">في دفتر الأستاذ العام، يمكنك إكمال إجراءات الإقفال لفترة أو سنة.</span><span class="sxs-lookup"><span data-stu-id="6ec57-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="6ec57-106">وتقوم عمليات الإقفال بإعداد النظام لفترة جديدة.</span><span class="sxs-lookup"><span data-stu-id="6ec57-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="6ec57-107">لإعداد النظام لسنة جديدة، يجب تشغيل عملية إقفال نهاية السنة.</span><span class="sxs-lookup"><span data-stu-id="6ec57-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="6ec57-108">تمتلك كل مؤسسة عمليات وخطوات مختلفة تنفذها في نهاية الفترة.</span><span class="sxs-lookup"><span data-stu-id="6ec57-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="6ec57-109">وفيما يلي بعض الخطوات الاختيارية لانتهاء الفترة:‬</span><span class="sxs-lookup"><span data-stu-id="6ec57-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="6ec57-110">أكمل كافة المهام لكافة الوحدات الأخرى، مثل الحسابات المدينة، والحسابات الدائنة، والمخزون.</span><span class="sxs-lookup"><span data-stu-id="6ec57-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="6ec57-111">التحقق من ترحيل كافة دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="6ec57-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="6ec57-112">تشغيل إعادة تقييم العملة الأجنبية لإنشاء أية مبالغ أرباح أو خسارة غير محققة.</span><span class="sxs-lookup"><span data-stu-id="6ec57-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="6ec57-113">تسوية الحركات لكل حساب دفتر أستاذ.</span><span class="sxs-lookup"><span data-stu-id="6ec57-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="6ec57-114">معالجة أي توزيعات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6ec57-114">Process any required allocations.</span></span>
-   <span data-ttu-id="6ec57-115">ترحيل تسويات نهاية الفترة يدوياً.</span><span class="sxs-lookup"><span data-stu-id="6ec57-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="6ec57-116">تسجيل دفتر يومية الحركات ومراجعة تقرير **دفتر يومية دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="6ec57-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="6ec57-117">تنفيذ تجميع باستخدام شركة تجميع أو إعداد التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="6ec57-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="6ec57-118">إنشاء القوائم المالية نهاية الفترة باستخدام إعداد التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="6ec57-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="6ec57-119">قم بتعيين فترات دفتر الأستاذ إلى **قيد الانتظار**، بحيث لا يحدث أي ترحيل آخر.</span><span class="sxs-lookup"><span data-stu-id="6ec57-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="6ec57-120">كما يمكنك تقييد فترة لمجموعة مستخدمين محددة أثناء حدوث أنشطة نهاية الفترة، للتحكم بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="6ec57-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="6ec57-121">ليست بفكرة جيدة أن يتم تعيين الفترات الزمنية إلى **‏‫تم الإقفال بشكل دائم‬**، لأنه لا يمكنك إعادة فتح فترة تم إقفالها.</span><span class="sxs-lookup"><span data-stu-id="6ec57-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="6ec57-122">يمكن استخدام مساحة عمل إقفال الفترة المالية لتنظيم المهام المطلوبة لمختلف عمليات انتهاء الفترة ولتتبعها.</span><span class="sxs-lookup"><span data-stu-id="6ec57-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="6ec57-123">لمزيد من المعلومات، راجع المواضيع التالية:</span><span class="sxs-lookup"><span data-stu-id="6ec57-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="6ec57-124">مساحة عمل إقفال الفترة المالية</span><span class="sxs-lookup"><span data-stu-id="6ec57-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="6ec57-125">إقفال نهاية السنة</span><span class="sxs-lookup"><span data-stu-id="6ec57-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="6ec57-126">إقفال شامل للفترة المالية</span><span class="sxs-lookup"><span data-stu-id="6ec57-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





