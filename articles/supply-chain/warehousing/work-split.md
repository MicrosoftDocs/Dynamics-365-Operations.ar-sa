---
title: تقسيم العمل
description: يوفر هذا الموضوع معلومات حول وظيفة تقسيم العمل. تتيح هذه الوظيفة تقسيم أوامر العمل الكبيرة إلى العديد من أوامر العمل الصغيرة والتي يمكنك تعيينها بعد ذلك للعاملين المستودع المتعددين. وبهذه الطريقة ، يمكن انتقاء نفس العمل في نفس الوقت من خلال العديد من عمال المستودع.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/05/2020
ms.locfileid: "4421842"
---
# <a name="work-split"></a><span data-ttu-id="0c4ad-105">تقسيم العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-105">Work split</span></span>

<span data-ttu-id="0c4ad-106">تتيح وظيفة تقسيم العمل تقسيم معرفات العمل الكبير (معرفات العمل التي تحتوي على سطور مختلفة) إلى العديد من أوامر العمل الصغيرة والتي يمكنك تعيينها بعد ذلك للعاملين المتعددين في المستودع.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="0c4ad-107">وبهذه الطريقة، يمكن انتقاء رقم إنشاء العمل في نفس الوقت من خلال العديد من عمال المستودع.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c4ad-108">يمكنك تقسيم أوامر العمل التي تكون حالتها *مفتوح* أو *قيد التقدم* فقط.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="0c4ad-109">تشغيل وظيفة تقسيم العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-109">Turn on the work split functionality</span></span>

<span data-ttu-id="0c4ad-110">قبل ان تتمكن من استخدام وظيفة تقسيم العمل ، يجب تشغيل ميزه وميزه المتطلبات الاساسيه الخاصة بها في النظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="0c4ad-111">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزات وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="0c4ad-112">أولا ، قم بتشغيل ميزه *حظر العمل المطلوب علي مستوي المؤسسة* إذا لم يتم تشغيلها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="0c4ad-113">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="0c4ad-114">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="0c4ad-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0c4ad-115">**اسم الميزة:** *حظر العمل على مستوى المؤسسة*</span><span class="sxs-lookup"><span data-stu-id="0c4ad-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="0c4ad-116">عند تنشيط هذه الميزة ، يتم تطبيق ترقيه البيانات تلقائيا بعد ان يتم تشغيل الميزة عبر جميع الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="0c4ad-117">بعد ذلك ، قم بتشغيل ميزه *تقسيم العمل*، والتي تكون مدرجه بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="0c4ad-118">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="0c4ad-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0c4ad-119">**اسم الميزة:** *تقسيم العمل*</span><span class="sxs-lookup"><span data-stu-id="0c4ad-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="0c4ad-120">تحسينات علي تفاصيل العمل وكافة صفحات العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="0c4ad-121">تضيف ميزه *تقسيم العمل* الزرين التاليين إلى علامة التبويب **العمل** في جزء الإجراءات في **تفاصيل العمل** وصفحات **كل العمل**:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="0c4ad-122">**تقسيم العمل** – قسّم معرّف العمل إلى معرّفات عمل صغيرة متعددة يمكن معالجتها بواسطة عاملين منفصلين.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="0c4ad-123">**إلغاء جلسة تقسيم العمل** - قم بإلغاء جلسة عمل تقسيم العمل وقم باتاحه العمل للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="0c4ad-124">![زرا تقسيم العمل وإلغاء جلسة عمل تقسيم العمل](media/Work_split_buttons.png "زرا تقسيم العمل وإلغاء جلسة عمل تقسيم العمل")</span><span class="sxs-lookup"><span data-stu-id="0c4ad-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c4ad-125">لن يتوفر الزر **تقسيم العمل** إذا تحققت اي من الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="0c4ad-126">حاله العمل شيئا غير *مفتوح* أو *قيد التقدم*.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="0c4ad-127">يقترن معرف الحاوية بمعرف العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="0c4ad-128">(لا يمكن تقسيم الحاوية بشكل منظم ، لأنها تتطلب إجراءات فعليه.)</span><span class="sxs-lookup"><span data-stu-id="0c4ad-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="0c4ad-129">العمل مقترن بنظام المجموعة.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="0c4ad-130">نوع أمر العمل هو شيء آخر غير أحد الأنواع التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="0c4ad-131">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="0c4ad-131">Sales orders</span></span>
>    - <span data-ttu-id="0c4ad-132">انتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="0c4ad-132">Raw material picking</span></span>
>    - <span data-ttu-id="0c4ad-133">مشكلة في النقل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-133">Transfer issue</span></span>
>
> - <span data-ttu-id="0c4ad-134">يتم حاليا تقسيم العمل بواسطة مستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-134">The work is currently being split by another user.</span></span> <span data-ttu-id="0c4ad-135">إذا حاولت فتح صفحه التقسيم للعمل الذي يتم تقسيمه بالفعل بواسطة مستخدم آخر ، ستتلقى رسالة الخطا التالية: " \#\#\#\#يتم الآن تقسيم العمل بالمعرف.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="0c4ad-136">أعد المحاولة بعد بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-136">Retry in a few minutes.</span></span> <span data-ttu-id="0c4ad-137">إذا استمر ظهور هذه الرسالة ، فاتصل بالمشرف."</span><span class="sxs-lookup"><span data-stu-id="0c4ad-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="0c4ad-138">يوضح سبب حظر العمل الجديد ، *عمل تقسيم* ، عندما يكون معرف العمل اثناء عمليه التقسيم.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="0c4ad-139">يظهر كل من صفحه **العمل المنقسمة** وفي تطبيق المستودع في حاله محاولة أحد المستخدمين تشغيل العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="0c4ad-140">عند استخدام أسباب الحظر ، يتم تغيير اسم حقل **الموجه المحظورة** من معرف العمل إلى **محظور**.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="0c4ad-141">بدء تقسيم عمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-141">Initiate a work split</span></span>

