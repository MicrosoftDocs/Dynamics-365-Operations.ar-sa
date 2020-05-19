---
title: استكشاف المشاكل العامة وإصلاحها
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء عامة في تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 8cc7c11233c745719af72222eba02fb71d7a8944
ms.sourcegitcommit: 4edc658448612afbf1c1663c166d12e08e4c4165
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/06/2020
ms.locfileid: "3340920"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="c4d6a-103">استكشاف المشاكل العامة وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="c4d6a-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c4d6a-104">يوفر هذا الموضوع معلومات حول استكشاف أخطاء عامة في تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4d6a-105">قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c4d6a-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c4d6a-106">يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="c4d6a-107">عند محاولة تثبيت حزمة الكتابة الثنائية باستخدام أداة موزع الحزمة، لا تتوفر حلول متوفرة</span><span class="sxs-lookup"><span data-stu-id="c4d6a-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="c4d6a-108">لا تتوافق بعض إصدارات أداة موزع الحزمة مع حزمة حلول الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="c4d6a-109">لتثبيت الحزمة بنجاح، تأكد من استخدام [إصدار 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) أو إصدار لاحق من أداة موزع الحزمة.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="c4d6a-110">بعد تثبيت أداة موزع الحزمة، قم بتثبيت حزمة الحل باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="c4d6a-111">قم بتنزيل ملف حزمة الحل الأخير من Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="c4d6a-112">بعد تنزيل ملف الضغط المضغوط للحزمة، انقر بزر الماوس الأيمن فوقه، ثم حدد **الخصائص**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="c4d6a-113">حدد خانة الاختيار **إلغاء الحظر**، ثم حدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="c4d6a-114">إذا لم تر خانة الاختيار **إلغاء الحظر** فقد تم إلغاء حظر الملف المضغوط بالفعل، ويمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![مربع حوار الخصائص](media/unblock_option.png)

