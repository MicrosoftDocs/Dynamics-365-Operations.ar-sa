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
ms.openlocfilehash: b34f156642b23f7b9754dac1ee81c7d0004872d8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478178"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="b9f74-103">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="b9f74-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9f74-104">يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b9f74-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="b9f74-105">يتيح لك اكتشاف المتجر استنادًا إلى الموقع‬ في التجارة توفير محتوي الموقع ذي الصلة للعملاء ، وذلك استنادا إلى موقعهم.</span><span class="sxs-lookup"><span data-stu-id="b9f74-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="b9f74-106">عند تشغيل اكتشاف المتجر استنادًا إلى الموقع، تستخدم خدمه العرض التجاري المعلومات الخاصة بالبلد/المنطقة من عنوان IP الخاص بمستعرض الويب الخاص بالعميل لتوجيه العميل إلى تكوين الموقع الجغرافي الأفضل المتوفر.</span><span class="sxs-lookup"><span data-stu-id="b9f74-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b9f74-107">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="b9f74-107">Privacy notice</span></span>

<span data-ttu-id="b9f74-108">إذا قمت بتشغيل ميزه اكتشاف المتجر استنادًا إلى الموقع، يتم إرسال المعلومات من مستعرض العميل إلى خدمه موقع Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9f74-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="b9f74-109">وعندئذ يتم استخدام هذه المعلومات لتوفير محتوي العميل المرتبط بالموقع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="b9f74-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="b9f74-110">وتخضع المعلومات التي يتم إرسالها من مستعرض العميل والمعلومات استنادًا إلى الموقع التي يتم إرجاعها إلى العميل إلى سياسات امتثال الخصوصية وملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="b9f74-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="b9f74-111">تشغيل اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="b9f74-111">Turn on location-based store detection</span></span>

<span data-ttu-id="b9f74-112">لتشغيل اكتشاف المتجر استنادًا إلى الموقع في Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b9f74-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b9f74-113">في أداة التأليف ، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="b9f74-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="b9f74-114">في جزء التنقل على اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b9f74-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="b9f74-115">حدد **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="b9f74-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="b9f74-116">قم بتعيين خيار **تمكين اكتشاف المتجر استنادًا إلى الموقع** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="b9f74-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9f74-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b9f74-117">Additional resources</span></span>

[<span data-ttu-id="b9f74-118">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="b9f74-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b9f74-119">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="b9f74-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b9f74-120">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="b9f74-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b9f74-121">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="b9f74-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b9f74-122">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="b9f74-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b9f74-123">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="b9f74-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b9f74-124">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="b9f74-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b9f74-125">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="b9f74-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b9f74-126">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="b9f74-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b9f74-127">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="b9f74-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
