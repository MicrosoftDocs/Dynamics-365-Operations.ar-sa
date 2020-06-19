---
title: Regulatory Configuration Services (RCS) - ميزات العولمة
description: يشرح هذه الموضوع كيفية استخدام Microsoft Regulatory Configuration Services (RCS) والمستودع العمومي لإنشاء ميزات العولمة واستخدامها.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 97206552616b248f88e516fea08b3f059257e8d1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3432037"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="c38bb-103">Regulatory Configuration Services (RCS) - ميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="c38bb-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c38bb-104">يمكنك استخدام Microsoft Regulatory Configuration Services (RCS) لإنشاء ميزة عولمة يمكن استخدامها في خدمات العمولمة، مثل خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="c38bb-105">تسمح لك خدمات RCS بتنفيذ هذه المهام:</span><span class="sxs-lookup"><span data-stu-id="c38bb-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="c38bb-106">تعريف مكونات ذات صلة لميزة ما.</span><span class="sxs-lookup"><span data-stu-id="c38bb-106">Define related components of a feature.</span></span>
- <span data-ttu-id="c38bb-107">إدارة دورة حياة الميزة من خلال حالة الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="c38bb-108">جعل ميزة متاحة لبيئات محددة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="c38bb-109">مشاركة ميزة مع المؤسسات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="c38bb-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="c38bb-110">تشرح الإجراءات التالية كيف يمكن للمستخدم في RCS إضافة ميزة عولمة ومكونات ذات صلة وتحديث حالة الميزة وجعل الميزة متوفرة بحيث يمكن استخدامها في خدمات العولمة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="c38bb-111">قبل إكمال الإجراءات، يجب عليك إكمال الخطوات المرتبطة بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="c38bb-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="c38bb-112">تعيين مثيل RCS.</span><span class="sxs-lookup"><span data-stu-id="c38bb-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="c38bb-113">إنشاء موفر تكوين وتنشيطه.</span><span class="sxs-lookup"><span data-stu-id="c38bb-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="c38bb-114">لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c38bb-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="c38bb-115">في مثيل تطبيقات Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="c38bb-116">انتقل إلى **إدارة المؤسسة** \> **مساحات العمل** \> **التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="c38bb-117">في حالة عدم تزويد بيئة RCS لشركتك، حدد **Regulatory services - التكوين**، واتبع الإرشادات لتزويد بيئة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="c38bb-118">إذا تم تزويد بيئة RCS لشركتك، فاستخدم عنوان URL للصفحة للوصول إلى البيئة عن طريق تحديد خيار تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="c38bb-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="c38bb-119">تشغيل ميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="c38bb-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="c38bb-120">في مثيل RCS، حدد الإطار المتجانب **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="c38bb-121">في مساحة عمل **إدارة الميزات**، حدد **ميزات العولمة** في القائمة، ثم حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![ميزات العولمة في إدارة الميزات](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="c38bb-123">ميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="c38bb-123">Globalization features</span></span>

<span data-ttu-id="c38bb-124">لاستخدام ميزة عولمة، يجب أولاً استيرادها من المستودع العمومي وإنشاء نسختك الخاصة منها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="c38bb-125">هناك طريقتان لإضافة ميزات العولمة:</span><span class="sxs-lookup"><span data-stu-id="c38bb-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="c38bb-126">إضافة ميزة مشتقة تستند إلى ميزة موجودة تم نشرها أو مشاركتها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="c38bb-127">إضافة ميزة جديدة أنشأتها من البداية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="c38bb-128">الوصول إلى ميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="c38bb-128">Access Globalization features</span></span>

1. <span data-ttu-id="c38bb-129">تأكد من أن ميزة **ميزات العولمة** قيد التشغيل في إدارة الميزات، كما ورد وصفه في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="c38bb-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="c38bb-130">افتح مساحة العمل الجديدة **ميزات العولمة**، ثم ضمن **الميزة**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![مساحة عمل الميزات العمومية](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="c38bb-132">تفتح صفح **ميزات الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-132">The **e-Invoicing Features** page is opened.</span></span>

    ![صفحة ميزات الفوترة الإلكترونية](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="c38bb-134">إضافة ميزة عولمة مشتقة</span><span class="sxs-lookup"><span data-stu-id="c38bb-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="c38bb-135">يمكنك إضافة ميزة عولمة جديدة من خلال اشتقاقها من ميزة موجودة تم نشرها أو مشاركتها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="c38bb-136">حدد **استيراد** لفتح صفحة **استيراد ميزة من المستودع العمومي**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![صفحة استيراد ميزة من المستودع العمومي](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="c38bb-138">حدد **مزامنة** للحصول على أحدث الميزات.</span><span class="sxs-lookup"><span data-stu-id="c38bb-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="c38bb-139">تتضمن القائمة المتزامنة الميزات المتوفرة لك إما سبب نشرها بواسطة Microsoft أو بسبب مشاركتها معك بواسطة موفر تكوين آخر.</span><span class="sxs-lookup"><span data-stu-id="c38bb-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![القائمة المتزامنة للميزات](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="c38bb-141">في القائمة، حدد الميزات المراد استيرادها، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="c38bb-142">ستتلقى رسالة عند استيراد الميزات المحددة بنجاح.</span><span class="sxs-lookup"><span data-stu-id="c38bb-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![رسالة تفيد بنجاح الاستيراد](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="c38bb-144">حدد **إضافة**، ثم في مربع حوار القائمة المنسدلة، حدد الخيار **استنادًا إلى الإصدار الموجود**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="c38bb-145">أدخل اسمًا ووصفًا للميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="c38bb-146">في قائمة الميزات المتوفرة، حدد الإصدار الأساسي للميزة، ثم حدد **إنشاء ميزة**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![إضافة ميزة مشتقة](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="c38bb-148">يتم إنشاء الميزة التي أضفتها وحالتها **مسودة**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![الميزة المشتقة التي لها الحالة "مسودة"](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="c38bb-150">راجع مكونات الميزة لتحديد ما إذا كانت التحديثات ضرورية:</span><span class="sxs-lookup"><span data-stu-id="c38bb-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="c38bb-151">راجع التكوينات، في حال كنت بحاجة إلى تخصيص تنسيقات التقارير الإلكترونية ورابطها مع تعيينات التنسيق لإصدار الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="c38bb-152">راجع الإعداد، في حال كنت بحاجة إلى تخصيص علامة التبويب **الإجراءات** أو علامة التبويب **قواعد إمكانية التطبيق**  أو علامة التبويب **المتغيرات** لإصدار الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="c38bb-153">على علامة التبويب **الإصدارات**، حدد التاريخ **ساري من**، وأدخل وصفًا إذا كان حقل **الوصف** فارغًا.</span><span class="sxs-lookup"><span data-stu-id="c38bb-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="c38bb-154">حدد **تغيير الحالة** لإكمال الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="c38bb-155">يمكن جعل الميزات المكتملة متوفرة لبيئة معينة بحيث يمكن استخدامها في خدمات العولمة، أو يمكن نشرها في المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c38bb-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="c38bb-156">يمكن مشاركة الميزات التي لديها **حالة إصدار الميزة** بقيمة **منشورة** مع مؤسسات خارجية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="c38bb-157">إضافة ميزة عولمة</span><span class="sxs-lookup"><span data-stu-id="c38bb-157">Add a new Globalization feature</span></span>

<span data-ttu-id="c38bb-158">يمكنك إضافة ميزة عولمة جديدة عن طريق إنشائها من البداية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="c38bb-159">في الصفحة **استيراد ميزة من المستودع العمومي**، حدد **إضافة**، ثم حدد الخيار **ميزة جديدة** في مربع القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="c38bb-160">أدخل اسمًا ووصفًا للميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="c38bb-161">حدد **إنشاء ميزة**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-161">Select **Create feature**.</span></span>

    ![إضافة ميزة جديدة](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="c38bb-163">على علامة التبويب **الإصدارات**، حدد التاريخ **ساري من**، ثم حدد **تغيير الحالة** لإكمال الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="c38bb-164">يمكن جعل الميزات المكتملة متوفرة لبيئة معينة بحيث يمكن استخدامها في خدمات العولمة، أو يمكن نشرها في المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c38bb-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="c38bb-165">يمكن مشاركة الميزات التي لديها **حالة إصدار الميزة** بقيمة **منشورة** مع مؤسسات خارجية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="c38bb-166">نظرة على مكونات الميزات</span><span class="sxs-lookup"><span data-stu-id="c38bb-166">Feature component overview</span></span>

<span data-ttu-id="c38bb-167">تتضمن ميزات العولمة عدة مكونات:</span><span class="sxs-lookup"><span data-stu-id="c38bb-167">Globalization features have several components:</span></span>

- <span data-ttu-id="c38bb-168">**الإصدار** – يدعم هذا المكون إدارة دورة حياة الميزات ويتيح للمستخدمين إدارة حالة إصدارات مختلفة للميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="c38bb-169">**التكوينات** – يتيح هذا المكون للمستخدمين إدارة تنسيقات التقارير الإلكترونية وتعيينات التنسيق وعرضها وتحريرها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="c38bb-170">**عمليات الإعداد** – يتيح هذا المكون لمستخدمي خدمات العولمة، مثل خدمة الفوترة الإلكترونية، إدارة عملية إعداد إصدار الميزة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="c38bb-171">وهو بالتالي يدعم البناء المرن لقواعد الاتصالات والاستجابات.</span><span class="sxs-lookup"><span data-stu-id="c38bb-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="c38bb-172">**البيئة** – يتيح هذا المكون لمستخدمي خدمات العولمة، مثل خدمة الفوترة الإلكترونية، إدارة البيئة حيث تم استخدام إعداد إصدار الميزة ومنح التخويل إلى المستخدمين الذين سيتمكنون من الوصول اليه.</span><span class="sxs-lookup"><span data-stu-id="c38bb-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="c38bb-173">**المؤسسات** – يسمح هذا المكون للمستخدمين بمشاركة الميزات مع المؤسسات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="c38bb-174">تكوين مكونات الميزات</span><span class="sxs-lookup"><span data-stu-id="c38bb-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="c38bb-175">الإصدار والحالة</span><span class="sxs-lookup"><span data-stu-id="c38bb-175">Version and status</span></span>

<span data-ttu-id="c38bb-176">يتم استخدام الإصدار لإدارة دورة حياة ميزات العولمة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="c38bb-177">يمكن تغيير الحالة في حقل **الحالة** على علامة تبويب **الإصدار**. تتوفر الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="c38bb-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="c38bb-178">**مسودة** – يمكن تحرير الميزة فقط عندما تكون في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="c38bb-179">**مكتملة** – تم إنجاز الميزة وكافة المكونات ذات الصلة (مكتملة) ولا يمكن تحريرها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="c38bb-180">**منشورة** – تم نشر الميزة وكافة المكونات ذات الصلة إلى المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c38bb-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="c38bb-181">**مشتركة** – تمت مشاركه الميزة وكافة المكونات ذات الصلة مع المؤسسات الخارجية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="c38bb-182">**ممكّنة** – تم تمكين ميزه وكافة المكونات ذات الصلة لاستخدامها في خدمة عولمة، مثل خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="c38bb-183">يجب نقل الميزات بطريقة تسلسلية عبر بعض هذه الحالات.</span><span class="sxs-lookup"><span data-stu-id="c38bb-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="c38bb-184">وبالتالي، قد لا تكون كل حالة متوفرة في كل مرحلة من مراحل دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="c38bb-185">تكوينات</span><span class="sxs-lookup"><span data-stu-id="c38bb-185">Configurations</span></span>

<span data-ttu-id="c38bb-186">تتوفر الإجراءات التالية لعمليات التكوين:</span><span class="sxs-lookup"><span data-stu-id="c38bb-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="c38bb-187">**عرض** – عرض تكوينات الميزات الأساسية التي لا تتطلب أي تحديث.</span><span class="sxs-lookup"><span data-stu-id="c38bb-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="c38bb-188">**تحرير** – إنشاء إصدار مسودة لتكوين محدد بحيث يمكنك تحرير التنسيق أو تعيين التنسيق في مصمم التنسيق.</span><span class="sxs-lookup"><span data-stu-id="c38bb-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="c38bb-189">**حذف** – حذف تكوين محدد من الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="c38bb-190">**إعادة تعريف** – إعادة تعريف الميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="c38bb-191">لمزيد من المعلومات، راجع القسم [إعادة تعريف ميزات العولمة المشتقة](#rebase) في قسم لاحق في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="c38bb-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="c38bb-192">عمليات الإعداد</span><span class="sxs-lookup"><span data-stu-id="c38bb-192">Setups</span></span>

<span data-ttu-id="c38bb-193">تتوفر الإجراءات التالية لعمليات إعداد الميزات:</span><span class="sxs-lookup"><span data-stu-id="c38bb-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="c38bb-194">**إضافة** – إنشاء عملية إعداد ميزة جديدة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="c38bb-195">يمكن اشتقاق إعداد الميزة هذا من إعداد ميزة موجودة أو تم إنشاؤها من البداية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="c38bb-196">**حذف** – حذف إعداد ميزة محددة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="c38bb-197">**عرض** – عرض إعداد ميزة أساسية لا تتطبق أي تغييرات.</span><span class="sxs-lookup"><span data-stu-id="c38bb-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="c38bb-198">**تحرير** – إنشاء سمات المكونات الرئيسية الثلاثة لإعداد الميزة أو حذفها أو تعديلها:</span><span class="sxs-lookup"><span data-stu-id="c38bb-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="c38bb-199">الإجراءات ومعلماتها</span><span class="sxs-lookup"><span data-stu-id="c38bb-199">Actions and their parameters</span></span>
    - <span data-ttu-id="c38bb-200">قواعد قابلية التطبيق</span><span class="sxs-lookup"><span data-stu-id="c38bb-200">Applicability rules</span></span>
    - <span data-ttu-id="c38bb-201">المتغيرات</span><span class="sxs-lookup"><span data-stu-id="c38bb-201">Variables</span></span>

![صفحة إعداد إصدار الميزة](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="c38bb-203">البيئات</span><span class="sxs-lookup"><span data-stu-id="c38bb-203">Environments</span></span>

<span data-ttu-id="c38bb-204">تتوفر الإجراءات التالية للبيئات:</span><span class="sxs-lookup"><span data-stu-id="c38bb-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="c38bb-205">**تمكين** – لإصدار ميزة محددة، حدد بيئة منشورة، وحدد تاريخ **ساري من** عندما يجب أن يكون متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="c38bb-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="c38bb-206">لمزيد من المعلومات، راجع القسم [تكوين البيئات لتمكينها](#configureenvironment) في قسم لاحق في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="c38bb-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="c38bb-207">**إلغاء** – إزالة بيئة لإعداد ميزة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="c38bb-208">المؤسسات</span><span class="sxs-lookup"><span data-stu-id="c38bb-208">Organizations</span></span>

<span data-ttu-id="c38bb-209">اتبع الخطوات التالية لمشاركة ميزة عولمة مع مؤسسة خارجية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="c38bb-210">في صفحة **ميزات الفوترة الإلكترونية**، حدد الميزة وإصدار الميزة المراد مشاركته.</span><span class="sxs-lookup"><span data-stu-id="c38bb-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="c38bb-211">في علامة التبويب **المؤسسات**، حدد **مشاركة مع**، ثم أدخل اسم مجال المؤسسة في مربع القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="c38bb-212">حدد **مشاركة**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-212">Select **Share**.</span></span>

    ![مشاركة ميزة مع مؤسسة](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="c38bb-214">تتم مشاركة الميزة مع المؤسسة المحددة وتكون متوفرة لهذه المؤسسة في المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c38bb-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="c38bb-215">من هناك، يمكن استيراد الميزة إلى مثيل المؤسسة لخدمات RCS أو Dynamics 365 Finance بحيث يمكن استخدامها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="c38bb-216">إعادة تعريف ميزات العولمة المشتقة‬‏‫</span><span class="sxs-lookup"><span data-stu-id="c38bb-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="c38bb-217">يمكنك إعادة تعريف ميزة عولمة مشتقة‬‏‫ إلى إصدار الميزة الجديد أو الإصدار الأساسي المحدّث.</span><span class="sxs-lookup"><span data-stu-id="c38bb-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="c38bb-218">وبهذه الطريقة، يمكن تحديث التغييرات التي حدثت في الإصدار الأساسي بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="c38bb-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="c38bb-219">يتم إنشاء إصدار الميزة الأساسي المحدّث بواسطة موفر التكوين الأصلي، وبعد ذلك يتم نشره أو مشاركته.</span><span class="sxs-lookup"><span data-stu-id="c38bb-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![إصدار الميزة الأساسي المحدّث](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="c38bb-221">على سبيل المثال، إذا أردت إعادة تعريف الإصدار المشتق من ميزة أنشأتها، ستحصل أولاً على إصدار الميزة الأخير عن طريق استيراده من المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="c38bb-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="c38bb-222">في صفحة **ميزات الفوترة الإلكترونية**، حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="c38bb-223">حدد **مزامنة** للحصول على أحدث الميزات.</span><span class="sxs-lookup"><span data-stu-id="c38bb-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="c38bb-224">في قائمة الميزات، حدد الميزات المراد استيرادها، ثم حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![استيراد الإصدار الأخير لميزة](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="c38bb-226">في قائمة الميزات، حدد الميزة المراد إعادة تعريفها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="c38bb-227">في علامة التبويب **الإصدار**، حدد **جديد** لإنشاء إصدار مسودة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![إنشاء إصدار مسودة جديد](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="c38bb-229">حدد **إعادة تعريف**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="c38bb-230">في مربع الحوار **إعادة تعريف**، حدد أحدث إصدار للميزة لإعادة التعريف إليه.</span><span class="sxs-lookup"><span data-stu-id="c38bb-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![مربع الحوار "إعادة تعريف"](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="c38bb-232">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-232">Select **OK**.</span></span>
9. <span data-ttu-id="c38bb-233">راجع مكونات الميزة، وقم بإجراء أي تغييرات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="c38bb-234">حدد **تغيير الحالة** لإكمال الميزة المعاد تعريفها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="c38bb-235">عند اكتمال إعادة التعريف، يمكنك تنفيذ إجراءات إضافية.</span><span class="sxs-lookup"><span data-stu-id="c38bb-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="c38bb-236">على سبيل المثال، يمكنك نشر الميزة وجعلها متوفرة للاستخدام في خدمات العولمة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![تحديث حالة الميزة إلى مكتملة](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="c38bb-238">تكوين بيئات لميزات العولمة</span><span class="sxs-lookup"><span data-stu-id="c38bb-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="c38bb-239">بإمكان مستخدمي خدمات العولمة إدارة البيئة لإعداد ميزة عولمة ومنح التخويل لمستخدمين آخرين الذين سيتمكنون من الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="c38bb-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="c38bb-240">في مساحة العمل **ميزات العولمة**، ضمن **البيئات**، حدد الإطار المتجانب **الفوترة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c38bb-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![مساحة عمل ميزات العولمة](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="c38bb-242">حدد **معلمات المخزن الرئيسي**، ثم حدد **جديد** لإنشاء سر Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="c38bb-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="c38bb-243">ادخل اسمًا ووصفًا للمخزن الرئيسي، ثم في **Key Vault URI**، أدخل عنوان URL الذي يعرف مورد المخزن الرئيسي في Azure.</span><span class="sxs-lookup"><span data-stu-id="c38bb-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="c38bb-244">على علامة التبويب السريعة **الشهادات**، حدد **إضافة** لإضافة‏‎ الشهادة، وأدخل اسمًا ووصفًا لكل شهادة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![تمت إضافة شهادة](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="c38bb-246">حدد **جديد** لإنشاء بيئة جديدة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="c38bb-247">أدخل اسمًا ووصفًا والرمز المميز لتوقيع الوصول المشترك المطلوب لمساحة التخزين.</span><span class="sxs-lookup"><span data-stu-id="c38bb-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="c38bb-248">على علامة التبويب السريعة **المستخدمون**، حدد **جديد** لإضافة مستخدم لديه إذن الوصول إلى هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="c38bb-249">أدخل معرف المستخدم وعنوان البريد الإلكتروني للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="c38bb-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="c38bb-250">كرر الخطوتين 7 و8 لإضافة المزيد من المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="c38bb-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="c38bb-251">حدد **نشر** لنشر البيئة.</span><span class="sxs-lookup"><span data-stu-id="c38bb-251">Select **Publish** to publish the environment.</span></span>

    ![بيئة منشورة](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
