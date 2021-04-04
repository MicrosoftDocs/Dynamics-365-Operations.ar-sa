---
title: تقييد الوصول إلى واجهة المتجر أثناء الاختبار أو التطوير
description: يشرح هذا الموضوع كيفية تقييد الوصول إلى واجهة متجر Microsoft Dynamics 365 Commerce أثناء حدوث اختبار أو تطوير داخلي.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585181"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="9480b-103">تقييد الوصول إلى واجهة المتجر أثناء الاختبار أو التطوير</span><span class="sxs-lookup"><span data-stu-id="9480b-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9480b-104">يشرح هذا الموضوع كيفية تقييد الوصول إلى واجهة متجر Microsoft Dynamics 365 Commerce أثناء حدوث اختبار أو تطوير داخلي.</span><span class="sxs-lookup"><span data-stu-id="9480b-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="9480b-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="9480b-105">Description</span></span>

<span data-ttu-id="9480b-106">أثناء الاختبار الداخلي أو التطوير النشط، قد تحتاج إلى تقييد الوصول إلى موقعك لمنع المستخدمين الخارجيين من الوصول إلى صفحات واجهة المتجر التي تم نشرها.</span><span class="sxs-lookup"><span data-stu-id="9480b-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="9480b-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="9480b-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="9480b-108">إعداد B2C لـ Azure AD باستخدام تدفقات المستخدم القياسية</span><span class="sxs-lookup"><span data-stu-id="9480b-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="9480b-109">لمزيد من المعلومات حول كيفية تكوين B2C لـ Azure Active Directory (B2Cلـ Azure AD) لموقع التجارة الإلكترونية، راجع [إعداد مستأجر B2C في Commerce](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="9480b-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="9480b-110">تقييد وصول المستخدمين إلى صفحات واجهة المتجر وحظر إنشاء مستخدمين جدد</span><span class="sxs-lookup"><span data-stu-id="9480b-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="9480b-111">لتقييد وصول المستخدم إلى صفحات واجهة المتجر في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9480b-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9480b-112">انتقل إلى موقعك.</span><span class="sxs-lookup"><span data-stu-id="9480b-112">Go to your site.</span></span>
1. <span data-ttu-id="9480b-113">حدد **صفحات** ، ثم حدد الصفحة لتقييد صلاحية وصول المستخدم إليها.</span><span class="sxs-lookup"><span data-stu-id="9480b-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="9480b-114">حدد فتحة الوحدة النمطية أو الجزء، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9480b-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="9480b-115">في جزء الخصائص ، حدد **يتطلب تسجيل الدخول؟**، ثم حدد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="9480b-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="9480b-116">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="9480b-116">Select **Publish**.</span></span>

<span data-ttu-id="9480b-117">لحظر إنشاء مستخدمين جدد في Azure AD، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9480b-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="9480b-118">انتقل إلى [مدخل Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="9480b-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="9480b-119">حدد تطبيق B2C لـ Azure AD الذي قمت بإنشائه للوصول إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9480b-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="9480b-120">في جزء التنقل الأيسر، حدد **تدفقات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="9480b-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="9480b-121">في أعلى صفحة **تدفقات المستخدم** ، حدد **تدفق مستخدم جديد**.</span><span class="sxs-lookup"><span data-stu-id="9480b-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="9480b-122">في صفحة **تحديد نوع تدفق المستخدم**، حدد **معاينة**.</span><span class="sxs-lookup"><span data-stu-id="9480b-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="9480b-123">في منتصف الصفحة، حدد **النسخة الثانية من تسجيل الدخول**.</span><span class="sxs-lookup"><span data-stu-id="9480b-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="9480b-124">ثم اتبع الخطوات الموجودة في [إعداد مستأجر B2C في Commerce](../set-up-b2c-tenant.md) لتكوين التدفق باعتباره تدفق المستخدم القياسي للموقع لـ B2C Azure AD أثناء الاختبار أو التطوير.</span><span class="sxs-lookup"><span data-stu-id="9480b-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9480b-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9480b-125">Additional resources</span></span>

[<span data-ttu-id="9480b-126">إعداد مستأجر متاجرة عمل-مستهلك في Commerce</span><span class="sxs-lookup"><span data-stu-id="9480b-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="9480b-127">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="9480b-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
