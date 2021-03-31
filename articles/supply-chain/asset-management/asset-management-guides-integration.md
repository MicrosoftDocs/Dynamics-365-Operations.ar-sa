---
title: تكامل Dynamics 365 Supply Chain Management (إدارة الأصول) مع Dynamics 365 Guides
description: يوضح هذا الموضوع كيفية تكامل الوحدة النمطية لإداره الأصول في Microsoft  Dynamics 365 Supply Chain Management مع Dynamics 365 Guides للاستفادة من دلائل الحقيقة المختلطة في مهام سير عمل الخدمات اليومية والصيانة.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: e3e9e74397faec12f6eecff1f562fd9d731ac5e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230142"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="b58db-103">تكامل Dynamics 365 Supply Chain Management (إدارة الأصول) مع Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="b58db-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="b58db-104">يمكنك تكامل الوحدة النمطية **لإداره الأصول** في Microsoft Dynamics 365 Supply Chain Management مع Dynamics 365 Guides للاستفادة من دلائل الحقيقة المختلطة في مهام سير عمل الخدمات اليومية والصيانة.</span><span class="sxs-lookup"><span data-stu-id="b58db-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="b58db-105">إذا كان الدليل مقترنا بأمر عمل إداره الأصول، فان العامل الذي يفتح قائمه فحص الصيانة الخاصة بأمر العمل في Supply Chain Management (Dynamics 365) للأجهزة المحمولة يري هذا الدليل متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="b58db-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="b58db-106">يمكن للعامل بعد ذلك العثور علي الدليل وفتحه في تطبيق Dynamics 365 Guides HoloLens.</span><span class="sxs-lookup"><span data-stu-id="b58db-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b58db-107">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="b58db-107">Prerequisites</span></span>

