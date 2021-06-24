---
title: فتح عنوان URL في نقطة البيع
description: يوفر هذا الموضوع نظرة عامة حول التحسينات التي تم إدخالها على وظيفة البحث عن المنتجات والعملاء في  Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193193"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="4ddad-103">فتح عنوان URL في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="4ddad-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ddad-104">يتناول هذا الموضوع كيفية تكوين زر في نقطة بيع (POS) Dynamics 365 Commerce لفتح عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="4ddad-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="4ddad-105">لا تتطلب هذه الميزة تخصيصات الأكواد، ويمكن لأي شخص لا يتمتع بدور مطور تكوينها.</span><span class="sxs-lookup"><span data-stu-id="4ddad-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="4ddad-106">تسمح هذه الميزة بتكوين زر في نقطة بيع، باستخدام مصمم شبكة الزر لفتح عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="4ddad-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="4ddad-107">وفي الوقت الحالي، هذه الميزة مدعومة في التكوينات التالية:</span><span class="sxs-lookup"><span data-stu-id="4ddad-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="4ddad-108">فتح في نافذة جديدة.</span><span class="sxs-lookup"><span data-stu-id="4ddad-108">Open in new window.</span></span>
- <span data-ttu-id="4ddad-109">فتح في نقطة بيع.</span><span class="sxs-lookup"><span data-stu-id="4ddad-109">Open within POS.</span></span>
- <span data-ttu-id="4ddad-110">فتح تطبيق أصلي.</span><span class="sxs-lookup"><span data-stu-id="4ddad-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="4ddad-111">فتح في نافذة جديدة</span><span class="sxs-lookup"><span data-stu-id="4ddad-111">Open in new window</span></span>

<span data-ttu-id="4ddad-112">يُحدد هذا التكوين ما إذا كنت تريد فتح عنوان URL في نافذة جديدة أو داخل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="4ddad-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="4ddad-113">عندما يتم تكوين ميزة لفتح عنوان URL خاص بموقع ويب داخل التطبيق، تكون لوحة التنقل الجانبية والشريط العلوي لنقطة البيع مرئية ومتاحة لتفاعل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4ddad-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="4ddad-114">عندما يتم تكوين هذه الميزة لفتحها في نافذة جديدة، فسوف يفتح عنوان URL في نافذة تطبيق جديدة في نقطة بيع حديثة لنافذة، وفي علامة تبويب مستعرض جديدة في جميع عملاء نقطة البيع الآخرين.</span><span class="sxs-lookup"><span data-stu-id="4ddad-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="4ddad-115">لتمكين هذه الميزة، يجب عليك تكوين عنوان URL باستخدام خيار **فتح في نافذة جديدة** المحدد.</span><span class="sxs-lookup"><span data-stu-id="4ddad-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="4ddad-116">فتح في نقطة بيع</span><span class="sxs-lookup"><span data-stu-id="4ddad-116">Open within POS</span></span>

<span data-ttu-id="4ddad-117">يتم حاليًا دعم ميزة فتح عنوان URL خاص بويب في نقطة بيع فقط لنقطة البيع الحديثة في Windows.</span><span class="sxs-lookup"><span data-stu-id="4ddad-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="4ddad-118">بالنسبة للعملاء الآخرين، فإن هذه الإمكانية قيد التطوير ومُخطط لإصدارها في التحديثات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="4ddad-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="4ddad-119">لتمكين هذه الميزة، يجب عليك تكوين عنوان URL باستخدام خيار **فتح في نافذة جديدة** غير المُحدد.</span><span class="sxs-lookup"><span data-stu-id="4ddad-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="4ddad-120">فتح تطبيق أصلي</span><span class="sxs-lookup"><span data-stu-id="4ddad-120">Open a native app</span></span>

