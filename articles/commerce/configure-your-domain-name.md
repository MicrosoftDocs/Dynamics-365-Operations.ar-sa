---
title: تكوين اسم مجالك
description: يوضح هذا الموضوع كيفية تكوين اسم مجال لموقع التجارة الإلكترونية Microsoft Dynamics 365.
author: psimolin
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4db774783dba4b1cea9552da3cff29a9528bd496
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002164"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="1e3fd-103">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="1e3fd-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1e3fd-104">يوضح هذا الموضوع كيفية تكوين اسم مجال لموقع التجارة الإلكترونية Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="1e3fd-105">إضافة المجالات أثناء تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1e3fd-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="1e3fd-106">لربط المجالات ببيئة التجارة الإلكترونية الخاصة بك، قم بتهيئة التجارة الإلكترونية كما هو موضح في [نشر موقع تجارة إلكترونية جديد](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="1e3fd-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="1e3fd-107">أثناء التهيئة، يُطلب منك تقديم المعلومات التي سيتم استخدامها لتوفير بيئة التجارة الإلكترونية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="1e3fd-108">في حقل **أسماء الأجهزة المضيفة المدعومة** ، أضف جميع المجالات التي تخطط لاستخدامها مع هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="1e3fd-109">يجب الفصل بين المجالات المتعددة بفاصلة منقوطة.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="1e3fd-110">وبهذه الطريقة، يتم تكوين المجالات في جميع مكونات التجارة الإلكترونية المطلوبة، وتكون جاهزة للاستخدام عند تبديل حركة المرور من شبكة تسليم المحتوى (CDN) أو خادم الويب وتوجيهها إلى الأطراف الأمامية للتجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="1e3fd-111">إضافة المجالات بعد تهيئة التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1e3fd-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="1e3fd-112">لربط المجالات الجديدة ببيئة التجارة الإلكترونية الخاصة بك بعد تهيئة التجارة الإلكترونية، يجب عليك تقديم طلب خدمة.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e3fd-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1e3fd-113">Additional resources</span></span>

[<span data-ttu-id="1e3fd-114">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="1e3fd-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="1e3fd-115">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="1e3fd-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="1e3fd-116">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="1e3fd-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="1e3fd-117">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="1e3fd-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="1e3fd-118">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="1e3fd-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="1e3fd-119">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="1e3fd-120">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="1e3fd-120">Enable location-based store detection</span></span>](enable-store-detection.md)
