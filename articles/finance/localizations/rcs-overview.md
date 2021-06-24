---
title: Regulatory Configuration Service
description: يقدم هذا الموضوع نظرة عامة حول إمكانيات Regulatory Configuration Service (RCS) ويشرح كيفية الوصول إلى الخدمة.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216552"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="38174-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="38174-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38174-104">إن Regulatory Configuration Service (RCS) عبارة عن مصمم مستقل وخدمة إدارة دورة حياة لوظيفة عولمة بدون كود/كود منخفض.</span><span class="sxs-lookup"><span data-stu-id="38174-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="38174-105">تسمح RCS للمساهمين في العولمة بتمديد وتخصيص مناطق العولمة الرئيسية للضرائب والفوترة الإلكترونية والتقارير التنظيمية والبنود ومستندات العمل من دون الحاجة إلى مشاركة المطورين.</span><span class="sxs-lookup"><span data-stu-id="38174-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="38174-106">يجعل أسلوب العولمة هذا بدون كود/كود منخفض العولمة أكثر سهولة وسرعة وأكثر فعالية من حيث التكلفة للإنشاء أو التمديد.</span><span class="sxs-lookup"><span data-stu-id="38174-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="38174-107">توفر ميزة RCS القدرات التالية:</span><span class="sxs-lookup"><span data-stu-id="38174-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="38174-108">دعم لكافة الوظائف التي يتم توفيرها بواسطة إعداد التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="38174-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="38174-109">أحد المتطلبات الأساسية لتكوين الخدمات الصغيرة الجديدة للعولمة.</span><span class="sxs-lookup"><span data-stu-id="38174-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="38174-110">دعم الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="38174-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="38174-111">لمزيد من المعلومات، راجع [الفوترة الإلكترونية‎](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="38174-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="38174-112">دعم حساب الضريبة.</span><span class="sxs-lookup"><span data-stu-id="38174-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="38174-113">لمزيد من المعلومات، راجع [خدمة الضريبة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="38174-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="38174-114">دعم وظيفة ميزات العولمة الجديدة التي تبسط إدارة دورة الحياة لميزات متعددة المكونات وتوفر قدرة إضافية لتكوين الإجراءات وإعداد معلمات الميزات.</span><span class="sxs-lookup"><span data-stu-id="38174-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="38174-115">لمزيد من المعلومات، راجع  [Regulatory Configuration Service – إدارة ميزات العولمة المبسطة لخدمات العولمة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="38174-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="38174-116">دعم عمليات النشر والتخزين والمشاركة المركزية للتكوينات المخصصة في المستودع العمومي لتبسيط إدارة التكوين المبسطة من دون الحاجة إلى استخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="38174-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="38174-117">الوصول إلى RCS</span><span class="sxs-lookup"><span data-stu-id="38174-117">Access RCS</span></span>

