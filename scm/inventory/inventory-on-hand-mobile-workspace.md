---
title: "مساحة العمل المحمولة للمخزون الفعلي"
description: "يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة للمخزون الفعلي التي تتوفر في تطبيق Microsoft Dynamics 365 for Operations للأجهزة المحمولة. تساعدك مساحة العمل هذه في الحصول على معلومات دقيقة على جهازك المحمول تتعلق بالمخزون المحجوز والمتوفر في أي وقت وفي أي مكان.‬"
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>مساحة العمل المحمولة للمخزون الفعلي

[!include[banner](../includes/banner.md)]


يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة للمخزون الفعلي التي تتوفر في تطبيق Microsoft Dynamics 365 for Operations للأجهزة المحمولة. تساعدك مساحة العمل هذه في الحصول على معلومات دقيقة على جهازك المحمول تتعلق بالمخزون المحجوز والمتوفر في أي وقت وفي أي مكان.‬

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>نظرة عامة على مساحة العمل المحمولة للمخزون الفعلي
--------------------------------------------------

عادةً، يكون للشركات شحنات متعددة وإيصالات مخزون متعددة يوميًا. تغير هذه الحركات باستمرار حالة المخزون الفعلي. تسمح لك مساحة العمل المحمولة **المخزون الفعلي** برؤية حالة المخزون الفعلي عبر الشركة، حتى يتسنى لك الحصول على آخر المعلومات الدقيقة حول بيانات المخزون على جهاز محمول من اختيارك. بغض النظر عن ما إذا كان عملك في المخزن أو في المشتريات أو المبيعات أو التصنيع أو الإدارة، أو كان لديك أدوار أخرى، يمكنك الوصول إلى بيانات المخزون الفعلي في أي وقت وفي أي مكان. 

توفر مساحة العمل المحمولة عرضًا فوريًا لحالة المخزون الفعلي عبر المرافق. إنها تسمح لك بعرض المخزون الفعلي عبر المرافق وعمليات حجز المواد الحالية والمخزون الفعلي غير المحجوز. ويمكنك أيضًا إدخال أرقام الأصناف للاستعلام عن المخزون الفعلي، ويمكنك إجراء بحث مُصفى عن المنتجات أو المتغيرات الفعلية. 

وبوجه خاص، توفر مساحة العمل المحمولة هذه الميزات:

-   يمكنك البحث حسب رقم المنتج أو اسم المنتج للعثور على منتجات لعرض حالة المخزون المتاح لها.

-   بالنسبة للمنتجات المحددة، يمكنك عرض المعلومات التالية:
    -   المخزون المتاح لكل موقع
    -   المخزون المتاح لكل مخزن
    -   المخزون المتاح لكل موقع
    -   المخزون المتاح لكل دفعة (للمنتجات الخاضعة لسيطرة الدفعة)
    -   المخزون المتاح لكل حالة مخزون
    
-   يتم عرض منتجات المخزون المتاح بالطريق التالية:
    -   حسب المخزون الفعلي (يمثل هذا العرض المبلغ الإجمالي.)
    -   حسب المخزون الفعلي (يمثل هذا العرض المبلغ المحجوز.)
    -   حسب المخزون الفعلي المتوفر (يمثل هذا العرض المبلغ المتاح والذي لا تنطبق عليه أي حجوزات.)

## <a name="prerequisites"></a>المتطلبات الأساسية
قبل استخدام مساحة العمل المحمولة **المخزون الفعلي**، تأكد من أن مسؤول النظام استكمل المتطلبات الأساسية التالية.

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
<td>في حال عدم نشر Dynamics 365 for Operations في المؤسسة، يجب على مسؤول النظام الاطلاع على <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">نشر بيئة عرض توضيحي Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>يجب أن يتم تطبيق KB 4013633.</td>
<td>مسؤول النظام</td>
<td>تحتوي مقالة قاعدة المعارف KB 4013633 (تحديث X + + أو إصلاح عاجل لبيانات التعريف) على أربع مساحات عمل محمولة لإدارة سلسلة التوريد. لتطبيق KB 4013633، يجب أن يتبع مسؤول النظام الخطوات التالية:
<ol>
<li>تنزيل KB 4013633 من Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>SCMMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">تطبيق الحزمة قابلة للنشر</a> على نظام Dynamics 365 for Operations.</li>
</ol></td>
</tr>
<tr class="odd">
<td>يجب نشر مساحة العمل المحمولة <strong>المخزون الفعلي</strong> إلى تطبيق Dynamics 365 for Operations للأجهزة المحمولة.</td>
<td>مسؤول النظام</td>
<td><ol>
<li>ابدأ تشغيل Dynamics 365 for Operations في المستعرض.</li>
<li>في صفحة <strong>محددات النظام</strong>، حدد <strong>إدارة مساحات العمل المحمولة</strong>.</li>
<li>حدد مساحة عمل <strong>المخزون الفعلي</strong>.</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>عرض المخزون الفعلي لمنتج باستخدام مساحة العمل المحمولة للمخزون الفعلي
1.  على جهازك المحمول، حدد مساحة عمل **المخزون المتاح**.
2.  حدد **تحديد المخزون الفعلي لصنف معين**. يمكن الآن رؤية قائمة المنتجات المُحمّلة على تطبيقك للاستخدام دون اتصال. بشكل افتراضي، تم تحميل 50 صنف، ولكن باستطاعة المطور تغيير هذا الرقم. للحصول على مزيد من المعلومات، يجب على المطورين الاطلاع على [النظام الأساسي للمحمول Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
3.  إذا لم يكن الصنف الخاص بك في القائمة، حدد **بحث عن المزيد** للقيام ببحث عبر إنترنت في Dynamics 365 for Operations. البحث حسب رقم المنتج، أو قم بالتبديل إلى بحث حسب اسم المنتج.
4.  حدد منتجًا. إذا كان الصنف يحتوي على صورة، فسوف تظهر الصورة.
5.  حدد أحد الخيارات التالية لعرض حالة المخزون الفعلي:
    -   عرض الكمية الحالية لكل موقع
    -   عرض الكمية الحالية لكل مستودع
    -   عرض الكمية الحالية لكل موقع
    -   عرض الكمية الحالية لكل دفعة (ينطبق ذلك على المنتجات الخاضعة للدفعة)
    -   عرض الكمية الحالية لكل حالة مخزون

    يتم عرض منتجات المخزون المتاح بالطريق التالية:
    -   حسب المخزون الفعلي (يمثل هذا العرض المبلغ الإجمالي.)
    -   حسب المخزون الفعلي (يمثل هذا العرض المبلغ المحجوز.)
    -   حسب المخزون الفعلي المتوفر (يمثل هذا العرض المبلغ المتاح والذي لا تنطبق عليه أي حجوزات.)






