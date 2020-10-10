---
title: مجموعات أمر العمل
description: يصف هذا الموضوع كيفية التعامل مع مجموعات أوامر العمل في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889495"
---
# <a name="work-order-pools"></a><span data-ttu-id="4d022-103">مجموعات أمر العمل</span><span class="sxs-lookup"><span data-stu-id="4d022-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="4d022-104">يمكنك استخدام مجموعات أوامر العمل لتجميع أوامر العمل التي يجمع ما بينها شيء مشترك.</span><span class="sxs-lookup"><span data-stu-id="4d022-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="4d022-105">فيما يلي بعض أمثلة الأشياء التي يمكنك إنشاء مجموعات أوامر عمل لها:</span><span class="sxs-lookup"><span data-stu-id="4d022-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="4d022-106">لأطقم العمل، على سبيل المثال، طاقم الصيانة A أو طاقم الصيانة B</span><span class="sxs-lookup"><span data-stu-id="4d022-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="4d022-107">المهارات المهنية، مثل عمال الكهرباء أو السباكة</span><span class="sxs-lookup"><span data-stu-id="4d022-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="4d022-108">المواقع الفعلية</span><span class="sxs-lookup"><span data-stu-id="4d022-108">Physical locations</span></span>  

- <span data-ttu-id="4d022-109">الجداول الزمنية، مثل أسابيع أو فترات أخرى</span><span class="sxs-lookup"><span data-stu-id="4d022-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="4d022-110">حسب الحاجة، يمكنك وضع أمر عمل واحد في مجموعات أوامر العمل متعددة.</span><span class="sxs-lookup"><span data-stu-id="4d022-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="4d022-111">إنشاء مجموعة أوامر عمل</span><span class="sxs-lookup"><span data-stu-id="4d022-111">Create a work order pool</span></span>

<span data-ttu-id="4d022-112">في **جميع مجموعات أوامر العمل** أو صفحة قائمة **مجموعات أوامر العمل النشطة**، يمكنك الحصول على نظرة عامة على مجموعات أوامر العمل وإنشاء مجموعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="4d022-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="4d022-113">حدد **إدارة الأصول** > **عام** > **مجموعات أوامر العمل** > **جميع مجموعات أوامر العمل** أو **مجموعات أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="4d022-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="4d022-114">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="4d022-114">Select **New**.</span></span>