<span data-ttu-id="0c4ad-142">تضيف الميزة صفحه **تقسيم عمل** جديده تتيح للمستخدمين تقسيم بنود العمل من معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="0c4ad-143">عند فتح الصفحة لأول مره ، فانها تعرض البنود التي تحتوي علي حاله العمل *مفتوح* ومتاح لتقسيمها.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="0c4ad-144">في جزء الاجراء ، حدد **تقسيم العمل** لمعالجه العمل المحدد.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="0c4ad-145">لتقسيم العمل ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="0c4ad-146">افتح إحدى صفحات العمل التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="0c4ad-147">**تفاصيل العمل** (**إدارة المستودعات \> العمل \> تفاصيل العمل**)</span><span class="sxs-lookup"><span data-stu-id="0c4ad-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="0c4ad-148">**كل العمل** (**إدارة المستودعات \> العمل \> كل العمل**)</span><span class="sxs-lookup"><span data-stu-id="0c4ad-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="0c4ad-149">في الشبكة ، حدد معرف العمل المراد تقسيمه.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="0c4ad-150">يجب تعيين حقل **نوع أمر العمل** إلى أحدي القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="0c4ad-151">أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="0c4ad-151">Sales orders</span></span>
    - <span data-ttu-id="0c4ad-152">انتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="0c4ad-152">Raw material picking</span></span>
    - <span data-ttu-id="0c4ad-153">مشكلة في النقل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-153">Transfer issue</span></span>

