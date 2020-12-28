---
title: تكوين كيانات Common Data Service الظاهرية
description: يوضح هذا الموضوع كيفيه تكوين الكيانات الظاهرية لـ Dynamics 365 Human Resources. إنشاء كيانات ظاهريه موجودة وتحديثها، وتحليل الكيانات التي تم إنشاؤها والمتاحة.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645591"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="935ee-104">تكوين كيانات Common Data Service الظاهرية</span><span class="sxs-lookup"><span data-stu-id="935ee-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="935ee-105">Dynamics 365 Human Resources هو مصدر بيانات ظاهري في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="935ee-106">وهو يوفر عمليات إنشاء وقراءه وتحديث وحذف (CRUD) كامله من Common Data Service وMicrosoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="935ee-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="935ee-107">لم يتم تخزين البيانات الخاصة بالكيانات الظاهرية في Common Data Service، ولكن في قاعده بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="935ee-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="935ee-108">لتمكين عمليات CRUD علي كيانات الموارد البشرية من Common Data Service، يجب توفير الكيانات ككيانات ظاهريه في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="935ee-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="935ee-109">يتيح هذا امكانيه اجراء عمليات CRUD من Common Data Service وMicrosoft Power Platform علي البيانات الموجودة في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="935ee-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="935ee-110">تدعم العمليات أيضا عمليات التحقق الكاملة من منطق العمل للموارد البشرية لضمان تكامل البيانات عند كتابه البيانات إلى الكيانات.</span><span class="sxs-lookup"><span data-stu-id="935ee-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="935ee-111">الكيانات الظاهرية المتاحة للموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="935ee-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="935ee-112">تتوفر كافة كيانات بروتوكول البيانات المفتوحة (OData) في الموارد البشرية ككيانات ظاهريه في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="935ee-113">وهي متوفرة أيضا في Power Platform.</span><span class="sxs-lookup"><span data-stu-id="935ee-113">They're also available in Power Platform.</span></span> <span data-ttu-id="935ee-114">يمكنك الآن إنشاء التطبيقات والخبرة بالبيانات مباشره من الموارد البشرية التي لها قدره CRUD كامله، دون نسخ البيانات أو مزامنتها إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="935ee-115">يمكنك استخدام مداخل Power Apps لإنشاء مواقع ويب خارجيه تمكن سيناريوهات التعاون للعمليات التجارية في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="935ee-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="935ee-116">يمكنك عرض قائمه بالكيانات الظاهرية الممكنة في البيئة، وبدء العمل مع الكيانات في [Power Apps](https://make.powerapps.com) في حل **كيانات HR الظاهرية لـ Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="935ee-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![كيانات HR الظاهرية لـ Dynamics 365 في Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="935ee-118">الكيانات الظاهرية مقابل الكيانات الطبيعية</span><span class="sxs-lookup"><span data-stu-id="935ee-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="935ee-119">لا تكون الكيانات الظاهرية للموارد البشرية متماثلة مع كيانات Common Data Service الطبيعية التي تم إنشاؤها للموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="935ee-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="935ee-120">يتم إنشاء الكيانات الطبيعية للموارد البشرية بشكل منفصل وصيانتها في الحل الشائع لـ HCM في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="935ee-121">باستخدام الكيانات الطبيعية، يتم تخزين البيانات في Common Data Service وتتطلب مزامنة مع قاعده بيانات التطبيق الخاصة بالموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="935ee-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="935ee-122">للحصول علي قائمه بكيانات Common Data Service الطبيعية للموارد البشرية، راجع [كيانات Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="935ee-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="935ee-123">الإعداد</span><span class="sxs-lookup"><span data-stu-id="935ee-123">Setup</span></span>

