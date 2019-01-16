---
title: "فتح عنوان URL في نقطة البيع"
description: "يوفر هذا الموضوع نظرة عامة حول التحسينات التي تم إدخالها على وظيفة البحث عن المنتجات والعملاء في Microsoft Dynamics 365 for Retail."
author: AamirAllaq
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: d2b692ac86244eca31780a558112167391fc6d77
ms.contentlocale: ar-sa
ms.lasthandoff: 01/04/2019

---

# <a name="open-url-in-pos"></a><span data-ttu-id="53ae8-103">فتح عنوان URL في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="53ae8-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="53ae8-104">يتناول هذا الموضوع كيفية تكوين زر في نقطة بيع (POS) البيع بالتجزئة لفتح عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="53ae8-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="53ae8-105">لا تتطلب هذه الميزة تخصيصات الأكواد، ويمكن لأي شخص لا يتمتع بدور مطور تكوينها.</span><span class="sxs-lookup"><span data-stu-id="53ae8-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span>

<span data-ttu-id="53ae8-106">تسمح هذه الميزة بتكوين زر في نقطة بيع، باستخدام مصمم شبكة الزر لفتح عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="53ae8-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="53ae8-107">وفي الوقت الحالي، هذه الميزة مدعومة في التكوينات التالية:</span><span class="sxs-lookup"><span data-stu-id="53ae8-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="53ae8-108">فتح في نافذة جديدة.</span><span class="sxs-lookup"><span data-stu-id="53ae8-108">Open in new window.</span></span>
- <span data-ttu-id="53ae8-109">فتح في نقطة بيع.</span><span class="sxs-lookup"><span data-stu-id="53ae8-109">Open within POS.</span></span>
- <span data-ttu-id="53ae8-110">فتح تطبيق أصلي.</span><span class="sxs-lookup"><span data-stu-id="53ae8-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="53ae8-111">فتح في نافذة جديدة</span><span class="sxs-lookup"><span data-stu-id="53ae8-111">Open in new window</span></span>

<span data-ttu-id="53ae8-112">يُحدد هذا التكوين ما إذا كنت تريد فتح عنوان URL في نافذة جديدة أو داخل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="53ae8-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="53ae8-113">عندما يتم تكوين ميزة لفتح عنوان URL خاص بموقع ويب داخل التطبيق، تكون لوحة التنقل الجانبية والشريط العلوي لنقطة البيع مرئية ومتاحة لتفاعل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="53ae8-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="53ae8-114">عندما يتم تكوين هذه الميزة لفتحها في نافذة جديدة، فسوف يفتح عنوان URL في نافذة تطبيق جديدة في نقطة بيع حديثة لنافذة، وفي علامة تبويب مستعرض جديدة في جميع عملاء نقطة البيع الآخرين.</span><span class="sxs-lookup"><span data-stu-id="53ae8-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="53ae8-115">لتمكين هذه الميزة، يجب عليك تكوين عنوان URL باستخدام خيار **فتح في نافذة جديدة** المحدد.</span><span class="sxs-lookup"><span data-stu-id="53ae8-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="53ae8-116">فتح في نقطة بيع</span><span class="sxs-lookup"><span data-stu-id="53ae8-116">Open within POS</span></span>

<span data-ttu-id="53ae8-117">يتم حاليًا دعم ميزة فتح عنوان URL خاص بويب في نقطة بيع فقط لنقطة البيع الحديثة في Windows.</span><span class="sxs-lookup"><span data-stu-id="53ae8-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="53ae8-118">بالنسبة للعملاء الآخرين، فإن هذه الإمكانية قيد التطوير ومُخطط لإصدارها في التحديثات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="53ae8-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="53ae8-119">لتمكين هذه الميزة، يجب عليك تكوين عنوان URL باستخدام خيار **فتح في نافذة جديدة** غير المُحدد.</span><span class="sxs-lookup"><span data-stu-id="53ae8-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="53ae8-120">فتح تطبيق أصلي</span><span class="sxs-lookup"><span data-stu-id="53ae8-120">Open a native app</span></span>

