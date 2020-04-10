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
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172681"
---
# <a name="general-troubleshooting"></a>استكشاف المشاكل العامة وإصلاحها

[!include [banner](../../includes/banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء عامة في تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>عند محاولة تثبيت حزمة الكتابة الثنائية باستخدام أداة موزع الحزمة، لا تتوفر حلول متوفرة

لا تتوافق بعض إصدارات أداة موزع الحزمة مع حزمة حلول الكتابة الثنائية. لتثبيت الحزمة بنجاح، تأكد من استخدام [إصدار 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) أو إصدار لاحق من أداة موزع الحزمة.

بعد تثبيت أداة موزع الحزمة، قم بتثبيت حزمة الحل باتباع الخطوات التالية.

1. قم بتنزيل ملف حزمة الحل الأخير من Yammer.com. بعد تنزيل ملف الضغط المضغوط للحزمة، انقر بزر الماوس الأيمن فوقه، ثم حدد **الخصائص**. حدد خانة الاختيار **إلغاء الحظر**، ثم حدد **تطبيق**. إذا لم تر خانة الاختيار **إلغاء الحظر** فقد تم إلغاء حظر الملف المضغوط بالفعل، ويمكنك تخطي هذه الخطوة.

    ![مربع حوار الخصائص](media/unblock_option.png)

2. قم باستخراج ملف الحزمة المضغوطة من نوع zip، ونسخ كافة الملفات الموجودة في المجلد  **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![محتويات مجلد Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. ألصق كافة الملفات المنسوخة في مجلد **الأدوات** الخاص بأداة موزع الحزمة. 
4. قم بتشغيل **PackageDeployer.exe** لتحديد بيئة Common Data Service وتثبيت الحلول.

    ![محتوى مجلد الأدوات](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>تمكين وعرض تسجيل تتبع المكونات الإضافية في Common Data Service لعرض تفاصيل الخطأ

**الدور المطلوب لتشغيل سجل التتبع وعرض الأخطاء:** مسؤول النظام

لتشغيل سجل التتبع‬، اتبع الخطوات التالية.

1. قم بتسجيل الدخول إلى تطبيق Finance and Operations، وافتح صفحة **الإعدادات** ثم ضمن **النظام**، حدد **الإدارة**.
2. في صفحة **الإدارة**، حدد **إعدادات النظام**.
3. ضمن علامة التبويب **تخصيص**، في حقل **المكون الإضافي وتتبع نشاط سير العمل المخصص**، حدد **الكل** لتمكين سجل تتبع المكون الإضافي. إذا كنت تريد تسجيل سجلات التتبع فقط في حالة حدوث استثناءات، فيمكنك تحديد **استثناء** بدلاً من ذلك.


لعرض سجل التتبع‬، اتبع الخطوات التالية.

1. قم بتسجيل الدخول إلى تطبيق Finance and Operations، وافتح صفحة **الإعدادات**، ثم ضمن **التخصيص**، حدد **سجل تتبع المكون الإضافي**.
2. ابحث عن سجلات التتبع التي يتم فيها تعيين حقل **اسم النوع** إلى **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.
3. انقر نقرًا مزدوجًا فوق أحد العناصر لعرض السجل الكامل، ثم في علامة التبويب السريع **تنفيذ**، راجع نص **كتلة الرسالة**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>تمكين وضع التصحيح لاستكشاف مشكلات المزامنة المباشرة وإصلاحها في تطبيقات Finance and Operations

**الدور المطلوب لعرض الأخطاء:** مسؤول النظام

يمكن أن تظهر أخطاء الكتابة الثنائية التي تنشأ في Common Data Service في تطبيق Finance and Operations. في بعض الحالات، لا يتوفر النص الكامل لرسالة الخطأ نظرا لأن الرسالة طويلة جدًا أو تحتوي على معلومات التعريف الشخصية (PII). يمكنك تشغيل التسجيل المطول للأخطاء باتباع الخطوات التالية.

1. تحتوي جميع تكوينات المشاريع في تطبيقات Finance and Operations على خاصية **IsDebugMode** في كيان **DualWriteProjectConfiguration**. افتح كيان **DualWriteProjectConfiguration** باستخدام المكون الإضافي لـ Excel.

    > [!TIP]
    > الطريقة السهلة لفتح الكيان هي تشغيل وضع **التصميم** في وظيفة Excel الإضافية ثم إضافة **DualWriteProjectConfigurationEntity** إلى ورقة العمل. لمزيد من المعلومات، راجع [فتح كيان بيانات في Excel وتحديثه باستخدام الوظيفة الإضافية لبرنامج Excel](../../office-integration/use-excel-add-in.md).

2. قم بتعيين خاصية **IsDebugMode** إلى **نعم** للمشروع.
3. قم بتشغيل السيناريو الذي يقوم بإنشاء الأخطاء.
4. تتوفر سجلات التسجيل المطول للأخطاء في جدول DualWriteErrorLog. للبحث عن البيانات في مستعرض الجداول، استخدم عنوان URL التالي (قم باستبدال **XXX** بالشكل المناسب):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>فحص أخطاء المزامنة على الجهاز الظاهري لتطبيق Finance and Operations

**الدور المطلوب لعرض الأخطاء:** مسؤول النظام

1. سجل دخولك إلى Microsoft Dynamics Lifecycle Services (LCS).
2. افتح مشروع LCS الذي اخترته لإجراء اختبار الكتابة الثنائية.
3. حدد تجانب **بيئات مستضافة على الشبكة السحابية**.
4. استخدم سطح المكتب البعيد لتسجيل الدخول إلى الجهاز الظاهري (VM) لتطبيق Finance and Operations. استخدم الحساب المحلي الموضح في LCS.
5. افتح عارض الأحداث.
6. حدد **سجلات التطبيقات والخدمات \> Microsoft \> Dynamics \> AX-DualWriteSync \> تشغيلي‏‎**.
7. راجع قائمة الأخطاء الأخيرة.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>إلغاء ارتباط بيئة Common Data Service أخرى من تطبيق Finance and Operations وربطها

**بيانات الاعتماد المطلوبة لإلغاء ربط البيئة:** مسؤول مستأجر Azure AD

1. قم بتسجيل الدخول إلى تطبيق Finance and Operations.
2. انتقل إلى **مساحات العمل \> إدارة البيانات**، وحدد تجانب **الكتابة الثنائية**.
3. حدد كافة التعيينات قيد التشغيل، ثم حدد **إيقاف**.
4. حدد **إلغاء ربط البيئة**.
5. حدد **نعم** لتأكيد العملية.

يمكنك الآن ربط بيئة جديدة.
