---
title: مجموعات أمر العمل
description: يصف هذا الموضوع كيفية التعامل مع مجموعات أوامر العمل في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875484"
---
# <a name="work-order-pools"></a><span data-ttu-id="a1a28-103">مجموعات أمر العمل</span><span class="sxs-lookup"><span data-stu-id="a1a28-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="a1a28-104">يمكنك استخدام مجموعات أوامر العمل لتجميع أوامر العمل التي يجمع ما بينها شيء مشترك.</span><span class="sxs-lookup"><span data-stu-id="a1a28-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="a1a28-105">على سبيل المثال، يمكنك إنشاء مجموعة أوامر عمل لما يلي:</span><span class="sxs-lookup"><span data-stu-id="a1a28-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="a1a28-106">لأطقم العمل، على سبيل المثال، طاقم الصيانة A، طاقم الصيانة B</span><span class="sxs-lookup"><span data-stu-id="a1a28-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="a1a28-107">المهارات المهنية، على سبيل المثال، عمال الكهرباء أو السباكة</span><span class="sxs-lookup"><span data-stu-id="a1a28-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="a1a28-108">المواقع الفعلية</span><span class="sxs-lookup"><span data-stu-id="a1a28-108">physical locations</span></span>  

- <span data-ttu-id="a1a28-109">الجداول الزمنية، على سبيل المثال، أسابيع أو فترات أخرى</span><span class="sxs-lookup"><span data-stu-id="a1a28-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="a1a28-110">إذا لزم الأمر، يمكن وضع أمر عمل واحد في عدد كبير من مجموعات أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="a1a28-111">إنشاء مجموعة أوامر عمل</span><span class="sxs-lookup"><span data-stu-id="a1a28-111">Create work order pool</span></span>

<span data-ttu-id="a1a28-112">في **جميع مجموعات أوامر العمل** أو **مجموعات أوامر العمل النشطة**، يمكنك الحصول على نظرة عامة على مجموعات أوامر العمل وإنشاء مجموعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="a1a28-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="a1a28-113">انقر فوق **إدارة الأصول** > **عام** > **مجموعات أوامر العمل** > **جميع مجموعات أوامر العمل** أو **مجموعات أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="a1a28-114">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-114">Click **New**.</span></span>

