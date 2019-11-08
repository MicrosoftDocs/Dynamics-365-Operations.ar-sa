---
title: تحرير أدلة وقوالب الإعداد في  Dynamics 365 Talent - Onboard
description: يشرح هذا الموضوع كيفية إضافة أنشطة ومعلومات أخرى إلى أدلة وقوالب الإعداد في  Microsoft Dynamics 365 Talent - Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0f4c68acfe021e736c259e91a40ce7d43d401246
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551992"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a><span data-ttu-id="582b7-103">تحرير أدلة وقوالب الإعداد في  Dynamics 365 Talent - Onboard</span><span class="sxs-lookup"><span data-stu-id="582b7-103">Edit onboarding guides and templates in Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="582b7-104">بعد إنشاء دليل أو قالب إعداد في  Microsoft Dynamics 365 Talent: Onboard، يجب إضافة مقدمة وأنشطة وجهات اتصال وموارد.</span><span class="sxs-lookup"><span data-stu-id="582b7-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="582b7-105">يسمح لك Onboard بتضمين محتوى غني في أدلة الإعداد، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="582b7-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="582b7-106">مقاطع فيديو YouTube</span><span class="sxs-lookup"><span data-stu-id="582b7-106">YouTube videos</span></span>
- <span data-ttu-id="582b7-107">عروض تقديميه من Microsoft Sway</span><span class="sxs-lookup"><span data-stu-id="582b7-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="582b7-108">تطبيقات Microsoft PowerApps</span><span class="sxs-lookup"><span data-stu-id="582b7-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="582b7-109">مقاطع فيديو Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="582b7-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="582b7-110">نماذج Microsoft Forms</span><span class="sxs-lookup"><span data-stu-id="582b7-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="582b7-111">Iframes التي تحتوي على محتوي الويب</span><span class="sxs-lookup"><span data-stu-id="582b7-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="582b7-112">تحرير المقدمات أو الأنشطة المستوردة من قالب</span><span class="sxs-lookup"><span data-stu-id="582b7-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="582b7-113">إذا أنشأت دليل إعداد من قالب، أو استوردت أنشطة من قالب إلى آخر، ستلاحظ وجود الزر **تأمين** على الأنشطة المستوردة.</span><span class="sxs-lookup"><span data-stu-id="582b7-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="582b7-114">تسمى هذه *الأنشطة المدارة*.</span><span class="sxs-lookup"><span data-stu-id="582b7-114">These are called *managed activities*.</span></span>