<span data-ttu-id="4ddad-121">تسمح هذه الميزة أيضًا بتحديد عناوين URL غير التابعة لعنوان ويب لفتح تطبيق أصلي.</span><span class="sxs-lookup"><span data-stu-id="4ddad-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="4ddad-122">على سبيل المثال، يمكنك تحديد بروتوكلات عنوان URL مثل MailTo أو SIP أو IM أو MSTEAMS، والتي يمكن التعامل معها بعد ذلك من خلال التطبيقات الأصلية الخاصة بها على الجهاز المضيف.</span><span class="sxs-lookup"><span data-stu-id="4ddad-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="4ddad-123">لتمكين هذه الميزة، يجب عليك تكوين عنوان URL باستخدام خيار **فتح في نافذة جديدة** المحدد.</span><span class="sxs-lookup"><span data-stu-id="4ddad-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="4ddad-124">بالنسبة لأجهزة الكمبيوتر التي تعمل بنظام تشغيل Windows، راجع [تصدير أو استيراد اقترانات التطبيقات الافتراضية ](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) لتعيين اقترانات البروتوكولات الاافتراضية إذا كنت تقوم بإعداد جهاز الكمبيوتر باستخدام خدمة نشر الصورة والإدارة (DISM).</span><span class="sxs-lookup"><span data-stu-id="4ddad-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="4ddad-125">إذا كنت تستخدم MDM، مثل Intune لإدارة أجهزة الكمبيوتر التي تعمل بنظام التشغيل Windows، راجع [سياسة CSP-ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="4ddad-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="4ddad-126">إذا كنت مطورًا تقوم بإنشاء موقع ويب مخصص، راجع [تشغيل التطبيق الافتراضي لعنوان URI](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="4ddad-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="4ddad-127">فتح تطبيق أصلي بسلاسة</span><span class="sxs-lookup"><span data-stu-id="4ddad-127">Open a native app seamlessly</span></span>

<span data-ttu-id="4ddad-128">تسمح أيضًا أنظمة التشغيل Windows وIOS وAndroid بفتح التطبيقات بطريقة أكثر سلاسة، استنادًا إلى اقتران بروتوكول التطبيق.</span><span class="sxs-lookup"><span data-stu-id="4ddad-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="4ddad-129">إذا لم يتم تكوين تطبيقك لمعالجة الفتح من مستعرض ويب مسبقًا، فقد تحتاج إلى مطور لتكوين هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="4ddad-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="4ddad-130">لأنظمة تشغيل Windows، راجع [تمكين التطبيقات لمواقع ويب باستخدام معالجات URI للتطبيق](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="4ddad-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="4ddad-131">لنظام تشغيل iOS، راجع [الارتباطات العالمية للمطورين](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="4ddad-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="4ddad-132">بالنسبة إلى نظام Android، راجع [معالجة ارتباطات تطبيق Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="4ddad-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="4ddad-133">العميل</span><span class="sxs-lookup"><span data-stu-id="4ddad-133">Client</span></span>                | <span data-ttu-id="4ddad-134">فتح في نافذة جديدة</span><span class="sxs-lookup"><span data-stu-id="4ddad-134">Open in new window</span></span> | <span data-ttu-id="4ddad-135">فتح تطبيق أصلي</span><span class="sxs-lookup"><span data-stu-id="4ddad-135">Open native app</span></span> | <span data-ttu-id="4ddad-136">فتح في نقطة بيع</span><span class="sxs-lookup"><span data-stu-id="4ddad-136">Open within POS</span></span> | <span data-ttu-id="4ddad-137">التفاصيل</span><span class="sxs-lookup"><span data-stu-id="4ddad-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="4ddad-138">نقطة بيع حديثة في نظام تشغيل Windows</span><span class="sxs-lookup"><span data-stu-id="4ddad-138">Modern POS on Windows</span></span> | <span data-ttu-id="4ddad-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ddad-139">✓\*</span></span>                | <span data-ttu-id="4ddad-140">✓</span><span class="sxs-lookup"><span data-stu-id="4ddad-140">✓</span></span>               | <span data-ttu-id="4ddad-141">✓</span><span class="sxs-lookup"><span data-stu-id="4ddad-141">✓</span></span>              | <span data-ttu-id="4ddad-142">\* فتح في نافذة نقطع بيع حديثة</span><span class="sxs-lookup"><span data-stu-id="4ddad-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="4ddad-143">نقطة بيع المجموعة‬</span><span class="sxs-lookup"><span data-stu-id="4ddad-143">Cloud POS</span></span>             | <span data-ttu-id="4ddad-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ddad-144">✓\*</span></span>                | <span data-ttu-id="4ddad-145">✓</span><span class="sxs-lookup"><span data-stu-id="4ddad-145">✓</span></span>               | <span data-ttu-id="4ddad-146">س</span><span class="sxs-lookup"><span data-stu-id="4ddad-146">X</span></span>              | <span data-ttu-id="4ddad-147">\* فتح في علامة تبويب مستعرض جديدة</span><span class="sxs-lookup"><span data-stu-id="4ddad-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="4ddad-148">نقطة بيع حديثة في نظام تشغيل iOS</span><span class="sxs-lookup"><span data-stu-id="4ddad-148">Modern POS on iOS</span></span>     | <span data-ttu-id="4ddad-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ddad-149">✓\*</span></span>                | <span data-ttu-id="4ddad-150">✓</span><span class="sxs-lookup"><span data-stu-id="4ddad-150">✓</span></span>               | <span data-ttu-id="4ddad-151">س</span><span class="sxs-lookup"><span data-stu-id="4ddad-151">X</span></span>              | <span data-ttu-id="4ddad-152">\* فتح في علامة تبويب مستعرض جديدة</span><span class="sxs-lookup"><span data-stu-id="4ddad-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="4ddad-153">Modern POS على Android</span><span class="sxs-lookup"><span data-stu-id="4ddad-153">Modern POS on Android</span></span> | <span data-ttu-id="4ddad-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="4ddad-154">✓\*</span></span>                | <span data-ttu-id="4ddad-155">✓</span><span class="sxs-lookup"><span data-stu-id="4ddad-155">✓</span></span>               | <span data-ttu-id="4ddad-156">س</span><span class="sxs-lookup"><span data-stu-id="4ddad-156">X</span></span>              | <span data-ttu-id="4ddad-157">\* فتح في علامة تبويب مستعرض جديدة</span><span class="sxs-lookup"><span data-stu-id="4ddad-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="4ddad-158">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="4ddad-158">Before you begin</span></span>

<span data-ttu-id="4ddad-159">قبل أن تبدأ، راجع كيفية تكوين [تخطيطات الشاشة لنقطة بيع (POS)](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="4ddad-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="4ddad-160">فتح عنوان URL في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="4ddad-160">Open URL in POS</span></span>

<span data-ttu-id="4ddad-161">لتكوين عنوان URL ليتم فتحه في نقطة بيع، نفذ الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="4ddad-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="4ddad-162">في المكتب الرئيسي، انتقل إلى **Retail and Commerce \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="4ddad-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="4ddad-163">حدد **شبكات الأزرار \> المصمم‏‎**.</span><span class="sxs-lookup"><span data-stu-id="4ddad-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="4ddad-164">قم بإنشاء زر جديد.</span><span class="sxs-lookup"><span data-stu-id="4ddad-164">Create a new button.</span></span>
4. <span data-ttu-id="4ddad-165">حدد خصائص **الزر**.</span><span class="sxs-lookup"><span data-stu-id="4ddad-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="4ddad-166">حدد **فتح URL** كإجراء.</span><span class="sxs-lookup"><span data-stu-id="4ddad-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="4ddad-167">أدخل عنوان URL الذي ترغب في استخدامه.</span><span class="sxs-lookup"><span data-stu-id="4ddad-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="4ddad-168">قم بتكوين ما إذا كنت تريد فتح عنوان URL في نافذة جديدة أو لا.</span><span class="sxs-lookup"><span data-stu-id="4ddad-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
