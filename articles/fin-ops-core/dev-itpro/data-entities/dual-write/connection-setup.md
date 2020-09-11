---
title: السيناريوهات المدعومة لإعداد الكتابة المزدوجة
description: يصف هذا الموضوع السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706242"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="d49c4-103">السيناريوهات المدعومة لإعداد الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="d49c4-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="d49c4-104">يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة Finance and Operations وبيئة Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d49c4-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="d49c4-105">توفر **بيئة Finance and Operations** النظام الأساسي لـ **تطبيقات Finance and Operations** (على سبيل المثال Microsoft Dynamics 365 Finance و Dynamics 365 Supply Chain Management وDynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="d49c4-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="d49c4-106">توفر **بيئة Common Data Service** النظام الأساسي **للتطبيقات المستندة إلى نموذج في Dynamics 365** ‏(Dynamics 365 Sales وDynamics 365 Customer Service وDynamics 365 Field Service Dynamics 365 Marketing وDynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="d49c4-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="d49c4-107">يدعم Human Resources في Finance and Operations  اتصالات الكتابة المزدوجة، ولكن لا يدعمها تطبيق Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d49c4-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="d49c4-108">تختلف آلية الإعداد باختلاف اشتراكك وبيئتك.</span><span class="sxs-lookup"><span data-stu-id="d49c4-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="d49c4-109">بالنسبة إلى المثيلات الجديدة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d49c4-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d49c4-110">إذا كان لديك ترخيص Microsoft Power Platform، فستحل على بيئة Common Data Service جديدة، إذا لم يكن لدى المستأجر بيئة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-110">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="d49c4-111">بالنسبة إلى المثيلات الموجودة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d49c4-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="d49c4-112">سيناريوهات الإعداد التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="d49c4-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="d49c4-113">مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="d49c4-114">مثيل جديد لتطبيق Finance and Operations ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="d49c4-115">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="d49c4-116">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="d49c4-117">مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="d49c4-118">مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="d49c4-119">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d49c4-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d49c4-120">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="d49c4-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="d49c4-121">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d49c4-122">يتم تزويد مثيل جديد وفارغ من تطبيق يستند إلى نموذج، حيث تم تثبيت حل CRM الأساسي.</span><span class="sxs-lookup"><span data-stu-id="d49c4-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="d49c4-123">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="d49c4-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d49c4-124">يتم تمكين خرائط الكيانات للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d49c4-125">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="d49c4-126">مثيل جديد لتطبيق Finance and Operations ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="d49c4-127">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل موجود لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d49c4-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d49c4-128">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="d49c4-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="d49c4-129">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d49c4-130">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="d49c4-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d49c4-131">يتم تمكين خرائط الكيانات للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d49c4-132">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="d49c4-133">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d49c4-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d49c4-134">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d49c4-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d49c4-135">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d49c4-136">[قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="d49c4-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="d49c4-137">لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="d49c4-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="d49c4-138">مثيل جديد لتطبيق Finance and Operations يتضمن بيانات عرض توضيحي ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="d49c4-139">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل جديد لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج‬](#new-new) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="d49c4-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="d49c4-140">عند اكتمال إعداد الاتصال، إذا أردت مزامنة بيانات العرض التوضيحي مع التطبيق المستند إلى نموذج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d49c4-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="d49c4-141">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="d49c4-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d49c4-142">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="d49c4-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="d49c4-143">مثيل جديد لتطبيق Finance and Operations يتضمن بيانات عرض توضيحي ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="d49c4-144">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل موجود لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج‬](#new-existing) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="d49c4-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="d49c4-145">عند اكتمال إعداد الاتصال، إذا أردت مزامنة بيانات العرض التوضيحي مع التطبيق المستند إلى نموذج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d49c4-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="d49c4-146">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="d49c4-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d49c4-147">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="d49c4-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="d49c4-148">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d49c4-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d49c4-149">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d49c4-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d49c4-150">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="d49c4-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d49c4-151">[قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="d49c4-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="d49c4-152">لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="d49c4-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="d49c4-153">مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="d49c4-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="d49c4-154">يحدث إعداد اتصال الكتابة المزدوجة بين مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق يستند إلى نموذج في Dynamics 365 في بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="d49c4-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="d49c4-155">قم بإعداد الاتصال من تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d49c4-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="d49c4-156">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬</span><span class="sxs-lookup"><span data-stu-id="d49c4-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="d49c4-157">لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="d49c4-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
