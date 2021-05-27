---
title: تزويد بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية توفير بيئة تقييم Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b675d4af6fb9a080f3f3a13e64b2c5b6ad4b783
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022412"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="c14db-103">تزويد بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c14db-104">يوضح هذا الموضوع كيفية توفير بيئة تقييم Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c14db-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="c14db-105">قبل البدء، نوصي بإجراء فحص سريع من خلال هذا الموضوع للتعرف علي فكره العملية التي تتطلبها.</span><span class="sxs-lookup"><span data-stu-id="c14db-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="c14db-106">لا تتوفر بيئات تقييم Commerce بشكل عام، ويتم منحها للشركاء والعملاء على أساس كل طلب.</span><span class="sxs-lookup"><span data-stu-id="c14db-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="c14db-107">لمزيد من المعلومات، اتصل بجهة اتصال شريك Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c14db-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="c14db-108">لتوفير بيئة تقييم Commerce بنجاح، يجب إنشاء مشروع له اسم منتج محدد ونوع معين.</span><span class="sxs-lookup"><span data-stu-id="c14db-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="c14db-109">تحتوي البيئة وCommerce Scale Unit (CSU) أيضًا على بعض المعلمات المحددة التي يجب استخدامها عند توقع توفير التجارة الإلكترونية في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="c14db-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="c14db-110">تصف الإرشادات الواردة في هذا الموضوع كافة الخطوات المطلوبة لإكمال توفيرها والمعلمات التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="c14db-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="c14db-111">بعد نجاحك في توفير بيئة تقييم Commerce، يجب إكمال بعض الخطوات التالية للتوفير لإعداد البيئة للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="c14db-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="c14db-112">بعض الخطوات تكون اختيارية، بناءً على أوجه النظام التي ترغب في تقييمها.</span><span class="sxs-lookup"><span data-stu-id="c14db-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="c14db-113">يمكنك دائمًا إكمال الخطوات الاختيارية لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="c14db-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="c14db-114">للحصول على معلومات حول كيفية تكوين بيئة تقييم Commerce بعد توفيرها، راجع [ تكوين بيئة تقييم Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="c14db-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="c14db-115">للحصول على معلومات حول كيفية تكوين الميزات الاختيارية لبيئة تقييم Commerce، راجع [تكوين الميزات الاختيارية لبيئة تقييم Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="c14db-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c14db-116">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="c14db-116">Prerequisites</span></span>

<span data-ttu-id="c14db-117">يجب توفر المتطلبات الأساسية التالية قبل توفير بيئة تقييم Commerce لك:</span><span class="sxs-lookup"><span data-stu-id="c14db-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="c14db-118">لقد تم ضمك إلى برنامج التقييم ولديك الآن إمكانيات بيئة التقييم.</span><span class="sxs-lookup"><span data-stu-id="c14db-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="c14db-119">يمكنك الوصول إلى مدخل Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c14db-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="c14db-120">أنت أحد شركاء 365 Microsoft Dynamics الموجودين أو أحد العملاء ويمكنك إنشاء مشروع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c14db-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="c14db-121">لديك حق الوصول كمسؤول لاشتراك Microsoft Azure، أو أنت على اتصال بمسؤول الاشتراك الذي يمكنه مساعدتك إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c14db-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="c14db-122">يتوفر لديك معرف مستأجر Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c14db-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="c14db-123">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كـ مجموعة مسؤولي نظام التجارة الإلكترونية ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="c14db-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="c14db-124">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كمجموعة المشرفين على التقييمات والمراجعات ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="c14db-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="c14db-125">(يمكن أن تكون مجموعة الأمان هذه هي نفس مجموعة مسؤولي نظام التجارة الإلكترونية.)</span><span class="sxs-lookup"><span data-stu-id="c14db-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="c14db-126">لاحظ أن هذه القائمة ليست شاملة.</span><span class="sxs-lookup"><span data-stu-id="c14db-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="c14db-127">في حالة مواجهة أي مشكلة، اتصل بجهة اتصال شريك Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="c14db-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="c14db-128">توفير بيئة تقييم Commerce لك</span><span class="sxs-lookup"><span data-stu-id="c14db-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="c14db-129">توضح هذه الإجراءات كيفية توفير بيئة تقييم Commerce.</span><span class="sxs-lookup"><span data-stu-id="c14db-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="c14db-130">بعد إكمالها بنجاح، ستكون بيئة تقييم Commerce جاهزة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="c14db-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="c14db-131">ويتم إجراء كافة الأنشطة الموضحة هنا في مدخل LCS.</span><span class="sxs-lookup"><span data-stu-id="c14db-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="c14db-132">إنشاء مشروع جديد</span><span class="sxs-lookup"><span data-stu-id="c14db-132">Create a new project</span></span>

<span data-ttu-id="c14db-133">لإنشاء مشروع جديد في LCS، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="c14db-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="c14db-134">في صفحة LCS الرئيسية، حدد علامة الجمع (**+**) لإنشاء مشروع.</span><span class="sxs-lookup"><span data-stu-id="c14db-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="c14db-135">في الجزء الأيسر، اتبع أحدي الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c14db-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="c14db-136">إذا كنت شريكا، فحدد **‏‫الترحيل وإنشاء الحلول وتعلم ‬**.</span><span class="sxs-lookup"><span data-stu-id="c14db-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="c14db-137">إذا كنت عميلاً، فحدد **‏‫عمليات ما قبل البيع المتوقعة‬**.</span><span class="sxs-lookup"><span data-stu-id="c14db-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="c14db-138">أدخل الاسم والوصف والصناعة.</span><span class="sxs-lookup"><span data-stu-id="c14db-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="c14db-139">في حقل **اسم المنتج**، حدد **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c14db-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="c14db-140">في حقل **إصدار المنتج**، حدد **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c14db-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="c14db-141">في حقل **المنهجية**، حدد **منهجية تنفيذ Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="c14db-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="c14db-142">اختياري: يمكنك استيراد الأدوار والمستخدمين من مشروع موجود.</span><span class="sxs-lookup"><span data-stu-id="c14db-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="c14db-143">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="c14db-143">Select **Create**.</span></span> <span data-ttu-id="c14db-144">تظهر طريقة عرض المشروع.</span><span class="sxs-lookup"><span data-stu-id="c14db-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="c14db-145">إضافة موصل Azure</span><span class="sxs-lookup"><span data-stu-id="c14db-145">Add the Azure Connector</span></span>

<span data-ttu-id="c14db-146">لإضافة موصل Azure إلى مشروع LCS لديك، اتبع الخطوات الموجودة في [إكمال عملية الإلحاق في Azure Resource Manager (ARM)](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span><span class="sxs-lookup"><span data-stu-id="c14db-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="c14db-147">نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="c14db-147">Deploy the environment</span></span>

<span data-ttu-id="c14db-148">لاستيراد البيئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="c14db-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="c14db-149">قد لا تضطر إلى إكمال الخطوات 6 و 7 و/أو 8، لأنه يتم تخطي الصفحات التي تحتوي على خيار واحد.</span><span class="sxs-lookup"><span data-stu-id="c14db-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="c14db-150">عند الوجود في طريقة عرض **معلمات البيئة**، تأكد من أن النص **Dynamics 365 Commerce - العرض التوضيحي (10.0.* x* مع تحديث النظام الأساسي *xx*)\*\* يظهر مباشرةً أعلى **اسم البيئة**.</span><span class="sxs-lookup"><span data-stu-id="c14db-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="c14db-151">للحصول على التفاصيل، راجع الرسم التوضيحي الذي يظهر بعد الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="c14db-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="c14db-152">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="c14db-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="c14db-153">حدد **إضافة** لإضافة بيئة.</span><span class="sxs-lookup"><span data-stu-id="c14db-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="c14db-154">في حقل **إصدار التطبيق**، حدد الإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="c14db-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="c14db-155">إذا كانت هناك حاجه محدده لتحديد إصدار تطبيق مختلف عن الإصدار الأحدث، فلا تقم بتحديد إصدار أقدم من **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="c14db-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="c14db-156">في الحقل **إصدار النظام الأساسي**، استخدم إصدار النظام الأساسي الذي يتم اختياره تلقائيا لإصدار التطبيق الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="c14db-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![تحديد إصدارات التطبيق والنظام الأساسي](./media/project1.png)

1. <span data-ttu-id="c14db-158">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="c14db-158">Select **Next**.</span></span>
1. <span data-ttu-id="c14db-159">حدد **العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="c14db-159">Select **Demo** as the environment topology.</span></span>

    ![تحديد مخطط البيئة 1](./media/project2.png)

1. <span data-ttu-id="c14db-161">في صفحة **بيئة النشر**، أدخل اسم بيئة.</span><span class="sxs-lookup"><span data-stu-id="c14db-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="c14db-162">اترك الإعدادات المتقدمة كما هي.</span><span class="sxs-lookup"><span data-stu-id="c14db-162">Leave the advanced settings as they are.</span></span>

    ![نشر صفحة البيئة](./media/project4.png)

1. <span data-ttu-id="c14db-164">اضبط حجم الجهاز الظاهري (VM) كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="c14db-164">Adjust the VM size as required.</span></span> <span data-ttu-id="c14db-165">(نوصي بوحدة حفظ المخزون للجهاز الظاهري (VM) \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="c14db-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="c14db-166">راجع شروط التسعير والترخيص، ثم حدد خانة الاختيار للإشارة إلى موافقتك عليها.</span><span class="sxs-lookup"><span data-stu-id="c14db-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="c14db-167">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="c14db-167">Select **Next**.</span></span>
1. <span data-ttu-id="c14db-168">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c14db-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="c14db-169">ستعود إلى طريقة العرض **بيئات مستضافة على الشبكة السحابية** بعدها ستظهر البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="c14db-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="c14db-170">سيتم عرض البيئة المطلوبة في قائمة الانتظار ثم نشرها.</span><span class="sxs-lookup"><span data-stu-id="c14db-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="c14db-171">ستستغرق عمليات سير العمل في البيئة بعض الوقت لإكمالها.</span><span class="sxs-lookup"><span data-stu-id="c14db-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="c14db-172">ولذلك، تحقق مره أخرى بعد ما يقرب من ست إلى تسع ساعات.</span><span class="sxs-lookup"><span data-stu-id="c14db-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="c14db-173">قبل المتابعة، تأكد أن حالة البيئة هي **تم النشر**.</span><span class="sxs-lookup"><span data-stu-id="c14db-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="c14db-174">تهيئة Commerce Scale Unit (السحابة)</span><span class="sxs-lookup"><span data-stu-id="c14db-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="c14db-175">لتهيئة CSU اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="c14db-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="c14db-176">في طريقة العرض **بيئات مستضافة على الشبكة السحابية**، حدد البيئة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="c14db-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="c14db-177">حدد **كل التفاصيل** من طريقة عرض البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="c14db-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="c14db-178">ستظهر طريقة عرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="c14db-178">The environment details view appears.</span></span>
1. <span data-ttu-id="c14db-179">ضمن **ميزات البيئة**، حدد **إدارة**</span><span class="sxs-lookup"><span data-stu-id="c14db-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="c14db-180">في علامة التبويب **Commerce**، حدد **تهيئه**.</span><span class="sxs-lookup"><span data-stu-id="c14db-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="c14db-181">ستظهر طريقة عرض معلمات تهيئة CSU.</span><span class="sxs-lookup"><span data-stu-id="c14db-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="c14db-182">في حقل **المنطقة**، حدد نفس المنطقة التي وزعت بيئتك بها أو منطقة قريبة منها.</span><span class="sxs-lookup"><span data-stu-id="c14db-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="c14db-183">اترك حقل **الإصدار** كما هو.</span><span class="sxs-lookup"><span data-stu-id="c14db-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="c14db-184">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="c14db-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="c14db-185">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c14db-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="c14db-186">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c14db-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="c14db-187">تم وضع CSU في قائمة الانتظار لعمية التوفير.</span><span class="sxs-lookup"><span data-stu-id="c14db-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="c14db-188">قبل المتابعة، تأكد أن حالة CSU هي **نجاح**.</span><span class="sxs-lookup"><span data-stu-id="c14db-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="c14db-189">تستغرق التهيئة حوالي ساعتين إلى خمس ساعات.</span><span class="sxs-lookup"><span data-stu-id="c14db-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="c14db-190">إذا لم تتمكن من العثور على الارتباط **إدارة** في طريقه عرض تفاصيل البيئة، فاتصل بجهة اتصال Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="c14db-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="c14db-191">أثناء عملية النشر، قد تتلقى رسالة الخطأ التالية:</span><span class="sxs-lookup"><span data-stu-id="c14db-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="c14db-192">تحتاج بيئات التقييم (العرض التوضيحي/الاختبار) إلى تسجيل تطبيق موصل وحدة المقياس \<application ID\> في المركز الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c14db-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="c14db-193">في حاله فشل تهيئة CSU وظهور رسالة الخطا هذه، قم بتدوين معرف التطبيق، والذي يعد معرفًا فريدًا عموميًا (GUID)، ثم اتبع الخطوات الواردة في القسم التالي لتسجيل تطبيق نشر CSU في المركز الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="c14db-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="c14db-194">تسجيل تطبيق نشر CSU في المركز الرئيسي لـ Commerce (إذا كان ذلك مطلوبًا)</span><span class="sxs-lookup"><span data-stu-id="c14db-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="c14db-195">لتسجيل تطبيق نشر CSU في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c14db-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c14db-196">في المركز الرئيسي لـ Commerce، انتقل إلى **‏‫إدارة النظام‬ \> الإعداد \> تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="c14db-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="c14db-197">في عمود **معرف العميل**، أدخل معرف التطبيق من رسالة الخطأ الخاصة بتهيئة CSU التي تلقيتها.</span><span class="sxs-lookup"><span data-stu-id="c14db-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="c14db-198">في عمود **الاسم**، أدخل أي نص وصفي (على سبيل المثال ، **CSU Eval**).</span><span class="sxs-lookup"><span data-stu-id="c14db-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="c14db-199">في عمود **معرف المستخدم**، أدخل **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="c14db-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="c14db-200">أعد محاولة تهيئة CSU والنشر من LCS.</span><span class="sxs-lookup"><span data-stu-id="c14db-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="c14db-201">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c14db-201">Initialize e-Commerce</span></span>

<span data-ttu-id="c14db-202">لتهيئة التجارة الإلكترونية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="c14db-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c14db-203">في علامة التبويب **التجارة الإكترونية**، راجع الموافقة على التقييم، ثم حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="c14db-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="c14db-204">أدخل اسمًا في الحقل **اسم بيئة التجارة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="c14db-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="c14db-205">لاحظ أن ذلك الاسم سيكون مرئيًا في بعض عناوين URL التي تشير إلى مثيل التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c14db-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="c14db-206">في الحقل **اسم Commerce Scale Unit‬‏‫**، حدد وحدة CSU في القائمة.</span><span class="sxs-lookup"><span data-stu-id="c14db-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="c14db-207">(يجب أن تحتوي القائمة على خيار واحد فقط).</span><span class="sxs-lookup"><span data-stu-id="c14db-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="c14db-208">يتم تعيين حقل **جغرافيا التجارة الإلكترونية** تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="c14db-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="c14db-209">للمتابعة، حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="c14db-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="c14db-210">في الحقل **أسماء الأجهزة المضيفة المدعومة**، أدخل أي مجال صالح، مثل `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="c14db-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="c14db-211">في الحقل **مجموعة أمان AAD لمسؤول النظام**، أدخل الأحرف الأولى لاسم مجموعة الأمان التي ترغب في استخدامها، ثم حدد رمز عدسة التكبير لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="c14db-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="c14db-212">حدد مجموعة الأمان الصحيحة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="c14db-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="c14db-213">في الحقل **مجموعة أمان AAD لمشروف التقييمات والمراجعات**، أدخل الأحرف الأولى لاسم مجموعة الأمان التي ترغب في استخدامها، ثم حدد رمز عدسة التكبير لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="c14db-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="c14db-214">حدد مجموعة الأمان الصحيحة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="c14db-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="c14db-215">عيِّن الخيار **تمكين خدمة التقييمات والمراجعات** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c14db-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="c14db-216">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="c14db-216">Select **Initialize**.</span></span> <span data-ttu-id="c14db-217">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c14db-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="c14db-218">تم بدء تشغيل تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c14db-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="c14db-219">قبل المتابعة، انتظر حتى تصبح حالة تهيئة التجارة الإلكترونية هي **نجاح التهيئة**.</span><span class="sxs-lookup"><span data-stu-id="c14db-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="c14db-220">ضمن **الارتباطات** الواردة في الجانب السفلي الأيمن، قم بتدوين عناوين URL للارتباطات التالية:</span><span class="sxs-lookup"><span data-stu-id="c14db-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="c14db-221">**موقع التجارة الإلكترونية**  – رابط جذر موقع التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c14db-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="c14db-222">**منشئ مواقع Commerce‬‏‫** – ارتباط أداة إدارة الموقع.</span><span class="sxs-lookup"><span data-stu-id="c14db-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c14db-223">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="c14db-223">Next steps</span></span>

<span data-ttu-id="c14db-224">لمتابعة عملية توفير وتكوين بيئة تقييم Commerce، راجع [ تكوين بيئة تقييم Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="c14db-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c14db-225">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c14db-225">Additional resources</span></span>

[<span data-ttu-id="c14db-226">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="c14db-227">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="c14db-228">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="c14db-229">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="c14db-230">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="c14db-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c14db-231">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="c14db-232">Commerce Scale Unit (السحابة)</span><span class="sxs-lookup"><span data-stu-id="c14db-232">Commerce Scale Unit (cloud)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="c14db-233">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="c14db-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="c14db-234">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c14db-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]