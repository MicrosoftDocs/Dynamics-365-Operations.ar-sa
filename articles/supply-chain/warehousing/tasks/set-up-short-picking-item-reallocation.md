--- 
title: "إعداد إعادة توزيع الأصناف للانتقاء القصير"
description: "يوضح هذا الإجراء كيفية تمكين العاملين في المستودع من العثور بسرعة على مواقع بديلة في حال عدم وجود مخزون كافٍ في الموقع الذي تم توجيههم إليه."
author: ShylaThompson
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 99a4afb58f0c4beef818fd7c0a6a1837e00638d8
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="97ce8-103">إعداد إعادة توزيع الأصناف للانتقاء القصير</span><span class="sxs-lookup"><span data-stu-id="97ce8-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97ce8-104">يوضح هذا الإجراء كيفية تمكين العاملين في المستودع من العثور بسرعة على مواقع بديلة في حال عدم وجود مخزون كافٍ في الموقع الذي تم توجيههم إليه.</span><span class="sxs-lookup"><span data-stu-id="97ce8-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="97ce8-105">من الممكن استخدام عملية إعادة توزيع تلقائي، تستخدم توجيهات الموقع لاسترداد السلع إذا كانت متوفرة في موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="97ce8-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="97ce8-106">بدلاً من ذلك، عند استخدام إعادة التوزيع اليدوي، يتم عرض قائمة بالمواقع مع الكمية المتوفرة على الجهاز المحمول، مما يسمح لعامل المستودع باختيار الموقع لاستخدام المخزون منه.</span><span class="sxs-lookup"><span data-stu-id="97ce8-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="97ce8-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="97ce8-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="97ce8-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="97ce8-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="97ce8-109">إعداد استثناءات العمل</span><span class="sxs-lookup"><span data-stu-id="97ce8-109">Set up work exceptions</span></span>
1. <span data-ttu-id="97ce8-110">انتقل إلى إدارة المستودعات > الإعداد > العمل > استثناءات العمل.</span><span class="sxs-lookup"><span data-stu-id="97ce8-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="97ce8-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="97ce8-111">Click New.</span></span>
    * <span data-ttu-id="97ce8-112">من الممكن تعريف عدة استثناءات عمل بواسطة سياسات إعادة توزيع أصناف مختلفة لتمكين العامل في المستودع من اختيار واحد بالاستناد إلى احتياجات الشحن التي يقوم بمعالجتها.</span><span class="sxs-lookup"><span data-stu-id="97ce8-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="97ce8-113">في الحقل "كود استثناء العمل‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="97ce8-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="97ce8-114">قم بإعطاء استثناء العمل عنوانًا للإشارة إلى المهمة التي يتم استخدامه من أجلها.</span><span class="sxs-lookup"><span data-stu-id="97ce8-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="97ce8-115">على سبيل المثال، دليل الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="97ce8-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="97ce8-116">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="97ce8-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97ce8-117">في الحقل "نوع الاستثناء"، حدد "انتقاء قصير".</span><span class="sxs-lookup"><span data-stu-id="97ce8-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="97ce8-118">حدد خانة الاختيار "تعديل المخزون".</span><span class="sxs-lookup"><span data-stu-id="97ce8-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="97ce8-119">يعني هذا الخيار أن تسوية المخزون ستتم بشكل تلقائي على 0 في موقع الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="97ce8-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="97ce8-120">في حقل "كود نوع التسوية الافتراضي‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="97ce8-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="97ce8-121">على سبيل المثال، في USMF، يمكنك تحديد "Remove Res Adj Out".</span><span class="sxs-lookup"><span data-stu-id="97ce8-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="97ce8-122">في الحقل "إعادة توزيع الصنف‬"، حدد "يدوي".</span><span class="sxs-lookup"><span data-stu-id="97ce8-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="97ce8-123">إذا قمت بتحديد "يدوي"، أو "تلقائي ويدوي"، يجب تمكين عامل المستودع لاستخدام إعادة التوزيع اليدوي.</span><span class="sxs-lookup"><span data-stu-id="97ce8-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="97ce8-124">إعداد عامل لاستخدام إعادة التوزيع الأصناف يدويًا</span><span class="sxs-lookup"><span data-stu-id="97ce8-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="97ce8-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="97ce8-125">Close the page.</span></span>
2. <span data-ttu-id="97ce8-126">انتقل إلى إدارة المستودعات > الإعداد > العامل.</span><span class="sxs-lookup"><span data-stu-id="97ce8-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="97ce8-127">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="97ce8-127">Click Edit.</span></span>
4. <span data-ttu-id="97ce8-128">في القائمة، حدد العامل 24.</span><span class="sxs-lookup"><span data-stu-id="97ce8-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="97ce8-129">قم بتوسيع مقطع "العمل".</span><span class="sxs-lookup"><span data-stu-id="97ce8-129">Expand the Work section.</span></span>
6. <span data-ttu-id="97ce8-130">حدد "نعم" في حقل "‏‫السماح بإعادة توزيع الأصناف يدويًا‬".</span><span class="sxs-lookup"><span data-stu-id="97ce8-130">Select Yes in the Allow manual item reallocation field.</span></span>


