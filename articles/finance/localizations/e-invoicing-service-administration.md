---
title: مكونات إدارة للفوترة الإلكترونية
description: يوفر هذا الموضوع معلومات حول المكونات المتعلقة بإدارة الفوترة الإلكترونية.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980912"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="1b1d3-103">مكونات إدارة للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1b1d3-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1b1d3-104">يوفر هذا الموضوع معلومات حول المكونات المتعلقة بإدارة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="1b1d3-105">كما يوفر معلومات حول كيفية تكوين خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="1b1d3-106">Azure</span><span class="sxs-lookup"><span data-stu-id="1b1d3-106">Azure</span></span>

<span data-ttu-id="1b1d3-107">استخدم Microsoft Azure لإنشاء الأسرار الخاصة بالمخزن الرئيسي وحساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="1b1d3-108">وبعد ذلك استخدم الأسرار الموجودة في تكوين الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="1b1d3-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="1b1d3-109">Lifecycle Services</span></span>

<span data-ttu-id="1b1d3-110">استخدم Microsoft Dynamics Lifecycle Services (LCS) لتمكين الخدمات المصغرة لمشروع نشر LCS الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="1b1d3-111">يتطلب تثبيت الخدمة الصغيرة في LCS وجود جهاز ظاهري من المستوى 2 على الأقل.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="1b1d3-112">لمزيد من المعلومات حول تخطيط البيئة، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d3-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="1b1d3-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="1b1d3-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="1b1d3-114">Dynamics 365 Regulatory Configuration Services (RCS) هو الواجهة التي تُستخدم لتكوين الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="1b1d3-115">ويتم إنشاء موارد مثل البيئات وميزات الفوترة الإلكترونية وصيانتها واستضافتها في RCS.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="1b1d3-116">عندما تكون الموارد جاهزة، يتم نشرها إلى خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="1b1d3-117">للتسجيل في RCS، راجع [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="1b1d3-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="1b1d3-118">لمزيد من المعلومات حول RCS، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="1b1d3-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="1b1d3-119">التكامل مع الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1b1d3-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="1b1d3-120">قبل أن تتمكن من استخدام RCS لتكوين الفواتير الإلكترونية، يجب تكوين RCS للسماح بالاتصال بالفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="1b1d3-121">قم بإكمال هذا التكوين في علامة التبويب **الفوترة الإلكترونية** في صفحة **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="1b1d3-122">نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-122">Service endpoint</span></span>

<span data-ttu-id="1b1d3-123">تتوفر الفوترة الإلكترونية في العديد من مناطق مراكز بيانات Azure الجغرافية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="1b1d3-124">يسرد الجدول التالي التوفر لكل منطقة.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="1b1d3-125">جغرافيا مركز بيانات Azure</span><span class="sxs-lookup"><span data-stu-id="1b1d3-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="1b1d3-126">الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-126">United States</span></span>              |
| <span data-ttu-id="1b1d3-127">أوروبا</span><span class="sxs-lookup"><span data-stu-id="1b1d3-127">Europe</span></span>                     |
| <span data-ttu-id="1b1d3-128">المملكة المتحدة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-128">United Kingdom</span></span>             |
| <span data-ttu-id="1b1d3-129">آسيا</span><span class="sxs-lookup"><span data-stu-id="1b1d3-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="1b1d3-130">بيئات الخدمة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-130">Service environments</span></span>

<span data-ttu-id="1b1d3-131">تعتبر بيئات الخدمة أقسامًا منطقية يتم إنشاؤها لدعم تنفيذ ميزات الفوترة الإلكترونية في الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="1b1d3-132">يجب تكوين أسرار الأمان والشهادات الرقمية، والتوجيه (بمعنى، أذونات الوصول)، على مستوى بيئة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="1b1d3-133">يمكن للعملاء إنشاء العديد من بيئات الخدمة كما يريدون.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="1b1d3-134">تكون كافة بيئات الخدمات التي ينشئها العميل مستقلة عن بعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="1b1d3-135">يجب إنشاء بيئات الخدمة وصيانتها في RCS.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="1b1d3-136">عندما تكون بيئات الخدمة جاهزة، يجب نشرها إلى الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="1b1d3-137">حالة بيئة الخدمة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-137">Service environment status</span></span>

<span data-ttu-id="1b1d3-138">يمكن إدارة بيئات الخدمة خلال الحالة.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-138">Service environments can be managed through status.</span></span> <span data-ttu-id="1b1d3-139">والخيارات المحتملة هي:</span><span class="sxs-lookup"><span data-stu-id="1b1d3-139">The possible options are:</span></span>

- <span data-ttu-id="1b1d3-140">**غير منشورة** – تم إنشاء البيئة، ولكن لم يتم نشرها بعد.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="1b1d3-141">**منشورة** – تم نشر البيئة إلى الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="1b1d3-142">**تم تغييرها** – تم تغيير سمات البيئة التي تم نشرها، ولكن لم يتم نشر التغييرات بعد.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="1b1d3-143">أسرار العميل</span><span class="sxs-lookup"><span data-stu-id="1b1d3-143">Customer secrets</span></span>

<span data-ttu-id="1b1d3-144">تتحمل خدمة الفوترة الإلكترونية المسولية عن تخزين جميع بيانات الأعمال في موارد Azure التي تملكها شركتك.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="1b1d3-145">للتأكد من أن الخدمة تعمل بشكل صحيح، وأن جميع بيانات العمل المطلوبة للفوترة الإلكترونية والتي تم إنشاؤها بواسطتها يتم الوصول إليها بشكل مناسب، يجب عليك إنشاء مصدرين رئيسيين في Azure:</span><span class="sxs-lookup"><span data-stu-id="1b1d3-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="1b1d3-146">حساب تخزين Azure (مخزن بيانات ثنائية كبيرة الحجم) والذي يخزن الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1b1d3-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="1b1d3-147">مخزن رئيسي في Azure والذي يخزن الشهادات ومعرف موقع منتظم (URI) لحساب التخزين</span><span class="sxs-lookup"><span data-stu-id="1b1d3-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="1b1d3-148">يجب تخصيص مخزن رئيسي مخصص وحساب تخزين للعميل لاستخدامهما خصيصًا مع الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="1b1d3-149">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d3-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="1b1d3-150">لمراقبة سلامة Key Vault وتلقي التنبيهات، قم بتكوين Azure Monitor لـ key Vault.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="1b1d3-151">من خلال تمكين تسجيل Key Vault، يمكنك مراقبة كيف ومتى ومن الذي يتم الوصول إلى Key Vaults الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="1b1d3-152">لمزيد منم المعلومات، راجع [المراقبة والتنبيه لـ Azure Key Vault](/azure/key-vault/general/alert) و[كيفية تمكين تسجيل الدخول إلى Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="1b1d3-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="1b1d3-153">كأفضل ممارسة، قم بتدوير الأسرار بشكل دوري.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="1b1d3-154">لمزيد من المعلومات، راجع [وثائق الأسرار](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="1b1d3-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="1b1d3-155">المستخدمين</span><span class="sxs-lookup"><span data-stu-id="1b1d3-155">Users</span></span>

<span data-ttu-id="1b1d3-156">يجب أن تسرد كل بيئة خدمة المستخدمين الذين يمكنهم الاتصال من Dynamics 365 Finance وDynamics 365 Supply Chain Management في الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="1b1d3-157">النشر</span><span class="sxs-lookup"><span data-stu-id="1b1d3-157">Publication</span></span>

<span data-ttu-id="1b1d3-158">يجب نشر بيئات الخدمة في الفوترة الإلكترونية حتى يمكن استخدامها.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="1b1d3-159">يمكن الوصول إلى البيئات المنشورة فقط من خلال Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1b1d3-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="1b1d3-160">بالاضافه إلى ذلك، يجب نشر بيئة الخدمة لكي تصبح أية تحديثات لسماتها نافذة المفعول في خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="1b1d3-161">التطبيقات المتصلة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-161">Connected applications</span></span>

<span data-ttu-id="1b1d3-162">تعتبر التطبيقات المتصلة مثيلات لـ Finance وSupply Chain Management التي قد ترغب في الوصول إليها من خلال RCS.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="1b1d3-163">بالاضافة إلى عنوان URL الخاص بالتطبيق والمستأجر الخاص به، يحتوي التطبيق المتصل على بيانات الاعتماد والتي تمكّن RCS من الاتصال بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="1b1d3-164">من خلال التطبيقات المتصلة، يمكنك تكوين جزء من ميزة الفوترة الإلكترونية في Finance وSupply Chain Management لجعل ميزة الفوترة الإلكترونية تعمل بالكامل.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="1b1d3-165">Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1b1d3-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="1b1d3-166">التكامل مع الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1b1d3-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="1b1d3-167">قبل أن تتمكن من استخدام Finance وSupply Chain Management لإصدار الفواتير الإلكترونية من خلال الفوترة الإلكترونية، يجب تكوين تكوينها للسماح بالاتصال بالخدمة.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="1b1d3-168">ميزة تكامل الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="1b1d3-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="1b1d3-169">لتمكين الاتصال بين Finance وSupply Chain Management والفوترة الإلكترونية، يجب تشغيل ميزة **تكامل الفوترة الإلكترونية** في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="1b1d3-170">نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="1b1d3-170">Service endpoint</span></span>

<span data-ttu-id="1b1d3-171">نقطة نهاية الخدمة هي عنوان URL الذي توجد فيه الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="1b1d3-172">قبل أن تتمكن من إصدار الفواتير الإلكترونية، يجب تكوين نقطة نهاية الخدمة في Finance وSupply Chain Management للسماح بالاتصال بالخدمة.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="1b1d3-173">لتكوين نقطة نهاية الخدمة، انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمة المستند الإلكتروني**، ثم، في علامة تبويب **خدمات الإرسال**، في حقل **URL الخاص بالفوترة الإلكترونية**، أدخل URL كما هو موضح في الجدول الموضح في قسم **نقطة نهاية الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="1b1d3-174">البيئات</span><span class="sxs-lookup"><span data-stu-id="1b1d3-174">Environments</span></span>

<span data-ttu-id="1b1d3-175">يشير اسم البيئة الذي تم إدخالة في Finance and Supply Chain Management إلى اسم البيئة الذي تم إنشاؤه في RCS ونشره إلى الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="1b1d3-176">ويجب تكوين البيئة في علامة التبويب **خدمات التسليم** في صفحة **معلمة المستند الإلكتروني**، وذلك لكي يحتوي كل طلب لإصدار الفواتير الإلكترونية على البيئة التي يمكن للفوترة الإلكترونية فيها تحديد أي ميزة للفوترة الإلكترونية يجب أن تعالج الطلب.</span><span class="sxs-lookup"><span data-stu-id="1b1d3-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b1d3-177">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1b1d3-177">Additional resources</span></span>

- [<span data-ttu-id="1b1d3-178">تكوين الفواتير الإلكترونية في RCS</span><span class="sxs-lookup"><span data-stu-id="1b1d3-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="1b1d3-179">إصدار الفواتير الإلكترونية في Finance وفي Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1b1d3-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
