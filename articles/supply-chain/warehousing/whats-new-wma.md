---
title: ما الجديد أو الذي تم تغييره في تطبيق Warehouse Management للأجهزة المحمولة
description: يسرد هذا الموضوع الميزات الجديدة والمتغيرة لكل إصدار تم إصداره من تطبيق Warehouse Management للأجهزة لـ Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261760"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="13299-103">ما الجديد أو الذي تم تغييره في تطبيق Warehouse Management للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="13299-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13299-104">يسرد هذا الموضوع الميزات الجديدة والتحسينات والمشكلات المعروفة لكل إصدار تم إصداره من تطبيق Warehouse Management للأجهزة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="13299-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="13299-105">الإصدار 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="13299-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="13299-106">الميزات الجديدة والإصلاحات والتحسينات في إصدار 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="13299-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="13299-107">يقدم هذا الإصدار الميزات الجديدة والإصلاحات والتحسينات التالية:</span><span class="sxs-lookup"><span data-stu-id="13299-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="13299-108">يعرض وضع العرض التوضيحي الآن كافة التسميات في لغة الجهاز.</span><span class="sxs-lookup"><span data-stu-id="13299-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="13299-109">من المحتمل ظهور رسالة الخطأ التالية بشكل أقل: "يتعذر العثور على طريقة عرض مناسبة للحجم المحدد."</span><span class="sxs-lookup"><span data-stu-id="13299-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="13299-110">لقد تم زيادة الحد الأدنى لارتفاع بطاقات العمل (للحالات التي يتم فيها تكوين ثلاثة حقول أو أقل لتظهر في قائمة العمل).</span><span class="sxs-lookup"><span data-stu-id="13299-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="13299-111">تم تحسين الهوامش (تلاشي للخارج) في أسفل بطاقات التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="13299-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="13299-112">الرموز الموجودة في ملفات XML التي يتم تبادلها مع الخادم تتم معالجتها الآن بأمان.</span><span class="sxs-lookup"><span data-stu-id="13299-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="13299-113">(على سبيل المثال، يتم الآن معالجة الأحرف غير القابلة للطباعة بأمان وبالتالي لم تعد تتسبب في توقف التطبيق عن الاستجابة.)</span><span class="sxs-lookup"><span data-stu-id="13299-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="13299-114">يتم الآن معالجة أخطاء HTTP (مثل "خطأ 503") عند إرسال طلب خادم بأمان.</span><span class="sxs-lookup"><span data-stu-id="13299-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="13299-115">أثناء ظهور خطأ، لا يتم عرض قائمة الخيارات تلقائيًا لعناصر تحكم مربع التحرير والسرد.</span><span class="sxs-lookup"><span data-stu-id="13299-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="13299-116">لم يعد التطبيق يتوقف عن الاستجابة بسبب اتجاه العرض المحدد في إعدادات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="13299-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="13299-117">يتم عرض صور المنتجات الآن في بيئات الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="13299-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="13299-118">(ينطبق هذا التغيير على الإصدارات منخفضة الدقة فقط.</span><span class="sxs-lookup"><span data-stu-id="13299-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="13299-119">لا تدعم خدمة إدارة الملفات الصور كاملة الحجم في بيئات الخدمة الذاتية.)</span><span class="sxs-lookup"><span data-stu-id="13299-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="13299-120">تم إصلاح مشكلة تضمين الانتقاءات القصير ذات الكمية الصفرية.</span><span class="sxs-lookup"><span data-stu-id="13299-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="13299-121">ولم يعد التطبيق يتوقف عن الاستجابة عندما تعرض بطاقة التفاصيل حقولاً متعددة متطابقة.</span><span class="sxs-lookup"><span data-stu-id="13299-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="13299-122">المشكلات المعروفة في الإصدار 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="13299-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="13299-123">توجد المشكلات المعروفة التالية في هذا الإصدار:</span><span class="sxs-lookup"><span data-stu-id="13299-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="13299-124">يصبح التطبيق (بشكل خاص قائمة العمل) أبطأ بمرور الوقت.</span><span class="sxs-lookup"><span data-stu-id="13299-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="13299-125">**إصدار Windows:** عند استخدام مسدس USB للمسح الضوئي في برنامج التشغيل Windows، تتسبب النتائج غير المتوافقة في خلط الرموز الممسوحة ضوئيًا.</span><span class="sxs-lookup"><span data-stu-id="13299-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="13299-126">الإصدار 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="13299-126">Version 2.0.5.0</span></span>

