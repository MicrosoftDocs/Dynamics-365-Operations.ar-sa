---
title: توفير Microsoft Teams من Dynamics 365 Commerce
description: يصف هذا الموضوع كيفية توفير Microsoft Teams باستخدام بيانات تنظيمية من Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1cb28fb50bdc972d1dae6d03a45f70a2f3a63357
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022436"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="40db7-103">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="40db7-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40db7-104">يصف هذا الموضوع كيفية توفير Microsoft Teams باستخدام بيانات تنظيمية من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40db7-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="40db7-105">يوفر Dynamics 365 Commerce طريقه سهله لتوفير Teams إذا لم تقم بعد بإعداد فرق لمتاجر البيع بالتجزئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="40db7-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="40db7-106">ومن خلال الاستفادة من المعلومات التي تم تحديدها جيدا من Commerce التي ترغب في استخدامها في Teams، يمكنك مساعده موظفي المتجر علي البدء في Teams.</span><span class="sxs-lookup"><span data-stu-id="40db7-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="40db7-107">تتضمن هذه المعلومات التسلسل الهرمي التنظيمي وأسماء المتاجر ومعلومات الموظف وحسابات Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="40db7-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="40db7-108">لعمليه توفير Teams خطوتين أساسيتين:</span><span class="sxs-lookup"><span data-stu-id="40db7-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="40db7-109">في Teams، قم بإنشاء فريق لكل متجر للبيع بالتجزئة، وأضف عمال المتجر كاعضاء في الفريق المناسب.</span><span class="sxs-lookup"><span data-stu-id="40db7-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="40db7-110">إذا كان الموظف مرتبطا بأكثر من متجر للبيع بالتجزئة، ستعكس عضويه الفريق هذه الحقيقة.</span><span class="sxs-lookup"><span data-stu-id="40db7-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="40db7-111">سيتم إنشاء فريق الاتصالات الذي يتضمن المديرين الإقليميين كاعضاء للمساعدة في نشر المهام من Teams.</span><span class="sxs-lookup"><span data-stu-id="40db7-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="40db7-112">تحميل التدرج الهرمي التنظيمي من Commerce إلى Teams.</span><span class="sxs-lookup"><span data-stu-id="40db7-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="40db7-113">توفير Teams في إدارة Commerce</span><span class="sxs-lookup"><span data-stu-id="40db7-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="40db7-114">قبل توفير Microsoft Teams، قم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="40db7-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="40db7-115">التاكد من جعل كافة المديرين الإقليميين مديري الاتصالات.</span><span class="sxs-lookup"><span data-stu-id="40db7-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="40db7-116">تاكد من ان حساب Azure الخاص بكل مدير متجر وعامله قد تم اقرانه بسجل العامل الخاص بالمدير أو العامل في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="40db7-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="40db7-117">لتوفير Teams في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="40db7-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="40db7-118">انتقل إلى **Retail وCommerce \> إعداد القناة \> Microsoft Teams تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="40db7-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="40db7-119">في جزء الإجراءات، حدد **توفير الفرق**.</span><span class="sxs-lookup"><span data-stu-id="40db7-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="40db7-120">يتم إنشاء مهمة المجموعة التي تسمي **توفير Teams**.</span><span class="sxs-lookup"><span data-stu-id="40db7-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="40db7-121">انتقل إلى **إدارة النظام \> الاستعلامات \> وظائف الدفعات**، وابحث عن الوظيفة الأحدث التي تشتمل على وصف **توفير Teams**.</span><span class="sxs-lookup"><span data-stu-id="40db7-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="40db7-122">انتظر حتى انتهاء تشغيل هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="40db7-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="40db7-123">إذا لم يكن أي من المديرين الإقليميين ومديري المتاجر وعمال المتجر مرتبطين بترخيص Teams، فقد تتلقى رسالة الخطأ التالية: "فشل استرداد فئات Sku القابلة للتطبيق للمستخدم."</span><span class="sxs-lookup"><span data-stu-id="40db7-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="40db7-124">لحل المشكلة، حدد **مزامنة الفرق والأعضاء** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="40db7-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="40db7-125">تحقق من صحة توفير Teams في مركز إدارة Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="40db7-126">للتحقق من صحة توفير Microsoft Teams في مركز إدارة Microsoft Teams، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="40db7-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="40db7-127">انتقل إلى [مركز إدارة Teams](https://admin.teams.microsoft.com/)، وقم بتسجيل الدخول كمسؤول عن مستأجر التجارة الإلكترونية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="40db7-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="40db7-128">في جزء التنقل الأيمن، حدد **Teams** لتوسيعه، ثم حدد **إدارة الفرق**.</span><span class="sxs-lookup"><span data-stu-id="40db7-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="40db7-129">تأكد من إنشاء فريق واحد لكل متجر تجزئة لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="40db7-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="40db7-130">حدد فريقًا وتأكد من إضافة عمال المتجر إليه كأعضاء.</span><span class="sxs-lookup"><span data-stu-id="40db7-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="40db7-131">في جزء التنقل الأيمن، حدد **المستخدمين**، وتاكد من أضافه كافة الموظفين المتجر في كافة المتاجر كمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="40db7-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="40db7-132">يبين الرسم التوضيحي التالي مثالا على صفحة **إدارة الفرق** في مركز إدارة Teams.</span><span class="sxs-lookup"><span data-stu-id="40db7-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![مثال على صفحة "إدارة الفرق" في مركز إدارة Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="40db7-134">تحميل التدرج الهرمي التنظيمي من Commerce إلى Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="40db7-135">يمكن استخدام التسلسل الهرمي التنظيمي لـ Commerce في Microsoft Teams لنشر المهام على جميع المتاجر أو المتاجر المحددة التي تستخدم نفس بنية التسلسل الهرمي.</span><span class="sxs-lookup"><span data-stu-id="40db7-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="40db7-136">لتحميل تسلسل هرمي تنظيمي لـ Commerce إلى Teams، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="40db7-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="40db7-137">في إدارة Commerce، انتقل إلى **Retail وCommerce \> إعداد القنوات \> تكوين تكامل Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="40db7-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="40db7-138">حدد **تحميل التدرج الهرمي المستهدف**، ثم حدد **متاجر البيع بالتجزئة حسب المنطقة** لتنزيل ملف قيم مفصوله بفواصل (CSV) في التدرج الهرمي التنظيمي.</span><span class="sxs-lookup"><span data-stu-id="40db7-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="40db7-139">قم بتثبيت وحدة Microsoft Teams PowerShell باتباع الخطوات في [تثبيت Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="40db7-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="40db7-140">عند مطالبتك في نافذة Teams PowerShell، قم بتسجيل الدخول باستخدام حساب المسؤول لمشتأجر Azure AD الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="40db7-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="40db7-141">اتبع الخطوات الواردة في [إعداد التدرج الهرمي لاستهداف فريقك](/microsoftteams/set-up-your-team-hierarchy) لتحميل ملف CSV لتدرج هرمي الاستهداف.</span><span class="sxs-lookup"><span data-stu-id="40db7-141">Follow the steps in [Set up your team targeting hierarchy](/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="40db7-142">التحقق من تحميل التدرج الهرمي التنظيمي إلى Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="40db7-143">للتحقق من تحميل التدرج الهرمي التنظيمي إلى Microsoft Teams، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="40db7-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="40db7-144">قم بتسجيل الدخول إلى Teams كمدير اتصالات.</span><span class="sxs-lookup"><span data-stu-id="40db7-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="40db7-145">في جزء التنقل الأيمن، حدد **المهام حسب Planner**</span><span class="sxs-lookup"><span data-stu-id="40db7-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="40db7-146">في علامة التبويب **القوائم المنشورة**، قم بإنشاء قائمه جديده تحتوي علي مهمة وهميه.</span><span class="sxs-lookup"><span data-stu-id="40db7-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="40db7-147">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="40db7-147">Select **Publish**.</span></span> <span data-ttu-id="40db7-148">يجب ان يظهر التدرج الهرمي التنظيمي في مربع الحوار **تحديد الأشخاص الذين سيتم النشر اليهم**، كما هو موضح في المثال الموجود في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="40db7-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![مثال على التسلسل الهرمي التنظيمي في مربع الحوار تحديد من تريد النشر إليه](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="40db7-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="40db7-150">Additional resources</span></span>

[<span data-ttu-id="40db7-151">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="40db7-152">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="40db7-153">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="40db7-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="40db7-154">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="40db7-155">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="40db7-156">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="40db7-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)