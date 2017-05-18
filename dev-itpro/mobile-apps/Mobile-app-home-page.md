---
title: "الصفحة الرئيسية لتطبيق Dynamics 365 for Operations للأجهزة المحمولة"
description: "يصف هذا الموضوع تطبيق Microsoft Dynamics 365 for Operations للأجهزة المحمولة ويوفر ارتباطات إلى موارد يمكن أن تساعدك في تطبيقه في مؤسستك."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>الصفحة الرئيسية لتطبيق Dynamics 365 for Operations للأجهزة المحمولة

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


يصف هذا الموضوع تطبيق Microsoft Dynamics 365 for Operations للأجهزة المحمولة ويوفر ارتباطات إلى موارد يمكن أن تساعدك في تطبيقه في مؤسستك.

<a name="overview"></a>نظرة عامة
--------

يسمح تطبيق Microsoft Dynamics 365 for Operations للأجهزة المحمولة لمؤسستك بجعل عمليات الأعمال لديها متوفرة على الأجهزة المحمولة. بعد أن يقوم مسؤول تقنية المعلومات بتمكين ميزة مساحات العمل المحمولة لمؤسستك، يمكن للمستخدمين تسجيل الدخول إلى التطبيق وبدء تشغيل عمليات الأعمال على الفور من أجهزتهم المحمولة. يتضمن تطبيق Dynamics 365 for Operations للأجهزة المحمولة الميزات التالية التي يمكن أن تساعدك في زيادة الإنتاجية:

-   باستطاعة المستخدمين عرض بيانات العمل وتحريرها والعمل عليها، حتى عندما يكون الاتصال بالشبكة متقطعًا أو عندما تكون أجهزتهم المحمولة غير متصلة تمامًا. عند يعيد جهاز تأسيس اتصال شبكة، تتم مزامنة العمليات على البيانات دون اتصال بشكل تلقائي مع Dynamics 365 لعمليات.
-   باستطاعة المطورين أو مسؤولي تقنية المعلومات بناء ونشر مساحات العمل المحمولة التي تم تخصيصها لمؤسستهم. يستخدم التطبيق أصول التعليمات البرمجية الموجودة. لذلك، لا يلزم إعادة تنفيذ إجراءات التحقق من الصحة أو منطق التسلسل العمل أو تكوين الأمان.
-   باستطاعة المطورين أو مسؤولي تقنية المعلومات تصميم مساحات العمل المحمولة بسهولة باستخدام مصمم مساحات العمل بالتأشير والنقر المضمن في عميل ويب Dynamics 365 for Operations.
-   باستطاعة المطورين أو مسؤولي تقنية المعلومات تحسين قدرات العمل دون اتصال في مساحات العمل المحمولة بشكل اختياري باستخدام إطار عمل قابلية لتوسعة منطق تسلسل العمل. نظراً لاستمرار معالجة البيانات بينما يكون الجهاز في وضع عدم الاتصال، تبقى سيناريوهات المحمول غنية وسلسة، حتى لو لم يتوفر للأجهزة اتصال ثابت بالشبكة.

## <a name="elements-of-the-mobile-app"></a>عناصر تطبيق الأجهزة المحمولة
يتكوّن التنقل في تطبيق الأجهزة المحمولة من أربعة مفاهيم بسيطة: لوحة المعلومات ومساحات العمل والصفحات والإجراءات. 

