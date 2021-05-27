---
title: Regulatory Configuration Service
description: يقدم هذا الموضوع نظرة عامة حول إمكانيات Regulatory Configuration Service (RCS) ويشرح كيفية الوصول إلى الخدمة.
author: JaneA07
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019384"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="7bcb1-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="7bcb1-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bcb1-104">إن Regulatory Configuration Service (RCS) عبارة عن مصمم مستقل وخدمة إدارة دورة حياة لوظيفة عولمة بدون كود/كود منخفض.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="7bcb1-105">تسمح RCS للمساهمين في العولمة بتمديد وتخصيص مناطق العولمة الرئيسية للضرائب والفوترة الإلكترونية والتقارير التنظيمية والبنود ومستندات العمل من دون الحاجة إلى مشاركة المطورين.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="7bcb1-106">يجعل أسلوب العولمة هذا بدون كود/كود منخفض العولمة أكثر سهولة وسرعة وأكثر فعالية من حيث التكلفة للإنشاء أو التمديد.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="7bcb1-107">توفر ميزة RCS القدرات التالية:</span><span class="sxs-lookup"><span data-stu-id="7bcb1-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="7bcb1-108">دعم لكافة الوظائف التي يتم توفيرها بواسطة إعداد التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="7bcb1-109">أحد المتطلبات الأساسية لتكوين الخدمات الصغيرة الجديدة للعولمة.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="7bcb1-110">دعم الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="7bcb1-111">لمزيد من المعلومات، راجع [الفوترة الإلكترونية‎](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="7bcb1-112">دعم حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="7bcb1-113">لمزيد من المعلومات، راجع [خدمة الضريبة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="7bcb1-114">دعم وظيفة ميزات العولمة الجديدة التي تبسط إدارة دورة الحياة لميزات متعددة المكونات وتوفر قدرة إضافية لتكوين الإجراءات وإعداد معلمات الميزات.</span><span class="sxs-lookup"><span data-stu-id="7bcb1-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="7bcb1-115">لمزيد من المعلومات، راجع  [Regulatory Configuration Service – إدارة ميزات العولمة المبسطة لخدمات العولمة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="7bcb1-116">دعم عمليات النشر والتخزين والمشاركة المركزية للتكوينات المخصصة في المستودع العمومي لتبسيط إدارة التكوين المبسطة من دون الحاجة إلى استخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="7bcb1-117">الوصول إلى RCS</span><span class="sxs-lookup"><span data-stu-id="7bcb1-117">Access RCS</span></span>

<span data-ttu-id="7bcb1-118">يمكنك التسجيل في RCS أو تسجيل الدخول إليها في [صفحة Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![التسجيل في/تسجيل الدخول إلى RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="7bcb1-120">في صفحة **Regulatory Configuration Service**، راجع ووافق على الشروط والأحكام الإضافية لاستخدام الخدمة، ثم حدد أحد الأزرار التالية:</span><span class="sxs-lookup"><span data-stu-id="7bcb1-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="7bcb1-121">**التسجيل** إذا كنت تستخدم الخدمة للمرة الأولى، وكنت تستخدم عنوان بريد إلكتروني للعمل لتزويد مؤسستك ببيئة خدمة</span><span class="sxs-lookup"><span data-stu-id="7bcb1-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="7bcb1-122">**تسجيل الدخول** إذا سبق لك التسجيل في الخدمة، وأردت الوصول إلى بيئة مؤسستك</span><span class="sxs-lookup"><span data-stu-id="7bcb1-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="7bcb1-123">التوافر الإقليمي</span><span class="sxs-lookup"><span data-stu-id="7bcb1-123">Regional availability</span></span>

<span data-ttu-id="7bcb1-124">تتوفر خدمة RCS بشكل عام في المناطق التالية:</span><span class="sxs-lookup"><span data-stu-id="7bcb1-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="7bcb1-125">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="7bcb1-125">United States</span></span>
- <span data-ttu-id="7bcb1-126">الهند</span><span class="sxs-lookup"><span data-stu-id="7bcb1-126">India</span></span>
- <span data-ttu-id="7bcb1-127">فرنسا</span><span class="sxs-lookup"><span data-stu-id="7bcb1-127">France</span></span>
- <span data-ttu-id="7bcb1-128">أوروبا</span><span class="sxs-lookup"><span data-stu-id="7bcb1-128">Europe</span></span>

<span data-ttu-id="7bcb1-129">للحصول على قائمه كامله بالمناطق، راجع [Dynamics 365 وPower Platform: التوافر وموقع البيانات واللغة والترجمة](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="7bcb1-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="7bcb1-130">وثائق RCS ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="7bcb1-130">Related RCS documentation</span></span>

<span data-ttu-id="7bcb1-131">لمزيد من المعلومات حول المكونات ذات الصلة، راجع الوثائق التالية:</span><span class="sxs-lookup"><span data-stu-id="7bcb1-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="7bcb1-132">**المستودع العمومي:**</span><span class="sxs-lookup"><span data-stu-id="7bcb1-132">**Global repository:**</span></span>

    - [<span data-ttu-id="7bcb1-133">إنشاء تكوين التقارير الإلكترونية وتحميله إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="7bcb1-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="7bcb1-134">مشاركة التكوين في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="7bcb1-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="7bcb1-135">التصفية المحسنة في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="7bcb1-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="7bcb1-136">تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="7bcb1-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="7bcb1-137">إيقاف التكوينات في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="7bcb1-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="7bcb1-138">**ميزة العولمة:**</span><span class="sxs-lookup"><span data-stu-id="7bcb1-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="7bcb1-139">Regulatory Configuration Service (RCS) - ميزة العولمة</span><span class="sxs-lookup"><span data-stu-id="7bcb1-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)