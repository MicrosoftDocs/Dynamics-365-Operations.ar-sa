---
title: تكوين كيانات Common Data Service الظاهرية
description: يوضح هذا الموضوع كيفيه تكوين الكيانات الظاهرية لـ Dynamics 365 Human Resources. إنشاء كيانات ظاهريه موجودة وتحديثها، وتحليل الكيانات التي تم إنشاؤها والمتاحة.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
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
ms.openlocfilehash: 0d6f79ea569a7a9b0d25e73e8666bf9ba19095d0
ms.sourcegitcommit: a8665c47696028d371cdc4671db1fd8fcf9e1088
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2020
ms.locfileid: "4058144"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="3f11c-104">تكوين كيانات Common Data Service الظاهرية</span><span class="sxs-lookup"><span data-stu-id="3f11c-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3f11c-105">Dynamics 365 Human Resources هو مصدر بيانات ظاهري في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="3f11c-106">وهو يوفر عمليات إنشاء وقراءه وتحديث وحذف (CRUD) كامله من Common Data Service وMicrosoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="3f11c-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="3f11c-107">لم يتم تخزين البيانات الخاصة بالكيانات الظاهرية في Common Data Service، ولكن في قاعده بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3f11c-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="3f11c-108">لتمكين عمليات CRUD علي كيانات الموارد البشرية من Common Data Service، يجب توفير الكيانات ككيانات ظاهريه في Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3f11c-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="3f11c-109">يتيح هذا امكانيه اجراء عمليات CRUD من Common Data Service وMicrosoft Power Platform علي البيانات الموجودة في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="3f11c-110">تدعم العمليات أيضا عمليات التحقق الكاملة من منطق العمل للموارد البشرية لضمان تكامل البيانات عند كتابه البيانات إلى الكيانات.</span><span class="sxs-lookup"><span data-stu-id="3f11c-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="3f11c-111">الكيانات الظاهرية المتاحة للموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3f11c-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="3f11c-112">تتوفر كافة كيانات بروتوكول البيانات المفتوحة (OData) في الموارد البشرية ككيانات ظاهريه في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="3f11c-113">وهي متوفرة أيضا في Power Platform.</span><span class="sxs-lookup"><span data-stu-id="3f11c-113">They're also available in Power Platform.</span></span> <span data-ttu-id="3f11c-114">يمكنك الآن إنشاء التطبيقات والخبرة بالبيانات مباشره من الموارد البشرية التي لها قدره CRUD كامله، دون نسخ البيانات أو مزامنتها إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="3f11c-115">يمكنك استخدام مداخل Power Apps لإنشاء مواقع ويب خارجيه تمكن سيناريوهات التعاون للعمليات التجارية في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="3f11c-116">يمكنك عرض قائمه بالكيانات الظاهرية الممكنة في البيئة، وبدء العمل مع الكيانات في [Power Apps](https://make.powerapps.com) في حل **كيانات HR الظاهرية لـ Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![كيانات HR الظاهرية لـ Dynamics 365 في Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="3f11c-118">الكيانات الظاهرية مقابل الكيانات الطبيعية</span><span class="sxs-lookup"><span data-stu-id="3f11c-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="3f11c-119">لا تكون الكيانات الظاهرية للموارد البشرية متماثلة مع كيانات Common Data Service الطبيعية التي تم إنشاؤها للموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="3f11c-120">يتم إنشاء الكيانات الطبيعية للموارد البشرية بشكل منفصل وصيانتها في الحل الشائع لـ HCM في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="3f11c-121">باستخدام الكيانات الطبيعية، يتم تخزين البيانات في Common Data Service وتتطلب مزامنة مع قاعده بيانات التطبيق الخاصة بالموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="3f11c-122">للحصول علي قائمه بكيانات Common Data Service الطبيعية للموارد البشرية، راجع [كيانات Common Data Service](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="3f11c-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="3f11c-123">الإعداد</span><span class="sxs-lookup"><span data-stu-id="3f11c-123">Setup</span></span>

