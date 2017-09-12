---
title: "إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة البيانات"
description: "يوضح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة بيانات Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: ar-sa
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="6a8cb-103">إعادة تعيين متجر البيانات للتقارير المالية بعد استعادة قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="6a8cb-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6a8cb-104">يوضح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة بيانات Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="6a8cb-105">إذا قمت في أي وقت باستعادة قاعدة بيانات Finance and Operations من نسخة احتياطية أو نسخ قاعدة البيانات من بيئة أخرى، فيجب اتباع الخطوات الواردة في هذا الموضوع للتأكد من أن متجر بيانات التقارير المالية يستخدم بشكل صحيح قاعدة بيانات Finance and Operations التي تمت استعادتها.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="6a8cb-106">الخطوات في هذه العملية مدعومة لإصدار Dynamics 365 for Operations مايو 2016 (إصدار التطبيق 7.0.1265.23014 وإصدار التقارير المالية 7.0.10000.4) والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="6a8cb-107">إذا كان لديك إصدار سابق من Finance and Operations، فاتصل بفريق الدعم للمساعدة.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="6a8cb-108">تصدير تعريفات التقارير</span><span class="sxs-lookup"><span data-stu-id="6a8cb-108">Export report definitions</span></span>
<span data-ttu-id="6a8cb-109">أولاً، تصدير تصميمات التقارير الموجودة في "مصمم التقرير"، باستخدام الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="6a8cb-110">في مصمم التقرير، انتقل إلى **الشركة** &gt; **مجموعات كتل الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="6a8cb-111">حدد مجموعة كتلة الإنشاء لتصديرها، ثم انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="6a8cb-112">ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="6a8cb-113">حدد تعريفات التقارير لتصديرها:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="6a8cb-114">لتصدير كافة تعريفات التقارير وكتل الإنشاء المقترنة، انقر فوق **تحديد الكل**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="6a8cb-115">لتصدير مجموعات محددة من التقارير أو الصفوف أو الأعمدة أو الأشجار أو الأبعاد، انقر فوق علامة التبويب المناسبة ثم حدد العناصر المراد تصديرها.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="6a8cb-116">اضغط مع الاستمرار على مفتاح Ctrl لتحديد أصناف متعددة في علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="6a8cb-117">عند تحديد التقارير لتصديرها، يتم تحديد مجموعات الصفوف المقترنة والأعمدة وشجر التدرجات والأبعاد.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="6a8cb-118">انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-118">Click **Export**.</span></span>
5.  <span data-ttu-id="6a8cb-119">أدخل اسم ملف وحدد موقع أمن حيث تريد حفظ تعريفات التقارير التي تم تصديرها.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="6a8cb-120">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-120">Click **Save**.</span></span>

