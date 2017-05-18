---
title: "مساحة العمل المحمولة لإدخال وقت المشروع في تطبيق Dynamics 365 for Operations"
description: "يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة لإدخال وقت المشروع. تسمح مساحة العمل هذه للمستخدمين بإدخال وتوفير الوقت مقابل مشروع ما باستخدام جهازهم المحمول."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>مساحة العمل المحمولة لإدخال وقت المشروع

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة لإدخال وقت المشروع لتطبيق Microsoft Dynamics 365 for Operations للأجهزة المحمولة. تسمح مساحة العمل هذه للمستخدمين بإدخال وتوفير الوقت مقابل مشروع ما باستخدام جهازهم المحمول.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>نظرة عامة على مساحة العمل المحمولة لإدخال وقت المشروع
---------------------------------------------------

تكون موارد المشروع في أغلب الأوقات موجودة في الموقع أو مسافرة، وذلك كجزء من عملها اليومي. تسمح مساحة العمل المحمولة **إدخال وقت المشروع** للمستخدمين بإدخال الوقت القابل للفوترة أو غير القابل للفوترة في مقابل مشروع ما على اجهاز محمول من اختيارهم. وبالتالي، تستطيع موارد المشروع تسجيل إدخالات الوقت في أي وقت وفي أي مكان. وباستطاعة الموارد أيضًا عرض إدخالات الوقت التي تم تسجيلها. 

وبوجه خاص، توفر مساحة العمل المحمولة **إدخال وقت المشروع** هذه الميزات:

-   لأي تاريخ محدد، أدخل عدد الساعات التي أمضيتها في العمل على مهمة معينة.
-   ابحث حسب اسم المشروع أو العميل للعثور على المشروع الذي تريد إدخال الوقت له.
-   حدد الفئة والنشاط للوقت الذي أمضيته.
-   سجّل الوقت كقابل للفوترة أو غير قابل للفوترة للمشروع.
-   بشكل اختياري، أدخل أية تعليقات خارجية أو داخلية.

لتطبيق مساحة العمل المحمولة **إدخال وقت المشروع**، راجع الأقسام التالية في هذا الموضوع.

## <a name="prerequisites"></a>المتطلبات الأساسية
قبل تنفيذ مساحة العمل المحمولة **إدخال وقت المشروع**، تأكد من أن مسؤول النظام استكمل المتطلبات الأساسية التالية.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>المتطلب الأساسي</th>
<th>الدور</th>
<th>‏‏الوصف</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>يجب تطبيق الإصدار 1611 من Microsoft Dynamics 365 for Operations مع تحديث النظام الأساسي 3 أو إصدار أحدث.</td>
<td>مسؤول النظام</td>
<td>في حال عدم نشر Dynamics 365 for Operations في المؤسسة، يجب على مسؤول النظام الاطلاع على <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">نشر بيئة عرض توضيحي Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>يجب أن يتم تطبيق KB 4018050.</td>
<td>مسؤول النظام</td>
<td>إن KB 4018050 عبارة عن تحديث X++ أو إصلاح عاجل لبيانات التعريف يحتوي على مساحة العمل المحمولة <strong>إدخال وقت المشروع</strong>. لتطبيق KB 4018050، يجب أن يتبع مسؤول النظام الخطوات التالية.
<ol>
<li>تنزيل KB 4018050 من Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>ApplicationSuite</strong> و<strong>ProjectMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">تطبيق الحزمة قابلة للنشر</a> على نظام Dynamics 365 for Operations.</li>
</ol></td>
</tr>
<tr class="odd">
<td>يجب نشر مساحة العمل المحمولة <strong>إدخال وقت المشروع</strong> إلى تطبيق Dynamics 365 for Operations للأجهزة المحمولة.</td>
<td>مسؤول النظام</td>
<td><ol>
<li>ابدأ تشغيل Dynamics 365 for Operations في المستعرض.</li>
<li>في صفحة <strong>محددات النظام</strong>، على علامة التبويب <strong>إدارة مساحات العمل المحمولة</strong>، حدد <strong>إدخال وقت المشروع</strong>.</li>
<li>انقر فوق <strong>نشر مساحة العمل المحمولة</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>تنزيل وتثبيت تطبيق Dynamics 365 for Operations للأجهزة المحمولة
يمكنك تنزيل وتثبيت تطبيق Dynamics 365 for operations للأجهزة المحمولة من متجر تطبيقات المحمول.

-   لـ Android: [Dynamics 365 for Operations على Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   لـ iPhone: [Dynamics 365 for Operations على iTunes apps store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>تسجيل الدخول إلى تطبيق Dynamics 365 for Operations للأجهزة المحمولة
1.  ابدأ تشغيل التطبيق على جهازك المحمول.
2.  أدخل عنوان URL لتطبيق Dynamics 365 for Operations.
3.  أدخل الشركة لتسجيل الدخول إلى. على سبيل المثال، أدخل **USMF**.
4.  في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بحسابك في تطبيق Microsoft Dynamics 365 for Operations. أدخل بيانات اعتمادك.
5.  بعد تسجيل الدخول، يمكنك رؤية مساحات العمل المتوفرة لشركتك. تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، يمكنك السحب لتحديث قائمة مساحات العمل المحمولة.

[![سحب للتحديث](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>إدخال الوقت باستخدام مساحة العمل المحمولة لإدخال وقت المشروع
1.  على جهازك المحمول، حدد مساحة عمل **إدخال وقت المشروع**.
2.  حدد **إدخال الوقت**. سترى تواريخ التقويم للأسبوع الحالي.
3.  لتاريخ محدد، حدد **الإجراءات** &gt; **إدخال جديد**.
4.  أدخل عدد الساعات التي يجب تسجيلها.
5.  حدد مشروعًا لإدخال الوقت. يمكن الآن رؤية قائمة المشاريع المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، يجب على المطورين الاطلاع على [النظام الأساسي للمحمول Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  إذا لم يكن المشروع المطلوب في القائمة، فحدد **بحث** للقيام ببحث عبر الإنترنت في Dynamics 365 for Operations. ابحث حسب الاسم، أو قم بالتبديل إلى البحث حسب اسم المشروع أو العميل.
7.  حدد إحدى الفئات. يمكن الآن رؤية قائمة الفئات المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، يجب على المطورين الاطلاع على [النظام الأساسي للمحمول Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  إذا لم تكن الفئة المطلوبة في القائمة، فحدد **بحث** للقيام ببحث عبر الإنترنت في Dynamics 365 for Operations. ابحث حسب الفئة أو قم بالتبديل إلى البحث حسب اسم الفئة.
9.  حدد نشاطًا. يمكن الآن رؤية قائمة الأنشطة المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، يجب على المطورين الاطلاع على [النظام الأساسي للمحمول Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. إذا لم يكن النشاط المطلوب في القائمة، فحدد **بحث** للقيام ببحث عبر الإنترنت في Dynamics 365 for Operations. ابحث حسب رقم النشاط أو قم بالتبديل إلى البحث حسب الغرض.
11. حدد خاصية البند.
12. بشكل اختياري، أدخل أية تعليقات خارجية أو داخلية.
13. حدد **تم**.






