---
title: التكامل مع LinkedIn Talent Hub
description: يشرح هذا الموضوع كيفية إعداد التكامل بين Microsoft Dynamics 365 Human Resources وLinkedIn Talent Hub.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efcac2bd82956015eb822c6a493b8625a35cd194
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805048"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="a37d8-103">التكامل مع LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="a37d8-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a37d8-104">يُعد [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) هو النظام الأساسي لنظام تتبع مقدم التطبيق (ATS).</span><span class="sxs-lookup"><span data-stu-id="a37d8-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="a37d8-105">يتيح لك إمكانية البحث عن المرشحين وإدارتهم وتوظيفهم في مكان واحد.</span><span class="sxs-lookup"><span data-stu-id="a37d8-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="a37d8-106">ومن خلال تكامل Microsoft Dynamics 365 Human Resources مع LinkedIn Talent Hub، فإنه يمكنك بسهولة إنشاء سجلات الموظفين في Human Resources لمقدمي الطلبات الذين تم توظيفهم لأحد المناصب.</span><span class="sxs-lookup"><span data-stu-id="a37d8-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="a37d8-107">الإعداد</span><span class="sxs-lookup"><span data-stu-id="a37d8-107">Setup</span></span>

<span data-ttu-id="a37d8-108">يجب أن يقوم مسؤول النظام بإكمال مهام الإعداد لتمكين التكامل مع LinkedIn Talent Hub.</span><span class="sxs-lookup"><span data-stu-id="a37d8-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="a37d8-109">أولاً، في البيئة Power Apps، فإنه يجب عليك إعداد مستخدم ودور أمان لمنح LinkedIn Talent Hub الأذونات المناسبة لكتابة البيانات في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a37d8-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="a37d8-110">اربط بيئتك بـ LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="a37d8-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="a37d8-111">افتح [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="a37d8-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="a37d8-112">في القائمة المنسدلة الخاصة بالمستخدم، حدد **إعدادات المنتج**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="a37d8-113">في جزء التنقل الأيسر، في القسم **خيارات متقدمة**، حدد **عمليات التكامل**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="a37d8-114">حدد **تخويل** لتكامل Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a37d8-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="a37d8-115">في الصفحة **Dynamics 365 Human Resources**، حدد البيئة لربط LinkedIn Talent Hub بها، ثم حدد **ربط**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![إعداد LinkedIn Talent Hub](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="a37d8-117">يمكنك الربط فقط بالبيئات التي يملك فيها حساب المستخدم الخاص بك حق الوصول كمسؤول إلى كل من بيئة Human Resources وبيئة Power Apps المقترنة منه.</span><span class="sxs-lookup"><span data-stu-id="a37d8-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="a37d8-118">إذا لم يتم سرد أية بيئات في صفحة ارتباط Human Resources، فتأكد من أنك قد قمت بترخيص بيئات Human Resources على المستأجر، وأن المستخدم الذي قمت بتسجيل الدخول إلى صفحة الارتباط كما أن لديه أذونات مسؤول لكل من بيئة Human Resources وبيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a37d8-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="a37d8-119">إنشاء دور أمان Power Apps</span><span class="sxs-lookup"><span data-stu-id="a37d8-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="a37d8-120">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a37d8-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="a37d8-121">في القائمة **البيئات**، حدد البيئة المقترنة ببيئة Human Resources التي ترغب في ربط مثيل LinkedIn Talent Hub الخاص بك بها.</span><span class="sxs-lookup"><span data-stu-id="a37d8-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="a37d8-122">حدد **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-122">Select **Settings**.</span></span>

4. <span data-ttu-id="a37d8-123">قم بتوسيع العقدة **المستخدمون + الأذونات**، وحدد **أدوار الأمان**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="a37d8-124">في الصفحة **أدوار الأمان**، من شريط الأدوات، حدد **دور جديد**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="a37d8-125">في علامة التبويب **التفاصيل**، أدخل اسمًا للدور، مثل **LinkedIn Talent Hub HRIS Integration**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="a37d8-126">في علامة التبويب **تخصيص**، حدد إذن **القراءة** على مستوى المؤسسة للكيانات التالية:</span><span class="sxs-lookup"><span data-stu-id="a37d8-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="a37d8-127">الكيان</span><span class="sxs-lookup"><span data-stu-id="a37d8-127">Entity</span></span>
    - <span data-ttu-id="a37d8-128">الحقل</span><span class="sxs-lookup"><span data-stu-id="a37d8-128">Field</span></span>
    - <span data-ttu-id="a37d8-129">العلاقة</span><span class="sxs-lookup"><span data-stu-id="a37d8-129">Relationship</span></span>

8. <span data-ttu-id="a37d8-130">قم بحفظ دور الأمان وإغلاقه.</span><span class="sxs-lookup"><span data-stu-id="a37d8-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="a37d8-131">إنشاء مستخدم تطبيق Power Apps</span><span class="sxs-lookup"><span data-stu-id="a37d8-131">Create a Power Apps application user</span></span>

<span data-ttu-id="a37d8-132">يجب إنشاء مستخدم التطبيق لمحول LinkedIn Talent Hub لمنح الأذونات إلى المحول لكتابة سجلات الترشيح في البيئة Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a37d8-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="a37d8-133">افتح [مركز مسؤول Power Platform](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a37d8-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="a37d8-134">في القائمة **البيئات**، حدد البيئة المقترنة ببيئة Human Resources التي ترغب في ربط مثيل LinkedIn Talent Hub الخاص بك بها.</span><span class="sxs-lookup"><span data-stu-id="a37d8-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="a37d8-135">حدد **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-135">Select **Settings**.</span></span>

4. <span data-ttu-id="a37d8-136">قم بتوسيع العقدة **المستخدمون + الأذونات**، وحدد **المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="a37d8-137">حدد **إدارة المستخدمين في Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="a37d8-138">استخدم القائمة المنسدلة فوق القائمة لتغيير طريقة العرض من طريقة عرض **المستخدمين الممكنين** إلى **مستخدمي التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![طريقة عرض مستخدمي التطبيقات](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="a37d8-140">من شريط الأدوات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="a37d8-141">في صفحة **المستخدم الجديد‬**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="a37d8-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="a37d8-142">قم بتغيير قيمة الحقل **نوع المستخدم** إلى **مستخدم التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="a37d8-143">قم بتعيين الحقل **اسم المستخدم** إلى **تكامل Dynamics365 HR LinkedIn HRIS**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="a37d8-144">عيّن الحقل **معرف التطبيق** إلى **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="a37d8-145">أدخل أية قيمة في الحقول **الاسم الأول** و **الاسم الأخير** و **البريد الإلكتروني الأساسي**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="a37d8-146">في شريط الأدوات، حدد **حفظ \& إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="a37d8-147">تعيين دور أمان للمستخدم الجديد</span><span class="sxs-lookup"><span data-stu-id="a37d8-147">Assign a security role to the new user</span></span>

<span data-ttu-id="a37d8-148">بعد أن تقوم بحفظ مستخدم التطبيق الجديد وإغلاقه في القسم السابق، فإنه يتم إرجاعك إلى الصفحة **قائمة المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="a37d8-149">في الصفحة **قائمة المستخدمين**، قم بتغيير طريقة العرض إلى **مستخدمي التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="a37d8-150">حدد مستخدم التطبيق الذي قمت بإنشاؤه في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="a37d8-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="a37d8-151">في شريط الأدوات ، حدد **إدارة الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="a37d8-152">حدد دور الأمان الذي قمت بإنشاؤه سابقًا للتكامل.</span><span class="sxs-lookup"><span data-stu-id="a37d8-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="a37d8-153">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="a37d8-154">أضف تطبيق Azure Active Directory في Human Resources</span><span class="sxs-lookup"><span data-stu-id="a37d8-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="a37d8-155">في Dynamics 365 Human Resources، افتح صفحة **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="a37d8-156">أضف سجلاً جديدًا إلى القائمة، ثم قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="a37d8-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="a37d8-157">**معرف العميل**: أدخل **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="a37d8-158">**الاسم**: أدخل اسم دور أمان Power Apps الذي قمت بإنشائه مسبقًا، مثل **تكامل LinkedIn Talent Hub HRIS**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="a37d8-159">**معرف المستخدم**: حدد المستخدم الذي لديه الأذونات لكتابة البيانات في إدارة الموظفين.</span><span class="sxs-lookup"><span data-stu-id="a37d8-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="a37d8-160">إنشاء جدول في Dataverse</span><span class="sxs-lookup"><span data-stu-id="a37d8-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a37d8-161">يعتمد التكامل مع LinkedIn Talent Hub على الجداول الظاهرية في Dataverse لـ Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a37d8-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="a37d8-162">وكمتطلب أساسي لهذه الخطوة في الإعداد، يجب تكوين الجداول الظاهرية.</span><span class="sxs-lookup"><span data-stu-id="a37d8-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="a37d8-163">للحصول على معلومات عن كيفية تكوين الجداول الظاهرية، راجع [تكوين جداول Dataverse الظاهرية](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="a37d8-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="a37d8-164">في الموارد البشرية، افتح صفحة **تكامل Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="a37d8-165">حدد علامة التبويب **الجداول الظاهرية**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="a37d8-166">قم بتصفية قائمة الكيانات حسب تسمية الكيان للعثور على **المرشح الذي تم تصديره من LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="a37d8-167">حدد الكيان، ثم حدد **إنشاء/تحديث**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="a37d8-168">تصدير سجلات المرشحين</span><span class="sxs-lookup"><span data-stu-id="a37d8-168">Exporting candidate records</span></span>

<span data-ttu-id="a37d8-169">بعد اكتمال الإعداد، يمكن لمسؤولي التعيين ومحترفي الموارد البشرية (HR) استخدام الوظيفة **تصدير إلى HRIS** في LinkedIn Talent Hub لتصدير سجلات المرشحين من تم توظيفها LinkedIn Talent Hub إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a37d8-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="a37d8-170">تصدير السجلات من LinkedIn Talent Hub</span><span class="sxs-lookup"><span data-stu-id="a37d8-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="a37d8-171">بعد نقل المرشح خلال عملية التوظيف وتوظيفه، فإنه يمكنك تصدير سجل المرشح من LinkedIn Talent Hub إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a37d8-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="a37d8-172">في LinkedIn Talent Hub، افتح المشروع الذي قمت بتوظيف الموظف الجديد به.</span><span class="sxs-lookup"><span data-stu-id="a37d8-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="a37d8-173">حدد سجل مرشح.</span><span class="sxs-lookup"><span data-stu-id="a37d8-173">Select a candidate record.</span></span>

3. <span data-ttu-id="a37d8-174">حدد **تغيير المرحلة**، ثم حدد **تم التوظيف**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="a37d8-175">في قائمة علامة القطع (**...**) لمرشح، حدد **تصدير إلى HRIS**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="a37d8-176">في الجزء **تصدير إلى HRIS**، أدخل المعلومات التي يجب تصديرها:</span><span class="sxs-lookup"><span data-stu-id="a37d8-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="a37d8-177">في الحقل **موفر HRIS**، حدد **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="a37d8-178">في الحقل **تاريخ البدء**، حدد قيمة الموظف الجديد.</span><span class="sxs-lookup"><span data-stu-id="a37d8-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="a37d8-179">في الحقل **المسمى الوظيفي**، أدخل المسمى الوظيفي لوظيفة الموظف الجديد.</span><span class="sxs-lookup"><span data-stu-id="a37d8-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="a37d8-180">في الحقل **الموقع**، أدخل الموقع الذي سيتواجد به الموظف.</span><span class="sxs-lookup"><span data-stu-id="a37d8-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="a37d8-181">أدخل عنوان البريد الإلكتروني للموظف أو تحقق منه.</span><span class="sxs-lookup"><span data-stu-id="a37d8-181">Enter or verify the employee's email address.</span></span>

![التصدير إلى جزء HRIS في لوحة LinkedIn Talent Hub](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="a37d8-183">إكمال الإعداد في Human Resources</span><span class="sxs-lookup"><span data-stu-id="a37d8-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="a37d8-184">تظهر سجلات المرشحين التي يتم تصديرها من LinkedIn Talent Hub إلى Human Resources في القسم **‬‏‫المرشحون المُراد توظيفهم** في الصفحة **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="a37d8-185">في Human Resources، افتح الصفحة **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="a37d8-186">في المقطع **المرشحين المُراد توظيفهم**، حدد **توظيف** للمرشح المحدد.</span><span class="sxs-lookup"><span data-stu-id="a37d8-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="a37d8-187">في مربع الحوار **توظيف عامل جديد**، راجع السجل وأضف أية معلومات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a37d8-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="a37d8-188">يمكنك أيضًا تحديد رقم المنصب الذي تم توظيف المرشح به.</span><span class="sxs-lookup"><span data-stu-id="a37d8-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="a37d8-189">بعد إدخال المعلومات المطلوبة، يمكنك متابعة العمليات القياسية لإنشاء سجلات الموظفين وإعداد الموظفين.</span><span class="sxs-lookup"><span data-stu-id="a37d8-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="a37d8-190">يتم استيراد التفاصيل التالية وتضمينها في سجل الموظف الجديد:</span><span class="sxs-lookup"><span data-stu-id="a37d8-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="a37d8-191">الاسم الأول</span><span class="sxs-lookup"><span data-stu-id="a37d8-191">First name</span></span>
- <span data-ttu-id="a37d8-192">اسم العائلة</span><span class="sxs-lookup"><span data-stu-id="a37d8-192">Last name</span></span>
- <span data-ttu-id="a37d8-193">تاريخ بداية التوظيف</span><span class="sxs-lookup"><span data-stu-id="a37d8-193">Employment start date</span></span>
- <span data-ttu-id="a37d8-194">عنوان البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a37d8-194">Email address</span></span>
- <span data-ttu-id="a37d8-195">رقم الهاتف</span><span class="sxs-lookup"><span data-stu-id="a37d8-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="a37d8-196">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="a37d8-196">See also</span></span>

[<span data-ttu-id="a37d8-197">تكوين جداول Dataverse الظاهرية</span><span class="sxs-lookup"><span data-stu-id="a37d8-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="a37d8-198">ما هو Microsoft Dataverse؟</span><span class="sxs-lookup"><span data-stu-id="a37d8-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]