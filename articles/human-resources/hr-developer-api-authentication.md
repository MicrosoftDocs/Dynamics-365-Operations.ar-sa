---
title: المصادقة
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008008"
---
# <a name="authentication"></a><span data-ttu-id="8a199-102">المصادقة</span><span class="sxs-lookup"><span data-stu-id="8a199-102">Authentication</span></span>

<span data-ttu-id="8a199-103">يقدم هذا المقال معلومات عامة حول كيفية المصادقة مع واجهة برمجة تطبيقات بيانات Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8a199-103">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="8a199-104">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8a199-104">Overview</span></span>

<span data-ttu-id="8a199-105">تعد واجهة برمجة تطبيقات البيانات للموارد البشرية بمثابة تطبيق OData.</span><span class="sxs-lookup"><span data-stu-id="8a199-105">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="8a199-106">لمزيد من المعلومات، راجع [‬‏‫بروتوكول البيانات المفتوحة (OData)‬](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="8a199-106">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="8a199-107">يجب أن يقوم التطبيق الخاص بك بالمصادقة كمتصل مخوّل قبل أن تتعامل واجهة API مع الطلبات التي تتلقاها من التطبيق الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8a199-107">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="8a199-108">القواعد الأساسية</span><span class="sxs-lookup"><span data-stu-id="8a199-108">Fundamentals</span></span>

<span data-ttu-id="8a199-109">لاستدعاء API للبيانات، يجب أن يحصل التطبيق الخاص بك على رمز مميز للوصول من النظام الأساسي لهويه Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a199-109">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="8a199-110">يحتوي الرمز المميز للوصول على معلومات حول التطبيق الخاص بك والإذن الذي يجب عليه استدعاء الموارد في الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="8a199-110">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="8a199-111">الرمز المميز للوصول</span><span class="sxs-lookup"><span data-stu-id="8a199-111">Access token</span></span>

<span data-ttu-id="8a199-112">الرموز المميزة للوصول التي يصدرها النظام الأساسي لهويه Microsoft هي رموز JavaScript Object Notation (JSON) مميزة للويب (JWTs) يتم ترميزها باستخدام base64.</span><span class="sxs-lookup"><span data-stu-id="8a199-112">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="8a199-113">وهي تحتوي على معلومات (مطالبات) تستخدمها واجهة API للبيانات (وواجهات API الويب الأخرى التي تم تأمينها بواسطة النظام الأساسي لهويه Microsoft) للتحقق من المتصل والتأكد من أنه يملك الأذونات الصحيحة لتنفيذ العملية التي يطلبها.</span><span class="sxs-lookup"><span data-stu-id="8a199-113">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="8a199-114">أثناء المكالمات، يمكنك التعامل مع رموز الوصول المميزة على أنها غير شفافة.</span><span class="sxs-lookup"><span data-stu-id="8a199-114">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="8a199-115">يجب عليك دائمًا نقل رموز الوصول المميزة عبر قناة آمنة ، مثل أمان طبقة النقل (TLS) وبروتوكول نقل النص التشعبي الآمن (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="8a199-115">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="8a199-116">وفيما يلي مثال لرمز وصول مميز تم إصداره بواسطة النظام الأساسي لهويه Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a199-116">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="8a199-117">لطب واجهة API للبيانات، قم بإرفاق الرمز المميز للوصول كرمز حامل لرأس التخويل في طلب HTTP الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8a199-117">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="8a199-118">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="8a199-118">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="8a199-119">تسجيل استمارة جديدة باستخدام مدخل Azure</span><span class="sxs-lookup"><span data-stu-id="8a199-119">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="8a199-120">قم بتسجيل الدخول إلى [مدخل Microsoft Azure ](https://portal.azure.com) باستخدام حساب العمل أو المؤسسة التعليمية، أو حساب Microsoft شخصي.</span><span class="sxs-lookup"><span data-stu-id="8a199-120">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="8a199-121">إذا كان الحساب الخاص بك يمنحك حق الوصول إلى أكثر من مستأجر، فحدد حسابك في الركن الأيمن العلوي، وعيّن جلسة المدخل الخاصة بك على مستأجر Azure Active Directory (Azure AD) الذي تريده.</span><span class="sxs-lookup"><span data-stu-id="8a199-121">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="8a199-122">في الجزء الأيمن ، حدد خدمة **Azure Active Directory**، ثم حدد **عمليات تسجيل التطبيق \> تسجيل جديد**.</span><span class="sxs-lookup"><span data-stu-id="8a199-122">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="8a199-123">عندما تظهر صفحة **تسجيل تطبيق**، أدخل معلومات تسجيل التطبيق الخاص بك:</span><span class="sxs-lookup"><span data-stu-id="8a199-123">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="8a199-124">**الاسم**: أدخل اسم التطبيق ذي معني الذي سيظهر لمستخدمي التطبيق.</span><span class="sxs-lookup"><span data-stu-id="8a199-124">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="8a199-125">**أنواع الحسابات المعتمدة**: حدد أنواع الحسابات التي يجب أن يدعمها تطبيقك.</span><span class="sxs-lookup"><span data-stu-id="8a199-125">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="8a199-126">أنواع الحسابات المعتمدة</span><span class="sxs-lookup"><span data-stu-id="8a199-126">Supported account types</span></span> | <span data-ttu-id="8a199-127">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="8a199-127">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="8a199-128">الحسابات الموجودة في الدليل التنظيمي هذا فقط</span><span class="sxs-lookup"><span data-stu-id="8a199-128">Accounts in this organizational directory only</span></span> | <span data-ttu-id="8a199-129">حدد هذا الخيار إذا كنت تقوم بتصميم تطبيق خاص بالأعمال التجارية.</span><span class="sxs-lookup"><span data-stu-id="8a199-129">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="8a199-130">لا يتوفر هذا الخيار الا إذا قمت بتسجيل التطبيق في دليل.</span><span class="sxs-lookup"><span data-stu-id="8a199-130">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="8a199-131">يتم تعيين هذا الخيار إلى **Azure AD مستأجر واحد فقط**.</span><span class="sxs-lookup"><span data-stu-id="8a199-131">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="8a199-132">ويعد هذا الخيار هو الخيار الافتراضي الا إذا كنت تقوم بتسجيل التطبيق خارج أحد الدلائل.</span><span class="sxs-lookup"><span data-stu-id="8a199-132">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="8a199-133">وفي هذه الحالة، يكون الخيار الافتراضي هو **Azure AD حسابات Microsoft شخصية ومتعددة المستأجرين**.</span><span class="sxs-lookup"><span data-stu-id="8a199-133">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="8a199-134">الحسابات الموجودة في أي دليل تنظيمي</span><span class="sxs-lookup"><span data-stu-id="8a199-134">Accounts in any organizational directory</span></span> | <span data-ttu-id="8a199-135">حدد هذا الخيار لاستهداف كافة العملاء التجاريين والتعليميين.</span><span class="sxs-lookup"><span data-stu-id="8a199-135">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="8a199-136">يتم تعيين هذا الخيار إلى **Azure AD مستأجرين متعددين فقط**.</span><span class="sxs-lookup"><span data-stu-id="8a199-136">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="8a199-137">إذا كنت قد قمت بتسجيل التطبيق كـ **Azure AD مستأجر واحد فقط** يمكنك استخدام ريشة **‏‫المصادقة‬**، لتحديثها إلى **Azure AD مستأجرين متعددين فقط** ثم الرجوع إلى **Azure AD مستأجر واحد فقط**.</span><span class="sxs-lookup"><span data-stu-id="8a199-137">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="8a199-138">الحسابات الموجودة في أي دليل تنظيمي وحسابات Microsoft الشخصية</span><span class="sxs-lookup"><span data-stu-id="8a199-138">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="8a199-139">حدد هذا الخيار لاستهداف أكبر مجموعة من العملاء.</span><span class="sxs-lookup"><span data-stu-id="8a199-139">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="8a199-140">يتم تعيين هذا الخيار إلى **Azure AD حسابات Microsoft شخصية ومتعددة المستأجرين**.</span><span class="sxs-lookup"><span data-stu-id="8a199-140">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="8a199-141">إذا كنت قد قمت بتسجيل التطبيق كـ **Azure AD حسابات Microsoft شخصية ومتعددة المستأجرين** فلن تتمكن من تغيير هذا الإعداد في واجهة المستخدم (UI).</span><span class="sxs-lookup"><span data-stu-id="8a199-141">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="8a199-142">بدلاً من ذلك، يجب عليك استخدام محرر بيان التطبيق لتغيير أنواع الحسابات المدعومة.</span><span class="sxs-lookup"><span data-stu-id="8a199-142">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="8a199-143">**عنوان URI لإعادة التوجيه (اختياري)** - حدد نوع التطبيق الذي تقوم بتصميمه: **ويب** أو **عميل عام (هاتف محمول وسطح المكتب)**.</span><span class="sxs-lookup"><span data-stu-id="8a199-143">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="8a199-144">ثم أدخل عنوان URI لإعادة التوجيه (أو عنوان URL الخاص بالرد) للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="8a199-144">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="8a199-145">بالنسبة لتطبيقات الويب، قم بتوفير عنوان URL الأساسي الخاص بالتطبيق.</span><span class="sxs-lookup"><span data-stu-id="8a199-145">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="8a199-146">على سبيل المثال، قد يكون `http://localhost:31544` هو عنوان URL الخاص بتطبيق ويب الذي يتم تشغيله علي الجهاز المحلي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8a199-146">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="8a199-147">ثم يقوم المستخدمون باستخدام عنوان URL هذا لتسجيل الدخول إلى تطبيق عميل ويب.</span><span class="sxs-lookup"><span data-stu-id="8a199-147">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="8a199-148">بالنسبة لتطبيقات العميل العامة، قم بتوفير عنوان URL الذي يستخدمه Azure AD لإرجاع استجابات الرمز المميزة.</span><span class="sxs-lookup"><span data-stu-id="8a199-148">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="8a199-149">أدخل قيمة خاصة بالتطبيق، مثل `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="8a199-149">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="8a199-150">لمشاهدة أمثلة معينة لتطبيقات الويب أو التطبيقات الأصلية، راجع قوالب التشغيل السريع في [النظام الأساسي للهوية Microsoft (الذي كان يسمى سابقًا Azure Active Directory للمطورين)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="8a199-150">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="8a199-151">ضمن **أذونات API**، حدد **إضافة إذن**.</span><span class="sxs-lookup"><span data-stu-id="8a199-151">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="8a199-152">ثم، في علامة التبويب **واجهات API التي تستخدمها مؤسستي** ابحث عن **Dynamics 365 Human Resources** وأضف الإذن **user\_impersonation** إلى التطبيق الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8a199-152">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="8a199-153">معرف التطبيق للموارد البشرية هو f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="8a199-153">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="8a199-154">استخدم هذا المعرف للتأكد من أنك قمت باختيار التطبيق الصحيح.</span><span class="sxs-lookup"><span data-stu-id="8a199-154">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="8a199-155">حدد **السجل**.</span><span class="sxs-lookup"><span data-stu-id="8a199-155">Select **Register**.</span></span>

   <span data-ttu-id="8a199-156">[![تسجيل تطبيق جديد في مدخل Azure](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8a199-156">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="8a199-157">يقوم Azure AD بتعيين معرف تطبيق فريد (معرف العميل) إلى التطبيق الخاص بك، ثم ينقلك إلى صفحة **نظرة عامة** للتطبيق الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8a199-157">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="8a199-158">لإضافة المزيد من الإمكانات إلى التطبيق، يمكنك تحديد خيارات التكوين الأخرى، مثل الخيارات الخاصة بالعلامة التجارية والشهادات والأسرار.</span><span class="sxs-lookup"><span data-stu-id="8a199-158">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="8a199-159">استرداد الرمز المميز للوصول</span><span class="sxs-lookup"><span data-stu-id="8a199-159">Retrieving an access token</span></span>

<span data-ttu-id="8a199-160">ستعتمد المواصفات الخاصة بكيفية استرداد رمز مميز للوصول للاتصال بواجهة API لبيانات الموارد البشرية على التقنيات التي تستخدمها لتطوير تطبيق العميل.</span><span class="sxs-lookup"><span data-stu-id="8a199-160">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="8a199-161">على سبيل المثال، قد [تقوم بالاختبار باستخدام أداة مساعدة لجهة خارجية](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (مثل Postman) أو تطوير تطبيق وحده تحكم C# أو خدمة ويب أو إنشاء عميل javascript/TypeScript.</span><span class="sxs-lookup"><span data-stu-id="8a199-161">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="8a199-162">مثال لتطبيق عميل C#:</span><span class="sxs-lookup"><span data-stu-id="8a199-162">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="8a199-163">بمجرد استرداد رمز وصول مميز، ستقوم بتمرير الرمز المميز في رأس التخويل كرمز مميز لحامل مع كل طلب تقوم بإرساله إلى واجهة API للبيانات، كما هو موضح أعلاه.</span><span class="sxs-lookup"><span data-stu-id="8a199-163">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
