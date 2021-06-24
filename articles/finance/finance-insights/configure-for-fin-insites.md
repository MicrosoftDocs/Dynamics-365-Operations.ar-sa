---
title: تكوين Finance Insights - الإصدارات حتى 10.0.19
description: يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights بالنسبة للإصدارات حتى 10.0.19.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186410"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="b60b6-103">تكوين Finance insights (معاينة)</span><span class="sxs-lookup"><span data-stu-id="b60b6-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="b60b6-104">تكون الإجراءات التالية لإعداد Finance insights صالحة لـ Microsoft Dynamics 365 Finance للإصدارات حتى 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="b60b6-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="b60b6-105">لإعداد Finance insights في الإصدار 10.0.20 والإصدارات اللاحقة، راجع [تكوين Finance insights (إصدار أولي) - الإصدارات 10.0.20 وما بعده](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="b60b6-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="b60b6-106">تضم Finance insights الوظيفة من Microsoft Dynamics 365 Finance مع Microsoft Dataverse وAzure و AI Builder لتوفير أدوات التنبؤ القوية لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="b60b6-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="b60b6-107">يشرح هذا الموضوع خطوات التكوين التي تتيح لنظامك إمكانية استخدام القدرات المتوفرة في Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="b60b6-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="b60b6-108">نشر Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b60b6-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="b60b6-109">نشر البيئات باتباع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="b60b6-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="b60b6-110">في Microsoft Dynamics Lifecycle Services (LCS)، قم بإنشاء أو تحديث بيئة Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b60b6-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="b60b6-111">تتطلب البيئة تحديث التطبيق النظام الأساسي 10.0.11 إلى الإصدار 35 أو أحدث.</span><span class="sxs-lookup"><span data-stu-id="b60b6-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="b60b6-112">يجب أن تكون البيئة بيئة عالية التوافر (HA) في وضع الحماية.</span><span class="sxs-lookup"><span data-stu-id="b60b6-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="b60b6-113">(يُعرف هذا النوع من البيئة أيضًا ببيئة الطبقة 2). لمزيد من المعلومات، راجع [تخطيط البيئة](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="b60b6-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="b60b6-114">إذا كنت تقوم بتكوين Finance insights في بيئة حماية، فقد تحتاج إلى نسخ بيانات الإنتاج إلى تلك البيئة لتوقعات العمل.</span><span class="sxs-lookup"><span data-stu-id="b60b6-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="b60b6-115">يستخدم نموذج التنبؤ سنوات متعددة من البيانات لبناء التوقعات.</span><span class="sxs-lookup"><span data-stu-id="b60b6-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="b60b6-116">لا تحتوي بيانات العرض التوضيحي لـ Contoso على بيانات تاريخية كافية للتدريب على نموذج التوقع بشكل ملائم.</span><span class="sxs-lookup"><span data-stu-id="b60b6-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="b60b6-117">تكوين Dataverse</span><span class="sxs-lookup"><span data-stu-id="b60b6-117">Configure Dataverse</span></span>

