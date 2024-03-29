---
title: استكشاف المشاكل وإصلاحها أثناء الإعداد الأولي
description: توفر هذه المقالة المعلومات التي يمكن أن تساعدك على إصلاح المشكلات التي قد تحدث في أثناء الإعداد الأولي لتكامل الكتابة الثنائية.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289503"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>استكشاف المشاكل وإصلاحها أثناء الإعداد الأولي

[!include [banner](../../includes/banner.md)]

توفر هذه المقالة معلومات استكشاف الأخطاء وإصلاحها في تكامل الكتابة المزدوجة بين تطبيقات التمويل والعمليات وDataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء الإعداد الأولي لتكامل الكتابة الثنائية.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي تتناولها هذه المقالة إما منصب مسؤول النظام أو بيانات اعتماد مسؤول مستأجر Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>لا يمكنك ربط تطبيق التمويل والعمليات بـ Dataverse

**الدور المطلوب لتعيين الكتابة المزدوجة:** مسؤول النظام في تطبيقات التمويل والعمليات وDataverse.

تحدث الأخطاء في صفحة **رابط الإعداد لـ Dataverse** عادة بسبب وجود مشكلات الإعداد غير المكتمل أو المشكلات المتعلقة بالأذونات. تأكد من نجاح عملية التحقق من الصحة الكاملة في صفحة **رابط الإعداد لـ Dataverse**، كما هو مبين في التوضيح التالي. لا يمكنك ربط الكتابة الثنائية إلا إذا نجحت عملية التحقق من الصحة الكاملة.

![عملية التحقق من السلامة الناجحة.](media/health_check.png)

يجب أن يكون لديك بيانات اعتماد مسؤول مستأجر Azure AD لربط بيئات التمويل والعمليات وDataverse. بعد ربط البيئات، يمكن للمستخدمين تسجيل الدخول باستخدام بيانات اعتماد الحساب الخاص بهم وتحديث خريطة جدول موجودة.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>البحث عن الحد الخاص بعدد الجداول القانونية أو الشركات التي يمكن ربطها للكتابة الثنائية

قد تظهر رسالة الخطأ التالية عندما تحاول تمكين المخططات:

*فشل الكتابة المزدوجة - فشل تسجيل المكون الإضافي: [(يتعذر الحصول على مخطط تقسيم لمشروع DWM- 1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. تجاوز الخطأ الحد الأقصى للأقسام المسموح بها لتعيين DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)]، حدث خطأ واحد أو أكثر.*

الحد الحالي عند ربط البيئات هو تقريبًا 40 جدولاً قانونيًا. يحدث هذا الخطأ إذا حاولت تمكين المخططات وكان أكثر من 40 جدولاً قانونيًا مرتبطًا بين البيئات.

## <a name="connection-set-failed-while-linking-environment"></a>فشل تعيين الاتصال أثناء ربط البيئة

أثناء ربط بيئة الكتابة المزدوجة، يفشل الإجراء مع رسالة خطأ:

*فشل حفظ مجموعة الاتصال! تمت إضافة عنصر بنفس المفتاح بالفعل.*

لا يدعم الكتابة المزدوجة كيانات/شركات قانونية متعددة تحمل نفس الاسم. على سبيل المثال، إذا كان لديك شركتين مع اسم "DAT" في Dataverse ثم سوف تحصل على رسالة الخطأ هذه.

لإلغاء حظر العميل، قم بإزالة السجلات المكررة من جدول **cdm_company** في Dataverse. أيضًا، إذا كان الجدول **cdm_company** يحتوي على سجلات باسم فارغ، قم بإزالة هذه السجلات أو تصحيحها.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>خطأ عند فتح صفحة الكتابة المزدوجة في تطبيقات التمويل والعمليات

قد تتلقى رسالة الخطأ التالية عند محاولتك ربط بيئة Dataverse للكتابة المزدوجة:

*لا يشير رمز حالة الاستجابة إلى النجاح: 404 (لم يتم العثور عليه).*

