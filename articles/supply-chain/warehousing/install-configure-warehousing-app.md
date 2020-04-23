---
title: نظرة عامة على تثبيت وتكوين تطبيق التخزين
description: يصف هذا الموضوع كيفية تثبيت وتكوين Dynamics 365 for Finance and Operations - تطبيق التخزين.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52882ef7542bfedebdae4a08de8404cddd01ed55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205588"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a><span data-ttu-id="75ee7-103">نظرة عامة على تثبيت وتكوين تطبيق التخزين</span><span class="sxs-lookup"><span data-stu-id="75ee7-103">Install and configure the Warehousing app overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> <span data-ttu-id="75ee7-104">يوضح هذا الموضوع كيفية تكوين التخزين لعمليات توزيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="75ee7-104">This topic describes how to configure warehousing for cloud deployments.</span></span> <span data-ttu-id="75ee7-105">إذا كنت تبحث عن كيفية تكوين التخزين لعمليات التوزيع المحلي، فيُرجى مراجعة [التخزين لعمليات التوزيع المحلية](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="75ee7-105">If you are looking for how to configure warehousing for on-premises deployments, please see [Warehousing for on-premises deployments](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).</span></span>


<span data-ttu-id="75ee7-106">يصف هذا الموضوع كيفية تثبيت وتكوين Dynamics 365 for Finance and Operations - تطبيق التخزين.</span><span class="sxs-lookup"><span data-stu-id="75ee7-106">This topic describes how to install and configure Dynamics 365 for Finance and Operations – Warehousing app.</span></span>

<span data-ttu-id="75ee7-107">يتوفر تطبيق التخزين في متجر Google Play وMicrosoft Store.</span><span class="sxs-lookup"><span data-stu-id="75ee7-107">Warehousing app is available on Google Play Store and Windows Store.</span></span> <span data-ttu-id="75ee7-108">بالنسبة إلى الإصدار الحالي من Dynamics 365 Supply Chain Management، يتوفر هذا التطبيق كمكون مستقل، مما يعني النشر الذاتي على الأجهزة المستخدمة لمهام المستودع.</span><span class="sxs-lookup"><span data-stu-id="75ee7-108">For the current version of Dynamics 365 Supply Chain Management, this app is provided as a standalone component, which means self-deployment on devices used for warehouse tasks.</span></span> <span data-ttu-id="75ee7-109">لاستخدام التطبيق، يجب تنزيل التطبيق على كل جهاز وتكوينه للاتصال ببيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="75ee7-109">In order to use the app, you must download the app on each device and configure it to connect to your Supply Chain Management environment.</span></span> <span data-ttu-id="75ee7-110">يصف هذا الموضوع كيفية تثبيت التطبيق على الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="75ee7-110">This topic describes how to install the app on your devices.</span></span> <span data-ttu-id="75ee7-111">وهو يوضح أيضًا كيفية تكوين التطبيق للاتصال ببيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="75ee7-111">It also explains how to configure the app to connect to your Supply Chain Management environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75ee7-112">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="75ee7-112">Prerequisites</span></span>
<span data-ttu-id="75ee7-113">يتوفر التطبيق على أنظمة تشغيل Android وWindows.</span><span class="sxs-lookup"><span data-stu-id="75ee7-113">The app is available on Android and Windows operating systems.</span></span> <span data-ttu-id="75ee7-114">لاستخدام هذا التطبيق، يجب أن يكون أحد أنظمة التشغيل التالية المعتمدة مثبتة على أجهزتك.</span><span class="sxs-lookup"><span data-stu-id="75ee7-114">To use this app, you must have one of the following supported operating systems installed on your devices.</span></span> <span data-ttu-id="75ee7-115">يجب أن يتوفر لديك أحد الإصدارات التالية المعتمدة.</span><span class="sxs-lookup"><span data-stu-id="75ee7-115">You must also have one of the following supported versions.</span></span> <span data-ttu-id="75ee7-116">استخدم المعلومات في الجدول التالي لتقييم جهوزية بيئة الأجهزة والبرامج لديك لدعم عملية التثبيت.</span><span class="sxs-lookup"><span data-stu-id="75ee7-116">Use the information in the following table to evaluate if your hardware and software environment is ready to support the installation.</span></span>