<span data-ttu-id="b58db-108">قبل إرفاق الأدلة بأوامر عمل إداره الأصول، يجب عليك إكمال هذه المتطلبات الاساسيه:</span><span class="sxs-lookup"><span data-stu-id="b58db-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="b58db-109">[إعداد Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) الإصدار 10.0.9 أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="b58db-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="b58db-110">[قم بتشغيل الكتابة المزدوجة لتطبيقات Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="b58db-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="b58db-111">[قم بتشغيل إصدار التقييم](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) لميزة **MRGuidesFeature** .</span><span class="sxs-lookup"><span data-stu-id="b58db-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="b58db-112">(بالنسبة لبيئات الإنتاج، يجب أولا إرسال بطاقة دعم لكي تتم إضافه المستاجر الخاص بك إلى مجموعة التقييم).</span><span class="sxs-lookup"><span data-stu-id="b58db-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="b58db-113">[قم بتشغيل مفاتيح التكوين التالية](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) في صفحة **تكوين الترخيص**:</span><span class="sxs-lookup"><span data-stu-id="b58db-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="b58db-114">إدارة الاصول \> الحقيقة المختلطة لإدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="b58db-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="b58db-115">الحقيقة المختلطة \> دليل الحقيقة المختلطة</span><span class="sxs-lookup"><span data-stu-id="b58db-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="b58db-116">[إعداد Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) الإصدار 200.0.0.96 أو إصدار لاحق</span><span class="sxs-lookup"><span data-stu-id="b58db-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="b58db-117">استخدام Dynamics 365 Guides مع إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="b58db-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="b58db-118">لإقران دليل، يمكنك استخدام بند قائمه فحص الصيانة في إداره الأصول.</span><span class="sxs-lookup"><span data-stu-id="b58db-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="b58db-119">يمكنك إنشاء الاقتران من خلال قالب قائمة فحص الصيانة أو نوع مهمة صيانة أو أمر عمل، نظرا لان الثلاثة تحتوي علي بنود قائمة فحص الصيانة.</span><span class="sxs-lookup"><span data-stu-id="b58db-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="b58db-120">يمكنك توفير الوقت باستخدام قالب، وذلك لأنه يمكن اقران قالب بكافة أنواع مهام الصيانة التي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="b58db-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="b58db-121">على سبيل المثال، يرتبط الدليل المرتبط بنوع مهمة صيانة تلقائيا بكافة أوامر العمل التي تحدد نوع المهمة هذا.</span><span class="sxs-lookup"><span data-stu-id="b58db-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="b58db-122">ومن ناحية أخرى، يكون الدليل المرتبط مباشره بأمر العمل موجودًا فقط لأمر العمل هذا.</span><span class="sxs-lookup"><span data-stu-id="b58db-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="b58db-123">إقران دليل بقالب قائمه فحص صيانة</span><span class="sxs-lookup"><span data-stu-id="b58db-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="b58db-124">لإقران دليل بقالب قائمه فحص صيانة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b58db-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="b58db-125">قم بإنشاء دليل باستخدام تطبيق Dynamics 365 Guides للكمبيوتر الشخصي وتطبيق HoloLens.</span><span class="sxs-lookup"><span data-stu-id="b58db-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="b58db-126">لمزيد من المعلومات حول كيفية إنشاء دليل، راجع المواضيع التالية:</span><span class="sxs-lookup"><span data-stu-id="b58db-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="b58db-127">استخدام تطبيق الكمبيوتر الشخصي لإنشاء دليل</span><span class="sxs-lookup"><span data-stu-id="b58db-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="b58db-128">استخدام تطبيق HoloLens لوضع الهولوغرام الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="b58db-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="b58db-129">في Supply Chain Management، [قم بإنشاء قالب قائمة فحص صيانة](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="b58db-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="b58db-130">قم باقران الدليل الذي قمت بإنشاءه ببند قائمه فحص الصيانة في قالب قائمه فحص الصيانة الجديدة:</span><span class="sxs-lookup"><span data-stu-id="b58db-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="b58db-131">في علامة التبويب السريعة **بنود قائمة فحص الصيانة** حدد البند الذي تريد إقران الدليل به.</span><span class="sxs-lookup"><span data-stu-id="b58db-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="b58db-132">في علامة التبويب السريعة **الأدلة المرتبطة** ، حدد **إضافة دليل**.</span><span class="sxs-lookup"><span data-stu-id="b58db-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="b58db-133">![إقران دليل ببند قائمة فحص صيانة](media/am-guides-integration-add-guide.png "إقران دليل ببند قائمة فحص صيانة")</span><span class="sxs-lookup"><span data-stu-id="b58db-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="b58db-134">في حقل **الاسم** حدد دليلا، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b58db-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="b58db-135">![تحديد دليل في حقل الاسم](media/am-guides-integration-select-guide.png "تحديد دليل في حقل الاسم")</span><span class="sxs-lookup"><span data-stu-id="b58db-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="b58db-136">قم بإقران قالب قائمه فحص الصيانةبنوع مهمة:</span><span class="sxs-lookup"><span data-stu-id="b58db-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="b58db-137">[قم بإنشاء نوع مهمة صيانة](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) ، أو حدد نوع مهمة صيانة موجود.</span><span class="sxs-lookup"><span data-stu-id="b58db-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="b58db-138">في جزء الاجراءات، حدد **الإعدادات الافتراضية لنوع مهمة الصيانة‬**.</span><span class="sxs-lookup"><span data-stu-id="b58db-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="b58db-139">![زر الإعدادات الافتراضية لنوع مهمة الصيانة](media/am-guides-integration-job-defaults.png "زر الإعدادات الافتراضية لنوع مهمة الصيانة")</span><span class="sxs-lookup"><span data-stu-id="b58db-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="b58db-140">قم بإنشاء بند، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b58db-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="b58db-141">![إنشاء بند](media/am-guides-integration-add-line.png "إنشاء بند")</span><span class="sxs-lookup"><span data-stu-id="b58db-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="b58db-142">في جزء الإجراءات‬، حدد **قائمة فحص الصيانة**.</span><span class="sxs-lookup"><span data-stu-id="b58db-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="b58db-143">![زر قائمة فحص الصيانة](media/am-guides-integration-maintenance-checklist.png "زر قائمة فحص الصيانة")</span><span class="sxs-lookup"><span data-stu-id="b58db-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="b58db-144">في علامة التبويب السريعة **بنود قائمة فحص الصيانة** قم بإضافه بند، ثم قم بتغيير قيمة حقل **النوع** إلى **قالب**.</span><span class="sxs-lookup"><span data-stu-id="b58db-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="b58db-145">![تغيير قيمة النوع](media/am-guides-integration-checklist-lines.png "تغيير قيمة النوع")</span><span class="sxs-lookup"><span data-stu-id="b58db-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="b58db-146">في علامة التبويب السريعة **تفاصيل البند** ، في حقل **القالب** حدد القالب الذي قمت باقران الدليل به، ثم حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b58db-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="b58db-147">![تحديد قالب](media/am-guides-integration-checklist-line-details.png "تحديد قالب")</span><span class="sxs-lookup"><span data-stu-id="b58db-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="b58db-148">[قم بإنشاء أمر عمل](work-orders/manually-created-workorders.md#create-work-order) ، ثم حدد نوع مهمة الصيانة التي تستخدم قالب قائمه فحص الصيانة الذي قمت بربطه بالدليل.</span><span class="sxs-lookup"><span data-stu-id="b58db-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="b58db-149">يقترن الدليل تلقائيا بأمر العمل.</span><span class="sxs-lookup"><span data-stu-id="b58db-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="b58db-150">![تحديد نوع مهمة الصيانة](media/am-guides-integration-create-work-order.png "تحديد نوع مهمة الصيانة")</span><span class="sxs-lookup"><span data-stu-id="b58db-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="b58db-151">عرض الدليل المرتبط بامر العمل والعاملين:</span><span class="sxs-lookup"><span data-stu-id="b58db-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="b58db-152">افتح [‏‫مساحة العمل المحمولة للأصل‬](asset-management-mobile-workspace.md) للوصول إلى أمر العمل.</span><span class="sxs-lookup"><span data-stu-id="b58db-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="b58db-153">[افتح قائمة فحص الصيانة](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) الخاصة بامر العمل.</span><span class="sxs-lookup"><span data-stu-id="b58db-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="b58db-154">حدد بند قائمة فحص لعرض الدليل المقترن.</span><span class="sxs-lookup"><span data-stu-id="b58db-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="b58db-155">![الدليل المقترن ببند قائمة الفحص](media/am-guides-integration-show-guide.png "الدليل المقترن ببند قائمة الفحص")</span><span class="sxs-lookup"><span data-stu-id="b58db-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="b58db-156">افتح الدليل على HoloLens.</span><span class="sxs-lookup"><span data-stu-id="b58db-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="b58db-157">![فتح الدليل على HoloLens](media/am-guides-integration-hololens-select.png "فتح الدليل على HoloLens").</span><span class="sxs-lookup"><span data-stu-id="b58db-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="b58db-158">يمكنك أيضا إقران دليل مباشره في قائمه فحص الصيانة لأمر عمل أو نوع مهمة.</span><span class="sxs-lookup"><span data-stu-id="b58db-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b58db-159">هناك مشكله معروفه عندما تقوم بإقران قالب قائمه فحص صيانة بنوع مهمة صيانة افتراضيه، لا يظهر الدليل المرتبط بالقالب على علامة التبويب السريعة **الدلائل المقترنة** بصفحة **الإعدادات الافتراضية لنوع مهمة الصيانة‬**.</span><span class="sxs-lookup"><span data-stu-id="b58db-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="b58db-160">ومع ذلك، سيظهر الدليل بعد تطبيق نوع المهمة علي أمر العمل على علامة التبويب السريعة **الدلائل المقترنة**.</span><span class="sxs-lookup"><span data-stu-id="b58db-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="b58db-161">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b58db-161">See also</span></span>

- [<span data-ttu-id="b58db-162">نظرة عامة على الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="b58db-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="b58db-163">نظرة عامة على إدارة الأصول</span><span class="sxs-lookup"><span data-stu-id="b58db-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]