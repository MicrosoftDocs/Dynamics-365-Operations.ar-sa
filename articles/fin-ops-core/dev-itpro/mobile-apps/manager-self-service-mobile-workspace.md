---
title: مساحة عمل جوال فريقي
description: توفر هذه المقالة معلومات عن مساحة العمل المحمولة فريقي، التي تسمح للمديرين بعرض المرؤوسين المباشرين وفريق العمل الموسع.
author: ShielaSogge
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f15ac24e5c32a42863cac8a9c9754c95aa4ff734
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868687"
---
# <a name="my-team-mobile-workspace"></a>مساحة عمل جوال فريقي

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

توفر هذه المقالة معلومات عن مساحة العمل المحمولة **فريقي**. تسمح مساحة العمل هذه للمدراء بعرض المرؤوسين المباشرين وفريق العمل الموسع.‬ ويمكنهم أيضًا إرسال ثناء إلى الأفراد في سلسلة التدرج الهرمي.

مساحة العمل المحمولة هذه مخصصة للاستخدام مع تطبيق Finance and Operations للأجهزة المحمولة. 

## <a name="overview"></a>نظرة عامة 
تسمح مساحة العمل المحمولة **فريقي** للمستخدمين بتنفيذ هذه المهام:

- عرض قائمة بالمرؤوسين المباشرين للمدير.
- عرض قائمة بفريق المرؤوسين الموسع التابع للمدير.
- عرض معلومات مفصلة حول عضو في الفريق، مثل معلومات عن تاريخ الميلاد وتاريخ الأقدمية وسنوات الخدمة والتعويض والأداء.
- إرسال ثناء لأي فرد من أعضاء فريق المرؤوسين الموسع التابع للمدير.

## <a name="prerequisites"></a>المتطلبات الأساسية
قبل أن تتمكن من استخدام مساحة العمل المحمولة هذه، يجب عليك تلبية المتطلبات الأساسية التالية.

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
<td>يجب أن يتم نشر أحد المنتجات التالية في مؤسستك:
<ul><li>تطبيق Finance and Operations</li>
<li>Microsoft Dynamics 365 Human Resources</li>
</ul>
</td>
<td>مسؤول النظام</td>
<td>إذا لم يتم نشر &#39; Finance and Operations في مؤسستك، فراجع نشر <a href="../deployment/deploy-demo-environment.md">نشر بيئة عرض توضيحي</a>. إذا لم يتم نشر Human Resources في مؤسستك، فباستطاعة مسؤول النظام الوصول إلى إصدار تجريبي من <a href="https://dynamics.microsoft.com/human-resources/overview/">صفحة ويب Human Resources</a>.
</td>
</tr>
<tr class="even">
<td>يجب نشر مساحة العمل المحمولة <strong>فريقي</strong>.</td>
<td>مسؤول النظام</td>
<td>راجع <a href="publish-mobile-workspace.md">نشر مساحة عمل محمولة</a></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>تنزيل وتثبيت تطبيق المحمول

تنزيل وتثبيت تطبيق Finance and Operations للأجهزة المحمولة:

-   [لهواتف Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [لهواتف iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>تسجيل الدخول إلى تطبيق الهاتف الجوال
1.  ابدأ تشغيل التطبيق على جهازك المحمول.
2.  أدخل عنوان URL لـ Microsoft Dynamics 365.
3.  في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك. أدخل بيانات اعتمادك.
4.  بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك. تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.

[![سحب للتحديث.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a>عرض أعضاء الفريق باستخدام مساحة العمل المحمولة "فريقي"
1.  في تطبيق المحمول، حدد مساحة عمل **فريقي**. تظهر قائمة بأعضاء الفريق. تعرض القائمة أيضًا المسمة الوظيفي لكل عضو من أعضاء الفريق، وأي مرؤوسين مباشرين لديه.
2.  حدد أحد أعضاء الفريق. تظهر صفحة **ملخص عضو الفريق**. تتضمن المعلومات في هذه الصفحة معلومات عن تاريخ ميلاد عضو الفريق وتاريخ الأقدمية وسنوات الخدمة وسنوات العمل في المنصب الحالي والتعويض.

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a>عرض أعضاء الفريق الموسع باستخدام مساحة العمل المحمولة "فريقي"
1.  في تطبيق المحمول، حدد مساحة عمل **فريقي**. تظهر قائمة بأعضاء الفريق. تعرض القائمة أيضًا المسمة الوظيفي لكل عضو من أعضاء الفريق، وأي مرؤوسين مباشرين لديه.
1.  حدد الارتباط **المرؤوسون المباشرون**. تظهر قائمة بأعضاء الفريق الموسع.
1.  حدد أحد أعضاء الفريق. تظهر صفحة **ملخص عضو الفريق**. تتضمن المعلومات في هذه الصفحة معلومات عن تاريخ ميلاد عضو الفريق وتاريخ الأقدمية وسنوات الخدمة وسنوات العمل في المنصب الحالي والتعويض.

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a>إرسال ثناء حول أعضاء الفريق باستخدام مساحة العمل المحمولة "فريقي"
1.  في تطبيق المحمول، حدد مساحة عمل **فريقي**. تظهر قائمة بأعضاء الفريق. تعرض القائمة أيضًا المسمة الوظيفي لكل عضو من أعضاء الفريق، وأي مرؤوسين مباشرين لديه.
1.  حدد أحد أعضاء الفريق. تظهر صفحة **ملخص عضو الفريق**.
1.  حدد **إرسال ثناء**. 
1. أدخل نص الثناء الذي تريد إرساله. 
1. حدد **تم**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
