---
title: استكشاف المشاكل وإصلاحها مع وحدة الكتابة المزدوجة في تطبيقات Finance and Operations
description: يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها الذي يمكن أن يساعدك في إصلاح المشكلات ذات الصلة بوحدة الكتابة الثنائية في تطبيقات Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997364"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>استكشاف المشاكل وإصلاحها مع وحدة الكتابة المزدوجة في تطبيقات Finance and Operations

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service. على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها في وحدة **الكتابة الثنائية** في تطبيقات Finance and Operations.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>لا يمكنك تحميل وحدة الكتابة المزدوجة في تطبيق Finance and Operations

إذا لم تتمكن من فتح صفحة **الكتابة الثنائية** بتحديد تجانب **الكتابة الثنائية** في مساحة عمل **إدارة البيانات** ، فربما تكون خدمة تكامل البيانات معطلة. أنشئ تذكرة دعم لطلب إعادة تشغيل خدمة تكامل البيانات.

## <a name="error-when-you-try-to-create-a-new-entity-map"></a>حدث خطأ عند محاولة إنشاء تعيين كيان جديد

**بيانات الاعتماد المطلوبة لإصلاح المشكلة** : نفس المستخدم الذي قام بإعداد الكتابة المزدوجة.

قد تتلقى رسالة الخطأ التالية عند محاولة تكوين كيان جديد للكتابة المزدوجة. المستخدم الوحيد الذي يمكنه إنشاء خريطة هو المستخدم الذي قام بإعداد اتصال الكتابة المزدوجة.

*لا يشير رمز حالة الاستجابة إلى النجاح: 401 (غير مرخص)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>حدث خطأ عند فتح واجهة مستخدم الكتابة الثنائية

قد تتلقى رسالة الخطأ التالية عند محاولة الوصول إلى الكتابة الثنائية من مساحة عمل **إدارة البيانات** :

*login.microsoftonline.com رفض الاتصال.*

لإصلاح المشكلة، قم بتسجيل الدخول باستخدام إطار InPrivate في Microsoft Edge أو في إطار وضع التخفي في Chromium أو في إطار وضع التخفي في Google Chrome. يجب أيضا إلغاء حظر ملفات تعريف ارتباط الجهات الخارجية أو مسحها.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>حدث خطأ عند ربط البيئة للكتابة الثنائية أو إضافة تعيين كيان جديد

**الدور المطلوب لحل المشكلة:** مسؤول النظام في كل من تطبيقات Finance and Operations وCommon Data Service.

قد تواجه الخطأ التالي عند الارتباط بالمخططات أو إنشائها:

*لا يشير رمز حالة الاستجابة إلى النجاح: 403 (tokenexchange).<br> معرف جلسة العمل: \<your session id\><br> معرف نشاط الجذر: \<your root activity id\>*

يمكن أن يحدث هذا الخطأ إذا لم يكن لديك الأذونات الكافية للربط بين الكتابة الثنائية أو إنشاء المخططات. يمكن أن يحدث هذا الخطأ إذا تمت إعادة تعيين بيئة Common Data Service بدون إلغاء ربط الكتابة المزدوجة. يمكن لأي مستخدم يتمتع بدور مسؤول النظام في كل من تطبيقات Finance and Operations وCommon Data Service ربط البيئات. يمكن فقط للمستخدم الذي قام بإعداد اتصال الكتابة المزدوجة إضافة تعيينات لكيانات جديدة. بعد الإعداد، يمكن لأي مستخدم يتمتع بدور مسؤول النظام مراقبة الحالة وتحرير التعيينات.

## <a name="error-when-you-stop-the-entity-mapping"></a>حدث خطأ عند إيقاف تعيين الكيان

قد تظهر رسالة الخطأ التالية عندما تحاول إيقاف تعيينات الكيانات:

*\[ممنوع\]، \[{"status":403,"source":"","message":"خطأ من رمز التبديل المميز: غير مسموح للمستخدم بالوصول إلى dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]، أرجع الخادم البعيد خطأ: (403) ممنوع.*

يحدث هذا الخطأ عندما تكون بيئة Common Data Service المرتبطة غير متوفرة.

لإصلاح المشكلة، أنشئ تذكرة لفريق تكامل البيانات. قم بإرفاق تتبع الشبكة حتى يتمكن فريق تكامل البيانات من وضع علامة على المخططات باعتبارها **ليست قيد التشغيل** في النهاية الخلفية.

## <a name="error-while-trying-to-start-an-entity-mapping"></a>حدث خطأ أثناء محاولة بدء تعيين كيان

قد تتلقي خطأ مثل التالي عند محاولة تعيين تلك الحالة من التعيين إلى **قيد التشغيل:**

*تعذر إكمال مزامنة البيانات الأولية. خطأ: فشل في الكتابة المزدوجة - فشل تسجيل المكون الإضافي: تعذر إنشاء بيانات تعريف لبحث الكتابة المزدوجة. خطأ لم يتم تعيين مرجع كائن إلى مثيل كائن.*

يعتمد إصلاح هذا الخطأ على سبب الخطأ:

+ إذا كان التعيين يتضمن تعيينات تابعة، فتأكد من تمكين التعيينات التابعة لتعيين هذا الكيان.
+ قد يكون التعيين مفتقدًا لحقول المصدر أو الوجهة. في حالة فقدان حقل في تطبيق Finance and Operations، اتبع الخطوات الموجودة في القسم [مشكلة فقدان حقول الكيان في التعيينات](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps). في حالة فقدان حقل في Common Data Service، عندئذ انقر فوق **تحديث الكيانات** على التعيين بحيث يتم ملء الحقول تلقائيًا إلى التعيين.
