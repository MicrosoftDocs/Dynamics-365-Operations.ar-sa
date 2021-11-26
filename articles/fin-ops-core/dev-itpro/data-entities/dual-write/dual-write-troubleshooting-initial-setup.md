---
title: استكشاف المشاكل وإصلاحها أثناء الإعداد الأولي
description: يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء الإعداد الأولي لتكامل الكتابة الثنائية.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c9bf5d9017579b4207e09769cff38361442e3938
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781430"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>استكشاف المشاكل وإصلاحها أثناء الإعداد الأولي

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وDataverse. على وجه التحديد، يوفر هذا الموضوع المعلومات التي يمكن أن تساعدك في إصلاح المشكلات التي قد تحدث أثناء الإعداد الأولي لتكامل الكتابة الثنائية.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>لا يمكنك ربط تطبيق Finance and Operations بـ Dataverse

**الدور المطلوب لتعيين الكتابة المزدوجة:** مسؤول النظام في تطبيقات Finance and Operations وDataverse.

تحدث الأخطاء في صفحة **رابط الإعداد لـ Dataverse** عادة بسبب وجود مشكلات الإعداد غير المكتمل أو المشكلات المتعلقة بالأذونات. تأكد من نجاح عملية التحقق من الصحة الكاملة في صفحة **رابط الإعداد لـ Dataverse**، كما هو مبين في التوضيح التالي. لا يمكنك ربط الكتابة الثنائية إلا إذا نجحت عملية التحقق من الصحة الكاملة.

![عملية التحقق من السلامة الناجحة.](media/health_check.png)

يجب أن يكون لديك بيانات اعتماد مسؤول مستأجر Azure AD لربط بيئات Finance and Operations وDataverse بعد ربط البيئات، يمكن للمستخدمين تسجيل الدخول باستخدام بيانات اعتماد الحساب الخاص بهم وتحديث خريطة جدول موجودة.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>البحث عن الحد الخاص بعدد الجداول القانونية أو الشركات التي يمكن ربطها للكتابة الثنائية

قد تظهر رسالة الخطأ التالية عندما تحاول تمكين المخططات:

*فشل الكتابة المزدوجة - فشل تسجيل المكون الإضافي: [(يتعذر الحصول على مخطط تقسيم لمشروع DWM- 1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. تجاوز الخطأ الحد الأقصى للأقسام المسموح بها لتعيين DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)]، حدث خطأ واحد أو أكثر.*

الحد الحالي عند ربط البيئات هو تقريبًا 40 جدولاً قانونيًا. يحدث هذا الخطأ إذا حاولت تمكين المخططات وكان أكثر من 40 جدولاً قانونيًا مرتبطًا بين البيئات.

## <a name="connection-set-failed-while-linking-environment"></a>فشل تعيين الاتصال أثناء ربط البيئة

أثناء ربط بيئة الكتابة المزدوجة، يفشل الإجراء مع رسالة خطأ:

*فشل حفظ مجموعة الاتصال! تمت إضافة عنصر بنفس المفتاح بالفعل.*

لا يدعم الكتابة المزدوجة كيانات/شركات قانونية متعددة تحمل نفس الاسم. على سبيل المثال، إذا كان لديك شركتين مع اسم "DAT" في Dataverse ثم سوف تحصل على رسالة الخطأ هذه.

لإلغاء حظر العميل، قم بإزالة السجلات المكررة من جدول **cdm_company** في Dataverse. أيضًا، إذا كان الجدول **cdm_company** يحتوي على سجلات باسم فارغ، قم بإزالة هذه السجلات أو تصحيحها.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>خطأ عند فتح صفحة الكتابة المزدوجة في تطبيقات Finance and Operations

قد تتلقى رسالة الخطأ التالية عند محاولتك ربط بيئة Dataverse للكتابة المزدوجة:

*لا يشير رمز حالة الاستجابة إلى النجاح: 404 (لم يتم العثور عليه).*

يحدث هذا الخطأ عندما لا تكتمل خطوة موافقة التطبيق. يمكنك التحقق مما إذا كان قد تم تقديم الموافقة عن طريق تسجيل الدخول إلى `portal.azure.com` باستخدام حساب مسؤول المستأجر، والتحقق مما إذا كان تطبيق الجهة الخارجية مع المعرف `33976c19-1db5-4c02-810e-c243db79efde` يظهر في قائمة تطبيقات المؤسسة في AAD. إذا لم يكن الأمر كذلك، فقم بإعادة تشغيل خطوة الموافقة كما هو موضح في القسم التالي.

### <a name="providing-app-consent"></a>توفير موافقة التطبيق

+ قم بتشغيل عنوان URL التالي باستخدام بيانات اعتماد المسؤول.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ حدد **قبول** للموافقة. أنت تقدم الموافقة على تثبيت التطبيق (مع `id=33976c19-1db5-4c02-810e-c243db79efde`) في المستأجر الخاص بك.
+ هذا التطبيق مطلوب Dataverse للاتصال بتطبيقات Finance and Operations.

    ![استكشاف أخطاء إعداد المزامنة الأولية وإصلاحها.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> إذا لم يفلح ذلك، فقم بتشغيل عنوان URL في الوضع الخاص لـ Microsoft Edge أو وضع التصفح المتخفي في Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>بيئة Finance and Operations غير قابلة للاكتشاف

قد تتلقى رسالة الخطأ التالية:

*بيئة تطبيقات Finance and Operations \*\*\*.cloudax.dynamics.com غير قابل للاكتشاف.*

هناك أمران يمكن أن يسببا مشكلة في البيئة التي لا يمكن اكتشافها:

+ المستخدم المُستخدم لتسجيل الدخول ليس في نفس المستأجر مثل مثيل Finance and Operations.
+ هناك بعض مثيلات Finance and Operations القديمة التي استضافتها Microsoft والتي كانت بها مشكلة في الاكتشاف. لإصلاح هذا، قم بتحديث مثيل Finance and Operations. تصبح البيئة قابلة للاكتشاف مع أي تحديث.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