1. <span data-ttu-id="0c4ad-154">في جزء الإجراءات، ضمن علامة التبويب **العمل**، في مجموعة **العمل**، حدد **تقسيم العمل**.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="0c4ad-155">تظهر صفحه **تقسيم العمل** وتظهر بنود العمل المفتوحة والمتاحة ليتم تقسيمها.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="0c4ad-156">بشكل افتراضي ، يتم عرض بنود العمل المتاحة فقط.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="0c4ad-157">لعرض كافة البنود لمعرف العمل (علي سبيل المثال ، الأسطر التي لها نوع العمل *تخزين*)، حدد خانه الاختيار **إظهار كافة البنود** الموجودة اعلي الشبكة.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="0c4ad-158">تظهر الرسالة التالية: "لا يمكن للمستخدمين معالجه بنود العمل حتى تنتهي من التقسيم وإغلاق هذه الصفحة."</span><span class="sxs-lookup"><span data-stu-id="0c4ad-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="0c4ad-159">سيتم تعيين حقل **سبب حظر العمل** للعمل الحالي علي *تقسيم العمل*، سيتم حظر العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="0c4ad-160">![سبب الحظر](media/Blocking_reason.png "سبب الحظر")</span><span class="sxs-lookup"><span data-stu-id="0c4ad-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="0c4ad-161">حدد البنود التي ستتم ازالتها من معرف العمل الحالي وأضف إلى معرف عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="0c4ad-162">تقع الأحداث التالية:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-162">The following events occur:</span></span>

    - <span data-ttu-id="0c4ad-163">عند تقسيم العمل ، يتم إلغاء البند أو البنود المحددة من معرف العمل الأصلي ثم نسخها إلى معرف عمل جديد.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="0c4ad-164">يتم الاحتفاظ ببنيه قالب العمل الموجود وموقع الوضع (وكذلك أزواج الانتقاء/الوضع المستقبلية).</span><span class="sxs-lookup"><span data-stu-id="0c4ad-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="0c4ad-165">يتم نسخ قيم حقول معرفات العمل التالية من العمل الأصلي إلى العمل الجديد:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="0c4ad-166">معرف الحِمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-166">Load ID</span></span>
        - <span data-ttu-id="0c4ad-167">معرف الشحنة</span><span class="sxs-lookup"><span data-stu-id="0c4ad-167">Shipment ID</span></span>
        - <span data-ttu-id="0c4ad-168">نوع أمر العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-168">Work order type</span></span>
        - <span data-ttu-id="0c4ad-169">رقم الطلب</span><span class="sxs-lookup"><span data-stu-id="0c4ad-169">Order number</span></span>
        - <span data-ttu-id="0c4ad-170">الموقع</span><span class="sxs-lookup"><span data-stu-id="0c4ad-170">Site</span></span>
        - <span data-ttu-id="0c4ad-171">المستودع</span><span class="sxs-lookup"><span data-stu-id="0c4ad-171">Warehouse</span></span>
        - <span data-ttu-id="0c4ad-172">أولوية العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-172">Work priority</span></span>
        - <span data-ttu-id="0c4ad-173">معرف وعاء العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-173">Work pool ID</span></span>
        - <span data-ttu-id="0c4ad-174">معرف الموجة</span><span class="sxs-lookup"><span data-stu-id="0c4ad-174">Wave ID</span></span>
        - <span data-ttu-id="0c4ad-175">رقم إنشاء العمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-175">Work creation number</span></span>

    - <span data-ttu-id="0c4ad-176">لم يتم نسخ الحقول التالية إلى معرف العمل الجديد:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="0c4ad-177">**معرف العمل** – يتم إنشاء معرف عمل جديد من التسلسل الرقمي المناسب.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="0c4ad-178">**حاله العمل** – تم تعيين هذا الحقل علي *مفتوح*.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="0c4ad-179">**مؤمن بواسطة** – يتم تعيين هذا الحقل أولا علي فارغ.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="0c4ad-180">**معرف لوح الترخيص الهدف** – يتم ترك هذا الحقل فارغا.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="0c4ad-181">**تاريخ ووقت الإنشاء** – يتم تعيين هذا الحقل إلى التاريخ والوقت الحاليين.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="0c4ad-182">**موجه محظورة/مجمدة** - تتم إعادة احتساب هذا الحقل لمعرف العمل الأصلي ومعرف العمل الجديد.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="0c4ad-183">في جزء الإجراءات، حدد **تقسيم العمل**.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="0c4ad-184">اثناء تقسيم العمل، يتم عرض الرسالة التالية: "تتم الآن معالجه عمل تقسيم العمل".</span><span class="sxs-lookup"><span data-stu-id="0c4ad-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="0c4ad-185">في حين ان هذه الرسالة مرئية ، يمكنك إلغاء العملية بتحديد **إلغاء الأمر** في مربع الرسالة.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="0c4ad-186">إذا تم إلغاء تحديد خانه الاختيار **إظهار كافة البنود**، فلن يظهر البند الذي تم تقسيمه وتم إلغاؤه بعد ذلك في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="0c4ad-187">في حاله تحديد خانه الاختيار ، يجب ان تري ان قيمه حقل **حاله العمل** الخاصة بهذا السطر قد تغيرت إلى *تم إلغاؤها*.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="0c4ad-188">يظهر الاعلام التالي للاشاره إلى انه تم إنشاء معرف العمل الجديد: "تم \#\#\#\#إنشاء العمل بالتقسيم من العمل الأصلي \#\#\#\#."</span><span class="sxs-lookup"><span data-stu-id="0c4ad-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="0c4ad-189">سيتم تعديل بنود العمل الأخرى من معرف العمل الأصلي (مثل بنود *التخزين*) وفقا لما هو مطلوب لإظهار بنود العمل التي تم إلغاؤها.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="0c4ad-190">علي سبيل المثال ، إذا كان معرف العمل الأصلي يحتوي علي بند *تخزين* لكميه مقدارها 15، وكانت بنود *الانتقاء* التي تم إلغاء الكمية الاجماليه لها هو 10، ستكون كميه *التخزين* الجديدة في معرف العمل الأصلي هي 5 الآن.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="0c4ad-191">ولن يتم تعيين العمل الجديد فورا إلى اي مستخدم.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="0c4ad-192">ومع ذلك ، يمكنك تعيينها إلى مستخدم الآن ، كما هو مطلوب ، باستخدام الوظيفة القياسية لصفحه **تفاصيل العمل**.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c4ad-193">يمكنك تقسيم معرفات العمل التي تحتوي علي بندين متوفرين أو أكثر من بنود العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="0c4ad-194">إذا قمت بتحديد **تقسيم العمل** عند وجود سطر عمل واحد فقط ، ستتلقى رسالة الخطا التالية: "يجب ان يبقي حد العمل الواحد علي الأقل في العمل الاولي."</span><span class="sxs-lookup"><span data-stu-id="0c4ad-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="0c4ad-195">في هذه الحالة ، لن يحدث اي تقسيم.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="0c4ad-196">إنهاء تقسيم عمل</span><span class="sxs-lookup"><span data-stu-id="0c4ad-196">Finish a work split</span></span>