<span data-ttu-id="935ee-124">اتبع خطوات الاعداد هذه لتمكين الكيانات الظاهرية في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="935ee-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="935ee-125">تمكين الكيانات الظاهرية في Human Resources</span><span class="sxs-lookup"><span data-stu-id="935ee-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="935ee-126">أولاً، يجب عليك تمكين الكيانات الظاهرية في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="935ee-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="935ee-127">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="935ee-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="935ee-128">حدد الإطار المتجانب **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="935ee-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="935ee-129">حدد **دعم الكيان الظاهري في HR/CDS**، ثم حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="935ee-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="935ee-130">لمزيد من المعلومات حول تمكين الميزات وتعطيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="935ee-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="935ee-131">قم بتسجيل التطبيق في Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="935ee-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="935ee-132">يجب عليك تسجيل مثيل Human Resources الخاص بك في مدخل Azure حتى يتمكن النظام الأساسي لهويه Microsoft من توفير خدمات المصادقة والتخويل للتطبيق والمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="935ee-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="935ee-133">لمزيد من المعلومات حول تسجيل التطبيقات في Azure، راجع [التشغيل السريع: تسجيل تطبيق بواسطة النظام الأساسي لهويه Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="935ee-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="935ee-134">افتح [مدخل Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="935ee-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="935ee-135">في قائمة خدمات Azure، حدد **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="935ee-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="935ee-136">حدد **تسجيل جديد**.</span><span class="sxs-lookup"><span data-stu-id="935ee-136">Select **New registration**.</span></span>

4. <span data-ttu-id="935ee-137">في حقل **الاسم**، أدخل اسمًا وصفيًا للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="935ee-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="935ee-138">علي سبيل المثال، **كيانات Dynamics 365 Human Resources الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="935ee-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="935ee-139">في الحقل **أعاده توجيه URI**، ادخل URL الخاص بمساحة الاسم لمثيل الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="935ee-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="935ee-140">حدد **السجل**.</span><span class="sxs-lookup"><span data-stu-id="935ee-140">Select **Register**.</span></span>

7. <span data-ttu-id="935ee-141">عند اكتمال التسجيل، يعرض مدخل Azure جزء **النظرة العامة** لتسجيل التطبيق الذي يتضمن **معرف التطبيق (العميل)**.</span><span class="sxs-lookup"><span data-stu-id="935ee-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="935ee-142">سجل **معرف التطبيق (العميل)** في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="935ee-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="935ee-143">ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الوحدة الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="935ee-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="935ee-144">في جزء التنقل الأيمن، حدد **الشهادات والاسرار**.</span><span class="sxs-lookup"><span data-stu-id="935ee-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="935ee-145">في القسم **أسرار العميل** في الصفحة، حدد **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="935ee-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="935ee-146">قم بتوفير وصف، وحدد مده، وحدد **أضافه**.</span><span class="sxs-lookup"><span data-stu-id="935ee-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="935ee-147">سجل قيمة السر.</span><span class="sxs-lookup"><span data-stu-id="935ee-147">Record the secret's value.</span></span> <span data-ttu-id="935ee-148">ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الوحدة الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="935ee-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="935ee-149">تاكد من مراعاه قيمه السر في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="935ee-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="935ee-150">لا يتم عرض السر أبدا مره أخرى بعد مغادره هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="935ee-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="935ee-151">تثبيت تطبيق Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="935ee-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="935ee-152">قم بتثبيت تطبيق Dynamics 365 HR Virtual Entity في البيئة Power Apps الخاصة بك لنشر حزمه حلول الكيان الظاهري إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="935ee-153">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="935ee-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="935ee-154">في قائمه **البيئات**، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="935ee-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="935ee-155">في القسم **الموارد** في الصفحة، حدد **تطبيقات Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="935ee-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="935ee-156">حدد اجراء **تثبيت التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="935ee-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="935ee-157">حدد **Dynamics 365 HR Virtual Entity**، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="935ee-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="935ee-158">مراجعه ووضع علامة علي الموافقة علي شروط الخدمة.</span><span class="sxs-lookup"><span data-stu-id="935ee-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="935ee-159">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="935ee-159">Select **Install**.</span></span>

<span data-ttu-id="935ee-160">يستغرق التثبيت بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="935ee-160">The install takes a few minutes.</span></span> <span data-ttu-id="935ee-161">وعند الانتهاء، انتقل إلى الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="935ee-161">When it completes, continue to the next steps.</span></span>

![تثبيت تطبيق Dynamics 365 HR Virtual Entity من مركز اداره Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="935ee-163">تكوين مصدر بيانات الكيان الظاهري</span><span class="sxs-lookup"><span data-stu-id="935ee-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="935ee-164">الخطوة التالية هي تكوين مصدر البيانات الكيان الظاهري في بيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="935ee-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="935ee-165">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="935ee-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="935ee-166">في قائمه **البيئات**، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="935ee-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="935ee-167">حدد **عنوان URL للبيئة** في قسم **التفاصيل** من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="935ee-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="935ee-168">في **مركز حماية الحل**، حدد الرمز **بحث متقدم** في الجزء العلوي الأيسر من صفحة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="935ee-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="935ee-169">في صفحه **بحث متقدم**، وفي القائمة المنسدلة **البحث عن**، حدد **تكوينات مصدر البيانات الظاهري Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="935ee-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="935ee-170">حدد **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="935ee-170">Select **Results**.</span></span>

7. <span data-ttu-id="935ee-171">حدد سجل **مصدر بيانات الموارد البشرية من Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="935ee-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="935ee-172">أدخل المعلومات المطلوبة لتكوين مصدر البيانات:</span><span class="sxs-lookup"><span data-stu-id="935ee-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="935ee-173">**URL الهدف**: عنوان URL لمساحة اسم الموارد البشرية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="935ee-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="935ee-174">تنسيق عنوان URL الهدف هو:</span><span class="sxs-lookup"><span data-stu-id="935ee-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="935ee-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="935ee-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="935ee-176">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="935ee-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="935ee-177">تأكد من تضمين الحرف "**/**" في نهاية عنوان URL لتجنب تلقي خطأ ما.</span><span class="sxs-lookup"><span data-stu-id="935ee-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="935ee-178">**معرف المستاجر**: معرف المستاجر في Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="935ee-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="935ee-179">**معرف تطبيق AAD**: معرف التطبيق (العميل) الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="935ee-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="935ee-180">لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="935ee-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="935ee-181">**سر تطبيق AAD**: سر التطبيق الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="935ee-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="935ee-182">لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="935ee-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![مصدر بيانات الموارد البشرية في Microsoft](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="935ee-184">حدد **حفظ وإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="935ee-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="935ee-185">منح أذونات التطبيق في الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="935ee-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="935ee-186">امنح أذونات لتطبيقي Azure AD في الموارد البشرية:</span><span class="sxs-lookup"><span data-stu-id="935ee-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="935ee-187">التطبيق الذي تم إنشاؤه للمستاجر في مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="935ee-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="935ee-188">تطبيق Dynamics 365 HR Virtual Entity الذي تم تبثبيته في من بيئة Power Apps</span><span class="sxs-lookup"><span data-stu-id="935ee-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="935ee-189">في الموارد البشرية، افتح صفحة **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="935ee-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="935ee-190">حدد **جديد** لإنشاء سجل تطبيق جديد:</span><span class="sxs-lookup"><span data-stu-id="935ee-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="935ee-191">في الحقل **معرف العميل**، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="935ee-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="935ee-192">في الحقل **معرف العميل**، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="935ee-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="935ee-193">في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="935ee-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="935ee-194">حدد **جديد** لإنشاء سجل تطبيق ثانٍ:</span><span class="sxs-lookup"><span data-stu-id="935ee-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="935ee-195">**معرف العميل**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="935ee-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="935ee-196">**الاسم**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="935ee-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="935ee-197">في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="935ee-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="935ee-198">إنشاء كيانات ظاهرية</span><span class="sxs-lookup"><span data-stu-id="935ee-198">Generate virtual entities</span></span>

<span data-ttu-id="935ee-199">عند اكتمال الاعداد، يمكنك تحديد الكيانات الظاهرية التي ترغب في إنشائها وتمكينها في مثيل Common Data Service الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="935ee-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="935ee-200">في Human Resources، افتح صفحة **تكامل Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="935ee-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="935ee-201">حدد علامة التبويب **الكيانات الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="935ee-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="935ee-202">سيتم تعيين زر التبديل **تمكين الكيان الظاهري** إلى **نعم** تلقائيًا عندما تم إكمال كافة الإعدادات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="935ee-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="935ee-203">إذا تم تعيين زر التبديل إلى **لا**، فراجع الخطوات الموجودة في الأقسام السابقة من هذا المستند لضمان إكمال كافة إعدادات المتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="935ee-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="935ee-204">حدد الكيان أو الكيانات التي ترغب في إنشائها في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="935ee-205">حدد **إنشاء/تحديث**.</span><span class="sxs-lookup"><span data-stu-id="935ee-205">Select **Generate/refresh**.</span></span>

![تكامل Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="935ee-207">التحقق من حالة إنشاء الكيان</span><span class="sxs-lookup"><span data-stu-id="935ee-207">Check entity generation status</span></span>

<span data-ttu-id="935ee-208">يتم إنشاء الكيانات الظاهرية في Common Data Service خلال عملية خلفية غير متزامنة.</span><span class="sxs-lookup"><span data-stu-id="935ee-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="935ee-209">تعرض التحديثات على العملية في مركز الإجراء.</span><span class="sxs-lookup"><span data-stu-id="935ee-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="935ee-210">تظهر التفاصيل الخاصة بالعملية، بما في ذلك سجلات الأخطاء، في الصفحة **التنفيذ التلقائي للعمليات**.</span><span class="sxs-lookup"><span data-stu-id="935ee-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="935ee-211">في Human Resources، افتح الصفحة **التنفيذ التلقائي للعمليات**.</span><span class="sxs-lookup"><span data-stu-id="935ee-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="935ee-212">حدد علامة التبويب **عمليات الخلفية**.</span><span class="sxs-lookup"><span data-stu-id="935ee-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="935ee-213">حدد **عملية خلفية للتشغيل غير المتزامن لاستقصاء الكيان الظاهري**.</span><span class="sxs-lookup"><span data-stu-id="935ee-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="935ee-214">حدد **عرض أحدث النتائج**.</span><span class="sxs-lookup"><span data-stu-id="935ee-214">Select **View most recent results**.</span></span>

<span data-ttu-id="935ee-215">يعرض الجزء المنبثق للخارج أحدث نتائج التنفيذ للعملية.</span><span class="sxs-lookup"><span data-stu-id="935ee-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="935ee-216">يمكنك عرض السجل للعملية، بما في ذلك أية أخطاء تم إرجاعها من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="935ee-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="935ee-217">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="935ee-217">See also</span></span>

[<span data-ttu-id="935ee-218">ما هو Common Data Service؟</span><span class="sxs-lookup"><span data-stu-id="935ee-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="935ee-219">نظرة عامة على الكيان</span><span class="sxs-lookup"><span data-stu-id="935ee-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="935ee-220">نظره عامه علي علاقات الكيانات</span><span class="sxs-lookup"><span data-stu-id="935ee-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="935ee-221">إنشاء كيانات ظاهريه تحتوي علي بيانات من مصدر بيانات خارجي وتحريرها</span><span class="sxs-lookup"><span data-stu-id="935ee-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="935ee-222">ما المقصود بمداخل Power Apps؟</span><span class="sxs-lookup"><span data-stu-id="935ee-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="935ee-223">نظره عامه حول إنشاء التطبيقات في Power Apps</span><span class="sxs-lookup"><span data-stu-id="935ee-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
