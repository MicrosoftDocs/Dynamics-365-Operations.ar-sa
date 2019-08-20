---
title: دليل استكشاف أخطاء تكامل البيانات وإصلاحها
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل البيانات وإصلاحها بين Microsoft Dynamics 365 for Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797265"
---
# <a name="troubleshooting-guide-for-data-integration"></a>دليل استكشاف أخطاء تكامل البيانات وإصلاحها

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>تمكين تتبع المكون الإضافي في Common Data Service والتحقق من تفاصيل أخطاء المكون الإضافي للكتابة المزدوجة

إذا كنت تواجه مشكلة أو خطأ مع مزامنة الكتابة المزدوجة، يمكنك فحص الأخطاء في سجل التتبع:

1. قبل أن تتمكن من فحص الأخطاء، يجب تمكين تتبع المكون الإضافي باستخدام الإرشادات في [تسجيل المكون الإضافي](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) لتمكين تتبع المكون الإضافي. الآن يمكنك فحص الأخطاء.
2. سجل دخولك إلى Dynamics 365 for Sales.
3. انقر فوق أيقونة الإعدادات (ترس)، وحدد **إعدادات متقدمة**.
4. في قائمة **الإعدادات**، اختر **تخصيص >** سجل تتبع المكون الإضافي.
5. انقر فوق اسم النوع **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** لعرض تفاصيل الأخطاء.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>التحقق من أخطاء مزامنة الكتابة المزدوجة في Finance and Operations

يمكنك التحقق من الأخطاء أثناء الاختبار باتباع الخطوات التالية:

+ سجل دخولك إلى LifeCycle Services (LCS).
+ افتح مشروع LCS الذي اخترته لإجراء اختبار الكتابة المزدوجة.
+ انتقل إلى البيئات المستضافة على الشبكة السحابية.
+ سطح المكتب البعيد إلى Finance and Operations VM باستخدام الحساب المحلي الذي يتم عرضه في LCS.
+ افتح عارض الأحداث. 
+ انتقل إلى **سجلات التطبيقات والخدمات > Microsoft > Dynamics > AX-DualWriteSync > تشغيلي**. يتم عرض الأخطاء والتفاصيل.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>كيفية إلغاء ربط بيئة Common Data Service أخرى بتطبيق Finance and Operations وربطها به

يمكنك تحديث الارتباطات باتباع الخطوات التالية:

+ انتقل إلى بيئة Finance and Operations.
+ افتح "إدارة البيانات".
+ انقر فوق **ارتباط إلى CDS للتطبيقات**.
+ حدد كافة التعيينات قيد التشغيل، وانقر فوق **إيقاف**. 
+ حدد كافة التعيينات، وانقر فوق **حذف**.

    > [!NOTE]
    > لن يظهر الخيار **حذف** إذا تم تحديد القالب **CustomerV3-Account**. قم بإلغاء تحديده إذا لزم الأمر. القالب **CustomerV3-Account** عبارة عن قالب تم تزويده في وقت سابق ويعمل مع الحل "العميل المتوقع إلى النقدية". وبسبب إصداره بشكل عمومي، تظهر جميع القوالب تحته.

+ انقر فوق **إلغاء ربط البيئة**.
+ انقر فوق **نعم** للتأكيد.
+ لربط البيئة الجديدة، اتبع الخطوات في [دليل التثبيت](https://aka.ms/dualwrite-docs).