<span data-ttu-id="0c4ad-197">لإنهاء تقسيم العمل، يجب أزاله سبب حظر *تقسيم العمل*.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="0c4ad-198">هناك طريقتان للقيام بهذه الخطوة:</span><span class="sxs-lookup"><span data-stu-id="0c4ad-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="0c4ad-199">يقوم المستخدم الذي يقوم بتقسيم العمل بإغلاق الصفحة **تقسيم العمل** عن طريق تحديد الزر **إغلاق** ( **X**) الموجود في الركن الأيمن العلوي.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="0c4ad-200">وعند إغلاق الصفحة، ستتم أزاله سبب حظر *تقسيم العمل*.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="0c4ad-201">ستتم إعادة احتساب الحالة *محظور* لهذا العمل، وفي حاله عدم وجود أسباب حظر متبقية لهذا العمل ، سيتم إلغاء حظر العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="0c4ad-202">يقوم اي مستخدم بفتح "معرف العمل" وتحديد الزر **إلغاء جلسة تقسيم العمل** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="0c4ad-203">ستتم أزاله سبب حظر *تقسيم العمل*، وسيتم إعادة احتساب الحالة *المحظورة* لهذا العمل تماما كما هو الحال عند إغلاق صفحه **تقسيم العمل**.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="0c4ad-204">بعد أزاله سبب حظر *تقسيم العمل*، يمكن تشغيل العمل علي الجهاز المحمول بشرط ان يتم تعيين الحالة **المحظورة** إلى *لا* علي معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="0c4ad-205">حظر المستخدم علي تطبيق المستودع</span><span class="sxs-lookup"><span data-stu-id="0c4ad-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="0c4ad-206">إذا حاولت فتح صفحه تقسيم العمل الذي يتم تقسيمه بالفعل بواسطة مستخدم آخر ، ستتلقى رسالة الخطا التالية: "\#\#\#\#يتم الآن تقسيم معرف العمل.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="0c4ad-207">إذا تلقيت هذه الرسالة ، فحدد **إلغاء الأمر**.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="0c4ad-208">يمكنك بعد ذلك متابعه معالجه العمل الآخر.</span><span class="sxs-lookup"><span data-stu-id="0c4ad-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="0c4ad-209">العمليات المحظورة الأخرى</span><span class="sxs-lookup"><span data-stu-id="0c4ad-209">Other blocked operations</span></span>

<span data-ttu-id="0c4ad-210">ستفشل إيه عمليات تقوم بتعديل بنود العمل أو حركات مخزون العمل أو ارتباطات الاستعاضة المرتبطة بالعمل الذي يتم تقسيمه ، ستظهر رسالة الخطا التالية: "يتم الآن تقسيم العمل ذي المعرف \#\#\#\# ."</span><span class="sxs-lookup"><span data-stu-id="0c4ad-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