3. <span data-ttu-id="a1a28-115">أدخل معرف مجموعة أوامر العمل في حقل **المجموعة** وأدخل اسمًا في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="a1a28-116">حدد "نعم" على زر التبديل **نشط** للإشارة إلى أن مجموعة أوامر العمل نشطة.</span><span class="sxs-lookup"><span data-stu-id="a1a28-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="a1a28-117">حدد "نعم" على زر التبديل **"حذف علاقات أوامر العمل** إذا أردت أن تتم إزالة أوامر العمل بشكل تلقائي من مجموعة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="a1a28-118">في الحقل **حذف حالة دورة الحياة**، حدد حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="a1a28-119">على سبيل المثال، يمكن تعيين حالة دورة حياة أمر العمل لحذف العلاقات بمجموعات أوامر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="a1a28-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="a1a28-120">يمكنك بدء إضافة أوامر العمل إلى مجموعة أوامر العمل على الفور.</span><span class="sxs-lookup"><span data-stu-id="a1a28-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="a1a28-121">على علامة التبويب السريعة **أوامر العمل**، انقر فوق **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="a1a28-122">حدد أمر عمل في حقل **أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="a1a28-123">يتم عندئذٍ تحديث الحقول المرتبطة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="a1a28-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="a1a28-124">كرر الخطوات من 7 إلى 8 لإضافة المزيد من أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="a1a28-125">في الحقل **ترتيب الفرز**، يمكنك الإشارة إلى ما إذا كان يجب تنفيذ أوامر العمل بترتيب معين.</span><span class="sxs-lookup"><span data-stu-id="a1a28-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="a1a28-126">ادخل الأرقام 1 و 2 و 3 وهكذا للإشارة إلى تسلسل معين لأوامر العمل المحددة.</span><span class="sxs-lookup"><span data-stu-id="a1a28-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="a1a28-127">انقر فوق الزر **أوامر العمل** لعرض قائمة بجميع أوامر العمل المضمنة في مجموعة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="a1a28-128">انقر فوق الزر‏‎ **القدرة الإنتاجية** لفتح **القدرة الإنتاجية**لحساب وعرض القدرة الإنتاجية لجدول الصيانة وأوامر العمل غير المجدولة وأوامر العمل المجدولة.</span><span class="sxs-lookup"><span data-stu-id="a1a28-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="a1a28-129">انقر فوق الزر **التنبؤ بالأصناف** لفتح **التنبؤ بالأصناف** لحساب وعرض التنبؤات للأصناف (قطع الغيار وقطع أخرى مطلوبة) ذات الصلة بجدول الصيانة وأوامر العمل غير المجدولة وأوامر العمل المجدولة.</span><span class="sxs-lookup"><span data-stu-id="a1a28-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="a1a28-130">انق فوق الزر **طلب شراء أمر العمل** لفتح قائمة **طلب شراء أمر العمل** للاطلاع على قائمة بطلبات الشراء ذات الصلة بأوامر العمل في مجموعة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="a1a28-131">انق فوق الزر **شراء أمر العمل** لفتح قائمة **شراء أمر العمل** للاطلاع على قائمة بأوامر الشراء ذات الصلة بأوامر العمل في مجموعة أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="a1a28-132">عندما لا تعود مجموعة أوامر العمل ذات صلة بتخطيط عملك، عيّن خانة الاختيار **نشط** لهذه المجموعة إلى "لا" في طريقة عرض قائمة **مجموعة أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="a1a28-133">حدد خانة الاختيار **حذف علاقات أوامر العمل** إذا كنت ترغب في حذف كافة بنود أمر العمل، على سبيل المثال، لإنشاء مجموعة فارغة يمكنك استخدامها في وقت لاحق لأوامر عمل أخرى.</span><span class="sxs-lookup"><span data-stu-id="a1a28-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="a1a28-134">تذكر ضرورة إلغاء تحديد خانة الاختيار **حذف علاقات أوامر العمل** إذا كنت تريد مجموعة أوامر العمل لإنشاء علاقات أوامر عمل جديدة في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="a1a28-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![الشكل 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="a1a28-136">أضافه أمر عمل إلى مجموعة أوامر عمل</span><span class="sxs-lookup"><span data-stu-id="a1a28-136">Add work order to a work order pool</span></span>

<span data-ttu-id="a1a28-137">كما هو موضح في القسم أعلاه، يمكنك إضافة أوامر العمل إلى مجموعة أوامر العمل عندما تقوم بإنشاء المجموعة.</span><span class="sxs-lookup"><span data-stu-id="a1a28-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="a1a28-138">يمكنك أيضًا إضافة أمر عمل إلى مجموعة أوامر عمل من إحدى قوائم **جميع أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="a1a28-139">انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a1a28-140">حدد أمر العمل في القائمة، وانقر فوق **مجموعة أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="a1a28-141">حدد "إضافة" في الحقل **إضافة/إزالة**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="a1a28-142">في الحقل **مجموعة**، حدد مجموعة‏‎ أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a1a28-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="a1a28-143">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-143">Click **OK**.</span></span>

6. <span data-ttu-id="a1a28-144">بعد إضافة أمر عمل إلى مجموعة أوامر عمل، إذا أردت وضع أمر العمل في تسلسل معين في المجموعة: افتح إحدى صفحات قوائم مجموعات أوامر العمل، وحدد المجموعة وانقر فوق **تحرير**، وعدّل ترتيب فرز أوامر العمل المضمنة في نموذج **مجموعة أوامر العمل** > علامة التبويب السريعة **أوامر‏‎ العمل** > حقل **ترتيب الفرز**.</span><span class="sxs-lookup"><span data-stu-id="a1a28-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="a1a28-145">إذا أردت إزالة أمر العمل المحدد من مجموعة أوامر العمل، حدد "إزالة" في الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="a1a28-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

