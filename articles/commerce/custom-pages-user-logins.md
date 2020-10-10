---
title: إعداد صفحات مخصصه لعمليات تسجيل دخول المستخدمين
description: يوضح هذا الموضوع كيفية إنشاء صفحات مخصصة في Microsoft Dynamics 365 Commerce التي تقوم بمعالجة عمليات تسجيل الدخول المخصصة لمستخدمي مستأجري ميزة عمل-مستهلك (B2C) في Azure Active Directory (Azure AD).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0b54bf6234dcb87c84b21259c30ca5c321869adf
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817296"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="3c715-103">إعداد صفحات مخصصه لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="3c715-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3c715-104">يوضح هذا الموضوع كيفية إنشاء صفحات مخصصة في Microsoft Dynamics 365 Commerce التي تقوم بمعالجة عمليات تسجيل الدخول المخصصة لمستخدمي مستأجري ميزة عمل-مستهلك (B2C) في Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="3c715-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="3c715-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="3c715-105">Overview</span></span>

<span data-ttu-id="3c715-106">لاستخدام الصفحات المخصصة المؤلفة في Dynamics 365 Commerce لمعالجة تدفقات تسجيل دخول المستخدم، ويجب إعداد سياسات Azure AD التي سيتم الرجوع إليها في بيئة التجارة.</span><span class="sxs-lookup"><span data-stu-id="3c715-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="3c715-107">يمكنك تكوين سياسات "تسجيل الاشتراك وتسجيل الدخول،" وسياسات تطبيق B2C Azure AD لخصائص "تحرير ملف التعريف" و"إعادة تعيين كلمه المرور" باستخدام تطبيق Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="3c715-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="3c715-108">ويمكن بعد ذلك الرجوع إلى مستأجر Azure AD B2C وأسماء السياسات أثناء عملية التوفير التي تمت لبيئة التجارة باستخدام Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3c715-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3c715-109">يمكن إنشاء صفحات التجارة المخصصة باستخدام تسجيل الدخول، أو التسجيل الاشتراك، أو تحرير ملف تعريف الحساب، أو الوحدة النمطية لإعادة تعيين كلمه المرور.</span><span class="sxs-lookup"><span data-stu-id="3c715-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="3c715-110">بعد ذلك، يجب الرجوع إلى عناوين URL للصفحة التي يتم نشرها لهذه الصفحات المخصصة في تكوينات سياسة Azure AD B2Cفي مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="3c715-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="3c715-111">إعداد سياسات B2C</span><span class="sxs-lookup"><span data-stu-id="3c715-111">Set up B2C policies</span></span>

