---
title: تمكين اكتشاف المتجر استنادًا إلى الموقع
description: يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.
author: brianshook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66ffe56f9d969c9d62ed4ff49f0848fab7e58a56
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096859"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="9bc55-103">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="9bc55-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9bc55-104">يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9bc55-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="9bc55-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="9bc55-105">Overview</span></span>

<span data-ttu-id="9bc55-106">يتيح لك اكتشاف المتجر استنادًا إلى الموقع‬ في التجارة توفير محتوي الموقع ذي الصلة للعملاء ، وذلك استنادا إلى موقعهم.</span><span class="sxs-lookup"><span data-stu-id="9bc55-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="9bc55-107">عند تشغيل اكتشاف المتجر استنادًا إلى الموقع، تستخدم خدمه العرض التجاري المعلومات الخاصة بالبلد/المنطقة من عنوان IP الخاص بمستعرض الويب الخاص بالعميل لتوجيه العميل إلى تكوين الموقع الجغرافي الأفضل المتوفر.</span><span class="sxs-lookup"><span data-stu-id="9bc55-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="9bc55-108">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="9bc55-108">Privacy notice</span></span>

<span data-ttu-id="9bc55-109">إذا قمت بتشغيل ميزه اكتشاف المتجر استنادًا إلى الموقع، يتم إرسال المعلومات من مستعرض العميل إلى خدمه موقع Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9bc55-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="9bc55-110">وعندئذ يتم استخدام هذه المعلومات لتوفير محتوي العميل المرتبط بالموقع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="9bc55-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="9bc55-111">وتخضع المعلومات التي يتم إرسالها من مستعرض العميل والمعلومات استنادًا إلى الموقع التي يتم إرجاعها إلى العميل إلى سياسات امتثال الخصوصية وملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="9bc55-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="9bc55-112">تشغيل اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="9bc55-112">Turn on location-based store detection</span></span>

<span data-ttu-id="9bc55-113">لتشغيل اكتشاف المتجر استنادًا إلى الموقع في Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="9bc55-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9bc55-114">في أداة التأليف ، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9bc55-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="9bc55-115">في جزء التنقل على اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="9bc55-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="9bc55-116">حدد **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="9bc55-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="9bc55-117">قم بتعيين خيار **تمكين اكتشاف المتجر استنادًا إلى الموقع** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="9bc55-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bc55-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9bc55-118">Additional resources</span></span>

[<span data-ttu-id="9bc55-119">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="9bc55-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9bc55-120">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="9bc55-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="9bc55-121">إعداد قناة متجر عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="9bc55-121">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="9bc55-122">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="9bc55-122">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9bc55-123">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="9bc55-123">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9bc55-124">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="9bc55-124">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9bc55-125">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="9bc55-125">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9bc55-126">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="9bc55-126">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9bc55-127">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="9bc55-127">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9bc55-128">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="9bc55-128">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9bc55-129">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="9bc55-129">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
