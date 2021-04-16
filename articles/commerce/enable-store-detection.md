---
title: تمكين اكتشاف المتجر استنادًا إلى الموقع
description: يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71e523cab20281d5db7efff40b5ef4f7293a4765
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799121"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="e88b1-103">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="e88b1-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e88b1-104">يوضح هذا الموضوع كيفية تشغيل اكتشاف المتجر استنادًا إلى الموقع‬ لموقع Dynamics 365 Commerce الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e88b1-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="e88b1-105">يتيح لك اكتشاف المتجر استنادًا إلى الموقع‬ في التجارة توفير محتوي الموقع ذي الصلة للعملاء ، وذلك استنادا إلى موقعهم.</span><span class="sxs-lookup"><span data-stu-id="e88b1-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="e88b1-106">عند تشغيل اكتشاف المتجر استنادًا إلى الموقع، تستخدم خدمه العرض التجاري المعلومات الخاصة بالبلد/المنطقة من عنوان IP الخاص بمستعرض الويب الخاص بالعميل لتوجيه العميل إلى تكوين الموقع الجغرافي الأفضل المتوفر.</span><span class="sxs-lookup"><span data-stu-id="e88b1-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e88b1-107">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="e88b1-107">Privacy notice</span></span>

<span data-ttu-id="e88b1-108">إذا قمت بتشغيل ميزه اكتشاف المتجر استنادًا إلى الموقع، يتم إرسال المعلومات من مستعرض العميل إلى خدمه موقع Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e88b1-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="e88b1-109">وعندئذ يتم استخدام هذه المعلومات لتوفير محتوي العميل المرتبط بالموقع الخاص به.</span><span class="sxs-lookup"><span data-stu-id="e88b1-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="e88b1-110">وتخضع المعلومات التي يتم إرسالها من مستعرض العميل والمعلومات استنادًا إلى الموقع التي يتم إرجاعها إلى العميل إلى سياسات امتثال الخصوصية وملفات تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="e88b1-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="e88b1-111">تشغيل اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="e88b1-111">Turn on location-based store detection</span></span>

<span data-ttu-id="e88b1-112">لتشغيل اكتشاف المتجر استنادًا إلى الموقع في Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="e88b1-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e88b1-113">في أداة التأليف ، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e88b1-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="e88b1-114">في جزء التنقل على اليسار، حدد **إدارة الموقع**.</span><span class="sxs-lookup"><span data-stu-id="e88b1-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="e88b1-115">حدد **إعدادات الموقع**.</span><span class="sxs-lookup"><span data-stu-id="e88b1-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="e88b1-116">قم بتعيين خيار **تمكين اكتشاف المتجر استنادًا إلى الموقع** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="e88b1-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e88b1-117">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e88b1-117">Additional resources</span></span>

[<span data-ttu-id="e88b1-118">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="e88b1-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e88b1-119">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="e88b1-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e88b1-120">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="e88b1-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e88b1-121">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e88b1-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e88b1-122">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="e88b1-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e88b1-123">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="e88b1-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e88b1-124">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="e88b1-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e88b1-125">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="e88b1-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e88b1-126">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="e88b1-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e88b1-127">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="e88b1-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
