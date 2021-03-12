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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c200f7f6ff0aa5672e50c539bfaa5e30213185
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003593"
---
# <a name="configure-a-worker"></a><span data-ttu-id="e06ec-103"> تكوين عامل</span><span class="sxs-lookup"><span data-stu-id="e06ec-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e06ec-104">يوضح هذا الإجراء كيفية تكوين عامل كمندوب مبيعات مؤهل للحصول على عمولة على المبيعات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="e06ec-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="e06ec-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="e06ec-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="e06ec-106">إنشاء مجموعة مبيعات العمولة‬ للعامل</span><span class="sxs-lookup"><span data-stu-id="e06ec-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="e06ec-107">انتقل إلى المبيعات والتسويق > العمولات > مجموعات المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e06ec-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="e06ec-108">يمكن تعيين العاملين إلى مجموعة مبيعات واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="e06ec-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="e06ec-109">في نقطة البيع، يمكنك اختيار أي مجموعة مبيعات تحتوي على عاملين من دفتر العناوين الخاص بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="e06ec-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="e06ec-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e06ec-110">Click New.</span></span>
3. <span data-ttu-id="e06ec-111">في الحقل "المجموعة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e06ec-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="e06ec-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e06ec-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e06ec-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e06ec-113">Click Save.</span></span>
6. <span data-ttu-id="e06ec-114">في جزء "الإجراءات"، انقر فوق "عام".</span><span class="sxs-lookup"><span data-stu-id="e06ec-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="e06ec-115">انقر فوق "مندوب المبيعات".</span><span class="sxs-lookup"><span data-stu-id="e06ec-115">Click Sales rep.</span></span>
    * <span data-ttu-id="e06ec-116">يمكن أن تحتوي مجموعة مبيعات على عامل واحد أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="e06ec-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="e06ec-117">يمكن تقسيم العمولات‬ بين العمال استنادًا إلى كيفية تعريف حصة العمولة.</span><span class="sxs-lookup"><span data-stu-id="e06ec-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="e06ec-118">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e06ec-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="e06ec-119">في الحقل "حصة العمولة‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="e06ec-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="e06ec-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e06ec-120">Click Save.</span></span>
11. <span data-ttu-id="e06ec-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e06ec-121">Close the page.</span></span>
12. <span data-ttu-id="e06ec-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e06ec-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="e06ec-123">تعيين مجموعة المبيعات الافتراضية إلى العاملين</span><span class="sxs-lookup"><span data-stu-id="e06ec-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="e06ec-124">انتقل إلى البيع بالتجزئة والتجارة > الموظفون > العامون.</span><span class="sxs-lookup"><span data-stu-id="e06ec-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="e06ec-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e06ec-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e06ec-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e06ec-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e06ec-127">انقر فوق علامة التبويب Commerce.</span><span class="sxs-lookup"><span data-stu-id="e06ec-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="e06ec-128">يمكن تعيين عامل إلى مجموعة مبيعات افتراضية.</span><span class="sxs-lookup"><span data-stu-id="e06ec-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="e06ec-129">ستُضاف مجموعة المبيعات الافتراضية تلقائيًا إلى بنود المبيعات في نقطة البيع إذا تم تمكين الخيار في ملف تعريف الوظائف الخاص بالمتجر.</span><span class="sxs-lookup"><span data-stu-id="e06ec-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="e06ec-130">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e06ec-130">Click Edit.</span></span>
6. <span data-ttu-id="e06ec-131">في حقل "المجموعة الافتراضية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e06ec-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="e06ec-132">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e06ec-132">Click Save.</span></span>

