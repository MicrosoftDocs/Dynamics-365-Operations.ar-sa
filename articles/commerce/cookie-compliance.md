---
title: توافق ملفات تعريف الارتباط
description: يصف هذا الموضوع اعتبارات توافق ملفات تعريف الارتباط والسياسات الافتراضية المضمنة في Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409792"
---
# <a name="cookie-compliance"></a><span data-ttu-id="5c859-103">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="5c859-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c859-104">يصف هذا الموضوع اعتبارات توافق ملفات تعريف الارتباط والسياسات الافتراضية المضمنة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5c859-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c859-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="5c859-105">Overview</span></span>

<span data-ttu-id="5c859-106">تعد الخصوصية عاملاً هامًا عند تتبع تقنيات تؤثر على عملاء التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="5c859-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="5c859-107">نظرًا لمعايير التوافق للخصوصية مثل ‏‫القانون العام لحماية البيانات (GDPR)‬ في الاتحاد الأوروبي (EU)، يجب مراعاة إرشادات الخصوصية الإلكترونية لأي موقع نشط اليوم.</span><span class="sxs-lookup"><span data-stu-id="5c859-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="5c859-108">نظرًا لأن العديد من مواقع التجارة الإلكترونية يمكن الوصول إليها عالميًا بشكل افتراضي، فمن المهم أن تراجع معايير التوافق لموقع التجارة الإلكترونية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="5c859-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="5c859-109">لمعرفة المزيد حول المبادئ الأساسية التي تستخدمها Microsoft لتوافق ملفات تعريف الارتباط، تفضل بزيارة [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="5c859-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="5c859-110">على هذا الموقع، يمكنك أيضًا الحصول على مزيد من المعلومات حول مجالات التوافق والخصوصية.</span><span class="sxs-lookup"><span data-stu-id="5c859-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="5c859-111">يعرض الجدول التالي قائمة المراجع الحالية لملفات تعريف الارتباط الموضوعة في مواقع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5c859-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="5c859-112">اسم ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="5c859-112">Cookie name</span></span>                               | <span data-ttu-id="5c859-113">الاستخدام</span><span class="sxs-lookup"><span data-stu-id="5c859-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="5c859-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="5c859-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="5c859-115">قم بتخزين ملفات تعريف ارتباط مصادقة Microsoft Azure Active Directory (Azure AD) تسجيل دخول أحادي (SSO).</span><span class="sxs-lookup"><span data-stu-id="5c859-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="5c859-116">تخزين معلومات المستخدم الأساسي المشفرة (الاسم، اللقب، البريد الإلكتروني).</span><span class="sxs-lookup"><span data-stu-id="5c859-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="5c859-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="5c859-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="5c859-118">معرف سلة المتاجر المستخدم للحصول على قائمة بالمنتجات المضافة إلى مثيل العربة.</span><span class="sxs-lookup"><span data-stu-id="5c859-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="5c859-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="5c859-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="5c859-120">تتبع موافقة توافق ملف تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="5c859-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="5c859-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="5c859-121">ai_session</span></span>                                  | <span data-ttu-id="5c859-122">الكشف عن عدد جلسات عمل نشاط المستخدم التي تتضمن بعض صفحات التطبيق والميزات الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="5c859-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="5c859-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="5c859-123">ai_user</span></span>                                     | <span data-ttu-id="5c859-124">الكشف عن عدد الأشخاص الذين تم استخدامهم للتطبيق وميزاته.</span><span class="sxs-lookup"><span data-stu-id="5c859-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="5c859-125">يتم حساب المستخدمين باستخدام معرفات مجهولة.</span><span class="sxs-lookup"><span data-stu-id="5c859-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="5c859-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="5c859-126">b2cru</span></span>                                       | <span data-ttu-id="5c859-127">يخزن عنوان URL لإعادة التوجيه بشكل حيوي.</span><span class="sxs-lookup"><span data-stu-id="5c859-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="5c859-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="5c859-128">JSESSIONID</span></span>                                  | <span data-ttu-id="5c859-129">مستخدم بواسطة موصل مدفوعات Adyen لتخزين جلسة عمل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="5c859-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="5c859-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="5c859-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="5c859-131">مصادقة</span><span class="sxs-lookup"><span data-stu-id="5c859-131">Authentication</span></span>                                               |
| <span data-ttu-id="5c859-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="5c859-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="5c859-133">مستخدم للمحافظة على حالة الطلب.</span><span class="sxs-lookup"><span data-stu-id="5c859-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="5c859-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="5c859-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="5c859-135">رمز تزوير الطلب عبر المواقع (CRSF) المستخدم للحماية من CRSF.</span><span class="sxs-lookup"><span data-stu-id="5c859-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="5c859-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="5c859-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="5c859-137">مستخدم لتوجيه الطلبات إلى مثيل خادم مصادقة الإنتاج المناسب.</span><span class="sxs-lookup"><span data-stu-id="5c859-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="5c859-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="5c859-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="5c859-139">مستخدم لتوجيه الطلبات إلى مثيل خادم مصادقة الإنتاج المناسب.</span><span class="sxs-lookup"><span data-stu-id="5c859-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="5c859-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="5c859-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="5c859-141">مستخدم لتوجيه الطلبات إلى مثيل خادم مصادقة الإنتاج المناسب.</span><span class="sxs-lookup"><span data-stu-id="5c859-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="5c859-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="5c859-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="5c859-143">مستخدم في الحفاظ على جلسة SSO.</span><span class="sxs-lookup"><span data-stu-id="5c859-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="5c859-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="5c859-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="5c859-145">مستخدم لتعقب الحركات (عدد علامات التبويب المفتوحة التي يتم مصادقتها مقابل موقع العمل إلى المستهلك (B2C))، بما في ذلك الحركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="5c859-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="5c859-146">الموافقة على ملفات تعريف ارتباط مستخدم الموقع في موقع التجارة الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="5c859-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="5c859-147">إذا كانت ميزة أو وحدة نمطية لموقع تجارة إلكترونية تستخدم ملف تعريف ارتباط غير أساسي، فيجب الحصول على موافقة مستخدم الموقع قبل تعقب ملف تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="5c859-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="5c859-148">للسماح لمستخدمي الموقع بتوفير الموافقة على ملفات تعريف الارتباط في موقع تجارة إلكترونية، يجب ان يقوم كاتب الموقع بإضافة الوحدة النمطية للموافقة على ملفات تعريف الارتباط وتكوينها في الوحدة النمطية للرأس لضمان طلب الموافقة واستلامها.</span><span class="sxs-lookup"><span data-stu-id="5c859-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="5c859-149">يجب إعطاء موافقة مستخدم الموقع قبل أن يتم عرض ميزة أو وحدة نمطية تستخدم ملف تعريف ارتباط غير أساسي في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="5c859-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c859-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5c859-150">Additional resources</span></span>

[<span data-ttu-id="5c859-151">ميزات وقدرات إمكانية الوصول</span><span class="sxs-lookup"><span data-stu-id="5c859-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="5c859-152">نظرة عامة على الامتثال</span><span class="sxs-lookup"><span data-stu-id="5c859-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="5c859-153">إضافة صفحة سياسة الخصوصية</span><span class="sxs-lookup"><span data-stu-id="5c859-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="5c859-154">استبدال معرفات المستخدم المقترنة بتغييرات المحتوى المتعقبة</span><span class="sxs-lookup"><span data-stu-id="5c859-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="5c859-155">الوحدة النمطية للموافقة على ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="5c859-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="5c859-156">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="5c859-156">Header module</span></span>](author-header-module.md)
