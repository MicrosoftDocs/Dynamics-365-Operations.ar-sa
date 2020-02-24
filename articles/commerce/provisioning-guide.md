---
title: توفير بيئة معاينة Dynamics 365 Commerce
description: يشرح هذا الموضوع كيفية توفير بيئة معاينة Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024626"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="88b33-103">توفير بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="88b33-104">يشرح هذا الموضوع كيفية توفير بيئة معاينة Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="88b33-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="88b33-105">قبل البدء، نوصي باجراء فحص سريع من خلال هذا الموضوع للتعرف علي فكره العملية التي تتطلبها.</span><span class="sxs-lookup"><span data-stu-id="88b33-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="88b33-106">إذا لم يتم منحك إلى الآن حق الوصول إلى معاينة Dynamics 365 Commerce فيمكنك طلب الوصول إلى المعاينة من موقع ويب [Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="88b33-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="88b33-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="88b33-107">Overview</span></span>

<span data-ttu-id="88b33-108">لتوفير بيئة معاينة Commerce بنجاح، يجب عليك إنشاء مشروع له اسم منتج محدد ونوع معين.</span><span class="sxs-lookup"><span data-stu-id="88b33-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="88b33-109">لدي البيئة وcommerce scale unit (CSU) بعض المعلمات المحددة التي يتعين عليك استخدامها لتوفير التجارة الإلكترونية في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="88b33-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="88b33-110">تصف الإرشادات الواردة في هذا الموضوع كافة الخطوات المطلوبة التي يجب عليك إكمال توفيرها والمعلمات التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="88b33-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="88b33-111">بعد نجاحك في توفير بيئة معاينة Commerce، يجب عليك إكمال بعض الخطوات التالية للتوفير التي يجب اتخاذها لإعداد البيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="88b33-112">بعض الخطوات تكون اختيارية، بناءً على أوجه النظام التي ترغب في تقييمها.</span><span class="sxs-lookup"><span data-stu-id="88b33-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="88b33-113">يمكنك دائمًا إكمال الخطوات الاختيارية لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="88b33-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="88b33-114">للحصول علي معلومات حول كيفية تكوين بيئة معاينة Commerce بعد توفيرها، راجع [ تكوين بيئة معاينة Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="88b33-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="88b33-115">للحصول علي معلومات حول كيفية تكوين الميزات الاختيارية لبيئة معاينة Commerce، راجع [تكوين الميزات الاختيارية لبيئة معاينة Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="88b33-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="88b33-116">إذا كان لديك أية أسئلة تتعلق بخطوات التوفير أو كنت تواجه أية مشكلات، يرجى إعلام Microsoft على [مجموعة Microsoft Dynamics 365 Commerce Preview Yammer](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="88b33-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="88b33-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="88b33-117">Prerequisites</span></span>

<span data-ttu-id="88b33-118">يجب تتوفر المتطلبات الأساسية التالية قبل توفير بيئة معاينة Commerce الخاصة بك:</span><span class="sxs-lookup"><span data-stu-id="88b33-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="88b33-119">يمكنك الوصول إلى مدخل Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="88b33-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="88b33-120">أنت أحد شركاء 365 Microsoft Dynamics الموجودين أو أحد العملاء ويمكنك إنشاء مشروع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="88b33-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="88b33-121">لقد تم قبولك في برنامج Dynamics 365 Commerce Preview.</span><span class="sxs-lookup"><span data-stu-id="88b33-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="88b33-122">لديك الأذونات المطلوبة لإنشاء مشروع لـ‏ **الترحيل وإنشاء الحلول والتعلم**.</span><span class="sxs-lookup"><span data-stu-id="88b33-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="88b33-123">أنت عضو في **‏‫مدير البيئة‬** أو دور **مالك المشروع** في المشروع الذي ستوفر فيه البيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="88b33-124">لديك حق وصول المسؤول إلى اشتراك Microsoft Azure الخاص بك، أو اتصل بمسؤول الاشتراك والذي يمكنه إكمال الخطوتين اللتين تتطلبان أذونات المسؤول نيابة عنك.</span><span class="sxs-lookup"><span data-stu-id="88b33-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="88b33-125">يتوفر لديك معرف مستأجر Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="88b33-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="88b33-126">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كـ مجموعة مسؤولي نظام التجارة الإلكترونية ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="88b33-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="88b33-127">لقد قمت بإنشاء مجموعة أمان Azure AD لاستخدامها كمجموعة المشرفين على التقييمات والمراجعات ويتوفر لديك معرف لها.</span><span class="sxs-lookup"><span data-stu-id="88b33-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="88b33-128">(يمكن أن تكون مجموعة الأمان هذه هي نفس مجموعة مسؤولي نظام التجارة الإلكترونية.)</span><span class="sxs-lookup"><span data-stu-id="88b33-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="88b33-129">توفير بيئة معاينة Commerce الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="88b33-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="88b33-130">توضح هذه الإجراءات كيفية توفير بيئة معاينة Commerce.</span><span class="sxs-lookup"><span data-stu-id="88b33-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="88b33-131">بعد إكمالها بنجاح، ستكون بيئة معاينة Commerce جاهزة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="88b33-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="88b33-132">ويتم إجراء كافة الأنشطة الموضحة هنا في مدخل LCS.</span><span class="sxs-lookup"><span data-stu-id="88b33-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88b33-133">يتم ربط الوصول إلى المعاينة إلى حساب LCS والمؤسسة التي قمت بتحديدها في تطبيق معاينة Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="88b33-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="88b33-134">يجب استخدام نفس الحساب لتوفير بيئة معاينة Commerce.</span><span class="sxs-lookup"><span data-stu-id="88b33-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="88b33-135">إذا كان يتعين عليك استخدام حساب LCS مختلف أو مستاجر لبيئة معاينة Commerce، يجب تقديم هذه التفاصيل إلى Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88b33-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="88b33-136">للحصول على معلومات جهة الاتصال، راجع قسم [دعم بيئة معاينة Commerce](#commerce-preview-environment-support) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="88b33-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="88b33-137">التأكد من توفير ميزات المعاينة وتمكينها في LCS</span><span class="sxs-lookup"><span data-stu-id="88b33-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="88b33-138">للتأكد من توفير ميزات المعاينة وتمكينها في LCS، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="88b33-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="88b33-139">قم بتسجيل الدخول إلى [بوابة LCS](https://lcs.dynamics.com) باستخدام نفس حساب LCS الذي استخدمته لطلب الوصول إلى المعاينة.</span><span class="sxs-lookup"><span data-stu-id="88b33-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="88b33-140">في صفحة LCS الرئيسية، قم بالتمرير أقصى اليمين ثم انقر فوق اللوحة **‏‫إدارة ميزات المعاينة‬**.</span><span class="sxs-lookup"><span data-stu-id="88b33-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![لوحة إدارة المعاينة](./media/preview1.png)

1. <span data-ttu-id="88b33-142">قم بالتمرير لأسفل إلى **ميزات المعاينة الخاصة** وتأكد من توفر الميزات التالية وتمكينها:</span><span class="sxs-lookup"><span data-stu-id="88b33-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="88b33-143">تقييم التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="88b33-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="88b33-144">بيئات برنامج Commerce Preview</span><span class="sxs-lookup"><span data-stu-id="88b33-144">Commerce Preview Program Environments</span></span>

    ![ميزات المعاينة الخاصة](./media/preview2.png)

1. <span data-ttu-id="88b33-146">إذا لم تظهر هذه الميزات في القائمة، فاتصل بـ Microsoft ، وقم بتوفير عنوان البريد الكتروني للعمل وحساب LCS وتفاصيل المستأجر.</span><span class="sxs-lookup"><span data-stu-id="88b33-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="88b33-147">للحصول على معلومات جهة الاتصال، راجع قسم [دعم بيئة معاينة Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="88b33-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="88b33-148">إنشاء مشروع جديد</span><span class="sxs-lookup"><span data-stu-id="88b33-148">Create a new project</span></span>

<span data-ttu-id="88b33-149">لإنشاء مشروع جديد في LCS، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="88b33-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="88b33-150">في صفحة LCS الرئيسية، حدد علامة الجمع (**+**) لإنشاء مشروع.</span><span class="sxs-lookup"><span data-stu-id="88b33-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="88b33-151">في الجزء الأيسر، اتبع أحدي الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="88b33-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="88b33-152">إذا كنت شريكا، فحدد **‏‫الترحيل وإنشاء الحلول وتعلم ‬**.</span><span class="sxs-lookup"><span data-stu-id="88b33-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="88b33-153">إذا كنت عميلاً، فحدد **‏‫عمليات ما قبل البيع المتوقعة‬**.</span><span class="sxs-lookup"><span data-stu-id="88b33-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="88b33-154">أدخل الاسم والوصف والصناعة.</span><span class="sxs-lookup"><span data-stu-id="88b33-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="88b33-155">في حقل **اسم المنتج**، حدد **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="88b33-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="88b33-156">في حقل **إصدار المنتج**، حدد **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="88b33-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="88b33-157">في حقل **المنهجية**، حدد **منهجية تنفيذ Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="88b33-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="88b33-158">اختياري: يمكنك استيراد الأدوار والمستخدمين من مشروع موجود.</span><span class="sxs-lookup"><span data-stu-id="88b33-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="88b33-159">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="88b33-159">Select **Create**.</span></span> <span data-ttu-id="88b33-160">تظهر طريقة عرض المشروع.</span><span class="sxs-lookup"><span data-stu-id="88b33-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="88b33-161">إضافة موصل Azure</span><span class="sxs-lookup"><span data-stu-id="88b33-161">Add the Azure Connector</span></span>

<span data-ttu-id="88b33-162">لإضافة موصل Azure إلى مشروع LCS، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="88b33-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="88b33-163">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="88b33-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="88b33-164">إذا كنت شريكًا، فحدد اللوحة **إعدادات المشروع** في أقصي اليمين.</span><span class="sxs-lookup"><span data-stu-id="88b33-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="88b33-165">إذا كنت عميلاً، فاختر **إعدادات المشروع** من القائمة العليا.</span><span class="sxs-lookup"><span data-stu-id="88b33-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="88b33-166">حدد **موصل‬ات Azure**.</span><span class="sxs-lookup"><span data-stu-id="88b33-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="88b33-167">حدد **+ إضافة** لإضافة موصل Azure.</span><span class="sxs-lookup"><span data-stu-id="88b33-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="88b33-168">أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="88b33-168">Enter a name.</span></span>
1. <span data-ttu-id="88b33-169">أدخل معرف اشتراك Azure الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="88b33-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="88b33-170">قم بتشغيل خيار **التكوين لاستخدام مدير موارد Azure ‏(ARM)**.</span><span class="sxs-lookup"><span data-stu-id="88b33-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="88b33-171">تحقق من أن قيمة **‏‫مجال مستأجر AAD لاشتراك Azure (أو المعرف)‬** صحيحة.</span><span class="sxs-lookup"><span data-stu-id="88b33-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="88b33-172">راجع مسؤول الاشتراك في Azure، عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="88b33-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="88b33-173">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="88b33-173">Select **Next**.</span></span>
1. <span data-ttu-id="88b33-174">اتبع الإرشادات على الصفحة لمنح التطبيقات المطلوب حق الوصول إلى الاشتراك الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="88b33-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="88b33-175">راجع مسؤول الاشتراك في Azure، عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="88b33-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="88b33-176">سجل الدخول إلى [مدخل Azure ](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="88b33-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="88b33-177">تأكد من تحديد الدليل الصحيح، ثم من القائمة على اليسار ، حدد **الاشتراكات**.</span><span class="sxs-lookup"><span data-stu-id="88b33-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="88b33-178">اعثر على موقع الاشتراك الصحيح من القائمة وحدده.</span><span class="sxs-lookup"><span data-stu-id="88b33-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="88b33-179">استخدم وظيفة البحث كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="88b33-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="88b33-180">في القائمة، حدد **التحكم في الوصول (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="88b33-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="88b33-181">حدد**إضافة** أسفل **إضافة تعيين دور** على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="88b33-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="88b33-182">يظهر جزء **إضافة تعيين دور**.</span><span class="sxs-lookup"><span data-stu-id="88b33-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="88b33-183">في حقل **الدور**، حدد **المساهم**.</span><span class="sxs-lookup"><span data-stu-id="88b33-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="88b33-184">في حقل **تعيين حق الوصول إلى**، اترك القيمة الافتراضية، أو مستخدم **Azure AD أو المجموعة أو كيان الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="88b33-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="88b33-185">ضمن **تحديد**، أدخل **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="88b33-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="88b33-186">حدد **خدمات نشر Dynamics \[تمكين wsfed\]** من القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="88b33-187">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="88b33-187">Select **Save**.</span></span>

1. <span data-ttu-id="88b33-188">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="88b33-188">Select **Next**.</span></span>
1. <span data-ttu-id="88b33-189">اتبع الإرشادات على الصفحة لمنح التطبيقات المطلوب حق الوصول إلى الاشتراك الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="88b33-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="88b33-190">راجع مسؤول الاشتراك في Azure، عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="88b33-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="88b33-191">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="88b33-191">Select **Next**.</span></span>
1. <span data-ttu-id="88b33-192">في حقل **منطقة Azure**، اختر إما **‏‫شرق الولايات المتحدة‬**، أو **‏‫شرق الولايات المتحدة‬ 2**، أو **‏‫غرب الولايات المتحدة‬** أو **‏‫غرب الولايات المتحدة‬ 2**.</span><span class="sxs-lookup"><span data-stu-id="88b33-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="88b33-193">حدد **اتصال**.</span><span class="sxs-lookup"><span data-stu-id="88b33-193">Select **Connect**.</span></span> <span data-ttu-id="88b33-194">يجب أن يظهر موصل Azure الخاص بك في القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="88b33-195">استيراد ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫‬‏‫</span><span class="sxs-lookup"><span data-stu-id="88b33-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="88b33-196">لاستيراد "ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫‬‏‫" في المشروع اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="88b33-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="88b33-197">افتح الصفحة الرئيسية للمشروع الخاص بك عن طريق تحديد اسم المشروع في الأعلى.</span><span class="sxs-lookup"><span data-stu-id="88b33-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="88b33-198">اتبع إحدى الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="88b33-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="88b33-199">إذا كنت شريكًا، فحدد اللوحة **مكتبة الأصول** في أقصي اليمين.</span><span class="sxs-lookup"><span data-stu-id="88b33-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="88b33-200">إذا كنت عميلاً، فاختر **مكتبة الأصول** من القائمة العليا.</span><span class="sxs-lookup"><span data-stu-id="88b33-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="88b33-201">حدد **‏‫حزمة قابلة للنشر للبرنامج‬** من القائمة الموجودة على اليسار.</span><span class="sxs-lookup"><span data-stu-id="88b33-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="88b33-202">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="88b33-202">Select **Import**.</span></span>
1. <span data-ttu-id="88b33-203">حدد **ملحق قاعدة العرض التوضيحي لمعاينة Commerce** من قائمة الأصول أسفل **‏‫مكتبة الأصول المشتركة‬**.</span><span class="sxs-lookup"><span data-stu-id="88b33-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="88b33-204">حدد **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="88b33-204">Select **Pick**.</span></span> <span data-ttu-id="88b33-205">سيتم إرجاعك إلى مكتبه الأصول وستشاهد الملحق في القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="88b33-206">يبين الرسم التوضيحي التالي الإجراءات التي يجب اتخاذها في صفحة **مكتبة الأصول** لـ LCS.</span><span class="sxs-lookup"><span data-stu-id="88b33-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![استيراد ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫‬‏‫](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="88b33-208">نشر البيئة</span><span class="sxs-lookup"><span data-stu-id="88b33-208">Deploy the environment</span></span>

<span data-ttu-id="88b33-209">لاستيراد البيئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="88b33-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="88b33-210">قد لا تضطر إلى إكمال الخطوات 6 و 7 و/أو 8 ، لأنه يتم تخطي الصفحات التي تحتوي على خيار واحد.</span><span class="sxs-lookup"><span data-stu-id="88b33-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="88b33-211">عند الوجود في طريقة عرض **معلمات البيئة**، تأكد من أن النص **Dynamics 365 Commerce - العرض التوضيحي (10.0.* x* مع تحديث النظام الأساسي *xx*)\*\* يظهر مباشرةً أعلى **اسم البيئة**.</span><span class="sxs-lookup"><span data-stu-id="88b33-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="88b33-212">للحصول على التفاصيل، راجع الرسم التوضيحي الذي يظهر بعد الخطوة 8.</span><span class="sxs-lookup"><span data-stu-id="88b33-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="88b33-213">في القائمة العلوية، حدد **البيئات المستضافة على السحابة**.</span><span class="sxs-lookup"><span data-stu-id="88b33-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="88b33-214">حدد **إضافة** لإضافة بيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="88b33-215">في حقل **إصدار التطبيق**، حدد الإصدار الأحدث.</span><span class="sxs-lookup"><span data-stu-id="88b33-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="88b33-216">إذا كانت هناك حاجه محدده لتحديد إصدار تطبيق مختلف عن الإصدار الأحدث، فلا تقم بتحديد إصدار أقدم من **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="88b33-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="88b33-217">في الحقل **إصدار النظام الأساسي**، استخدم إصدار النظام الأساسي الذي يتم اختياره تلقائيا لإصدار التطبيق الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="88b33-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![تحديد إصدارات التطبيق والنظام الأساسي](./media/project1.png)

1. <span data-ttu-id="88b33-219">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="88b33-219">Select **Next**.</span></span>
1. <span data-ttu-id="88b33-220">حدد **العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-220">Select **Demo** as the environment topology.</span></span>

    ![تحديد مخطط البيئة 1](./media/project2.png)

1. <span data-ttu-id="88b33-222">حدد **Dynamics 365 Commerce - العرض التوضيحي** كمخطط البيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="88b33-223">إذا قمت بتكوين موصل Azure سابقًا، فسيتم استخدامه لهذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="88b33-224">إذا قمت بتكوين موصلات Azure متعددة، يمكنك تحديد الموصل المراد استخدامه: **‏‫شرق الولايات المتحدة‬** أو **‏‫شرق الولايات المتحدة‬ 2** أو **‏‫غرب الولايات المتحدة‬** أو **غرب الولايات المتحدة‬ 2**.</span><span class="sxs-lookup"><span data-stu-id="88b33-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="88b33-225">(للحصول علي أفضل أداء، ننصحك باختيار **غرب الولايات المتحدة‬ 2**.)</span><span class="sxs-lookup"><span data-stu-id="88b33-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![تحديد مخطط البيئة 2](./media/project3.png)

1. <span data-ttu-id="88b33-227">في صفحة **بيئة النشر**، أدخل اسم بيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="88b33-228">اترك الإعدادات المتقدمة كما هي.</span><span class="sxs-lookup"><span data-stu-id="88b33-228">Leave the advanced settings as they are.</span></span>

    ![نشر صفحة البيئة](./media/project4.png)

1. <span data-ttu-id="88b33-230">اضبط حجم الجهاز الظاهري (VM) كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="88b33-230">Adjust the VM size as required.</span></span> <span data-ttu-id="88b33-231">(نوصي بوحدة حفظ المخزون للجهاز الظاهري (VM) \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="88b33-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="88b33-232">راجع شروط التسعير والترخيص، ثم حدد خانة الاختيار للإشارة إلى موافقتك عليها.</span><span class="sxs-lookup"><span data-stu-id="88b33-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="88b33-233">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="88b33-233">Select **Next**.</span></span>
1. <span data-ttu-id="88b33-234">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="88b33-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="88b33-235">ستعود إلى طريقة العرض **بيئات مستضافة على الشبكة السحابية** بعدها ستظهر البيئة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="88b33-236">سيتم عرض البيئة المطلوبة في قائمة الانتظار ثم نشرها.</span><span class="sxs-lookup"><span data-stu-id="88b33-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="88b33-237">ستستغرق عمليات سير العمل في البيئة بعض الوقت لإكمالها.</span><span class="sxs-lookup"><span data-stu-id="88b33-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="88b33-238">ولذلك، تحقق مره أخرى بعد ما يقرب من ست إلى تسع ساعات.</span><span class="sxs-lookup"><span data-stu-id="88b33-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="88b33-239">قبل المتابعة، تأكد أن حالة البيئة هي **تم النشر**.</span><span class="sxs-lookup"><span data-stu-id="88b33-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="88b33-240">تهيئه commerce scale unit (CSU)</span><span class="sxs-lookup"><span data-stu-id="88b33-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="88b33-241">لتهيئة CSU اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="88b33-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="88b33-242">في طريقة العرض **بيئات مستضافة على الشبكة السحابية**، حدد البيئة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="88b33-243">حدد **كل التفاصيل** من طريقة عرض البيئة الموجودة على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="88b33-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="88b33-244">ستظهر طريقة عرض تفاصيل البيئة.</span><span class="sxs-lookup"><span data-stu-id="88b33-244">The environment details view appears.</span></span>
1. <span data-ttu-id="88b33-245">ضمن **ميزات البيئة**، حدد **إدارة**</span><span class="sxs-lookup"><span data-stu-id="88b33-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="88b33-246">في علامة التبويب **Commerce**، حدد **تهيئه**.</span><span class="sxs-lookup"><span data-stu-id="88b33-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="88b33-247">ستظهر طريقة عرض معلمات تهيئة CSU.</span><span class="sxs-lookup"><span data-stu-id="88b33-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="88b33-248">في حقل **المنطقة**، اختر إما **‏‫شرق الولايات المتحدة‬**، أو **‏‫شرق الولايات المتحدة‬ 2**، أو **‏‫غرب الولايات المتحدة‬** أو **‏‫غرب الولايات المتحدة‬ 2**.</span><span class="sxs-lookup"><span data-stu-id="88b33-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="88b33-249">في حقل **الإصدار** ، حدد **تحديد إصدار** في القائمة، ثم حدد **9.18.20014.4** في الحقل الذي يظهر.</span><span class="sxs-lookup"><span data-stu-id="88b33-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="88b33-250">تأكد من تحديد نفس الإصدار المشار اليه هنا.</span><span class="sxs-lookup"><span data-stu-id="88b33-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="88b33-251">وإلا، سيلزمك تحديث RCSU إلى الإصدار الصحيح لاحقا.</span><span class="sxs-lookup"><span data-stu-id="88b33-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="88b33-252">قم بتشغيل خيار **تطبيق الملحق**.</span><span class="sxs-lookup"><span data-stu-id="88b33-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="88b33-253">من قائمة الملحقات، حدد **ملحق قاعدة العرض التوضيحي لمعاينة Commerce‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="88b33-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="88b33-254">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="88b33-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="88b33-255">في صفحة تأكيد النشر، تحقق من صحة التفاصيل، ثم حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="88b33-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="88b33-256">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="88b33-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="88b33-257">تم وضع CSU في قائمة الانتظار لعمية التوفير.</span><span class="sxs-lookup"><span data-stu-id="88b33-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="88b33-258">قبل المتابعة، تأكد أن حالة CSU هي **نجاح**.</span><span class="sxs-lookup"><span data-stu-id="88b33-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="88b33-259">تستغرق التهيئة حوالي ساعتين إلى خمس ساعات.</span><span class="sxs-lookup"><span data-stu-id="88b33-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="88b33-260">تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="88b33-260">Initialize e-Commerce</span></span>

<span data-ttu-id="88b33-261">لتهيئة التجارة الإلكترونية، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="88b33-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="88b33-262">في علامة التبويب **التجارة الإكترونية**، راجع موافقه المعاينة، ثم حدد **إعداد**.</span><span class="sxs-lookup"><span data-stu-id="88b33-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="88b33-263">أدخل اسما لـ **اسم مستأجر التجارة الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="88b33-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="88b33-264">ومع ذلك، لاحظ أن ذلك الاسم سيكون مرئيًا في بعض عناوين URL التي تشير إلى مثيل التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="88b33-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="88b33-265">في الحقل **اسم Commerce scale unit‬‏‫**، حدد CSU الخاص بك في القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="88b33-266">(يجب أن تحتوي القائمة على خيار واحد فقط).</span><span class="sxs-lookup"><span data-stu-id="88b33-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="88b33-267">يتم تعيين حقل **جغرافيا التجارية الإلكترونية** تلقائيًا، ولا يمكن تغيير القيمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="88b33-268">للمتابعة، حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="88b33-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="88b33-269">في الحقل **أسماء الأجهزة المضيفة المدعومة**، أدخل أي مجال صالح، مثل `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="88b33-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="88b33-270">في الحقل **مجموعة أمان AAD لمسؤول النظام‬‏‫**، أدخل الأحرف القليلة الأولى من اسم مجموعة الأمان التي تريد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="88b33-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="88b33-271">حدد رمز العدسة المكبرة لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="88b33-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="88b33-272">حدد مجموعة الأمان الصحيحة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="88b33-273">في الحقل **مجموعه أمان AAD الخاصة بالمشرف على التقييمات والمراجعات**، أدخل الأحرف القليلة الأولى من اسم مجموعة الأمان التي تريد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="88b33-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="88b33-274">حدد رمز العدسة المكبرة لعرض نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="88b33-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="88b33-275">حدد مجموعة الأمان الصحيحة من القائمة.</span><span class="sxs-lookup"><span data-stu-id="88b33-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="88b33-276">اترك خيار **تمكين خدمة التقييمات والمراجعات** ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="88b33-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="88b33-277">حدد **تهيئة**.</span><span class="sxs-lookup"><span data-stu-id="88b33-277">Select **Initialize**.</span></span> <span data-ttu-id="88b33-278">تظهر طريقة عرض **إدارة Commerce** مره أخرى، حيث يتم تحديد علامة التبويب **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="88b33-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="88b33-279">تم بدء تشغيل تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="88b33-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="88b33-280">قبل المتابعة، انتظر حتى تصبح حالة تهيئة التجارة الإلكترونية هي **نجاح التهيئة**.</span><span class="sxs-lookup"><span data-stu-id="88b33-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="88b33-281">ضمن **الارتباطات** الواردة في الجانب السفلي الأيمن، قم بتدوين عناوين URL للارتباطات التالية:</span><span class="sxs-lookup"><span data-stu-id="88b33-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="88b33-282">**موقع التجارة الإلكترونية**  – رابط جذر موقع التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="88b33-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="88b33-283">**أداة إدارة موقع التجارة الإلكترونية‬‏‫** – رابط أداة إدارة الموقع.</span><span class="sxs-lookup"><span data-stu-id="88b33-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="88b33-284">دعم بيئة معاينة Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-284">Commerce preview environment support</span></span>

<span data-ttu-id="88b33-285">في حالة مواجهة مشكلات أثناء إكمال خطوات التوفير، يُرجى زيارة، [مجموعة Microsoft Dynamics 365 Commerce Preview Yammer ](https://aka.ms/Dynamics365CommercePreviewYammer) للحصول على المساعدة.</span><span class="sxs-lookup"><span data-stu-id="88b33-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="88b33-286">إذا واجهت مشكلات عند محاولة الوصول إلى مجموعة Yammer ، يمكنك التواصل مع Microsoft عبر البريد الكتروني <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="88b33-286">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="88b33-287">لا يتم مراقبة هذا البريد الإلكتروني بنشاط.</span><span class="sxs-lookup"><span data-stu-id="88b33-287">This email address isn't actively monitored.</span></span> <span data-ttu-id="88b33-288">لذا، توقع تأخير في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="88b33-288">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="88b33-289">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="88b33-289">Next steps</span></span>

<span data-ttu-id="88b33-290">لمتابعة عملية توفير وتكوين بيئة معاينة Commerce، راجع [ تكوين بيئة معاينة Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="88b33-290">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88b33-291">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="88b33-291">Additional resources</span></span>

[<span data-ttu-id="88b33-292">نظرة عامة على بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-292">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="88b33-293">تكوين بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-293">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="88b33-294">تكوين ميزات اختيارية لبيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-294">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="88b33-295">الأسئلة الشائعة حول بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-295">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="88b33-296">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="88b33-296">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="88b33-297">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="88b33-297">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="88b33-298">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="88b33-298">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="88b33-299">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="88b33-299">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

