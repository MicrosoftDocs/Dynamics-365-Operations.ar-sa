---
title: تكوين اسم مجالك
description: يوضح هذا الموضوع كيفية تكوين اسم مجال لموقع التجارة الإلكترونية Microsoft Dynamics 365.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ac1b0c8baaddd6ca62cc49657fff364df21c14f2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517102"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="8499d-103">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="8499d-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8499d-104">يوضح هذا الموضوع كيفية تكوين اسم مجال لموقع التجارة الإلكترونية Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8499d-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="8499d-105">إضافة المجالات أثناء تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="8499d-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="8499d-106">لربط المجالات ببيئة التجارة الإلكترونية لـ Dynamics 365 Commerce الخاصة بك، قم بتهيئة التجارة الإلكترونية كما هو موضح في [نشر مستأجر تجارة إلكترونية جديد‬](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="8499d-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="8499d-107">أثناء التهيئة، يُطلب منك تقديم المعلومات التي سيتم استخدامها لتوفير بيئة التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="8499d-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="8499d-108">في حقل **أسماء الأجهزة المضيفة المدعومة** ، أضف جميع المجالات التي تخطط لاستخدامها مع هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="8499d-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="8499d-109">يجب الفصل بين المجالات المتعددة بفاصلة منقوطة.</span><span class="sxs-lookup"><span data-stu-id="8499d-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="8499d-110">وبهذه الطريقة، يتم تكوين المجالات في جميع مكونات التجارة الإلكترونية المطلوبة، وتكون جاهزة للاستخدام عند تبديل حركة المرور من شبكة تسليم المحتوى (CDN) أو خادم الويب وتوجيهها إلى الأطراف الأمامية للتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8499d-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="8499d-111">إضافة المجالات بعد تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="8499d-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="8499d-112">لربط المجالات الجديدة ببيئة التجارة الإلكترونية الخاصة بك بعد تهيئة التجارة الإلكترونية، يجب عليك تقديم طلب خدمة.</span><span class="sxs-lookup"><span data-stu-id="8499d-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8499d-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8499d-113">Additional resources</span></span>

[<span data-ttu-id="8499d-114">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="8499d-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8499d-115">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="8499d-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8499d-116">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="8499d-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8499d-117">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="8499d-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8499d-118">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="8499d-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8499d-119">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="8499d-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8499d-120">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="8499d-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8499d-121">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="8499d-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8499d-122">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="8499d-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8499d-123">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="8499d-123">Enable location-based store detection</span></span>](enable-store-detection.md)
