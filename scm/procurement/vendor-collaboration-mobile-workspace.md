---
title: "مساحة العمل المحمولة‬ لتعاون المورّد في تطبيق Microsoft Dynamics 365 for Operations"
description: "من خلال مساحة العمل المحمولة‬ لتعاون المورّد، باستطاعة المورّدين البقاء على اطلاع دائم على أوامر الشراء التي تم إرسالها إليهم للموافقة عليها وعرض معلومات حول أوامر الشراء وجهات الاتصال الجديدة والمحدثة."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>مساحة العمل المحمولة‬ لتعاون المورّد في تطبيق Microsoft Dynamics 365 for Operations

من خلال مساحة العمل المحمولة‬ لتعاون المورّد، باستطاعة المورّدين البقاء على اطلاع دائم على أوامر الشراء التي تم إرسالها إليهم للموافقة عليها وعرض معلومات حول أوامر الشراء وجهات الاتصال الجديدة والمحدثة.

<a name="prerequisites"></a>المتطلبات الأساسية
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>المتطلب الأساسي</th>
<th>‏‏الوصف</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>اقرأ حول النظام الأساسي للمحمول لـ Microsoft Dynamics 365 for Operations</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">النظام الأساسي للمحمول Dynamics 365 for Operations</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>تأكد من أنك تستخدم بيئة تحتوي على Microsoft Dynamics 365 for Operations إصدار 1611، والإصدار 3 من تحديث النظام الأساسي لـ Microsoft Dynamics 365 for Operations (نوفمبر 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">جهاز محمول تم فيه تثبيت تطبيق Dynamics 365 for Operations</span></td>
<td><span style="color: #000000;">تنزيل تطبيق Dynamics 365 for Operations من متجر التطبيقات على جهازك المحمول.</span></td>
</tr>
<tr class="even">
<td>الإصلاح العاجل KB 3215650</td>
<td>تثبيت الإصلاح العاجل لتمكين مساحات العمل التي تم توفيرها في Dynamics 365 for Operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">الإصلاح العاجل KB 3216943</span> </span></td>
<td>تثبيت الإصلاح العاجل لتمكين مساحة العمل المحمولة‬ لتعاون المورّد.</td>
</tr>
<tr class="even">
<td>يجب أن يتوفر لدى مورّد المستخدم حق الوصول إلى واجهة ويب لتعاون المورّد في Dynamics 365 for Operations وإعداد مستخدم لتعاون المورّد.</td>
<td>اتبع الخطوات الموضحة في المواضيع التالية لإعداد واجهة ويب لتعاون المورّد واستخدامها.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">استخدام تعاون المورّد للعمل مع مورّدين خارجيين</a></li>
<li><a href="manage-vendor-collaboration-users.md">إدارة مستخدمي تعاون المورد‬</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">إعداد تعاون المورد والمحافظة عليه</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">استخدام تعاون المورّد للعمل مع عملاء في Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>نظرة عامة
تسمح مساحة العمل المحمولة‬ لتعاون المورّد للمورّدين بالبقاء على اطلاع دائم على أوامر الشراء الجديدة لكي يتمكنوا من رؤية أوامر الشراء والاستجابة لها في عميل ويب Dynamics 365 for Operations.  

**ملاحظة:** يجب استخدام مساحة العمل المحمولة‬ لتعاون المورّد كملحق لواجهة ويب لتعاون المورّد، ولكن ليس كبديل.  

من خلال مساحة العمل المحمولة‬ لتعاون المورّد، باستطاعة المورّدين الآن عرض أوامر الشراء الجديدة المرسلة للموافقة عليها. وتعرض مساحة العمل هذه معلومات حول أوامر الشراء، مثل المنتجات والكمية وتواريخ التسليم المطلوب. وتتوفر معلومات حول الأسعار، وهذا يتوقف على تكوين كل مورّد.  

عندما يسجل مستخدم دخوله كمورّد، سيرى أوامر الشراء التي تمت الاستجابة لها، أو أوامر الشراء التي ما زالت تنتظر قيام العميل باتخاذ الإجراء المناسب. من المحتمل أن يكون المورّد قد اقترح تاريخ تسليم آخر لم يتم الاتفاق عليه بعد مع العميل، ولذلك ينتظر أمر الشراء قيام العميل باتخاذ الإجراء المناسب. وسيرى المورّد أيضًا قائمة بأوامر الشراء التي تم تأكيدها ولكن لم يتم تسليمها بعد.  

