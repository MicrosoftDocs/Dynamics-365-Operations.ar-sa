---
title: "مساحة عمل محمولة لإدخال وقت المشروع"
description: "يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة لإدخال وقت المشروع. تسمح مساحة العمل هذه للمستخدمين بإدخال وتوفير الوقت مقابل مشروع ما باستخدام جهازهم المحمول."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: c04ffccdcbf104b1d5db30a41116663fcedd4e1d
ms.contentlocale: ar-sa
ms.lasthandoff: 12/01/2017

---

# <a name="project-time-entry-mobile-workspace"></a>مساحة عمل محمولة لإدخال وقت المشروع

[!include[banner](../includes/banner.md)]

يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة **إدخال وقت المشروع**. تسمح مساحة العمل هذه للمستخدمين بإدخال وتوفير الوقت مقابل مشروع ما باستخدام جهازهم المحمول.

تهدف مساحة العمل المحمولة هذه إلى استخدامها بواسطة تطبيق المحمول Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>نظرة عامة
تكون موارد المشروع في أغلب الأوقات موجودة في الموقع أو مسافرة، وذلك كجزء من عملها اليومي. تسمح مساحة العمل المحمولة **إدخال وقت المشروع** للمستخدمين بإدخال الوقت القابل للفوترة أو غير القابل للفوترة في مقابل مشروع ما على اجهاز محمول من اختيارهم. وبالتالي، تستطيع موارد المشروع تسجيل إدخالات الوقت في أي وقت وفي أي مكان. وباستطاعة الموارد أيضًا عرض إدخالات الوقت التي تم تسجيلها. 

باستطاعة المستخدمين تنفيذ هذه المهام على وجه التحديد في مساحة العمل المحمولة **إدخال وقت المشروع**.

-   لأي تاريخ محدد، أدخل عدد الساعات التي أمضيتها في العمل على مهمة معينة.
-   ابحث حسب اسم المشروع أو العميل للعثور على المشروع الذي تريد إدخال الوقت له.
-   حدد الفئة والنشاط للوقت الذي أمضيته.
-   سجّل الوقت كقابل للفوترة أو غير قابل للفوترة للمشروع.
-   بشكل اختياري، أدخل أية تعليقات خارجية أو داخلية.

## <a name="prerequisites"></a>المتطلبات الأساسية
تختلف المتطلبات الأساسية، بناءً على إصدار Microsoft Dynamics 365 الذي تم نشره لمؤسستك.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>المتطلبات الأساسية إذا كنت تستخدم Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition
إذا تم نشر Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition لمؤسستك، فيتعين على مسؤول النظام نشر مساحة العمل المحمولة **إدخال وقت المشروع**. للاطلاع على الإرشادات، راجع [نشر مساحة العمل المحمولة ](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>المتطلبات الأساسية إذا كنت تستخدم الإصدار 1611 من Microsoft Dynamics 365 for Operations مع تحديث النظام الأساسي 3 أو إصدار أحدث
إذا تم نشر الإصدار 1611 من Microsoft Dynamics 365 for Operations مع تحديث النظام الأساسي 3 أو إصدار أحدث لمؤسستك، فيجب على مسؤول النظام إكمال المتطلبات الأساسية التالية. 

<table>
<thead>
<tr class="header">
<th>المتطلب الأساسي</th>
<th>الدور</th>
<th>‏‏الوصف</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>تطبيق قاعدة المعارف 4018050.</td>
<td>مسؤول النظام</td>
<td>إن KB 4018050 عبارة عن تحديث X++ أو إصلاح عاجل لبيانات التعريف يحتوي على مساحة العمل المحمولة <strong>إدخال وقت المشروع</strong>. لتطبيق KB 4018050، يجب أن يتبع مسؤول النظام الخطوات التالية.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">تنزيل الإصلاح العاجل لبيانات التعريف من Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>ApplicationSuite</strong> و<strong>ProjectMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">تطبيق الحزمة القابلة للنشر</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>نشر مساحة العمل المحمولة <strong>إدخال وقت المشروع</strong>.</td>
<td>مسؤول النظام</td>
<td>راجع <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">نشر مساحة عمل محمولة</a></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>تحميل وتثبيت تطبيق الجوال

تنزيل وتثبيت تطبيق Dynamics 365 for Unified Operations للأجهزة المحمولة:

-   [لهواتف Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [لهواتف iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>تسجيل الدخول إلى تطبيق الهاتف الجوال
1.  ابدأ تشغيل التطبيق على جهازك المحمول.
2.  أدخل عنوان URL لـ Dynamics 365.
3.  في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك. أدخل بيانات اعتمادك.
4.  بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك. تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.

[![سحب للتحديث](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>إدخال الوقت باستخدام مساحة العمل المحمولة لإدخال وقت المشروع
1.  على جهازك المحمول، حدد مساحة عمل **إدخال وقت المشروع**.
2.  حدد **إدخال الوقت**. تظهر تواريخ التقويم للأسبوع الحالي.
3.  لتاريخ محدد، حدد **الإجراءات** &gt; **إدخال جديد**.
4.  أدخل عدد الساعات التي يجب تسجيلها.
5.  حدد مشروعًا لإدخال الوقت. تعرض قائمة المشاريع المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، راجع [النظام الأساسي للمحمول](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  إذا لم يكن مشروعك موجودًا في القائمة، فحدد **بحث عن المزيد‬**. ابحث حسب الاسم، أو قم بالتبديل إلى البحث حسب اسم المشروع أو العميل.
7.  حدد إحدى الفئات. تعرض قائمة الفئات المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، راجع [النظام الأساسي للمحمول](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  إذا لم تكن فئتك موجودة في القائمة، فحدد **بحث عن المزيد‬**. ابحث حسب الفئة أو قم بالتبديل إلى البحث حسب اسم الفئة.
9.  حدد نشاطًا. تعرض قائمة الأنشطة المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، راجع [النظام الأساسي للمحمول](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. إذا لم يكن نشاطك موجودًا في القائمة، فحدد **بحث عن المزيد‬**. ابحث حسب رقم النشاط أو قم بالتبديل إلى البحث حسب الغرض.

11. حدد خاصية البند.
12. بشكل اختياري، أدخل أية تعليقات خارجية أو داخلية.
13. حدد **تم**.

