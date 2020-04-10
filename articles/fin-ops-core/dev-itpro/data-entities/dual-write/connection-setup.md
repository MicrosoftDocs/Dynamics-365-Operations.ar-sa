---
title: السيناريوهات المدعومة لإعداد الكتابة المزدوجة
description: يصف هذا الموضوع السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172844"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="b7c1e-103">السيناريوهات المدعومة لإعداد الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="b7c1e-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b7c1e-104">يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة Finance and Operations وبيئة Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="b7c1e-105">توفر **بيئة Finance and Operations** النظام الاساسي **لتطبيقات Finance and Operations** (على سبيل المثال Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Retail وDynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="b7c1e-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="b7c1e-106">توفر **بيئة Common Data Service** النظام الأساسي **للتطبيقات المستندة إلى نموذج في Dynamics 365** ‏(Dynamics 365 Sales وDynamics 365 Customer Service وDynamics 365 Field Service Dynamics 365 Marketing وDynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="b7c1e-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="b7c1e-107">تختلف آلية الإعداد باختلاف اشتراكك وبيئتك.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="b7c1e-108">بالنسبة إلى المثيلات الجديدة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b7c1e-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b7c1e-109">إذا كان لديك ترخيص Microsoft Power Platform، فستحل على بيئة Common Data Service جديدة، إذا لم يكن لدى المستأجر بيئة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="b7c1e-110">بالنسبة إلى المثيلات الموجودة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="b7c1e-111">سيناريوهات الإعداد التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="b7c1e-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="b7c1e-112">مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="b7c1e-113">مثيل جديد لتطبيق Finance and Operations ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="b7c1e-114">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="b7c1e-115">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="b7c1e-116">مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="b7c1e-117">مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="b7c1e-118">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b7c1e-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b7c1e-119">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="b7c1e-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="b7c1e-120">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b7c1e-121">يتم تزويد مثيل جديد وفارغ من تطبيق يستند إلى نموذج، حيث تم تثبيت حل CRM الأساسي.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="b7c1e-122">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b7c1e-123">يتم تمكين خرائط الكيانات للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b7c1e-124">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="b7c1e-125">مثيل جديد لتطبيق Finance and Operations ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="b7c1e-126">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل موجود لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="b7c1e-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b7c1e-127">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="b7c1e-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="b7c1e-128">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b7c1e-129">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b7c1e-130">يتم تمكين خرائط الكيانات للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b7c1e-131">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="b7c1e-132">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b7c1e-133">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b7c1e-134">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b7c1e-135">[قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="b7c1e-136">لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="b7c1e-137">مثيل جديد لتطبيق Finance and Operations يتضمن بيانات عرض توضيحي ومثيل جديد لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="b7c1e-138">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل جديد لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج‬](#new-new) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="b7c1e-139">عند اكتمال إعداد الاتصال، إذا أردت مزامنة بيانات العرض التوضيحي مع التطبيق المستند إلى نموذج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="b7c1e-140">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b7c1e-141">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="b7c1e-142">مثيل جديد لتطبيق Finance and Operations يتضمن بيانات عرض توضيحي ومثيل موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="b7c1e-143">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات عرض توضيحي ومثيل موجود لتطبيق يستند إلى نموذج في Dynamics 365، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق مستند إلى نموذج‬](#new-existing) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="b7c1e-144">عند اكتمال إعداد الاتصال، إذا أردت مزامنة بيانات العرض التوضيحي مع التطبيق المستند إلى نموذج، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="b7c1e-145">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b7c1e-146">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للكيانات التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b7c1e-147">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b7c1e-148">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b7c1e-149">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b7c1e-150">[قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="b7c1e-151">لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="b7c1e-152">مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق مستند إلى نموذج</span><span class="sxs-lookup"><span data-stu-id="b7c1e-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="b7c1e-153">يحدث إعداد اتصال الكتابة المزدوجة بين مثيل موجود لتطبيق Finance and Operations ومثيل جديد أو موجود لتطبيق يستند إلى نموذج في Dynamics 365 في بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="b7c1e-154">قم بإعداد الاتصال من تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="b7c1e-155">لمزامنة بيانات Common Data Service الموجودة إلى تطبيق Finance and Operations، [قم بتمهيد](bootstrap-company-data.md) بيانات Common Data Service باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬</span><span class="sxs-lookup"><span data-stu-id="b7c1e-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="b7c1e-156">لأن الكتابة المزدوجة في وضع التزامن المباشر، يبدأ تدفق البيانات من Common Data Service إلى تطبيق Finance and Operations بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="b7c1e-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
