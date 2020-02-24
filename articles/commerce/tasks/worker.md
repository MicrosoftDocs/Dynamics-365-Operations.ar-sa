---
title: " تكوين عامل"
description: يوضح هذا الإجراء كيفية تكوين عامل كمندوب مبيعات مؤهل للحصول على عمولة على المبيعات في نقطة البيع.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aee84f2dc39d2225985992fac0f9c20985ed9804
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021454"
---
# <a name="configure-a-worker"></a><span data-ttu-id="54fbf-103"> تكوين عامل</span><span class="sxs-lookup"><span data-stu-id="54fbf-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="54fbf-104">يوضح هذا الإجراء كيفية تكوين عامل كمندوب مبيعات مؤهل للحصول على عمولة على المبيعات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="54fbf-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="54fbf-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="54fbf-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="54fbf-106">إنشاء مجموعة مبيعات العمولة‬ للعامل</span><span class="sxs-lookup"><span data-stu-id="54fbf-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="54fbf-107">انتقل إلى المبيعات والتسويق > العمولات > مجموعات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="54fbf-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="54fbf-108">يمكن تعيين العاملين إلى مجموعة مبيعات واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="54fbf-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="54fbf-109">في نقطة البيع، يمكنك اختيار أي مجموعة مبيعات تحتوي على عاملين من دفتر العناوين الخاص بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="54fbf-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="54fbf-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="54fbf-110">Click New.</span></span>
3. <span data-ttu-id="54fbf-111">في الحقل "المجموعة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="54fbf-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="54fbf-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="54fbf-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="54fbf-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="54fbf-113">Click Save.</span></span>
6. <span data-ttu-id="54fbf-114">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="54fbf-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="54fbf-115">انقر فوق "مندوب المبيعات".</span><span class="sxs-lookup"><span data-stu-id="54fbf-115">Click Sales rep.</span></span>
    * <span data-ttu-id="54fbf-116">يمكن أن تحتوي مجموعة مبيعات على عامل واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="54fbf-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="54fbf-117">يمكن تقسيم العمولات‬ بين العمال استنادًا إلى كيفية تعريف حصة العمولة.</span><span class="sxs-lookup"><span data-stu-id="54fbf-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="54fbf-118">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="54fbf-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="54fbf-119">في الحقل "حصة العمولة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="54fbf-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="54fbf-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="54fbf-120">Click Save.</span></span>
11. <span data-ttu-id="54fbf-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="54fbf-121">Close the page.</span></span>
12. <span data-ttu-id="54fbf-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="54fbf-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="54fbf-123">تعيين مجموعة المبيعات الافتراضية إلى العاملين</span><span class="sxs-lookup"><span data-stu-id="54fbf-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="54fbf-124">انتقل إلى البيع بالتجزئة والتجارة > الموظفون > العامون.</span><span class="sxs-lookup"><span data-stu-id="54fbf-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="54fbf-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="54fbf-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="54fbf-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="54fbf-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54fbf-127">انقر فوق علامة التبويب Commerce.</span><span class="sxs-lookup"><span data-stu-id="54fbf-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="54fbf-128">يمكن تعيين عامل إلى مجموعة مبيعات افتراضية.</span><span class="sxs-lookup"><span data-stu-id="54fbf-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="54fbf-129">ستُضاف مجموعة المبيعات الافتراضية تلقائيًا إلى بنود المبيعات في نقطة البيع إذا تم تمكين الخيار في ملف تعريف الوظائف الخاص بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="54fbf-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="54fbf-130">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="54fbf-130">Click Edit.</span></span>
6. <span data-ttu-id="54fbf-131">في حقل "المجموعة الافتراضية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="54fbf-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="54fbf-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="54fbf-132">Click Save.</span></span>

