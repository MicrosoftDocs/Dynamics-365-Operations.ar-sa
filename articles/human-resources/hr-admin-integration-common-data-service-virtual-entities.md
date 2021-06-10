---
title: تكوين جداول Dataverse الظاهرية
description: يوضح هذا الموضوع كيفيه تكوين الجداول الظاهرية لـ Dynamics 365 Human Resources. قم إنشاء جداول ظاهريه موجودة وتحديثها، وتحليل الجداول التي تم إنشاؤها والمتاحة.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c2e207efe0eeec6fc7e679a6ae12edcb21b291f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058574"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="23eb7-104">تكوين جداول Dataverse الظاهرية</span><span class="sxs-lookup"><span data-stu-id="23eb7-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="23eb7-105">Dynamics 365 Human Resources هو مصدر بيانات ظاهري في Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="23eb7-106">وهو يوفر عمليات إنشاء وقراءه وتحديث وحذف (CRUD) كامله من Dataverse وMicrosoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="23eb7-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="23eb7-107">لا يتم تخزين البيانات الخاصة بالجداول الظاهرية في Dataverse، ولكن في قاعدة بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="23eb7-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="23eb7-108">لتمكين عمليات CRUD على كيانات الموارد البشرية من Dataverse، يجب توفير الكيانات كجداول ظاهرية في Dataverse</span><span class="sxs-lookup"><span data-stu-id="23eb7-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="23eb7-109">يتيح هذا امكانيه اجراء عمليات CRUD من Dataverse وMicrosoft Power Platform علي البيانات الموجودة في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="23eb7-110">تدعم العمليات أيضا عمليات التحقق الكاملة من منطق العمل للموارد البشرية لضمان تكامل البيانات عند كتابه البيانات إلى الكيانات.</span><span class="sxs-lookup"><span data-stu-id="23eb7-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="23eb7-111">تتوافق كيانات Human Resources مع جداول Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="23eb7-112">لمزيد من المعلومات حول Dataverse (المعروف في السابق باسم Common Data Service) وتحديثات المصطلحات، راجع [الجديد في Microsoft Dataverse؟](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="23eb7-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="23eb7-113">الجداول الظاهرية المتاحة للموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="23eb7-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="23eb7-114">تتوفر كافة كيانات بروتوكول البيانات المفتوحة (OData) في الموارد البشرية كجداول ظاهرية في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="23eb7-115">وهي متوفرة أيضا في Power Platform.</span><span class="sxs-lookup"><span data-stu-id="23eb7-115">They're also available in Power Platform.</span></span> <span data-ttu-id="23eb7-116">يمكنك الآن إنشاء التطبيقات والخبرة بالبيانات مباشره من الموارد البشرية التي لها قدره CRUD كامله، دون نسخ البيانات أو مزامنتها إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="23eb7-117">يمكنك استخدام مداخل Power Apps لإنشاء مواقع ويب خارجيه تمكن سيناريوهات التعاون للعمليات التجارية في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="23eb7-118">يمكنك عرض قائمة بالجداول الظاهرية الممكنة في البيئة، وبدء العمل مع الجداول في [Power Apps](https://make.powerapps.com) في حل **جداول HR الظاهرية لـ Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![جداول HR الظاهرية لـ Dynamics 365 في Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="23eb7-120">الجداول الظاهرية مقابل الجداول الأصلية</span><span class="sxs-lookup"><span data-stu-id="23eb7-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="23eb7-121">لا تكون الجداول الظاهرية للموارد البشرية متماثلة مع جداول Dataverse الأصلية التي تم إنشاؤها للموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="23eb7-122">يتم إنشاء الجداول الأصلية للموارد البشرية بشكل منفصل وصيانتها في الحل الشائع HCM في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="23eb7-123">باستخدام الجداول الأصلية، يتم تخزين البيانات في Dataverse وتتطلب مزامنة مع قاعدة بيانات التطبيق الخاصة بالموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="23eb7-124">للحصول على قائمة بجداول Dataverse الأصلية للموارد البشرية، راجع [جداول Dataverse](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="23eb7-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="23eb7-125">الإعداد</span><span class="sxs-lookup"><span data-stu-id="23eb7-125">Setup</span></span>

<span data-ttu-id="23eb7-126">اتبع خطوات الإعداد هذه لتمكين الجداول الظاهرية في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="23eb7-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="23eb7-127">تمكين الجداول الظاهرية في الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="23eb7-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="23eb7-128">أولاً، يجب عليك تمكين الجداول الظاهرية في مساحة عمل **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="23eb7-129">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="23eb7-130">حدد الإطار المتجانب **إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="23eb7-131">حدد **دعم الجدول الظاهري للموارد البشرية في Dataverse**، ثم حدد **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="23eb7-132">لمزيد من المعلومات حول تمكين الميزات وتعطيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="23eb7-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="23eb7-133">قم بتسجيل التطبيق في Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="23eb7-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="23eb7-134">يجب عليك تسجيل مثيل Human Resources الخاص بك في مدخل Azure حتى يتمكن النظام الأساسي لهويه Microsoft من توفير خدمات المصادقة والتخويل للتطبيق والمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="23eb7-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="23eb7-135">لمزيد من المعلومات حول تسجيل التطبيقات في Azure، راجع [التشغيل السريع: تسجيل تطبيق بواسطة النظام الأساسي لهويه Microsoft](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="23eb7-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="23eb7-136">افتح [مدخل Microsoft Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="23eb7-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="23eb7-137">في قائمة خدمات Azure، حدد **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="23eb7-138">حدد **تسجيل جديد**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-138">Select **New registration**.</span></span>

4. <span data-ttu-id="23eb7-139">في حقل **الاسم**، أدخل اسمًا وصفيًا للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="23eb7-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="23eb7-140">علي سبيل المثال، **جداول Dynamics 365 Human Resources الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="23eb7-141">في الحقل **أعاده توجيه URI**، ادخل URL الخاص بمساحة الاسم لمثيل الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="23eb7-142">حدد **السجل**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-142">Select **Register**.</span></span>

7. <span data-ttu-id="23eb7-143">عند اكتمال التسجيل، يعرض مدخل Azure جزء **النظرة العامة** لتسجيل التطبيق الذي يتضمن **معرف التطبيق (العميل)**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="23eb7-144">سجل **معرف التطبيق (العميل)** في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="23eb7-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="23eb7-145">ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الجدول الظاهري](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="23eb7-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="23eb7-146">في جزء التنقل الأيمن، حدد **الشهادات والاسرار**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="23eb7-147">في القسم **أسرار العميل** في الصفحة، حدد **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="23eb7-148">قم بتوفير وصف، وحدد مده، وحدد **أضافه**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="23eb7-149">تسجيل قيمة السر من خاصية **القيمة** للجدول.</span><span class="sxs-lookup"><span data-stu-id="23eb7-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="23eb7-150">ستقوم بإدخال هذه المعلومات عند [تكوين مصدر بيانات الجدول الظاهري](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="23eb7-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="23eb7-151">تاكد من مراعاه قيمه السر في هذا الوقت.</span><span class="sxs-lookup"><span data-stu-id="23eb7-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="23eb7-152">لا يتم عرض السر أبدا مره أخرى بعد مغادره هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="23eb7-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="23eb7-153">تثبيت تطبيق الجدول الظاهري Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="23eb7-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="23eb7-154">قم بتثبيت تطبيق الجدول الظاهري Dynamics 365 HR Virtual Table في البيئة Power Apps الخاصة بك لنشر حزمة حل الجدول الظاهري إلى Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="23eb7-155">في الموارد البشرية، افتح صفحة **تكامل Microsoft Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="23eb7-156">حدد علامة التبويب **الجداول الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="23eb7-157">حدد **تثبيت تطبيق الجدول الظاهري**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="23eb7-158">تكوين مصدر بيانات الجدول الظاهري</span><span class="sxs-lookup"><span data-stu-id="23eb7-158">Configure the virtual table data source</span></span>

<span data-ttu-id="23eb7-159">الخطوة التالية هي تكوين مصدر البيانات الجدول الظاهري في بيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="23eb7-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="23eb7-160">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="23eb7-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="23eb7-161">في قائمه **البيئات**، حدد بيئة Power Apps المقترنة بمثيل الموارد البشرية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="23eb7-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="23eb7-162">حدد **عنوان URL للبيئة** في قسم **التفاصيل** من الصفحة.</span><span class="sxs-lookup"><span data-stu-id="23eb7-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="23eb7-163">في **مركز حماية الحل**، حدد الرمز **بحث متقدم** في الجزء العلوي الأيسر من صفحة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="23eb7-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="23eb7-164">في صفحه **بحث متقدم**، وفي القائمة المنسدلة **البحث عن**، حدد **تكوينات مصدر البيانات الظاهري Finance and Operations**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="23eb7-165">قد يستغرق تثبيت تطبيق الجدول الظاهري من خطوة الإعداد السابقة بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="23eb7-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="23eb7-166">إذا لم تتوفر **تكوينات مصدر البيانات الظاهرية لـ Finance and Operations** في القائمة، انتظر لمدة دقيقة وقم بتحديث القائمة.</span><span class="sxs-lookup"><span data-stu-id="23eb7-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="23eb7-167">حدد **النتائج**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-167">Select **Results**.</span></span>

7. <span data-ttu-id="23eb7-168">حدد سجل **مصدر بيانات الموارد البشرية من Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="23eb7-169">أدخل المعلومات المطلوبة لتكوين مصدر البيانات:</span><span class="sxs-lookup"><span data-stu-id="23eb7-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="23eb7-170">**URL الهدف**: عنوان URL لمساحة اسم الموارد البشرية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="23eb7-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="23eb7-171">تنسيق عنوان URL الهدف هو:</span><span class="sxs-lookup"><span data-stu-id="23eb7-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="23eb7-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="23eb7-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="23eb7-173">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="23eb7-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="23eb7-174">تأكد من تضمين الحرف "**/**" في نهاية عنوان URL لتجنب تلقي خطأ ما.</span><span class="sxs-lookup"><span data-stu-id="23eb7-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="23eb7-175">**معرف المستأجر**: معرف المستأجر في Azure Active Directory ( Azure AD).</span><span class="sxs-lookup"><span data-stu-id="23eb7-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="23eb7-176">**معرف تطبيق AAD**: معرف التطبيق (العميل) الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23eb7-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="23eb7-177">لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="23eb7-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="23eb7-178">**سر تطبيق AAD**: سر التطبيق الذي تم إنشاؤه للتطبيق المسجل في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23eb7-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="23eb7-179">لقد تلقيت هذه المعلومات مبكرا اثناء الخطوة [تسجيل التطبيق في Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="23eb7-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![مصدر بيانات الموارد البشرية في Microsoft](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="23eb7-181">حدد **حفظ وإغلاق**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="23eb7-182">منح أذونات التطبيق في الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="23eb7-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="23eb7-183">امنح أذونات لتطبيقي Azure AD في الموارد البشرية:</span><span class="sxs-lookup"><span data-stu-id="23eb7-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="23eb7-184">التطبيق الذي تم إنشاؤه للمستأجر في مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="23eb7-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="23eb7-185">تطبيق Dynamics 365 HR Virtual Table الذي تم تبثبيته في من بيئة Power Apps</span><span class="sxs-lookup"><span data-stu-id="23eb7-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="23eb7-186">في الموارد البشرية، افتح صفحة **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="23eb7-187">حدد **جديد** لإنشاء سجل تطبيق جديد:</span><span class="sxs-lookup"><span data-stu-id="23eb7-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="23eb7-188">في الحقل **معرف العميل**، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23eb7-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="23eb7-189">في الحقل **معرف العميل**، ادخل معرف العميل الخاص بالتطبيق الذي قمت بتسجيله في مدخل Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="23eb7-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="23eb7-190">في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="23eb7-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="23eb7-191">حدد **جديد** لإنشاء سجل تطبيق ثانٍ:</span><span class="sxs-lookup"><span data-stu-id="23eb7-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="23eb7-192">**معرف العميل**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="23eb7-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="23eb7-193">**الاسم**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="23eb7-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="23eb7-194">في الحقل **معرف المستخدم** ، حدد معرف المستخدم الخاص بمستخدم لديه أذونات المسؤول في الموارد البشرية وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="23eb7-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="23eb7-195">إنشاء جداول ظاهرية</span><span class="sxs-lookup"><span data-stu-id="23eb7-195">Generate virtual tables</span></span>

<span data-ttu-id="23eb7-196">عند اكتمال الإعداد، يمكنك تحديد الجداول الظاهرية التي ترغب في إنشائها وتمكينها في مثيل Dataverse الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="23eb7-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="23eb7-197">في الموارد البشرية، افتح صفحة **تكامل Microsoft Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="23eb7-198">حدد علامة التبويب **الجداول الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="23eb7-199">سيتم تعيين زر التبديل **تمكين الجداول الظاهرية** إلى **نعم** تلقائيًا عند اكتمال كافة الإعدادات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="23eb7-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="23eb7-200">إذا تم تعيين زر التبديل إلى **لا**، فراجع الخطوات الموجودة في الأقسام السابقة من هذا المستند لضمان إكمال كافة إعدادات المتطلبات الأساسية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="23eb7-201">حدد الجدول أو الجداول التي ترغب في إنشائها في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="23eb7-202">حدد **إنشاء/تحديث**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-202">Select **Generate/refresh**.</span></span>

![تكامل Dataverse](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="23eb7-204">التحقق من حالة إنشاء الجدول</span><span class="sxs-lookup"><span data-stu-id="23eb7-204">Check table generation status</span></span>

<span data-ttu-id="23eb7-205">يتم إنشاء الجداول الظاهرية في Dataverse خلال عملية خلفية غير متزامنة.</span><span class="sxs-lookup"><span data-stu-id="23eb7-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="23eb7-206">تعرض التحديثات على العملية في مركز الإجراء.</span><span class="sxs-lookup"><span data-stu-id="23eb7-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="23eb7-207">تظهر التفاصيل الخاصة بالعملية، بما في ذلك سجلات الأخطاء، في الصفحة **التنفيذ التلقائي للعمليات**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="23eb7-208">في Human Resources، افتح الصفحة **التنفيذ التلقائي للعمليات**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="23eb7-209">حدد علامة التبويب **عمليات الخلفية**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="23eb7-210">حدد **عملية خلفية للتشغيل غير المتزامن لاستقصاء الجدول الظاهري**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="23eb7-211">حدد **عرض أحدث النتائج**.</span><span class="sxs-lookup"><span data-stu-id="23eb7-211">Select **View most recent results**.</span></span>

<span data-ttu-id="23eb7-212">يعرض الجزء المنبثق للخارج أحدث نتائج التنفيذ للعملية.</span><span class="sxs-lookup"><span data-stu-id="23eb7-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="23eb7-213">يمكنك عرض السجل للعملية، بما في ذلك أية أخطاء تم إرجاعها من Dataverse.</span><span class="sxs-lookup"><span data-stu-id="23eb7-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="23eb7-214">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="23eb7-214">See also</span></span>

[<span data-ttu-id="23eb7-215">ما هو Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="23eb7-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="23eb7-216">الجداول في Dataverse</span><span class="sxs-lookup"><span data-stu-id="23eb7-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="23eb7-217">نظرة عامة على علاقات الجداول</span><span class="sxs-lookup"><span data-stu-id="23eb7-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="23eb7-218">إنشاء جداول ظاهرية تحتوي على بيانات من مصدر بيانات خارجي وتحريرها</span><span class="sxs-lookup"><span data-stu-id="23eb7-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="23eb7-219">ما المقصود بمداخل Power Apps؟</span><span class="sxs-lookup"><span data-stu-id="23eb7-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="23eb7-220">نظره عامه حول إنشاء التطبيقات في Power Apps</span><span class="sxs-lookup"><span data-stu-id="23eb7-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