<span data-ttu-id="3c715-112">بعد إعداد مستأجر Azure AD B2C وربطه ببيئة التجارة الخاصة بك، انتقل إلى صفحة **Azure AD B2C** في مدخل Azure، ثم في القائمة، ضمن **السياسات**، حدد **تدفقات المستخدم (السياسات)**.</span><span class="sxs-lookup"><span data-stu-id="3c715-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![أمر تدفقات المستخدم (السياسات) في القائمة](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="3c715-114">يمكنك الآن تكوين تدفقات تسجيل الدخول لمستخدم "تسجيل الاشتراك وتسجيل الدخول" و "تحرير ملف التعريف" و "إعادة تعيين كلمة المرور".</span><span class="sxs-lookup"><span data-stu-id="3c715-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="3c715-115">تكوين سياسة "تسجيل الاشتراك وتسجيل الدخول"</span><span class="sxs-lookup"><span data-stu-id="3c715-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="3c715-116">لتكوين سياسة "تسجيل الاشتراك وتسجيل الدخول"، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3c715-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="3c715-117">حدد **تدفق مستخدم جديد**، ثم في علامة التبويب **الموصي به** ، حدد سياسة **تسجيل الاشتراك وتسجيل الدخول** .</span><span class="sxs-lookup"><span data-stu-id="3c715-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="3c715-118">أدخل اسمًا للسياسة (على سبيل المثال، **B2C\_1\_1**تسجيل الاشتراك وتسجيل الدخول).</span><span class="sxs-lookup"><span data-stu-id="3c715-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="3c715-119">في المقطع **موفري الهوية** ، حدد موفرو الهوية المراد استخدامهم للسياسة.</span><span class="sxs-lookup"><span data-stu-id="3c715-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="3c715-120">يجب تحديد على الأقل **تسجيل الاشتراك بالبريد الإلكتروني** .</span><span class="sxs-lookup"><span data-stu-id="3c715-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="3c715-121">في العمود **سمة التجميع** ، حدد خانات الاختيار لـ **عنوان البريد الكتروني**،و **الاسم المحدد**، و **اللقب**.</span><span class="sxs-lookup"><span data-stu-id="3c715-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="3c715-122">في العمود **إرجاع مطالبة** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني**، و **الاسم المحدد**، و **موفر الهوية**، و **اللقب**، و **معرف الكائن الخاص بالمستخدم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![تحديد السمات والمطالبات](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="3c715-124">حدد **موافق** لإنشاء السياسة.</span><span class="sxs-lookup"><span data-stu-id="3c715-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="3c715-125">انقر نقرا مزدوجًا فوق اسم السياسة الجديدة، ثم في جزء التنقل ،حدد **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="3c715-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="3c715-126">قم بتعيين خيار **تمكين JavaScript لتخطيط الصفحة (معاينة)** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="3c715-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![صفحه الخصائص للسياسة الجديدة](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="3c715-128">سيتم الإشارة إلى اسم السياسة بشكل كامل في بيئة التجارة.</span><span class="sxs-lookup"><span data-stu-id="3c715-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="3c715-129">(سوف يتم تضمين البادئة **B2C\_1\_** في المرجع.) ولا يمكن إعادة تسمية السياسة بعد إنشائها.</span><span class="sxs-lookup"><span data-stu-id="3c715-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="3c715-130">إذا كنت تستبدل سياسة موجودة لبيئة التجارة الخاصة بك، فيمكنك حذف السياسة الأصلية وإنشاء سياسة جديدة لها نفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="3c715-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="3c715-131">وبدلاً من ذلك، إذا تم توفير البيئة بالفعل، فيمكنك توفير اسم السياسة الجديدة من خلال طلب خدمة.</span><span class="sxs-lookup"><span data-stu-id="3c715-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="3c715-132">سوف تعود إلى هذه السياسة لإنهاء الإعداد بعد إنشاء الصفحات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="3c715-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="3c715-133">والآن، قم بإغلاق السياسة للعودة إلى صفحة **تدفقات المستخدم (السياسات)** في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="3c715-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="3c715-134">تكوين سياسة "تحرير ملف التعريف"</span><span class="sxs-lookup"><span data-stu-id="3c715-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="3c715-135">لتكوين سياسة "تحرير ملف التعريف"، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="3c715-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="3c715-136">حدد **تدفق مستخدم جديد**، ثم في علامة التبويب **مستحسن** ، حدد سياسة **تحرير ملف التعريف** .</span><span class="sxs-lookup"><span data-stu-id="3c715-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="3c715-137">ادخل اسمًا للسياسة (على سبيل المثال، **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="3c715-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="3c715-138">في المقطع **موفري الهوية** ، حدد موفرو الهوية المراد استخدامهم للسياسة.</span><span class="sxs-lookup"><span data-stu-id="3c715-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="3c715-139">يجب تحديد **تسجيل الدخول للحساب المحلي** كحد أدني.</span><span class="sxs-lookup"><span data-stu-id="3c715-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="3c715-140">في العمود **سمة التجميع** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني** و **اللقب**.</span><span class="sxs-lookup"><span data-stu-id="3c715-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="3c715-141">في العمود **إرجاع مطالبة** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني**، و **الاسم المحدد**، و **موفر الهوية**، و **اللقب**، و **معرف الكائن الخاص بالمستخدم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="3c715-142">حدد **موافق** لإنشاء السياسة.</span><span class="sxs-lookup"><span data-stu-id="3c715-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="3c715-143">انقر نقرا مزدوجًا فوق اسم السياسة الجديدة، ثم في جزء التنقل ،حدد **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="3c715-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="3c715-144">قم بتعيين خيار **تمكين JavaScript لتخطيط الصفحة (معاينة)** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="3c715-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="3c715-145">سوف تعود إلى هذه السياسة لإنهاء الإعداد بعد إنشاء الصفحات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="3c715-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="3c715-146">والآن، قم بإغلاق السياسة للعودة إلى صفحة **تدفقات المستخدم (السياسات)** في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="3c715-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="3c715-147">تكوين سياسة "إعادة تعيين كلمه المرور"</span><span class="sxs-lookup"><span data-stu-id="3c715-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="3c715-148">لتكوين سياسة "إعادة تعيين كلمة المرور"، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="3c715-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="3c715-149">حدد **تدفق مستخدم جديد**، ثم في علامة التبويب **معاينة** ، حدد سياسة **إعادة تعيين كلمة المرور الإصدار 1.1** .</span><span class="sxs-lookup"><span data-stu-id="3c715-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![سياسة إعادة تعيين كلمة المرور في الإصدار 1.1 في علامة التبويب مُعاينة](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="3c715-151">أدخل اسمًا للسياسة (على سبيل المثال، **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="3c715-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="3c715-152">في القسم **موفرو الهوية** ، حدد **إعادة تعيين كلمة المرور باستخدام عنوان البريد الكتروني**.</span><span class="sxs-lookup"><span data-stu-id="3c715-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="3c715-153">في العمود **إرجاع مطالبة** ، حدد خانات الاختيار لـ **عناوين البريد الإلكتروني**، و **الاسم المحدد**، و **اللقب**، و **معرف الكائن الخاص بالمستخدم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![المطالبات المحددة](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="3c715-155">حدد **موافق** لإنشاء السياسة.</span><span class="sxs-lookup"><span data-stu-id="3c715-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="3c715-156">انقر نقرا مزدوجًا فوق اسم السياسة الجديدة، ثم في جزء التنقل ،حدد **خصائص**.</span><span class="sxs-lookup"><span data-stu-id="3c715-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="3c715-157">قم بتعيين خيار **تمكين JavaScript لتخطيط الصفحة (معاينة)** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="3c715-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="3c715-158">سوف تعود إلى هذه السياسة لإنهاء الإعداد بعد إنشاء الصفحات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="3c715-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="3c715-159">والآن، قم بإغلاق السياسة للعودة إلى صفحة **تدفقات المستخدم (السياسات)** في مدخل Azure.</span><span class="sxs-lookup"><span data-stu-id="3c715-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="3c715-160">إنشاء صفحات مخصصة</span><span class="sxs-lookup"><span data-stu-id="3c715-160">Build the custom pages</span></span>

<span data-ttu-id="3c715-161">لإنشاء الصفحات المخصصة للتعامل مع وظائف تسجيل الدخول الخاصة بالمستخدم، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3c715-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="3c715-162">في أدوات التأليف الخاصة بـ Commerce، انتقل إلى الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="3c715-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="3c715-163">بناء القوالب الخمسة والصفحات الخمسة التالية:</span><span class="sxs-lookup"><span data-stu-id="3c715-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="3c715-164">قالب وصفحة **تسجيل الدخول** التي تستخدم الوحدة النمطية تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="3c715-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="3c715-165">قالب وصفحة **تسجيل الاشتراك** التي تستخدم الوحدة النمطية تسجيل الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="3c715-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="3c715-166">قالب وصفحة **إعادة تعيين كلمة المرور** والتي تستخدم الوحدة النمطية إعادة تعيين كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="3c715-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="3c715-167">قالب وصفحة **التحقق من إعادة تعيين كلمة المرور** والتي تستخدم الوحدة النمطية التحقق من إعادة تعيين كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="3c715-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="3c715-168">قالب وصفحة **تحرير ملف التعريف** التي تستخدم الوحدة النمطية تحرير ملف تعريف الحساب.</span><span class="sxs-lookup"><span data-stu-id="3c715-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="3c715-169">عند إنشاء الصفحات، اتبع الإرشادات التالية:</span><span class="sxs-lookup"><span data-stu-id="3c715-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="3c715-170">لكل صفحة أو وحدة نمطية، استخدم التخطيط والنمط الأكثر ملائمة لمتطلبات أعمالك.</span><span class="sxs-lookup"><span data-stu-id="3c715-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="3c715-171">انشر كافة الصفحات وعناوين URL التي يجب استخدامها في إعداد Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="3c715-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="3c715-172">بعد نشر الصفحات وعناوين URL، قم بتجميع عناوين URL التي يجب استخدامها لتكوينات سياسة Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="3c715-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="3c715-173">تتم إضافة اللاحقة **?preloadscripts=true** إلى كل عنوان URL عند استخدامه.</span><span class="sxs-lookup"><span data-stu-id="3c715-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c715-174">لا تعيد استخدام العناوين والتذييلات العامة التي لها ارتباطات نسبية.</span><span class="sxs-lookup"><span data-stu-id="3c715-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="3c715-175">ونظرًا لاستضافة هذه الصفحات في المجال Azure AD B2C عند استخدامها، يجب فقط استخدام عناوين URL المطلقة لكافة الارتباطات.</span><span class="sxs-lookup"><span data-stu-id="3c715-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="3c715-176">تكوين سياسات Azure AD B2C باستخدام معلومات صفحة مخصصة</span><span class="sxs-lookup"><span data-stu-id="3c715-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="3c715-177">في مدخل Azure، ارجع إلى الصفحة **Azure AD B2C** ، ثم في القائمة، تحت **السياسات**، حدد **تدفقات المستخدم (السياسات)**.</span><span class="sxs-lookup"><span data-stu-id="3c715-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="3c715-178">تحديث سياسة "تسجيل الاشتراك وتسجيل الدخول" باستخدام معلومات الصفحة المخصصة</span><span class="sxs-lookup"><span data-stu-id="3c715-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="3c715-179">لتحديث سياسة "تسجيل الاشتراك وتسجيل الدخول" باستخدام معلومات الصفحة المخصصة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3c715-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="3c715-180">في سياسة **تسجيل الاشتراك وتسجيل الدخول** التي قمت بتكوينها سابقًا، في جزء التنقل ، حدد **تخطيطات الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="3c715-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="3c715-181">حدد تخطيط صفحة **تسجيل الاشتراك وتسجيل الدخول** .</span><span class="sxs-lookup"><span data-stu-id="3c715-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="3c715-182">قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c715-183">في الحقل **URI للصفحة المخصصة** ، ادخل عنوان URL لتسجيل الدخول الكامل.</span><span class="sxs-lookup"><span data-stu-id="3c715-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="3c715-184">ضمن اللاحقة **?preloadscripts=true** .</span><span class="sxs-lookup"><span data-stu-id="3c715-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c715-185">على سبيل المثال، أدخل ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="3c715-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c715-186">في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="3c715-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c715-187">حدد تخطيط **صفحة تسجيل الدخول بالحساب المحلي** .</span><span class="sxs-lookup"><span data-stu-id="3c715-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="3c715-188">قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c715-189">في الحقل **عنوان URI للصفحة المخصصة** ، ادخل عنوان URL للتسجيل الكامل للدخول.</span><span class="sxs-lookup"><span data-stu-id="3c715-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="3c715-190">ضمن اللاحقة **?preloadscripts=true** .</span><span class="sxs-lookup"><span data-stu-id="3c715-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c715-191">على سبيل المثال، أدخل ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="3c715-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c715-192">في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="3c715-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c715-193">في القسم **سمات المستخدم** ، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="3c715-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="3c715-194">بالنسبة **لعنوان البريد الكتروني**، و **الاسم المحدد**، وسمات **اللقب** ، حدد **لا** في الحقل **يتطلب إجراء عملية تحقق**.</span><span class="sxs-lookup"><span data-stu-id="3c715-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="3c715-195">بالنسبة لـ **الاسم المحدد** وسمات **اللقب** ، حدد **لا** في الحقل **اختياري** .</span><span class="sxs-lookup"><span data-stu-id="3c715-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![تكوين سياسة صفحة تسجيل الدخول بالحساب المحلي](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="3c715-197">تحديث سياسة "تحرير ملف التعريف" باستخدام معلومات الصفحة المخصصة</span><span class="sxs-lookup"><span data-stu-id="3c715-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="3c715-198">لتحديث سياسة "تحرير ملف التعريف" باستخدام معلومات الصفحة المخصصة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3c715-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="3c715-199">في سياسة **تحرير ملف التعريف** الذي قمت بتكوينه سابقًا، في جزء التنقل، حدد **تخطيطات الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="3c715-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="3c715-200">حدد تخطيط **صفحة تحرير ملف التعريف** .</span><span class="sxs-lookup"><span data-stu-id="3c715-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="3c715-201">قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c715-202">في الحقل **عنوان URI للصفحة المخصصة** ، أدخل عنوان URL الكامل لتعديل الملف الشخصي.</span><span class="sxs-lookup"><span data-stu-id="3c715-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="3c715-203">ضمن اللاحقة **?preloadscripts=true** .</span><span class="sxs-lookup"><span data-stu-id="3c715-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c715-204">على سبيل المثال، أدخل ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="3c715-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c715-205">في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="3c715-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c715-206">في القسم **سمات المستخدم** ، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="3c715-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="3c715-207">بالنسبة لـ **عنوان البريد الكتروني**، وسمات **الاسم المحدد** ، حدد **لا** في الحقل **يتطلب إجراء عملية تحقق** .</span><span class="sxs-lookup"><span data-stu-id="3c715-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="3c715-208">بالنسبة لـ **الاسم المحدد** وسمات **اللقب** ، حدد **لا** في الحقل **اختياري** .</span><span class="sxs-lookup"><span data-stu-id="3c715-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="3c715-209">تحديث سياسة "إعادة تعيين كلمة المرور" باستخدام معلومات الصفحة المخصصة</span><span class="sxs-lookup"><span data-stu-id="3c715-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="3c715-210">لتحديث سياسة "إعادة تعيين كلمة المرور" باستخدام معلومات الصفحة المخصصة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="3c715-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="3c715-211">في سياسة **إعادة تعيين كلمة المرور** الذي قمت بتكوينه سابقًا، في جزء التنقل، حدد **تخطيطات الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="3c715-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="3c715-212">حدد تخطيط **صفحة كلمة المرور الجديدة** .</span><span class="sxs-lookup"><span data-stu-id="3c715-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="3c715-213">قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c715-214">في الحقل **عنوان URI للصفحة المخصصة** ، أدخل عنوان URL الكامل لإعادة تعيين كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="3c715-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="3c715-215">ضمن اللاحقة **?preloadscripts=true** .</span><span class="sxs-lookup"><span data-stu-id="3c715-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c715-216">على سبيل المثال، أدخل ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="3c715-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c715-217">في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="3c715-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="3c715-218">حدد تخطيط **صفحة التحقق من الحساب** .</span><span class="sxs-lookup"><span data-stu-id="3c715-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="3c715-219">قم بتعيين الخيار **استخدام محتوي صفحة مخصصة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3c715-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="3c715-220">في الحقل **عنوان URI للصفحة المخصصة** ، أدخل عنوان URL الكامل لإعادة التحقق من كلمة المرور.</span><span class="sxs-lookup"><span data-stu-id="3c715-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="3c715-221">ضمن اللاحقة **?preloadscripts=true** .</span><span class="sxs-lookup"><span data-stu-id="3c715-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="3c715-222">على سبيل المثال، أدخل ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="3c715-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="3c715-223">في الحقل **إصدار تخطيط الصفحة (معاينة)** ، حدد **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="3c715-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="3c715-224">تخصيص السلاسل النصية الافتراضية للتسميات والأوصاف</span><span class="sxs-lookup"><span data-stu-id="3c715-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="3c715-225">في مكتبة الوحدات النمطية، تتم تعبئة وحدات تسجيل الدخول النمطية مسبقًا باستخدام سلاسل نصية افتراضية للتسميات والأوصاف.</span><span class="sxs-lookup"><span data-stu-id="3c715-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="3c715-226">يمكنك تخصيص هذه السلاسل في مجموعه تطوير البرامج (SDK) عن طريق تحديث القيم الموجودة في ملف global.json الخاص بتسجيل الدخول في الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="3c715-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="3c715-227">على سبيل المثال، يكون النص الافتراضي لارتباط كلمة المرور المنسية هو **كلمه المرور المنسية؟**.</span><span class="sxs-lookup"><span data-stu-id="3c715-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="3c715-228">فيما يلي يظهر النص الافتراضي في صفحة تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="3c715-228">The following shows this default text on the sign-in page.</span></span>

![النص الافتراضي لارتباط كلمة المرور المنسية في صفحة تسجيل الدخول](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="3c715-230">ومع ذلك، في ملف global.json للوحدة النمطية لتسجيل الدخول إلى مكتبة الوحدات النمطية، يمكنك تحرير النص إلى **هل نسيت كلمة المرور؟**، كما هو مبين في التوضيح التالي.</span><span class="sxs-lookup"><span data-stu-id="3c715-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![تم تحديث نص الارتباط في ملف global.json الخاص بالوحدة النمطية تسجيل الدخول](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="3c715-232">بعد تحديث ملف global.json ونشر التغييرات، يظهر نص الارتباط الجديد في الوحدة النمطية تسجيل الدخول في كل من Commerce وصفحة تسجيل الدخول المباشر.</span><span class="sxs-lookup"><span data-stu-id="3c715-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c715-233">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="3c715-233">Additional resources</span></span>

[<span data-ttu-id="3c715-234">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="3c715-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3c715-235">نشر موقع تجارة إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="3c715-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3c715-236">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="3c715-236">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3c715-237">إقران موقع عبر الإنترنت بقناة</span><span class="sxs-lookup"><span data-stu-id="3c715-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3c715-238">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="3c715-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3c715-239">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="3c715-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="3c715-240">إعداد مستأجر B2C في Commerce</span><span class="sxs-lookup"><span data-stu-id="3c715-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3c715-241">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="3c715-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="3c715-242">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="3c715-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3c715-243">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="3c715-243">Enable location-based store detection</span></span>](enable-store-detection.md)
