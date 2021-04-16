---
title: الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce
description: يوفر هذا الموضوع إجابات للأسئلة الشائعة حول بيئة تقييم Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e42618a522f5ad551f608605300c30b5ffb8e299
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795921"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="206dc-103">الأسئلة المتداولة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="206dc-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="206dc-104">يوفر هذا الموضوع إجابات للأسئلة الشائعة حول بيئة تقييم Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="206dc-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="206dc-105">**هل يمكن استخدام بيئة تقييم Commerce كواجهة للتجارة الإلكترونية للعملاء الذين يتولون حاليًا مسؤولية تنفيذ البيع بالتجزئة؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="206dc-106">الرقم</span><span class="sxs-lookup"><span data-stu-id="206dc-106">No.</span></span> <span data-ttu-id="206dc-107">بيئة تقييم Commerce هي بيئة مخصصة للتقييم فقط.</span><span class="sxs-lookup"><span data-stu-id="206dc-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="206dc-108">إذا كنت تحتاج إلى بيئة للعميل الذي يقوم بتنفيذ البيع بالتجزئة، اتصل بـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="206dc-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="206dc-109">**هل يمكن استخدام بيئة تقييم التجارة لتوفير ميزات التجارة الإلكترونية على رأس تطبيق/بيئة حالية تنفذ البيع بالتجزئة؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="206dc-110">لا (غالبًا).</span><span class="sxs-lookup"><span data-stu-id="206dc-110">No (mostly).</span></span> <span data-ttu-id="206dc-111">لا تتوفر مكونات تقييم التجارة إلا للبيئات التي تطابق التكوينات المحددة في دليل التوفير والمتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="206dc-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="206dc-112">وبالإضافة إلى ذلك، لن تتوفر بيانات العرض التوضيحي الأساسي المطلوبة في البيئات التي تم نشرها بإصدار أولي أقدم من 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="206dc-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="206dc-113">**ما التكاليف التي ينطوي عليها نشر بيئة تقييم Commerce في Microsoft Azure عبر خدمات Microsoft Dynamics Lifecycle Services (LCS)؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="206dc-114">ستتم استضافة بيئة Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce تقليدية للعرض التوضيحي للمقرات الرئيسية (جهاز ظاهري \[VM\]) في اشتراكك في Azure.</span><span class="sxs-lookup"><span data-stu-id="206dc-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="206dc-115">يمكنك استخدام [حاسبة تسعير Azure](https://azure.microsoft.com/pricing/calculator/) لتقدير هذه التكلفة.</span><span class="sxs-lookup"><span data-stu-id="206dc-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="206dc-116">ستتوفر المكونات الأخرى مثل Commerce Scale Unit ومنشئ مواقع Commerce وموقع التجارة الإلكترونية كخدمة تأجير البرامج (SaaS) وستتم استضافتها بواسطة Microsoft.</span><span class="sxs-lookup"><span data-stu-id="206dc-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="206dc-117">**ما مناطق Azure الجغرافية المدعومة حاليًا لبيئة تقييم Commerce؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="206dc-118">لا يمكن نشر بيئة تقييم Commerce إلا في جغرافيا أمريكا الشمالية.</span><span class="sxs-lookup"><span data-stu-id="206dc-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="206dc-119">**هل يوجد قرص ثابت ظاهري قابل للتنزيل (VHD) به خيار جهاز ظاهري (جهاز ظاهري) OneBox كامل؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="206dc-120">تعتبر Dynamics 365 Commerce وCommerce Scale Unit بمثابة خدمة تأجير البرامج‬ (SaaS) ويجب استضافتها على السحابة.</span><span class="sxs-lookup"><span data-stu-id="206dc-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="206dc-121">**ما طول مدة استخدام بيئة تقييم Commerce؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="206dc-122">تنطوي بيئة تقييم Commerce على حد زمني لمدة 30 يومًا من تاريخ توفير مكونات خدمة تأجير البرامج مثل Commerce Scale Unit ومنشئ مواقع Commerce وموقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="206dc-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="206dc-123">**هل يمكنني تمديد الحد الزمني لبيئة تقييم Commerce لدي؟**</span><span class="sxs-lookup"><span data-stu-id="206dc-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="206dc-124">يعد تمديد الحد الزمني استثناءًا للقاعدة ويتم اعتباره لكل حالة على حدة.</span><span class="sxs-lookup"><span data-stu-id="206dc-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="206dc-125">ينبغي الاتصال بجهة اتصال شريك Microsoft للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="206dc-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="206dc-126">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="206dc-126">Additional resources</span></span>

[<span data-ttu-id="206dc-127">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="206dc-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="206dc-128">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="206dc-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="206dc-129">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="206dc-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="206dc-130">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="206dc-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="206dc-131">تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="206dc-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]