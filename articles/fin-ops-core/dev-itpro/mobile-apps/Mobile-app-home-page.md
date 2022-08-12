---
title: الصفحة الرئيسية لتطبيق الأجهزة المحمولة
description: توضح هذه المقالة تطبيق التمويل والعمليات ‏(Dynamics 365) للأجهزة المحمولة، وتوفر ارتباطات إلى موارد يمكنها أن تساعدك على تطبيقه في مؤسستك.
author: ChrisGarty
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 973fdcd81a83b6b70e8fa941c4f0c9d24b5cb559
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066442"
---
# <a name="mobile-app-home-page"></a>الصفحة الرئيسية لتطبيق الأجهزة المحمولة

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

توضح هذه المقالة تطبيق **التمويل والعمليات (Dynamics 365)** للأجهزة المحمولة، وتوفر ارتباطات إلى موارد يمكنها أن تساعدك على تطبيقه في مؤسستك.

## <a name="overview"></a>نظرة عامة

يسمح تطبيق الأجهزة المحمولة لمؤسستك بجعل عمليات الأعمال لديها متوفرة على الأجهزة المحمولة. بعد أن يقوم مسؤول تقنية المعلومات بتمكين مساحات العمل المحمولة لمؤسستك، يمكن للمستخدمين تسجيل الدخول إلى التطبيق وبدء تشغيل عمليات الأعمال على الفور من أجهزتهم المحمولة. يتضمن تطبيق الأجهزة المحمولة الميزات التالية التي يمكن أن تساعدك في زيادة الإنتاجية:

- باستطاعة المستخدمين عرض بيانات العمل وتحريرها والعمل عليها، حتى عندما يكون الاتصال بالشبكة متقطعًا أو عندما تكون أجهزتهم المحمولة غير متصلة تمامًا. عندما يعيد جهاز تأسيس اتصال شبكة، تتم مزامنة عمليات البيانات دون اتصال بشكل تلقائي.
- باستطاعة المطورين أو مسؤولي تقنية المعلومات بناء ونشر مساحات العمل المحمولة التي تم تخصيصها لمؤسستهم. يستخدم التطبيق أصول التعليمات البرمجية الموجودة. لذلك، لا يلزم إعادة تنفيذ إجراءات التحقق من الصحة أو منطق التسلسل العمل أو تكوين الأمان.
- باستطاعة مسؤولي تقنية المعلومات أو المطورين تصميم مساحات العمل المحمولة بسهولة باستخدام مصمم مساحات العمل بالتأشير والنقر المضمن مع عميل ويب.
- باستطاعة المطورين أو مسؤولي تقنية المعلومات تحسين قدرات العمل دون اتصال في مساحات العمل المحمولة بشكل اختياري باستخدام إطار عمل قابلية لتوسعة منطق تسلسل العمل. نظراً لاستمرار معالجة البيانات بينما يكون الجهاز في وضع عدم الاتصال، تبقى سيناريوهات المحمول غنية وسلسة، حتى لو لم يتوفر للأجهزة اتصال ثابت بالشبكة.

## <a name="elements-of-the-mobile-app"></a>عناصر تطبيق الأجهزة المحمولة
يتكوّن التنقل في تطبيق الأجهزة المحمولة من أربعة مفاهيم أساسية: لوحة المعلومات ومساحات العمل والصفحات والإجراءات. 