<span data-ttu-id="13299-127">يقدم هذا الإصدار الميزات الجديدة والإصلاحات والتحسينات التالية:</span><span class="sxs-lookup"><span data-stu-id="13299-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="13299-128">لم يعد سر العميل مخفيًا في ضبط إعدادات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="13299-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="13299-129">يمكنك الآن القيام بضغطة طويلة على أي نص لرؤيته بالكامل.</span><span class="sxs-lookup"><span data-stu-id="13299-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="13299-130">تم تحسين رسالة الخطأ التي تظهر عند فقد أذونات التخزين.</span><span class="sxs-lookup"><span data-stu-id="13299-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="13299-131">تمت إضافة تسلسلات تحكم جديدة لبعض التدفقات.</span><span class="sxs-lookup"><span data-stu-id="13299-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="13299-132">لم يعد زر الإرسال متوفرًا بشكل صحيح بسبب حجم النافذة.</span><span class="sxs-lookup"><span data-stu-id="13299-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="13299-133">يمكن الآن لأشرطة التمرير المتابعة على شاشات أصغر عند استخدام أحجام أزرار أكبر.</span><span class="sxs-lookup"><span data-stu-id="13299-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="13299-134">لم يعد تراكب الزر الرباعي مقطوعًا بعد الآن.</span><span class="sxs-lookup"><span data-stu-id="13299-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="13299-135">تدعم لوحة المفاتيح الآن زر الحذف.</span><span class="sxs-lookup"><span data-stu-id="13299-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="13299-136">تم إصلاح مشكلة سطوع قد تحدث عند الضغط على لوحة المفاتيح.</span><span class="sxs-lookup"><span data-stu-id="13299-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="13299-137">تم إصلاح مشكلات العرض التوضيحي المختلفة.</span><span class="sxs-lookup"><span data-stu-id="13299-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="13299-138">تم إصلاح مشكلة قد تكون أثرت على الحقول الرقمية في صفحة التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="13299-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="13299-139">لم تعد تختفي لوحة المفاتيح الموجودة على الشاشة أحيانًا في بعض الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="13299-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="13299-140">تم إصلاح أخطاء مختلفة لواجهة المستخدم (UI)، مثل الأخطاء التي تؤثر في لون الخلفية وموضعها.</span><span class="sxs-lookup"><span data-stu-id="13299-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="13299-141">تم تحسين واجهة مستخدم اللغة الروسية.</span><span class="sxs-lookup"><span data-stu-id="13299-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="13299-142">تم إصلاح المشكلات المختلفة التي أدت إلى توقف النظام عن الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="13299-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="13299-143">تم إصلاح مشكلة تتعلق بإعادة فتح الحاسبة.</span><span class="sxs-lookup"><span data-stu-id="13299-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="13299-144">إصدار **Android:** تم إصلاح مشكلة أدت لتوقف Android 4.4 عن الاستجابة عند بدء التشغيل.</span><span class="sxs-lookup"><span data-stu-id="13299-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="13299-145">إصدار **Android:** تم تقليل الحد الأدنى للقياس إلى 50 بالمئة.</span><span class="sxs-lookup"><span data-stu-id="13299-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="13299-146">الإصدار 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="13299-146">Version 2.0.4.0</span></span>

<span data-ttu-id="13299-147">كان إصدار 2.0.4.0 هو الإصدار الأول المتوفر بشكل عام لتطبيق Warehouse Management للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="13299-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="13299-148">الميزات الجديدة والإصلاحات والتحسينات في إصدار 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="13299-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="13299-149">يقدم هذا الإصدار الميزات الجديدة والإصلاحات والتحسينات التالية غير المتوفرة في إصدار المعاينة:</span><span class="sxs-lookup"><span data-stu-id="13299-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="13299-150">إذا كانت بطاقة التفاصيل تتضمن تسميتين لهما بيانات متطابقة، فإنه يتم إخفاء إحدى التسميات.</span><span class="sxs-lookup"><span data-stu-id="13299-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="13299-151">يتم الآن إظهار الأحرف الخاصة الآن بشكل افتراضي، وتمت إزالة خيار إخفاءها من إعدادات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="13299-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="13299-152">يتم الآن إظهار أزرار الإرسال المعطلة على أنها غير متوفرة في طريقة عرض الهاتف المحمول الصغير.</span><span class="sxs-lookup"><span data-stu-id="13299-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="13299-153">يضمن تغيير منطق تسلسل لعناصر التحكم تحجيمًا أسهل بين الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="13299-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="13299-154">ولذلك، تكون هناك حاجة أقل لضبط حجم الخطوط أو الأزرار.</span><span class="sxs-lookup"><span data-stu-id="13299-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="13299-155">تم تغيير سمة اللون الافتراضية إلى *داكن*.</span><span class="sxs-lookup"><span data-stu-id="13299-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="13299-156">تمت إضافة الرمز المفقود لزر الإرسال المعطل في طريقة عرض الشريط.</span><span class="sxs-lookup"><span data-stu-id="13299-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="13299-157">تنتقل استثناءات المهلة الآن إلى صفحة الاتصال بدلاً من إظهار خطأ داخلي.</span><span class="sxs-lookup"><span data-stu-id="13299-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="13299-158">في حالة عدم توفر أي إجراء للإرسال (مثل **موافق** أو **نعم** أو **قبول** أو **تم** أو **منتهي**)، سيتم تعطيل الزر إرسال.</span><span class="sxs-lookup"><span data-stu-id="13299-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="13299-159">تم تحسين استقرار التطبيق.</span><span class="sxs-lookup"><span data-stu-id="13299-159">App stability has been improved.</span></span>
- <span data-ttu-id="13299-160">هناك إصلاح لمشكلة الثغرة الأمنية [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="13299-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="13299-161">**إصدار Windows:** تم إصلاح مشكلة عدم الاستجابة للقوائم بعد تغيير حجم النافذة في نظام التشغيل Windows.</span><span class="sxs-lookup"><span data-stu-id="13299-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="13299-162">المشكلة المعروفة في الإصدار 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="13299-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="13299-163">توجد المشكلة المعروفة التالية في هذا الإصدار:</span><span class="sxs-lookup"><span data-stu-id="13299-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="13299-164">يحتوي هذا الإصدار على مشكلة في الأجهزة التي تستخدم Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="13299-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="13299-165">قد تواجه مشكلات عند استخدام التطبيق على إصدار Android هذا.</span><span class="sxs-lookup"><span data-stu-id="13299-165">You might experience issues when you use the app on this Android version.</span></span>
