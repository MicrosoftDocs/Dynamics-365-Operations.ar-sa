---
title: توفير بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية توفير بيئة تقييم Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: e5ce2002c66a1c36d5647d3c76684b394fc1ff79
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599840"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="8cb4a-103">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8cb4a-104">يوضح هذا الموضوع كيفية توفير بيئة تقييم Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="8cb4a-105">قبل البدء، نوصي بإجراء فحص سريع من خلال هذا الموضوع للتعرف علي فكره العملية التي تتطلبها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="8cb4a-106">لا تتوفر بيئات تقييم Commerce بشكل عام، ويتم منحها للشركاء والعملاء على أساس كل طلب.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="8cb4a-107">لمزيد من المعلومات، اتصل بجهة اتصال شريك Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="8cb4a-108">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8cb4a-108">Overview</span></span>

<span data-ttu-id="8cb4a-109">لتوفير بيئة تقييم Commerce بنجاح، يجب إنشاء مشروع له اسم منتج محدد ونوع معين.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="8cb4a-110">تحتوي البيئة وCommerce Scale Unit (CSU) أيضًا على بعض المعلمات المحددة التي يجب استخدامها عند توقع توفير التجارة الإلكترونية في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="8cb4a-111">تصف الإرشادات الواردة في هذا الموضوع كافة الخطوات المطلوبة لإكمال توفيرها والمعلمات التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="8cb4a-112">بعد نجاحك في توفير بيئة تقييم Commerce، يجب إكمال بعض الخطوات التالية للتوفير لإعداد البيئة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="8cb4a-113">بعض الخطوات تكون اختيارية، بناءً على أوجه النظام التي ترغب في تقييمها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="8cb4a-114">يمكنك دائمًا إكمال الخطوات الاختيارية لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="8cb4a-115">للحصول على معلومات حول كيفية تكوين بيئة تقييم Commerce بعد توفيرها، راجع [ تكوين بيئة تقييم Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="8cb4a-116">للحصول على معلومات حول كيفية تكوين الميزات الاختيارية لبيئة تقييم Commerce، راجع [تكوين الميزات الاختيارية لبيئة تقييم Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8cb4a-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="8cb4a-117">Prerequisites</span></span>

<span data-ttu-id="8cb4a-118">يجب توفر المتطلبات الأساسية التالية قبل توفير بيئة تقييم Commerce لك:</span><span class="sxs-lookup"><span data-stu-id="8cb4a-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="8cb4a-119">يمكنك الوصول إلى مدخل Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="8cb4a-120">أنت أحد شركاء 365 Microsoft Dynamics الموجودين أو أحد العملاء ويمكنك إنشاء مشروع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="8cb4a-121">لديك حق الوصول كمسؤول لاشتراك Microsoft Azure، أو أنت على اتصال بمسؤول الاشتراك الذي يمكنه مساعدتك إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="8cb4a-122">يتوفر لديك معرف مستأجر Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="8cb4a-123">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كـ مجموعة مسؤولي نظام التجارة الإلكترونية ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="8cb4a-124">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كمجموعة المشرفين على التقييمات والمراجعات ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="8cb4a-125">(يمكن أن تكون مجموعة الأمان هذه هي نفس مجموعة مسؤولي نظام التجارة الإلكترونية.)</span><span class="sxs-lookup"><span data-stu-id="8cb4a-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="8cb4a-126">لاحظ أن هذه القائمة ليست شاملة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="8cb4a-127">في حالة مواجهة أي مشكلة، اتصل بجهة اتصال شريك Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="8cb4a-128">توفير بيئة تقييم Commerce لك</span><span class="sxs-lookup"><span data-stu-id="8cb4a-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="8cb4a-129">توضح هذه الإجراءات كيفية توفير بيئة تقييم Commerce.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="8cb4a-130">بعد إكمالها بنجاح، ستكون بيئة تقييم Commerce جاهزة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="8cb4a-131">ويتم إجراء كافة الأنشطة الموضحة هنا في مدخل LCS.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="8cb4a-132">إنشاء مشروع جديد</span><span class="sxs-lookup"><span data-stu-id="8cb4a-132">Create a new project</span></span>

<span data-ttu-id="8cb4a-133">لإنشاء مشروع جديد في LCS، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="8cb4a-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="8cb4a-134">في صفحة LCS الرئيسية، حدد علامة الجمع (**+**) لإنشاء مشروع.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="8cb4a-135">في الجزء الأيسر، اتبع أحدي الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="8cb4a-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="8cb4a-136">إذا كنت شريكا، فحدد **‏‫الترحيل وإنشاء الحلول وتعلم ‬**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="8cb4a-137">إذا كنت عميلاً، فحدد **‏‫عمليات ما قبل البيع المتوقعة‬**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="8cb4a-138">أدخل الاسم والوصف والصناعة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="8cb4a-139">في حقل **اسم المنتج**، حدد **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="8cb4a-140">في حقل **إصدار المنتج**، حدد **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="8cb4a-141">في حقل **المنهجية**، حدد **منهجية تنفيذ Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="8cb4a-142">اختياري: يمكنك استيراد الأدوار والمستخدمين من مشروع موجود.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="8cb4a-143">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-143">Select **Create**.</span></span> <span data-ttu-id="8cb4a-144">تظهر طريقة عرض المشروع.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="8cb4a-145">إضافة موصل Azure</span><span class="sxs-lookup"><span data-stu-id="8cb4a-145">Add the Azure Connector</span></span>

<span data-ttu-id="8cb4a-146">لإضافة موصل Azure إلى مشروع LCS لديك، اتبع الخطوات الموجودة في [إكمال عملية الإلحاق في Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="8cb4a-147">نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="8cb4a-147">Deploy the environment</span></span>

<span data-ttu-id="8cb4a-148">لاستيراد البيئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="8cb4a-149">قد لا تضطر إلى إكمال الخطوات 6 و 7 و/أو 8، لأنه يتم تخطي الصفحات التي تحتوي على خيار واحد.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="8cb4a-150">عند الوجود في طريقة عرض **معلمات البيئة**، تأكد من أن النص **Dynamics 365 Commerce - العرض التوضيحي (10.0.* x* مع تحديث النظام الأساسي *xx*)\*\* يظهر مباشرةً أعلى **اسم البيئة**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="8cb4a-151">للحصول على التفاصيل، راجع الرسم التوضيحي الذي يظهر بعد الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="8cb4a-152">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="8cb4a-153">حدد **إضافة** لإضافة بيئة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="8cb4a-154">في حقل **إصدار التطبيق**، حدد الإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="8cb4a-155">إذا كانت هناك حاجه محدده لتحديد إصدار تطبيق مختلف عن الإصدار الأحدث، فلا تقم بتحديد إصدار أقدم من **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="8cb4a-156">في الحقل **إصدار النظام الأساسي**، استخدم إصدار النظام الأساسي الذي يتم اختياره تلقائيا لإصدار التطبيق الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![تحديد إصدارات التطبيق والنظام الأساسي](./media/project1.png)

1. <span data-ttu-id="8cb4a-158">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-158">Select **Next**.</span></span>
1. <span data-ttu-id="8cb4a-159">حدد **العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-159">Select **Demo** as the environment topology.</span></span>

    ![تحديد مخطط البيئة 1](./media/project2.png)

1. <span data-ttu-id="8cb4a-161">في صفحة **بيئة النشر**، أدخل اسم بيئة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="8cb4a-162">اترك الإعدادات المتقدمة كما هي.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-162">Leave the advanced settings as they are.</span></span>

    ![نشر صفحة البيئة](./media/project4.png)

1. <span data-ttu-id="8cb4a-164">اضبط حجم الجهاز الظاهري (VM) كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-164">Adjust the VM size as required.</span></span> <span data-ttu-id="8cb4a-165">(نوصي بوحدة حفظ المخزون للجهاز الظاهري (VM) \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="8cb4a-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="8cb4a-166">راجع شروط التسعير والترخيص، ثم حدد خانة الاختيار للإشارة إلى موافقتك عليها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="8cb4a-167">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-167">Select **Next**.</span></span>
1. <span data-ttu-id="8cb4a-168">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="8cb4a-169">ستعود إلى طريقة العرض **بيئات مستضافة على الشبكة السحابية** بعدها ستظهر البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="8cb4a-170">سيتم عرض البيئة المطلوبة في قائمة الانتظار ثم نشرها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="8cb4a-171">ستستغرق عمليات سير العمل في البيئة بعض الوقت لإكمالها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="8cb4a-172">ولذلك، تحقق مره أخرى بعد ما يقرب من ست إلى تسع ساعات.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="8cb4a-173">قبل المتابعة، تأكد أن حالة البيئة هي **تم النشر**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="8cb4a-174">تهيئة Commerce Scale Unit (السحابة)</span><span class="sxs-lookup"><span data-stu-id="8cb4a-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="8cb4a-175">لتهيئة CSU اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="8cb4a-175">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="8cb4a-176">في طريقة العرض **بيئات مستضافة على الشبكة السحابية**، حدد البيئة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="8cb4a-177">حدد **كل التفاصيل** من طريقة عرض البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="8cb4a-178">ستظهر طريقة عرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-178">The environment details view appears.</span></span>
1. <span data-ttu-id="8cb4a-179">ضمن **ميزات البيئة**، حدد **إدارة**</span><span class="sxs-lookup"><span data-stu-id="8cb4a-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="8cb4a-180">في علامة التبويب **Commerce**، حدد **تهيئه**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="8cb4a-181">ستظهر طريقة عرض معلمات تهيئة CSU.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="8cb4a-182">في حقل **المنطقة**، حدد نفس المنطقة التي وزعت بيئتك بها أو منطقة قريبة منها.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="8cb4a-183">اترك حقل **الإصدار** كما هو.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="8cb4a-184">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="8cb4a-185">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="8cb4a-186">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="8cb4a-187">تم وضع CSU في قائمة الانتظار لعمية التوفير.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="8cb4a-188">قبل المتابعة، تأكد أن حالة CSU هي **نجاح**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="8cb4a-189">تستغرق التهيئة حوالي ساعتين إلى خمس ساعات.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="8cb4a-190">إذا لم تتمكن من العثور على الارتباط **إدارة** في طريقه عرض تفاصيل البيئة، فاتصل بجهة اتصال Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="8cb4a-191">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="8cb4a-191">Initialize e-Commerce</span></span>

<span data-ttu-id="8cb4a-192">لتهيئة التجارة الإلكترونية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="8cb4a-192">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8cb4a-193">في علامة التبويب **التجارة الإكترونية**، راجع الموافقة على التقييم، ثم حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-193">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="8cb4a-194">أدخل اسمًا في الحقل **اسم بيئة التجارة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-194">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="8cb4a-195">لاحظ أن ذلك الاسم سيكون مرئيًا في بعض عناوين URL التي تشير إلى مثيل التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-195">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="8cb4a-196">في الحقل **اسم Commerce Scale Unit‬‏‫**، حدد وحدة CSU في القائمة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-196">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="8cb4a-197">(يجب أن تحتوي القائمة على خيار واحد فقط).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-197">(The list should have only one option.)</span></span>

    <span data-ttu-id="8cb4a-198">يتم تعيين حقل **جغرافيا التجارة الإلكترونية** تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-198">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="8cb4a-199">للمتابعة، حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-199">Select **Next** to continue.</span></span>
1. <span data-ttu-id="8cb4a-200">في الحقل **أسماء الأجهزة المضيفة المدعومة**، أدخل أي مجال صالح، مثل `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-200">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="8cb4a-201">في الحقل **مجموعة أمان AAD لمسؤول النظام**، أدخل الأحرف الأولى لاسم مجموعة الأمان التي ترغب في استخدامها، ثم حدد رمز عدسة التكبير لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-201">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="8cb4a-202">حدد مجموعة الأمان الصحيحة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-202">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="8cb4a-203">في الحقل **مجموعة أمان AAD لمشروف التقييمات والمراجعات**، أدخل الأحرف الأولى لاسم مجموعة الأمان التي ترغب في استخدامها، ثم حدد رمز عدسة التكبير لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-203">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="8cb4a-204">حدد مجموعة الأمان الصحيحة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-204">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="8cb4a-205">عيِّن الخيار **تمكين خدمة التقييمات والمراجعات** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-205">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="8cb4a-206">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-206">Select **Initialize**.</span></span> <span data-ttu-id="8cb4a-207">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-207">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="8cb4a-208">تم بدء تشغيل تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-208">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="8cb4a-209">قبل المتابعة، انتظر حتى تصبح حالة تهيئة التجارة الإلكترونية هي **نجاح التهيئة**.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-209">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="8cb4a-210">ضمن **الارتباطات** الواردة في الجانب السفلي الأيمن، قم بتدوين عناوين URL للارتباطات التالية:</span><span class="sxs-lookup"><span data-stu-id="8cb4a-210">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="8cb4a-211">**موقع التجارة الإلكترونية**  – رابط جذر موقع التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-211">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="8cb4a-212">**منشئ مواقع Commerce‬‏‫** – ارتباط أداة إدارة الموقع.</span><span class="sxs-lookup"><span data-stu-id="8cb4a-212">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8cb4a-213">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="8cb4a-213">Next steps</span></span>

<span data-ttu-id="8cb4a-214">لمتابعة عملية توفير وتكوين بيئة تقييم Commerce، راجع [ تكوين بيئة تقييم Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="8cb4a-214">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cb4a-215">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8cb4a-215">Additional resources</span></span>

[<span data-ttu-id="8cb4a-216">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-216">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="8cb4a-217">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-217">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="8cb4a-218">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-218">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="8cb4a-219">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-219">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="8cb4a-220">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-220">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="8cb4a-221">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8cb4a-221">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="8cb4a-222">Commerce Scale Unit (السحابة)</span><span class="sxs-lookup"><span data-stu-id="8cb4a-222">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="8cb4a-223">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="8cb4a-223">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="8cb4a-224">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8cb4a-224">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
