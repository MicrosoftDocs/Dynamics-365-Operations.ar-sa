---
title: معاينة ميزة إدارة التغييرات الهندسية
description: يقدم هذا الموضوع معاينة شاملة للنهاية توضح كيفية العمل مع إدارة التغييرات الهندسية.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b6270bbb6780786ed4535ca2987ed44448bd81ad
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2020
ms.locfileid: "4421828"
---
# <a name="engineering-change-management-feature-walkthrough"></a><span data-ttu-id="8431d-103">معاينة ميزة إدارة التغييرات الهندسية</span><span class="sxs-lookup"><span data-stu-id="8431d-103">Engineering change management feature walkthrough</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8431d-104">يقدم هذا الموضوع معاينة شاملة للنهاية توضح كيفية العمل مع إدارة التغييرات الهندسية.</span><span class="sxs-lookup"><span data-stu-id="8431d-104">This topic provides an end-to-end walkthrough that shows how to work with engineering change management.</span></span> <span data-ttu-id="8431d-105">ويمر خلال كل من السيناريوهات الأكثر أهميه:</span><span class="sxs-lookup"><span data-stu-id="8431d-105">It goes through each of the most important scenarios:</span></span>

- <span data-ttu-id="8431d-106">تكوين الميزة الاساسيه</span><span class="sxs-lookup"><span data-stu-id="8431d-106">Basic feature configuration</span></span>
- <span data-ttu-id="8431d-107">كيف تقوم شركه هندسية بإنشاء منتج هندسي جديد</span><span class="sxs-lookup"><span data-stu-id="8431d-107">How an engineering company creates a new engineering product</span></span>
- <span data-ttu-id="8431d-108">كيف تصدر شركه هندسية منتج هندسي إلى شركه محليه</span><span class="sxs-lookup"><span data-stu-id="8431d-108">How an engineering company releases an engineering product to a local company</span></span>
- <span data-ttu-id="8431d-109">كيف يمكن للشركة المحلية مراجعه منتج تم إصداره من قبل أحدي الشركات الهندسية وقبوله</span><span class="sxs-lookup"><span data-stu-id="8431d-109">How a local company can review and accept a product that has been released to it by an engineering company</span></span>
- <span data-ttu-id="8431d-110">كيف يمكن للشركة المحلية استخدام منتج هندسي في الحركات القياسية</span><span class="sxs-lookup"><span data-stu-id="8431d-110">How a local company can use an engineering product in standard transactions</span></span>
- <span data-ttu-id="8431d-111">كيفيه أضافه منتج هندسي لأمر التوريد</span><span class="sxs-lookup"><span data-stu-id="8431d-111">How to add an engineering product to a sales order</span></span>
- <span data-ttu-id="8431d-112">كيفيه طلب اجراء تغييرات علي منتج هندسي من خلال إنشاء طلب تغيير هندسي</span><span class="sxs-lookup"><span data-stu-id="8431d-112">How to request changes to an engineering product by creating an engineering change request</span></span>
- <span data-ttu-id="8431d-113">كيفيه جدوله التغييرات المطلوبة وتنفيذها عن طريق إنشاء ترتيب تغيير هندسي</span><span class="sxs-lookup"><span data-stu-id="8431d-113">How to schedule and implement requested changes by creating an engineering change order</span></span>
- <span data-ttu-id="8431d-114">كيفيه إصدار منتج تم تغييره</span><span class="sxs-lookup"><span data-stu-id="8431d-114">How to release a product that has been changed</span></span>

<span data-ttu-id="8431d-115">تستخدم كافة التمرينات الواردة في هذا الموضوع بيانات العينة القياسية التي يتم توفيرها لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8431d-115">All the exercises in this topic use the standard sample data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8431d-116">بالاضافه إلى ذلك، يبني كل تمرين على التمرين السابق.</span><span class="sxs-lookup"><span data-stu-id="8431d-116">Additionally, each exercise builds on the previous exercise.</span></span> <span data-ttu-id="8431d-117">التالي، نوصي بالعمل من خلال التدريبات بالترتيب، من البداية إلى النهاية، خاصه إذا لم تكن قد استخدمت ميزه أداره التغيير الهندسية قبل ذلك.</span><span class="sxs-lookup"><span data-stu-id="8431d-117">Therefore, we recommend that you work through the exercises in order, from beginning to end, especially if you've never used the engineering change management feature before.</span></span> <span data-ttu-id="8431d-118">وبهذه الطريقة، ستحصل علي فهم كامل لهذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="8431d-118">In this way, you will gain a complete understanding of the feature.</span></span>

## <a name="set-up-for-the-sample-scenario"></a><span data-ttu-id="8431d-119">إعداد للسيناريو النموذجي</span><span class="sxs-lookup"><span data-stu-id="8431d-119">Set up for the sample scenario</span></span>

<span data-ttu-id="8431d-120">لاتباع السيناريو النموذجي الذي تم توفيره في هذا الموضوع، يجب أولا اعداد الميزة وذلك بجعل بيانات العرض التوضيحي متوفرة وأضافه بعض السجلات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="8431d-120">To follow the sample scenario that is provided in this topic, you must first prepare the feature by making demo data available and adding a few custom records.</span></span>

<span data-ttu-id="8431d-121">قبل ان تحاول القيام بأي من التمرينات الموجودة في بقية هذا الموضوع، اتبع الإرشادات الموجودة في كافة الأقسام الفرعية التالية.</span><span class="sxs-lookup"><span data-stu-id="8431d-121">Before you try to do any of the exercises in the rest of this topic, follow the instructions in all the following subsections.</span></span> <span data-ttu-id="8431d-122">تقوم هذه الأقسام الفرعية أيضا بتقديم العديد من صفحات الإعدادات الهامه التي ستستخدمها عند اعداد أداره التغييرات الهندسية للمؤسسة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8431d-122">These subsections also introduce several important settings pages that you will use when you set up engineering change management for your own organization.</span></span>

### <a name="make-standard-demo-data-available"></a><span data-ttu-id="8431d-123">جعل بيانات العرض التوضيحي القياسي متاحة</span><span class="sxs-lookup"><span data-stu-id="8431d-123">Make standard demo data available</span></span>

