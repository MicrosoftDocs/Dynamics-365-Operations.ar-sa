---
title: مكونات إدارة الوظيفة الإضافية للفوترة الإلكترونية
description: يوفر هذا الموضوع معلومات حول المكونات المتعلقة بإدارة الوظيفة الإضافيه للفوترة الإلكترونية.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592564"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="e0894-103">مكونات إدارة الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e0894-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e0894-104">يوفر هذا الموضوع معلومات حول المكونات المتعلقة بإدارة الوظيفة الإضافيه للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="e0894-105">كما يوفر معلومات حول كيفية تكوين الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="e0894-106">Azure</span><span class="sxs-lookup"><span data-stu-id="e0894-106">Azure</span></span>

<span data-ttu-id="e0894-107">استخدم Microsoft Azure لإنشاء الأسرار الخاصة بالمخزن الرئيسي وحساب التخزين.</span><span class="sxs-lookup"><span data-stu-id="e0894-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="e0894-108">وبعد ذلك استخدم الأسرار الموجودة في تكوين الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="e0894-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e0894-109">Lifecycle Services</span></span>

<span data-ttu-id="e0894-110">استخدم Microsoft Dynamics Lifecycle Services (LCS) لتمكين الوظيفة الإضافية للخدمات المصغرة لمشروع نشر LCS الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e0894-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="e0894-111">يتطلب تثبيت الوظيفة الإضافية للخدمة الصغيرة في LCS وجود جهاز ظاهري من المستوى 2 على الأقل.</span><span class="sxs-lookup"><span data-stu-id="e0894-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="e0894-112">لمزيد من المعلومات حول تخطيط البيئة، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e0894-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="e0894-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="e0894-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="e0894-114">Dynamics 365 Regulatory Configuration Services (RCS) هو الواجهة التي تُستخدم لتكوين الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="e0894-115">ويتم إنشاء موارد مثل البيئات وميزات الفوترة الإلكترونية وصيانتها واستضافتها في RCS.</span><span class="sxs-lookup"><span data-stu-id="e0894-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="e0894-116">عندما تكون الموارد جاهزة، يتم نشرها إلى خدمة الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="e0894-117">للتسجيل في RCS، راجع [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="e0894-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="e0894-118">لمزيد من المعلومات حول RCS، راجع [Regulatory Configuration Services (RCS) - ميزات العولمة](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="e0894-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="e0894-119">التكامل مع الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e0894-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="e0894-120">قبل أن تتمكن من استخدام RCS لتكوين الفواتير الإلكترونية، يجب تكوين RCS للسماح بالاتصال بالوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="e0894-121">قم بإكمال هذا التكوين في علامة التبويب **الوظيفة الإضافية للفوترة الإلكترونية** في صفحة **معلمات التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="e0894-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="e0894-122">نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="e0894-122">Service endpoint</span></span>

<span data-ttu-id="e0894-123">تتوفر الوظيفة الإضافية للفوترة الإلكترونية في العديد من مناطق مراكز بيانات Azure الجغرافية.</span><span class="sxs-lookup"><span data-stu-id="e0894-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="e0894-124">يسرد الجدول التالي التوفر لكل منطقة.</span><span class="sxs-lookup"><span data-stu-id="e0894-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="e0894-125">جغرافيا مركز بيانات Azure</span><span class="sxs-lookup"><span data-stu-id="e0894-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="e0894-126">شرق الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="e0894-126">East US</span></span>                    |
| <span data-ttu-id="e0894-127">غرب الولايات المتحدة</span><span class="sxs-lookup"><span data-stu-id="e0894-127">West US</span></span>                    |
| <span data-ttu-id="e0894-128">شمال الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="e0894-128">North EU</span></span>                   |
| <span data-ttu-id="e0894-129">غرب الاتحاد الأوروبي</span><span class="sxs-lookup"><span data-stu-id="e0894-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="e0894-130">بيئات الخدمة</span><span class="sxs-lookup"><span data-stu-id="e0894-130">Service environments</span></span>

<span data-ttu-id="e0894-131">تعتبر بيئات الخدمة أقسامًا منطقية يتم إنشاؤها لدعم تنفيذ ميزات الفوترة الإلكترونية في الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="e0894-132">يجب تكوين أسرار الأمان والشهادات الرقمية، والتوجيه (بمعنى، أذونات الوصول)، على مستوى بيئة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="e0894-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="e0894-133">يمكن للعملاء إنشاء العديد من بيئات الخدمة كما يريدون.</span><span class="sxs-lookup"><span data-stu-id="e0894-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="e0894-134">تكون كافة بيئات الخدمات التي ينشئها العميل مستقلة عن بعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="e0894-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="e0894-135">يجب إنشاء بيئات الخدمة وصيانتها في RCS.</span><span class="sxs-lookup"><span data-stu-id="e0894-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="e0894-136">عندما تكون بيئات الخدمة جاهزة، يجب نشرها إلى الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="e0894-137">حالة بيئة الخدمة</span><span class="sxs-lookup"><span data-stu-id="e0894-137">Service environment status</span></span>

<span data-ttu-id="e0894-138">يمكن إدارة بيئات الخدمة خلال الحالة.</span><span class="sxs-lookup"><span data-stu-id="e0894-138">Service environments can be managed through status.</span></span> <span data-ttu-id="e0894-139">والخيارات المحتملة هي:</span><span class="sxs-lookup"><span data-stu-id="e0894-139">The possible options are:</span></span>

- <span data-ttu-id="e0894-140">**غير منشورة** – تم إنشاء البيئة، ولكن لم يتم نشرها بعد.</span><span class="sxs-lookup"><span data-stu-id="e0894-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="e0894-141">**منشورة** – تم نشر البيئة إلى الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="e0894-142">**تم تغييرها** – تم تغيير سمات البيئة التي تم نشرها، ولكن لم يتم نشر التغييرات بعد.</span><span class="sxs-lookup"><span data-stu-id="e0894-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="e0894-143">أسرار العميل</span><span class="sxs-lookup"><span data-stu-id="e0894-143">Customer secrets</span></span>

<span data-ttu-id="e0894-144">تتحمل خدمة الوظيفة الإضافية الفوترة الإلكترونية المسولية عن تخزين جميع بيانات الأعمال في موارد Azure التي تملكها شركتك.</span><span class="sxs-lookup"><span data-stu-id="e0894-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="e0894-145">لضمان عمل الخدمة بشكل صحيح، وأن الوصول إلى كافة بيانات الأعمال المطلوبة والمُنشأة من قِبل الوظيفة الإضافية للفوترة الإلكترونية يتم فقط بواسطة هذه الوظيفة الإضافية، يجب عليك إنشاء موردين أساسيين في Azure:</span><span class="sxs-lookup"><span data-stu-id="e0894-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="e0894-146">حساب تخزين Azure (مخزن بيانات ثنائية كبيرة الحجم) والذي يخزن الفواتير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e0894-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="e0894-147">مخزن رئيسي في Azure والذي يخزن الشهادات ومعرف موقع منتظم (URI) لحساب التخزين</span><span class="sxs-lookup"><span data-stu-id="e0894-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="e0894-148">يجب تخصيص مخزن رئيسي مخصص وحساب تخزين للعميل لاستخدامهما خصيصًا مع الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="e0894-149">لمزيد من المعلومات، راجع [إنشاء حساب تخزين وKey Vault ومخزن رئيسي](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="e0894-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="e0894-150">المستخدمين</span><span class="sxs-lookup"><span data-stu-id="e0894-150">Users</span></span>

<span data-ttu-id="e0894-151">يجب أن تسرد كل بيئة خدمة المستخدمين الذين يمكنهم الاتصال من Dynamics 365 Finance وDynamics 365 Supply Chain Management في الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="e0894-152">النشر</span><span class="sxs-lookup"><span data-stu-id="e0894-152">Publication</span></span>

<span data-ttu-id="e0894-153">يجب نشر بيئات الخدمة في الوظيفة الإضافية للفوترة الإلكترونية حتى يمكن استخدامها.</span><span class="sxs-lookup"><span data-stu-id="e0894-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="e0894-154">يمكن الوصول إلى البيئات المنشورة فقط من خلال Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e0894-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="e0894-155">بالاضافه إلى ذلك، يجب نشر بيئة الخدمة لكي تصبح أية تحديثات لسماتها نافذة المفعول في خدمة الفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="e0894-156">التطبيقات المتصلة</span><span class="sxs-lookup"><span data-stu-id="e0894-156">Connected applications</span></span>

<span data-ttu-id="e0894-157">تعتبر التطبيقات المتصلة مثيلات لـ Finance وSupply Chain Management التي قد ترغب في الوصول إليها من خلال RCS.</span><span class="sxs-lookup"><span data-stu-id="e0894-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="e0894-158">بالاضافة إلى عنوان URL الخاص بالتطبيق والمستأجر الخاص به، يحتوي التطبيق المتصل على بيانات الاعتماد والتي تمكّن RCS من الاتصال بالبيئة.</span><span class="sxs-lookup"><span data-stu-id="e0894-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="e0894-159">من خلال التطبيقات المتصلة، يمكنك تكوين جزء من ميزة الفوترة الإلكترونية في Finance وSupply Chain Management لجعل ميزة الفوترة الإلكترونية تعمل بالكامل.</span><span class="sxs-lookup"><span data-stu-id="e0894-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="e0894-160">Finance وSupply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e0894-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="e0894-161">التكامل مع الوظيفة الإضافية للفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e0894-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="e0894-162">قبل أن تتمكن من استخدام Finance وSupply Chain Management لإصدار الفواتير الإلكترونية من خلال الوظيفة الإضافية للفوترة الإلكترونية، يجب تكوين الوظيفة الإضافية للسماح بالاتصال بالخدمة.</span><span class="sxs-lookup"><span data-stu-id="e0894-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="e0894-163">ميزة تكامل الوظيفة الإضافية الفوترة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="e0894-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="e0894-164">لتمكين الاتصال بين Finance وSupply Chain Management والوظيفة الإضافية للفوترة الإلكترونية، يجب تشغيل ميزة **تكامل الوظيفة الإضافية للفوترة الإلكترونية** في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="e0894-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="e0894-165">نقطة نهاية الخدمة</span><span class="sxs-lookup"><span data-stu-id="e0894-165">Service endpoint</span></span>

<span data-ttu-id="e0894-166">نقطة نهاية الخدمة هي عنوان URL الذي توجد فيه الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="e0894-167">قبل أن تتمكن من إصدار الفواتير الإلكترونية، يجب تكوين نقطة نهاية الخدمة في Finance وSupply Chain Management للسماح بالاتصال بالخدمة.</span><span class="sxs-lookup"><span data-stu-id="e0894-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="e0894-168">لتكوين نقطة نهاية الخدمة، انتقل إلى **إدارة المؤسسة \> الإعداد \> معلمة المستند الإلكتروني**، ثم، في علامة تبويب **خدمات الإرسال**، في حقل **URL الخاص بالوظيفة الإضافية للفوترة الإلكترونية**، أدخل URL كما هو موضح في الجدول الموضح في قسم **نقطة نهاية الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="e0894-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="e0894-169">البيئات</span><span class="sxs-lookup"><span data-stu-id="e0894-169">Environments</span></span>

<span data-ttu-id="e0894-170">يشير اسم البيئة الذي تم إدخالة في Finance and Supply Chain Management إلى اسم البيئة الذي تم إنشاؤه في RCS ونشره إلى الوظيفة الإضافية للفوترة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="e0894-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="e0894-171">ويجب تكوين البيئة في علامة التبويب **خدمات التسليم** في صفحة **معلمة المستند الإلكتروني**، وذلك لكي يحتوي كل طلب لإصدار الفواتير الإلكترونية على البيئة التي يمكن للوظيفة الإضافية للفوترة الإلكترونية فيها تحديد أي ميزة للفوترة الإلكترونية يجب أن تعالج الطلب.</span><span class="sxs-lookup"><span data-stu-id="e0894-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0894-172">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="e0894-172">Additional resources</span></span>

- [<span data-ttu-id="e0894-173">تكوين الفواتير الإلكترونية في RCS</span><span class="sxs-lookup"><span data-stu-id="e0894-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="e0894-174">إصدار الفواتير الإلكترونية في Finance وفي Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e0894-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