<span data-ttu-id="6a8cb-121">يمكن نسخ الملف أو تحميله إلى موقع آمن، ليسمح ذلك باستيرادها إلى بيئة مختلفة في وقت آخر.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="6a8cb-122">يمكن العثور على معلومات حول كيفية استخدام حساب Microsoft Azure storage في [نقل البيانات باستخدام أداة سطر الأوامر المساعدة AzCopy"](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="6a8cb-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="6a8cb-123">لا تقدم Microsoft حساب تخزين كجزء من اتفاقية Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="6a8cb-124">يجب عليك شراء حساب تخزين أو استخدام حساب تخزين من اشتراك Azure منفصل.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="6a8cb-125">يجب مراعاة سلوك محرك الأقراص D على أجهزة Azure الظاهرية.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="6a8cb-126">لا تحتفظ بمجموعات كتل الإنشاء التي تم تصديرها هنا بشكل دائم.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="6a8cb-127">لمزيد من المعلومات حول محركات الأقراص المؤقتة، انظر [فهم آلية عمل محرك الأقراص المؤقت على الأجهزة الظاهرية لـ Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="6a8cb-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="6a8cb-128">وقف الخدمات</span><span class="sxs-lookup"><span data-stu-id="6a8cb-128">Stop services</span></span>
<span data-ttu-id="6a8cb-129">استخدم "سطح المكتب البعيد" للاتصال بكافة أجهزة الكمبيوتر الموجودة في البيئة وإيقاف خدمات Windows التالية باستخدام services.msc:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="6a8cb-130">خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="6a8cb-131">خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="6a8cb-132">خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="6a8cb-133">ستكون لهذه الخدمات اتصالات مفتوحة بقاعدة بيانات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="6a8cb-134">إعادة التعيين</span><span class="sxs-lookup"><span data-stu-id="6a8cb-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="6a8cb-135">تحديد موقع حزمة MinorVersionDataUpgrade.zip الأحدث وتنزيلها</span><span class="sxs-lookup"><span data-stu-id="6a8cb-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="6a8cb-136">حدد موقع حزمة MinorVersionDataUpgrade.zip الأحدث باستخدام الإرشادات التي يمكن العثور عليها في [تنزيل أحدث حزمة قابلة للنشر لترقية البيانات](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="6a8cb-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="6a8cb-137">توضح الإرشادات كيفية تحديد موقع الإصدار الصحيح من حزمة ترقية البيانات وتنزيلها.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="6a8cb-138">لا حاجة إلى إجراء عملية ترقية لتنزيل حزمة MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="6a8cb-139">أنت تحتاج فقط إلى إكمال الخطوات المذكورة في القسم "تنزيل أحدث حزمة قابلة للنشر لترقية البيانات" من دون تنفيذ أي من الخطوات الأخرى الواردة في المقالة لاسترداد نسخة من حزمة MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="6a8cb-140">تنفيذ البرامج النصية مقابل قاعدة بيانات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6a8cb-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="6a8cb-141">قم بتشغيل البرامج النصية التالية مقابل قاعدة بيانات تشغيل (وليس مقابل قاعدة بيانات التقارير المالية).</span><span class="sxs-lookup"><span data-stu-id="6a8cb-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="6a8cb-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="6a8cb-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="6a8cb-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="6a8cb-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="6a8cb-144">تضمن هذه البرامج النصية صحة إعدادات تتبع المستخدمين والأدوار والتغيير.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="6a8cb-145">تنفيذ أمر PowerShell لإعادة تعيين قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="6a8cb-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="6a8cb-146">تنفيذ الأمر التالي مباشرة على جهاز كمبيوتر AOS، لإعادة تعيين التكامل بين تشغيل والتقارير المالية:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="6a8cb-147">قم بفتح Windows PowerShell كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="6a8cb-148">تنفيذ: F:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-148">Execute: F:</span></span>
3.  <span data-ttu-id="6a8cb-149">تنفيذ: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="6a8cb-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="6a8cb-150">تنفيذ: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="6a8cb-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="6a8cb-151">تنفيذ: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span><span class="sxs-lookup"><span data-stu-id="6a8cb-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="6a8cb-152">سيتم مطالبتك بإدخال "نعم" للتأكيد.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="6a8cb-153">شرح المعلمات:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="6a8cb-154">القيم الصالحة لـ"السبب": الخدمة،BADDATA، أخرى.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="6a8cb-155">تُمثل معلمة ReasonDetail نص حر.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="6a8cb-156">سيتم تسجيل السبب ReasonDetail في مراقبة القياس عن بعد /البيئة.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="6a8cb-157">‏‏بدء الخدمات</span><span class="sxs-lookup"><span data-stu-id="6a8cb-157">Start services</span></span>
<span data-ttu-id="6a8cb-158">استخدم services.msc لإعادة تشغيل الخدمات التي قمت بوقفها في وقت سابق:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="6a8cb-159">خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="6a8cb-160">خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="6a8cb-161">خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)</span><span class="sxs-lookup"><span data-stu-id="6a8cb-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="6a8cb-162">استيراد تعريفات التقارير</span><span class="sxs-lookup"><span data-stu-id="6a8cb-162">Import report definitions</span></span>
<span data-ttu-id="6a8cb-163">استيراد تصاميم التقارير من "مصمم التقرير"، باستخدام الملف الذي قمت بإنشاؤه أثناء عملية التصدير:</span><span class="sxs-lookup"><span data-stu-id="6a8cb-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="6a8cb-164">في مصمم التقرير، انتقل إلى **الشركة** &gt; **مجموعات كتل الإنشاء**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="6a8cb-165">حدد مجموعة كتلة الإنشاء لتصديرها، ثم انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="6a8cb-166">ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="6a8cb-167">حدد **الخيار الافتراضي**لكتلة الإنشاء، ثم انقر فوق **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="6a8cb-168">حدد الملف الذي يحتوي على تعريفات التقرير الذي تم تصديره، ثم انقر فوق **فتح**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="6a8cb-169">في مربع الحوار استيراد، حدد تعريفات التقرير المراد استيرادها.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="6a8cb-170">لاستيراد كافة تعريفات التقارير وكتل الإنشاء الداعمة، انقر فوق **تحديد الكل**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="6a8cb-171">لاستيراد تقارير أو صفوف أو أعمدة أو أشجار أو مجموعات أبعاد محددة، حدد التقارير أو الصفوف أو الأعمدة أو الأشجار أو مجموعات الأبعاد لاستيرادها.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="6a8cb-172">انقر فوق **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="6a8cb-172">Click **Import**.</span></span>





