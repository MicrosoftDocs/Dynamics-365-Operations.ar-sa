---
title: تكامل عميل Microsoft Project
description: التخطيط والاحتفاظ بجدول مشروع يمكن أن يكون معقدًا، لأن مديرو المشاريع بحاجة إلى استخدام الأدوات التي تساعدهم في إدارة هذه المهمة. يوفر التكامل مع عميل Microsoft Project الدعم لفتح وإدارة هيكل تنظيم عمل مشروع.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "317466"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="5c033-104">تكامل عميل Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="5c033-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c033-105">التخطيط والاحتفاظ بجدول مشروع يمكن أن يكون معقدًا، لأن مديرو المشاريع بحاجة إلى استخدام الأدوات التي تساعدهم في إدارة هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="5c033-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="5c033-106">يوفر التكامل مع عميل Microsoft Project الدعم لفتح وإدارة هيكل تنظيم عمل مشروع.</span><span class="sxs-lookup"><span data-stu-id="5c033-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="5c033-107">يستطيع مدير المشروع نشر أي تغييرات مرة أخرى إلى هيكل تنظيم عمل مشروع Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5c033-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="5c033-108">إذا كنت تستخدم تحديث شهر يوليو لتطبيق Microsoft Dynamics 365 for Finance and Operations، فيجب تثبيت KB 4054797 و4055884.</span><span class="sxs-lookup"><span data-stu-id="5c033-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="5c033-109">تكوين الأداة الإضافية لعميل Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="5c033-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="5c033-110">لتمكين التكامل مع عميل Microsoft Project، يلزم تثبيت الأداة الإضافية لـ Microsoft Dynamics 365 في تطبيق عميل Microsoft Project للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="5c033-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="5c033-111">يتم ذلك عن طريق فتح **مساحة عمل إدارة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="5c033-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="5c033-112">•   انقر فوق **تكوين الأداة الإضافية لعميل المشروع** من قسم **الارتباطات** > **الإعداد** في مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="5c033-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="5c033-113">•   انقر فوق **فتح**، ثم انقر فوق **تشغيل** عند مطالبتك بذلك.</span><span class="sxs-lookup"><span data-stu-id="5c033-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="5c033-114">فتح وتحرير مسودة هيكل تنظيم عمل موجودة في عميل Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="5c033-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="5c033-115">إذا تم إنشاء هيكل تنظيم عمل لمشروع Finance and Operations بالفعل، يمكن فتح هيكل تنظيم العمل في تطبيق عميل Microsoft Project إذا كان هيكل تنظيم العمل بحالة مسودة.</span><span class="sxs-lookup"><span data-stu-id="5c033-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="5c033-116">لفتحه من صفحة **المشروع**، انقر فوق الارتباط **فتح في Microsoft Project** من علامة التبويب **تخطيط**. يمكن أيضًا فتح هذه الصفحة من داخل تطبيق عميل Microsoft Project بالنقر فوق **فتح** على علامة التبويب **Microsoft Dynamics 365**. حدد **الكيان القانوني** و**المشروع‏‎** من القائمة.</span><span class="sxs-lookup"><span data-stu-id="5c033-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="5c033-117">إذا كنت تستخدم Internet Explorer كمستعرض، فستحتاج إلى النقر فوق **حفظ** للفتح يدويًا من الموقع الذي تم تنزيل الملف في.</span><span class="sxs-lookup"><span data-stu-id="5c033-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="5c033-118">أو، انقر فوق **حفظ وفتح** لفتح الملف في عميل Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="5c033-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="5c033-119">لا تعيد تسمية اسم الملف عند الحفظ.</span><span class="sxs-lookup"><span data-stu-id="5c033-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="5c033-120">قبل إجراء أي عمليات تحرير على الملف باستخدام عميل Microsoft Project، تحتاج إلى سحبه. انقر فوق **سحب** على علامة التبويب **Microsoft Dynamics 365**. سيؤدي ذلك إلى منع المستخدمين الآخرين من تحرير هيكل تنظيم العمل من داخل Finance and Operations في الوقت نفسه.</span><span class="sxs-lookup"><span data-stu-id="5c033-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="5c033-121">لنشر هيكل تنظيم العمل بعد إتمام أي عمليات تحرير، انقر فوق **إيداع‏‎** على علامة التبويب **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5c033-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="5c033-122">إذا تمت بالفعل إضافة فريق مشروع للمشروع في Finance and Operations، فسيتم ملء قائمة الموارد بأعضاء الفريق.</span><span class="sxs-lookup"><span data-stu-id="5c033-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="5c033-123">في حال عدم إضافة فريق المشروع إلى المشروع حتى الآن، فيمكنك تحديد الموارد وإنشاء الفريق في عميل Microsoft Project عن طريق النقر فوق الزر **الموارد** على علامة التبويب **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5c033-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="5c033-124">ستتم مزامنة البيانات التالية مرة أخرى مع Finance and Operations كجزء من عملية الإيداع:</span><span class="sxs-lookup"><span data-stu-id="5c033-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="5c033-125">•   اسم المهمة</span><span class="sxs-lookup"><span data-stu-id="5c033-125">•   Task name</span></span>

