---
title: تكوين مصادقة Azure Active Directory لتسجيل الدخول إلى نقطة البيع
description: يشرح هذا الموضوع كيفيه تكوين Azure Active Directory كأسلوب المصادقة في نقطة بيع Microsoft Dynamics 365 Commerce.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937448"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="0e4b6-103">تكوين مصادقة Azure Active Directory لتسجيل الدخول إلى نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="0e4b6-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="0e4b6-104">يشرح هذا الموضوع كيفية تكوين Azure Active Directory (Azure AD) كأسلوب المصادقة في نقطة البيع (POS) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="0e4b6-105">يريد تجار التجزئة الذين يستخدمون Dynamics 365 Commerce جنبًا إلى جنب مع خدمات سحابة Microsoft الأخرى مثل Microsoft Azure، وMicrosoft 365، وMicrosoft Teams غالبًا استخدام Azure AD للإدارة المركزية لبيانات اعتماد المستخدم لتجربة تسجيل دخول آمنة وسلسة عبر التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="0e4b6-106">لاستخدام مصادقة Azure AD لنقطة بيع Commerce، يجب أولاً تكوين Azure AD كأسلوب المصادقة في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="0e4b6-107">تكوين أسلوب مصادقة POS</span><span class="sxs-lookup"><span data-stu-id="0e4b6-107">Configure POS authentication method</span></span>