3. <span data-ttu-id="4d022-115">في الحقل **الوعاء**، أدخل معرفًا لمجموعة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="4d022-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="4d022-116">في حقل **الاسم**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="4d022-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="4d022-117">قم بتعيين الخيار **نشط** على **نعم** للإشارة إلى أن مجموعة أمر العمل نشطة.</span><span class="sxs-lookup"><span data-stu-id="4d022-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="4d022-118">قم بتعيين الخيار **حذف علاقات أوامر العمل** على **نعم** إذا أردت أن تتم إزالة أوامر العمل بشكل تلقائي من مجموعة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="4d022-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="4d022-119">في الحقل **حذف حالة دورة الحياة**، حدد حالة دورة حياة أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="4d022-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="4d022-120">على سبيل المثال، يمكن تعيين حالة دورة حياة أمر العمل لحذف العلاقات بمجموعات أوامر العمل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="4d022-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="4d022-121">يمكنك بدء إضافة أوامر العمل إلى مجموعة أوامر العمل على الفور.</span><span class="sxs-lookup"><span data-stu-id="4d022-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="4d022-122">على علامة التبويب السريعة **أوامر العمل**، حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="4d022-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="4d022-123">في الحقل **أمر العمل**، حدد أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="4d022-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="4d022-124">يتم عندئذٍ تحديث الحقول المرتبطة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="4d022-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="4d022-125">كرر الخطوات من 8 إلى 9 لإضافة مزيد من أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="4d022-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="4d022-126">إذا كانت أوامر العمل التي قمت بإضافتها يجب تنفيذها ببترتيب معين، ففي حقل **‏‫ترتيب الفرز**، يمكنك إدخال الأرقام **1** و **2** و **3** وهكذا لتحديد ذلك الأمر.</span><span class="sxs-lookup"><span data-stu-id="4d022-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="4d022-127">لعرض قائمة بجميع أوامر العمل المضمنة في مجموعة أمر العمل، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل** في مجموعة **عرض مجموعة أمر العمل المرتبطة**، حدد **أوامر العمل** لفتح صفحة قائمة **جميع أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="4d022-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="4d022-128">لحساب القدرة الإنتاجية وعرضها لجدول الصيانة وأوامر العمل غير المجدولة وأوامر العمل المجدولة، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل**، في مجموعة **عرض مجموعة أمر العمل المرتبطة**، حدد **القدرة الإنتاجية** لفتح مربع الحوار **حساب القدرة الإنتاجية**.</span><span class="sxs-lookup"><span data-stu-id="4d022-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="4d022-129">لحساب التنبؤات وعرضها للأصناف (قطع الغيار والأصناف المطلوبة الأخرى) المرتبطة بجدول الصيانة وأوامر العمل غير المجدولة وأوامر العمل المجدولة، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل**، في مجموعة **عرض مجموعة أمر العمل المرتبطة**، حدد **‏‫التنبؤ بالأصناف‬** لفتح مربع الحوار **‏‫حساب تنبؤ العنصر‬**.</span><span class="sxs-lookup"><span data-stu-id="4d022-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="4d022-130">لعرض قائمة بطلبات الشراء المرتبطة بأوامر العمل في مجموعة أمر العمل، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل** في مجموعة **التدبير‬**، حدد **‏‫طلب الشراء لأمر العمل‬** لفتح صفحة قائمة **‏‫طلب الشراء لأمر العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="4d022-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="4d022-131">لعرض قائمة بأوامر الشراء المرتبطة بأوامر العمل في مجموعة أمر العمل، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل** في مجموعة **التدبير‬**، حدد **‏‫‏‫شراء أمر العمل‬** لفتح صفحة قائمة **‏‫‏‫شراء أمر العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="4d022-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="4d022-132">عندما لا تعود مجموعة أوامر العمل ذات صلة بتخطيط عملك، قم بتعيين الخيار **نشط** لتلك المجموعة إلى**لا** في طريقة عرض القائمة بصفحة **مجموعة أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="4d022-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="4d022-133">لحذف جميع بنود أمر العامل، قم بتعيين الخيار **حذف علاقات أوامر العمل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="4d022-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="4d022-134">ويعد هذا الخيار مفيدًا إذا كنت ترغب على سبيل المثال في إنشاء مجموعة فارغة يمكنك استخدامها لاحقا لأوامر العمل الأخرى.</span><span class="sxs-lookup"><span data-stu-id="4d022-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="4d022-135">تذكر تعيين الخيار **حذف علاقات أوامر العمل** على **لا** إذا كنت جاهزًا لاستخدام مجموعة أوامر العمل لإنشاء علاقات أوامر عمل جديدة في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="4d022-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="4d022-136">يوضح الرسم التوضيحي المبين أدناه مثال لصفحة قائمة **مجموعة أمر العمل‬**.</span><span class="sxs-lookup"><span data-stu-id="4d022-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![الشكل 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="4d022-138">إضافة أمر عمل إلى مجموعة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="4d022-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="4d022-139">كما هو موضح في القسم السابق، يمكنك إضافة أوامر العمل إلى مجموعة أوامر العمل عندما تقوم بإنشاء تلك المجموعة.</span><span class="sxs-lookup"><span data-stu-id="4d022-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="4d022-140">يمكنك أيضا إضافة أوامر العمل إلى مجموعة أمر عمل في صفحة قائمة **جميع أوامر العمل** أو  **أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="4d022-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="4d022-141">حدد أمر العمل ثم في جزء الإجراءات، من علامة التبويب **أمر العمل**، في مجموعة **صيانة‬** ، حدد **مجموعة أمر العمل**.</span><span class="sxs-lookup"><span data-stu-id="4d022-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="4d022-142">حدد أمر العمل في القائمة، وانقر فوق **مجموعة أوامر العمل**.</span><span class="sxs-lookup"><span data-stu-id="4d022-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="4d022-143">في مربع الحوار **صيانة مجموعة أمر العمل** في الحقل **إضافة/إزالة**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="4d022-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="4d022-144">في الحقل **الوعاء**، حدد مجموعة‏‎ أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="4d022-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="4d022-145">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4d022-145">Select **OK**.</span></span>

6. <span data-ttu-id="4d022-146">لوضع أمر العمل الذي قمت بإضافته بترتيب معين في مجموعة أمر العمل، في **جميع مجموعات أوامر العمل** أو صفحة قائمة **‏‫مجموعات أوامر العمل النشطة‬**، حدد المجموعة، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="4d022-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="4d022-147">ثم في الصفحة **مجموعة أمر العمل**على علامة التبويب السريعة **أوامر العمل** استخدم الحقل **ترتيب الفرز** لتعديل ترتيب الفرز الخاص بأوامر العمل المضمنة في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="4d022-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="4d022-148">لإزالة أمر عمل من مجموعة أمر العمل، كرر تلك الخطوات، ولكن حدد **إزالة** في الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="4d022-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

