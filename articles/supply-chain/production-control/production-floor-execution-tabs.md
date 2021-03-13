---
title: تصميم واجهة تنفيذ صالة الإنتاج‬ واستخدامها
description: يوضح هذا الموضوع كيفيه تصميم محتوي واجهه المستخدم لكل تكوين.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 786ea9a3da98e9f1812b007d4301cb47680e6894
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077568"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="591a0-103">تصميم واجهة تنفيذ صالة الإنتاج‬ واستخدامها</span><span class="sxs-lookup"><span data-stu-id="591a0-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="591a0-104">يمكنك تصميم محتوي واجهه المستخدم لكل تكوين يتم استخدامه بواسطة واجهه تنفيذ صالة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="591a0-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="591a0-105">علي سبيل المثال ، قد يحتاج العاملون في خليه عمل واحده إلى التمكن من فتح إرشادات الوظيفة في حاله الإنتاج ، بينما في خليه عمل أخرى ، لا توجد حاجه إلى التعليمات.</span><span class="sxs-lookup"><span data-stu-id="591a0-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="591a0-106">وفي هذه الحالة ، يجب إنشاء تكوينين ، واحدا بالزر لفتح مرفقات المستند والاخر بدون هذا الزر.</span><span class="sxs-lookup"><span data-stu-id="591a0-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="591a0-107">تصميم علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="591a0-107">Design a tab</span></span>

<span data-ttu-id="591a0-108">في الصفحة **تكوين تنفيذ صالة الإنتاج**، يمكن إنشاء علامات التبويب وتكوينها عن طريق تحديد **تصميم علامات التبويب** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="591a0-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="591a0-109">يتم تقسيم كل علامة تبويب إلى أربعه مقاطع ، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="591a0-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="591a0-110">![تخطيط علامة التبويب](media/pfe-tab-layout.png "تخطيط علامة التبويب")</span><span class="sxs-lookup"><span data-stu-id="591a0-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="591a0-111">يتم عرض العناصر التالية في الرسم التوضيحي:</span><span class="sxs-lookup"><span data-stu-id="591a0-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="591a0-112">شريط الأدوات الرئيسي</span><span class="sxs-lookup"><span data-stu-id="591a0-112">Primary toolbar</span></span>
1. <span data-ttu-id="591a0-113">شريط الأدوات الثانوي</span><span class="sxs-lookup"><span data-stu-id="591a0-113">Secondary toolbar</span></span>
1. <span data-ttu-id="591a0-114">طريقة العرض الرئيسية</span><span class="sxs-lookup"><span data-stu-id="591a0-114">Main view</span></span>
1. <span data-ttu-id="591a0-115">عرض تفصيلي</span><span class="sxs-lookup"><span data-stu-id="591a0-115">Detailed view</span></span>