<span data-ttu-id="b60b6-118">استخدم الخطوات التالية لتكوين Dataverse لـ Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="b60b6-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="b60b6-119">افتح صفحة البيئة في LCS وتحقق من أن قسم **تكامل Power Platform** تم إعداده بالفعل.</span><span class="sxs-lookup"><span data-stu-id="b60b6-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="b60b6-120">في حالة إعداده بالفعل، يجب سرد اسم بيئة Dataverse المرتبط ببيئة Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b60b6-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="b60b6-121">انسخ اسم بيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b60b6-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="b60b6-122">في حالة عدم إعداده، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="b60b6-123">حدد زر **الإعداد** في قسم تكامل Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b60b6-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="b60b6-124">قد يستغرق إعداد البيئة ما يصل إلى ساعة.</span><span class="sxs-lookup"><span data-stu-id="b60b6-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="b60b6-125">في حالة إعداد بيئة Dataverse، يجب سرد اسم بيئة Dataverse ببيئة Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b60b6-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="b60b6-126">انسخ اسم بيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b60b6-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="b60b6-127">بعد إكمال إعداد البيئة، **لا** تحدد زر **الارتباط بـ CDS للتطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="b60b6-128">هذا ليس ضروريًا لـ Finance Insights وسيؤدي إلى تعطيل القدرة على إكمال الوظائف الإضافية للبيئة المطلوبة في LCS.</span><span class="sxs-lookup"><span data-stu-id="b60b6-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="b60b6-129">افتح مركز الإدارة [Power Platform ](https://admin.powerplatform.microsoft.com/)، واتبع هذه الخطوات لإنشاء بيئة Dataverse جديدة في مستأجر خدمة Active Directory نفسه.</span><span class="sxs-lookup"><span data-stu-id="b60b6-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="b60b6-130">افتح صفحة **البيئات**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="b60b6-131">[![صفحة البيئات](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="b60b6-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="b60b6-132">حدد بيئة Dataverse التي تم إنشاؤها أعلاه، ثم حدد **الإعدادات**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="b60b6-133">حدد **الموارد \> كافة الإعدادات القديمة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="b60b6-134">في شريط التنقل العلوي، حدد **الإعدادات**، ثم حدد **التخصيصات**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="b60b6-135">حدد **موارد المطور**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="b60b6-136">انسخ قيمة **معرف مؤسسة Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="b60b6-137">في شريط العنوان الخاص بالمستعرض، قم بتسجيل عنوان URL الخاص بمؤسسة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b60b6-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="b60b6-138">على سبيل المثال، قد يكون عنوان URL `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="b60b6-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="b60b6-139">إذا كنت تخطط لاستخدام ميزة تقديرات التدفقات النقدية أو التنبؤ بالموازنة، اتبع الخطوات التالية لتحديث حد التعليق التوضيحي لمؤسسك إلى 50 ميغابايت على الأقل (MB):</span><span class="sxs-lookup"><span data-stu-id="b60b6-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="b60b6-140">افتح [مدخل Power Apps](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="b60b6-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="b60b6-141">حدد البيئة التي قمت بإنشائها للتو، ثم حدد **الإعدادات المتقدمة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="b60b6-142">حدد **إعدادات \> تكوين البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="b60b6-143">قم بتغيير قيمة الحقل **الحد الأقصى حجم الملف** إلى **51.200**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="b60b6-144">(ويتم التعبير عن القيمة بالكيلو بايت \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="b60b6-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="b60b6-145">حدد **موافق** لحفظ التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b60b6-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="b60b6-146">تكوين إعداد Azure</span><span class="sxs-lookup"><span data-stu-id="b60b6-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="b60b6-147">أدخل معرف الدليل Dataverse ومعرف الكائن الخاص بمستخدم Azure AD</span><span class="sxs-lookup"><span data-stu-id="b60b6-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="b60b6-148">أدخل مُعرف الدليل Dataverse:</span><span class="sxs-lookup"><span data-stu-id="b60b6-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="b60b6-149">افتح [مدخل Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="b60b6-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="b60b6-150">قم بتسجيل الدخول باستخدام معرف المستخدم الذي تم استخدامه لإنشاء البيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b60b6-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="b60b6-151">الانتقال إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="b60b6-152">انسخ قيمة **معرف المستأجر**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="b60b6-153">أدخل معرف كائن Azure Active Directory (Azure AD):</span><span class="sxs-lookup"><span data-stu-id="b60b6-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="b60b6-154">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **المستخدمين**، وابحث عن المستخدم بعنوان البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="b60b6-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="b60b6-155">حدد اسم المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b60b6-155">Select the user's name.</span></span>
    3. <span data-ttu-id="b60b6-156">انسخ قيمة **معرف الكائن**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="b60b6-157">استخدام Azure Cloud Shell لإعداد موارد Finance insights Data Lake</span><span class="sxs-lookup"><span data-stu-id="b60b6-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="b60b6-158">استخدم البرنامج النصي لـ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b60b6-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="b60b6-159">لقد تم توفير برنامج Windows PowerShell النصي، حتى يمكنك بسهولة إعداد موارد Azure الموضحة في [تكوين التصدير إلى Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="b60b6-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="b60b6-160">إذا كنت تفضل القيام بالإعداد اليدوي، فعليك تخطي هذا الإجراء، ومتابعة الإجراء في القسم [الإعداد اليدوي](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="b60b6-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="b60b6-161">اتبع الخطوات التالية لتشغيل البرنامج النصي PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b60b6-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="b60b6-162">قد لا يعمل الخيار Azure CLI "جربه"، أو تشغيل البرنامج النصي على الكمبيوتر.</span><span class="sxs-lookup"><span data-stu-id="b60b6-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="b60b6-163">اتبع الخطوات التالية لتكوين Azure باستخدام البرنامج النصي لـ Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b60b6-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="b60b6-164">يجب أن يكون لديك حقوق بإنشاء مجموعة موارد Azure وموارد Azure وتطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b60b6-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="b60b6-165">للحصول على معلومات حول الأذونات المطلوبة، راجع [التحقق من أذونات Azure AD ](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="b60b6-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="b60b6-166">في [مدخل azure ](https://portal.azure.com)، انتقل إلى اشتراك هدف Azure.</span><span class="sxs-lookup"><span data-stu-id="b60b6-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="b60b6-167">حدد الزر **Cloud Shell** الموجود إلى يمين الحقل **بحث**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="b60b6-168">حدد **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="b60b6-169">قم بإنشاء تخزين، إذا تمت مطالبتك بالقيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="b60b6-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="b60b6-170">انتقل إلى علامة التبويب **Azure CLI** وحدد **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="b60b6-171">افتح المفكرة (Notepad) والصق برنامج PowerShell النصي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="b60b6-172">احفظ الملف باسم ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="b60b6-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="b60b6-173">قم بتحميل البرنامج النصي Windows PowerShell إلى الجلسة باستخدام خيار القائمة للتحميل في Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="b60b6-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="b60b6-174">قم بتشغيل البرنامج النصي .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="b60b6-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="b60b6-175">اتبع المطالبات لتشغيل البرنامج النصي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="b60b6-176">استخدم المعلومات من إخراج البرنامج النصي لتثبيت الوظيفة الإضافية **التصدير إلى Data Lake** في LCS.</span><span class="sxs-lookup"><span data-stu-id="b60b6-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="b60b6-177">استخدم المعلومات من إخراج البرنامج النصي لتمكين مخزن الكيان في الصفحة **اتصالات البيانات** في Finance (**إدارة النظام \> معلمات النظام \> اتصالات البيانات**).</span><span class="sxs-lookup"><span data-stu-id="b60b6-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="b60b6-178">إعداد يدوي</span><span class="sxs-lookup"><span data-stu-id="b60b6-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="b60b6-179">إضافة التطبيقات إلى المستأجر Azure AD</span><span class="sxs-lookup"><span data-stu-id="b60b6-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="b60b6-180">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="b60b6-181">حدد **إدارة \> تطبيقات Enterprise**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="b60b6-182">ابحث عن التطبيقات التالية حسب معرف التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b60b6-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="b60b6-183">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="b60b6-183">Application</span></span>                              | <span data-ttu-id="b60b6-184">معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="b60b6-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="b60b6-185">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="b60b6-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="b60b6-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="b60b6-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="b60b6-187">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="b60b6-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="b60b6-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="b60b6-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="b60b6-189">خدمة تخويل AI Builder</span><span class="sxs-lookup"><span data-stu-id="b60b6-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="b60b6-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="b60b6-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="b60b6-191">في حالة تعذر العثور على أي من التطبيقات السابقة، حاول القيام بالخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b60b6-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="b60b6-192">على جهازك المحلي، حدد القائمة **ابدأ**، وابحث عن **powershell**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="b60b6-193">حدد واستمر في الضغط (أو انقر بزر الماوس الأيمن) **Windows PowerShell**، ثم حدد **تشغيل كمسؤول**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="b60b6-194">قم بتشغيل الأمر التالي لتثبيت الوحدة النمطية **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="b60b6-195">إذا كان موفر NuGet مطلوبًا للمتابعة، حدد **Y** لتثبيته.</span><span class="sxs-lookup"><span data-stu-id="b60b6-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="b60b6-196">إذا ظهرت رسالة "مستودع غير موثوق به"، حدد **Y** للمتابعة.</span><span class="sxs-lookup"><span data-stu-id="b60b6-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="b60b6-197">بالنسبة لكل تطبيق يجب إضافته، قم بتشغيل الأوامر التالية لإضافة التطبيق إلى Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b60b6-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="b60b6-198">عند المطالبة، قم بتسجيل الدخول كمسؤول Azure AD.</span><span class="sxs-lookup"><span data-stu-id="b60b6-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="b60b6-199">إنشاء موارد Azure</span><span class="sxs-lookup"><span data-stu-id="b60b6-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="b60b6-200">تأكد من إنشاء الموارد التالية في مثيل Azure AD نفسه كبيئة Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b60b6-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="b60b6-201">لا يمكنك استخدام موارد من مثيل Azure AD مختلف.</span><span class="sxs-lookup"><span data-stu-id="b60b6-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="b60b6-202">قم بإنشاء حساب تخزين جديد:</span><span class="sxs-lookup"><span data-stu-id="b60b6-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="b60b6-203">في [مدخل Azure](https://portal.azure.com)، قم بحساب تخزين.</span><span class="sxs-lookup"><span data-stu-id="b60b6-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="b60b6-204">في مربع الحوار **إنشاء حساب تخزين**، قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="b60b6-205">**الموقع** – حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b60b6-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="b60b6-206">**الأداء** – إننا نوصي بأن تقوم بتحديد **قياسي**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="b60b6-207">**نوع الحساب** – يجب تحديد **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="b60b6-208">في مربع الحوار **خيارات متقدمة**، بالنسبة للخيار **Data Lake storage Gen2**، حدد **تمكين** ضمن ميزة **مساحات الأسماء الهرمية**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="b60b6-209">في حالة تعطيل هذه الميزة، فإنه لا يمكنك استهلاك البيانات التي يكتبها تطبيق Finance and Operations باستخدام خدمات مثل تدفقات بيانات Power BI.</span><span class="sxs-lookup"><span data-stu-id="b60b6-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="b60b6-210">حدد **مراجعة وإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-210">Select **Review and create**.</span></span> <span data-ttu-id="b60b6-211">عند اكتمال النشر، سيظهر المورد الجديد في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="b60b6-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="b60b6-212">انتقل إلى حساب التخزين الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="b60b6-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="b60b6-213">في القائمة اليمنى، حدد **مفاتيح الوصول**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="b60b6-214">قم بنسخ سلسلة الاتصال وحفظها إما إلى **Key1** أو **Key2**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="b60b6-215">قم بنسخ اسم حساب التخزين وحفظه.</span><span class="sxs-lookup"><span data-stu-id="b60b6-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="b60b6-216">إنشاء مخزن رئيسي جديد:</span><span class="sxs-lookup"><span data-stu-id="b60b6-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="b60b6-217">في [مدخل Azure](https://portal.azure.com)، قم إنشاء مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="b60b6-218">في مربع الحوار **إنشاء مخزن رئيسي**، في الحقل **الموقع**، حدد مركز البيانات الذي تقع فيه البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b60b6-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="b60b6-219">بعد إنشاء مخزن رئيسي، حدده في القائمة، ثم حدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="b60b6-220">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="b60b6-221">في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="b60b6-222">أدخل اسمًا للسر.</span><span class="sxs-lookup"><span data-stu-id="b60b6-222">Enter a name for the secret.</span></span> <span data-ttu-id="b60b6-223">قم بتدوين الاسم، لأنه سيتعين عليك توفيره لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="b60b6-224">في الحقل **القيمة**، أدخل سلسلة الاتصال التي حصلت عليها من حساب التخزين في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="b60b6-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="b60b6-225">حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b60b6-226">يتم إنشاء السر وإضافة إلى مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="b60b6-227">انتقل إلى **نظرة عامة حول مخزن رئيسي**، وقم بتدوين اسم DNS.</span><span class="sxs-lookup"><span data-stu-id="b60b6-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="b60b6-228">إنشاء وتسجيل تطبيق Azure AD:</span><span class="sxs-lookup"><span data-stu-id="b60b6-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="b60b6-229">في [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="b60b6-230">حدد **تسجيل تطبيق جديد**، ثم قم بتعيين الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="b60b6-231">**الاسم** - أدخل اسم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="b60b6-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="b60b6-232">**نوع التطبيق** – حدد **API للويب**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="b60b6-233">**إعادة توجيه إعداد عنوان URI** – أدخل عنوان URL لمثيل Dynamics 365 الخاص بك، مثل، `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="b60b6-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="b60b6-234">انتقل إلى التطبيق الذي قمت بإنشائه الآن، وقم بنسخ وحفظ قيمة **معرف تطبيق (عميل) الخاصة بالتطبيق**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="b60b6-235">سيتعين عليك توفير هذه القيمة لاحقًا، عند إعداد المخزن الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="b60b6-236">انتقل إلى **أذونات API**، واتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="b60b6-237">حدد **إضافة إذن**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="b60b6-238">حدد **مخزن Azure رئيسي**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="b60b6-239">بعد تحديد الأذونات المفوضة، حدد **user\_impersonation**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="b60b6-240">حدد **إضافة أذونات**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="b60b6-241">في القائمة الخاصة بالتطبيق، حدد **الشهادات \& الأسرار**، ثم اتبع الخطوات التالية لإنشاء أسرار المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="b60b6-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="b60b6-242">حدد **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="b60b6-243">في الحقل **الوصف الرئيسي**، أدخل اسمًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="b60b6-244">حدد مدة، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="b60b6-245">يتم إنشاء سر في الحفل **القيمة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="b60b6-246">قم بنسخ القيمة السرية وحفظها.</span><span class="sxs-lookup"><span data-stu-id="b60b6-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="b60b6-247">إنشاء أسرار المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="b60b6-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="b60b6-248">انتقل إلى المخزن الرئيسي الذي قمت بإنشائه سابقًا، وحدد **الأسرار**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="b60b6-249">بالنسبة لكل اسم سري في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b60b6-250">حدد **إنشاء/استيراد**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="b60b6-251">في مربع الحوار **إنشاء سر**، في الحقل **خيارات التحميل**، حدد **يدوي**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="b60b6-252">قم بإنشاء الاسم السري والقيمة من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="b60b6-253">حدد **ممكّن‬‬‏‫**، ثم حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="b60b6-254">يتم إنشاء السر وإضافة إلى مخزن رئيسي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="b60b6-255">اسم السر</span><span class="sxs-lookup"><span data-stu-id="b60b6-255">Secret name</span></span>                       | <span data-ttu-id="b60b6-256">قيمة سرية</span><span class="sxs-lookup"><span data-stu-id="b60b6-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="b60b6-257">معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="b60b6-257">app-id</span></span>                            | <span data-ttu-id="b60b6-258">معرف التطبيق الخاص بالتطبيق الذي قمت بإنشائه سابقًا</span><span class="sxs-lookup"><span data-stu-id="b60b6-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="b60b6-259">سر التطبيق</span><span class="sxs-lookup"><span data-stu-id="b60b6-259">app-secret</span></span>                        | <span data-ttu-id="b60b6-260">سر العميل الذي قمت بحفظه مسبقًا</span><span class="sxs-lookup"><span data-stu-id="b60b6-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="b60b6-261">اسم حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="b60b6-261">storage-account-name</span></span>              | <span data-ttu-id="b60b6-262">اسم حساب التخزين الذي قمت بإنشائه مسبقًا، مثل **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="b60b6-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="b60b6-263">التخزين-الحساب-الاتصال-السلسلة</span><span class="sxs-lookup"><span data-stu-id="b60b6-263">storage-account-connection-string</span></span> | <span data-ttu-id="b60b6-264">سلسلة الاتصال التي قمت بنسخها من الصفحة **مفاتيح الوصول** لحساب التخزين</span><span class="sxs-lookup"><span data-stu-id="b60b6-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="b60b6-265">تخويل التطبيق للوصول إلى المخزن الرئيسي:</span><span class="sxs-lookup"><span data-stu-id="b60b6-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="b60b6-266">في [مدخل Azure](https://portal.azure.com)، قم بفتح المخزن الرئيسي الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="b60b6-267">حدد نهج الوصول.</span><span class="sxs-lookup"><span data-stu-id="b60b6-267">Select the access policies.</span></span>
    3. <span data-ttu-id="b60b6-268">بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b60b6-269">حدد **إضافة نهج وصول** لإنشاء سياسة وصول.</span><span class="sxs-lookup"><span data-stu-id="b60b6-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="b60b6-270">في الحقل **الأذونات السرية**، حدد الأذونات من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="b60b6-271">في الحقل **تحديد الرئيسي**، ابحث عن اسم عرض التطبيق من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="b60b6-272">حدد **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-272">Select **Select**.</span></span>
        5. <span data-ttu-id="b60b6-273">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-273">Select **Add**.</span></span>
        6. <span data-ttu-id="b60b6-274">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-274">Select **Save**.</span></span>

        | <span data-ttu-id="b60b6-275">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="b60b6-275">Application</span></span>                                              | <span data-ttu-id="b60b6-276">الأذونات</span><span class="sxs-lookup"><span data-stu-id="b60b6-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="b60b6-277">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="b60b6-277">The display name of the new application that you created</span></span> | <span data-ttu-id="b60b6-278">الحصول على، قائمة</span><span class="sxs-lookup"><span data-stu-id="b60b6-278">Get, List</span></span>   |
        | <span data-ttu-id="b60b6-279">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="b60b6-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="b60b6-280">الحصول على، قائمة</span><span class="sxs-lookup"><span data-stu-id="b60b6-280">Get, List</span></span>   |

6. <span data-ttu-id="b60b6-281">قم بتعيين أدوار للوصول إلى حساب التخزين:</span><span class="sxs-lookup"><span data-stu-id="b60b6-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="b60b6-282">في [مدخل Azure](https://portal.azure.com)، قم بفتح حساب التخزين الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="b60b6-283">حدد **التحكم في الوصول (IAM)**، ثم حدد **مهمات الأدوار**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="b60b6-284">حدد **إضافة، أضف مهمة الدور**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="b60b6-285">بالنسبة لكل تطبيق في الجدول التالي، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="b60b6-286">حدد الدور من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="b60b6-287">اجعل الحقل **تعيين حق الوصول إلى** على مستخدم **Azure AD أو مجموعة أو كيان الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="b60b6-288">في الحقل **تحديد**، قم بالدخول إلى استمارة التقديم من الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="b60b6-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="b60b6-289">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-289">Select **Save**.</span></span>

        | <span data-ttu-id="b60b6-290">استمارة التقديم</span><span class="sxs-lookup"><span data-stu-id="b60b6-290">Application</span></span>                                              | <span data-ttu-id="b60b6-291">دور</span><span class="sxs-lookup"><span data-stu-id="b60b6-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="b60b6-292">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="b60b6-292">The display name of the new application that you created</span></span> | <span data-ttu-id="b60b6-293">المالك</span><span class="sxs-lookup"><span data-stu-id="b60b6-293">Owner</span></span>                       |
        | <span data-ttu-id="b60b6-294">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="b60b6-294">The display name of the new application that you created</span></span> | <span data-ttu-id="b60b6-295">المساهم</span><span class="sxs-lookup"><span data-stu-id="b60b6-295">Contributor</span></span>                 |
        | <span data-ttu-id="b60b6-296">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="b60b6-296">The display name of the new application that you created</span></span> | <span data-ttu-id="b60b6-297">المساهم في حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="b60b6-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="b60b6-298">اسم عرض التطبيق الجديد الذي قمت بإنشائه</span><span class="sxs-lookup"><span data-stu-id="b60b6-298">The display name of the new application that you created</span></span> | <span data-ttu-id="b60b6-299">مالك بيانات التخزين كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="b60b6-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="b60b6-300">**خدمة تخويل AI Builder**</span><span class="sxs-lookup"><span data-stu-id="b60b6-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="b60b6-301">قارئ بيانات التخزين كبيرة الحجم</span><span class="sxs-lookup"><span data-stu-id="b60b6-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="b60b6-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="b60b6-302">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="b60b6-303">تكوين data lake</span><span class="sxs-lookup"><span data-stu-id="b60b6-303">Configure the data lake</span></span>

<span data-ttu-id="b60b6-304">اتبع الخطوات التالية لاستخدام LCS لإضافة الوظيفة الإضافية Azure Data Lake add-in إلى البيئة.</span><span class="sxs-lookup"><span data-stu-id="b60b6-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="b60b6-305">قم بتسجيل الدخول إلى LCS، ثم، ضمن اسم البيئة على الجانب الأيسر من الصفحة، حدد **تفاصيل كاملة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="b60b6-306">في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="b60b6-307">حدد الوظيفة الإضافية، حدد **تصدير إلى Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="b60b6-308">أدخل القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b60b6-308">Enter the following values.</span></span>

    | <span data-ttu-id="b60b6-309">قيمة</span><span class="sxs-lookup"><span data-stu-id="b60b6-309">Value</span></span>                                                              | <span data-ttu-id="b60b6-310">الوصف</span><span class="sxs-lookup"><span data-stu-id="b60b6-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="b60b6-311">معرف المستأجر لاشتراك Azure حيث يوجد المخزن الرئيسي</span><span class="sxs-lookup"><span data-stu-id="b60b6-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="b60b6-312">يوجد معرف المستأجر الذي يوجد به حساب التخزين والتطبيقات والمخازن الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="b60b6-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="b60b6-313">للعثور على هذه القيمة، افتح [مدخل Azure](https://portal.azure.com)، انتقل إلى **Azure Active Directory**، ثم انسخ قيمة **معرف المستأجر**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="b60b6-314">توفير اسم DNS لـ Key Vault الخاص بك</span><span class="sxs-lookup"><span data-stu-id="b60b6-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="b60b6-315">اسم DNS للمخزن الرئيسي، مثل `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="b60b6-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="b60b6-316">(تتطابق هذه القيمة مع اسم DNS المستخدم في مخزن الكيان.)</span><span class="sxs-lookup"><span data-stu-id="b60b6-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="b60b6-317">توفير السر الذي يحتوي على اسم حساب التخزين</span><span class="sxs-lookup"><span data-stu-id="b60b6-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="b60b6-318">**اسم حساب التخزين**</span><span class="sxs-lookup"><span data-stu-id="b60b6-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="b60b6-319">اسم السر لمعرف التطبيق الذي سيتم استخدامه للوصول إلى Data Lake</span><span class="sxs-lookup"><span data-stu-id="b60b6-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="b60b6-320">**معرف التطبيق**</span><span class="sxs-lookup"><span data-stu-id="b60b6-320">**app-id**</span></span> |
    | <span data-ttu-id="b60b6-321">اسم السر الذي سيتم استخدامه مع معرف التطبيق</span><span class="sxs-lookup"><span data-stu-id="b60b6-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="b60b6-322">**سر التطبيق**</span><span class="sxs-lookup"><span data-stu-id="b60b6-322">**app-secret**</span></span> |

5. <span data-ttu-id="b60b6-323">وافق علي الشروط، وحدد **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="b60b6-324">سيتم تثبيت الوظيفة الإضافية خلال بضع دقائق.</span><span class="sxs-lookup"><span data-stu-id="b60b6-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="b60b6-325">تكوين AI Builder</span><span class="sxs-lookup"><span data-stu-id="b60b6-325">Configure AI Builder</span></span>

1. <span data-ttu-id="b60b6-326">قم بتسجيل الدخول إلى LCS، وافتح الصفحة **تفاصيل البيئة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="b60b6-327">قم بالتمرير إلى قسم **الوظائف الإضافية للبيئة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="b60b6-328">يجب أن ترى الوظائف الإضافية التي تم تثبيتها بالفعل في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="b60b6-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="b60b6-329">إذا لم تكن الوظيفة الإضافية **التصدير إلى Data Lake**، فقم بتكوين هذه الوظيفة الإضافية.</span><span class="sxs-lookup"><span data-stu-id="b60b6-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="b60b6-330">حدد الوظيفة الإضافية **Get insights**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="b60b6-331">من صفحة التفاصيل **Get insights**، أدخل القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="b60b6-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="b60b6-332">قيمة</span><span class="sxs-lookup"><span data-stu-id="b60b6-332">Value</span></span>                                                    | <span data-ttu-id="b60b6-333">الوصف</span><span class="sxs-lookup"><span data-stu-id="b60b6-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="b60b6-334">عنوان URL للمؤسسة CDS</span><span class="sxs-lookup"><span data-stu-id="b60b6-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="b60b6-335">تم نسخ عنوان URL لمؤسسة Dataverse مما سبق.</span><span class="sxs-lookup"><span data-stu-id="b60b6-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="b60b6-336">معرف مؤسسة CDS</span><span class="sxs-lookup"><span data-stu-id="b60b6-336">CDS Org ID</span></span>                                               | <span data-ttu-id="b60b6-337">تم نسخ معرف مؤسسة Dataverse مما سبق.</span><span class="sxs-lookup"><span data-stu-id="b60b6-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="b60b6-338">قم بتمكين **هل هذه هي البيئة الافتراضية بالنسبة للمستأجر لديك**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="b60b6-339">تكوين متجر الكيان</span><span class="sxs-lookup"><span data-stu-id="b60b6-339">Configure the entity store</span></span>

<span data-ttu-id="b60b6-340">اتبع هذه الخطوات لإعداد مخزن الكيان في بيئة Finance.</span><span class="sxs-lookup"><span data-stu-id="b60b6-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="b60b6-341">انتقل إلى **إدارة النظام \> إعداد \> معلمات النظام \> اتصالات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="b60b6-342">تعيين حقول المخزن الرئيسي التالية:</span><span class="sxs-lookup"><span data-stu-id="b60b6-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="b60b6-343">**معرف استمارة التطبيق (العميل)** – أدخل معرف عميل استمارة التقديم الذي قمت بإنشائه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="b60b6-344">**سر استمارة التقديم** – أدخل كلمة السر التي قمت بحفظها لاستمارة التقديم التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="b60b6-345">**اسم DNS** – يمكنك العثور على اسم نظام اسم المجال (DNS) في صفحة تفاصيل استمارة التقديم لاستمارة التطبيق التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b60b6-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="b60b6-346">**اسم السر** - أدخل **تخزين-حساب-اتصال-سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="b60b6-347">قم بتمكين **تمكين تكامل Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="b60b6-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="b60b6-348">حدد **اختبار Azure Key Vault** وتحقق من عدم وجود أي أخطاء.</span><span class="sxs-lookup"><span data-stu-id="b60b6-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="b60b6-349">حدد **اختبار تخزين Azure** وتحقق من عدم وجود أي أخطاء.</span><span class="sxs-lookup"><span data-stu-id="b60b6-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="b60b6-350">الملاحظات والدعم</span><span class="sxs-lookup"><span data-stu-id="b60b6-350">Feedback and support</span></span>

<span data-ttu-id="b60b6-351">الرجاء إرسال بريد الكتروني إلى [‏‫معلومات دفع العميل (معاينة) ](mailto:fiap@microsoft.com) إذا كنت مهتمًا بتقديم الملاحظات أو تحتاج إلى الدعم.</span><span class="sxs-lookup"><span data-stu-id="b60b6-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="b60b6-352">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="b60b6-352">Privacy notice</span></span>

<span data-ttu-id="b60b6-353">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="b60b6-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
