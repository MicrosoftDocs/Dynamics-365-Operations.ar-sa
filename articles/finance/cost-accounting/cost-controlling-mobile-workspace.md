---
title: مساحة العمل المحمولة للتحكم في التكلفة
description: تقدم هذه المقالة معلومات عن مساحة العمل المحمولة التحكم في التكلفة. تسمح مساحة العمل هذه لمدراء مركز التكلفة بعرض معلومات حول أداء مراكز التكلفة في أي وقت وفي أي مكان.
author: AndersGirke
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2d6d3fdcc0b0387a92f138b0ba7cf537f473b91a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069552"
---
# <a name="cost-controlling-mobile-workspace"></a>مساحة العمل المحمولة للتحكم في التكلفة

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

تقدم هذه المقالة معلومات عن مساحة العمل المحمولة **التحكم في التكلفة**. تسمح مساحة العمل هذه لمدراء مركز التكلفة بعرض معلومات حول أداء مراكز التكلفة في أي وقت وفي أي مكان.

مساحة العمل المحمولة هذه مخصصة للاستخدام مع تطبيق Finance and Operations (Dynamics 365) للأجهزة المحمولة. 

## <a name="overview"></a>نظرة عامة
توفر مساحة العمل المحمولة **التحكم في التكلفة** طريقة عرض فورية للأداء الحالي لمراكز التكلفة من خلال مقارنة التكاليف الفعلية في مقابل التكاليف المُدرجة في الموازنة. يمكنك التنقل لأسفل لمشاهدة حالة عناصر التكلفة الفردية.

على سبيل المثال، يستلم أحد الموظفين دعوة لحضور مؤتمر دولي، ولكن يجب أن تغطي المؤسسة كافة مصروفات السفر. يسأل الموظف مديره إذا كان بإمكانه حضور المؤتمر. يفتح المدير مساحة العمل المحمولة **التحكم في التكلفة** على جهازه المحمول، لمعرفة إذا ما كان لديه ميزانية تتيح للموظف حضور المؤتمر أم لا.

### <a name="data-security"></a>أمان البيانات
تتم حماية البيانات في مساحة العمل المحمولة **التحكم في التكلفة** عبر بيانات اعتماد المستخدم. يُسمح لمدير مركز التكلفة فقط برؤية بيانات مركز التكلفة الخاص به. تتم إدارة أمان مستوى الوصول ضمن وحدة **محاسبة التكاليف**.

يحدد محاسبو التكلفة تكوين مساحة العمل المحمولة **التحكم في التكلفة** في وحدة **التحكم في التكلفة‏‎**. بعد نشر مساحة العمل على تطبيق الأجهزة المحمولة، ستكون متوفرة في التطبيق. وبالتالي، سيتمكن جميع مدراء مراكز التكلفة في المؤسسة من عرض البيانات بالتنسيق نفسه.

### <a name="actions-views-and-links"></a>الإجراءات، وطرق العرض والارتباطات
توفر مساحة العمل المحمولة **التحكم في التكلفة** الإجراءات التالية، وطرق العرض والارتباطات:

-   **الإجراءات:**

    -   استخدم **تحديد التكوين** لتحديد تخطيط.
    -   استخدم **حدد الكائن التكلفة** لتحديد مراكز التكلفة لتصفية البيانات عليها.
    
        > [!NOTE]
        > تتوقف مراكز التكلفة التي تظهر في القائمة على الوصول الممنوح في وحدة **محاسبة التكاليف**.

-   **طرق العرض:** استنادًا إلى الإجراءات المحددة والتكوين في وحدة **محاسبة التكاليف** يمكنك عرض المعلومات التالية في البطاقات:

    -   القيمة الفعلية مقابل الموازنة (الفترة الحالية)
    -   القيمة الفعلية مقابل الموازنة المراجعة (الفترة الحالية)
    -   الفعلي مقابل الموازنة (الفترة السابقة)
    -   الفعلي مقابل الموازنة التي تمت مراجعتها (الفترة السابقة)
    -   الفعلي مقابل الموازنة (السنة حتى تاريخه)
    -   الفعلي مقابل الموازنة التي تمت مراجعتها (السنة حتى تاريخه)

    تظهر المبالغ التالية على كل بطاقة: الفعلي والموازنة والفرق والفرق %.