للاستجابة لأمر شراء، يجب على المورّد استخدام واجهة ويب لتعاون المورّد المتوفرة في عميل ويب Dynamics 365 for Operations. وهذا أيضًا المكان حيث سيحصل المورّد على مزيد من المعلومات حول الأمر، مثل مرفقات المستندات وعنوان التسليم لكل بند، والتكاليف المقترنة بالمورّد.  

باستخدام دور أمان خاص، يستطيع المورّد معرفة جهات الاتصال المسجلة لحساب مورّد. وباستخدام دور الأمان نفسه، يستطيع المورّد عرض حالة أي طلب من طلبات المستخدم التي تم إرسالها.  

يجب إنشاء جهات اتصال جديدة وتقديم طلبات مستخدمين جدد في واجهة تعاون المورّد المتوفرة في عميل ويب Dynamics 365 for Operations.  

باستخدام مساحة العمل المحمولة، يستطيع المورّد:

-   عرض أوامر الشراء الجديدة المرسلة إلى المورّد.
-   عرض أوامر الشراء التي استجاب لها المورّد والتي تنتظر قيام العميل باتخاذ الإجراء المناسب.
-   عرض أوامر الشراء المؤكدة والتي لم يتم استلامها بشكل تام.
-   عرض معلومات جهة الاتصال التي تم تسجيلها لحساب المورّد (يحتاج ذلك إلى دور أمان إضافي).
-   عرض معلومات حول طلب مستخدم تم إرساله من قِبل المورّد ومتابعة حالة الطلب (يحتاج هذ الأمر إلى دور أمان إضافي).

## <a name="get-started"></a>بدء الاستخدام
لبدء التشغيل على جهازك المحمول:

1.  في متجر التطبيقات على هاتفك المحمول، يمكنك تحميل وتثبيت تطبيق Microsoft Dynamics 365 for operations.
2.  بدء تشغيل التطبيق على جهازك.
3.  أدخل عنوان URL لـ Dynamics 365.
4.  أدخل الشركة لتسجيل الدخول إلى. على سبيل المثال، أدخل **USMF**.
5.  في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بحسابك على تطبيق Microsoft Dynamics 365 for Operations. 

بعد أن تقوم بتسجيل الدخول إلى التطبيق، لا توجد أي مساحات عمل مرئية. لعرض مساحات العمل على التطبيق المحمول الخاص بك، يجب عليك أولًا نشر مساحات العمل المطلوبة على تطبيق Dynamics 365 for Operations. إنك تحتاج إلى إذن مسؤول النظام لنشر مساحة العمل.

1.  بدء تشغيل Dynamics 365 for Operations.
2.  انتقل إلى **إدارة النظام** &gt; **إعداد** &gt; **محددات النظام**.
3.  حدد **إدارة تطبيق المحمول**.
4.  حدد مساحة عمل **تعاون المورّد** للنشر إلى النظام الأساسي للمحمول.
5.  حدد **نشر مساحة العمل**.
6.  قم بتحديث جهازك لمعرفة مساحات العمل المنشورة.
7.  حدد مساحة عمل **تعاون المورّد**. ستنتقل إلى الصفحة التالية.