[![مفاهيم التنقل في تطبيق الأجهزة المحمولة](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   عند بدء تشغيل التطبيق، يمكنك الانتقال إلى **لوحة المعلومات**.
-   في لوحة المعلومات، يمكنك مشاهدة قائمة تضمّ **مساحات عمل** التي يتم نشرها في بيئة Dynamics 365 for Operations.
-   في كل مساحة عمل، يمكنك رؤية قائمة تضمّ **الصفحات** التي تتوفر لمساحة العمل تلك.
-   في إحدى الصفحات، يمكنك عرض البيانات التي تم جمعها من صفحة واحدة أو أكثر في Dynamics 365 for Operations.
-   من صفحة، يمكنك الانتقال إلى صفحات أخرى للبيانات ذات الصلة، مثل تفاصيل الكيان أو البنود.
-   في صفحة، يمكنك أيضًا رؤية قائمة تضمّ **الإجراءات** التي تتوفر لتلك الصفحة.
-   تسمح لك الإجراءات بإنشاء أو تحرير البيانات الموجودة.

## <a name="implementation-process"></a>عملية التطبيق
يبين الرسم التوضيحي التالي عملية تطبيق Dynamics 365 for Operations للأجهزة المحمولة في مؤسسةك. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

يتضمن الجدول التالي ارتباطات إلى موارد من يمكنها مساعدتك في تطبيق Dynamics 365 for Operations للأجهزة المحمولة في مؤسستك. تتوافق الأرقام في العمود الأول مع الخطوات المرقمة في الرسم التوضيحي السابق.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>الخطوة</th>
<th>الدور</th>
<th>إجراء</th>
<th>موارد لمساعدتك على إكمال الإجراء</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>مسؤول النظام</td>
<td>تطبيق Dynamics 365 for Operations للمؤسسة.</td>
<td>في حال عدم نشر Dynamics 365 for Operations في المؤسسة، راجع <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">نشر بيئة عرض توضيحي Microsoft Dynamics 365 for Operations</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>مسؤول النظام</td>
<td>تنزيل وتثبيت مقالات قاعدة المعارف التي تمكّن مساحات العمل المحمولة التي توفرها قبل Microsoft.</td>
<td>راجع قسم &quot;المتطلبات الأساسية‬&quot; في الموضوع المتعلق بمساحة العمل المحمولة التي تريد مؤسستك استخدامها:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">مساحة العمل المحمولة للتحكم في التكلفة</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">مساحة العمل المحمولة للمخزون الفعلي</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">مساحات العمل المحمولة لأوامر المبيعات</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">مساحة العمل المحمولة لتعاون المورد</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">مساحة العمل المحمولة لإدخال وقت المشروع</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>مسؤول النظام</td>
<td>نشر مساحات العمل المحمولة التي توفرها Microsoft.</td>
<td>راجع قسم &quot;المتطلبات الأساسية‬&quot; في الموضوع المتعلق بمساحة العمل المحمولة التي تريد مؤسستك استخدامها:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">مساحة العمل المحمولة للتحكم في التكلفة</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">مساحة العمل المحمولة للمخزون الفعلي</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">مساحات العمل المحمولة لأوامر المبيعات</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">مساحة العمل المحمولة لتعاون المورد</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">مساحة العمل المحمولة لإدخال وقت المشروع</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>مطور أو مورِّد برامج مستقل (ISV)</td>
<td>استخدام إطار عمل Dynamics 365 for Operations للأجهزة المحمولة لإنشاء مساحات عمل محمولة مخصصة.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">إطار عمل Dynamics 365 for Operations للأجهزة المحمولة</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">مساحة عمل X++ APIs لـ Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>مورِّد برامج مستقل (ISV)</td>
<td>إنشاء حزمة قابلة للنشر تحتوي على مساحات عمل محمولة مخصصة، وتحميل الحزمة إلى Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">إنشاء حزمة قابلة للنشر</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>مسؤول النظام</td>
<td>تطبيق الحزمة قابلة للنشر التي تحتوي على مساحات العمل المخصصة التي يوفرها مورّد البرامج المستقل (ISV).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">تطبيق حزمة قابلة للنشر على نظام Microsoft Dynamics 365 for Operations</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>مسؤول النظام</td>
<td>نشر مساحات العمل المحمولة المخصصة التي يوفرها مورّد البرامج المستقل (ISV).‬</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">نشر مساحة عمل محمولة</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>المستخدم</td>
<td>تنزيل وتثبيت تطبيق Dynamics 365 for Operations للأجهزة المحمولة.</td>
<td><ul>
<li>لـ Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations على Google Play Store</a></li>
<li>لـ iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations على iTunes apps store</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>المستخدم</td>
<td>تسجيل الدخول إلى تطبيق Dynamics 365 for Operations للأجهزة المحمولة واستخدامه. يتضمن التطبيق مساحات العمل المحمولة التي تم نشرها.</td>
<td>قامت Microsoft بتوفير مساحات العمل المحمولة التالية:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">مساحة العمل المحمولة للتحكم في التكلفة</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">مساحة العمل المحمولة للمخزون الفعلي</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">مساحات العمل المحمولة لأوامر المبيعات</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">مساحة العمل المحمولة لتعاون المورد</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">مساحة العمل المحمولة لإدخال وقت المشروع</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>راجع أيضًا
--------

[مساحات العمل المحمولة التي تم إصدارها مؤخرًا لتطبيق Dynamics 365 for Operations للأجهزة المحمولة](mobile-workspaces-released.md)





