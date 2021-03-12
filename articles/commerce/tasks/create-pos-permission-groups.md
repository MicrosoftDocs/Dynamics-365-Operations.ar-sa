---
title: إنشاء مجموعات أذونات نقطة البيع
description: يوضح هذا الموضوع كيفية إنشاء مجموعة أذونات نقطة البيع‬.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac03e1bfb7a2463b31feca0a4303c182a00ad259
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964809"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="5c40b-103">إنشاء مجموعات أذونات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="5c40b-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c40b-104">يوضح هذا الموضوع كيفية إنشاء مجموعة أذونات نقطة البيع‬.</span><span class="sxs-lookup"><span data-stu-id="5c40b-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="5c40b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذه المهمة هي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="5c40b-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5c40b-106">هذه المهمة محددة لدور إدارة عمليات التجارة.</span><span class="sxs-lookup"><span data-stu-id="5c40b-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="5c40b-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > البيع بالتجزئة والتجارة > الموظفون > مجموعات الأذونات**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="5c40b-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-108">Select **New**.</span></span>
3. <span data-ttu-id="5c40b-109">في حقل **معرف مجموعة أذونات نقطة البيع‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5c40b-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="5c40b-110">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5c40b-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5c40b-111">حدد **نعم** في حقل "**عرض إدخالات ساعة الوقت‬**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="5c40b-112">يمكنك الآن تمكين أذونات مختلفة لمجموعة أذونات نقطة البيع أو تعطيلها.</span><span class="sxs-lookup"><span data-stu-id="5c40b-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="5c40b-113">للحصول على بعض الأذونات، يمكنك تعيين قيمة ليتم استخدامها للتقييم إذا كان مستخدم نقطة البيع يمكنه تنفيذ الإجراء.</span><span class="sxs-lookup"><span data-stu-id="5c40b-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="5c40b-114">يعمل دليل المهمة هذا على تمكين عدد قليل من الأذونات التي قد يتم منحها للصراف.</span><span class="sxs-lookup"><span data-stu-id="5c40b-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="5c40b-115">حدد **نعم** في حقل **السماح بإنشاء أمر**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="5c40b-116">حدد **نعم** في حقل **‏‫السماح بتحرير أمر‬**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="5c40b-117">حدد **نعم** في حقل **السماح باسترداد أمر‬**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="5c40b-118">حدد **نعم** في حقل **السماح بتغيير كلمة المرور**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="5c40b-119">حدد **نعم** في حقل **السماح بإغلاق مخفي‬**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="5c40b-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-120">Select **Save**.</span></span> <span data-ttu-id="5c40b-121">بعد حفظ التغييرات الخاصة بك، تحتاج إلى تشغيل جدول توزيع الموظفين لدفع التغييرات إلى قنوات التجارة.</span><span class="sxs-lookup"><span data-stu-id="5c40b-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="5c40b-122">في جزء التنقل، انتقل إلى **الوحدات النمطية > الموارد‏‎ البشرية > الوظائف > الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="5c40b-123">بعد ذلك، سنقوم بتعيين مجموعة أذونات نقطة البيع لوظيفة.</span><span class="sxs-lookup"><span data-stu-id="5c40b-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="5c40b-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5c40b-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5c40b-125">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-125">Select **Edit**.</span></span>
15. <span data-ttu-id="5c40b-126">قم بتوسيع القسم **تصنيف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="5c40b-127">في حقل "‏‫مجموعة أذونات نقطة البيع‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5c40b-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="5c40b-128">سيستخدم كافة العاملين في مناصب لهذه الوظيفة إعدادات مجموعة أذونات نقطة البيع هذه ما لم يكن قد تم تجاوز أذونات نقطة البيع للعاملين على مستوى مناصبهم.</span><span class="sxs-lookup"><span data-stu-id="5c40b-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="5c40b-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5c40b-129">Select **Save**.</span></span> <span data-ttu-id="5c40b-130">بعد حفظ التغييرات الخاصة بك، تحتاج إلى تشغيل جدول توزيع الموظفين لدفع التغييرات إلى القنوات.</span><span class="sxs-lookup"><span data-stu-id="5c40b-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

