---
title: " إنشاء مجموعات أذونات نقطة البيع"
description: سيظهر هذا الإجراء كيفية إنشاء مجموعة أذونات نقطة البيع.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566354"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="ce033-103"> إنشاء مجموعات أذونات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="ce033-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ce033-104">سيظهر هذا الإجراء كيفية إنشاء مجموعة أذونات نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="ce033-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="ce033-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="ce033-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="ce033-106">تم إعداد هذه المهمة لدور إدارة عمليات Retail.</span><span class="sxs-lookup"><span data-stu-id="ce033-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="ce033-107">انتقل إلى مجموعات الأذونات.</span><span class="sxs-lookup"><span data-stu-id="ce033-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="ce033-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ce033-108">Click New.</span></span>
3. <span data-ttu-id="ce033-109">في حقل "معرف مجموعة أذونات نقطة البيع‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ce033-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="ce033-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ce033-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ce033-111">حدد "نعم" في حقل "‏‫عرض إدخالات ساعة الوقت‬".</span><span class="sxs-lookup"><span data-stu-id="ce033-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="ce033-112">يمكنك الآن تمكين أذونات مختلفة لمجموعة أذونات نقطة البيع أو تعطيلها.</span><span class="sxs-lookup"><span data-stu-id="ce033-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="ce033-113">للحصول على بعض الأذونات، يمكنك تعيين قيمة ليتم استخدامها للتقييم إذا كان مستخدم نقطة البيع يمكنه تنفيذ الإجراء.</span><span class="sxs-lookup"><span data-stu-id="ce033-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="ce033-114">يعمل دليل المهمة هذا على تمكين عدد قليل من الأذونات التي قد يتم منحها للصراف.</span><span class="sxs-lookup"><span data-stu-id="ce033-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="ce033-115">حدد "نعم" في حقل "‏‫السماح بإنشاء أمر‬".</span><span class="sxs-lookup"><span data-stu-id="ce033-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="ce033-116">حدد "نعم" في حقل "‏‫السماح بتحرير أمر‬".</span><span class="sxs-lookup"><span data-stu-id="ce033-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="ce033-117">حدد "نعم" في حقل "‏‫السماح باسترداد أمر‬".</span><span class="sxs-lookup"><span data-stu-id="ce033-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="ce033-118">حدد "نعم" في حقل "‏‫السماح بتغيير كلمة المرور".</span><span class="sxs-lookup"><span data-stu-id="ce033-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="ce033-119">حدد "نعم" في حقل "‏‫‏‫السماح بإغلاق مخفي‬".</span><span class="sxs-lookup"><span data-stu-id="ce033-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="ce033-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ce033-120">Click Save.</span></span>
    * <span data-ttu-id="ce033-121">بعد أن يتم حفظ التغييرات الخاصة بك، تحتاج إلى تشغيل جدول توزيع الموظفين لدفع التغييرات إلى قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="ce033-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="ce033-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ce033-122">Close the page.</span></span>
13. <span data-ttu-id="ce033-123">انتقل إلى الوظائف.</span><span class="sxs-lookup"><span data-stu-id="ce033-123">Go to Jobs.</span></span>
    * <span data-ttu-id="ce033-124">بعد ذلك، سنقوم بتعيين مجموعة أذونات نقطة البيع لوظيفة.</span><span class="sxs-lookup"><span data-stu-id="ce033-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="ce033-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="ce033-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ce033-126">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ce033-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ce033-127">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="ce033-127">Click Edit.</span></span>
17. <span data-ttu-id="ce033-128">قم بتوسيع مقطع تصنيف الوظائف.</span><span class="sxs-lookup"><span data-stu-id="ce033-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="ce033-129">في حقل "‏‫مجموعة أذونات نقطة البيع‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ce033-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce033-130">سيستخدم كافة العاملين في مناصب لهذه الوظيفة إعدادات مجموعة أذونات نقطة البيع هذه ما لم يكن قد تم تجاوز أذونات نقطة البيع للعاملين على مستوى مناصبهم.</span><span class="sxs-lookup"><span data-stu-id="ce033-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="ce033-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ce033-131">Click Save.</span></span>
    * <span data-ttu-id="ce033-132">بعد أن يتم حفظ التغييرات الخاصة بك، تحتاج إلى تشغيل جدول توزيع الموظفين لدفع التغييرات إلى قنوات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="ce033-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