<span data-ttu-id="5c033-126">•   تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="5c033-126">•   Start date</span></span>

<span data-ttu-id="5c033-127">•   تاريخ الانتهاء</span><span class="sxs-lookup"><span data-stu-id="5c033-127">•   Finish date</span></span>

<span data-ttu-id="5c033-128">•   العناصر السابقة</span><span class="sxs-lookup"><span data-stu-id="5c033-128">•   Predecessors</span></span>

<span data-ttu-id="5c033-129">•   أسماء الموارد</span><span class="sxs-lookup"><span data-stu-id="5c033-129">•   Resource names</span></span>

<span data-ttu-id="5c033-130">•   الفئة</span><span class="sxs-lookup"><span data-stu-id="5c033-130">•   Category</span></span>

<span data-ttu-id="5c033-131">•   فئة المورد</span><span class="sxs-lookup"><span data-stu-id="5c033-131">•   Resource category</span></span>

<span data-ttu-id="5c033-132">•   ساعات العمل</span><span class="sxs-lookup"><span data-stu-id="5c033-132">•   Work hours</span></span>

<span data-ttu-id="5c033-133">•   الملاحظات</span><span class="sxs-lookup"><span data-stu-id="5c033-133">•   Notes</span></span>

<span data-ttu-id="5c033-134">•   الأولوية</span><span class="sxs-lookup"><span data-stu-id="5c033-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="5c033-135">إذا قمت بإضافة أي أعمدة أخرى إلى ملف عميل Microsoft Project، فلن يتم حفظ للملف ولن يتم عرضه عند فتح الملف مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="5c033-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="5c033-136">إنشاء هيكل تنظيم العمل لمشروع موجود باستخدام عميل Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="5c033-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="5c033-137">لإنشاء هيكل تنظيم عمل جديد باستخدام عميل Microsoft Project، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5c033-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="5c033-138">افتح عميل Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="5c033-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5c033-139">على علامة التبويب **Microsoft Dynamics 365**، انقر فوق **فتح**.</span><span class="sxs-lookup"><span data-stu-id="5c033-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="5c033-140">حدد **الكيان القانوني** للمشروع.</span><span class="sxs-lookup"><span data-stu-id="5c033-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="5c033-141">حدد **المشروع**.</span><span class="sxs-lookup"><span data-stu-id="5c033-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="5c033-142">انقر فوق **سحب** على علامة التبويب **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5c033-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="5c033-143">عندما تصبح جاهزًا للنشر في Finance and Operations، انقر فوق **إيداع‏‎** على علامة التبويب **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5c033-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="5c033-144">استبدال هيكل تنظيم العمل لمشروع موجود باستخدام عميل Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="5c033-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="5c033-145">لإنشاء هيكل تنظيم عمل جديد باستخدام عميل Microsoft Project واستبدال هيكل تنظيم عمل موجود لمشروع موجود، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="5c033-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="5c033-146">افتح عميل Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="5c033-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5c033-147">أنشئ الجدول في عميل Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="5c033-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="5c033-148">على علامة التبويب **Microsoft Dynamics 365**، انقر فوق **حفظ التغييرات** > **استبدال مشروع موجود**.</span><span class="sxs-lookup"><span data-stu-id="5c033-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="5c033-149">حدد **الكيان القانوني** للمشروع.</span><span class="sxs-lookup"><span data-stu-id="5c033-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="5c033-150">حدد **المشروع**.</span><span class="sxs-lookup"><span data-stu-id="5c033-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="5c033-151">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c033-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="5c033-152">إنشاء مشروع جديد من داخل عميل Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="5c033-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="5c033-153">افتح عميل Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="5c033-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="5c033-154">أنشئ الجدول في عميل Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="5c033-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="5c033-155">على علامة التبويب **Microsoft Dynamics 365**، انقر فوق **حفظ التغييرات** > **حفظ إلى مشروع جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c033-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="5c033-156">حدد **الكيان القانوني** للمشروع.</span><span class="sxs-lookup"><span data-stu-id="5c033-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="5c033-157">قم بإدخال **معرف المشروع**، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="5c033-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="5c033-158">أدخل **اسم المشروع**.</span><span class="sxs-lookup"><span data-stu-id="5c033-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="5c033-159">حدد **نوع المشروع** و**مجموعة المشروع** و**معرف عقد المشروع**.</span><span class="sxs-lookup"><span data-stu-id="5c033-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="5c033-160">بدلاً من ذلك، يمكنك إنشاء عقد مشروع جديد بالنقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c033-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="5c033-161">حدد **التقويم** المُراد استخدامه لإدارة الموارد.</span><span class="sxs-lookup"><span data-stu-id="5c033-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="5c033-162">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5c033-162">Click **OK**.</span></span>