[![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>جهات الاتصال
تسمح لك صفحة **جهات الاتصال** برؤية كافة جهات الاتصال التي تم إعدادها لحساب المورّد. وهي تعرض اسم جهة الاتصال وعنوان البريد الإلكتروني الأساسي والاسم المستعار للمستخدمين، عند توفره. وتُظهر أيضًا ما إذا كان حساب مستخدم جهة الاتصال عبارة عن حساب نشط. عندما تحدد جهة اتصال، ستتمكن من رؤية تفاصيل جهة الاتصال، مثل الكيانات القانونية التي يُعتبر الشخص بمثابة جهة اتصال لها، ومعلومات الاتصال مثل رقم هاتف أو عنوان بريد إلكتروني مختلف.

## <a name="user-requests"></a>طلبات المستخدم
تسمح لك صفحة **طلبات المستخدم** برؤية كافة طلبات المستخدمين التي أرسلتها عبر واجهة ويب تعاون المورّد، وتسمح لك أيضًا بمتابعة حالة هذه الطلبات. عندما تحدد طلب مستخدم، يمكنك معرفة ما تم طلبه وإضافة مستخدم أو إلغاء تنشيطه وتغيير الأمان والاطلاع على أدوار الأمان التي تم طلبها للمستخدم.

## <a name="purchase-orders-ready-for-review"></a>أوامر الشراء الجاهزة للمراجعة
تسمح لك صفحة **أوامر الشراء الجاهزة للمراجعة** برؤية كل أوامر الشراء التي تم إرسالها من قبل العميل والتي لم يتم الردّ عليها. ويمكنك عرض معلومات محددة حول الأمر، مثل المنتجات التي تم طلبها والتاريخ الذي يجب أن يتم فيه تسليم هذه المنتجات. وتتوفر معلومات حول السعر فقط إذا تم تكوين ذلك للمورّد.  

يمكنك رؤية إن كان أوامر الشراء تتضمن مرفقات أو ملاحظات. لفتح المرفقات، تحتاج إلى استخدام تعاون المورّد في عميل ويب. حدد **سطر أمر الشراء** لرؤية كافة الأسطر بالتفاصيل. تجدر الإشارة إلى ظهور مؤشر، لكل بند، لعرض ما إذا كان هناك ملاحظات أو مرفقات، أو إذا كان هناك عنوان تسليم يختلف عن العنوان الذي يظهر في الرأس.  

للاستجابة لأمر شراء، يجب استخدام تعاون المورّد في عميل ويب.

## <a name="awaiting-customer-action"></a>انتظار إجراء العميل
تسمح لك الصفحة **انتظار إجراء العميل‬** بالعثور على أوامر الشراء التي استجبت أنت لها أو استجاب لها شخص آخر في شركتك لديه حق الوصول إلى تعاون المورّد. وتكون أوامر الشراء مرئية فقط في هذه القائمة إذا أحتاج العميل لتنفيذ أحد الإجراءات التالية على أمر الشراء.

-   إذا تم رفض أمر الشراء، قد يحتاج العميل إما إلى تحديث الأمر المرسل وإرساله مرة أخرى، أو إلغاء الأمر وإعادة إرساله. عند إرسال أمر الشراء مرة أخرى، سوف يختفي من صفحة **انتظار إجراء العميل‬**.
-   إذا تم قبول أمر الشراء مع تغييرات، سيحتاج العميل إلى تحديث الأمر الأصلي وإعادة إرساله للمراجعة، أو تحديثه وفقًا للتغييرات وتأكيده على الفور. وفي الحالتين، سوف يختفي أمر الشراء من صفحة **انتظار إجراء العميل‬**.
-   إذا تم قبول أمر الشراء وظهر في صفحة **انتظار إجراء العميل**، فسبب ذلك يعود إلى عدم تأكيد أمر الشراء تلقائيًا عندما تم قبوله. وهو ينتظر قيام وكيل الشراء بتغيير الأمر إلى "مؤكد". بشكل عام، يُعتبر أمر الشراء بمثابة اتفاقية بين العميل والمورّد فور موافقة المورّد على الأمر. وسيكون نقل أمر الشراء إلى الحالة "مؤكد" مجرد إجراء شكلي.

عند تحديد أمر الشراء، تظهر تفاصيل إضافية حول الاستجابة. يمكنك رؤية تفاصيل البند والاستجابة لكل بند. تُظهر حالة البند الاستجابات التالية التي تم منحها.

-   مقبول
-   مرفوض
-   تم القبول مع التغييرات
-   تم الاستبدال/بديل
-   تقسيم الجدول/بند الجدول‬

لاحظ وجود مؤشر يعرض **التسليم‬**= نعم/لا، ويتم استخدامه للإشارة إلى أنه لن يتم تسليم البنود. قد يعود سبب ذلك إلى رفض البند أو استبداله حيث من غير المتوقع تسليم البنود الأصلية، أو أن أحد البنود قد تم تقسيمه إلى عدة بنود جدول ومن غير المتوقع تسليم البند الأصلي كما ورد في الأمر المستلم.  

يتم عرض أي تغييرات تم إدخالها على الاستجابة لبند أمر، باستثناء ما يتعلق بالملاحظات والمرفقات التي تم تحميلها، والتي يمكن رؤيتها باستخدام واجهة ويب لتعاون المورّد.

## <a name="open-confirmed-orders"></a>الأوامر المؤكدة المفتوحة
عندما يؤكد العميل أمر الشراء، مما يعني أن حالة أمر الشراء تغيرت إلى "مؤكد"، يظهر أمر الشراء هذا في قائمة الأوامر المؤكدة المفتوحة. وسوف يبقى في القائمة حتى يتم تسجيله على أنه أمر استلمه العميل.