<span data-ttu-id="38174-118">يمكنك التسجيل في RCS أو تسجيل الدخول إليها في [صفحة Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="38174-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![التسجيل في/تسجيل الدخول إلى RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="38174-120">في صفحة **Regulatory Configuration Service**، راجع ووافق على الشروط والأحكام الإضافية لاستخدام الخدمة، ثم حدد أحد الأزرار التالية:</span><span class="sxs-lookup"><span data-stu-id="38174-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="38174-121">**التسجيل** إذا كنت تستخدم الخدمة للمرة الأولى، وكنت تستخدم عنوان بريد إلكتروني للعمل لتزويد مؤسستك ببيئة خدمة</span><span class="sxs-lookup"><span data-stu-id="38174-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="38174-122">**تسجيل الدخول** إذا سبق لك التسجيل في الخدمة، وأردت الوصول إلى بيئة مؤسستك</span><span class="sxs-lookup"><span data-stu-id="38174-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="38174-123">التوافر الإقليمي</span><span class="sxs-lookup"><span data-stu-id="38174-123">Regional availability</span></span>

<span data-ttu-id="38174-124">تتوفر خدمة RCS بشكل عام في المناطق التالية:</span><span class="sxs-lookup"><span data-stu-id="38174-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="38174-125">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="38174-125">United States</span></span>
- <span data-ttu-id="38174-126">الهند</span><span class="sxs-lookup"><span data-stu-id="38174-126">India</span></span>
- <span data-ttu-id="38174-127">فرنسا</span><span class="sxs-lookup"><span data-stu-id="38174-127">France</span></span>
- <span data-ttu-id="38174-128">أوروبا</span><span class="sxs-lookup"><span data-stu-id="38174-128">Europe</span></span>

<span data-ttu-id="38174-129">للحصول على قائمه كامله بالمناطق، راجع [Dynamics 365 وPower Platform: التوافر وموقع البيانات واللغة والترجمة](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="38174-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="38174-130">الشركة الافتراضية RCS</span><span class="sxs-lookup"><span data-stu-id="38174-130">RCS default company</span></span>

<span data-ttu-id="38174-131">تتم مشاركة وظيفة وقت التصميم المستخدمة في RCS عبر كافة الشركات.</span><span class="sxs-lookup"><span data-stu-id="38174-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="38174-132">لا توجد وظيفة خاصة بالشركة.</span><span class="sxs-lookup"><span data-stu-id="38174-132">There is no company-specific functionality.</span></span> <span data-ttu-id="38174-133">وبالتالي، نُوصي باستخدام شركة واحدة، **DAT**، مع بيئة RCS الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="38174-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="38174-134">ومع ذلك، في بعض السيناريوهات، قد تحتاج إلى جعل تنسيقات التقارير الإلكترونية تستخدم المعلمات المرتبطة بكيان قانوني محدد.</span><span class="sxs-lookup"><span data-stu-id="38174-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="38174-135">في هذه السيناريوهات هذه فقط، يجب استخدام مبدل الشركة الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="38174-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="38174-136">على سبيل المثال، راجع [تكوين تنسيقات التقارير الإلكترونية لاستخدام المعلمات المحددة لكل كيان قانوني](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="38174-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="38174-137">وثائق RCS ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="38174-137">Related RCS documentation</span></span>

<span data-ttu-id="38174-138">لمزيد من المعلومات حول المكونات ذات الصلة، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="38174-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="38174-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="38174-139">**RCS:**</span></span>

    - [<span data-ttu-id="38174-140">إنشاء تكوينات ER في RCS وتحميلها إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="38174-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="38174-141">**المستودع العمومي:**</span><span class="sxs-lookup"><span data-stu-id="38174-141">**Global repository:**</span></span>

    - [<span data-ttu-id="38174-142">إنشاء تكوين التقارير الإلكترونية وتحميله إلى المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="38174-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="38174-143">مشاركة التكوين في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="38174-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="38174-144">التصفية المحسنة في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="38174-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="38174-145">تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="38174-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="38174-146">إيقاف التكوينات في المستودع العمومي</span><span class="sxs-lookup"><span data-stu-id="38174-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="38174-147">إهلاك تخزين Regulatory Configuration Service (RCS) – Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="38174-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="38174-148">**ميزة العولمة:**</span><span class="sxs-lookup"><span data-stu-id="38174-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="38174-149">Regulatory Configuration Service (RCS) - ميزة العولمة</span><span class="sxs-lookup"><span data-stu-id="38174-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="38174-150">استكشاف أخطاء التسجيل في RCS وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="38174-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="38174-151">عندما تقوم بالتسجيل في RCS من صفحة الخدمة، قد تواجه مشكلة مرتبطة بـ Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="38174-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="38174-152">تشير رسالة الخطأ التي تظهر إلى أنه تم إيقاف تشغيل التسجيل في RCS حاليًا ويجب تشغيل التسجيل قبل أن تتمكن من إكمال عملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="38174-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![رسالة خطأ التسجيل في RCS](media/01_RCSSignUpError.jpg)

<span data-ttu-id="38174-154">تحدث هذه المشكلة بسبب أنك محظور من التسجيل للاشتراكات المخصصة، ويجب تمكين الخاصية `AllowAdHocSubscriptions` في المستأجر الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="38174-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="38174-155">إذا قام قسم تكنولوجيا المعلومات الخاص بك بإدارة مستأجري Azure لمؤسسك، فاتصل بذلك القسم للإبلاغ عن المشكلة.</span><span class="sxs-lookup"><span data-stu-id="38174-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="38174-156">إذا كنت مسؤولاً عن إدارة مستأجري Azure، فيمكنك إصلاح المشكلات باتباع الخطوات الموجودة في [ما التسجيل بالخدمة الذاتية لـ Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="38174-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
