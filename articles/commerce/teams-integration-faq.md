---
title: الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يوفر هذا الموضوع إجابات للأسئلة الشائعة حول تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
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
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019460"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="d5cee-103">الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="d5cee-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5cee-104">يوفر هذا الموضوع إجابات للأسئلة الشائعة حول تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d5cee-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="d5cee-105">من في المتجر يصبح مالكًا للفريق أثناء توفير Teams من Commerce؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="d5cee-106">تتم إضافة جميع مديري المتاجر تلقائيًا كمالكين إلى مجموعة الفريق المقابلة حتى يتمكنوا من إجراء عمليات مثل إضافة قناة خاصة وإضافة الأعضاء أو حذفهم.</span><span class="sxs-lookup"><span data-stu-id="d5cee-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="d5cee-107">كيف يمكنني تعيين دور "مدير الاتصالات" لموظف في إدارة Commerce؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="d5cee-108">يتمتع مديرو الاتصالات في Microsoft Teams بالقدرة علي إنشاء قوائم مهام ونشرها.</span><span class="sxs-lookup"><span data-stu-id="d5cee-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="d5cee-109">يجب أن يكون لموظفي المؤسسة الذين يحتاجون إلى أن يصبحوا مديري اتصالات دور "مدير مهام البيع بالتجزئة" المعين لهم في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5cee-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="d5cee-110">لتعيين دور مدير مهام البيع بالتجزئة إلى موظف في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d5cee-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d5cee-111">انتقل إلى **Retail and Commerce \> الموظفون \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="d5cee-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="d5cee-112">حدد موظفًا.</span><span class="sxs-lookup"><span data-stu-id="d5cee-112">Select an employee.</span></span>
1. <span data-ttu-id="d5cee-113">في علامة التبويب السريعة، **أدوار المستخدم** حدد **تعيين‏‎ الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="d5cee-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="d5cee-114">في مربع الحوار **تعيين أدوار للمستخدم** حدد دور **مدير مهمة البيع بالتجزئة** ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d5cee-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="d5cee-115">كيف أجعل التسلسل الهرمي لمؤسسة معينة متاحًا للتحميل في Microsoft Teams؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="d5cee-116">في إدارة Commerce، يرتبط التسلسل الهرمي لكل مؤسسة بهدف أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="d5cee-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="d5cee-117">تاكد من ان التدرج الهرمي الذي تريد توفيره في Microsoft Teams به غرض **تقارير Retail** مقترنًا به، كما هو موضح في صورة المثال التالية.</span><span class="sxs-lookup"><span data-stu-id="d5cee-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![مثال لغرض التدرج الهرمي للمؤسسات في إدارة Commerce](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="d5cee-119">كيف يمكنني تمكين عمال متجر البيع بالتجزئة من تسجيل الدخول إلى نقطة بيع Commerce (POS) باستخدام Azure Active Directory (Azure AD)؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="d5cee-120">للحصول على معلومات حول كيفية تكوين تجربة تسجيل الدخول إلى نقطة بيع Commerce لاستخدام مصادقة Azure AD، راجع [تمكين مصادقة Azure Active Directory لتسجيل الدخول إلى نقطة البيع (POS)](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="d5cee-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="d5cee-121">كيف يمكنني تعيين المتاجر والفرق المقابلة في إدارة Commerce إذا كانت مؤسستي قد أنشأت بالفعل فرقًا في Microsoft Teams؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="d5cee-122">للحصول على معلومات حول كيفية تعيين المتاجر والفرق في حالة وجود فرق موجودة مسبقًا، راجع [تعيين المتاجر والفرق المقابلة إذا كان لدى مؤسستك فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="d5cee-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="d5cee-123">كيف يمكنني مسح رمز Microsoft Graph API المميز المخزن في تخزين الجلسة؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="d5cee-124">المستخدم الذي قام بتسجيل الدخول إلى نقطة البيع (POS) باستخدام حساب Azure Active Directory (Azure AD) يجب عليه تسجيل الخروج من نقطة البيع أو إغلاق التطبيق لمسح تخزين الجلسة.</span><span class="sxs-lookup"><span data-stu-id="d5cee-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="d5cee-125">من أفضل الممارسات الموصى بها أن تجعل عمال المتجر يغلقون محطة نقاط البيع أو يسجلون الخروج من الجلسة عند عدم استخدام الوحدة الطرفية.</span><span class="sxs-lookup"><span data-stu-id="d5cee-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="d5cee-126">ماذا يحدث إذا لم يكن لدى المتجر مديرو متجر؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="d5cee-127">إذا لم يكن لدى المتجر مديرين، فلن يتم إنشاء مجموعة فريق للمتجر أو في Teams.</span><span class="sxs-lookup"><span data-stu-id="d5cee-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="d5cee-128">ماذا يحدث إذا ترك مدير المتجر الشركة؟</span><span class="sxs-lookup"><span data-stu-id="d5cee-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="d5cee-129">يمكن لأي شخص لديه دور المالك إضافة مدير متجر جديد في إدارة Commerce وإعادة توفير Teams بحيث يتمتع المدير الجديد بالامتيازات الضرورية في Teams للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="d5cee-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d5cee-130">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d5cee-130">Additional resources</span></span>

[<span data-ttu-id="d5cee-131">نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="d5cee-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="d5cee-132">تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams</span><span class="sxs-lookup"><span data-stu-id="d5cee-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="d5cee-133">توفير Microsoft Teams من Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d5cee-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="d5cee-134">مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d5cee-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="d5cee-135">إدارة أدوار المستخدمين في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d5cee-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="d5cee-136">تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d5cee-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