| <span data-ttu-id="75ee7-117">النظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="75ee7-117">Platform</span></span>                    | <span data-ttu-id="75ee7-118">الإصدار</span><span class="sxs-lookup"><span data-stu-id="75ee7-118">Version</span></span>                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ee7-119">Android</span><span class="sxs-lookup"><span data-stu-id="75ee7-119">Android</span></span>                     | <span data-ttu-id="75ee7-120">4.4، 5.0، 6.0، 7.0، 8.0، 9.0</span><span class="sxs-lookup"><span data-stu-id="75ee7-120">4.4, 5.0, 6.0, 7.0, 8.0, 9.0</span></span>                                                                                                                                                     |
| <span data-ttu-id="75ee7-121">Windows ‏(UWP)</span><span class="sxs-lookup"><span data-stu-id="75ee7-121">Windows (UWP)</span></span>               | <span data-ttu-id="75ee7-122">Windows 10 (كل الإصدارات)</span><span class="sxs-lookup"><span data-stu-id="75ee7-122">Windows 10 (all versions)</span></span>                                                                                                                                                   |
| <span data-ttu-id="75ee7-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75ee7-123">Finance and Operations</span></span> | <span data-ttu-id="75ee7-124">الإصدار 1611 من Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="75ee7-124">Microsoft Dynamics 365 for Operations, version 1611</span></span> <br><span data-ttu-id="75ee7-125">-أو -</span><span class="sxs-lookup"><span data-stu-id="75ee7-125">-or-</span></span> <br><span data-ttu-id="75ee7-126">الإصدار 7.0/7.0.1 من Microsoft Dynamics AX وMicrosoft Dynamics AX platform update 2 مع الإصلاح العاجل KB 3210014</span><span class="sxs-lookup"><span data-stu-id="75ee7-126">Microsoft Dynamics AX version 7.0/7.0.1 and Microsoft Dynamics AX platform update 2 with hotfix KB 3210014</span></span> |

