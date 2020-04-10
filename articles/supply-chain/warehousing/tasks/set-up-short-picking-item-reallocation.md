---
title: إعداد إعادة توزيع الأصناف للانتقاء القصير
description: يوضح هذا الإجراء كيفية تمكين العاملين في المستودع من العثور بسرعة على مواقع بديلة في حال عدم وجود مخزون كافٍ في الموقع الذي تم توجيههم إليه.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eae86b307ac8d8539c3897293c2fc21ea57d2d60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148229"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="a5e2b-103">إعداد إعادة توزيع الأصناف للانتقاء القصير</span><span class="sxs-lookup"><span data-stu-id="a5e2b-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5e2b-104">يوضح هذا الإجراء كيفية تمكين العاملين في المستودع من العثور بسرعة على مواقع بديلة في حال عدم وجود مخزون كافٍ في الموقع الذي تم توجيههم إليه.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn't sufficient inventory at the location they've been directed to.</span></span> <span data-ttu-id="a5e2b-105">من الممكن استخدام عملية إعادة توزيع تلقائي، تستخدم توجيهات الموقع لاسترداد السلع إذا كانت متوفرة في موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-105">It's possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they're available at another location.</span></span> <span data-ttu-id="a5e2b-106">بدلاً من ذلك، عند استخدام إعادة التوزيع اليدوي، يتم عرض قائمة بالمواقع مع الكمية المتوفرة على الجهاز المحمول، مما يسمح لعامل المستودع باختيار الموقع لاستخدام المخزون منه.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="a5e2b-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="a5e2b-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="a5e2b-109">إعداد استثناءات العمل</span><span class="sxs-lookup"><span data-stu-id="a5e2b-109">Set up work exceptions</span></span>
1. <span data-ttu-id="a5e2b-110">في **جزء التنقل**، انتقل إلى **إدارة المستودعات > الإعداد > العمل > استثناءات العمل**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="a5e2b-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-111">Click **New**.</span></span> <span data-ttu-id="a5e2b-112">من الممكن تعريف عدة استثناءات عمل بواسطة سياسات إعادة توزيع أصناف مختلفة لتمكين العامل في المستودع من اختيار واحد بالاستناد إلى احتياجات الشحن التي يقوم بمعالجتها.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="a5e2b-113">اكتب قيمة في حقل **كود استثناء العمل**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="a5e2b-114">قم بإعطاء استثناء العمل عنوانًا للإشارة إلى المهمة التي يتم استخدامه من أجلها.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-114">Give the work exception a title to indicate what it's used for.</span></span> <span data-ttu-id="a5e2b-115">على سبيل المثال، دليل الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="a5e2b-116">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a5e2b-117">في الحقل **نوع الاستثناء**، حدد "انتقاء قصير".</span><span class="sxs-lookup"><span data-stu-id="a5e2b-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="a5e2b-118">حدد خانة الاختيار **تعديل المخزون**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="a5e2b-119">يعني هذا الخيار أن تسوية المخزون ستتم بشكل تلقائي على 0 في موقع الانتقاء القصير.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="a5e2b-120">في حقل **كود نوع التسوية الافتراضي‬**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="a5e2b-121">على سبيل المثال، في USMF، يمكنك تحديد "Remove Res Adj Out".</span><span class="sxs-lookup"><span data-stu-id="a5e2b-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="a5e2b-122">في الحقل **إعادة توزيع الصنف**، حدد "يدوي".</span><span class="sxs-lookup"><span data-stu-id="a5e2b-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="a5e2b-123">إذا قمت بتحديد "يدوي"، أو "تلقائي ويدوي"، يجب تمكين عامل المستودع لاستخدام إعادة التوزيع اليدوي.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="a5e2b-124">إعداد عامل لاستخدام إعادة التوزيع الأصناف يدويًا</span><span class="sxs-lookup"><span data-stu-id="a5e2b-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="a5e2b-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-125">Close the page.</span></span>
2. <span data-ttu-id="a5e2b-126">في **جزء التنقل**، انتقل إلى **إدارة المستودعات > الإعداد > العامل**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="a5e2b-127">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-127">Click **Edit**.</span></span>
4. <span data-ttu-id="a5e2b-128">في القائمة، حدد العامل 24.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="a5e2b-129">وسّع علامة التبويب السريعة **العمل**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="a5e2b-130">حدد "نعم" في حقل **السماح بإعادة توزيع الأصناف يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="a5e2b-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