<span data-ttu-id="3f11c-124">اتبع خطوات الاعداد هذه لتمكين الكيانات الظاهرية في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3f11c-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="3f11c-125">قم بتسجيل التطبيق في Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="3f11c-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="3f11c-126">أولا، يجب تسجيل التطبيق في مدخل Azure حتى يتمكن النظام الأساسي لهويه Microsoft من توفير خدمات المصادقة والتخويل للتطبيق والمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3f11c-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="3f11c-127">لمزيد من المعلومات حول تسجيل التطبيقات في Azure، راجع [التشغيل السريع: تسجيل تطبيق بواسطة النظام الأساسي لهويه Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="3f11c-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="3f11c-128">افتح [مدخل Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="3f11c-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="3f11c-129">في قائمة خدمات Azure، حدد **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="3f11c-130">حدد **تسجيل جديد**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-130">Select **New registration**.</span></span>

4. <span data-ttu-id="3f11c-131">في حقل **الاسم** ، أدخل اسمًا وصفيًا للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="3f11c-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="3f11c-132">علي سبيل المثال، **كيانات Dynamics 365 Human Resources الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="3f11c-133">في الحقل **أعاده توجيه URI** ، ادخل URL الخاص بمساحة الاسم لمثيل الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="3f11c-134">حدد **السجل**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-134">Select **Register**.</span></span>

7. <span data-ttu-id="3f11c-135">عند اكتمال التسجيل، يعرض مدخل Azure جزء **النظرة العامة** لتسجيل التطبيق الذي يتضمن **معرف التطبيق (العميل)**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="3f11c-136">سجل **معرف التطبيق (العميل)** في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="3f11c-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="3f11c-137">ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الوحدة الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="3f11c-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="3f11c-138">في جزء التنقل الأيمن، حدد **الشهادات والاسرار**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="3f11c-139">في القسم **أسرار العميل** في الصفحة، حدد **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="3f11c-140">قم بتوفير وصف، وحدد مده، وحدد **أضافه**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="3f11c-141">سجل قيمة السر.</span><span class="sxs-lookup"><span data-stu-id="3f11c-141">Record the secret's value.</span></span> <span data-ttu-id="3f11c-142">ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الوحدة الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="3f11c-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3f11c-143">تاكد من مراعاه قيمه السر في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="3f11c-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="3f11c-144">لا يتم عرض السر أبدا مره أخرى بعد مغادره هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f11c-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="3f11c-145">تثبيت تطبيق Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="3f11c-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="3f11c-146">قم بتثبيت تطبيق Dynamics 365 HR Virtual Entity في البيئة Power Apps الخاصة بك لنشر حزمه حلول الكيان الظاهري إلى Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="3f11c-147">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3f11c-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3f11c-148">في قائمه **البيئات** ، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3f11c-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="3f11c-149">في القسم **الموارد** في الصفحة، حدد **تطبيقات Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="3f11c-150">حدد اجراء **تثبيت التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="3f11c-151">حدد **Dynamics 365 HR Virtual Entity** ، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-151">Select **Dynamics 365 HR Virtual Entity** , and select **Next**.</span></span>

6. <span data-ttu-id="3f11c-152">مراجعه ووضع علامة علي الموافقة علي شروط الخدمة.</span><span class="sxs-lookup"><span data-stu-id="3f11c-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="3f11c-153">حدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-153">Select **Install**.</span></span>

<span data-ttu-id="3f11c-154">يستغرق التثبيت بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="3f11c-154">The install takes a few minutes.</span></span> <span data-ttu-id="3f11c-155">وعند الانتهاء، انتقل إلى الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-155">When it completes, continue to the next steps.</span></span>

![تثبيت تطبيق Dynamics 365 HR Virtual Entity من مركز اداره Power Platform](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="3f11c-157">تكوين مصدر بيانات الكيان الظاهري</span><span class="sxs-lookup"><span data-stu-id="3f11c-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="3f11c-158">الخطوة التالية هي تكوين مصدر البيانات الكيان الظاهري في بيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3f11c-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="3f11c-159">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3f11c-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="3f11c-160">في قائمه **البيئات** ، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3f11c-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="3f11c-161">حدد **عنوان URL للبيئة** في قسم **التفاصيل** من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f11c-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="3f11c-162">في **مركز حماية الحل** ، حدد الرمز **بحث متقدم** في الجزء العلوي الأيسر من صفحة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="3f11c-162">In the **Solution Health Hub** , select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="3f11c-163">في صفحه **بحث متقدم** ، وفي القائمة المنسدلة **البحث عن** ، حدد **تكوينات مصدر البيانات الظاهري Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="3f11c-164">حدد **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-164">Select **Results**.</span></span>

7. <span data-ttu-id="3f11c-165">حدد سجل **مصدر بيانات الموارد البشرية من Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="3f11c-166">ادخل المعلومات المطلوبة لتكوين مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="3f11c-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="3f11c-167">**URL الهدف** : عنوان URL لمساحة اسم الموارد البشرية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3f11c-167">**Target URL** : The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="3f11c-168">**معرف المستاجر** : معرف المستاجر في Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3f11c-168">**Tenant ID** : The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="3f11c-169">**معرف تطبيق AAD** : معرف التطبيق (العميل) الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f11c-169">**AAD Application ID** : The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="3f11c-170">لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="3f11c-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="3f11c-171">**سر تطبيق AAD** : سر التطبيق الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f11c-171">**AAD Application Secret** : The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="3f11c-172">لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="3f11c-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="3f11c-173">حدد **حفظ وإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-173">Select **Save & Close**.</span></span>

   ![مصدر بيانات الموارد البشرية في Microsoft](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="3f11c-175">منح أذونات التطبيق في الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="3f11c-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="3f11c-176">امنح أذونات لتطبيقي Azure AD في الموارد البشرية:</span><span class="sxs-lookup"><span data-stu-id="3f11c-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="3f11c-177">التطبيق الذي تم إنشاؤه للمستاجر في مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="3f11c-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="3f11c-178">تطبيق Dynamics 365 HR Virtual Entity الذي تم تبثبيته في من بيئة Power Apps</span><span class="sxs-lookup"><span data-stu-id="3f11c-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="3f11c-179">في الموارد البشرية، افتح صفحة **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="3f11c-180">حدد **جديد** لإنشاء سجل تطبيق جديد:</span><span class="sxs-lookup"><span data-stu-id="3f11c-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="3f11c-181">في الحقل **معرف العميل** ، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f11c-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="3f11c-182">في الحقل **معرف العميل** ، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f11c-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="3f11c-183">في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3f11c-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="3f11c-184">حدد **جديد** لإنشاء سجل تطبيق ثانٍ:</span><span class="sxs-lookup"><span data-stu-id="3f11c-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="3f11c-185">**معرف العميل** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="3f11c-185">**Client Id** : f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="3f11c-186">**الاسم** : Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="3f11c-186">**Name** : Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="3f11c-187">في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3f11c-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="3f11c-188">إنشاء كيانات ظاهرية</span><span class="sxs-lookup"><span data-stu-id="3f11c-188">Generate virtual entities</span></span>

<span data-ttu-id="3f11c-189">عند اكتمال الاعداد، يمكنك تحديد الكيانات الظاهرية التي ترغب في إنشائها وتمكينها في مثيل Common Data Service الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3f11c-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="3f11c-190">في Human Resources، افتح صفحة **تكامل Common Data Service (CDS)**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-190">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="3f11c-191">حدد علامة التبويب **الكيانات الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-191">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="3f11c-192">سيتم تعيين زر التبديل **تمكين الكيان الظاهري** إلى **نعم** تلقائيًا عندما تم إكمال كافة الإعدادات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3f11c-192">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="3f11c-193">إذا تم تعيين زر التبديل إلى **لا** ، فراجع الخطوات الموجودة في الأقسام السابقة من هذا المستند لضمان إكمال كافة إعدادات المتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-193">If the toggle is set to **No** , review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="3f11c-194">حدد الكيان أو الكيانات التي ترغب في إنشائها في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-194">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="3f11c-195">حدد **إنشاء/تحديث**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-195">Select **Generate/refresh**.</span></span>

![تكامل Common Data Service](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="3f11c-197">التحقق من حالة إنشاء الكيان</span><span class="sxs-lookup"><span data-stu-id="3f11c-197">Check entity generation status</span></span>

<span data-ttu-id="3f11c-198">يتم إنشاء الكيانات الظاهرية في Common Data Service خلال عملية خلفية غير متزامنة.</span><span class="sxs-lookup"><span data-stu-id="3f11c-198">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="3f11c-199">تعرض التحديثات على العملية في مركز الإجراء.</span><span class="sxs-lookup"><span data-stu-id="3f11c-199">Updates on the process display in the action center.</span></span> <span data-ttu-id="3f11c-200">تظهر التفاصيل الخاصة بالعملية، بما في ذلك سجلات الأخطاء، في الصفحة **التنفيذ التلقائي للعمليات**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-200">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="3f11c-201">في Human Resources، افتح الصفحة **التنفيذ التلقائي للعمليات**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-201">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="3f11c-202">حدد علامة التبويب **عمليات الخلفية**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-202">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="3f11c-203">حدد **عملية خلفية للتشغيل غير المتزامن لاستقصاء الكيان الظاهري**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-203">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="3f11c-204">حدد **عرض أحدث النتائج**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-204">Select **View most recent results**.</span></span>

<span data-ttu-id="3f11c-205">يعرض الجزء المنبثق للخارج أحدث نتائج التنفيذ للعملية.</span><span class="sxs-lookup"><span data-stu-id="3f11c-205">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="3f11c-206">يمكنك عرض السجل للعملية، بما في ذلك أية أخطاء تم إرجاعها من Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3f11c-206">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f11c-207">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="3f11c-207">See also</span></span>

[<span data-ttu-id="3f11c-208">ما هو Common Data Service؟</span><span class="sxs-lookup"><span data-stu-id="3f11c-208">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="3f11c-209">نظرة عامة على الكيان</span><span class="sxs-lookup"><span data-stu-id="3f11c-209">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="3f11c-210">نظره عامه علي علاقات الكيانات</span><span class="sxs-lookup"><span data-stu-id="3f11c-210">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="3f11c-211">إنشاء كيانات ظاهريه تحتوي علي بيانات من مصدر بيانات خارجي وتحريرها</span><span class="sxs-lookup"><span data-stu-id="3f11c-211">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="3f11c-212">ما المقصود بمداخل Power Apps؟</span><span class="sxs-lookup"><span data-stu-id="3f11c-212">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="3f11c-213">نظره عامه حول إنشاء التطبيقات في Power Apps</span><span class="sxs-lookup"><span data-stu-id="3f11c-213">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
