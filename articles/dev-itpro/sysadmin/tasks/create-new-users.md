---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916474"
---
# <a name="create-new-users"></a><span data-ttu-id="8509f-103">إنشاء مستخدمين جدد</span><span class="sxs-lookup"><span data-stu-id="8509f-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8509f-104">المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.</span><span class="sxs-lookup"><span data-stu-id="8509f-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="8509f-105">يستطيع المسؤولون عن النظام إكمال هذا الإجراء لإضافة مستخدمين إلى النظام.</span><span class="sxs-lookup"><span data-stu-id="8509f-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="8509f-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="8509f-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="8509f-107">إضافة مستخدم جديد</span><span class="sxs-lookup"><span data-stu-id="8509f-107">Add a new user</span></span>
1. <span data-ttu-id="8509f-108">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النظام > المستخدمون > المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="8509f-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="8509f-109">انقر فوق **جديد** في **جزء الإجراءات**.</span><span class="sxs-lookup"><span data-stu-id="8509f-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="8509f-110">في الحقل **معرف المستخدم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8509f-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="8509f-111">أدخل معرّفًا فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="8509f-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="8509f-112">يجب إدخال معرف مستخدم.</span><span class="sxs-lookup"><span data-stu-id="8509f-112">A user ID is required.</span></span>  
4. <span data-ttu-id="8509f-113">في الحقل **اسم المستخدم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8509f-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="8509f-114">أدخل اسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="8509f-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="8509f-115">في الحقل **المجال**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8509f-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="8509f-116">أدخل مجال المستخدم.</span><span class="sxs-lookup"><span data-stu-id="8509f-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="8509f-117">في الحقل **الاسم المستعار**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="8509f-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="8509f-118">أدخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="8509f-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="8509f-119">في الحقل **الشركة**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8509f-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8509f-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8509f-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="8509f-121">في القسم **أدوار المستخدم**، انقر فوق **تعيين‏‎ الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="8509f-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="8509f-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8509f-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="8509f-123">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8509f-123">Click **OK**.</span></span>
12. <span data-ttu-id="8509f-124">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8509f-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="8509f-125">استيراد المستخدمين</span><span class="sxs-lookup"><span data-stu-id="8509f-125">Import users</span></span>
1. <span data-ttu-id="8509f-126">في **جزء الإجراءات**، انقر فوق **استيراد المستخدمين‬**.</span><span class="sxs-lookup"><span data-stu-id="8509f-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="8509f-127">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8509f-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8509f-128">انقر فوق **استيراد المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="8509f-128">Click **Import users**.</span></span>
4. <span data-ttu-id="8509f-129">انقر فوق **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="8509f-129">Click **Close**.</span></span>

