---
title: دورات الصيانة
description: يشرح هذا الموضوع دورات الصيانة في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4c9a2fee7d43142f8bb17f4e819c9949a2a20c41
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570020"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="af8f9-103">دورات الصيانة</span><span class="sxs-lookup"><span data-stu-id="af8f9-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="af8f9-104">في **إدارة الأصول**، يمكنك إنشاء دورات الصيانة لأصول مختلفة تحتاج إلى تنفيذ مهمة مماثلة عليها على فترات منتظمة</span><span class="sxs-lookup"><span data-stu-id="af8f9-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="af8f9-105">على سبيل المثال، مهام التشحيم أو فحص السلامة التي يجب تنفيذها على عدد من الأجهزة خلال الفترات الزمنية نفسها.</span><span class="sxs-lookup"><span data-stu-id="af8f9-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="af8f9-106">يجب أولاً إنشاء دورة صيانة، بما في ذلك الأصول التي تتطلب نموذج مهمة الصيانة نفسه.</span><span class="sxs-lookup"><span data-stu-id="af8f9-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="af8f9-107">بعد ذلك، يمكنك جدولة دورات الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="af8f9-108">وعند إكمال جدول دورات الصيانة، يمكنك الاطلاع على كافة سجلات المهام المرتبط بدورة الصيانة في **جدول الصيانة بكامله** و**بنود جدول الصيانة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="af8f9-109">يمكن أيضًا إعداد دورات الصيانة على مواقع العمل التي يجب إكمالها على الأصول المثبتة في موقع العمل عند إنشاء أمر العمل الذي يستند إلى دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="af8f9-110">راجع [إنشاء مواقع عمل‬](../functional-locations/create-functional-locations.md) لمزيد من المعلومات حول إعداد دورات الصيانة على مواقع العمل.</span><span class="sxs-lookup"><span data-stu-id="af8f9-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="af8f9-111">إعداد دورة الصيانة</span><span class="sxs-lookup"><span data-stu-id="af8f9-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="af8f9-112">انقر فوق **إدارة الأصول** > **الإعداد** > **الصيانة الوقائية** > **دورات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="af8f9-113">انقر فوق **جديد** لإنشاء دورة صيانة جديدة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="af8f9-114">أدخل معرفًا في حقل **دورة الصيانة** واسمًا لدورة الصيانة في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="af8f9-115">في الحقل **تاريخ البدء**، حدد تاريخ بدء دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="af8f9-116">في الحقلين **الانتهاء ضمن الأيام** و**الانتهاء ضمن الساعات**، يمكنك إدخال تاريخ الانتهاء المتوقع بالأيام أو الساعات.</span><span class="sxs-lookup"><span data-stu-id="af8f9-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="af8f9-117">يتم حساب تاريخ الانتهاء المتوقع بالنسبة إلى تاريخ البدء، والذي يتم حسابه عند إنشاء بنود جدولة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="af8f9-118">على سبيل المثال، يمكنك إدخال "7" في حقل **الانتهاء ضمن الأيام** للإشارة إلى أنه يجب إكمال المهمة ذات الصلة خلال أسبوع من تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="af8f9-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="af8f9-119">حدد "نعم" على زر التبديل **إنشاء تلقائي** إذا كان يجب إنشاء أوامر العمل تلقائيًا من بنود جدول الصيانة التي يتم إنشاؤها من دورة الصيانة هذه.</span><span class="sxs-lookup"><span data-stu-id="af8f9-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="af8f9-120">في الحقل **نوع أمر العمل**، حدد نوع أمر العمل المطلوب استخدامه على أوامر العمل التي تم إنشاؤها لدورة الصيانة هذه.</span><span class="sxs-lookup"><span data-stu-id="af8f9-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="af8f9-121">في الحقل **مستوى الخدمة**، حدد مستوى خدمة أمر العمل المطلوب استخدامه على أوامر العمل التي تم إنشاؤها لدورة الصيانة هذه.</span><span class="sxs-lookup"><span data-stu-id="af8f9-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="af8f9-122">على علامة التبويب السريعة **بنود الأصول**، انقر فوق **إضافة** لإضافة أصل إلى دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="af8f9-123">يتم إدخال رقم بند بشكل تلقائي في حقل **رقم البند** للإشارة إلى تسلسل الأصول في دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="af8f9-124">حدد الأصل في حقل **الأصل**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="af8f9-125">حدد نوع مهمة الصيانة للأصل في الحقل **نوع مهمة الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="af8f9-126">حدد **متغير نوع مهمة الصيانة** و**المعاملات** ذات الصلة بنوع مهمة الصيانة، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="af8f9-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="af8f9-127">حدد التكرار (يوم، أسبوع، غير ذلك) في الحقل‏‎ **نوع الفترة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="af8f9-128">في الحقل **تكرار الفترة**، أدخل عدد مرات التكرار لدورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="af8f9-129">مثال: إذا قمت بتحديد "يوم" في حقل **نوع الفترة**، وأدخلت الرقم "7" في هذا الحقل، سيتم إنشاء بنود دورة صيانة جديدة أثناء جدولة الصيانة الوقائية مرة واحدة في الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="af8f9-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="af8f9-130">حدد تاريخ بدء للأصل ليتم تضمينه في دورة الصيانة في الحقل **تاريخ البدء**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="af8f9-131">قد يختلف هذا التاريخ عن تاريخ البدء المحدد على دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="af8f9-132">كرر الخطوات من 9 إلى 16 لإضافة المزيد من الأصول إلى دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="af8f9-133">على علامة التبويب السريعة **بنود موقع العمل**، انقر فوق **إضافة** لإضافة موقع عمل إلى دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="af8f9-134">يمكنك مراجعة وصف الحقول ذات الصلة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="af8f9-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="af8f9-135">تتوفر الحقول نفسها لإنشاء بند أصل، ولكن يمكنك أيضًا إضافة **شركة مصنعة** و**نموذج** لموقع عمل، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="af8f9-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="af8f9-136">إذا حددت فقط موقع عمل على بند، ولكن من دون إجراء تحديدات في **نوع الأصل** و**الشركة المصنعة** و**النموذج** و**نوع مهمة الصيانة** و**متغير نوع مهمة الصيانة** و**المعاملات**، فسيتم تضمين جميع الأصول المرتبطة بموقع العمل هذا عند جدولة الصيانة في دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="af8f9-137">على علامة التبويب السريعة **المجموعات**، انقر فوق **إضافة** لتحديد مجموعة أوامر عمل لتضمينها في في دورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="af8f9-138">يمكن ربط العديد من مجموعات أوامر العمل بدورة صيانة واحدة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="af8f9-139">احفظ إعدادك.</span><span class="sxs-lookup"><span data-stu-id="af8f9-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="af8f9-140">تعرض حقول **الأصول** و**البنود** في مجموعة **التفاصيل** على علامة التبويب السريعة **الرأس** العدد الإجمالي للأصول والبنود ذات الصلة بدورة الصيانة المحددة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="af8f9-141">يُبين الرسم التوضيحي التالي ويضرب مثالًا لدورة الصيانة التي تحتوي على ثلاثة أصول.</span><span class="sxs-lookup"><span data-stu-id="af8f9-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![الشكل 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="af8f9-143">دورات الصيانة المجدولة</span><span class="sxs-lookup"><span data-stu-id="af8f9-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="af8f9-144">عند إعداد دورة صيانة، تقوم بتشغيل مهمة جدولة لجدولة جميع المهام المرتبطة بدورة الصيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="af8f9-145">انقر فوق **إدارة الأصول** > **دوري** > **الصيانة الوقائية** > **جدولة دورات الصيانة** أو **إدارة الأصول** > **عام** > **جدول الصيانة** > **جدول الصيانة** أو **بنود جدول الصيانة المفتوحة** أو **مجموعات جداول الصيانة المفتوحة** > حدد بند جدول صيانة في القائمة > زر **دورات الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="af8f9-146">في الحقل‏‎ **الفترة**، حدد نوع الفترة التي يجب استخدامها لوظيفة الجدولة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="af8f9-147">في الحقل **تكرار الفترة**، أدخل عدد الفترات الزمنية المطلوب تضمينها في وظيفة الجدولة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="af8f9-148">بداية الجدولة هي التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="af8f9-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="af8f9-149">حدد "نعم" على زر التبديل زر **إنشاء تلقائي**  إذا كان يجب إنشاء أمر عمل تلقائيًا استنادًا إلى دورة صيانة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="af8f9-150">إذا تم تعيين زر التبديل هذا إلى "نعم" وأيضًا زر التبديل **تشغيل تلقائي** إلى "نعم" على دورة الصيانة في نموذج **دورات الصيانة**، فسيتم أيضًا إنشاء أوامر العمل استنادًا إلى بنود دورة الصيانة وبنود جدول الصيانة مع الحالة "تم إنشاء أمر العمل".</span><span class="sxs-lookup"><span data-stu-id="af8f9-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="af8f9-151">إذا تم تعيين زر واحد فقط من أزرار التبديل **إنشاء تلقائي** إلى "نعم"، في هذه القائمة المنسدلة أو في **دورات الصيانة**، فسيتم إنشاء بنود جدول الصيانة فقط مع الحالة "تم الإنشاء".</span><span class="sxs-lookup"><span data-stu-id="af8f9-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="af8f9-152">في هذه الحالة، لا يتم إنشاء أوامر عمل.</span><span class="sxs-lookup"><span data-stu-id="af8f9-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="af8f9-153">إذا لزم الأمر، يمكنك تحديد دورات معينة أو تاريخ بدء آخر لوظيفة الجدولة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="af8f9-154">انقر فوق‏‎ **تصفية**، وأضف الدورات التي سيتم تضمينها.</span><span class="sxs-lookup"><span data-stu-id="af8f9-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="af8f9-155">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-155">Click **OK**.</span></span>

7. <span data-ttu-id="af8f9-156">يمكنك الآن رؤية مهام دورات الصيانة في **إدارة الأصول** > **عام** > **جدول الصيانة** > **جدول الصيانة بكامله** أو **بنود جدول الصيانة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="af8f9-157">إذا كانت دورات الصيانة المجدولة مرتبطة بمجموعة أوامر عمل أخرى، فسترى أيضًا بنود جدول الصيانة في  **مجموعات جدول الصيانة المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="af8f9-158">سيكون نوع المرجع لبنود جدول الصيانة التي تم إنشاؤها من دورة "دورات صيانة".</span><span class="sxs-lookup"><span data-stu-id="af8f9-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="af8f9-159">يُبين الرسمان التوضيحيان أدانه مهمة الجدول في مربع حوار **دورات الصيانة المُجدولة**، وبنود جدول الصيانة التي تم إنشاؤها في **كل جداول الصيانة** بناءً على مهمة الجدولة هذه.</span><span class="sxs-lookup"><span data-stu-id="af8f9-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![الشكل 2](media/14-preventive-maintenance.png)

![الشكل 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="af8f9-162">عند إنشاء أوامر العمل يدويًا على الأصول التي تتم تغطيتها بواسطة ضمان المورّد، يتم عرض مربع حوار لإعلام المستخدم بالضمان.</span><span class="sxs-lookup"><span data-stu-id="af8f9-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="af8f9-163">ويمكن بعد ذلك إلغاء إنشاء أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="af8f9-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="af8f9-164">ويتم حذف عملية الفحص الخاصة بعلاقة الضمان لأوامر العمل التي يتم إنشاؤها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="af8f9-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="af8f9-165">يمكنك إعداد وظيفة دفعية على علامة التبويب السريعة **تشغيل في الخلفية** لجدولة الدورات على فترات زمنية منتظمة.</span><span class="sxs-lookup"><span data-stu-id="af8f9-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="af8f9-166">إذا تم تضمين دورة في مجموعات أوامر عمل متعددة، (راجع [مجموعات أوامر العمل](../work-orders/work-order-pools.md))، يظهر سجل واحد لكل مجموعة في **مجموعات جدول الصيانة المفتوحة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="af8f9-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="af8f9-167">ويتم ذلك لتحسين خيارات التصفية لمجموعات أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="af8f9-167">This is done to optimize the filtering options for work order pools.</span></span>

