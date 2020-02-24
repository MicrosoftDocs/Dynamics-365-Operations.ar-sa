---
title: إدارة المستخدمين والأدوار في التجارة الإلكترونية
description: يشرح هذا الموضوع كيفية منح المستخدمين صلاحية الوصول إلى بيئة التأليف لموقع Microsoft Dynamics 365 Commerce .
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003523"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="12374-103">إدارة المستخدمين والأدوار في التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="12374-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="12374-104">يشرح هذا الموضوع كيفية منح المستخدمين صلاحية الوصول إلى بيئة التأليف لموقع Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="12374-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="12374-105">للمساعدة في التحكم في وصول المستخدم ومنح الإذن للمستخدمين لتنفيذ مهام معينة، تستخدم بيئة تأليف المواقع مجموعات الأمان التي تقوم بإنشاءها في Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="12374-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="12374-106">تقوم أولاً بتعيين مجموعة أمان جديدة أو موجودة من Azure AD لكل دور في بيئة التأليف.</span><span class="sxs-lookup"><span data-stu-id="12374-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="12374-107">ثم قم بمنح الأذونات أو إبطالها للمستخدمين الفرديين إما بإضافة هؤلاء المستخدمين إلى مجموعة أمان مناسبة أو إزالتهم من مجموعة أمان.</span><span class="sxs-lookup"><span data-stu-id="12374-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="12374-108">نظرة عامة على الأدوار في بيئة التأليف</span><span class="sxs-lookup"><span data-stu-id="12374-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="12374-109">يدعم Dynamics 365 for Commerce بيئة التأليف الأدوار التالية.</span><span class="sxs-lookup"><span data-stu-id="12374-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="12374-110">دور</span><span class="sxs-lookup"><span data-stu-id="12374-110">Role</span></span>                 | <span data-ttu-id="12374-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="12374-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="12374-112">مسؤول نظام</span><span class="sxs-lookup"><span data-stu-id="12374-112">System Administrator</span></span> | <span data-ttu-id="12374-113">المستخدمون الذين لديهم هذا الدور يتمتعون بكافة الامتيازات لكافة الأدوات وكافة التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="12374-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="12374-114">كما يمكنهم إنشاء مواقع.</span><span class="sxs-lookup"><span data-stu-id="12374-114">They can also create sites.</span></span> |
| <span data-ttu-id="12374-115">المسؤول</span><span class="sxs-lookup"><span data-stu-id="12374-115">Administrator</span></span>   | <span data-ttu-id="12374-116">ويتمتع المستخدمون الذين لديهم هذا الدور بكافة الامتيازات لكافة الأدوات وRnR في بنية موقع محددة.</span><span class="sxs-lookup"><span data-stu-id="12374-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="12374-117">منتج ويب</span><span class="sxs-lookup"><span data-stu-id="12374-117">Web Producer</span></span>         | <span data-ttu-id="12374-118">يمكن للمستخدمين الذين لديهم هذا الدور إنشاء الصفحات والأجزاء والقوالب وتحميل الأصول وإدارتها وإثراء المنتجات والفئات.</span><span class="sxs-lookup"><span data-stu-id="12374-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="12374-119">القارئ</span><span class="sxs-lookup"><span data-stu-id="12374-119">Reader</span></span>               | <span data-ttu-id="12374-120">يمكن للمستخدمين الذين لديهم هذا الدور عرض الصفحات والقوالب والأصول والأجزاء والتخطيطات والإعدادات ولكن قد لا يمكنهم اجراء تغييرات.</span><span class="sxs-lookup"><span data-stu-id="12374-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="12374-121">وسيط RnR</span><span class="sxs-lookup"><span data-stu-id="12374-121">RnR Moderator</span></span>        | <span data-ttu-id="12374-122">المستخدمون الذين لديهم هذا الدور يمكنهم التحكم في مراجعات المنتج.</span><span class="sxs-lookup"><span data-stu-id="12374-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="12374-123">دور مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="12374-123">System Administrator role</span></span>

<span data-ttu-id="12374-124">عندما توفر Dynamics 365 Commerce في بيئة Microsoft Dynamics Lifecycle Services (LCS) ، تتم مطالبتك بتوفير مجموعة أمان لدور **مسؤول النظام**.</span><span class="sxs-lookup"><span data-stu-id="12374-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="12374-125">ومن ثم يتم تطبيق هذا الدور تلقائيًا على كافة المواقع التي تقوم بإنشائها في البيئة التي تقوم بتكوينها.</span><span class="sxs-lookup"><span data-stu-id="12374-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="12374-126">يمكن تحديث مجموعة الأمان لهذا الدور في LCS فقط.</span><span class="sxs-lookup"><span data-stu-id="12374-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="12374-127">في صفحة **إدارة الموقع** لكافة المواقع ، تظهر للقراءة فقط ولأغراض المعلومات فقط.</span><span class="sxs-lookup"><span data-stu-id="12374-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="12374-128">دور المسؤول</span><span class="sxs-lookup"><span data-stu-id="12374-128">Administrator role</span></span>

<span data-ttu-id="12374-129">عند تقوم بإنشاء موقع جديد في Commerce، تتم مطالبتك بتوفير مجموعة أمان لدور **المسؤول**.</span><span class="sxs-lookup"><span data-stu-id="12374-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="12374-130">راجع الجدول السابق في هذا الموضوع للحصول على نظرة عامة حول الأذونات التي يمنحها هذا الدور.</span><span class="sxs-lookup"><span data-stu-id="12374-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="12374-131">إضافة مجموعات الأمان أو تحديثها</span><span class="sxs-lookup"><span data-stu-id="12374-131">Add or update security groups</span></span>

<span data-ttu-id="12374-132">بعد إنشاء الموقع الخاص بك، يمكن للمستخدمين في مجموعات الأمان المرتبطة بالأدوار **مسؤول النظام** و **المسؤول**‎ دون سواهم الوصول إلى بيئة التأليف الخاصة بهذا الموقع.</span><span class="sxs-lookup"><span data-stu-id="12374-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="12374-133">لتعيين مستخدمين إلى الأدوار **‏‫منتج ويب‬** و **وسيط RnR** و **القارئ** يجب تعيين مجموعات أمان لهذه الأدوار.</span><span class="sxs-lookup"><span data-stu-id="12374-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="12374-134">لإضافة مجموعة أمان إلى أحد الأدوار أو لتحديث مجموعة أمان يتم تعيينها حاليا لأحد الأدوار ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="12374-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="12374-135">انتقل إلى الموقع الذي تريد تحديثه.</span><span class="sxs-lookup"><span data-stu-id="12374-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="12374-136">في **إدارة الموقع**، افتح صفحة **الأمان**.</span><span class="sxs-lookup"><span data-stu-id="12374-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="12374-137">حدد الدور المراد تعديله.</span><span class="sxs-lookup"><span data-stu-id="12374-137">Select the role to modify.</span></span>
1. <span data-ttu-id="12374-138">أضف مجموعات الأمان إلى الأدوار، أو أزل مجموعات الأمان من الأدوار.</span><span class="sxs-lookup"><span data-stu-id="12374-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12374-139">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="12374-139">Additional resources</span></span>

[<span data-ttu-id="12374-140">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="12374-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="12374-141">اعتبارات تحسين محرك البحث (SEO) لموقعك</span><span class="sxs-lookup"><span data-stu-id="12374-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="12374-142">إدارة سياسة أمان المحتوى (CSP)</span><span class="sxs-lookup"><span data-stu-id="12374-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