[![مفاهيم التنقل في تطبيق الأجهزة المحمولة.](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. عند بدء تشغيل التطبيق، يمكنك الانتقال إلى **لوحة المعلومات**.
2. في لوحة المعلومات، يمكنك مشاهدة قائمة تتضمن **مساحات عمل** التي تم نشرها.
3. في كل مساحة عمل، يمكنك رؤية قائمة تضمّ **الصفحات** التي تتوفر لمساحة العمل تلك.
4. بعد أن تصل إلى صفحة، يمكنك تنفيذ العديد من الإجراءات. فيما يلي بعض الأمثلة:

    - عرض البيانات التفصيلية.
    - الانتقال إلى صفحات أخرى للبيانات ذات الصلة، مثل تفاصيل الكيان أو البنود.
    - عرض قائمة تتضمن **الإجراءات** التي تتوفر لتلك الصفحة. تسمح لك الإجراءات بإنشاء أو تحرير البيانات الموجودة.

## <a name="implementation-process"></a>عملية التطبيق
يعرض الرسم التوضيحي التالي عملية تنفيذ مساحات العمل المحمولة التي يتم توفيرها من قبل Microsoft ومساحات العمل المحمولة المخصصة. 

[![عملية تنفيذ تطبيقات الأجهزة المحمولة.](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

يتضمن الجدول التالي ارتباطات إلى الموارد التي يمكن أن تساعدك في تنفيذ مساحات العمل المحمولة التي يتم توفيرها من قبل Microsoft ومساحات العمل المحمولة المخصصة. تتوافق الأرقام في العمود الأول مع الخطوات المرقمة في الرسم التوضيحي السابق.

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
<td>تنفيذ تطبيق Finance and Operations في المؤسسة الخاصة بك.</td>
<td><ul><li>إذا لم تكن قد قمت بعد بنشر إصدار من Microsoft Dynamics 365، فراجع <a href="../deployment/deploy-demo-environment.md">نشر بيئة عرض توضيحي</a>.</li><li>لمشاهدة قائمة بمساحات العمل المحمولة التي يمكن استخدامها، راجع <a href="mobile-workspaces-released.md">مساحات العمل المحمولة التي تم إصدارها مؤخرًا</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>مسؤول النظام</td>
<td><strong>إذا كنت تستخدم الإصدار 1611 من Microsoft Dynamics 365 for Operations:</strong> يمكنك تنزيل وتثبيت مقالات قاعدة المعارف التي تمكّن مساحات العمل المحمولة التي توفرها Microsoft.</td>
<td>راجع الموضوعات التالية لمزيد من المعلومات:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">مساحة العمل المحمولة للتحكم في التكلفة</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">مساحة عمل محمولة للمخزون الفعلي</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">مساحات العمل المحمولة لأوامر المبيعات</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">مساحة العمل المحمولة لتعاون المورد</a></li>
<li><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">مساحة عمل محمولة لإدخال وقت المشروع</a></li>
<li><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">مساحة عمل محمولة لإدارة المصروفات</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>مسؤول النظام</td>
<td>نشر مساحات العمل المحمولة التي توفرها Microsoft.</td>
<td><a href="publish-mobile-workspace.md">نشر مساحة عمل محمولة</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>مطور أو مورِّد برامج مستقل (ISV)</td>
<td>استخدام النظام الأساسي للمحمول لإنشاء مساحات عمل محمولة مخصصة.</td>
<td><a href="platform/mobile-platform-home-page.md">النظام الأساسي للأجهزة المحمولة</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>مورِّد برامج مستقل (ISV)</td>
<td>إنشاء حزمة قابلة للنشر تحتوي على مساحات عمل محمولة مخصصة، وتحميل الحزمة إلى Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">إنشاء حزمة قابلة للنشر</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>مسؤول النظام</td>
<td>تطبيق الحزمة القابلة للنشر التي تحتوي على مساحات العمل المخصصة التي يوفرها مورّد البرامج المستقل (ISV).</td>
<td><a href="../deployment/apply-deployable-package-system.md">تطبيق حزمة قابلة للنشر</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>مسؤول النظام</td>
<td>نشر مساحات العمل المحمولة المخصصة التي يوفرها مورّد البرامج المستقل (ISV).‬</td>
<td><a href="publish-mobile-workspace.md">نشر مساحة عمل محمولة</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>المستخدم</td>
<td>تنزيل وتثبيت تطبيق الأجهزة المحمولة.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and operations app ل Android</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and operations app ل iOS</a><BR/>
(Windows Phone غير معتمد)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>المستخدم</td>
<td>تسجيل الدخول واستخدام تطبيق الأجهزة المحمولة. يتضمن التطبيق مساحات العمل المحمولة التي تم نشرها بواسطة مسؤول النظام.</td>
<td>لرؤية قائمة بمساحات العمل المحمولة التي توفرها Microsoft، راجع <a href="mobile-workspaces-released.md">مساحات العمل المحمولة التي تم إصدارها مؤخرًا</a>.
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها
[موارد النظام الأساسي للجوال](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

