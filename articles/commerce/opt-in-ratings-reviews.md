---
title: الموافقة على استخدام التقييمات والمراجعات
description: يشرح هذا الموضوع كيفية الاشتراك في استخدام التقييمات والمراجعات في موقع Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697970"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="0dbf7-103">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="0dbf7-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0dbf7-104">يشرح هذا الموضوع كيفية الاشتراك في استخدام التقييمات والمراجعات في موقع Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="0dbf7-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="0dbf7-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="0dbf7-105">Overview</span></span>

<span data-ttu-id="0dbf7-106">حل التقييمات والمراجعات هو حل متعدد الاتجاهات يمكنك توفيره في Dynamics 365 Commerce باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0dbf7-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0dbf7-107">LCS هو مدخل للإدارة يستخدمه بائعو التجزئة لإدارة بيئاتهم بداية من التشغيل وحتى التفكيك.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="0dbf7-108">إذا كنت ترغب في استخدام حل التقييمات والمراجعات على موقع ويب Commerce، فيجب عليك الاشتراك أولاً.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="0dbf7-109">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="0dbf7-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="0dbf7-110">للاشتراك في استخدام التقييمات والمراجعات على موقعك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="0dbf7-111">اتبع الخطوات في [‏‫نشر موقع تجارة إلكترونية جديد‬](deploy-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="0dbf7-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="0dbf7-112">بينما تكون في LCS، انتقل إلى **‏‫إعداد نشر Retail‬ \> إعدادات أخرى**.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="0dbf7-113">قم بتعيين خيار **تمكين خدمة التقييمات والمراجعات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="0dbf7-114">في الحقل **مجموعه أمان AAD الخاصة بالمشرف على التقييمات والمراجعات (معرف كائن مجموعة الأمان)**، أدخل معرف مجموعة أمان Microsoft Azure Active Directory (Azure AD) التي تتضمن المشرفين على التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![الموافقة على استخدام التقييمات والمراجعات](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="0dbf7-116">أكمل عملية تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0dbf7-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0dbf7-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0dbf7-117">Additional resources</span></span>

[<span data-ttu-id="0dbf7-118">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="0dbf7-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0dbf7-119">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="0dbf7-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="0dbf7-120">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="0dbf7-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="0dbf7-121">مزامنة تقييمات المنتجات في Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="0dbf7-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
