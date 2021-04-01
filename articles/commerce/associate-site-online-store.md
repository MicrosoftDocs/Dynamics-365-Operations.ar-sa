---
title: إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت
description: يشرح هذا الموضوع كيفية ربط موقع Microsoft Dynamics 365 Commerce الخاص بك بواحد أو أكثر من المتاجر عبر الإنترنت.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb39b54e45e387067720dcbc5d9ccffbf8bf08b4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211512"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="4e618-103">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="4e618-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e618-104">يشرح هذا الموضوع كيفية ربط موقع Microsoft Dynamics 365 Commerce الخاص بك بواحد أو أكثر من المتاجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4e618-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="4e618-105">بعد قيامك بتوفير بيئة التجارة الإلكترونية لـ Dynamics 365 Commerce الخاصة بك باستخدام مدخل Microsoft Dynamics Lifecycle Services (LCS)، تُصبح جاهزًا لإنشاء موقعك الأول للتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4e618-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="4e618-106">وكجزء من إنشاء الموقع الأولي، قم بربط الموقع مع متجر عبر الإنترنت تم إنشاؤه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="4e618-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="4e618-107">تربط هذه الخطوة الموقع بقناة على الإنترنت وتتيح للموقع عرض ‏‫التدرج الهرمي للتنقل والمنتجات والفئات والأسعار وخيارات الشحن وكل ما قمت بتحديده في المتجر عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4e618-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="4e618-108">لإنشاء موقع جديد وربط متجر عبر الإنترنت به، في LCS، حدد الرابط الخاص ببيئة تأليف الموقع.</span><span class="sxs-lookup"><span data-stu-id="4e618-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="4e618-109">ثم، على صفحة بيئة تأليف الموقع، حدد **موقع جديد**.</span><span class="sxs-lookup"><span data-stu-id="4e618-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="4e618-110">في مربع الحوار **موقع جديد** ، يجب عليك توفير بعض المعلومات الأساسية حول موقعك.</span><span class="sxs-lookup"><span data-stu-id="4e618-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="4e618-111">للحصول على شرح كامل للمعلومات التي يجب عليك توفيرها، راجع [إنشاء موقع جديد للتجارة الإلكترونية](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="4e618-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="4e618-112">بعد إنشاء موقعك، يمكنك التحقق من أنه مرتبط بمتجرك عبر الإنترنت من خلال تحديد علامة التبويب **المنتجات**. يجب أن تشاهد مجموعة متنوعة من المنتجات التي تم تخصيصها لمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="4e618-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="4e618-113">يمكنك أيضًا استخدام الحقل المنسدل في أعلى يمين الصفحة للوصول إلى المنتجات حسب الفئة.</span><span class="sxs-lookup"><span data-stu-id="4e618-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e618-114">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4e618-114">Additional resources</span></span>

[<span data-ttu-id="4e618-115">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="4e618-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4e618-116">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="4e618-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4e618-117">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="4e618-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4e618-118">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="4e618-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4e618-119">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="4e618-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4e618-120">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="4e618-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4e618-121">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="4e618-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4e618-122">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="4e618-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4e618-123">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="4e618-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4e618-124">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="4e618-124">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]