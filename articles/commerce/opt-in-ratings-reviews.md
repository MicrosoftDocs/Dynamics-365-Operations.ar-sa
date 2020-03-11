---
title: الموافقة على استخدام التقييمات والمراجعات
description: يشرح هذا الموضوع كيفية الاشتراك في استخدام التقييمات والمراجعات في موقع Microsoft Dynamics 365 Commerce .
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057500"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="86c6f-103">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="86c6f-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86c6f-104">يشرح هذا الموضوع كيفية الاشتراك في استخدام التقييمات والمراجعات في موقع Microsoft Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="86c6f-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="86c6f-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="86c6f-105">Overview</span></span>

<span data-ttu-id="86c6f-106">حل التقييمات والمراجعات هو حل متعدد الاتجاهات يمكنك توفيره في Dynamics 365 Commerce باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="86c6f-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="86c6f-107">LCS هو مدخل للإدارة يستخدمه بائعو التجزئة لإدارة بيئاتهم بداية من التشغيل وحتى التفكيك.</span><span class="sxs-lookup"><span data-stu-id="86c6f-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="86c6f-108">إذا كنت ترغب في استخدام حل التصنيفات والمراجعات علي موقع ويب الخاص بالتجارة ، فيجب عليك الاشتراك في التصنيفات والمراجعات اثناء نشر موقع التجارة الكترونيه على Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86c6f-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="86c6f-109">الموافقة على استخدام التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="86c6f-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="86c6f-110">للاشتراك في استخدام التقييمات والمراجعات على موقعك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="86c6f-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="86c6f-111">اتبع الخطوات في [‏‫نشر موقع تجارة إلكترونية جديد‬](deploy-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="86c6f-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="86c6f-112">بينما تكون في LCS، انتقل إلى **‏‫إعداد نشر Retail‬ \> إعدادات أخرى**.</span><span class="sxs-lookup"><span data-stu-id="86c6f-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="86c6f-113">قم بتعيين خيار **تمكين خدمة التقييمات والمراجعات** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="86c6f-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="86c6f-114">في الحقل **مجموعه أمان AAD الخاصة بالمشرف على التقييمات والمراجعات (معرف كائن مجموعة الأمان)**، أدخل معرف مجموعة أمان Microsoft Azure Active Directory (Azure AD) التي تتضمن المشرفين على التقييمات والمراجعات.</span><span class="sxs-lookup"><span data-stu-id="86c6f-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![الموافقة على استخدام التقييمات والمراجعات](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="86c6f-116">أكمل عملية تهيئة التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="86c6f-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="86c6f-117">إذا كنت عميلا حاليًا لـ Dynamics 365 Commerceقد قام بالفعل بنشر موقع تجاره الكترونيه دون ان يتم الاشتراك في التصنيفات والمراجعات وترغب الآن في استخدام التصنيفات والمراجعات من حزمة Dynamics 365 Commerce، فالرجاء تقديم طلب خدمه.</span><span class="sxs-lookup"><span data-stu-id="86c6f-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="86c6f-118">لمزيد من المعلومات حول كيفيه تقديم طلب خدمه، راجع [عملية إرسال الطلبات](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="86c6f-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="86c6f-119">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="86c6f-119">Additional resources</span></span>

[<span data-ttu-id="86c6f-120">نظرة عامة على التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="86c6f-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="86c6f-121">إدارة التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="86c6f-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="86c6f-122">تكوين التقييمات والمراجعات</span><span class="sxs-lookup"><span data-stu-id="86c6f-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="86c6f-123">مزامنة تقييمات المنتجات في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86c6f-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