## <a name="get-the-app"></a><span data-ttu-id="75ee7-127">الحصول على التطبيق</span><span class="sxs-lookup"><span data-stu-id="75ee7-127">Get the app</span></span>
-   <span data-ttu-id="75ee7-128">Windows ‏(UWP)</span><span class="sxs-lookup"><span data-stu-id="75ee7-128">Windows (UWP)</span></span>
     - [<span data-ttu-id="75ee7-129">Finance and Operations - التخزين في متجر Windows</span><span class="sxs-lookup"><span data-stu-id="75ee7-129">Finance and Operations - Warehousing on the Windows Store</span></span>](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   <span data-ttu-id="75ee7-130">Android</span><span class="sxs-lookup"><span data-stu-id="75ee7-130">Android</span></span>
    - [<span data-ttu-id="75ee7-131">Finance and Operations - التخزين في Google Play Store</span><span class="sxs-lookup"><span data-stu-id="75ee7-131">Finance and Operations - Warehousing on the Google Play Store</span></span>](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> <span data-ttu-id="75ee7-132">تم إيقاف Zebra App Gallery عن العمل، مما يعني أن تطبيق التخزين لن يعود متوفرًا لتنزيله من هذا الموقع.</span><span class="sxs-lookup"><span data-stu-id="75ee7-132">The Zebra App Gallery has been retired, which means that the Warehousing app will no longer be available for download from that location.</span></span>

## <a name="create-a-web-service-application-in-azure-active-directory"></a><span data-ttu-id="75ee7-133">إنشاء تطبيق خدمة ويب في Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="75ee7-133">Create a web service application in Azure Active Directory</span></span>
<span data-ttu-id="75ee7-134">لتمكين التطبيق من التفاعل مع خادم Supply Chain Management معين، يجب عليك تسجيل تطبيق خدمة ويب في Azure Active Directory لمستأجر Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="75ee7-134">To enable the app to interact with a specific Supply Chain Management server, you must register a web service application in an Azure Active Directory for the Supply Chain Management tenant.</span></span> <span data-ttu-id="75ee7-135">لأسباب تتعلق بالأمان، نوصي بإنشاء تطبيق خدمة ويب لكل جهاز تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="75ee7-135">For security reasons, we recommend that you create a web service application for each device that you use.</span></span> <span data-ttu-id="75ee7-136">لإنشاء تطبيق خدمة ويب في Azure Active Directory (Azure AD)، أكمل الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="75ee7-136">To create a web service application in Azure Active Directory (Azure AD), complete the following steps:</span></span>

1.  <span data-ttu-id="75ee7-137">في مستعرض ويب، انتقل إلى <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="75ee7-137">In a web browser, go to <https://portal.azure.com>.</span></span>
2.  <span data-ttu-id="75ee7-138">أدخل اسم المستخدم وكلمة المرور لمستخدم له حق الوصول إلى اشتراك Azure.</span><span class="sxs-lookup"><span data-stu-id="75ee7-138">Enter the name and password for the user who has access to the Azure subscription.</span></span>
3.  <span data-ttu-id="75ee7-139">في مدخل Azure، في جزء التنقل الأيمن، انقر فوق **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-139">In Azure Portal, in the left navigation pane, click **Azure Active Directory**.</span></span>

    <span data-ttu-id="75ee7-140">[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-140">[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)</span></span>

4.  <span data-ttu-id="75ee7-141">تأكد من أن مثيل Active Directory هو المثيل الذي يتم استخدامه بواسطة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="75ee7-141">Ensure that the Active Directory instance is the one that is used by Supply Chain Management.</span></span>
5.  <span data-ttu-id="75ee7-142">في القائمة، انقر فوق **عمليات تسجيل التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-142">In the list, click **App registrations**.</span></span> 

    <span data-ttu-id="75ee7-143">[![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-143">[![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)</span></span>

6.  <span data-ttu-id="75ee7-144">في الجزء العلوي، انقر فوق **تسجيل جديد**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-144">In the top pane, click **New registration**.</span></span> <span data-ttu-id="75ee7-145">يبدأ تشغيل **معالج تسجيل تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-145">The **Register an application wizard** starts.</span></span>
7.  <span data-ttu-id="75ee7-146">ادخل اسمًا للتطبيق وحدد **حسابات في هذا الدليل التنظيمي فقط**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-146">Enter a name for the application and select **Accounts in this organizational directory only**.</span></span> <span data-ttu-id="75ee7-147">انقر فوق **تسجيل**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-147">Click **Register**.</span></span>  

    <span data-ttu-id="75ee7-148">[![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-148">[![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)</span></span>

8.  <span data-ttu-id="75ee7-149">يفتح تسجيل التطبيق الجديد.</span><span class="sxs-lookup"><span data-stu-id="75ee7-149">Your new app registration will open.</span></span> 

    <span data-ttu-id="75ee7-150">[![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-150">[![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)</span></span>

9.  <span data-ttu-id="75ee7-151">تذكر **"معرف تطبيق"**، أنك ستحتاجه فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="75ee7-151">Remember the **Application ID**, you will need it later.</span></span> <span data-ttu-id="75ee7-152">ستتم الإشارة إلى **معرف التطبيق** لاحقًا باعتباره **معرف العميل**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-152">The **Application ID** will later be referred to as the **Client ID**.</span></span>
10. <span data-ttu-id="75ee7-153">انقر فوق **الشهادة والأسرار** في الجزء **إدارة**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-153">Click **Certificate & secrets** in the **Manage** pane.</span></span> <span data-ttu-id="75ee7-154">انقر فوق **سر عميل جديد**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-154">Click on **New client secret**.</span></span> 

    <span data-ttu-id="75ee7-155">[![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-155">[![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)</span></span>

11. <span data-ttu-id="75ee7-156">أنشئ مفتاحًا عن طريق إدخال وصف مفتاح وفترة زمنية في قسم **كلمات المرور**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-156">Create a key by entering a key description and a duration in the **Passwords** section.</span></span> <span data-ttu-id="75ee7-157">انقر فوق **إضافة** وانسخ المفتاح.</span><span class="sxs-lookup"><span data-stu-id="75ee7-157">Click **Add** and copy the key.</span></span> <span data-ttu-id="75ee7-158">سيُشار إلى هذا المفتاح لاحقًا على أنه **سر العميل**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-158">This key will later be referred to as the **Client secret**.</span></span> 

    <span data-ttu-id="75ee7-159">[![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-159">[![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)</span></span>

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><span data-ttu-id="75ee7-160">إنشاء وتكوين حساب مستخدم في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="75ee7-160">Create and configure a user account in Supply Chain Management</span></span>
<span data-ttu-id="75ee7-161">لتمكين Supply Chain Management لاستخدام تطبيق Azure AD، تحتاج إلى إكمال خطوات التكوين التالية:</span><span class="sxs-lookup"><span data-stu-id="75ee7-161">To enable Supply Chain Managementto use your Azure AD application, you need to complete the following configuration steps:</span></span>

1.  <span data-ttu-id="75ee7-162">أنشئ مستخدمًا يتطابق مع بيانات اعتماد مستخدم تطبيق التخزين.</span><span class="sxs-lookup"><span data-stu-id="75ee7-162">Create a user that corresponds to the warehousing app user credentials.</span></span>
    1.  <span data-ttu-id="75ee7-163">انتقل إلى **إدارة النظام** &gt; **عام** &gt; **المستخدمون**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-163">Go to **System administration** &gt; **Common** &gt; **Users**.</span></span>
    2.  <span data-ttu-id="75ee7-164">أنشئ مستخدمًا جديدًا.</span><span class="sxs-lookup"><span data-stu-id="75ee7-164">Create a new user.</span></span>
    3.  <span data-ttu-id="75ee7-165">عيّن مستخدم الجهاز المحمول للمستودع‬، كما هو موضح في لقطة الشاشة التالية.</span><span class="sxs-lookup"><span data-stu-id="75ee7-165">Assign the Warehouse mobile device user, as shown in the following screenshot.</span></span> 
    
        <span data-ttu-id="75ee7-166">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-166">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span></span>

2.  <span data-ttu-id="75ee7-167">قم بإقران تطبيق Azure Active Directory بمستخدم تطبيق التخزين.</span><span class="sxs-lookup"><span data-stu-id="75ee7-167">Associate your Azure Active Directory application with the warehousing app user.</span></span>
    1.  <span data-ttu-id="75ee7-168">في Supply Chain Management، انتقل إلى **إدارة النظام** &gt; **الإعداد‏‎** &gt; **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-168">In Supply Chain Management, go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
    2.  <span data-ttu-id="75ee7-169">قم بإنشاء بند جديد.</span><span class="sxs-lookup"><span data-stu-id="75ee7-169">Create a new line.</span></span>
    3.  <span data-ttu-id="75ee7-170">أدخل **"معرف العميل"** (الذي تم الحصول عليه في القسم الأخير)، وأدخل اسمًا له، وحدد المستخدم الذي أنشأته في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="75ee7-170">Enter the **Client ID** (obtained in the last section), give it a name, and select the previously created user.</span></span> <span data-ttu-id="75ee7-171">نوصي بتمييز كل أجهزتك بحيث يمكنك أن تزيل بسهولة حق وصولها إلى Supply Chain Management من هذه الصفحة في حال فقدانها.</span><span class="sxs-lookup"><span data-stu-id="75ee7-171">We recommend that you tag all your devices so that you can easily remove their access to Supply Chain Management from this page in case they are lost.</span></span> 
    
        <span data-ttu-id="75ee7-172">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-172">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span></span>

## <a name="configure-the-application"></a><span data-ttu-id="75ee7-173">تكوين التطبيق</span><span class="sxs-lookup"><span data-stu-id="75ee7-173">Configure the application</span></span>
<span data-ttu-id="75ee7-174">يجب عليك تكوين التطبيق على الجهاز للاتصال بخادم Supply Chain Management من خلال تطبيق Azure AD.</span><span class="sxs-lookup"><span data-stu-id="75ee7-174">You must configure the app on the device to connect to the Supply Chain Management server through the Azure AD application.</span></span> <span data-ttu-id="75ee7-175">ولإجراء ذلك، أكمل الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="75ee7-175">To do this, complete the following steps.</span></span>

1.  <span data-ttu-id="75ee7-176">في التطبيق، انتقل إلى **إعدادات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-176">In the app, go to **Connection settings**.</span></span>
2.  <span data-ttu-id="75ee7-177">انقر فوق حقل **وضع العرض التوضيحي**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-177">Clear the **Demo mode** field.</span></span> <br>

    <span data-ttu-id="75ee7-178">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-178">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span></span>

3.  <span data-ttu-id="75ee7-179">أدخل المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="75ee7-179">Enter the following information:</span></span> 
    + <span data-ttu-id="75ee7-180">**معرف عميل Azure Active Directory** - يتم الحصول على معرف العميل في الخطوة 9 "إنشاء تطبيق خدمة ويب في Active Directory".</span><span class="sxs-lookup"><span data-stu-id="75ee7-180">**Azure Active directory client ID** - The client ID is obtained in step 9 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="75ee7-181">**سر عميل Azure Active Directory** - يتم الحصول على سر العميل في الخطوة 11 "إنشاء تطبيق خدمة ويب في Active Directory".</span><span class="sxs-lookup"><span data-stu-id="75ee7-181">**Azure Active directory client secret** - The client secret is obtained in step 11 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="75ee7-182">**مورد Azure Active Directory** - يمثل مورد Azure AD Directory‏‎ عنوان URL الجذر لـ Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="75ee7-182">**Azure Active directory resource** - The Azure AD directory resource depicts the Supply Chain Managementroot URL.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="75ee7-183">لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="75ee7-183">Do not end this field with a forward slash character (/).</span></span> 

    + <span data-ttu-id="75ee7-184">**مستأجر Azure Active Directory** - مستأجر Azure AD Directory‏‎ المستخدم مع خادم Supply Chain Management: `https://login.windows.net/your-AD-tenant-ID`.</span><span class="sxs-lookup"><span data-stu-id="75ee7-184">**Azure Active directory tenant** - The Azure AD directory tenant used with the Supply Chain Management server: `https://login.windows.net/your-AD-tenant-ID`.</span></span> <span data-ttu-id="75ee7-185">على سبيل المثال: `https://login.windows.net/contosooperations.onmicrosoft.com.`</span><span class="sxs-lookup"><span data-stu-id="75ee7-185">For example: `https://login.windows.net/contosooperations.onmicrosoft.com.`</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="75ee7-186">لا تضع حرف خط مائل للأمام (/) في نهاية هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="75ee7-186">Do not end this field with a forward slash character (/).</span></span> 
    
    + <span data-ttu-id="75ee7-187">**الشركة** - أدخل الكيان القانوني في Supply Chain Management الذي تريد أن يتصل به التطبيق.</span><span class="sxs-lookup"><span data-stu-id="75ee7-187">**Company** - Enter the legal entity in Supply Chain Management to which you want the application to connect.</span></span> <br>
    
    <span data-ttu-id="75ee7-188">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-188">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span></span>

4.  <span data-ttu-id="75ee7-189">حدد زر **السابق** في الزاوية العلوية اليمنى من التطبيق.</span><span class="sxs-lookup"><span data-stu-id="75ee7-189">Select the **Back** button in the top-left corner of the application.</span></span> <span data-ttu-id="75ee7-190">سيتصل الآن التطبيق بخادم Supply Chain Management وستظهر شاشة تسجيل الدخول لعامل المستودع.</span><span class="sxs-lookup"><span data-stu-id="75ee7-190">The application will now connect to your Supply Chain Management server and the log-in screen for the warehouse worker will display.</span></span>

    <span data-ttu-id="75ee7-191">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span><span class="sxs-lookup"><span data-stu-id="75ee7-191">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span></span>

<span data-ttu-id="75ee7-192">لمزيد من المعلومات حول كيفية إعداد تطبيق التخزين لمسح الأكواد الشريطية باستخدام كاميرا على جهاز محمول، راجع [مسح الأكواد الشريطية باستخدام كاميرا في تطبيق Dynamics 365 for Finance and Operations – التخزين](scan-bar-codes-using-a-camera.md).</span><span class="sxs-lookup"><span data-stu-id="75ee7-192">For information on how to set up the Warehousing app to scan bar codes using a camera on a mobile device, see [Scan bar codes using a camera in Dynamics 365 for Finance and Operations - Warehousing app](scan-bar-codes-using-a-camera.md).</span></span>

## <a name="remove-access-for-a-device"></a><span data-ttu-id="75ee7-193">إزالة حق الوصول لجهاز</span><span class="sxs-lookup"><span data-stu-id="75ee7-193">Remove access for a device</span></span>
<span data-ttu-id="75ee7-194">عند فقدان جهاز أو تعرضه للاختراق، يجب إزالة حق الوصول إلى Supply Chain Management للجهاز.</span><span class="sxs-lookup"><span data-stu-id="75ee7-194">In case of a lost or compromised device, you must remove access to Supply Chain Management for the device.</span></span> <span data-ttu-id="75ee7-195">تصف الخطوات التالية العملية الموصى بها لإزالة حق الوصول.</span><span class="sxs-lookup"><span data-stu-id="75ee7-195">The following steps describe the recommended process to remove access.</span></span>

1.  <span data-ttu-id="75ee7-196">انتقل إلى **إدارة النظام** &gt; **الإعداد** &gt; **تطبيقات Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="75ee7-196">Go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
2.  <span data-ttu-id="75ee7-197">احذف السطر الذي يتوافق مع الجهاز الذي تريد إزالة حق الوصول الممنوح له.</span><span class="sxs-lookup"><span data-stu-id="75ee7-197">Delete the line that corresponds to the device to which you want to remove access.</span></span> <span data-ttu-id="75ee7-198">تذكر **معرف العميل** المستخدم للجهاز الذي تمت إزالته، أنك ستحتاجه فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="75ee7-198">Remember the **Client ID** used for the removed device, you will need it later.</span></span>
3.  <span data-ttu-id="75ee7-199">سجل الدخول إلى مدخل Azure على العنوان <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="75ee7-199">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
4.  <span data-ttu-id="75ee7-200">انقر فوق رمز **Active Directory** في القائمة اليسرى، وتأكد من أنك في الدليل الصحيح.</span><span class="sxs-lookup"><span data-stu-id="75ee7-200">Click the **Active Directory** icon on the left menu, and ensure that you are in the correct directory.</span></span>
5.  <span data-ttu-id="75ee7-201">في القائمة، انقر فوق **عمليات تسجيل التطبيقات**، ثم انقر فوق التطبيق الذي تريد تكوينه.</span><span class="sxs-lookup"><span data-stu-id="75ee7-201">In the list, click **App registrations**, and then click the application that you want to configure.</span></span> <span data-ttu-id="75ee7-202">ستظهر صفحة **الإعدادات** مع معلومات التكوين.</span><span class="sxs-lookup"><span data-stu-id="75ee7-202">The **Settings** page will appear with configuration information.</span></span>
6.  <span data-ttu-id="75ee7-203">تأكد من أن **معرف العميل** هو نفسه كما هو موضح في الخطوة 2 في هذا القسم.</span><span class="sxs-lookup"><span data-stu-id="75ee7-203">Ensure that the **Client ID** of the application is the same as in step 2 in this section.</span></span>
7.  <span data-ttu-id="75ee7-204">انقر فوق الزر **حذف** في الجزء العلوي.</span><span class="sxs-lookup"><span data-stu-id="75ee7-204">Click the **Delete** button in the top pane.</span></span>
8.  <span data-ttu-id="75ee7-205">انقر فوق **نعم** في رسالة التأكيد.</span><span class="sxs-lookup"><span data-stu-id="75ee7-205">Click **Yes** in the confirmation message.</span></span>
