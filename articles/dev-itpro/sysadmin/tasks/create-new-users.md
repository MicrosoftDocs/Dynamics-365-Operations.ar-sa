---
title: إنشاء مستخدمين جدد
description: المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558701"
---
# <a name="create-new-users"></a><span data-ttu-id="d422d-103">إنشاء مستخدمين جدد</span><span class="sxs-lookup"><span data-stu-id="d422d-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d422d-104">المستخدمون هم الموظفون الداخليون في مؤسستك، أو الموردون والعملاء الخارجيون، ممن يحتاجون إلى الوصول إلى النظام لإنجاز أعمالهم.</span><span class="sxs-lookup"><span data-stu-id="d422d-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="d422d-105">يستطيع المسؤولون عن النظام إكمال هذا الإجراء لإضافة مستخدمين إلى النظام.</span><span class="sxs-lookup"><span data-stu-id="d422d-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="d422d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="d422d-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="d422d-107">إضافة مستخدم جديد</span><span class="sxs-lookup"><span data-stu-id="d422d-107">Add a new user</span></span>
1. <span data-ttu-id="d422d-108">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="d422d-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="d422d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d422d-109">Click New.</span></span>
3. <span data-ttu-id="d422d-110">في الحقل "معرف المستخدم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d422d-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="d422d-111">أدخل معرّفًا فريدًا للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d422d-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="d422d-112">يجب إدخال معرف مستخدم.</span><span class="sxs-lookup"><span data-stu-id="d422d-112">A user ID is required.</span></span>  
4. <span data-ttu-id="d422d-113">في الحقل "اسم المستخدم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d422d-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="d422d-114">أدخل اسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d422d-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="d422d-115">في الحقل "المجال"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d422d-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="d422d-116">أدخل مجال المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d422d-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="d422d-117">في الحقل "الاسم المستعار"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d422d-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="d422d-118">أدخل الاسم المستعار للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="d422d-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="d422d-119">في الحقل "الشركة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d422d-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d422d-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d422d-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d422d-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d422d-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d422d-122">تحديد شركة المستخدم</span><span class="sxs-lookup"><span data-stu-id="d422d-122">Select the user's company</span></span>  
10. <span data-ttu-id="d422d-123">انقر فوق "تعيين الأدوار".</span><span class="sxs-lookup"><span data-stu-id="d422d-123">Click Assign roles.</span></span>
11. <span data-ttu-id="d422d-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d422d-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d422d-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d422d-125">Click OK.</span></span>
13. <span data-ttu-id="d422d-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d422d-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="d422d-127">استيراد المستخدمين</span><span class="sxs-lookup"><span data-stu-id="d422d-127">Import users</span></span>
1. <span data-ttu-id="d422d-128">انقر فوق "استيراد المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="d422d-128">Click Import users.</span></span>
2. <span data-ttu-id="d422d-129">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d422d-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d422d-130">انقر فوق "استيراد المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="d422d-130">Click Import users.</span></span>
4. <span data-ttu-id="d422d-131">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="d422d-131">Click Close.</span></span>

