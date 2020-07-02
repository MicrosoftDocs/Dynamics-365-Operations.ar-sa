---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435574"
---
# <a name="create-new-users"></a><span data-ttu-id="0e416-103">إنشاء مستخدمين جدد</span><span class="sxs-lookup"><span data-stu-id="0e416-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e416-104">المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.</span><span class="sxs-lookup"><span data-stu-id="0e416-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="0e416-105">إقران مستخدم بترخيص (أنواع التراخيص الجديدة فقط)</span><span class="sxs-lookup"><span data-stu-id="0e416-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="0e416-106">بالنسبة إلى العملاء الموجودين على أحد أنواع الترخيص الجديدة التي تمت اضافتها في 2019 أكتوبر، يجب إقران المستخدمين بترخيص.</span><span class="sxs-lookup"><span data-stu-id="0e416-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="0e416-107">يُضاف المستخدمون المرتبطون بترخيص بشكل تلقائي كمستخدمي نظام ليس لديهم أي أدوار في المرة الأولى التي يقومون فيها بتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="0e416-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="0e416-108">بإمكان مسؤولي النظام [تعيين تراخيص إلى المستخدمين](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) في [مركز إدارة Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="0e416-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="0e416-109">إقران مستخدم خارجي بترخيص (أنواع التراخيص الجديدة فقط)</span><span class="sxs-lookup"><span data-stu-id="0e416-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="0e416-110">يحتاج المستخدمون الخارجيون للمستأجر الذي تم نشر البيئة فيه إلى تمثيلهم في دليل المستأجر المضيف (Azure Active Directory (Azure AD)) حتى يمكن تعيين تراخيص لهم.</span><span class="sxs-lookup"><span data-stu-id="0e416-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="0e416-111">يجب إضافة هؤلاء المستخدمين الخارجيين إلى المستأجر في Azure AD كمستخدمين ضيوف ثم تعيين التراخيص المناسبة لهم.</span><span class="sxs-lookup"><span data-stu-id="0e416-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="0e416-112">لمزيد من المعلومات، راجع [إضافة مستخدمي تعاون B2B Azure Active Directory في مدخل Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="0e416-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="0e416-113">إضافة مستخدم جديد</span><span class="sxs-lookup"><span data-stu-id="0e416-113">Add a new user</span></span>
1. <span data-ttu-id="0e416-114">انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="0e416-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="0e416-115">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0e416-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="0e416-116">في الحقل **معرف المستخدم**، أدخل معرفًا فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="0e416-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="0e416-117">يجب إدخال معرف مستخدم.</span><span class="sxs-lookup"><span data-stu-id="0e416-117">A user ID is required.</span></span>  
4. <span data-ttu-id="0e416-118">في حقل **اسم المستخدم**، أدخل اسم المستخدم‏‎.</span><span class="sxs-lookup"><span data-stu-id="0e416-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="0e416-119">في الحقل **المجال**، أدخل مجال المستخدم.</span><span class="sxs-lookup"><span data-stu-id="0e416-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="0e416-120">في الحقل‏‎ **الاسم المستعار**، أدخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="0e416-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="0e416-121">في حقل **الشركة**، حدد الشركة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0e416-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="0e416-122">في علامة التبويب السريعة **أدوار المستخدمين**، حدد **تعيين أدوار** لتعيين مستخدمين إلى أدوار الأمان</span><span class="sxs-lookup"><span data-stu-id="0e416-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="0e416-123">لمزيد من المعلومات، راجع ‏‫[تعيين مستخدمين إلى أدوار أمان‬](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0e416-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="0e416-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0e416-124">Select **OK**.</span></span>
10. <span data-ttu-id="0e416-125">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0e416-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="0e416-126">استيراد المستخدمين</span><span class="sxs-lookup"><span data-stu-id="0e416-126">Import users</span></span>
1. <span data-ttu-id="0e416-127">انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="0e416-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="0e416-128">في جزء الإجراءات، حدد **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="0e416-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="0e416-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0e416-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0e416-130">حدد **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="0e416-130">Select **Import users**.</span></span>
5. <span data-ttu-id="0e416-131">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="0e416-131">Select **Close**.</span></span>

