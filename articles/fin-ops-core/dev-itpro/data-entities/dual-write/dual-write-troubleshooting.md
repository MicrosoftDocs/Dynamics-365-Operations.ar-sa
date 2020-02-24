---
title: دليل استكشاف أخطاء تكامل البيانات وإصلاحها
description: يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل البيانات وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service.
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
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019621"
---
# <a name="troubleshooting-guide-for-data-integration"></a>دليل استكشاف أخطاء تكامل البيانات وإصلاحها

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>تمكين سجلات تتبع المكون الإضافي في Common Data Service وفحص تفاصيل أخطاء المكون الإضافي للكتابة المزدوجة

إذا واجهت مشكلة أو خطأ ما أثناء مزامنة لكتابة المزدوجة، فاتبع الخطوات التالية لفحص الأخطاء الموجودة في سجل التتبع.

1. قبل ان تتمكن من فحص الأخطاء، يجب تمكين سجلات تتبع المكون الإضافي. للحصول على الإرشادات، راجع القسم "عرض سجلات التتبع" في [البرنامج التعليمي: كتابة مكون إضافي وتسجيله](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    الآن يمكنك فحص الأخطاء.

2. سجل دخولك إلى Microsoft Dynamics 365 Sales.
3. حدد زر **الإعدادات** (رمز الترس)، ثم حدد **الإعدادات المتقدمة**.
4. في قائمة **الإعدادات**، اختر **تخصيص \> سجل تتبع المكون الإضافي**.
5. حدد **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** كاسم النوع لإظهار تفاصيل الأخطاء.

## <a name="inspect-dual-write-synchronization-errors"></a>فحص أخطاء مزامنة الكتابة المزدوجة

اتبع الخطوات التالية لفحص الأخطاء أثناء الاختبار.

1. سجل دخولك إلى Microsoft Dynamics Lifecycle Services (LCS).
2. افتح مشروع LCS لإجراء اختبار الكتابة المزدوجة له.
3. حدد **بيئات مستضافة على الشبكة السحابية**.
4. أنشئ اتصال سطح مكتب بعيد بالجهاز الظاهري (VM) للتطبيق باستخدام الحساب المحلي الذي يظهر في LCS.
5. افتح عارض الأحداث. 
6. انتقل إلى **سجلات التطبيقات والخدمات \> Microsoft \> Dynamics \> AX-DualWriteSync \> تشغيلي‏‎**. تظهر الأخطاء والتفاصيل.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>كيفية إلغاء ربط بيئة Common Data Service بالتطبيق وربط بيئة أخرى

اتبع الخطوات التالية لتحديث الارتباطات.

1. انتقل إلى بيئة التطبيق.
2. افتح "إدارة البيانات".
3. حدد **ارتباط إلى CDS للتطبيقات**.
4. حدد جميع التعيينات قيد التشغيل، ثم حدد **إيقاف**.
5. حدد حدد جميع التعيينات، ثم حدد‏‎**حذف**.

    > [!NOTE]
    > لن يتوفر الخيار **حذف** إذا تم تحديد القالب **CustomerV3-Account**. قم بإلغاء تحديد هذا القالب كما هو مطلوب. القالب **CustomerV3-Account** عبارة عن قالب تم تزويده في وقت سابق ويعمل مع الحل "العميل المتوقع إلى النقدية". وبسبب إصداره بشكل عمومي، يظهر تحت جميع القوالب.

6. حدد **إلغاء ربط البيئة**.
7. حدد **نعم** لتأكيد العملية.
8. لربط البيئة الجديدة، اتبع الخطوات في [دليل التثبيت](https://aka.ms/dualwrite-docs).