<span data-ttu-id="582b7-115">[![الأنشطة المدارة](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="582b7-116">عند تحديد نشاط مدار، يمكنك رؤية القالب المصدر في أعلى النشاط.</span><span class="sxs-lookup"><span data-stu-id="582b7-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="582b7-117">[![مصدر النشاط المدار](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="582b7-118">إذا قمت بتحرير نشاط في قالب، سيقوم Onboard بدفع التغييرات إلى كافة القوالب والدلائل غير المرسلة التي تستند إلى هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="582b7-119">إذا حددت دليلاً غير مرسل يستند إلى قالب قمت بتحريره، ثم حددت علامة تبويب **الأنشطة** في الدليل، فسترى إشعارًا يعلمك بأن الدليل قد تغير.</span><span class="sxs-lookup"><span data-stu-id="582b7-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="582b7-120">لتجاهل الإعلام، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="582b7-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="582b7-121">[![إعلام بالتغيير](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="582b7-122">سترى نقطة سوداء بجوار الأنشطة المحدثة.</span><span class="sxs-lookup"><span data-stu-id="582b7-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="582b7-123">[![نشاط متغير](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="582b7-124">لا يمكنك تحرير الأنشطة المدارة خارج القالب الأصلي، باستثناء أضافه معيَّن أو تاريخ استحقاق أو أي معلومات أخرى في القسم الأيسر من النشاط.</span><span class="sxs-lookup"><span data-stu-id="582b7-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="582b7-125">إذا أردت تحرير نشاط مدار، أو إذا لم تكن ترغب في أن يتلقى النشاط تحديثات من القالب الذي أتى منه، فحدد الزر **تأمين** لذلك النشاط.</span><span class="sxs-lookup"><span data-stu-id="582b7-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="582b7-126">سيختفي الزر **تأمين**.</span><span class="sxs-lookup"><span data-stu-id="582b7-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="582b7-127">لن يعود النشاط مدارًا بواسطة القالب الأصلي، وسيتوقف عن تلقي التحديثات من ذلك القالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="582b7-128">لن يتأثر القالب الأصلي بالتحديثات التي تجريها على نشاط ما.</span><span class="sxs-lookup"><span data-stu-id="582b7-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="582b7-129">إذا قمت بحذف نشاط من دليل ودفعت التغييرات من قالب هذا الدليل، فسيبقى النشاط محذوفًا في الدليل.</span><span class="sxs-lookup"><span data-stu-id="582b7-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="582b7-130">لا تُدار جهات الاتصال والموارد بواسطة القوالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="582b7-131">علاوةً على ذلك، فالأقسام لا تُدار، وبالتالي إذا قمت بإضافة قسم أو تحريره في قالب، فلن يتم دفع التغييرات إلى أي أدلة أو قوالب تستخدم هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="582b7-132">إذا قمت بإضافة أنشطة جديدة إلى قالب، سيتم دفع الأنشطة الجديدة إلى الأدلة والقوالب المستندة إلى هذا القالب، وتظهر الأنشطة الجديدة في الأعلى.</span><span class="sxs-lookup"><span data-stu-id="582b7-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="582b7-133">استيراد أنشطة من قالب آخر</span><span class="sxs-lookup"><span data-stu-id="582b7-133">Import activities from another template</span></span>

<span data-ttu-id="582b7-134">يمكنك استيراد أنشطة من قالب واحد أو أكثر إلى دليل أو قالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="582b7-135">حدد الدليل أو القالب الذي تريد تحريره.</span><span class="sxs-lookup"><span data-stu-id="582b7-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="582b7-136">حدد علامة تبويب **الأنشطة‬**.</span><span class="sxs-lookup"><span data-stu-id="582b7-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="582b7-137">حدد علامة التبويب **استيراد** في القسم إلى اليسار.</span><span class="sxs-lookup"><span data-stu-id="582b7-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="582b7-138">[![استيراد أنشطة](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="582b7-139">لمعاينة المهام في علامة تبويب جديدة في المستعرض، حدد الزر **فتح في علامة تبويب جديدة** على أي قالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="582b7-140">[![استيراد أنشطة](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="582b7-141">اسحب القالب المطلوب ثم أفلته في الموقع الموجود في قالب الدليل حيث ترغب في ظهور الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="582b7-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="582b7-142">استمر في تحرير الدليل أو القالب.</span><span class="sxs-lookup"><span data-stu-id="582b7-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="582b7-143">ستحتوي الأنشطة المستوردة على الزر **تأمين**، مما يشير إلى أن هذه الأنشطة تُدار بواسطة القالب الذي استوردتها منه.</span><span class="sxs-lookup"><span data-stu-id="582b7-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="582b7-144">عند إدخال تغييرات على القالب الذي قمت باستيراده، سيتم تحديث هذه الأنشطة في القالب الذي قمت باستيرادها اليه.</span><span class="sxs-lookup"><span data-stu-id="582b7-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="582b7-145">ومع ذلك، لن يتم دفع التغييرات بشكل تلقائي إلى أي أدلة تم إنشاؤها من القالب الذي استوردتها اليه.</span><span class="sxs-lookup"><span data-stu-id="582b7-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="582b7-146">دفع التغييرات من قالب إلى قوالب أو أدلة أخرى</span><span class="sxs-lookup"><span data-stu-id="582b7-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="582b7-147">إذا قمت بتحرير قالب يحتوي على أنشطة مستخدمة في قوالب أو أدلة أخرى، فيجب دفع التغييرات إذا كنت ترغب في ظهورها في القوالب أو الأدلة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="582b7-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="582b7-148">إذا لم تكن متأكدًا من استخدام أنشطة القالب في قوالب أو أدلة أخرى، فحدد علامة التبويب **مستخدم في** لعرض المكان الذي تظهر فيه هذه الأنشطة.</span><span class="sxs-lookup"><span data-stu-id="582b7-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="582b7-149">[![عرض الأدلة والقوالب التي يتم فيها استخدام الأنشطة](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="582b7-150">لدفع التغييرات التي أجريتها:</span><span class="sxs-lookup"><span data-stu-id="582b7-150">To push your changes:</span></span>

1. <span data-ttu-id="582b7-151">احفظ التغييرات عن طريق تحديد الزر **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="582b7-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="582b7-152">إذا لم تفعل ذلك، ستتم مطالبتك بحفظ التغييرات التي قمت بها في الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="582b7-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="582b7-153">حدد **دفع هذه التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="582b7-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="582b7-154">إضافة مقدمة أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="582b7-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="582b7-155">في علامة التبويب **المقدمة**، أدخل عنوانًا لدليلك ورسالة افتتاحيه.</span><span class="sxs-lookup"><span data-stu-id="582b7-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="582b7-156">لاستخدام عينة نص، حدد **استخدام هذه الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="582b7-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="582b7-157">[![علامة التبويب "المقدمة" في قالب Onboard](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="582b7-158">استخدم أزرار التنسيق لتقديم وسيلة شرح للنص، أو لإضافة صور أو ارتباطات.</span><span class="sxs-lookup"><span data-stu-id="582b7-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="582b7-159">حدد **حفظ** لحفظ عملك.</span><span class="sxs-lookup"><span data-stu-id="582b7-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="582b7-160">إضافة أنشطة أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="582b7-160">Add or edit activities</span></span>

1. <span data-ttu-id="582b7-161">في علامة التبويب **الأنشطة**، اسحب العناصر من اليسار إلى منطقة التحرير.</span><span class="sxs-lookup"><span data-stu-id="582b7-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="582b7-162">لتنظيم الدليل في أقسام، اسحب العنصر **قسم جديد** إلى منطقة التحرير، وأدخل اسمًا ووصفًا اختياريًا للقسم.</span><span class="sxs-lookup"><span data-stu-id="582b7-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="582b7-163">إضافة قسم جديد إلى دليل أو قالب إعداد</span><span class="sxs-lookup"><span data-stu-id="582b7-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="582b7-164">لإضافة أنشطة إلى الموظف الجديد، اسحب العنصر **نشاط جديد** إلى منطقة التحرير، ثم أدخل اسمًا ووصفًا للنشاط.</span><span class="sxs-lookup"><span data-stu-id="582b7-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="582b7-165">إضافة نشاط جديد إلى دليل أو قالب إعداد</span><span class="sxs-lookup"><span data-stu-id="582b7-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="582b7-166">أضافه محتوى غني إلى دليل الإعداد:</span><span class="sxs-lookup"><span data-stu-id="582b7-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="582b7-167">لإضافة مقطع فيديو YouTube، اسحب عنصر **YouTube** إلى منطقة التحرير، وأدخل اسمًا ووصفًا للنشاط، ثم أدخل عنوان URL لفيديو YouTube.</span><span class="sxs-lookup"><span data-stu-id="582b7-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="582b7-168">لإضافة رسالة إخبارية أو عرض تقديمي من Sway، اسحب عنصر**Sway** إلى منطقة التحرير، وأدخل اسمًا ووصفًا للنشاط، وأدخل عنوان URL المضمن للرسالة الإخبارية أو العرض التقديمي من Sway.</span><span class="sxs-lookup"><span data-stu-id="582b7-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="582b7-169">لإضافة تطبيق PowerApps، اسحب عنصر **PowerApps** إلى منطقة التحرير، وأدخل اسمًا ووصفًا للنشاط، وحدد تطبيق PowerApps أو أدخل مُعرف تطبيق PowerApps.</span><span class="sxs-lookup"><span data-stu-id="582b7-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="582b7-170">لإضافة مقطع فيديو Microsoft Stream، اسحب عنصر **Microsoft Stream** إلى منطقة التحرير، وأدخل اسمًا ووصفًا للنشاط، ثم أدخل عنوان URL لفيديو Microsoft Stream.</span><span class="sxs-lookup"><span data-stu-id="582b7-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="582b7-171">لإضافة نموذج Microsoft Forms، اسحب عنصر **Microsoft Forms** إلى منطقة التحرير، وأدخل اسمًا ووصفًا للنشاط، وأدخل عنوان URL لنموذج Microsoft Forms، وحدد حجم منطقة الشاشة.</span><span class="sxs-lookup"><span data-stu-id="582b7-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="582b7-172">لإضافة iframe يتضمن محتوى ويب، اسحب عنصر **محتوى ويب (iframe)** إلى منطقة التحرير، وأدخل اسمًا ووصفًا للنشاط، وأدخل عنوان URL لمحتوى الويب وحدد حجم منطقة الشاشة.</span><span class="sxs-lookup"><span data-stu-id="582b7-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="582b7-173">إضافة محتوى غني إلى دليل أو قالب إعداد</span><span class="sxs-lookup"><span data-stu-id="582b7-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="582b7-174">اختياري: في المنطقة الموجودة إلى يسار كل نشاط، قم بتعيين النشاط إلى شخص أو دور معين، وأضف تاريخ استحقاق وجهة اتصال، وعيّن لون فئة.</span><span class="sxs-lookup"><span data-stu-id="582b7-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="582b7-175">عند تعيين نشاط إلى شخص أو دور، يتم إنشاء مهمة لكل فرد.</span><span class="sxs-lookup"><span data-stu-id="582b7-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="582b7-176">تظهر هذه المهمة في قائمة **المهام** في Onboard.</span><span class="sxs-lookup"><span data-stu-id="582b7-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="582b7-177">[![تعيين نشاط في دليل أو قالب إعداد](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="582b7-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="582b7-178">حدد **حفظ** لحفظ عملك.</span><span class="sxs-lookup"><span data-stu-id="582b7-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="582b7-179">لحذف نشاط أو قسم، حدد الزر **حذف** (رمز سلة مهملات) في الركن العلوي الأيسر من النشاط أو القسم.</span><span class="sxs-lookup"><span data-stu-id="582b7-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="582b7-180">لإعادة ترتيب الأنشطة والأقسام، اسحبها إلى موقع جديد.</span><span class="sxs-lookup"><span data-stu-id="582b7-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="582b7-181">إضافة جهات اتصال أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="582b7-181">Add or edit contacts</span></span>

<span data-ttu-id="582b7-182">يمكنك إضافة جهات اتصال يمكنها مساعدة الموظف الجديد على تحقيق بنجاح من اليوم الأول.</span><span class="sxs-lookup"><span data-stu-id="582b7-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="582b7-183">قد تكون جهات الاتصال هذه من مسؤولي التعيين أو من الزملاء في فريق ومن المسؤولين في مجال الإعداد والمشرفين والمسؤولين وموظفي دعم تكنولوجيا المعلومات.</span><span class="sxs-lookup"><span data-stu-id="582b7-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="582b7-184">على علامة التبويب **جهات الاتصال**، حدد **جهة اتصال جديدة**.</span><span class="sxs-lookup"><span data-stu-id="582b7-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="582b7-185">في مربع الحوار **إضافة عضو فريق**، أدخل اسم جهة الاتصال أو عنوان بريدها الإلكتروني، وأدخل وصفًا قصيرًا يشرح الطريقة التي يمكن لجهة الاتصال أن تساعد من خلالها الموظف الجديد، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="582b7-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="582b7-186">إضافة جهات اتصال إلى دليل أو قالب إعداد</span><span class="sxs-lookup"><span data-stu-id="582b7-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="582b7-187">أو يمكنك تحديد جهة اتصال‏‎ أو أكثر ضمن **اقتراحات**.</span><span class="sxs-lookup"><span data-stu-id="582b7-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="582b7-188">حدد **حفظ** لحفظ عملك.</span><span class="sxs-lookup"><span data-stu-id="582b7-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="582b7-189">لحذف جهة اتصال، حدد الزر **حذف** (رمز سلة المهملات) إلى يسار جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="582b7-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="582b7-190">لتحرير جهة اتصال، حدد الزر **تحرير** (رمز القلم) إلى يسار جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="582b7-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="582b7-191">إضافة موارد أو تحريرها</span><span class="sxs-lookup"><span data-stu-id="582b7-191">Add or edit resources</span></span>

<span data-ttu-id="582b7-192">يمكنك إضافة ملفات وخرائط وارتباطات مفيدة إلى قسم **الموارد** في دليل الإعداد.</span><span class="sxs-lookup"><span data-stu-id="582b7-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="582b7-193">على علامة التبويب **الموارد‏‎**، حدد **مورد جديد**.</span><span class="sxs-lookup"><span data-stu-id="582b7-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="582b7-194">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="582b7-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="582b7-195">لإضافة ملف، حدد علامة التبويب‏‎ **ملف**، ثم اسحب الملف إلى المنطقة المعينة.</span><span class="sxs-lookup"><span data-stu-id="582b7-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="582b7-196">(أو انقر في أي مكان في هذه المنطقة للاستعراض بحثًا عن الملف على الكمبيوتر، أو حدد **استعراض OneDrive**.) أدخل اسمًا للملف، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="582b7-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="582b7-197">لإضافة ارتباط، حدد علامة التبويب **ارتباط**، ثم أدخل اسمًا وعنوانًا للارتباط، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="582b7-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="582b7-198">لإضافة خريطة، حدد علامة التبويب **خريطة**، ثم أدخل اسمًا وعنوانًا للخريطة، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="582b7-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="582b7-199">سيتضمن Onboard خريطة للعنوان الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="582b7-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="582b7-200">إضافة مورد إلى دليل أو قالب إعداد</span><span class="sxs-lookup"><span data-stu-id="582b7-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="582b7-201">حدد **حفظ** لحفظ عملك.</span><span class="sxs-lookup"><span data-stu-id="582b7-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="582b7-202">لحذف مورد، حدد الزر **حذف** (رمز سلة المهملات) إلى يسار المورد.</span><span class="sxs-lookup"><span data-stu-id="582b7-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="582b7-203">لتحرير جهة اتصال، حدد الزر **تحرير** (رمز القلم) إلى يسار المورد.</span><span class="sxs-lookup"><span data-stu-id="582b7-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="582b7-204">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="582b7-204">Next steps</span></span>

- [<span data-ttu-id="582b7-205">مشاركة المحتوى مع مساهمين آخرين</span><span class="sxs-lookup"><span data-stu-id="582b7-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="582b7-206">عرض حالة المهام وإعداد الموظفين</span><span class="sxs-lookup"><span data-stu-id="582b7-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="582b7-207">إنشاء فرق توظيف في Onboard‎</span><span class="sxs-lookup"><span data-stu-id="582b7-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="582b7-208">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="582b7-208">See also</span></span>

- [<span data-ttu-id="582b7-209">تجربة تطبيق Onboard أو شراؤه</span><span class="sxs-lookup"><span data-stu-id="582b7-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="582b7-210">الجديد</span><span class="sxs-lookup"><span data-stu-id="582b7-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="582b7-211">ملاحظات الإصدار</span><span class="sxs-lookup"><span data-stu-id="582b7-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="582b7-212">الحصول على الدعم</span><span class="sxs-lookup"><span data-stu-id="582b7-212">Get support</span></span>](./talent-support.md)