2. <span data-ttu-id="c4d6a-116">قم باستخراج ملف الحزمة المضغوطة من نوع zip، ونسخ كافة الملفات الموجودة في المجلد  **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![محتويات مجلد Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="c4d6a-118">ألصق كافة الملفات المنسوخة في مجلد **الأدوات** الخاص بأداة موزع الحزمة.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="c4d6a-119">قم بتشغيل **PackageDeployer.exe** لتحديد بيئة Common Data Service وتثبيت الحلول.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![محتوى مجلد الأدوات](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="c4d6a-121">تمكين وعرض تسجيل تتبع المكونات الإضافية في Common Data Service لعرض تفاصيل الخطأ</span><span class="sxs-lookup"><span data-stu-id="c4d6a-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="c4d6a-122">**الدور المطلوب لتشغيل سجل التتبع وعرض الأخطاء:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="c4d6a-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="c4d6a-123">لتشغيل سجل التتبع‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="c4d6a-124">قم بتسجيل الدخول إلى التطبيق المستند إلى النموذج في Dynamics 365، وافتح صفحة **الإعدادات** ثم ضمن **النظام** حدد **الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="c4d6a-125">في صفحة **الإدارة**، حدد **إعدادات النظام**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="c4d6a-126">ضمن علامة التبويب **تخصيص**، في حقل **المكون الإضافي وتتبع نشاط سير العمل المخصص**، حدد **الكل** لتمكين سجل تتبع المكون الإضافي.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="c4d6a-127">إذا كنت تريد تسجيل سجلات التتبع فقط في حالة حدوث استثناءات، فيمكنك تحديد **استثناء** بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="c4d6a-128">لعرض سجل التتبع‬، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="c4d6a-129">قم بتسجيل الدخول إلى التطبيق المستند إلى النموذج في Dynamics 365، وافتح صفحة **الإعدادات** ثم ضمن **التخصيص** حدد **سجل تتبع المكون الإضافي‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="c4d6a-130">ابحث عن سجلات التتبع التي يتم فيها تعيين حقل **اسم النوع** إلى **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="c4d6a-131">انقر نقرًا مزدوجًا فوق أحد العناصر لعرض السجل الكامل، ثم في علامة التبويب السريع **تنفيذ**، راجع نص **كتلة الرسالة**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="c4d6a-132">تمكين وضع التصحيح لاستكشاف مشكلات المزامنة المباشرة وإصلاحها في تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c4d6a-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="c4d6a-133">**الدور المطلوب لعرض الأخطاء:** يمكن أن تظهر أخطاء الكتابة المزدوجة لمسؤول النظام التي تنشأ في Common Data Service مع التطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-133">**Required role to view the errors:** System admin Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="c4d6a-134">في بعض الحالات، لا يتوفر النص الكامل لرسالة الخطأ نظرا لأن الرسالة طويلة جدًا أو تحتوي على معلومات التعريف الشخصية (PII).</span><span class="sxs-lookup"><span data-stu-id="c4d6a-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="c4d6a-135">يمكنك تشغيل التسجيل المطول للأخطاء باتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="c4d6a-136">تحتوي جميع تكوينات المشاريع في تطبيقات Finance and Operations على خاصية **IsDebugMode** في كيان **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="c4d6a-137">افتح كيان **DualWriteProjectConfiguration** باستخدام المكون الإضافي لـ Excel.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="c4d6a-138">الطريقة السهلة لفتح الكيان هي تشغيل وضع **التصميم** في وظيفة Excel الإضافية ثم إضافة **DualWriteProjectConfigurationEntity** إلى ورقة العمل.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="c4d6a-139">لمزيد من المعلومات، راجع [فتح كيان بيانات في Excel وتحديثه باستخدام الوظيفة الإضافية لبرنامج Excel](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="c4d6a-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="c4d6a-140">قم بتعيين خاصية **IsDebugMode** إلى **نعم** للمشروع.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="c4d6a-141">قم بتشغيل السيناريو الذي يقوم بإنشاء الأخطاء.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="c4d6a-142">تتوفر سجلات التسجيل المطول للأخطاء في جدول DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="c4d6a-143">للبحث عن البيانات في مستعرض الجداول، استخدم عنوان URL التالي (قم باستبدال **XXX** بالشكل المناسب):</span><span class="sxs-lookup"><span data-stu-id="c4d6a-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="c4d6a-144">فحص أخطاء المزامنة على الجهاز الظاهري لتطبيق Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c4d6a-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="c4d6a-145">**الدور المطلوب لعرض الأخطاء:** مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="c4d6a-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="c4d6a-146">سجل دخولك إلى Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c4d6a-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="c4d6a-147">افتح مشروع LCS الذي اخترته لإجراء اختبار الكتابة الثنائية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="c4d6a-148">حدد تجانب **بيئات مستضافة على الشبكة السحابية**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="c4d6a-149">استخدم سطح المكتب البعيد لتسجيل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="c4d6a-150">استخدم الحساب المحلي الموضح في LCS.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="c4d6a-151">افتح عارض الأحداث.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-151">Open Event viewer.</span></span>
6. <span data-ttu-id="c4d6a-152">حدد **سجلات التطبيقات والخدمات \> Microsoft \> Dynamics \> AX-DualWriteSync \> تشغيلي‏‎**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="c4d6a-153">راجع قائمة الأخطاء الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="c4d6a-154">إلغاء ارتباط بيئة Common Data Service أخرى من تطبيق Finance and Operations وربطها</span><span class="sxs-lookup"><span data-stu-id="c4d6a-154">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="c4d6a-155">**الدور المطلوب لإلغاء ارتباط البيئة:** مسؤول النظام لتطبيق Finance and Operations أو Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Common Data Service.</span></span>

1. <span data-ttu-id="c4d6a-156">قم بتسجيل الدخول إلى تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="c4d6a-157">انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد تجانب **الكتابة الثنائية**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="c4d6a-158">حدد كافة التعيينات قيد التشغيل، ثم حدد **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="c4d6a-159">حدد **إلغاء ربط البيئة**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="c4d6a-160">حدد **نعم** لتأكيد العملية.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="c4d6a-161">يمكنك الآن ربط بيئة جديدة.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="c4d6a-162">يتعذر عرض نموذج معلومات بند أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="c4d6a-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="c4d6a-163">عند إنشاء أمر مبيعات في Dynamics 365 Sales، فإن النقر فوق **+ إضافة منتجات** قد يعيد توجيهك إلى نموذج بند الأمر الخاص بـ Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="c4d6a-164">لا توجد طريقة من هذا النموذج لعرض نموذج **المعلومات** لبند أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="c4d6a-165">لا يظهر الخيار الخاص بـ **المعلومات** في القائمة المنسدلة أسفل **بند أمر جديد**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="c4d6a-166">يحدث هذا لأنه تم تثبيت Project Operations في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="c4d6a-167">لإعادة تمكين خيار نموذج **المعلومات**، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c4d6a-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="c4d6a-168">انتقل إلى كيان **بند الأمر**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="c4d6a-169">ابحث عن نموذج **المعلومات** أسفل عقدة النماذج.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="c4d6a-170">حدد نموذج **المعلومات** وانقر فوق **تمكين أدوار الأمان**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="c4d6a-171">قم بتغيير إعدادات الأمان إلى **العرض للجميع**.</span><span class="sxs-lookup"><span data-stu-id="c4d6a-171">Change the security setting to **Display to everyone**.</span></span>