<span data-ttu-id="591a0-116">لإنشاء علامة تبويب جديدة وتكوينها، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="591a0-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="591a0-117">انتقل إلى **التحكم بالإنتاج &gt; إعداد &gt; ‏‫التنفيذ التصنيعي**.</span><span class="sxs-lookup"><span data-stu-id="591a0-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="591a0-118">حدد **تصميم علامات التبويب** في جزء الإجراءات لفتح صفحه **تصميم علامات التبويب**.</span><span class="sxs-lookup"><span data-stu-id="591a0-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="591a0-119">![صفحة تصميم علامات التبويب](media/pfe-design-tabs.png "صفحة تصميم علامات التبويب")</span><span class="sxs-lookup"><span data-stu-id="591a0-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="591a0-120">حدد **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="591a0-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="591a0-121">قم بالإعدادات التالية في راس الصفحة:</span><span class="sxs-lookup"><span data-stu-id="591a0-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="591a0-122">**اسم علامة التبويب** - حدد اسما لعلامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="591a0-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="591a0-123">**العرض الرئيسي** - يتم التحديد بين قائمتي الوظائف المعرفتان مسبقا (*الوظائف النشطة* أو *كافة الوظائف* أو *آلتي*).</span><span class="sxs-lookup"><span data-stu-id="591a0-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="591a0-124">**عرض التفاصيل** - اختر من بين قيمه فارغه أو **تفاصيل المهمة**.</span><span class="sxs-lookup"><span data-stu-id="591a0-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="591a0-125">إذا قمت بتحديد القيمة الفارغة ، فلن تكون هناك طريقه عرض مفصله في علامة التبويب إذا قمت بتحديد **تفاصيل الوظيفة**، ستحتوي طريقه العرض التفصيلية علي وصف تفصيلي للوظيفة المحددة في قائمه الوظائف في طريقه العرض الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="591a0-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="591a0-126">في قسم **شريط الادوات الرئيسي**، اختر الأزرار التي يجب ان تكون متوفرة في شريط الادوات الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="591a0-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="591a0-127">يعرض العمود **الإجراءات المتوفرة** قائمه بكافة الأزرار التي يمكن اضافتها.</span><span class="sxs-lookup"><span data-stu-id="591a0-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="591a0-128">تعرض أعمده **الإجراءات المحددة** قائمه بكافة الأزرار المضمنة في التكوين الحالي.</span><span class="sxs-lookup"><span data-stu-id="591a0-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="591a0-129">استخدم الأزرار الموجودة بين الاعمده لنقل العناصر المحددة بين الاعمده حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="591a0-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="591a0-130">استخدم الزرين لاعلي ولأسفل بجانب عمود **الإجراءات المحددة** للتحكم في الترتيب الذي يتم به عرض الأزرار في واجهه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="591a0-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="591a0-131">في قسم **شريط الادوات** **الثانوي**، اختر الأزرار التي يجب ان تكون متوفرة في شريط الادوات الثانوي.</span><span class="sxs-lookup"><span data-stu-id="591a0-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="591a0-132">يعرض العمود **الإجراءات المتوفرة** قائمه بكافة الأزرار التي يمكن اضافتها.</span><span class="sxs-lookup"><span data-stu-id="591a0-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="591a0-133">تعرض أعمده **الإجراءات المحددة** قائمه بكافة الأزرار المضمنة في التكوين الحالي.</span><span class="sxs-lookup"><span data-stu-id="591a0-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="591a0-134">استخدم الأزرار الموجودة بين الاعمده لنقل العناصر المحددة بين الاعمده حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="591a0-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="591a0-135">استخدم الزرين لاعلي ولأسفل بجانب عمود **الإجراءات المحددة** للتحكم في الترتيب الذي يتم به عرض الأزرار في واجهه المستخدم.</span><span class="sxs-lookup"><span data-stu-id="591a0-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="591a0-136">اقران علامة تبويب بتكوين</span><span class="sxs-lookup"><span data-stu-id="591a0-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="591a0-137">بعد تصميم كافة علامات التبويب التي تحتاجها ، يمكنك اقرانها بالتكوين.</span><span class="sxs-lookup"><span data-stu-id="591a0-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="591a0-138">انتقل إلى **التحكم بالإنتاج &gt; إعداد &gt; تكوين تنفيذ صالة الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="591a0-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="591a0-139">![تكوين التنفيذ في منطقة الإنتاج‬](media/pfe-config-prod-floor-execution.png "تكوين التنفيذ في منطقة الإنتاج‬")</span><span class="sxs-lookup"><span data-stu-id="591a0-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="591a0-140">على علامة التبويب السريعة **تحديد علامة التبويب** ، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="591a0-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="591a0-141">تتم إضافة صف جديد إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="591a0-141">A new row is added to the grid.</span></span> <span data-ttu-id="591a0-142">بالنسبة لهذا الصف الجديد ، حدد اسم علامة التبويب التي ترغب في اضافتها إلى التكوين.</span><span class="sxs-lookup"><span data-stu-id="591a0-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="591a0-143">استمر في أضافه علامات التبويب الاضافيه حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="591a0-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="591a0-144">استخدم الزرين **تحريك لاعلي** و **تحريك لأسفل** علي شريط الادوات لترتيب علامات التبويب حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="591a0-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="591a0-145">سيتم عرض علامات التبويب من اليسار إلى اليمين بالترتيب الموضح في لقطه الشاشة أعلاه (يتم عرض علامة التبويب في الأعلى علي اليسار).</span><span class="sxs-lookup"><span data-stu-id="591a0-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