يحدث هذا الخطأ عندما لا تكتمل خطوة موافقة التطبيق. يمكنك التحقق مما إذا كان قد تم تقديم الموافقة عن طريق تسجيل الدخول إلى `portal.azure.com` باستخدام حساب مسؤول المستأجر، والتحقق مما إذا كان تطبيق الجهة الخارجية مع المعرف `33976c19-1db5-4c02-810e-c243db79efde` يظهر في قائمة تطبيقات المؤسسة في AAD. إذا لم يكن الأمر كذلك، فقم بإعادة تشغيل خطوة الموافقة كما هو موضح في القسم التالي.

### <a name="providing-app-consent"></a>توفير موافقة التطبيق

+ قم بتشغيل عنوان URL التالي باستخدام بيانات اعتماد المسؤول.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ حدد **قبول** للموافقة. أنت تقدم الموافقة على تثبيت التطبيق (مع `id=33976c19-1db5-4c02-810e-c243db79efde`) في المستأجر الخاص بك.
+ هذا التطبيق مطلوب لـ Dataverse للاتصال بتطبيقات التمويل والعمليات.

    ![استكشاف أخطاء إعداد المزامنة الأولية وإصلاحها.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> إذا لم يفلح ذلك، فقم بتشغيل عنوان URL في الوضع الخاص لـ Microsoft Edge أو وضع التصفح المتخفي في Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>بيئة التمويل والعمليات غير قابلة للاكتشاف

قد تتلقى رسالة الخطأ التالية:

*بيئة تطبيقات التمويل والعمليات \*\*\*.cloudax.dynamics.com غير قابلة للاكتشاف.*

هناك أمران يمكن أن يسببا مشكلة في البيئة التي لا يمكن اكتشافها:

+ المستخدم الذي تم استخدامه لتسجيل الدخول ليس في نفس المستأجر حيث مثيل التمويل والعمليات.
+ هناك بعض مثيلات التمويل والعمليات القديمة التي استضافتها Microsoft والتي كانت بها مشكلة في الاكتشاف. لإصلاح هذا، قم بتحديث مثيل التمويل والعمليات. تصبح البيئة قابلة للاكتشاف مع أي تحديث.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>خطا 403 (محظور) اثناء إنشاء الاتصالات

كجزء من عمليه أضافه ارتباطات الكتابة المزدوجة، يتم إنشاء اتصالين (يعرفان Power Apps أيضا بالاتصالات *الأبيبه* ) بالنيابة عن المستخدم في البيئة المرتبطة Dataverse. إذا لم يكن لدي العميل ترخيص للبيئة Power Apps ، يفشل إنشاء اتصالات ApiHub، ويظهر خطا 403 (محظور). فيما يلي مثال على رسالة الخطأ:

> الرسالة =\[فشل في اعداد بيئة الكتابة الثنائية. تفاصيل الخطأ: رمز حالة الاستجابة لا يشير إلى النجاح: 403 (ممنوع). - رمز حالة الاستجابة لا يشير إلى النجاح: 403 (ممنوع).\] STACKTRACE=\[   at Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs: السطر 297 --- نهاية تتبع المكدس من الموقع السابق حيث تم طرح استثناء --- في System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw () في System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification (TaskAwaiter.HandleNonSuccessAndDebugger) في Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

يحدث هذا الخطأ بسبب نقص Power Apps الترخيص. قم بتعيين ترخيص مناسب (علي سبيل المثال ، الخطة التجريبية Power Apps )2 للمستخدم بحيث يكون لدي المستخدم الاذن لإنشاء الاتصالات. للتحقق من الترخيص ، يمكن للعميل الانتقال إلى [حسابي](https://portal.office.com/account/?ref=MeControl#subscriptions) لعرض التراخيص التي تم تعيينها للمستخدم حاليًا.

لمزيد من المعلومات حول Power Apps الترخيص ، راجع المقالات التالية:

- [تعيين التراخيص للمستخدمين](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [شراء Power Apps لمؤسستك](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