<span data-ttu-id="8431d-124">العمل علي نظام يتم فيه [تثبيت بيانات العرض التوضيحي القياسية](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8431d-124">Work on a system where the [standard demo data is installed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span></span> <span data-ttu-id="8431d-125">وتضيف بيانات العرض التوضيحي القياسية بيانات للعديد من الكيانات القانونية لعرض توضيحي (الشركات والمؤسسات).</span><span class="sxs-lookup"><span data-stu-id="8431d-125">The standard demo data adds data for several demo legal entities (companies and organizations).</span></span> <span data-ttu-id="8431d-126">واثناء العمل خلال التمرينات، ستستخدم منتقي الشركة علي الجانب الأيسر من شريط التنقل للتبديل بين شركه واحده ( *DEMF*) يتم اعدادها *كمؤسسه هندسية* وشركه أخرى (*USMF*) التي يتم اعدادها *كمؤسسه تشغيليه*.</span><span class="sxs-lookup"><span data-stu-id="8431d-126">As you work through the exercises, you will use the company picker on the right side of the navigation bar to switch between one company (*DEMF*) that is set up as an *engineering organization* and another company (*USMF*) that is set up as an *operational organization*.</span></span>

### <a name="set-up-an-engineering-organization"></a><span data-ttu-id="8431d-127">إعداد مؤسسة هندسية</span><span class="sxs-lookup"><span data-stu-id="8431d-127">Set up an engineering organization</span></span>

<span data-ttu-id="8431d-128">تمتلك مؤسسه الهندسة بيانات الهندسة، وتكون مسؤوله عن التغييرات في تصميم المنتج والمنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-128">An engineering organization owns the engineering data, and is responsible for product design and product changes.</span></span> <span data-ttu-id="8431d-129">لإعداد المؤسسات الهندسية الخاصة بك‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="8431d-129">To set up your engineering organizations, follow these steps.</span></span>

1. <span data-ttu-id="8431d-130">انتقل إلى **إدارة التغييرات الهندسية &gt; الإعداد &gt; مؤسسات هندسية**.</span><span class="sxs-lookup"><span data-stu-id="8431d-130">Go to **Engineering change management &gt; Setup &gt; Engineering organizations**.</span></span>
1. <span data-ttu-id="8431d-131">حدد **جديد** لإضافة صف إلى الشبكة، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="8431d-131">Select **New** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-132">**المؤسسة الهندسية:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="8431d-132">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="8431d-133">**اسم المؤسسة:** *Contoso Entertainment System Germany*</span><span class="sxs-lookup"><span data-stu-id="8431d-133">**Organization name:** *Contoso Entertainment System Germany*</span></span>

    <span data-ttu-id="8431d-134">![إضافة مؤسسة هندسية](media/engineering-org.png "إضافة مؤسسة هندسية")</span><span class="sxs-lookup"><span data-stu-id="8431d-134">![Adding an engineering organization](media/engineering-org.png "Adding an engineering organization")</span></span>

### <a name="set-up-the-version-product-dimension-group"></a><span data-ttu-id="8431d-135">اعداد مجموعه ابعاد منتج الإصدار</span><span class="sxs-lookup"><span data-stu-id="8431d-135">Set up the version product dimension group</span></span>

1. <span data-ttu-id="8431d-136">الانتقال إلى **إداره معلومات المنتج&gt; إعداد &gt; مجموعات الأبعاد والمتغيرات &gt; مجموعات أبعاد المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8431d-136">Go to **Product information management &gt; Setup &gt; Dimensions and variant groups &gt; Product dimension groups**.</span></span>
1. <span data-ttu-id="8431d-137">حدد **جديد** لإنشاء مجموعة أبعاد المنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-137">Select **New** to create a product dimension group.</span></span>
1. <span data-ttu-id="8431d-138">قم بتعيين حقل **الاسم** إلى *الإصدار*.</span><span class="sxs-lookup"><span data-stu-id="8431d-138">Set the **Name** field to *Version*.</span></span>
1. <span data-ttu-id="8431d-139">حدد **حفظ** لحفظ البعد الجديد وتحميل القيم علي علامة التبويب السريعة **ابعاد المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8431d-139">Select **Save** to save the new dimension and load values onto the **Product dimensions** FastTab.</span></span>
1. <span data-ttu-id="8431d-140">في علامة التبويب السريعة **ابعاد المنتج**، قم بتعيين **الإصدار** كبعد منتج نشط.</span><span class="sxs-lookup"><span data-stu-id="8431d-140">On the **Product dimensions** FastTab, set **Version** as an active product dimension.</span></span>

    <span data-ttu-id="8431d-141">![إضافة مجموعة أبعاد منتج](media/product-dimension-groups.png "إضافة مجموعة أبعاد منتج")</span><span class="sxs-lookup"><span data-stu-id="8431d-141">![Adding a product dimension group](media/product-dimension-groups.png "Adding a product dimension group")</span></span>

### <a name="set-up-product-lifecycle-states"></a><span data-ttu-id="8431d-142">إعداد حالات دورة حياة المنتج</span><span class="sxs-lookup"><span data-stu-id="8431d-142">Set up product lifecycle states</span></span>

<span data-ttu-id="8431d-143">خلال دورة حياة المنتج الهندسي، من المهم التحكم في الحركات المسموح بها لكل حالة من حالات دورة الحياة.</span><span class="sxs-lookup"><span data-stu-id="8431d-143">As an engineering product goes through its lifecycle, it's important that you be able to control which transactions are allowed for each lifecycle state.</span></span> <span data-ttu-id="8431d-144">لإعداد حالات دورة حياة المنتج، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="8431d-144">To set up the product lifecycle states, follow these steps.</span></span>

1. <span data-ttu-id="8431d-145">انتقل إلى **إدارة التغييرات الهندسية &gt; الإعداد &gt; حالة دورة حياة المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8431d-145">Go to **Engineering change management &gt; Setup &gt; Product lifecycle state**.</span></span>
1. <span data-ttu-id="8431d-146">حدد **جديد** لإضافة حالة دورة حياة، ثم عيِّن القيم التالية لها:</span><span class="sxs-lookup"><span data-stu-id="8431d-146">Select **New** to add a lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-147">**الحالة:** *جاهزه للعمل*</span><span class="sxs-lookup"><span data-stu-id="8431d-147">**State:** *Operational*</span></span>
    - <span data-ttu-id="8431d-148">**الوصف:** *جاهزة للعمل*</span><span class="sxs-lookup"><span data-stu-id="8431d-148">**Description:** *Operational*</span></span>

1. <span data-ttu-id="8431d-149">حدد **حفظ** لحفظ حالة دورة الحياة الجديدة وتحميل القيم علي علامة التبويب السريعة **عمليات الأعمال الممكنة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-149">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="8431d-150">في علامة التبويب السريعة **عمليات الاعمال الممكنة**، حدد عمليات الأعمال التي يجب ان تكون متاحه.</span><span class="sxs-lookup"><span data-stu-id="8431d-150">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="8431d-151">بالنسبة لهذا المثال، اترك حقل **النهج** معينا إلى *ممكن* لكافة عمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="8431d-151">For this example, leave the **Policy** field set to *Enabled* for all business processes.</span></span>

    <span data-ttu-id="8431d-152">![تمكين العمليات التجارية لحاله دوره الحياة](media/product-lifecycle-states-1.png "تمكين العمليات التجارية لحاله دوره الحياة")</span><span class="sxs-lookup"><span data-stu-id="8431d-152">![Enabling business processes for a lifecycle state](media/product-lifecycle-states-1.png "Enabling business processes for a lifecycle state")</span></span>

1. <span data-ttu-id="8431d-153">حدد **جديد** لإضافة حالة دورة حياة أخرى، ثم عيِّن القيم التالية لها:</span><span class="sxs-lookup"><span data-stu-id="8431d-153">Select **New** to add another lifecycle state, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-154">**الحالة:** *نموذج اولي*</span><span class="sxs-lookup"><span data-stu-id="8431d-154">**State:** *Prototype*</span></span>
    - <span data-ttu-id="8431d-155">**الوصف:** *نموذج اولي*</span><span class="sxs-lookup"><span data-stu-id="8431d-155">**Description:** *Prototype*</span></span>

1. <span data-ttu-id="8431d-156">حدد **حفظ** لحفظ حالة دورة الحياة الجديدة وتحميل القيم علي علامة التبويب السريعة **عمليات الأعمال الممكنة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-156">Select **Save** to save the new lifecycle state and load values onto the **Enabled business processes** FastTab.</span></span>
1. <span data-ttu-id="8431d-157">في علامة التبويب السريعة **عمليات الاعمال الممكنة**، حدد عمليات الأعمال التي يجب ان تكون متاحه.</span><span class="sxs-lookup"><span data-stu-id="8431d-157">On the **Enabled business processes** FastTab, select the business processes that should be available.</span></span> <span data-ttu-id="8431d-158">بالنسبة لهذا المثال، اترك حقل **النهج** معينا إلى *ممكن مع تحذير* لكافة عمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="8431d-158">For this example, set the **Policy** field to *Enabled with warning* for all business processes.</span></span>

    <span data-ttu-id="8431d-159">![تمكين العمليات التجارية (مع تحذيرات) لحاله دوره الحياة](media/product-lifecycle-states-2.png "تمكين العمليات التجارية (مع تحذيرات) لحاله دوره الحياة")</span><span class="sxs-lookup"><span data-stu-id="8431d-159">![Enabling (with warnings) business processes for a lifecycle state](media/product-lifecycle-states-2.png "Enabling (with warnings) business processes for a lifecycle state")</span></span>

### <a name="set-up-a-version-number-rule"></a><span data-ttu-id="8431d-160">اعداد قاعده رقم إصدار</span><span class="sxs-lookup"><span data-stu-id="8431d-160">Set up a version number rule</span></span>

1. <span data-ttu-id="8431d-161">انتقل إلى **إدارة التغييرات الهندسية &gt; الإعداد &gt; قاعدة رقم إصدار المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8431d-161">Go to **Engineering change management &gt; Setup &gt; Product version number rule**.</span></span>
1. <span data-ttu-id="8431d-162">حدد **جديد** لإضافة قاعدة، ثم عيِّن القيم التالية لها:</span><span class="sxs-lookup"><span data-stu-id="8431d-162">Select **New** to add a rule, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-163">**الاسم:** *تلقائي*</span><span class="sxs-lookup"><span data-stu-id="8431d-163">**Name:** *Auto*</span></span>
    - <span data-ttu-id="8431d-164">**قاعده الأرقام:** *تلقائية*</span><span class="sxs-lookup"><span data-stu-id="8431d-164">**Number rule:** *Auto*</span></span>
    - <span data-ttu-id="8431d-165">**التنسيق:** *V-\#\#*</span><span class="sxs-lookup"><span data-stu-id="8431d-165">**Format:** *V-\#\#*</span></span>

    <span data-ttu-id="8431d-166">![أضافه قاعده رقم إصدار منتج](media/version-number-rule.png "أضافه قاعده رقم إصدار منتج")</span><span class="sxs-lookup"><span data-stu-id="8431d-166">![Adding a product version number rule](media/version-number-rule.png "Adding a product version number rule")</span></span>

### <a name="set-up-a-product-release-policy"></a><span data-ttu-id="8431d-167">اعداد سياسة إصدار منتج</span><span class="sxs-lookup"><span data-stu-id="8431d-167">Set up a product release policy</span></span>

1. <span data-ttu-id="8431d-168">انتقل إلى **إدارة التغييرات الهندسية &gt; الإعداد &gt; سياسات إصدار المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8431d-168">Go to **Engineering change management &gt; Setup &gt; Product release policies**.</span></span>
1. <span data-ttu-id="8431d-169">حدد **جديد** لإضافة سياسة، ثم عيِّن القيم التالية لها:</span><span class="sxs-lookup"><span data-stu-id="8431d-169">Select **New** to add a release policy, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-170">**الاسم:** *المكونات*</span><span class="sxs-lookup"><span data-stu-id="8431d-170">**Name:** *Components*</span></span>
    - <span data-ttu-id="8431d-171">**الوصف:** *المكونات*</span><span class="sxs-lookup"><span data-stu-id="8431d-171">**Description:** *Components*</span></span>

1. <span data-ttu-id="8431d-172">في علامة التبويب السريعة **عام**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="8431d-172">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8431d-173">**نوع المنتج:** *الصنف*</span><span class="sxs-lookup"><span data-stu-id="8431d-173">**Product type:** *Item*</span></span>
    - <span data-ttu-id="8431d-174">**تطبيق القوالب:** *دائما*</span><span class="sxs-lookup"><span data-stu-id="8431d-174">**Apply templates:** *Always*</span></span>
    - <span data-ttu-id="8431d-175">**نشط:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="8431d-175">**Active:** *Yes*</span></span>

1. <span data-ttu-id="8431d-176">في علامة التبويب السريعة **جميع المنتجات**، حدد **إضافة** لإضافة سطر، ثم عيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="8431d-176">On the **All products** FastTab, select **Add** to add a line, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-177">**الشركة:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="8431d-177">**Company:** *DEMF*</span></span>
    - <span data-ttu-id="8431d-178">**قالب المنتج المُصدر:** *D0006*</span><span class="sxs-lookup"><span data-stu-id="8431d-178">**Template released product:** *D0006*</span></span>

1. <span data-ttu-id="8431d-179">حدد **إضافة** لإضافة سطر آخر، ثم قم بتعيين القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="8431d-179">Select **Add** to add another line, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-180">**معرف حسابات الشركة:** *USMF*</span><span class="sxs-lookup"><span data-stu-id="8431d-180">**Company accounts ID:** *USMF*</span></span>
    - <span data-ttu-id="8431d-181">**قالب المنتج المُصدر:** *D0006*</span><span class="sxs-lookup"><span data-stu-id="8431d-181">**Template released product:** *D0006*</span></span>
    - <span data-ttu-id="8431d-182">**استلام قائمة مكونات الصنف:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="8431d-182">**Receive BOM:** Select this check box.</span></span>
    - <span data-ttu-id="8431d-183">**نسخ اعتماد قائمه مكونات الصنف:** حدد خانه الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="8431d-183">**Copy BOM approval:** Select this check box.</span></span>
    - <span data-ttu-id="8431d-184">**نسخ تنشيط قائمه مكونات الصنف:** حدد خانه الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="8431d-184">**Copy BOM activation:** Select this check box.</span></span>
    - <span data-ttu-id="8431d-185">**مسار الاستلام:** حدد خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="8431d-185">**Receive route:** Select this check box.</span></span>
    - <span data-ttu-id="8431d-186">**نسخ اعتماد المسار:** حدد خانه الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="8431d-186">**Copy route approval:** Select this check box.</span></span>
    - <span data-ttu-id="8431d-187">**نسخ تنشيط المسار:** حدد خانه الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="8431d-187">**Copy route activation:** Select this check box.</span></span>

    <span data-ttu-id="8431d-188">![اضافة سياسة إصدار منتج](media/product-release-policy.png "اضافة سياسة إصدار منتج")</span><span class="sxs-lookup"><span data-stu-id="8431d-188">![Adding a product release policy](media/product-release-policy.png "Adding a product release policy")</span></span>

### <a name="set-up-an-engineering-product-category"></a><span data-ttu-id="8431d-189">اعداد فئة منتج هندسي</span><span class="sxs-lookup"><span data-stu-id="8431d-189">Set up an engineering product category</span></span> 

<span data-ttu-id="8431d-190">توفر فئات المنتجات الهندسية أساسا لإنشاء المنتجات الهندسية (اي المنتجات التي يتم إصدارها والتحكم فيها من خلال أداره التغييرات الهندسية).</span><span class="sxs-lookup"><span data-stu-id="8431d-190">Engineering product categories provide the basis for creating engineering products (that is, products that are versioned and controlled through engineering change management).</span></span> <span data-ttu-id="8431d-191">لإعداد فئات المؤسسات الهندسية الخاصة بك‬، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="8431d-191">To set up engineering product categories, follow these steps.</span></span>

1. <span data-ttu-id="8431d-192">انتقل إلى **أداره التغييرات الهندسية &gt; تفاصيل فئة المنتج الهندسي**.</span><span class="sxs-lookup"><span data-stu-id="8431d-192">Go to **Engineering change management &gt; Engineering product category details**.</span></span>
1. <span data-ttu-id="8431d-193">حدد **جديد**، لإنشاء فئة.</span><span class="sxs-lookup"><span data-stu-id="8431d-193">Select **New** to create a category.</span></span>
1. <span data-ttu-id="8431d-194">في علامة التبويب السريعة **التفاصيل**، عيّن القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="8431d-194">On the **Details** FastTab, set the following values:</span></span>

    - <span data-ttu-id="8431d-195">**الاسم:** *المكونات*</span><span class="sxs-lookup"><span data-stu-id="8431d-195">**Name:** *Components*</span></span>
    - <span data-ttu-id="8431d-196">**المؤسسة الهندسية:** *DEMF*</span><span class="sxs-lookup"><span data-stu-id="8431d-196">**Engineering organization:** *DEMF*</span></span>
    - <span data-ttu-id="8431d-197">**نوع المنتج:** *الصنف*</span><span class="sxs-lookup"><span data-stu-id="8431d-197">**Product type:** *Item*</span></span>
    - <span data-ttu-id="8431d-198">**إصدار التتبع في المعاملات:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="8431d-198">**Track version in transactions:** *Yes*</span></span>
    - <span data-ttu-id="8431d-199">**مجموعة أبعاد المنتج:** *الإصدار*</span><span class="sxs-lookup"><span data-stu-id="8431d-199">**Product dimension group:** *Version*</span></span>
    - <span data-ttu-id="8431d-200">**حاله دوره حياه المنتج عند الإنشاء:** *جاهز للعمل*</span><span class="sxs-lookup"><span data-stu-id="8431d-200">**Product lifecycle state at creation:** *Operational*</span></span>
    - <span data-ttu-id="8431d-201">**قاعده رقم الإصدار:** *تلقائية*</span><span class="sxs-lookup"><span data-stu-id="8431d-201">**Version number rule:** *Auto*</span></span>
    - <span data-ttu-id="8431d-202">**فرض الفعالية:** *لا*</span><span class="sxs-lookup"><span data-stu-id="8431d-202">**Enforce effectivity:** *No*</span></span>
    - <span data-ttu-id="8431d-203">**استخدم مصطلحات قاعده الرقم:** *لا*</span><span class="sxs-lookup"><span data-stu-id="8431d-203">**Use number rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="8431d-204">**استخدم مصطلحات قاعده الاسم:** *لا*</span><span class="sxs-lookup"><span data-stu-id="8431d-204">**Use name rule nomenclature:** *No*</span></span>
    - <span data-ttu-id="8431d-205">**استخدم مصطلحات قاعده الوصف:** *لا*</span><span class="sxs-lookup"><span data-stu-id="8431d-205">**Use description rule nomenclature:** *No*</span></span>

1. <span data-ttu-id="8431d-206">في علامة التبويب السريعة **سياسة الإصدار**، قم بتعيين حقل **سياسة إصدار المنتج** إلى *المكونات*.</span><span class="sxs-lookup"><span data-stu-id="8431d-206">On the **Release policy** FastTab, set the **Product release policy** field to *Components*.</span></span>
1. <span data-ttu-id="8431d-207">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8431d-207">Select **Save**.</span></span>

    <span data-ttu-id="8431d-208">![اضافة فئة منتج هندسي](media/product-category-details.png "اضافة فئة منتج هندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-208">![Adding an engineering product category](media/product-category-details.png "Adding an engineering product category")</span></span>

### <a name="set-up-product-acceptance-conditions"></a><span data-ttu-id="8431d-209">اعداد شروط قبول المنتج</span><span class="sxs-lookup"><span data-stu-id="8431d-209">Set up product acceptance conditions</span></span>

1. <span data-ttu-id="8431d-210">استخدم منتقي الشركة علي الجانب الأيمن من شريط التنقل للتبديل إلى الكيان القانوني (الشركة) *USMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-210">Use the company picker on the right side of the navigation bar to switch to the *USMF* legal entity (company).</span></span>
1. <span data-ttu-id="8431d-211">انتقل إلى **إدارة التغييرات الهندسية &gt; الإعداد &gt; معلمات إدارة التغييرات الهندسية**.</span><span class="sxs-lookup"><span data-stu-id="8431d-211">Go to **Engineering change management &gt; Setup &gt; Engineering change management parameters**.</span></span>
1. <span data-ttu-id="8431d-212">في علامة التبويب **التحكم بالإصدار**، في قسم **قبول المنتج**، قم بتعيين حقل **قبول المنتج** إلى *يدوي*.</span><span class="sxs-lookup"><span data-stu-id="8431d-212">On the **Release control** tab, in the **Product acceptance** section, set the **Product acceptance** field to *Manual*.</span></span>

    <span data-ttu-id="8431d-213">![اعداد شروط قبول المنتج](media/engineering-change-management-parameters.png "اعداد شروط قبول المنتج")</span><span class="sxs-lookup"><span data-stu-id="8431d-213">![Setting up product acceptance conditions](media/engineering-change-management-parameters.png "Setting up product acceptance conditions")</span></span>

## <a name="create-a-new-engineering-product"></a><span data-ttu-id="8431d-214">إنشاء منتج هندسي جديد</span><span class="sxs-lookup"><span data-stu-id="8431d-214">Create a new engineering product</span></span>

<span data-ttu-id="8431d-215">المنتج الهندسي هو منتج يتم إصداره والتحكم فيه من خلال أداره التغييرات الهندسية.</span><span class="sxs-lookup"><span data-stu-id="8431d-215">An engineering product is a product that is versioned and controlled through engineering change management.</span></span> <span data-ttu-id="8431d-216">بمعني آخر، يمكنك التحكم في التغييرات اثناء حياتها، سيتم حفظ معلومات التغيير باستخدام أوامر التغيير الهندسي.</span><span class="sxs-lookup"><span data-stu-id="8431d-216">In other words, you can control the changes during its life, and the change information will be saved using engineering change orders.</span></span> <span data-ttu-id="8431d-217">لإنشاء منتجات هندسية، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8431d-217">To create engineering products, follow these steps.</span></span>

1. <span data-ttu-id="8431d-218">تاكد من انك في الكيان القانوني للمؤسسه الهندسية الخاصة بك ( *DEMF* لهذا المثال).</span><span class="sxs-lookup"><span data-stu-id="8431d-218">Make sure that you're in the legal entity of your engineering organization (*DEMF* for this example).</span></span> <span data-ttu-id="8431d-219">استخدم منتقي الشركة علي الجانب الأيمن من شريط التنقل كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="8431d-219">Use the company picker on the right side of the navigation bar as required.</span></span>
1. <span data-ttu-id="8431d-220">افتح صفحة **المنتجات الصادرة**، من خلال اتباع إحدى الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8431d-220">Open the **Released products** page by following one of these steps:</span></span>

    - <span data-ttu-id="8431d-221">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-221">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
    - <span data-ttu-id="8431d-222">انتقل إلى **إدارة التغييرات الهندسية &gt; عام &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-222">Go to **Engineering change management &gt; Common &gt; Released products**.</span></span>

1. <span data-ttu-id="8431d-223">في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **جديد‬**، حدد **منتج هندسي**.</span><span class="sxs-lookup"><span data-stu-id="8431d-223">On the Action Pane, on the **Product** tab, in the **New** group, select **Engineering product**.</span></span>
1. <span data-ttu-id="8431d-224">في مربع الحوار **منتج جديد**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="8431d-224">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="8431d-225">**فئة المنتج الهندسي:** *المكونات*</span><span class="sxs-lookup"><span data-stu-id="8431d-225">**Engineering Product Category:** *Components*</span></span>
    - <span data-ttu-id="8431d-226">**رقم المنتج:** *Z0001*</span><span class="sxs-lookup"><span data-stu-id="8431d-226">**Product number:** *Z0001*</span></span>
    - <span data-ttu-id="8431d-227">**اسم المنتج:** *مجموعه المتحدثين*</span><span class="sxs-lookup"><span data-stu-id="8431d-227">**Product name:** *Speaker set*</span></span>

    <span data-ttu-id="8431d-228">![اضافة منتج هندسي](media/new-product-dialog.png "اضافة منتج هندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-228">![Adding an engineering product](media/new-product-dialog.png "Adding an engineering product")</span></span>

    <span data-ttu-id="8431d-229">لاحظ انه يتم تعيين حقل **الإصدار** تلقائيا باستخدام قاعده رقم إصدار المنتج التي قمت باعدادها في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="8431d-229">Note that the **Version** field is automatically set by using the product version number rule that you set up earlier.</span></span>

1. <span data-ttu-id="8431d-230">حدد **موافق** لإنشاء المنتج وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="8431d-230">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="8431d-231">يتم فتح صفحه التفاصيل الخاصة بالمنتج الجديد.</span><span class="sxs-lookup"><span data-stu-id="8431d-231">The details page for the new product is opened.</span></span> <span data-ttu-id="8431d-232">لاحظ انه تم بالفعل ملء القيم لبعض الحقول، مثل **مجموعه ابعاد التخزين** و/أو **مجموعه ابعاد التعقب** و /أو **مجموعه نماذج الصنف**.</span><span class="sxs-lookup"><span data-stu-id="8431d-232">Notice that values are already filled in for some fields, such as **Storage dimension group**, **Tracking dimension group**, and/or **Item model group**.</span></span> <span data-ttu-id="8431d-233">تم تعيين هذه الحقول تلقائيا لان المنتج يتم إصداره في الكيان القانوني *DEMF* وتستخدم سياسة إصدار المنتج *المكونات*، المرتبط بفئة المنتج الهندسي *المكونات*.</span><span class="sxs-lookup"><span data-stu-id="8431d-233">These fields were automatically set because the product is being released in the *DEMF* legal entity and uses the *Components* product release policy, which is associated with the *Components* engineering product category.</span></span> <span data-ttu-id="8431d-234">نظرا لاستخدام الصنف مسبقا  *D0006* كقالب لاعداد بند للكيان القانوني *DEMF*، يتم أخذ القيم التي تم ملؤها من البند *D0006*.</span><span class="sxs-lookup"><span data-stu-id="8431d-234">Because you previously used item *D0006* as a template to set up a line for the *DEMF* legal entity, the values that were filled in were taken from item *D0006*.</span></span>

    <span data-ttu-id="8431d-235">![تفاصيل المنتج الذي تم إصداره](media/product-details.png "تفاصيل المنتج الذي تم إصداره")</span><span class="sxs-lookup"><span data-stu-id="8431d-235">![Released product details](media/product-details.png "Released product details")</span></span>

1. <span data-ttu-id="8431d-236">في قسم الإجراءات، ضمن علامة التبويب **المهندس**، في المجموعة **أداره التغييرات الهندسية**، حدد **إصدارات هندسية** لعرض إصدارات المنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-236">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions** to view the versions of the product.</span></span>

    <span data-ttu-id="8431d-237">![إصدارات الهندسة](media/engineering-versions-list.png "إصدارات الهندسة")</span><span class="sxs-lookup"><span data-stu-id="8431d-237">![Engineering versions](media/engineering-versions-list.png "Engineering versions")</span></span>

1. <span data-ttu-id="8431d-238">في صفحه **الإصدارات الهندسية**، لاحظ انه يوجد إصدار واحد فقط للمنتج، ويكون نشطا.</span><span class="sxs-lookup"><span data-stu-id="8431d-238">On the **Engineering versions** page, notice that there is only one version for the product, and it's active.</span></span>
1. <span data-ttu-id="8431d-239">حدد الإصدار لعرض تفاصيله.</span><span class="sxs-lookup"><span data-stu-id="8431d-239">Select the version to view its details.</span></span>

    <span data-ttu-id="8431d-240">![تفاصيل الإصدار الهندسي](media/engineering-version-details.png "تفاصيل الإصدار الهندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-240">![Engineering version details](media/engineering-version-details.png "Engineering version details")</span></span>

1. <span data-ttu-id="8431d-241">في الصفحة **الإصدار الهندسي**، على علامة التبويب السريعة **قائمة مكونات الصنف**، حدد **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="8431d-241">On the **Engineering version** page, on the **Bill of material** FastTab, select **Create BOM**.</span></span>
1. <span data-ttu-id="8431d-242">في مربع الحوار **إنشاء قائمة مكونات الصنف**، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="8431d-242">In the **Create BOM** dialog box, set the following values:</span></span>

    - <span data-ttu-id="8431d-243">**رقم قائمة مكونات الصنف:** Z0001</span><span class="sxs-lookup"><span data-stu-id="8431d-243">**BOM number:** Z0001</span></span>
    - <span data-ttu-id="8431d-244">**الاسم:** مجموعه المتحدثين</span><span class="sxs-lookup"><span data-stu-id="8431d-244">**Name:** Speaker set</span></span>
    - <span data-ttu-id="8431d-245">**الموقع:** 1</span><span class="sxs-lookup"><span data-stu-id="8431d-245">**Site:** 1</span></span>

    <span data-ttu-id="8431d-246">![إنشاء BOM](media/create-bom.png "إنشاء BOM")</span><span class="sxs-lookup"><span data-stu-id="8431d-246">![Creating a BOM](media/create-bom.png "Creating a BOM")</span></span>

1. <span data-ttu-id="8431d-247">حدد **موافق** لإضافة قائمة مكونات الصنف وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="8431d-247">Select **OK** to add the BOM and close the dialog box.</span></span>
1. <span data-ttu-id="8431d-248">في علامة التبويب السريعة **قائمة مكونات الصنف**، حدد **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="8431d-248">On the **Bill of materials** FastTab, select **Bill of material**.</span></span>
1. <span data-ttu-id="8431d-249">في صفح **قائمة مكونات الصنف**، في علامة التبويب السريعة **بنود قائمه مكونات الصنف**، أضف ثلاثه سطور، كل منها لأحد أرقام الأصناف *D0001* و *D0003* و *D0006*.</span><span class="sxs-lookup"><span data-stu-id="8431d-249">On the **Bill of materials** page, on the **Bill of materials lines** FastTab, add three lines, one each for item numbers *D0001*, *D0003*, and *D0006*.</span></span>

    <span data-ttu-id="8431d-250">![أضافه بنود قائمه مكونات الصنف](media/bom.png "أضافه بنود قائمه مكونات الصنف")</span><span class="sxs-lookup"><span data-stu-id="8431d-250">![Adding BOM lines](media/bom.png "Adding BOM lines")</span></span>

1. <span data-ttu-id="8431d-251">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8431d-251">Select **Save**.</span></span>
1. <span data-ttu-id="8431d-252">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8431d-252">Close the page.</span></span>
1. <span data-ttu-id="8431d-253">في الصفحة **الإصدار الهندسي**، على علامة التبويب السريعة **قائمة مكونات الصنف**، حدد **اعتماد**.</span><span class="sxs-lookup"><span data-stu-id="8431d-253">On the **Engineering version** page, on the **Bill of material** FastTab, select **Approve**.</span></span>
1. <span data-ttu-id="8431d-254">في مربع الحوار الذي يظهر، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8431d-254">In the dialog box that appears, select **OK**.</span></span>

    <span data-ttu-id="8431d-255">![اعتماد قائمة مكونات الصنف](media/approve-dialog.png "اعتماد قائمة مكونات الصنف")</span><span class="sxs-lookup"><span data-stu-id="8431d-255">![Approving the BOM](media/approve-dialog.png "Approving the BOM")</span></span>

1. <span data-ttu-id="8431d-256">في الصفحة **الإصدار الهندسي**، على علامة التبويب السريعة **قائمة مكونات الصنف**، حدد **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="8431d-256">On the **Engineering version** page, on the **Bill of material** FastTab, select **Activate**.</span></span>
1. <span data-ttu-id="8431d-257">لاحظ ان خانتي الاختيار **نشط** و **معتمد** محدده لقائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="8431d-257">Notice that the **Active** and **Approved** check boxes are selected for the BOM.</span></span>

    <span data-ttu-id="8431d-258">![قائمة مكونات الصنف النشطة والمعتمدة](media/approved-bom.png "قائمة مكونات الصنف النشطة والمعتمدة")</span><span class="sxs-lookup"><span data-stu-id="8431d-258">![Active and approved BOM](media/approved-bom.png "Active and approved BOM")</span></span>

1. <span data-ttu-id="8431d-259">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8431d-259">Close the page.</span></span>

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a><span data-ttu-id="8431d-260">إصدار منتج هندسي لشركه محليه</span><span class="sxs-lookup"><span data-stu-id="8431d-260">Release an engineering product to a local company</span></span>

<span data-ttu-id="8431d-261">لقد تم الآن تصميم المنتج بواسطة القسم الهندسي.</span><span class="sxs-lookup"><span data-stu-id="8431d-261">The product has now been designed by the Engineering department.</span></span> <span data-ttu-id="8431d-262">بالنسبة لهذا المثال، يعتبر المنتج نموذجا أوليا تم تصميمه لأحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="8431d-262">For this example, the product is a prototype that engineering has designed for a customer.</span></span> <span data-ttu-id="8431d-263">نظرا لان العميل هو عميل للكيان القانوني *USMF*، يجب إصدار المنتج لهذا الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="8431d-263">Because the customer is a customer of the *USMF* legal entity, the product must be released to that legal entity.</span></span>

1. <span data-ttu-id="8431d-264">الاحتفاظ بإعداد الكيان القانوني على *DEMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-264">Keep the legal entity set to *DEMF*.</span></span> <span data-ttu-id="8431d-265">(استخدم منتقي الشركة علي الجانب الأيمن من شريط التنقل كما هو مطلوب.)</span><span class="sxs-lookup"><span data-stu-id="8431d-265">(Use the company picker on the right side of the navigation bar as required.)</span></span>
1. <span data-ttu-id="8431d-266">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-266">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="8431d-267">تحديد المنتج *Z0001*.</span><span class="sxs-lookup"><span data-stu-id="8431d-267">Select product *Z0001*.</span></span>
1. <span data-ttu-id="8431d-268">في جزء الإجراءات، ضمن علامة التبويب **المنتج**، في المجموعة **صيانة**، حدد **إصدار بنيه المنتج** لفتح معالج **منتجات الإصدار**.</span><span class="sxs-lookup"><span data-stu-id="8431d-268">On the Action Pane, on the **Product** tab, in the **Maintain** group, select **Release product structure** to open the **Release products** wizard.</span></span>
1. <span data-ttu-id="8431d-269">في الصفحة **تحديد المنتجات الهندسية للإصدار**، حدد خانه الاختيار **تحديد** للمنتج *Z0001*.</span><span class="sxs-lookup"><span data-stu-id="8431d-269">On the **Select engineering products to release** page, select the **Select** check box for product *Z0001*.</span></span>

    <span data-ttu-id="8431d-270">![تحديد المنتجات الهندسية لإصدارها](media/select-eng-product-to-release.png "تحديد المنتجات الهندسية لإصدارها")</span><span class="sxs-lookup"><span data-stu-id="8431d-270">![Selecting the engineering products to release](media/select-eng-product-to-release.png "Selecting the engineering products to release")</span></span>

1. <span data-ttu-id="8431d-271">حدد **تفاصيل الإصدار**.</span><span class="sxs-lookup"><span data-stu-id="8431d-271">Select **Release details**.</span></span>
1. <span data-ttu-id="8431d-272">تظهر الصفحة **تفاصيل إصدار المنتج**، حيث يمكنك مراجعه تفاصيل المنتج الذي سيتم إصداره، وبنيه المنتج الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="8431d-272">The **Product release details** page appears, where you can review the details of the product that will be released, and its product structure.</span></span> <span data-ttu-id="8431d-273">تأكد من تعيين خيار **إرسال قائمة مكونات الصنف** إلى *نعم*.</span><span class="sxs-lookup"><span data-stu-id="8431d-273">Notice that the **Send BOM** option is set to *Yes*.</span></span> <span data-ttu-id="8431d-274">لذلك، سيتم إصدار كل من المنتج *Z0001* وكافة الأصناف الفرعية الخاصة به من قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="8431d-274">Therefore, both product *Z0001* and all its child items from the BOM will be released.</span></span>

    <span data-ttu-id="8431d-275">يمكنك تحديد اي عنصر تابع في الجزء الأيمن لمراجعه التفاصيل الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="8431d-275">You can select any child item in the left pane to review its details.</span></span> <span data-ttu-id="8431d-276">إذا كان لأي صنف تابع قائمة مكونات الصنف، فيمكنك أيضا تحديد إصدار قائمة مكونات الصنف الخاصة بهذا الصنف الفرعي.</span><span class="sxs-lookup"><span data-stu-id="8431d-276">If any child item has a BOM, you can also select to release the BOM of that child item.</span></span>

    <span data-ttu-id="8431d-277">![مراجعه تفاصيل إصدار المنتج](media/product-release-details.png "مراجعه تفاصيل إصدار المنتج")</span><span class="sxs-lookup"><span data-stu-id="8431d-277">![Reviewing the product release details](media/product-release-details.png "Reviewing the product release details")</span></span>

1. <span data-ttu-id="8431d-278">قم بإغلاق الصفحة للعودة إلى معالج **إصدار المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="8431d-278">Close the page to return to the **Release products** wizard.</span></span>
1. <span data-ttu-id="8431d-279">حدد **التالي** لفتح صفحة **تحديد المنتجات للإصدار**.</span><span class="sxs-lookup"><span data-stu-id="8431d-279">Select **Next** to open the **Select products to release** page.</span></span> <span data-ttu-id="8431d-280">إذا كنت قد قمت بتحديد إيه منتجات قياسيه (غير هندسية)، ستظهر علي هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8431d-280">If you had selected any standard (non-engineering) products, they would appear on this page.</span></span> <span data-ttu-id="8431d-281">لاحظ انه عند إصدار منتج قياسي عن طريق تحديد **بنيه منتج الإصدار**، يتم أيضا إصدار قائمه مكونات الصنف والمسار الخاص به.</span><span class="sxs-lookup"><span data-stu-id="8431d-281">Note that when you release a standard product by selecting **Release product structure**, its BOM and route are also released.</span></span>

    <span data-ttu-id="8431d-282">![تحديد المنتجات القياسية لإصدارها](media/select-std-product-to-release.png "تحديد المنتجات القياسية لإصدارها")</span><span class="sxs-lookup"><span data-stu-id="8431d-282">![Selecting the standard products to release](media/select-std-product-to-release.png "Selecting the standard products to release")</span></span>

1. <span data-ttu-id="8431d-283">حدد **التالي** لفتح صفحة **تحديد متغيرات المنتجات للإصدار**.</span><span class="sxs-lookup"><span data-stu-id="8431d-283">Select **Next** to open the **Select product variants to release** page.</span></span> <span data-ttu-id="8431d-284">علي سبيل المثال، لا توجد إيه متغيرات.</span><span class="sxs-lookup"><span data-stu-id="8431d-284">For this example, there aren't any variants.</span></span>
1. <span data-ttu-id="8431d-285">حدد **التالي** لفتح صفحة **تحديد الشركات**.</span><span class="sxs-lookup"><span data-stu-id="8431d-285">Select **Next** to open the **Select companies** page.</span></span>
1. <span data-ttu-id="8431d-286">حدد الشركات التي يجب إصدار المنتج اليها.</span><span class="sxs-lookup"><span data-stu-id="8431d-286">Select the companies that the product should be released to.</span></span> <span data-ttu-id="8431d-287">لهذا المثال، حدد خانة الاختيار **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8431d-287">For this example, select the check box for **USMF**.</span></span>

    <span data-ttu-id="8431d-288">![تحديد الشركات المراد الإصدار لها](media/select-release-companies.png "تحديد الشركات المراد الإصدار لها")</span><span class="sxs-lookup"><span data-stu-id="8431d-288">![Selecting the companies to release to](media/select-release-companies.png "Selecting the companies to release to")</span></span>

1. <span data-ttu-id="8431d-289">حدد **التالي** لفتح صفحة **تأكيد التحديد**.</span><span class="sxs-lookup"><span data-stu-id="8431d-289">Select **Next** to open the **Confirm selection** page.</span></span>
1. <span data-ttu-id="8431d-290">حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="8431d-290">Select **Finish**.</span></span>

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a><span data-ttu-id="8431d-291">قم بمراجعه المنتج وقبوله قبل إصداره في الشركة المحلية</span><span class="sxs-lookup"><span data-stu-id="8431d-291">Review and accept the product before you release it in the local company</span></span>

<span data-ttu-id="8431d-292">لقد قام الآن قسم الهندسة بإصدار المعلومات إلى الشركات المحلية حيث سيتم استخدام المنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-292">The Engineering department has now released the information to the local companies where the product will be used.</span></span> <span data-ttu-id="8431d-293">في هذا المثال، الشركة المحلية هي *USMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-293">For this example, the local company is *USMF*.</span></span>

<span data-ttu-id="8431d-294">نظرا لأنك تقوم بتعيين حقل **قبول المنتج** على *يدوي* في صفحه **معلمات أداره التغييرات الهندسية** للشركة *USMF*، يجب قبول المنتجات يدويا قبل إصدارها لهذه الشركة.</span><span class="sxs-lookup"><span data-stu-id="8431d-294">Because you set the **Product acceptance** field to *Manual* on the **Engineering change management parameters** page for the *USMF* company, products must be manually accepted before they are released to that company.</span></span> <span data-ttu-id="8431d-295">بمعني آخر، يجب مراجعتها وقبولها قبل ان تصبح منتجات تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="8431d-295">In other words, they must be reviewed and accepted before they become released products.</span></span>

<span data-ttu-id="8431d-296">لمراجعه المنتج وإصداره في الشركة *USMF*، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8431d-296">To review the product and release it in the *USMF* company, follow these steps.</span></span>

1. <span data-ttu-id="8431d-297">إعداد الكيان القانوني على *USMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-297">Set the legal entity to *USMF*.</span></span> <span data-ttu-id="8431d-298">(استخدم منتقي الشركة علي الجانب الأيمن من شريط التنقل.)</span><span class="sxs-lookup"><span data-stu-id="8431d-298">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="8431d-299">الانتقال إلى **أداره التغييرات الهندسية &gt; عام &gt; إصدارات المنتج &gt; افتح إصدارات المنتجات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-299">Go to **Engineering change management &gt; Common &gt; Product releases &gt; Open product releases**.</span></span>

    <span data-ttu-id="8431d-300">تعرض صفحه **إصدارات المنتجات المفتوحة** المنتج *Z0001*، والذي تكون حالته هي *الموافقة معلقة*.</span><span class="sxs-lookup"><span data-stu-id="8431d-300">The **Open product releases** page shows product *Z0001*, which has a status of *Pending acceptance*.</span></span>

    <span data-ttu-id="8431d-301">![فتح إصدارات المنتجات](media/open-product-releases.png "فتح إصدارات المنتجات")</span><span class="sxs-lookup"><span data-stu-id="8431d-301">![Open product releases](media/open-product-releases.png "Open product releases")</span></span>

1. <span data-ttu-id="8431d-302">حدد القيمة في العمود **رقم المنتج** لفتح الصفحة **تفاصيل إصدار المنتج**.</span><span class="sxs-lookup"><span data-stu-id="8431d-302">Select the value in the **Product number** column to open the **Product release details** page.</span></span> <span data-ttu-id="8431d-303">لاحظ التفاصيل التالية:</span><span class="sxs-lookup"><span data-stu-id="8431d-303">Notice the following details:</span></span>

    - <span data-ttu-id="8431d-304">تظهر علامة التبويب السريعة **عام** معلومات حول إصدار المنتج، مثل الشركة التي تقوم بالإصدار ( *DEMF* لهذا المثال) وموقع الإطلاق ( *1*) وموقع الاستلام ( *1*).</span><span class="sxs-lookup"><span data-stu-id="8431d-304">The **General** FastTab shows information about the product release, such as the releasing company (*DEMF* for this example), the releasing site (*1*), and the receiving site (*1*).</span></span> <span data-ttu-id="8431d-305">ونظرا لأنك لم تحدد موقع استلام في معالج **منتجات الإصدار**، يتم نسخ قيمه الموقع الإصدار إلى موقع الاستلام.</span><span class="sxs-lookup"><span data-stu-id="8431d-305">Because you didn't specify a receiving site in the **Release products** wizard, the the releasing site value is copied to the receiving site.</span></span>
    - <span data-ttu-id="8431d-306">تعرض علامة التبويب السريعة **تفاصيل الإصدار** معلومات حول المنتج والإصدار الذي تم إصداره.</span><span class="sxs-lookup"><span data-stu-id="8431d-306">The **Release details** FastTab shows information about the product and the version that was released.</span></span> <span data-ttu-id="8431d-307">وهنا، يمكنك تعديل الإعدادات مثل تواريخ السريان.</span><span class="sxs-lookup"><span data-stu-id="8431d-307">Here, you can modify settings such as the effectivity dates.</span></span>
    - <span data-ttu-id="8431d-308">تعرض علامة التبويب السريعة **المسار** مسار المنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-308">The **Route** FastTab shows the route of the product.</span></span> <span data-ttu-id="8431d-309">علي الرغم من ذلك ، بالنسبة لهذا المثال ، لم تحرر إيه مسارات.</span><span class="sxs-lookup"><span data-stu-id="8431d-309">However, for this example, you didn't release any routes.</span></span>

    <span data-ttu-id="8431d-310">![تفاصيل إصدار المنتج](media/product-release-details-2.png "تفاصيل إصدار المنتج")</span><span class="sxs-lookup"><span data-stu-id="8431d-310">![Product release details](media/product-release-details-2.png "Product release details")</span></span>

1. <span data-ttu-id="8431d-311">عندما تنتهي من مراجعه المعلومات ، فانك تكون مستعدا لقبول المنتج وبهذه الطريقة ، إصداره في شركة *USMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-311">When you've finished reviewing the information, you're ready to accept the product and, in this way, release it in the *USMF* company.</span></span> <span data-ttu-id="8431d-312">في جزء الإجراءات، حدد **الإجراءات &gt; قبول**.</span><span class="sxs-lookup"><span data-stu-id="8431d-312">On the Action Pane, select **Actions &gt; Accept**.</span></span>
1. <span data-ttu-id="8431d-313">تم إصدار المنتج الآن في شركة *USMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-313">The product is now released in the *USMF* company.</span></span> <span data-ttu-id="8431d-314">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-314">Go to **Product information management &gt;Products &gt; Released products**.</span></span> <span data-ttu-id="8431d-315">يجب ان تشاهد الصنف *Z0001*.</span><span class="sxs-lookup"><span data-stu-id="8431d-315">You should see item *Z0001*.</span></span>

## <a name="use-the-product-in-transactions-in-the-local-company"></a><span data-ttu-id="8431d-316">استخدام المنتج في الحركات الموجودة في الشركة المحلية</span><span class="sxs-lookup"><span data-stu-id="8431d-316">Use the product in transactions in the local company</span></span>

<span data-ttu-id="8431d-317">ويرغب مدير البيانات الرئيسي للشركة *USMF* في التاكد من ان المنتج في حاله *نموذج اولي* ، للتاكد من انه سيتم تحذير المستخدمين إذا قاموا بالمصادفة بإضافته إلى العمليات التي يعملون بها بطريق المصادفة.</span><span class="sxs-lookup"><span data-stu-id="8431d-317">The master data manager for the *USMF* company wants to make sure that the product is in a *Prototype* state, to ensure that users will be warned if they accidentally add it to processes that they are working on.</span></span>

1. <span data-ttu-id="8431d-318">انتقل إلى **إدارة معلومات المنتج‬ &gt; المنتجات &gt; المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-318">Go to **Product information management &gt; Products &gt; Released products**.</span></span>
1. <span data-ttu-id="8431d-319">حدد المنتج *Z0001* لفتح صفحه التفاصيل الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="8431d-319">Select product *Z0001* to open its details page.</span></span> <span data-ttu-id="8431d-320">(يمكنك استخدام عامل التصفية للعثور علي المنتج.)</span><span class="sxs-lookup"><span data-stu-id="8431d-320">(You can use the filter to find the product.)</span></span>
1. <span data-ttu-id="8431d-321">في جزء الإجراء، ضمن علامة التبويب **المهندس**، في مجموعة **‏إدارة التغييرات الهندسية**، حدد **الإصدارات الهندسية**.</span><span class="sxs-lookup"><span data-stu-id="8431d-321">On the Action Pane, on the **Engineer** tab, in the **Engineering change management** group, select **Engineering versions**.</span></span>
1. <span data-ttu-id="8431d-322">في صفحة **الإصدارات الهندسية**، حدد رقم الإصدار *V-01* لفتح صفحه التفاصيل الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="8431d-322">On the **Engineering versions** page, select version number *V-01* to open its details page.</span></span>
1. <span data-ttu-id="8431d-323">في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **حالة دورة الحياة‬**، حدد **تغيير حالة دورة الحياة**.</span><span class="sxs-lookup"><span data-stu-id="8431d-323">On the Action Pane, on the **Product** tab, in the **Lifecycle state** group, select **Change lifecycle state**.</span></span>
1. <span data-ttu-id="8431d-324">في مربع الحوار **تغيير حاله دوره الحياة**، قم بتعيين حقل **الحالة** إلى *نموذج اولي*، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8431d-324">In the **Change lifecycle state** drop-down dialog box, set the **State** field to *Prototype*, and then select **OK**.</span></span>

    <span data-ttu-id="8431d-325">![تغيير حالة دورة الحياة](media/change-lifecycle-state.png "تغيير حالة دورة الحياة")</span><span class="sxs-lookup"><span data-stu-id="8431d-325">![Changing the lifecycle state](media/change-lifecycle-state.png "Changing the lifecycle state")</span></span>

## <a name="add-the-engineering-product-to-a-sales-order"></a><span data-ttu-id="8431d-326">أضافه منتج هندسي لأمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="8431d-326">Add the engineering product to a sales order</span></span>

<span data-ttu-id="8431d-327">يمكن الآن بيع المنتج إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="8431d-327">The product can now be sold to a customer.</span></span> <span data-ttu-id="8431d-328">لإضافة المنتج إلى أمر مبيعات، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8431d-328">To add the product to a sales order, follow these steps.</span></span>

1. <span data-ttu-id="8431d-329">انتقل إلى **المبيعات والتسويق &gt; أوامر المبيعات &gt; كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="8431d-329">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="8431d-330">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8431d-330">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8431d-331">في مربع الحوار **إنشاء أمر مبيعات**، قم بإعداد حقل **حساب العميل**، على *US-0002* وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8431d-331">In the **Create sales order** dialog box, set the **Customer account** field to *US-0002*, and then select **OK**.</span></span>
1. <span data-ttu-id="8431d-332">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="8431d-332">The new sales order is opened.</span></span> <span data-ttu-id="8431d-333">في علامة التبويب السريعة **بنود أمر المبيعات**، قم باضافه صف، ثم قم بتعيين حقل **رقم الصنف** إلى *Z000* لهذا الصف.</span><span class="sxs-lookup"><span data-stu-id="8431d-333">On the **Sales order lines** FastTab, add a row, and set the **Item number** field to *Z000* for it.</span></span>
1. <span data-ttu-id="8431d-334">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8431d-334">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="8431d-335">وتتلقي رسالة تحذير تخبرك بان الصنف له الحالة *نموذج اولي*.</span><span class="sxs-lookup"><span data-stu-id="8431d-335">You receive a warning message that informs you that the item has a status of *Prototype*.</span></span> <span data-ttu-id="8431d-336">ومع ذلك ، نظرا لان الرسالة هي تحذير فقط ، فان أمر التوريد لا يزال يتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="8431d-336">However, because the message is just a warning, the sales order was still created.</span></span>

    <span data-ttu-id="8431d-337">![أمر المبيعات لمنتج هندسي](media/sales-order-eng-product.png "أمر المبيعات لمنتج هندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-337">![Sales order for an engineering product](media/sales-order-eng-product.png "Sales order for an engineering product")</span></span>

## <a name="request-changes-in-the-engineering-product"></a><span data-ttu-id="8431d-338">طلب اجراء تغييرات في المنتج الهندسي</span><span class="sxs-lookup"><span data-stu-id="8431d-338">Request changes in the engineering product</span></span>

<span data-ttu-id="8431d-339">تم إرسال المنتج إلى العميل ، ولكن لم يكن العميل راضيًا بالكامل ويقدم ملاحظات تتضمن اقتراحات للتحسين.</span><span class="sxs-lookup"><span data-stu-id="8431d-339">The product was sent to a customer, but the customer wasn't completely satisfied and provides feedback that includes suggestions for improvement.</span></span> <span data-ttu-id="8431d-340">بينما يكون العميل يتحدث مع موظف المبيعات علي الهاتف ، يمكن لموظف المبيعات طلب التغييرات التي يصفها العميل.</span><span class="sxs-lookup"><span data-stu-id="8431d-340">While the customer is speaking with a sales clerk on the phone, the sales clerk can request the changes that the customer is describing.</span></span>

1. <span data-ttu-id="8431d-341">انتقل إلى **المبيعات والتسويق &gt; أوامر المبيعات &gt; كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="8431d-341">Go to **Sales and marketing &gt; Sales orders &gt; All sales orders**.</span></span>
1. <span data-ttu-id="8431d-342">ابحث عن أمر التوريد الذي قمت بإنشاءه في التمرين السابق وافتحه.</span><span class="sxs-lookup"><span data-stu-id="8431d-342">Find and open the sales order that you created in the previous exercise.</span></span>
1. <span data-ttu-id="8431d-343">في علامة  التبويب السريعة **بنود أمر المبيعات**، حدد **أداره التغييرات الهندسية &gt; طلب التغيير الهندسي الجديد**.</span><span class="sxs-lookup"><span data-stu-id="8431d-343">On the **Sales order lines** FastTab, select **Engineering change management &gt; New engineering change request**.</span></span>

    <span data-ttu-id="8431d-344">![إنشاء طلب تغيير هندسي من أمر مبيعات](media/sales-order-eng-change-request.png "إنشاء طلب تغيير هندسي من أمر مبيعات")</span><span class="sxs-lookup"><span data-stu-id="8431d-344">![Creating an engineering change request from a sales order](media/sales-order-eng-change-request.png "Creating an engineering change request from a sales order")</span></span>

1. <span data-ttu-id="8431d-345">قم بملء طلب تغيير هندسي، بناء علي ملاحظات العميل.</span><span class="sxs-lookup"><span data-stu-id="8431d-345">Fill in the engineering change request, based on the customer's feedback.</span></span> <span data-ttu-id="8431d-346">بالنسبة إلى هذا المثال، قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="8431d-346">For this example, set the following values:</span></span>

    - <span data-ttu-id="8431d-347">**طلب التغيير:** *555*</span><span class="sxs-lookup"><span data-stu-id="8431d-347">**Change request:** *555*</span></span>
    - <span data-ttu-id="8431d-348">**العنوان:** *تغيير العميل Z0001*</span><span class="sxs-lookup"><span data-stu-id="8431d-348">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="8431d-349">**الاولويه:** *منخفضه*</span><span class="sxs-lookup"><span data-stu-id="8431d-349">**Priority:** *low*</span></span>
    - <span data-ttu-id="8431d-350">**الفئة:** تعيين التغيير</span><span class="sxs-lookup"><span data-stu-id="8431d-350">**Category:** set change</span></span>
    - <span data-ttu-id="8431d-351">**درجه الخطورة:** *متوسط*</span><span class="sxs-lookup"><span data-stu-id="8431d-351">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="8431d-352">في علامة التبويب السريعة **المعلومات**، حدد **جديد &gt; ملاحظة**  لإضافة ملاحظة إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="8431d-352">On the **Information** FastTab, select **New &gt; Note** to add a note to the grid.</span></span>
1. <span data-ttu-id="8431d-353">في الحقل **الوصف** للملاحظة الجديدة، قم بالاشاره إلى انه يجب حذف الصنف *D0003* من قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="8431d-353">In the **Description** field for the new note, indicate that item *D0003* should be deleted from the BOM.</span></span> <span data-ttu-id="8431d-354">إذا كان من الضروري أضافه مزيد من المعلومات للملاحظة ، يمكنك إدخال نص في حقل **الملاحظات**.</span><span class="sxs-lookup"><span data-stu-id="8431d-354">If you must add more information for the note, you can enter text in the **Notes** field.</span></span>

    <span data-ttu-id="8431d-355">![طلب تغيير الهندسة](media/eng-change-request.png "طلب تغيير الهندسة")</span><span class="sxs-lookup"><span data-stu-id="8431d-355">![Engineering change request](media/eng-change-request.png "Engineering change request")</span></span>

1. <span data-ttu-id="8431d-356">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8431d-356">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8431d-357">لاحظ انه تمت أضافه الصنف تلقائيا علام التبويب السريعة **المنتجات**، وانه قد تمت أضافه مصدر طلب التغيير الهندسي (أمر المبيعات) علي علامة التبويب السريعة **المصدر**.</span><span class="sxs-lookup"><span data-stu-id="8431d-357">Notice that the item has automatically been added on the **Products** FastTab, and that the source of the engineering change request (the sales order) has been added on the **Source** FastTab.</span></span>

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a><span data-ttu-id="8431d-358">اجراء تغييرات علي المنتج باستخدام أمر تغيير هندسي</span><span class="sxs-lookup"><span data-stu-id="8431d-358">Make changes to the product by using an engineering change order</span></span>

<span data-ttu-id="8431d-359">يعرف موظف المبيعات ان المنتج مهم وتم تصميمه خصيصا للعميل.</span><span class="sxs-lookup"><span data-stu-id="8431d-359">The sales clerk knows that the product is important and was designed especially for the customer.</span></span> <span data-ttu-id="8431d-360">لذلك، يقوم موظف المبيعات باستدعاء مهندس في شركة *DEMF* لاعلامه بطلب التغيير.</span><span class="sxs-lookup"><span data-stu-id="8431d-360">Therefore, the sales clerk calls an engineer in the *DEMF* company to notify them about the change request.</span></span> <span data-ttu-id="8431d-361">وبهذه الطريقة ، يمكن ان يقوم المهندس بتسريع العملية.</span><span class="sxs-lookup"><span data-stu-id="8431d-361">In this way, the engineer can speed up the process.</span></span>

<span data-ttu-id="8431d-362">يقوم المهندس الآن بمراجعه الطلب من العميل وإنشاء أمر تغيير للمنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-362">The engineer now reviews the request from the customer and creates a change order for the product.</span></span>

1. <span data-ttu-id="8431d-363">نظرا لان المهندس يعمل في شركة *DEMF*، قم بتعيين الكيان القانوني إلى *DEMF*.</span><span class="sxs-lookup"><span data-stu-id="8431d-363">Because the engineer works in the *DEMF* company, set the legal entity to *DEMF*.</span></span> <span data-ttu-id="8431d-364">(استخدم منتقي الشركة علي الجانب الأيمن من شريط التنقل.)</span><span class="sxs-lookup"><span data-stu-id="8431d-364">(Use the company picker on the right side of the navigation bar.)</span></span>
1. <span data-ttu-id="8431d-365">انتقل إلى **أداره التغييرات الهندسية &gt; عام &gt; طلبات التغيير الهندسية**.</span><span class="sxs-lookup"><span data-stu-id="8431d-365">Go to **Engineering change management &gt; Common &gt; Engineering change requests**.</span></span>
1. <span data-ttu-id="8431d-366">طلب التغيير المفتوح: *555*</span><span class="sxs-lookup"><span data-stu-id="8431d-366">Open change request *555*.</span></span>
1. <span data-ttu-id="8431d-367">راجع المعلومات، ثم قم باعتماد التغيير.</span><span class="sxs-lookup"><span data-stu-id="8431d-367">Review the information, and then approve the change.</span></span> <span data-ttu-id="8431d-368">ثم بعد ذلك، في جزء الإجراءات، ضمن علامة التبويب **طلب تغيير** ، في مجموعة **‏حالة التغيير**، حدد **اعتماد**.</span><span class="sxs-lookup"><span data-stu-id="8431d-368">On the Action Pane, on the **Change request** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="8431d-369">انتقل إلى **أداره التغييرات الهندسية &gt; عام &gt; أوامر التغيير الهندسية**.</span><span class="sxs-lookup"><span data-stu-id="8431d-369">Go to **Engineering change management &gt; Common &gt; Engineering change orders**.</span></span>
1. <span data-ttu-id="8431d-370">في جزء الإجراءات، حدد **جديد** لإنشاء أمر التغيير وعيِّن القيم التالية له:</span><span class="sxs-lookup"><span data-stu-id="8431d-370">On the Action Pane, select **New** to create a change order, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-371">**أمر التغيير:** *555*</span><span class="sxs-lookup"><span data-stu-id="8431d-371">**Change order:** *555*</span></span>
    - <span data-ttu-id="8431d-372">**العنوان:** *تغيير العميل Z0001*</span><span class="sxs-lookup"><span data-stu-id="8431d-372">**Title:** *Z0001 customer change*</span></span>
    - <span data-ttu-id="8431d-373">**الفئة:** *تغيير العميل*</span><span class="sxs-lookup"><span data-stu-id="8431d-373">**Category:** *Customer change*</span></span>
    - <span data-ttu-id="8431d-374">**الاولويه:** *منخفضه*</span><span class="sxs-lookup"><span data-stu-id="8431d-374">**Priority:** *Low*</span></span>
    - <span data-ttu-id="8431d-375">**درجه الخطورة:** *متوسط*</span><span class="sxs-lookup"><span data-stu-id="8431d-375">**Severity:** *Medium*</span></span>

1. <span data-ttu-id="8431d-376">على علامة التبويب السريعة **المنتجات المتأثرة**، حدد **جديد &gt; إضافة منتج موجود** لإضافة صف إلى الشبكة، ثم عيّن القيم التالية للمنتج الجديد:</span><span class="sxs-lookup"><span data-stu-id="8431d-376">On the **Impacted products** FastTab, select **New &gt; Add existing product** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="8431d-377">**المنتج:** *Z0001*</span><span class="sxs-lookup"><span data-stu-id="8431d-377">**Product:** *Z0001*</span></span>
    - <span data-ttu-id="8431d-378">**التاثير:** *إصدار جديد*</span><span class="sxs-lookup"><span data-stu-id="8431d-378">**Impact:** *New version*</span></span>

    <span data-ttu-id="8431d-379">![إنشاء أمر تغيير هندسي](media/eng-change-order.png "إنشاء أمر تغيير هندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-379">![Creating an engineering change order](media/eng-change-order.png "Creating an engineering change order")</span></span>

1. <span data-ttu-id="8431d-380">لاحظ انه ، نظرا لقيامك بتعيين الحقل **التاثير** إلى *الإصدار الجديد*، يظهر الحقل **الإصدار الجديد** في علامة التبويب **التفاصيل** الخاصة بعلامة التبويب السريعة **تفاصيل المنتج** ما هو رقم الإصدار الجديد ( *V-02* لهذا المثال).</span><span class="sxs-lookup"><span data-stu-id="8431d-380">Notice that, because you set the **Impact** field to *New version*, the **New version** field on the **Details** tab of the **Product details** FastTab shows what the new version number will be (*V-02* for this example).</span></span>

    <span data-ttu-id="8431d-381">![تفاصيل المنتج لأمر تغيير هندسي](media/eng-change-order-product-details.png "تفاصيل المنتج لأمر تغيير هندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-381">![Product details for an engineering change order](media/eng-change-order-product-details.png "Product details for an engineering change order")</span></span>

1. <span data-ttu-id="8431d-382">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8431d-382">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8431d-383">في علامة التبويب السريعة **تفاصيل المنتج**، ضمن علامة التبويب **قائمة مكونات الصنف**، حدد **البنود** لفتح قائمة مكونات الصنف الخاصة بالإصدار *V-01* من المنتج *Z0001*.</span><span class="sxs-lookup"><span data-stu-id="8431d-383">On the **Product details** FastTab, on the **Bill of material** tab, select **Lines** to open the BOM for version *V-01* of product *Z0001*.</span></span>

    <span data-ttu-id="8431d-384">![بنود قائمه مكونات الصنف لمنتج هندسي](media/eng-product-bom-lines.png "بنود قائمه مكونات الصنف لمنتج هندسي")</span><span class="sxs-lookup"><span data-stu-id="8431d-384">![Engineering product BOM lines](media/eng-product-bom-lines.png "Engineering product BOM lines")</span></span>

1. <span data-ttu-id="8431d-385">حدد البند لرقم الصنف *D0003*، ثم في جزء الاجراء ، حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="8431d-385">Select the line for item number *D0003*, and then, on the Action Pane, select **Delete**.</span></span> <span data-ttu-id="8431d-386">تتغير قيمه حقل **نوع التغيير** لهذا السطر إلى *محذوف*.</span><span class="sxs-lookup"><span data-stu-id="8431d-386">The value of the **Change type** field for this line changes to *Deleted*.</span></span>
1. <span data-ttu-id="8431d-387">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8431d-387">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="8431d-388">![بنود قائمه مكونات الصنف لمنتج هندسي معدل](media/eng-product-bom-lines-modified.png "بنود قائمه مكونات الصنف لمنتج هندسي معدل")</span><span class="sxs-lookup"><span data-stu-id="8431d-388">![Modified engineering product BOM lines](media/eng-product-bom-lines-modified.png "Modified engineering product BOM lines")</span></span>

1. <span data-ttu-id="8431d-389">قم بإغلاق صفحه **بند قائمة مكونات الصنف** للرجوع إلى الصفحة **أمر التغيير الهندسي**.</span><span class="sxs-lookup"><span data-stu-id="8431d-389">Close the **BOM line** page to return to the **Engineering change order** page.</span></span>
1. <span data-ttu-id="8431d-390">في علامة التبويب السريعة **تفاصيل المنتج**، ضمن علامة التبويب **قائمة مكونات الصنف**، لاحظ ان قيمه حقل **نوع التغيير** لقائمة مكونات الصنف *Z0001* أصبحت الآن *تم التغيير*.</span><span class="sxs-lookup"><span data-stu-id="8431d-390">On the **Product details** FastTab, on the **Bill of material** tab, notice that the value of the **Change type** field for BOM *Z0001* is now *Changed*.</span></span>

    <span data-ttu-id="8431d-391">![أمر التغيير الهندسي الذي يتضمن قائمة مكونات صنف تم تغييرها](media/eng-change-order-changed-bom.png "أمر التغيير الهندسي الذي يتضمن قائمة مكونات صنف تم تغييرها")</span><span class="sxs-lookup"><span data-stu-id="8431d-391">![Engineering change order that includes a changed BOM](media/eng-change-order-changed-bom.png "Engineering change order that includes a changed BOM")</span></span>

    <span data-ttu-id="8431d-392">يجب اعتماد الأمر قبل معالجة التغييرات.</span><span class="sxs-lookup"><span data-stu-id="8431d-392">The order must now be approved before the changes can be processed.</span></span> <span data-ttu-id="8431d-393">عند معالجه التغييرات ، يتم تحديث المنتجات بالتغييرات التي يتم تضمينها في أمر التغيير الهندسي.</span><span class="sxs-lookup"><span data-stu-id="8431d-393">When the changes are processed, the products are updated with the changes that are included in the engineering change order.</span></span> <span data-ttu-id="8431d-394">بالنسبة لهذا المثال ، تم تحديد الشخص الذي قام بإنشاء أمر التغيير الهندسي كمعتمد.</span><span class="sxs-lookup"><span data-stu-id="8431d-394">For this example, the person who creates the engineering change order has been specified as the approver.</span></span>

1. <span data-ttu-id="8431d-395">ثم بعد ذلك، في جزء الإجراءات، ضمن علامة التبويب **أمر التغيير**، في مجموعة **‏حالة التغيير**، حدد **اعتماد**.</span><span class="sxs-lookup"><span data-stu-id="8431d-395">On the Action Pane, on the **Change order** tab, in the **Change status** group, select **Approve**.</span></span>
1. <span data-ttu-id="8431d-396">حدد **عمليه** لتحديث معلومات المنتج.</span><span class="sxs-lookup"><span data-stu-id="8431d-396">Select **Process** to update the product's information.</span></span>
1. <span data-ttu-id="8431d-397">حدد **إكمال** لوضع علامة علي أمر التغيير كمكتمل.</span><span class="sxs-lookup"><span data-stu-id="8431d-397">Select **Complete** to mark the change order as completed.</span></span>

## <a name="release-the-changed-product"></a><span data-ttu-id="8431d-398">إصدار المنتج الذي تم تغييره</span><span class="sxs-lookup"><span data-stu-id="8431d-398">Release the changed product</span></span>

<span data-ttu-id="8431d-399">يمكن الآن إصدار المنتج مره أخرى إلى الشركة *USMF* ثم إرساله إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="8431d-399">The product can now be released again to the *USMF* company and then sent to the customer.</span></span> <span data-ttu-id="8431d-400">لإصدار المنتج مباشره من أمر التغيير الهندسي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8431d-400">To release the product directly from the engineering change order, follow these steps.</span></span>

1. <span data-ttu-id="8431d-401">افتح أمر التغيير الهندسي الذي قمت بإنشائه في التدريب السابق ، إذا لم يكن مفتوحا بالفعل.</span><span class="sxs-lookup"><span data-stu-id="8431d-401">Open the engineering change order that you created in the previous exercise, if it isn't already open.</span></span>
1. <span data-ttu-id="8431d-402">ثم بعد ذلك، في جزء الإجراءات، ضمن علامة التبويب **أمر التغيير**، في مجموعة **‏إصدارات المنتج**، حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="8431d-402">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Search**.</span></span>
1. <span data-ttu-id="8431d-403">تظهر نتائج البحث الشركات التي تم إصدار المنتجات المتاثره اليها.</span><span class="sxs-lookup"><span data-stu-id="8431d-403">The search results show which companies the affected products have been released to.</span></span> <span data-ttu-id="8431d-404">قم بإغلاق نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="8431d-404">Close the search results.</span></span>
1. <span data-ttu-id="8431d-405">في جزء الإجراءات ، ضمن علامة التبويب **أمر التغيير**، في المجموعة **إصدارات المنتجات**، حدد **عرض** لفتح مربع الحوار **إصدارات**، حيث يمكنك عرض نتائج البحث السابق.</span><span class="sxs-lookup"><span data-stu-id="8431d-405">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **View** to open the **Releases** dialog box, where you can view the results of the previous search.</span></span>
1. <span data-ttu-id="8431d-406">حدد كل شركه ترغب في تحرير المنتجات اليها.</span><span class="sxs-lookup"><span data-stu-id="8431d-406">Select each company that you want to release products to.</span></span>
1. <span data-ttu-id="8431d-407">حدد **موافق** لإغلاق مربع الحوار **الإصدارات** والعودة إلى أمر التغيير.</span><span class="sxs-lookup"><span data-stu-id="8431d-407">Select **OK** to close the **Releases** dialog box and return to the change order.</span></span>
1. <span data-ttu-id="8431d-408">في جزء الإجراءات ، ضمن علامة التبويب **أمر التغيير**، في المجموعة **إصدارات المنتجات**، حدد **معالجة** لإصدار المنتجات المتاثره إلى الشركات المحددة.</span><span class="sxs-lookup"><span data-stu-id="8431d-408">On the Action Pane, on the **Change order** tab, in the **Product releases** group, select **Process** to release the affected products to the selected companies.</span></span> <span data-ttu-id="8431d-409">وبدلا من ذلك ، حدد **إصدار بنيه المنتج** لبدء عمليه الإصدار.</span><span class="sxs-lookup"><span data-stu-id="8431d-409">Alternatively, select **Release product structure** to start the release process.</span></span>
