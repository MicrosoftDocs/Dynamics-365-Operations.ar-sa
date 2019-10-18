---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
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
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180934"
---
# <a name="create-new-users"></a><span data-ttu-id="0318d-103">إنشاء مستخدمين جدد</span><span class="sxs-lookup"><span data-stu-id="0318d-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0318d-104">المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.</span><span class="sxs-lookup"><span data-stu-id="0318d-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="0318d-105">إقران مستخدم بترخيص (أنواع التراخيص الجديدة فقط)</span><span class="sxs-lookup"><span data-stu-id="0318d-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="0318d-106">بالنسبة إلى العملاء الموجودين على أحد أنواع الترخيص الجديدة التي تمت اضافتها في 2019 أكتوبر، يجب إقران المستخدمين بترخيص.</span><span class="sxs-lookup"><span data-stu-id="0318d-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="0318d-107">يُضاف المستخدمون المرتبطون بترخيص بشكل تلقائي كمستخدمي نظام ليس لديهم أي أدوار في المرة الأولى التي يقومون فيها بتسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="0318d-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="0318d-108">يتلقى المستخدمون الذين لا يقترنون بترخيص رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="0318d-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="0318d-109">بإمكان مسؤولي النظام [تعيين تراخيص إلى المستخدمين](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) في [مركز إدارة Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="0318d-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="0318d-110">إضافة مستخدم جديد</span><span class="sxs-lookup"><span data-stu-id="0318d-110">Add a new user</span></span>
1. <span data-ttu-id="0318d-111">انتقل إلى **إدارة النظام \> المستخدمون‏‎ \> المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="0318d-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="0318d-112">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0318d-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="0318d-113">في الحقل **معرف المستخدم**، أدخل معرفًا فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="0318d-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="0318d-114">يجب إدخال معرف مستخدم.</span><span class="sxs-lookup"><span data-stu-id="0318d-114">A user ID is required.</span></span>  
4. <span data-ttu-id="0318d-115">في حقل **اسم المستخدم**، أدخل اسم المستخدم‏‎.</span><span class="sxs-lookup"><span data-stu-id="0318d-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="0318d-116">في الحقل **المجال**، أدخل مجال المستخدم.</span><span class="sxs-lookup"><span data-stu-id="0318d-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="0318d-117">في الحقل‏‎ **الاسم المستعار**، أدخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="0318d-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="0318d-118">في حقل **الشركة**، حدد الشركة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0318d-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="0318d-119">على علامة التبويب السريعة **أدوار المستخدمين**، حدد **تعيين أدوار** من أجل [تعيين مستخدمين إلى أدوار الأمان](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="0318d-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="0318d-120">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0318d-120">Select **OK**.</span></span>
10. <span data-ttu-id="0318d-121">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0318d-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="0318d-122">استيراد المستخدمين</span><span class="sxs-lookup"><span data-stu-id="0318d-122">Import users</span></span>
1. <span data-ttu-id="0318d-123">في جزء الإجراءات، حدد **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="0318d-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="0318d-124">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0318d-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0318d-125">حدد **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="0318d-125">Select **Import users**.</span></span>
4. <span data-ttu-id="0318d-126">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="0318d-126">Select **Close**.</span></span>

