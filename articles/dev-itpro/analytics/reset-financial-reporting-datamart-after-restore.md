---
title: "إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة البيانات"
description: "يوضح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة بيانات Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="f39b1-103">إعادة تعيين متجر البيانات للتقارير المالية بعد استعادة قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="f39b1-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f39b1-104">يوضح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة بيانات Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f39b1-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="f39b1-105">إذا قمت في أي وقت باستعادة قاعدة بيانات Finance and Operations من نسخة احتياطية أو نسخ قاعدة البيانات من بيئة أخرى، فيجب اتباع الخطوات الواردة في هذا الموضوع للتأكد من أن متجر بيانات التقارير المالية يستخدم بشكل صحيح قاعدة بيانات Finance and Operations التي تمت استعادتها.</span><span class="sxs-lookup"><span data-stu-id="f39b1-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="f39b1-106">الخطوات في هذه العملية مدعومة لإصدار Dynamics 365 for Operations مايو 2016 (إصدار التطبيق 7.0.1265.23014 وإصدار التقارير المالية 7.0.10000.4) والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="f39b1-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="f39b1-107">إذا كان لديك إصدار سابق من Finance and Operations، فاتصل بفريق الدعم للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="f39b1-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="f39b1-108">تصدير تعريفات التقارير</span><span class="sxs-lookup"><span data-stu-id="f39b1-108">Export report definitions</span></span>
<span data-ttu-id="f39b1-109">أولاً، تصدير تصميمات التقارير الموجودة في "مصمم التقرير"، باستخدام الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f39b1-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="f39b1-110">في مصمم التقرير، انتقل إلى **الشركة** &gt; **مجموعات كتل الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="f39b1-111">حدد مجموعة كتلة الإنشاء لتصديرها، ثم انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="f39b1-112">ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="f39b1-113">حدد تعريفات التقارير لتصديرها:</span><span class="sxs-lookup"><span data-stu-id="f39b1-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="f39b1-114">لتصدير كافة تعريفات التقارير وكتل الإنشاء المقترنة، انقر فوق **تحديد الكل**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="f39b1-115">لتصدير مجموعات محددة من التقارير أو الصفوف أو الأعمدة أو الأشجار أو الأبعاد، انقر فوق علامة التبويب المناسبة ثم حدد العناصر المراد تصديرها.</span><span class="sxs-lookup"><span data-stu-id="f39b1-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="f39b1-116">اضغط باستمرار على المفتاح Ctrl لتحديد عدة عناصر على علامة تبويب. عندما تحدد تقارير لتصديرها، سيتم تحديد الصفوف والأعمدة والأشجار ومجموعات الأبعاد ذات الصلة.‬</span><span class="sxs-lookup"><span data-stu-id="f39b1-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="f39b1-117">انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-117">Click **Export**.</span></span>
5.  <span data-ttu-id="f39b1-118">أدخل اسم ملف وحدد موقع أمن حيث تريد حفظ تعريفات التقارير التي تم تصديرها.</span><span class="sxs-lookup"><span data-stu-id="f39b1-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="f39b1-119">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-119">Click **Save**.</span></span>