<span data-ttu-id="0e4b6-108">لتكوين أسلوب مصادقة نقطة البيع في إدارة Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="0e4b6-109">انتقل إلى **Retail وCommerce \> إعداد القنوات \> إعداد نقطة البيع \> ملفات تعريف نقطة البيع \> ملفات تعريف الوظائف**، وحدد ملف تعريف الوظائف المطلوب تغييره.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="0e4b6-110">في قسم **تسجيل دخول موظفي نقطة البيع** في علامة التبويب السريع **الوظائف**، حدد خيار أسلوب المصادقة المطلوب من القائمة المنسدلة **أسلوب مصادقة تسجيل الدخول**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="0e4b6-111">يشتمل **طريقة مصادقة تسجيل الدخول** على ثلاثة خيارات:</span><span class="sxs-lookup"><span data-stu-id="0e4b6-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="0e4b6-112">**معرف الموظف وكلمة المرور** - يتطلب هذا الخيار الافتراضي من مستخدمي POS إدخال معرف شخصي وكلمة مرور لتسجيل الدخول إلى نقطة البيع والوصول إلى وظيفة تجاوز المدير.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="0e4b6-113">**Azure AD بدون تسجيل دخول أحادي** - يتطلب هذا الخيار من مستخدمي POS استخدام بيانات اعتماد Azure AD لتسجيل الدخول إلى وظيفة تجاوز مدير الوصول ونقاط البيع.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="0e4b6-114">عندما يتم تحديث عميل نقطة البيع أو إعادة فتحه ، يجب على مستخدم نقطة البيع توفير بيانات اعتماد Azure AD لتسجيل الدخول مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="0e4b6-115">**Azure AD باستخدام تسجيل الدخول الأحادي** - عند تحديد هذا الخيار، يمكن لمستخدمي نقطة البيع تسجيل الدخول إلى Cloud POS (CPOS) باستخدام بيانات اعتماد Azure AD النشطة التي تستخدمها تطبيقات الويب الأخرى في متصفح الويب نفسه، أو قم بتسجيل الدخول إلى Modern POS (MPOS) باستخدام بيانات اعتماد Azure AD لتسجيل الدخول إلى Windows.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="0e4b6-116">كلا الطريقتين تسمحان بتسجيل الدخول دون الحاجة لإدخال بيانات اعتماد Azure AD في شاشة تسجيل الدخول في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="0e4b6-117">ومع ذلك، سيظل الوصول إلى وظيفة تجاوز مدير نقطة البيع يتطلب تسجيل الدخول باستخدام بيانات اعتماد Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="0e4b6-118">انتقل إلى **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > جدول التوزيع** وقم بتشغيل وظيفة **1070 (تكوين القنوات)** لمزامنة أحدث إعدادات ملف تعريف الوظائف لعملاء نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="0e4b6-119">يقوم خيار أسلوب مصادقة **Azure AD دون تسجيل الدخول الأحادي** باستبدال خيار **Azure Active Directory** في إصدار Commerce رقم 10.0.18 والإصدارات الأقدم.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="0e4b6-120">تتطلب مصادقة Azure AD اتصال إنترنت نشطًا، ولكنها لن تعمل عندما تكون نقطه البيع في وضع عدم الاتصال.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="0e4b6-121">إقران حسابات Azure AD بمستخدمي نقطه البيع</span><span class="sxs-lookup"><span data-stu-id="0e4b6-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="0e4b6-122">لاستخدام Azure AD كأسلوب مصادقة نقطة البيع، يجب عليك إقران حسابات Azure AD بمستخدمي نقطه البيع في إدارة Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="0e4b6-123">لإقران حسابات Azure AD بمستخدمي نقطه البيع في إدارة Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="0e4b6-124">انتقل إلى **Retail وCommerce > الموظفين > العمال** وافتح سجل عمال.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="0e4b6-125">في جزء الإجراءات، حدد علامة تبويب **Commerce**، ثم ضمن **الهوية الخارجية**، حدد **إقران هوية موجودة**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="0e4b6-126">في مربع الحوار **استخدام هوية خارجية موجودة**، حدد **البحث باستخدام البريد الإلكتروني**، وأدخل عنوان بريد إلكتروني في Azure AD، ثم حدد **بحث**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="0e4b6-127">حدد حساب Azure AD المرتجع، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="0e4b6-128">بعد خطوات التكوين أعلاه، ستتم تعبئة حقول **الاسم المستعار** و **UPN** و **المعرف الفرعي الخارجي** على علامة تبويب **Commerce** في صفحة تفاصيل العامل.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="0e4b6-129">يجب عليك تشغيل وظيفة **1060 (الفريق)** في **Retail وCommerce > تكنولوجيا معلومات Retail وCommerce > جدول التوزيع** لمزامنة أحدث مستخدم نقطة بيع وبيانات حساب Azure AD مع القناة.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="0e4b6-130">كأفضل ممارسة، بعد تحديث معلومات العامل مثل كلمة المرور، أو إذن نقطة البيع، أو حساب Azure AD المقترن أو دفتر عناوين الموظف في إدارة Commerce، يُوصى بشدة بتشغيل وظيفة **1060 (الفريق)** لمزامنة أحدث معلومات العامل مع القناة.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="0e4b6-131">يمكن لعميل نقطة البيع بعد ذلك إحضار البيانات الصحيحة للتحقق من مصادقة المستخدم والتفويض.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="0e4b6-132">سجل قفل نقاط البيع وتسجيل الخروج باستخدام مصادقة Azure AD</span><span class="sxs-lookup"><span data-stu-id="0e4b6-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="0e4b6-133">يحدث التالي عند تكوين نقطة البيع لاستخدام أسلوب مصادقة Azure AD:</span><span class="sxs-lookup"><span data-stu-id="0e4b6-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="0e4b6-134">لن تتوفر وظيفة **سجل القفل** في تطبيق نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="0e4b6-135">ستؤدي وظيفة **القفل تلقائيًا** نفس الشيء مثل وظيفة **تسجيل الخروج تلقائيًا**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="0e4b6-136">إذا حدد مستخدم نقطة البيع **تسجيل الخروج**، سيُطلب من المستخدم تسجيل الدخول باستخدام بيانات اعتماد Azure AD في المرة التالية التي يتم فيها تشغيل نقطة البيع، بغض النظر عما إذا كان تسجيل الدخول الأحادي ممكّنًا أم لا.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="0e4b6-137">وظيفة تجاوز المدير مع مصادقة Azure AD</span><span class="sxs-lookup"><span data-stu-id="0e4b6-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="0e4b6-138">عندما يتم تكوين نقطة البيع لاستخدام مصادقة Azure AD، ستفتح وظيفة تجاوز المدير مربع حوار يطالبك ببيانات اعتماد Azure AD لمستخدم المدير.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="0e4b6-139">بعد الموافقة على تسجيل دخول المدير، سيتم إلغاء بيانات اعتماد Azure AD الخاصة بالمدير وسيتم استخدام بيانات اعتماد Azure AD الخاصة بالمستخدم السابق لعمليات نقطة البيع اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="0e4b6-140">في إصدارات Commerce رقم 10.0.18 والإصدارات الأقدم، لا تدعم وظيفة تجاوز المدير Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="0e4b6-141">مطلوب معرف شخصي وكلمة مرور حتى إذا تم تكوين نقطة البيع لاستخدام أسلوب مصادقة Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="0e4b6-142">عند استخدام CPOS مع مستعرض Safari على جهاز Apple iOS، يجب عليك أولاً إيقاف تشغيل **حظر النوافذ المنبثقة** في إعدادات Safari حتى يتمكن المدير من العمل معها باستخدام مصادقة Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="0e4b6-143">أفضل ممارسات الأمان لمصادقة نقطة البيع المستندة إلى Azure AD على الأجهزة المشتركة</span><span class="sxs-lookup"><span data-stu-id="0e4b6-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="0e4b6-144">يقوم العديد من بائعي التجزئة بإعداد بيئة متاجر البيع بالتجزئة الخاصة بهم بطريقة يحتاجها العديد من المستخدمين للوصول إلى تطبيق نقطة البيع من جهاز فعلي مشترك.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="0e4b6-145">في هذا السياق، بينما يوفر تسجيل الدخول الأحادي تجربة مصادقة مريحة وسلسة، فقد يؤدي أيضًا إلى إنشاء ثغرة أمنية حيث قد لا يدرك مستخدم نقطة البيع الحالي أن بيانات اعتماد مستخدم آخر يتم استخدامها لإجراء حركات أو عمليات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="0e4b6-146">قبل تكوين نقطة البيع لاستخدام أسلوب مصادقة Azure AD، يُوصى بشدة بمراجعة سياسة الأمان وإعدادات تسجيل الدخول للجهاز المشترك لتحديد الخيار الأنسب.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="0e4b6-147">إذا كانت بيئة البيع بالتجزئة الخاصة بك تستخدم حسابًا مشتركًا (على سبيل المثال، حساب محلي) لتسجيل الدخول الفعلي للجهاز، فمن المستحسن استخدام خيار **Azure AD بلا تسجيل الدخول الأحادي**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="0e4b6-148">يضمن هذا أن كل مستخدم نقطة بيع يوفر بشكل صريح بيانات اعتماد Azure AD لتسجيل الدخول إلى نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="0e4b6-149">إذا كانت بيئة البيع بالتجزئة الخاصة بك تتطلب من الموظفين استخدام حسابات Azure AD الخاصة بهم لتسجيل الدخول إلى نقطة البيع وجهازها الفعلي المستضيف، يُوصى باستخدام خيار **Azure AD بلا تسجيل الدخول الأحادي**.</span><span class="sxs-lookup"><span data-stu-id="0e4b6-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e4b6-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0e4b6-150">Additional resources</span></span>

[<span data-ttu-id="0e4b6-151"> تكوين عامل</span><span class="sxs-lookup"><span data-stu-id="0e4b6-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="0e4b6-152">إنشاء ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="0e4b6-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="0e4b6-153">إعداد وظيفة تسجيل الدخول الموسع لنقطة البيع الحديثة ونقطة البيع السحابية</span><span class="sxs-lookup"><span data-stu-id="0e4b6-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="0e4b6-154">أفضل ممارسات الأمان لنقطة بيع السحابة في البيئات المشتركة</span><span class="sxs-lookup"><span data-stu-id="0e4b6-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
