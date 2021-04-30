---
title: توفير Microsoft Teams من Dynamics 365 Commerce
description: يصف هذا الموضوع كيفية توفير Microsoft Teams باستخدام بيانات تنظيمية من Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908894"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="20456-103">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20456-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20456-104">يصف هذا الموضوع كيفية توفير Microsoft Teams باستخدام بيانات تنظيمية من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="20456-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="20456-105">يوفر Dynamics 365 Commerce طريقه سهله لتوفير Teams إذا لم تقم بعد بإعداد فرق لمتاجر البيع بالتجزئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="20456-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="20456-106">ومن خلال الاستفادة من المعلومات التي تم تحديدها جيدا من Commerce التي ترغب في استخدامها في Teams، يمكنك مساعده موظفي المتجر علي البدء في Teams.</span><span class="sxs-lookup"><span data-stu-id="20456-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="20456-107">تتضمن هذه المعلومات التسلسل الهرمي التنظيمي وأسماء المتاجر ومعلومات الموظف وحسابات Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="20456-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="20456-108">لعمليه توفير Teams خطوتين أساسيتين:</span><span class="sxs-lookup"><span data-stu-id="20456-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="20456-109">في Teams، قم بإنشاء فريق لكل متجر للبيع بالتجزئة، وأضف عمال المتجر كاعضاء في الفريق المناسب.</span><span class="sxs-lookup"><span data-stu-id="20456-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="20456-110">إذا كان الموظف مرتبطا بأكثر من متجر للبيع بالتجزئة، ستعكس عضويه الفريق هذه الحقيقة.</span><span class="sxs-lookup"><span data-stu-id="20456-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="20456-111">سيتم إنشاء فريق الاتصالات الذي يتضمن المديرين الإقليميين كاعضاء للمساعدة في نشر المهام من Teams.</span><span class="sxs-lookup"><span data-stu-id="20456-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="20456-112">تحميل التدرج الهرمي التنظيمي من Commerce إلى Teams.</span><span class="sxs-lookup"><span data-stu-id="20456-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="20456-113">توفير Teams في إدارة Commerce</span><span class="sxs-lookup"><span data-stu-id="20456-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="20456-114">قبل توفير Microsoft Teams، قم بإكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="20456-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="20456-115">التاكد من جعل كافة المديرين الإقليميين مديري الاتصالات.</span><span class="sxs-lookup"><span data-stu-id="20456-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="20456-116">تاكد من ان حساب Azure الخاص بكل مدير متجر وعامله قد تم اقرانه بسجل العامل الخاص بالمدير أو العامل في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="20456-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="20456-117">لتوفير Teams في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="20456-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="20456-118">انتقل إلى **Retail وCommerce \> إعداد القناة \> Microsoft Teams تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="20456-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="20456-119">في جزء الإجراءات، حدد **توفير الفرق**.</span><span class="sxs-lookup"><span data-stu-id="20456-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="20456-120">يتم إنشاء مهمة المجموعة التي تسمي **توفير Teams**.</span><span class="sxs-lookup"><span data-stu-id="20456-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="20456-121">انتقل إلى **إدارة النظام \> الاستعلامات \> وظائف الدفعات**، وابحث عن الوظيفة الأحدث التي تشتمل على وصف **توفير Teams**.</span><span class="sxs-lookup"><span data-stu-id="20456-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="20456-122">انتظر حتى انتهاء تشغيل هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="20456-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="20456-123">إذا لم يكن أي من المديرين الإقليميين ومديري المتاجر وعمال المتجر مرتبطين بترخيص Teams، فقد تتلقى رسالة الخطأ التالية: "فشل استرداد فئات Sku القابلة للتطبيق للمستخدم."</span><span class="sxs-lookup"><span data-stu-id="20456-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="20456-124">لحل المشكلة، حدد **مزامنة الفرق والأعضاء** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="20456-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="20456-125">تحقق من صحة توفير Teams في مركز إدارة Teams</span><span class="sxs-lookup"><span data-stu-id="20456-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="20456-126">للتحقق من صحة توفير Microsoft Teams في مركز إدارة Microsoft Teams، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="20456-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="20456-127">انتقل إلى [مركز إدارة Teams](https://admin.teams.microsoft.com/)، وقم بتسجيل الدخول كمسؤول عن مستأجر التجارة الإلكترونية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="20456-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="20456-128">في جزء التنقل الأيمن، حدد **Teams** لتوسيعه، ثم حدد **إدارة الفرق**.</span><span class="sxs-lookup"><span data-stu-id="20456-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="20456-129">تأكد من إنشاء فريق واحد لكل متجر تجزئة لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="20456-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="20456-130">حدد فريقًا وتأكد من إضافة عمال المتجر إليه كأعضاء.</span><span class="sxs-lookup"><span data-stu-id="20456-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="20456-131">في جزء التنقل الأيمن، حدد **المستخدمين**، وتاكد من أضافه كافة الموظفين المتجر في كافة المتاجر كمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="20456-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="20456-132">يبين الرسم التوضيحي التالي مثالا على صفحة **إدارة الفرق** في مركز إدارة Teams.</span><span class="sxs-lookup"><span data-stu-id="20456-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![مثال على صفحة "إدارة الفرق" في مركز إدارة Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="20456-134">تحميل التدرج الهرمي التنظيمي من Commerce إلى Teams</span><span class="sxs-lookup"><span data-stu-id="20456-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="20456-135">يمكن استخدام التسلسل الهرمي التنظيمي لـ Commerce في Microsoft Teams لنشر المهام على جميع المتاجر أو المتاجر المحددة التي تستخدم نفس بنية التسلسل الهرمي.</span><span class="sxs-lookup"><span data-stu-id="20456-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="20456-136">لتحميل تسلسل هرمي تنظيمي لـ Commerce إلى Teams، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="20456-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="20456-137">في إدارة Commerce، انتقل إلى **Retail وCommerce \> إعداد القنوات \> تكوين تكامل Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="20456-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="20456-138">حدد **تحميل التدرج الهرمي المستهدف**، ثم حدد **متاجر البيع بالتجزئة حسب المنطقة** لتنزيل ملف قيم مفصوله بفواصل (CSV) في التدرج الهرمي التنظيمي.</span><span class="sxs-lookup"><span data-stu-id="20456-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="20456-139">قم بتثبيت وحدة Microsoft Teams PowerShell باتباع الخطوات في [تثبيت Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="20456-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="20456-140">عند مطالبتك في نافذة Teams PowerShell، قم بتسجيل الدخول باستخدام حساب المسؤول لمشتأجر Azure AD الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="20456-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="20456-141">اتبع الخطوات الواردة في [إعداد التدرج الهرمي لاستهداف فريقك](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) لتحميل ملف CSV لتدرج هرمي الاستهداف.</span><span class="sxs-lookup"><span data-stu-id="20456-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="20456-142">التحقق من تحميل التدرج الهرمي التنظيمي إلى Teams</span><span class="sxs-lookup"><span data-stu-id="20456-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="20456-143">للتحقق من تحميل التدرج الهرمي التنظيمي إلى Microsoft Teams، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="20456-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="20456-144">قم بتسجيل الدخول إلى Teams كمدير اتصالات.</span><span class="sxs-lookup"><span data-stu-id="20456-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="20456-145">في جزء التنقل الأيمن، حدد **المهام حسب Planner**</span><span class="sxs-lookup"><span data-stu-id="20456-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="20456-146">في علامة التبويب **القوائم المنشورة**، قم بإنشاء قائمه جديده تحتوي علي مهمة وهميه.</span><span class="sxs-lookup"><span data-stu-id="20456-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="20456-147">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="20456-147">Select **Publish**.</span></span> <span data-ttu-id="20456-148">يجب ان يظهر التدرج الهرمي التنظيمي في مربع الحوار **تحديد الأشخاص الذين سيتم النشر اليهم**، كما هو موضح في المثال الموجود في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="20456-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![مثال على التسلسل الهرمي التنظيمي في مربع الحوار تحديد من تريد النشر إليه](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="20456-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="20456-150">Additional resources</span></span>

[<span data-ttu-id="20456-151">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="20456-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="20456-152">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="20456-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="20456-153">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="20456-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="20456-154">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="20456-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="20456-155">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="20456-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="20456-156">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="20456-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