<span data-ttu-id="f39b1-120">يمكن نسخ الملف أو تحميله إلى موقع آمن، ليسمح ذلك باستيرادها إلى بيئة مختلفة في وقت آخر.</span><span class="sxs-lookup"><span data-stu-id="f39b1-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="f39b1-121">يمكن العثور على معلومات حول كيفية استخدام حساب Microsoft Azure storage في [نقل البيانات باستخدام أداة سطر الأوامر المساعدة AzCopy"](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="f39b1-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="f39b1-122">لا تقدم Microsoft حساب تخزين كجزء من اتفاقية Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f39b1-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="f39b1-123">يجب عليك شراء حساب تخزين أو استخدام حساب تخزين من اشتراك Azure منفصل.</span><span class="sxs-lookup"><span data-stu-id="f39b1-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="f39b1-124">يجب مراعاة سلوك محرك الأقراص D على أجهزة Azure الظاهرية.</span><span class="sxs-lookup"><span data-stu-id="f39b1-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="f39b1-125">لا تحتفظ بمجموعات كتل الإنشاء التي تم تصديرها هنا بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="f39b1-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="f39b1-126">لمزيد من المعلومات حول محركات الأقراص المؤقتة، انظر [فهم آلية عمل محرك الأقراص المؤقت على الأجهزة الظاهرية لـ Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="f39b1-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="f39b1-127">وقف الخدمات</span><span class="sxs-lookup"><span data-stu-id="f39b1-127">Stop services</span></span>
<span data-ttu-id="f39b1-128">استخدم "سطح المكتب البعيد" للاتصال بكافة أجهزة الكمبيوتر الموجودة في البيئة وإيقاف خدمات Windows التالية باستخدام services.msc:</span><span class="sxs-lookup"><span data-stu-id="f39b1-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="f39b1-129">خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)</span><span class="sxs-lookup"><span data-stu-id="f39b1-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="f39b1-130">خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)</span><span class="sxs-lookup"><span data-stu-id="f39b1-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="f39b1-131">خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)</span><span class="sxs-lookup"><span data-stu-id="f39b1-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="f39b1-132">ستكون لهذه الخدمات اتصالات مفتوحة بقاعدة بيانات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f39b1-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="f39b1-133">إعادة التعيين</span><span class="sxs-lookup"><span data-stu-id="f39b1-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="f39b1-134">تحديد موقع حزمة MinorVersionDataUpgrade.zip الأحدث وتنزيلها</span><span class="sxs-lookup"><span data-stu-id="f39b1-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="f39b1-135">حدد موقع حزمة MinorVersionDataUpgrade.zip الأحدث باستخدام الإرشادات التي يمكن العثور عليها في [تنزيل أحدث حزمة قابلة للنشر لترقية البيانات](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="f39b1-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="f39b1-136">توضح الإرشادات كيفية تحديد موقع الإصدار الصحيح من حزمة ترقية البيانات وتنزيلها.</span><span class="sxs-lookup"><span data-stu-id="f39b1-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="f39b1-137">لا حاجة إلى إجراء عملية ترقية لتنزيل حزمة MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="f39b1-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="f39b1-138">أنت تحتاج فقط إلى إكمال الخطوات المذكورة في القسم "تنزيل أحدث حزمة قابلة للنشر لترقية البيانات" من دون تنفيذ أي من الخطوات الأخرى الواردة في المقالة لاسترداد نسخة من حزمة MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="f39b1-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="f39b1-139">تنفيذ البرامج النصية مقابل قاعدة بيانات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f39b1-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="f39b1-140">قم بتشغيل البرامج النصية التالية مقابل قاعدة بيانات تشغيل (وليس مقابل قاعدة بيانات التقارير المالية).</span><span class="sxs-lookup"><span data-stu-id="f39b1-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="f39b1-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="f39b1-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="f39b1-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="f39b1-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="f39b1-143">تضمن هذه البرامج النصية صحة إعدادات تتبع المستخدمين والأدوار والتغيير.</span><span class="sxs-lookup"><span data-stu-id="f39b1-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="f39b1-144">تنفيذ أمر PowerShell لإعادة تعيين قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="f39b1-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="f39b1-145">على كمبيوتر AOS، نفّذ الأوامر التالية مباشرة في PowerShell كمسؤول لإعادة تعيين التكامل بين Finance and Operations والتقارير المالية:</span><span class="sxs-lookup"><span data-stu-id="f39b1-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="f39b1-146">بعد تنفيذ الأوامر، ستتم مطالبتك بإدخال "نعم" للتأكيد.</span><span class="sxs-lookup"><span data-stu-id="f39b1-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="f39b1-147">شرح المعلمات:</span><span class="sxs-lookup"><span data-stu-id="f39b1-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="f39b1-148">القيم الصالحة لـ"السبب": الخدمة،BADDATA، أخرى.</span><span class="sxs-lookup"><span data-stu-id="f39b1-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="f39b1-149">تُمثل معلمة ReasonDetail نص حر.</span><span class="sxs-lookup"><span data-stu-id="f39b1-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="f39b1-150">سيتم تسجيل السبب ReasonDetail في مراقبة القياس عن بعد /البيئة.</span><span class="sxs-lookup"><span data-stu-id="f39b1-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="f39b1-151">‏‏بدء الخدمات</span><span class="sxs-lookup"><span data-stu-id="f39b1-151">Start services</span></span>
<span data-ttu-id="f39b1-152">استخدم services.msc لإعادة تشغيل الخدمات التي قمت بوقفها في وقت سابق:</span><span class="sxs-lookup"><span data-stu-id="f39b1-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="f39b1-153">خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)</span><span class="sxs-lookup"><span data-stu-id="f39b1-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="f39b1-154">خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)</span><span class="sxs-lookup"><span data-stu-id="f39b1-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="f39b1-155">خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)</span><span class="sxs-lookup"><span data-stu-id="f39b1-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="f39b1-156">استيراد تعريفات التقارير</span><span class="sxs-lookup"><span data-stu-id="f39b1-156">Import report definitions</span></span>
<span data-ttu-id="f39b1-157">استيراد تصاميم التقارير من "مصمم التقرير"، باستخدام الملف الذي قمت بإنشاؤه أثناء عملية التصدير:</span><span class="sxs-lookup"><span data-stu-id="f39b1-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="f39b1-158">في مصمم التقرير، انتقل إلى **الشركة** &gt; **مجموعات كتل الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="f39b1-159">حدد مجموعة كتلة الإنشاء لتصديرها، ثم انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="f39b1-160">ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="f39b1-161">حدد **الخيار الافتراضي**لكتلة الإنشاء، ثم انقر فوق **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="f39b1-162">حدد الملف الذي يحتوي على تعريفات التقرير الذي تم تصديره، ثم انقر فوق **فتح**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="f39b1-163">في مربع الحوار استيراد، حدد تعريفات التقرير المراد استيرادها.</span><span class="sxs-lookup"><span data-stu-id="f39b1-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="f39b1-164">لاستيراد كافة تعريفات التقارير وكتل الإنشاء الداعمة، انقر فوق **تحديد الكل**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="f39b1-165">لاستيراد تقارير أو صفوف أو أعمدة أو أشجار أو مجموعات أبعاد محددة، حدد التقارير أو الصفوف أو الأعمدة أو الأشجار أو مجموعات الأبعاد لاستيرادها.</span><span class="sxs-lookup"><span data-stu-id="f39b1-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="f39b1-166">انقر فوق **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="f39b1-166">Click **Import**.</span></span>





