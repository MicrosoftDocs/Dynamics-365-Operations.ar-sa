---
title: توافق ملفات تعريف الارتباط
description: يصف هذا الموضوع اعتبارات توافق ملفات تعريف الارتباط والسياسات الافتراضية المضمنة في Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
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
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446903"
---
# <a name="cookie-compliance"></a><span data-ttu-id="4952c-103">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="4952c-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4952c-104">يصف هذا الموضوع اعتبارات توافق ملفات تعريف الارتباط والسياسات الافتراضية المضمنة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4952c-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4952c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="4952c-105">Overview</span></span>

<span data-ttu-id="4952c-106">تعد الخصوصية عاملاً هامًا عند تتبع تقنيات تؤثر على عملاء التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4952c-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="4952c-107">نظرًا لمعايير التوافق للخصوصية مثل ‏‫القانون العام لحماية البيانات (GDPR)‬ في الاتحاد الأوروبي (EU)، يجب مراعاة إرشادات الخصوصية الإلكترونية لأي موقع نشط اليوم.</span><span class="sxs-lookup"><span data-stu-id="4952c-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="4952c-108">نظرًا لأن العديد من مواقع التجارة الإلكترونية يمكن الوصول إليها عالميًا بشكل افتراضي، فمن المهم أن تراجع معايير التوافق لموقع التجارة الإلكترونية الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="4952c-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="4952c-109">لمعرفة المزيد حول المبادئ الأساسية التي تستخدمها Microsoft لتوافق ملفات تعريف الارتباط، تفضل بزيارة [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="4952c-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="4952c-110">على هذا الموقع، يمكنك أيضًا الحصول على مزيد من المعلومات حول مجالات التوافق والخصوصية.</span><span class="sxs-lookup"><span data-stu-id="4952c-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="4952c-111">يعرض الجدول التالي قائمة المراجع الحالية لملفات تعريف الارتباط الموضوعة في مواقع Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4952c-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="4952c-112">اسم ملف تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="4952c-112">Cookie name</span></span>                               | <span data-ttu-id="4952c-113">الاستخدام</span><span class="sxs-lookup"><span data-stu-id="4952c-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="4952c-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="4952c-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="4952c-115">قم بتخزين ملفات تعريف ارتباط مصادقة Microsoft Azure Active Directory (Azure AD) تسجيل دخول أحادي (SSO).</span><span class="sxs-lookup"><span data-stu-id="4952c-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="4952c-116">تخزين معلومات المستخدم الأساسي المشفرة (الاسم، اللقب، البريد الإلكتروني).</span><span class="sxs-lookup"><span data-stu-id="4952c-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="4952c-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="4952c-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="4952c-118">معرف سلة المتاجر المستخدم للحصول على قائمة بالمنتجات المضافة إلى مثيل العربة.</span><span class="sxs-lookup"><span data-stu-id="4952c-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="4952c-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="4952c-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="4952c-120">تتبع موافقة توافق ملف تعريف الارتباط.</span><span class="sxs-lookup"><span data-stu-id="4952c-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="4952c-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="4952c-121">ai_session</span></span>                                  | <span data-ttu-id="4952c-122">الكشف عن عدد جلسات عمل نشاط المستخدم التي تتضمن بعض صفحات التطبيق والميزات الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="4952c-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="4952c-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="4952c-123">ai_user</span></span>                                     | <span data-ttu-id="4952c-124">الكشف عن عدد الأشخاص الذين تم استخدامهم للتطبيق وميزاته.</span><span class="sxs-lookup"><span data-stu-id="4952c-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="4952c-125">يتم حساب المستخدمين باستخدام معرفات مجهولة.</span><span class="sxs-lookup"><span data-stu-id="4952c-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="4952c-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="4952c-126">b2cru</span></span>                                       | <span data-ttu-id="4952c-127">يخزن عنوان URL لإعادة التوجيه بشكل حيوي.</span><span class="sxs-lookup"><span data-stu-id="4952c-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="4952c-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="4952c-128">JSESSIONID</span></span>                                  | <span data-ttu-id="4952c-129">مستخدم بواسطة موصل مدفوعات Adyen لتخزين جلسة عمل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4952c-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="4952c-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="4952c-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="4952c-131">مصادقة</span><span class="sxs-lookup"><span data-stu-id="4952c-131">Authentication</span></span>                                               |
| <span data-ttu-id="4952c-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="4952c-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="4952c-133">مستخدم للمحافظة على حالة الطلب.</span><span class="sxs-lookup"><span data-stu-id="4952c-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="4952c-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="4952c-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="4952c-135">رمز تزوير الطلب عبر المواقع (CRSF) المستخدم للحماية من CRSF.</span><span class="sxs-lookup"><span data-stu-id="4952c-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="4952c-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="4952c-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="4952c-137">مستخدم لتوجيه الطلبات إلى مثيل خادم مصادقة الإنتاج المناسب.</span><span class="sxs-lookup"><span data-stu-id="4952c-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4952c-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="4952c-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="4952c-139">مستخدم لتوجيه الطلبات إلى مثيل خادم مصادقة الإنتاج المناسب.</span><span class="sxs-lookup"><span data-stu-id="4952c-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4952c-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="4952c-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="4952c-141">مستخدم لتوجيه الطلبات إلى مثيل خادم مصادقة الإنتاج المناسب.</span><span class="sxs-lookup"><span data-stu-id="4952c-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4952c-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="4952c-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="4952c-143">مستخدم في الحفاظ على جلسة SSO.</span><span class="sxs-lookup"><span data-stu-id="4952c-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="4952c-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="4952c-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="4952c-145">مستخدم لتعقب الحركات (عدد علامات التبويب المفتوحة التي يتم مصادقتها مقابل موقع العمل إلى المستهلك (B2C))، بما في ذلك الحركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="4952c-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4952c-146">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="4952c-146">Additional resources</span></span>

[<span data-ttu-id="4952c-147">ميزات وقدرات إمكانية الوصول</span><span class="sxs-lookup"><span data-stu-id="4952c-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="4952c-148">نظرة عامة على الامتثال</span><span class="sxs-lookup"><span data-stu-id="4952c-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="4952c-149">إضافة صفحة سياسة الخصوصية</span><span class="sxs-lookup"><span data-stu-id="4952c-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="4952c-150">استبدال معرفات المستخدمين المرتبطة بتغييرات المحتوى المتعقبة</span><span class="sxs-lookup"><span data-stu-id="4952c-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
