---
title: توفير بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية توفير بيئة تقييم Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/05/2020
ms.locfileid: "4410047"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="448b3-103">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="448b3-104">يوضح هذا الموضوع كيفية توفير بيئة تقييم Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="448b3-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="448b3-105">قبل البدء، نوصي بإجراء فحص سريع من خلال هذا الموضوع للتعرف علي فكره العملية التي تتطلبها.</span><span class="sxs-lookup"><span data-stu-id="448b3-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="448b3-106">لا تتوفر بيئات تقييم Commerce بشكل عام، ويتم منحها للشركاء والعملاء على أساس كل طلب.</span><span class="sxs-lookup"><span data-stu-id="448b3-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="448b3-107">لمزيد من المعلومات، اتصل بجهة اتصال شريك Microsoft.</span><span class="sxs-lookup"><span data-stu-id="448b3-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="448b3-108">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="448b3-108">Overview</span></span>

<span data-ttu-id="448b3-109">لتوفير بيئة تقييم Commerce بنجاح، يجب إنشاء مشروع له اسم منتج محدد ونوع معين.</span><span class="sxs-lookup"><span data-stu-id="448b3-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="448b3-110">تحتوي البيئة وCommerce Scale Unit (CSU) أيضًا على بعض المعلمات المحددة التي يجب استخدامها عند توقع توفير التجارة الإلكترونية في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="448b3-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="448b3-111">تصف الإرشادات الواردة في هذا الموضوع كافة الخطوات المطلوبة لإكمال توفيرها والمعلمات التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="448b3-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="448b3-112">بعد نجاحك في توفير بيئة تقييم Commerce، يجب إكمال بعض الخطوات التالية للتوفير لإعداد البيئة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="448b3-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="448b3-113">بعض الخطوات تكون اختيارية، بناءً على أوجه النظام التي ترغب في تقييمها.</span><span class="sxs-lookup"><span data-stu-id="448b3-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="448b3-114">يمكنك دائمًا إكمال الخطوات الاختيارية لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="448b3-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="448b3-115">للحصول على معلومات حول كيفية تكوين بيئة تقييم Commerce بعد توفيرها، راجع [ تكوين بيئة تقييم Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="448b3-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="448b3-116">للحصول على معلومات حول كيفية تكوين الميزات الاختيارية لبيئة تقييم Commerce، راجع [تكوين الميزات الاختيارية لبيئة تقييم Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="448b3-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="448b3-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="448b3-117">Prerequisites</span></span>

<span data-ttu-id="448b3-118">يجب توفر المتطلبات الأساسية التالية قبل توفير بيئة تقييم Commerce لك:</span><span class="sxs-lookup"><span data-stu-id="448b3-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="448b3-119">لقد تم ضمك إلى برنامج التقييم ولديك الآن إمكانيات بيئة التقييم.</span><span class="sxs-lookup"><span data-stu-id="448b3-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="448b3-120">يمكنك الوصول إلى مدخل Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="448b3-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="448b3-121">أنت أحد شركاء 365 Microsoft Dynamics الموجودين أو أحد العملاء ويمكنك إنشاء مشروع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="448b3-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="448b3-122">لديك حق الوصول كمسؤول لاشتراك Microsoft Azure، أو أنت على اتصال بمسؤول الاشتراك الذي يمكنه مساعدتك إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="448b3-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="448b3-123">يتوفر لديك معرف مستأجر Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="448b3-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="448b3-124">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كـ مجموعة مسؤولي نظام التجارة الإلكترونية ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="448b3-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="448b3-125">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كمجموعة المشرفين على التقييمات والمراجعات ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="448b3-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="448b3-126">(يمكن أن تكون مجموعة الأمان هذه هي نفس مجموعة مسؤولي نظام التجارة الإلكترونية.)</span><span class="sxs-lookup"><span data-stu-id="448b3-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="448b3-127">لاحظ أن هذه القائمة ليست شاملة.</span><span class="sxs-lookup"><span data-stu-id="448b3-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="448b3-128">في حالة مواجهة أي مشكلة، اتصل بجهة اتصال شريك Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="448b3-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="448b3-129">توفير بيئة تقييم Commerce لك</span><span class="sxs-lookup"><span data-stu-id="448b3-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="448b3-130">توضح هذه الإجراءات كيفية توفير بيئة تقييم Commerce.</span><span class="sxs-lookup"><span data-stu-id="448b3-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="448b3-131">بعد إكمالها بنجاح، ستكون بيئة تقييم Commerce جاهزة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="448b3-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="448b3-132">ويتم إجراء كافة الأنشطة الموضحة هنا في مدخل LCS.</span><span class="sxs-lookup"><span data-stu-id="448b3-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="448b3-133">إنشاء مشروع جديد</span><span class="sxs-lookup"><span data-stu-id="448b3-133">Create a new project</span></span>

<span data-ttu-id="448b3-134">لإنشاء مشروع جديد في LCS، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="448b3-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="448b3-135">في صفحة LCS الرئيسية، حدد علامة الجمع (**+**) لإنشاء مشروع.</span><span class="sxs-lookup"><span data-stu-id="448b3-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="448b3-136">في الجزء الأيسر، اتبع أحدي الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="448b3-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="448b3-137">إذا كنت شريكا، فحدد **‏‫الترحيل وإنشاء الحلول وتعلم ‬**.</span><span class="sxs-lookup"><span data-stu-id="448b3-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="448b3-138">إذا كنت عميلاً، فحدد **‏‫عمليات ما قبل البيع المتوقعة‬**.</span><span class="sxs-lookup"><span data-stu-id="448b3-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="448b3-139">أدخل الاسم والوصف والصناعة.</span><span class="sxs-lookup"><span data-stu-id="448b3-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="448b3-140">في حقل **اسم المنتج**، حدد **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="448b3-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="448b3-141">في حقل **إصدار المنتج**، حدد **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="448b3-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="448b3-142">في حقل **المنهجية**، حدد **منهجية تنفيذ Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="448b3-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="448b3-143">اختياري: يمكنك استيراد الأدوار والمستخدمين من مشروع موجود.</span><span class="sxs-lookup"><span data-stu-id="448b3-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="448b3-144">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="448b3-144">Select **Create**.</span></span> <span data-ttu-id="448b3-145">تظهر طريقة عرض المشروع.</span><span class="sxs-lookup"><span data-stu-id="448b3-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="448b3-146">إضافة موصل Azure</span><span class="sxs-lookup"><span data-stu-id="448b3-146">Add the Azure Connector</span></span>

<span data-ttu-id="448b3-147">لإضافة موصل Azure إلى مشروع LCS لديك، اتبع الخطوات الموجودة في [إكمال عملية الإلحاق في Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="448b3-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="448b3-148">نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="448b3-148">Deploy the environment</span></span>

<span data-ttu-id="448b3-149">لاستيراد البيئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="448b3-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="448b3-150">قد لا تضطر إلى إكمال الخطوات 6 و 7 و/أو 8، لأنه يتم تخطي الصفحات التي تحتوي على خيار واحد.</span><span class="sxs-lookup"><span data-stu-id="448b3-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="448b3-151">عند الوجود في طريقة عرض **معلمات البيئة**، تأكد من أن النص **Dynamics 365 Commerce - العرض التوضيحي (10.0.* x* مع تحديث النظام الأساسي *xx*)\*\* يظهر مباشرةً أعلى **اسم البيئة**.</span><span class="sxs-lookup"><span data-stu-id="448b3-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="448b3-152">للحصول على التفاصيل، راجع الرسم التوضيحي الذي يظهر بعد الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="448b3-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="448b3-153">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="448b3-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="448b3-154">حدد **إضافة** لإضافة بيئة.</span><span class="sxs-lookup"><span data-stu-id="448b3-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="448b3-155">في حقل **إصدار التطبيق**، حدد الإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="448b3-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="448b3-156">إذا كانت هناك حاجه محدده لتحديد إصدار تطبيق مختلف عن الإصدار الأحدث، فلا تقم بتحديد إصدار أقدم من **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="448b3-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="448b3-157">في الحقل **إصدار النظام الأساسي**، استخدم إصدار النظام الأساسي الذي يتم اختياره تلقائيا لإصدار التطبيق الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="448b3-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![تحديد إصدارات التطبيق والنظام الأساسي](./media/project1.png)

1. <span data-ttu-id="448b3-159">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="448b3-159">Select **Next**.</span></span>
1. <span data-ttu-id="448b3-160">حدد **العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="448b3-160">Select **Demo** as the environment topology.</span></span>

    ![تحديد مخطط البيئة 1](./media/project2.png)

1. <span data-ttu-id="448b3-162">في صفحة **بيئة النشر**، أدخل اسم بيئة.</span><span class="sxs-lookup"><span data-stu-id="448b3-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="448b3-163">اترك الإعدادات المتقدمة كما هي.</span><span class="sxs-lookup"><span data-stu-id="448b3-163">Leave the advanced settings as they are.</span></span>

    ![نشر صفحة البيئة](./media/project4.png)

1. <span data-ttu-id="448b3-165">اضبط حجم الجهاز الظاهري (VM) كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="448b3-165">Adjust the VM size as required.</span></span> <span data-ttu-id="448b3-166">(نوصي بوحدة حفظ المخزون للجهاز الظاهري (VM) \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="448b3-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="448b3-167">راجع شروط التسعير والترخيص، ثم حدد خانة الاختيار للإشارة إلى موافقتك عليها.</span><span class="sxs-lookup"><span data-stu-id="448b3-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="448b3-168">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="448b3-168">Select **Next**.</span></span>
1. <span data-ttu-id="448b3-169">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="448b3-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="448b3-170">ستعود إلى طريقة العرض **بيئات مستضافة على الشبكة السحابية** بعدها ستظهر البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="448b3-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="448b3-171">سيتم عرض البيئة المطلوبة في قائمة الانتظار ثم نشرها.</span><span class="sxs-lookup"><span data-stu-id="448b3-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="448b3-172">ستستغرق عمليات سير العمل في البيئة بعض الوقت لإكمالها.</span><span class="sxs-lookup"><span data-stu-id="448b3-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="448b3-173">ولذلك، تحقق مره أخرى بعد ما يقرب من ست إلى تسع ساعات.</span><span class="sxs-lookup"><span data-stu-id="448b3-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="448b3-174">قبل المتابعة، تأكد أن حالة البيئة هي **تم النشر**.</span><span class="sxs-lookup"><span data-stu-id="448b3-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="448b3-175">تهيئة Commerce Scale Unit (السحابة)</span><span class="sxs-lookup"><span data-stu-id="448b3-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="448b3-176">لتهيئة CSU اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="448b3-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="448b3-177">في طريقة العرض **بيئات مستضافة على الشبكة السحابية**، حدد البيئة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="448b3-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="448b3-178">حدد **كل التفاصيل** من طريقة عرض البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="448b3-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="448b3-179">ستظهر طريقة عرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="448b3-179">The environment details view appears.</span></span>
1. <span data-ttu-id="448b3-180">ضمن **ميزات البيئة**، حدد **إدارة**</span><span class="sxs-lookup"><span data-stu-id="448b3-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="448b3-181">في علامة التبويب **Commerce**، حدد **تهيئه**.</span><span class="sxs-lookup"><span data-stu-id="448b3-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="448b3-182">ستظهر طريقة عرض معلمات تهيئة CSU.</span><span class="sxs-lookup"><span data-stu-id="448b3-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="448b3-183">في حقل **المنطقة**، حدد نفس المنطقة التي وزعت بيئتك بها أو منطقة قريبة منها.</span><span class="sxs-lookup"><span data-stu-id="448b3-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="448b3-184">اترك حقل **الإصدار** كما هو.</span><span class="sxs-lookup"><span data-stu-id="448b3-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="448b3-185">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="448b3-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="448b3-186">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="448b3-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="448b3-187">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="448b3-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="448b3-188">تم وضع CSU في قائمة الانتظار لعمية التوفير.</span><span class="sxs-lookup"><span data-stu-id="448b3-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="448b3-189">قبل المتابعة، تأكد أن حالة CSU هي **نجاح**.</span><span class="sxs-lookup"><span data-stu-id="448b3-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="448b3-190">تستغرق التهيئة حوالي ساعتين إلى خمس ساعات.</span><span class="sxs-lookup"><span data-stu-id="448b3-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="448b3-191">إذا لم تتمكن من العثور على الارتباط **إدارة** في طريقه عرض تفاصيل البيئة، فاتصل بجهة اتصال Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="448b3-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="448b3-192">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="448b3-192">Initialize e-Commerce</span></span>

<span data-ttu-id="448b3-193">لتهيئة التجارة الإلكترونية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="448b3-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="448b3-194">في علامة التبويب **التجارة الإكترونية**، راجع الموافقة على التقييم، ثم حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="448b3-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="448b3-195">أدخل اسمًا في الحقل **اسم بيئة التجارة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="448b3-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="448b3-196">لاحظ أن ذلك الاسم سيكون مرئيًا في بعض عناوين URL التي تشير إلى مثيل التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="448b3-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="448b3-197">في الحقل **اسم Commerce Scale Unit‬‏‫**، حدد وحدة CSU في القائمة.</span><span class="sxs-lookup"><span data-stu-id="448b3-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="448b3-198">(يجب أن تحتوي القائمة على خيار واحد فقط).</span><span class="sxs-lookup"><span data-stu-id="448b3-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="448b3-199">يتم تعيين حقل **جغرافيا التجارة الإلكترونية** تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="448b3-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="448b3-200">للمتابعة، حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="448b3-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="448b3-201">في الحقل **أسماء الأجهزة المضيفة المدعومة**، أدخل أي مجال صالح، مثل `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="448b3-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="448b3-202">في الحقل **مجموعة أمان AAD لمسؤول النظام**، أدخل الأحرف الأولى لاسم مجموعة الأمان التي ترغب في استخدامها، ثم حدد رمز عدسة التكبير لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="448b3-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="448b3-203">حدد مجموعة الأمان الصحيحة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="448b3-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="448b3-204">في الحقل **مجموعة أمان AAD لمشروف التقييمات والمراجعات**، أدخل الأحرف الأولى لاسم مجموعة الأمان التي ترغب في استخدامها، ثم حدد رمز عدسة التكبير لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="448b3-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="448b3-205">حدد مجموعة الأمان الصحيحة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="448b3-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="448b3-206">عيِّن الخيار **تمكين خدمة التقييمات والمراجعات** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="448b3-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="448b3-207">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="448b3-207">Select **Initialize**.</span></span> <span data-ttu-id="448b3-208">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="448b3-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="448b3-209">تم بدء تشغيل تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="448b3-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="448b3-210">قبل المتابعة، انتظر حتى تصبح حالة تهيئة التجارة الإلكترونية هي **نجاح التهيئة**.</span><span class="sxs-lookup"><span data-stu-id="448b3-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="448b3-211">ضمن **الارتباطات** الواردة في الجانب السفلي الأيمن، قم بتدوين عناوين URL للارتباطات التالية:</span><span class="sxs-lookup"><span data-stu-id="448b3-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="448b3-212">**موقع التجارة الإلكترونية**  – رابط جذر موقع التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="448b3-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="448b3-213">**منشئ مواقع Commerce‬‏‫** – ارتباط أداة إدارة الموقع.</span><span class="sxs-lookup"><span data-stu-id="448b3-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="448b3-214">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="448b3-214">Next steps</span></span>

<span data-ttu-id="448b3-215">لمتابعة عملية توفير وتكوين بيئة تقييم Commerce، راجع [ تكوين بيئة تقييم Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="448b3-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="448b3-216">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="448b3-216">Additional resources</span></span>

[<span data-ttu-id="448b3-217">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="448b3-218">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="448b3-219">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="448b3-220">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="448b3-221">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="448b3-222">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="448b3-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="448b3-223">Commerce Scale Unit (السحابة)</span><span class="sxs-lookup"><span data-stu-id="448b3-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="448b3-224">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="448b3-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="448b3-225">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="448b3-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
