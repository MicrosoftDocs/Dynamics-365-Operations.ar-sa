---
title: إرشادات حول كيفية إعداد الكتابة المزدوجة
description: يصف هذا الموضوع السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088496"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="27015-103">إرشادات حول كيفية إعداد الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="27015-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="27015-104">يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة Finance and Operations وبيئة Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="27015-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="27015-105">توفر **بيئة Finance and Operations** النظام الأساسي لـ **تطبيقات Finance and Operations** (على سبيل المثال Microsoft Dynamics 365 Finance و Dynamics 365 Supply Chain Management وDynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="27015-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="27015-106">توفر **بيئة Common Data Service** النظام الأساسي لـ **تطبيقات customer engagement** (Dynamics 365 Sales و Dynamics 365 Customer Service و Dynamics 365 Field Service و Dynamics 365 Marketing و Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="27015-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="27015-107">يدعم Human Resources في Finance and Operations  اتصالات الكتابة المزدوجة، ولكن لا يدعمها تطبيق Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="27015-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="27015-108">تختلف آلية الإعداد باختلاف اشتراكك وبيئتك.</span><span class="sxs-lookup"><span data-stu-id="27015-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="27015-109">بالنسبة إلى المثيلات الجديدة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="27015-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="27015-110">إذا كان لديك ترخيص Power Platform، فستحل على بيئة Common Data Service جديدة، إذا لم يكن لدى المستأجر بيئة.</span><span class="sxs-lookup"><span data-stu-id="27015-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="27015-111">بالنسبة إلى المثيلات الموجودة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27015-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="27015-112">قبل بدء الكتابة الثنائية لكيان ما، يمكنك تشغيل مزامنة أولية لمعالجة البيانات الموجودة على جانبي تطبيقات Finance and Operations وتطبيقات customer engagement.</span><span class="sxs-lookup"><span data-stu-id="27015-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="27015-113">يمكنك تخطي المزامنة الأولية إذا لم تكن بحاجة إلى مزامنة البيانات بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="27015-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="27015-114">تتيح المزامنة الأولية إمكانية نسخ البيانات الموجودة من تطبيق واحد إلى آخر بشكل ثنائي الاتجاه.</span><span class="sxs-lookup"><span data-stu-id="27015-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="27015-115">هناك عدة سيناريوهات إعداد مختلفة استنادًا إلى البيئات التي لديك بالفعل ونوع البيانات الموجودة في البيئات.</span><span class="sxs-lookup"><span data-stu-id="27015-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="27015-116">سيناريوهات الإعداد التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="27015-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="27015-117">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="27015-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="27015-118">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="27015-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="27015-119">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل جديد لتطبيق customer engagement</span><span class="sxs-lookup"><span data-stu-id="27015-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="27015-120">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل موجود لتطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="27015-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="27015-121">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="27015-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="27015-122">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="27015-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="27015-123">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="27015-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="27015-124">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق customer engagement، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="27015-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="27015-125">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="27015-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="27015-126">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="27015-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="27015-127">يتم تزويد مثيل جديد وفارغ من تطبيق customer engagement، حيث تم تثبيت حل CRM الأساسي.</span><span class="sxs-lookup"><span data-stu-id="27015-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="27015-128">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="27015-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="27015-129">يتم تمكين خرائط الكيانات للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="27015-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="27015-130">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="27015-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="27015-131">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="27015-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="27015-132">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق customer engagement حالي، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="27015-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="27015-133">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="27015-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="27015-134">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="27015-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="27015-135">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="27015-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="27015-136">يتم تمكين خرائط الكيانات للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="27015-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="27015-137">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="27015-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="27015-138">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="27015-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="27015-139">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27015-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="27015-140">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="27015-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="27015-141">[قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="27015-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="27015-142">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="27015-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27015-143">للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="27015-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="27015-144">مثيل تطبيق Finance and Operations جديد ويحتوي على بيانات ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="27015-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="27015-145">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل جديد لتطبيق customer engagement، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق customer engagement‬](#new-new) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="27015-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="27015-146">عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="27015-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="27015-147">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="27015-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="27015-148">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="27015-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27015-149">للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="27015-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="27015-150">مثيل تطبيق Finance and Operations جديد يحتوي على بيانات ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="27015-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="27015-151">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل حالي لتطبيق customer engagement، اتبع الخطوات الموجودة في [مثيل لتطبيق Finance and Operations ومثيل حالي لتطبيق customer engagement‬](#new-existing) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="27015-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="27015-152">عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="27015-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="27015-153">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="27015-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="27015-154">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="27015-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27015-155">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="27015-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="27015-156">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27015-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="27015-157">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="27015-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="27015-158">[قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="27015-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="27015-159">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="27015-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27015-160">للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="27015-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="27015-161">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="27015-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="27015-162">يحدث إعداد اتصال الكتابة المزدوجة بين مثيل حالي لتطبيق Finance and Operations ومثيل جديد لتطبيق customer engagement في بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="27015-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="27015-163">[قم بإعداد الاتصال من تطبيق Finance and Operations ](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="27015-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="27015-164">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="27015-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27015-165">للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="27015-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="27015-166">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="27015-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="27015-167">يحدث إعداد اتصال الكتابة المزدوجة بين مثيل حالي لتطبيق Finance and Operations ومثيل حالي لتطبيق customer engagement في بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="27015-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="27015-168">قم بإعداد الاتصال من تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27015-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="27015-169">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬</span><span class="sxs-lookup"><span data-stu-id="27015-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="27015-170">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="27015-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="27015-171">للاطلاع على مثال وطريقة بديلة، راجع [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="27015-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="27015-172">مثال</span><span class="sxs-lookup"><span data-stu-id="27015-172">Example</span></span>

<span data-ttu-id="27015-173">على سبيل المثال، راجع [تمكين Customers الإصدار 3—تعيين كيان جهات الاتصال](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="27015-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="27015-174">للحصول على أسلوب بديل يستند إلى وحدات تخزين البيانات في كل كيان التي يجب تشغيل المزامنة الأولية بها، راجع [اعتبارات المزامنة الأولية](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="27015-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
