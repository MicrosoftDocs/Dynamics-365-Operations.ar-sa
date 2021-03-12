---
title: تمكين اكتشاف المتجر استنادًا إلى الموقع
description: يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000711"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="8e609-103">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="8e609-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8e609-104">يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8e609-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="8e609-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8e609-105">Overview</span></span>

<span data-ttu-id="8e609-106">يتيح لك اكتشاف المتجر استنادًا إلى الموقع‬ في التجارة توفير محتوي الموقع ذي الصلة للعملاء ، وذلك استنادا إلى موقعهم.</span><span class="sxs-lookup"><span data-stu-id="8e609-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="8e609-107">عند تشغيل اكتشاف المتجر استنادًا إلى الموقع، تستخدم خدمه العرض التجاري المعلومات الخاصة بالبلد/المنطقة من عنوان IP الخاص بمستعرض الويب الخاص بالعميل لتوجيه العميل إلى تكوين الموقع الجغرافي الأفضل المتوفر.</span><span class="sxs-lookup"><span data-stu-id="8e609-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="8e609-108">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="8e609-108">Privacy notice</span></span>

<span data-ttu-id="8e609-109">إذا قمت بتشغيل ميزه اكتشاف المتجر استنادًا إلى الموقع، يتم إرسال المعلومات من مستعرض العميل إلى خدمه موقع Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8e609-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="8e609-110">وعندئذ يتم استخدام هذه المعلومات لتوفير محتوي العميل المرتبط بالموقع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="8e609-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="8e609-111">وتخضع المعلومات التي يتم إرسالها من مستعرض العميل والمعلومات استنادًا إلى الموقع التي يتم إرجاعها إلى العميل إلى سياسات امتثال الخصوصية وملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="8e609-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="8e609-112">تشغيل اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="8e609-112">Turn on location-based store detection</span></span>

<span data-ttu-id="8e609-113">لتشغيل اكتشاف المتجر استنادًا إلى الموقع في Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8e609-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="8e609-114">في أداة التأليف ، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8e609-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="8e609-115">في جزء التنقل على اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="8e609-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="8e609-116">حدد **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="8e609-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="8e609-117">قم بتعيين خيار **تمكين اكتشاف المتجر استنادًا إلى الموقع** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="8e609-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e609-118">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8e609-118">Additional resources</span></span>

[<span data-ttu-id="8e609-119">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="8e609-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8e609-120">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="8e609-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8e609-121">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="8e609-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8e609-122">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8e609-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8e609-123">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="8e609-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8e609-124">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="8e609-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8e609-125">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="8e609-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8e609-126">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="8e609-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8e609-127">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="8e609-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8e609-128">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="8e609-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
