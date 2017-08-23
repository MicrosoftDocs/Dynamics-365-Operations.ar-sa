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

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>إعادة تعيين متجر البيانات للتقارير المالية بعد استعادة قاعدة البيانات

[!include[banner](../includes/banner.md)]


يوضح هذا الموضوع كيفية إعادة تعيين متجر بيانات التقارير المالية بعد استعادة قاعدة بيانات Microsoft Dynamics 365 for Finance and Operations.

إذا قمت في أي وقت باستعادة قاعدة بيانات Finance and Operations من نسخة احتياطية أو نسخ قاعدة البيانات من بيئة أخرى، فيجب اتباع الخطوات الواردة في هذا الموضوع للتأكد من أن متجر بيانات التقارير المالية يستخدم بشكل صحيح قاعدة بيانات Finance and Operations التي تمت استعادتها. 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> الخطوات في هذه العملية مدعومة لإصدار Dynamics 365 for Operations مايو 2016 (إصدار التطبيق 7.0.1265.23014 وإصدار التقارير المالية 7.0.10000.4) والإصدارات الأحدث. إذا كان لديك إصدار سابق من Finance and Operations، فاتصل بفريق الدعم للمساعدة.

## <a name="export-report-definitions"></a>تصدير تعريفات التقارير
أولاً، تصدير تصميمات التقارير الموجودة في "مصمم التقرير"، باستخدام الخطوات التالية:

1.  في مصمم التقرير، انتقل إلى **الشركة** &gt; **مجموعات كتل الإنشاء**.
2.  حدد مجموعة كتلة الإنشاء لتصديرها، ثم انقر فوق **تصدير**. 
    > [!Note] 
    > ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.
3.  حدد تعريفات التقارير لتصديرها:
    -   لتصدير كافة تعريفات التقارير وكتل الإنشاء المقترنة، انقر فوق **تحديد الكل**.
    -   لتصدير مجموعات محددة من التقارير أو الصفوف أو الأعمدة أو الأشجار أو الأبعاد، انقر فوق علامة التبويب المناسبة ثم حدد العناصر المراد تصديرها. اضغط مع الاستمرار على مفتاح Ctrl لتحديد أصناف متعددة في علامة التبويب. عند تحديد التقارير لتصديرها، يتم تحديد مجموعات الصفوف المقترنة والأعمدة وشجر التدرجات والأبعاد.

4.  انقر فوق **تصدير**.
5.  أدخل اسم ملف وحدد موقع أمن حيث تريد حفظ تعريفات التقارير التي تم تصديرها.
6.  انقر فوق **حفظ**.

يمكن نسخ الملف أو تحميله إلى موقع آمن، ليسمح ذلك باستيرادها إلى بيئة مختلفة في وقت آخر. يمكن العثور على معلومات حول كيفية استخدام حساب Microsoft Azure storage في [نقل البيانات باستخدام أداة سطر الأوامر المساعدة AzCopy"](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> لا تقدم Microsoft حساب تخزين كجزء من اتفاقية Finance and Operations. يجب عليك شراء حساب تخزين أو استخدام حساب تخزين من اشتراك Azure منفصل. 
> [!WARNING]
> يجب مراعاة سلوك محرك الأقراص D على أجهزة Azure الظاهرية. لا تحتفظ بمجموعات كتل الإنشاء التي تم تصديرها هنا بشكل دائم. لمزيد من المعلومات حول محركات الأقراص المؤقتة، انظر [فهم آلية عمل محرك الأقراص المؤقت على الأجهزة الظاهرية لـ Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>وقف الخدمات
استخدم "سطح المكتب البعيد" للاتصال بكافة أجهزة الكمبيوتر الموجودة في البيئة وإيقاف خدمات Windows التالية باستخدام services.msc:

-   خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)
-   خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)
-   خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)

ستكون لهذه الخدمات اتصالات مفتوحة بقاعدة بيانات Finance and Operations.

## <a name="reset"></a>إعادة التعيين
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>تحديد موقع حزمة MinorVersionDataUpgrade.zip الأحدث وتنزيلها