<span data-ttu-id="53ae8-121">تسمح هذه الميزة أيضًا بتحديد عناوين URL غير التابعة لعنوان ويب لفتح تطبيق أصلي.</span><span class="sxs-lookup"><span data-stu-id="53ae8-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="53ae8-122">على سبيل المثال، يمكنك تحديد بروتوكلات عنوان URL مثل MailTo أو SIP أو IM أو MSTEAMS، والتي يمكن التعامل معها بعد ذلك من خلال التطبيقات الأصلية الخاصة بها على الجهاز المضيف.</span><span class="sxs-lookup"><span data-stu-id="53ae8-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="53ae8-123">لتمكين هذه الميزة، يجب عليك تكوين عنوان URL باستخدام خيار **فتح في نافذة جديدة** المحدد.</span><span class="sxs-lookup"><span data-stu-id="53ae8-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="53ae8-124">بالنسبة لأجهزة الكمبيوتر التي تعمل بنظام تشغيل Windows ، راجع [تصدير أو استيراد اقترانات التطبيقات الافتراضية ](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) لتعيين اقترانات البروتوكولات الاافتراضية إذا كنت تقوم بإعداد جهاز الكمبيوتر باستخدام خدمة نشر الصورة والإدارة (DISM).</span><span class="sxs-lookup"><span data-stu-id="53ae8-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="53ae8-125">إذا كنت تستخدم MDM، مثل Intune لإدارة أجهزة الكمبيوتر التي تعمل بنظام التشغيل Windows، راجع [سياسة CSP-ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="53ae8-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="53ae8-126">إذا كنت مطورًا تقوم بإنشاء موقع ويب مخصص، راجع [تشغيل التطبيق الافتراضي لعنوان URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="53ae8-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="53ae8-127">فتح تطبيق أصلي بسلاسة</span><span class="sxs-lookup"><span data-stu-id="53ae8-127">Open a native app seamlessly</span></span>

<span data-ttu-id="53ae8-128">تسمح أيضًا نظم التشغيل Windows و IOS و Android بفتح التطبيقات بطريقة أكثر سلاسة، استنادًا إلى اقتران بروتوكول التطبيق.</span><span class="sxs-lookup"><span data-stu-id="53ae8-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="53ae8-129">إذا لم يتم تكوين تطبيقك لمعالجة الفتح من مستعرض ويب مسبقًا، فقد تحتاج إلى مطور لتكوين هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="53ae8-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="53ae8-130">لأنظمة تشغيل Windows، راجع [تمكين التطبيقات لمواقع ويب باستخدام معالجات URI للتطبيق](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="53ae8-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="53ae8-131">لنظام تشغيل iOS، راجع [الارتباطات العالمية للمطورين](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="53ae8-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="53ae8-132">لنظام تشغيل Android، راجع [مُعالجة ارتباطات تطبيق Android](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="53ae8-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="53ae8-133">العميل</span><span class="sxs-lookup"><span data-stu-id="53ae8-133">Client</span></span>                | <span data-ttu-id="53ae8-134">فتح في نافذة جديدة</span><span class="sxs-lookup"><span data-stu-id="53ae8-134">Open in new window</span></span> | <span data-ttu-id="53ae8-135">فتح تطبيق أصلي</span><span class="sxs-lookup"><span data-stu-id="53ae8-135">Open native app</span></span> | <span data-ttu-id="53ae8-136">فتح في نقطة بيع</span><span class="sxs-lookup"><span data-stu-id="53ae8-136">Open within POS</span></span> | <span data-ttu-id="53ae8-137">التفاصيل</span><span class="sxs-lookup"><span data-stu-id="53ae8-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="53ae8-138">نقطة بيع حديثة في نظام تشغيل Windows</span><span class="sxs-lookup"><span data-stu-id="53ae8-138">Modern POS on Windows</span></span> | <span data-ttu-id="53ae8-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="53ae8-139">✓\*</span></span>                | <span data-ttu-id="53ae8-140">✓</span><span class="sxs-lookup"><span data-stu-id="53ae8-140">✓</span></span>               | <span data-ttu-id="53ae8-141">✓</span><span class="sxs-lookup"><span data-stu-id="53ae8-141">✓</span></span>              | <span data-ttu-id="53ae8-142">\* فتح في نافذة نقطع بيع حديثة</span><span class="sxs-lookup"><span data-stu-id="53ae8-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="53ae8-143">نقطة بيع المجموعة‬</span><span class="sxs-lookup"><span data-stu-id="53ae8-143">Cloud POS</span></span>             | <span data-ttu-id="53ae8-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="53ae8-144">✓\*</span></span>                | <span data-ttu-id="53ae8-145">✓</span><span class="sxs-lookup"><span data-stu-id="53ae8-145">✓</span></span>               | <span data-ttu-id="53ae8-146">س</span><span class="sxs-lookup"><span data-stu-id="53ae8-146">X</span></span>              | <span data-ttu-id="53ae8-147">\* فتح في علامة تبويب مستعرض جديدة</span><span class="sxs-lookup"><span data-stu-id="53ae8-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="53ae8-148">نقطة بيع حديثة في نظام تشغيل iOS</span><span class="sxs-lookup"><span data-stu-id="53ae8-148">Modern POS on iOS</span></span>     | <span data-ttu-id="53ae8-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="53ae8-149">✓\*</span></span>                | <span data-ttu-id="53ae8-150">✓</span><span class="sxs-lookup"><span data-stu-id="53ae8-150">✓</span></span>               | <span data-ttu-id="53ae8-151">س</span><span class="sxs-lookup"><span data-stu-id="53ae8-151">X</span></span>              | <span data-ttu-id="53ae8-152">\* فتح في علامة تبويب مستعرض جديدة</span><span class="sxs-lookup"><span data-stu-id="53ae8-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="53ae8-153">نقطة بيع حديثة في نظام التشغيل Android</span><span class="sxs-lookup"><span data-stu-id="53ae8-153">Modern POS on Android</span></span> | <span data-ttu-id="53ae8-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="53ae8-154">✓\*</span></span>                | <span data-ttu-id="53ae8-155">✓</span><span class="sxs-lookup"><span data-stu-id="53ae8-155">✓</span></span>               | <span data-ttu-id="53ae8-156">س</span><span class="sxs-lookup"><span data-stu-id="53ae8-156">X</span></span>              | <span data-ttu-id="53ae8-157">\* فتح في علامة تبويب مستعرض جديدة</span><span class="sxs-lookup"><span data-stu-id="53ae8-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="53ae8-158">قبل البدء</span><span class="sxs-lookup"><span data-stu-id="53ae8-158">Before you begin</span></span>

<span data-ttu-id="53ae8-159">قبل أن تبدأ، راجع كيفية تكوين [تخطيطات الشاشة لنقطة بيع (POS)](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="53ae8-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="53ae8-160">فتح عنوان URL في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="53ae8-160">Open URL in POS</span></span>

<span data-ttu-id="53ae8-161">لتكوين عنوان URL ليتم فتحه في نقطة بيع، نفذ الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="53ae8-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="53ae8-162">في المكتب الرئيسي، انتقل إلى **البيع بالتجزئة \> إعداد القناة \> إعداد نقطة البيع \> نقطة البيع \> تخطيطات الشاشة**.</span><span class="sxs-lookup"><span data-stu-id="53ae8-162">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="53ae8-163">حدد **شبكات الأزرار \> المصمم‏‎**.</span><span class="sxs-lookup"><span data-stu-id="53ae8-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="53ae8-164">قم بإنشاء زر جديد.</span><span class="sxs-lookup"><span data-stu-id="53ae8-164">Create a new button.</span></span>
4. <span data-ttu-id="53ae8-165">حدد خصائص **الزر**.</span><span class="sxs-lookup"><span data-stu-id="53ae8-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="53ae8-166">حدد **فتح URL** كإجراء.</span><span class="sxs-lookup"><span data-stu-id="53ae8-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="53ae8-167">أدخل عنوان URL الذي ترغب في استخدامه.</span><span class="sxs-lookup"><span data-stu-id="53ae8-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="53ae8-168">قم بتكوين ما إذا كنت تريد فتح عنوان URL في نافذة جديدة أو لا.</span><span class="sxs-lookup"><span data-stu-id="53ae8-168">Configure whether to open the URL in a new window.</span></span>

