---
title: إرشادات حول إعداد الكتابة المزدوجة
description: يصف هذا الموضوع السيناريوهات المدعومة لإعداد الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 999b37970be1c10fd5e78c3d8ac6c1fb25cad367
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751376"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="95a7a-103">إرشادات حول إعداد الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="95a7a-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="95a7a-104">يمكنك إعداد اتصال الكتابة المزدوجة بين بيئة Finance and Operations وبيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="95a7a-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="95a7a-105">توفر **بيئة Finance and Operations** النظام الاساسي **لتطبيقات Finance and Operations** (على سبيل المثال Microsoft Dynamics 365 Finance وDynamics 365 Supply Chain Management وDynamics 365 Commerce وDynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="95a7a-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="95a7a-106">توفر **بيئة Dataverse** النظام الأساسي **لتطبيقات customer engagement** ‏(Dynamics 365 Sales وDynamics 365 Customer Service وDynamics 365 column Service وDynamics 365 Marketing وDynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="95a7a-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95a7a-107">تدعم وحدة Human Resources في Dynamics 365 Finance  اتصالات الكتابة المزدوجة، ولكن لا يدعمها تطبيق Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="95a7a-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="95a7a-108">تختلف آلية الإعداد باختلاف اشتراكك وبيئتك:</span><span class="sxs-lookup"><span data-stu-id="95a7a-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="95a7a-109">بالنسبة إلى المثيلات الجديدة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="95a7a-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="95a7a-110">إذا كان لديك ترخيص Microsoft Power Platform، فستحل على بيئة Dataverse جديدة، إذا لم يكن لدى المستأجر بيئة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="95a7a-111">بالنسبة إلى المثيلات الموجودة لتطبيقات Finance and Operations، يبدأ إعداد اتصال الكتابة المزدوجة في بيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95a7a-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="95a7a-112">قبل بدء الكتابة الثنائية لكيان ما، يمكنك تشغيل مزامنة أولية لمعالجة البيانات الموجودة على الجانبين: تطبيقات Finance and Operations وتطبيقات Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="95a7a-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="95a7a-113">يمكنك تخطي المزامنة الأولية إذا لم تكن بحاجة إلى مزامنة البيانات بين البيئتين.</span><span class="sxs-lookup"><span data-stu-id="95a7a-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="95a7a-114">تتيح المزامنة الأولية إمكانية نسخ البيانات الموجودة من تطبيق واحد إلى آخر بشكل ثنائي الاتجاه.</span><span class="sxs-lookup"><span data-stu-id="95a7a-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="95a7a-115">هناك العديد من سيناريوهات الإعداد، بناءً على البيئات التي لديك بالفعل ونوع البيانات الموجودة فيها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="95a7a-116">سيناريوهات الإعداد التالية مدعومة:</span><span class="sxs-lookup"><span data-stu-id="95a7a-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="95a7a-117">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="95a7a-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="95a7a-118">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="95a7a-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="95a7a-119">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل جديد لتطبيق customer engagement</span><span class="sxs-lookup"><span data-stu-id="95a7a-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="95a7a-120">مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل موجود لتطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="95a7a-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="95a7a-121">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="95a7a-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="95a7a-122">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="95a7a-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="95a7a-123">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="95a7a-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="95a7a-124">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق customer engagement، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="95a7a-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="95a7a-125">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="95a7a-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="95a7a-126">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="95a7a-127">يتم تزويد مثيل جديد وفارغ من تطبيق customer engagement، حيث تم تثبيت حل CRM الأساسي.</span><span class="sxs-lookup"><span data-stu-id="95a7a-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="95a7a-128">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="95a7a-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="95a7a-129">يتم تمكين خرائط الجداول للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="95a7a-130">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="95a7a-131">مثيل تطبيق Finance and Operations جديد ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="95a7a-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="95a7a-132">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations لا يحتوي على بيانات ومثيل جديد لتطبيق customer engagement حالي، اتبع الخطوات الموجودة في [إعداد الكتابة المزدوجة من Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="95a7a-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="95a7a-133">عند اكتمال إعداد الاتصال، تحدث الإجراءات التالية بشكل تلقائي:</span><span class="sxs-lookup"><span data-stu-id="95a7a-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="95a7a-134">يتم تزويد بيئة Finance and Operations جديدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="95a7a-135">يتم إنشاء اتصال الكتابة المزدوجة لبيانات شركة DAT.</span><span class="sxs-lookup"><span data-stu-id="95a7a-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="95a7a-136">يتم تمكين خرائط الجداول للمزامنة المباشرة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="95a7a-137">عندئذٍ، تصبح البيئتين جاهزتين لمزامنة البيانات المباشرة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="95a7a-138">لمزامنة بيانات Dataverse الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="95a7a-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="95a7a-139">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95a7a-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="95a7a-140">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="95a7a-141">[قم بتمهيد](bootstrap-company-data.md) بيانات Dataverse باستخدام كود شركة المنظمة العالمية للمواصفات المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="95a7a-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="95a7a-142">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95a7a-143">للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="95a7a-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="95a7a-144">مثيل تطبيق Finance and Operations جديد ويحتوي على بيانات ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="95a7a-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="95a7a-145">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل جديد لتطبيق customer engagement، اتبع الخطوات الموجودة في [مثيل جديد لتطبيق Finance and Operations ومثيل جديد لتطبيق customer engagement‬](#new-new) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="95a7a-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="95a7a-146">عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="95a7a-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="95a7a-147">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="95a7a-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="95a7a-148">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95a7a-149">للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="95a7a-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="95a7a-150">مثيل تطبيق Finance and Operations جديد يحتوي على بيانات ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="95a7a-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="95a7a-151">لإعداد اتصال الكتابة المزدوجة بين مثيل جديد لتطبيق Finance and Operations يحتوي على بيانات ومثيل حالي لتطبيق customer engagement، اتبع الخطوات الموجودة في [مثيل لتطبيق Finance and Operations ومثيل حالي لتطبيق customer engagement‬](#new-existing) في قسم سابق من هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="95a7a-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="95a7a-152">عند اكتمال إعداد الاتصال، إذا أردت مزامنة البيانات مع التطبيق customer engagement، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="95a7a-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="95a7a-153">افتح تطبيق Finance and Operations من صفحة LCS، وسجل دخولك، ثم انتقل إلى **إدارة البيانات \> الكتابة المزدوجة**.</span><span class="sxs-lookup"><span data-stu-id="95a7a-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="95a7a-154">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95a7a-155">لمزامنة بيانات Dataverse الموجودة إلى تطبيق Finance and Operations، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="95a7a-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="95a7a-156">أنشئ شركة جديدة في تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="95a7a-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="95a7a-157">أضف الشركة إلى إعداد اتصال الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="95a7a-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="95a7a-158">[قم بتمهيد](bootstrap-company-data.md) بيانات Dataverse باستخدام كود شركة ISO المكون من ثلاثة أحرف.</span><span class="sxs-lookup"><span data-stu-id="95a7a-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="95a7a-159">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95a7a-160">للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="95a7a-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="95a7a-161">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement جديد</span><span class="sxs-lookup"><span data-stu-id="95a7a-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="95a7a-162">يحدث إعداد اتصال الكتابة المزدوجة بين مثيل حالي لتطبيق Finance and Operations ومثيل جديد لتطبيق customer engagement في بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="95a7a-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="95a7a-163">[قم بإعداد الاتصال من تطبيق Finance and Operations ](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="95a7a-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="95a7a-164">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95a7a-165">للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="95a7a-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="95a7a-166">مثيل تطبيق Finance and Operations حالي ومثيل تطبيق customer engagement حالي</span><span class="sxs-lookup"><span data-stu-id="95a7a-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="95a7a-167">يحدث إعداد اتصال الكتابة المزدوجة بين مثيل حالي لتطبيق Finance and Operations ومثيل حالي لتطبيق customer engagement في بيئة Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="95a7a-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="95a7a-168">[قم بإعداد الاتصال من تطبيق Finance and Operations ](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="95a7a-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="95a7a-169">لمزامنة بيانات Dataverse الموجودة إلى تطبيق Finance and Operations، [قم بتمهيد](bootstrap-company-data.md) بيانات Dataverse باستخدام كود شركة ISO المكون من ثلاثة أحرف.‬</span><span class="sxs-lookup"><span data-stu-id="95a7a-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="95a7a-170">قم بتشغيل وظيفة‏‎ **المزامنة الأولية** للجداول التي ترغب في مزامنة بياناتها.</span><span class="sxs-lookup"><span data-stu-id="95a7a-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="95a7a-171">للحصول على روابط لمثال وطريقة بديلة، راجع قسم [المثال](#example).</span><span class="sxs-lookup"><span data-stu-id="95a7a-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="95a7a-172">مثال</span><span class="sxs-lookup"><span data-stu-id="95a7a-172">Example</span></span>

<span data-ttu-id="95a7a-173">على سبيل المثال، راجع [تمكين Customers الإصدار 3—تعيين جدول جهات الاتصال](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="95a7a-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="95a7a-174">للحصول على أسلوب بديل يستند إلى وحدات تخزين البيانات في كل كيان التي يجب تشغيل المزامنة الأولية بها، راجع [اعتبارات المزامنة الأولية](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="95a7a-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]