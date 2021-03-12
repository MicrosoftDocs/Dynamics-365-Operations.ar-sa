---
title: منضدة عمل إنشاء الحِمل
description: يصف هذا الموضوع كيفيه العمل مع منضدة إنشاء حمل العمل.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974203"
---
# <a name="load-building-workbench"></a><span data-ttu-id="e9f5e-103">منضدة عمل إنشاء الحِمل</span><span class="sxs-lookup"><span data-stu-id="e9f5e-103">Load building workbench</span></span>

<span data-ttu-id="e9f5e-104">يتيح لك منضدة إنشاء التحميل تطبيق استراتيجيات بناء التحميل عند قيامك بإنشاء أحمال العمل.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="e9f5e-105">إنشاء إستراتيجية إنشاء حمل العمل</span><span class="sxs-lookup"><span data-stu-id="e9f5e-105">Create a load building strategy</span></span>

<span data-ttu-id="e9f5e-106">يمكنك استخدام خطط إنشاء أحمال العمل لإنشاء أحمال العمل تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="e9f5e-107">يمكن ان تكون هذه الامكانيه مفيدة في المواقف التالية:</span><span class="sxs-lookup"><span data-stu-id="e9f5e-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="e9f5e-108">إذا قمت بشحن مجموعه محدده من المنتجات بشكل دوري ، تساعد استراتيجيات التحميل علي توفير الوقت ، لأنه ليس من الضروري إنشاء نفس الحمل كل مره.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="e9f5e-109">إذا أردت تجنب التحميلات الكاملة لزيادة الفعالية ، فان تحميل الاستراتيجيات يمكن ان يساعد في تعبئة كل حمل قدر المستطاع.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="e9f5e-110">توفر فئة استراتيجية بناء التحميل المسماة`TMSLoadBuildingVolumeStrategy` استراتيجية لبناء التحميل التي تسمي *استراتيجية بناء التحميل المستندة إلى وحده التخزين*.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="e9f5e-111">تسمح لك هذه الاستراتيجية باستخدام القيم القصوى المحددة للطول والوزن في قالب حمل العمل، أو يمكنك تجاوز الإعدادات بإدخال قيم جديدة.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="e9f5e-112">هذه الاستراتيجية هي الاستراتيجية الوحيدة التي يتم تضمينها خارج الصندوق.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="e9f5e-113">(ومع ذلك ، قد يكون لديك بعض الاستراتيجيات المخصصة.)</span><span class="sxs-lookup"><span data-stu-id="e9f5e-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="e9f5e-114">لاستخدام استراتيجية *استراتيجية التحميل التي تستند إلى وحده التخزين* الجاهزة، قم بتحديدها في الحقل **استراتيجية بناء التحميل** في صفحه **منضدة بناء التحميل** (**أداره النقل &gt; التخطيط  &gt; منضدة بناء التحميل**).</span><span class="sxs-lookup"><span data-stu-id="e9f5e-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="e9f5e-115">لإنشاء استراتيجية بناء حمل العمل، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="e9f5e-116">انتقل إلى **أداره النقل &gt; إعداد &gt; بناء التحميل &gt; استراتيجيات بناء التحميل**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="e9f5e-117">في جزء الاجراء ، حدد **إنشاء قائمه فئات** للتاكد من ان لديك أحدث الإصدارات من كافة الفئات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="e9f5e-118">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e9f5e-119">ادخل اسما فريدا لاستراتيجية ، وحدد فئة استراتيجية البناء التي تم تحميلها لها ، وادخل وصفا.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="e9f5e-120">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e9f5e-121">في جزء الإجراءات، حدد **المعلمات**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="e9f5e-122">في الصفحة **معلمات استراتيجية بناء التحميل**، حدد **قدره وحده التخزين** في القائمة، ثم في حقل **القيمة**، ادخل النسبة المئوية للقدرة الاجماليه لحجم الحمل التي يجب تطبيقها علي استراتيجية إنشاء التحميل الجديدة.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="e9f5e-123">حدد **قدره الوزن** في القائمة، ثم في حقل **القيمة**، ادخل النسبة المئوية للقدرة الاجماليه لوزن الحمل التي يجب تطبيقها علي استراتيجية بناء التحميل الجديدة.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="e9f5e-124">قم بإغلاق الصفحة **معلمات استراتيجية التحميل**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="e9f5e-125">قم بإغلاق الصفحة **استراتيجيات بناء التحميل**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="e9f5e-126">يمكنك الآن تعيين استراتيجية بناء التحميل إلى قالب بناء التحميل.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="e9f5e-127">بدلا من ذلك ، يمكنك استخدامه مباشره في منضدة تخطيط الحِمل.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="e9f5e-128">استخدم استراتيجية بناء تحميل في منضدة بناء التحميل.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="e9f5e-129">انتقل إلى **إدارة النقل &gt; التخطيط &gt; منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="e9f5e-130">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="e9f5e-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="e9f5e-131">حدد استراتيجية في الحقل **استراتيجية بناء التحميل**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="e9f5e-132">إذا قمت بتحديد قالب بناء تحميل وقمت بتعيين استراتيجية بناء التحميل اليه ، في جزء الاجراء ، ضمن علامة التبويب **أداره القوالب**، حدد **تطبيق قالب**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="e9f5e-133">ثم في مربع الحوار المنسدل **تطبيق قالب بناء التحميل**، حدد قالبا في الحقل **اسم قالب بناء التحميل**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="e9f5e-134">في علامة التبويب السريعة **تسلسل قوالب التحميل**، حدد واحد أو أكثر من [قوالب التحميل](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="e9f5e-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="e9f5e-135">ستحاول المنضدة احتواء الحمل في هذه الأنواع من الحاويات ، بالتسلسل الذي تم تحديده هنا.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="e9f5e-136">عاده ، يجب وضع أصغر الحاويات في اعلي القائمة لضمان تحديد أصغر حاويه ممكنة أولا.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="e9f5e-137">في جزء الإجراءات، حدد **اقتراح الأحمال**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="e9f5e-138">راجع التحميلات المقترحة وخطوط التحميل المقترحة.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="e9f5e-139">في جزء الاجراء ، حدد **إنشاء تحميلات** لإنشاء تحميلات تستند إلى سطور المستند المصدر في علامة التبويب السريعة **بنود التحميل المقترحة**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="e9f5e-140">قم بإغلاق الصفحة **منضدة بناء التحميل**.</span><span class="sxs-lookup"><span data-stu-id="e9f5e-140">Close the **Load building workbench** page.</span></span>