حدد موقع حزمة MinorVersionDataUpgrade.zip الأحدث باستخدام الإرشادات التي يمكن العثور عليها في [تنزيل أحدث حزمة قابلة للنشر لترقية البيانات](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). توضح الإرشادات كيفية تحديد موقع الإصدار الصحيح من حزمة ترقية البيانات وتنزيلها. لا حاجة إلى إجراء عملية ترقية لتنزيل حزمة MinorVersionDataUpgrade.zip. أنت تحتاج فقط إلى إكمال الخطوات المذكورة في القسم "تنزيل أحدث حزمة قابلة للنشر لترقية البيانات" من دون تنفيذ أي من الخطوات الأخرى الواردة في المقالة لاسترداد نسخة من حزمة MinorVersionDataUpgrade.zip.

#### <a name="execute-scripts-against-finance-and-operations-database"></a>تنفيذ البرامج النصية مقابل قاعدة بيانات Finance and Operations

قم بتشغيل البرامج النصية التالية مقابل قاعدة بيانات تشغيل (وليس مقابل قاعدة بيانات التقارير المالية).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

تضمن هذه البرامج النصية صحة إعدادات تتبع المستخدمين والأدوار والتغيير.

#### <a name="execute-powershell-command-to-reset-database"></a>تنفيذ أمر PowerShell لإعادة تعيين قاعدة البيانات

تنفيذ الأمر التالي مباشرة على جهاز كمبيوتر AOS، لإعادة تعيين التكامل بين تشغيل والتقارير المالية:

1.  قم بفتح Windows PowerShell كمسؤول.
2.  تنفيذ: F:
3.  تنفيذ: cd F:\\MRApplicationService\\MRInstallDirectory
4.  تنفيذ: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  تنفيذ: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”
    -   سيتم مطالبتك بإدخال "نعم" للتأكيد.

شرح المعلمات:

-   القيم الصالحة لـ"السبب": الخدمة،BADDATA، أخرى.
-   تُمثل معلمة ReasonDetail نص حر.
-   سيتم تسجيل السبب ReasonDetail في مراقبة القياس عن بعد /البيئة.

## <a name="start-services"></a>‏‏بدء الخدمات
استخدم services.msc لإعادة تشغيل الخدمات التي قمت بوقفها في وقت سابق:

-   خدمة النشر على شبكة الإنترنت العالمية (على كافة أجهزة الكمبيوتر التي تعمل بنظام AOS)
-   خدمة إدارة الدفعة لـ Microsoft Dynamics 365 for Finance and Operations (على أجهزة الكمبيوتر التي لا تعمل بنظام AOS فقط)
-   خدمة عملية 2012 لإدارة تقارير الأداة (على أجهزة كمبيوتر BI فقط)

## <a name="import-report-definitions"></a>استيراد تعريفات التقارير
استيراد تصاميم التقارير من "مصمم التقرير"، باستخدام الملف الذي قمت بإنشاؤه أثناء عملية التصدير:

1.  في مصمم التقرير، انتقل إلى **الشركة** &gt; **مجموعات كتل الإنشاء**.
2.  حدد مجموعة كتلة الإنشاء لتصديرها، ثم انقر فوق **تصدير**. 

    > [!NOTE]
    > ملاحظة: بالنسبة إلى Finance and Operations، يتم دعم مجموعة واحدة فقط من كتل الإنشاء، وهي المجموعة **الافتراضية**.
    
3.  حدد **الخيار الافتراضي**لكتلة الإنشاء، ثم انقر فوق **استيراد**.
4.  حدد الملف الذي يحتوي على تعريفات التقرير الذي تم تصديره، ثم انقر فوق **فتح**.
5.  في مربع الحوار استيراد، حدد تعريفات التقرير المراد استيرادها.
    -   لاستيراد كافة تعريفات التقارير وكتل الإنشاء الداعمة، انقر فوق **تحديد الكل**.
    -   لاستيراد تقارير أو صفوف أو أعمدة أو أشجار أو مجموعات أبعاد محددة، حدد التقارير أو الصفوف أو الأعمدة أو الأشجار أو مجموعات الأبعاد لاستيرادها.

6.  انقر فوق **استيراد**.