-   **الارتباطات:**

    -   تفاصيل للفترة الحالية
    -   تفاصيل للفترة السابقة
    -   تفاصيل السنة حتى تاريخه

    عندما تقوم بتحديد ارتباط، تظهر بطاقة لكل عنصر التكلفة. تظهر المبالغ التالية على كل بطاقة: الفعلي والموازنة وفرق الموازنة وفرق الموازنة % والموازنة التي تمت مراجعتها وفرق الموازنة التي تمت مراجعتها وفرق الموازنة التي تمت مراجعتها %.
    
    [![بطاقة لعنصر تكلفة.](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>المتطلبات الأساسية
تختلف المتطلبات الأساسية، استنادًا إلى إصدار Microsoft Dynamics 365 الذي تم نشره لمؤسستك.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>المتطلبات الأساسية عند استخدام Microsoft Dynamics 365 Finance
إذا تم نشر Finance لمؤسستك، فيتعين على مسؤول النظام نشر مساحة العمل المحمولة **التحكم في التكلفة**‬. للاطلاع على الإرشادات، راجع [نشر مساحة العمل المحمولة ](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>المتطلبات الأساسية إذا كنت تستخدم الإصدار 1611 مع Platform update 3 أو إصدار لاحق
إذا تم نشر الإصدار 1611 مع Platform update 3 أو إصدار أحدث لمؤسستك، فيجب على مسؤول النظام إكمال المتطلبات الأساسية التالية.

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
<td>تطبيق قاعدة المعارف 4013633.</td>
<td>مسؤول النظام</td>

<td>إن KB 4013633 عبارة عن تحديث X++ أو إصلاح عاجل لبيانات التعريف يحتوي على مساحة العمل المحمولة <strong>التحكم في التكاليف</strong>. لتطبيق KB 4013633، يجب أن يتبع مسؤول النظام الخطوات التالية.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">تنزيل الإصلاح العاجل لبيانات التعريف من Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>SCMMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">تطبيق الحزمة القابلة للنشر</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>نشر مساحة العمل المحمولة لـ <strong>التحكم في التكاليف</strong>.</td>
<td>مسؤول النظام</td>
<td>راجع <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">نشر مساحة عمل محمولة</a></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>تنزيل وتثبيت تطبيق المحمول
تنزيل وتثبيت تطبيق Finance and Operations (Dynamics 365) للأجهزة المحمولة:

-   [لهواتف Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [لهواتف iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>تسجيل الدخول إلى تطبيق الهاتف الجوال

1.  ابدأ تشغيل التطبيق على جهازك المحمول.
2.  أدخل عنوان URL لـ Dynamics 365.
3.  في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك. أدخل بيانات اعتمادك.
4.  بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك. تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.

[![سحب للتحديث.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>عرض أداء مركز التكلفة باستخدام مساحة العمل المحمولة للتحكم في التكلفة

1.  على جهازك المحمول، حدد مساحة عمل **التحكم في التكلفة**.
2.  حدد **التحكم في كائن التكلفة**.
3.  حدد **الإجراءات**.
4.  حدد **تحديد التكوين** لتحديد تخطيط التحكم في التكلفة.
5.  حدد **تم**.
6.  حدد **الإجراءات**.
7.  حدد **تحديد كائن التكلفة** لتحديد مراكز التكلفة التي تم منحك حق الوصول إليها.
8.  حدد **تم**.
9.  عرض الأداء الإجمالي لمركز التكلفة الخاص بك.
10. حدد الارتباط **تفاصيل للفترة الحالية**.
11. عرض أداء عناصر تكاليف الفردية.
12. يمكنك أيضا البحث عن عناصر تكلفة معينة.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

