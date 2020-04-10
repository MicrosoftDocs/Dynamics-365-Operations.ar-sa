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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172750"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>استكشاف المشاكل وإصلاحها مع وحدة الكتابة المزدوجة في تطبيقات Finance and Operations

[!include [banner](../../includes/banner.md)]



يوفر هذا الموضوع معلومات حول استكشاف أخطاء تكامل الكتابة الثنائية وإصلاحها بين تطبيقات Finance and Operations وCommon Data Service. على وجه التحديد، يوفر هذا الموضوع استكشاف الأخطاء وإصلاحها في وحدة **الكتابة الثنائية** في تطبيقات Finance and Operations.

> [!IMPORTANT]
> قد تتطلب بعض المشكلات التي يتناولها هذا الموضوع إما دور إدارة النظام أو بيانات اعتماد مسؤول مستأجر  Microsoft Azure Active Directory (Azure AD). يوضح القسم الخاص بكل مشكلة ما إذا كانت هناك حاجة إلى دور محدد أو بيانات اعتماد.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>لا يمكنك تحميل وحدة الكتابة الثنائية في تطبيق Finance and Operations

إذا لم تتمكن من فتح صفحة **الكتابة الثنائية** بتحديد تجانب **الكتابة الثنائية** في مساحة عمل **إدارة البيانات**، فربما تكون خدمة تكامل البيانات معطلة. أنشئ تذكرة دعم لطلب إعادة تشغيل خدمة تكامل البيانات.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>حدث خطأ عند محاولة إنشاء تعيين كيان جديد

**بيانات الاعتماد المطلوبة لإصلاح المشكلة:** مسؤول مستأجر Azure AD

قد تتلقى رسالة الخطأ التالية عند محاولة تكوين كيان جديد للكتابة الثنائية:

*لا يشير رمز حالة الاستجابة إلى النجاح: 401 (غير مرخص)*

يحدث هذا الخطأ نظرًا لأنه يمكن لمسؤول مستأجر Azure AD فقط إضافة تعيين كيان جديد.

لإصلاح هذه المشكلة، قم بتسجيل الدخول إلى تطبيق Finance and Operations كمستأجر مسؤول Azure AD. كما يجب عليك الانتقال إلى موقع web.PowerApps.com وإعادة التحقق من اتصالك.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>حدث خطأ عند فتح واجهة مستخدم الكتابة الثنائية

قد تتلقى رسالة الخطأ التالية عند محاولة الوصول إلى الكتابة الثنائية من مساحة عمل **إدارة البيانات**:

*login.microsoftonline.com رفض الاتصال.*

لإصلاح المشكلة، قم بتسجيل الدخول باستخدام إطار InPrivate في Microsoft Edge أو في إطار وضع التخفي في Chromium أو في إطار وضع التخفي في Google Chrome. يجب أيضا إلغاء حظر ملفات تعريف ارتباط الجهات الخارجية أو مسحها.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>حدث خطأ عند ربط البيئة للكتابة الثنائية أو إضافة تعيين كيان جديد

**بيانات الاعتماد المطلوبة لإصلاح المشكلة:** مسؤول مستأجر Azure AD

قد تواجه الخطأ التالي عند الارتباط بالمخططات أو إنشائها:

*لا يشير رمز حاله الاستجابة إلى النجاح: 403 (tokenexchange).<br>معرف جلسة العمل: \<معرف جلسة العمل\><br> معرف النشاط الجذر \<معرف النشاط الجذر الخاص بك\>*

يمكن أن يحدث هذا الخطأ إذا لم يكن لديك الأذونات الكافية للربط بين الكتابة الثنائية أو إنشاء المخططات. يجب عليك استخدام حساب مسؤول مستأجر Azure AD لربط البيئات وإضافة تعيينات جديدة للكيانات. ولكن، بعد الإعداد، يمكنك استخدام حساب غير مسؤول لمراقبه الحالة وتحرير التعيينات.

## <a name="error-when-you-stop-the-entity-mapping"></a>حدث خطأ عند إيقاف تعيين الكيان

قد تظهر رسالة الخطأ التالية عندما تحاول إيقاف تعيينات الكيانات:

*\[ممنوع\]، \[{"status":403,"source":"","message":"خطأ من رمز التبديل المميز: غير مسموح للمستخدم بالوصول إلى dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]، أرجع الخادم البعيد خطأ: (403) ممنوع.*

يحدث هذا الخطأ عندما تكون بيئة Common Data Service المرتبطة غير متوفرة.

لإصلاح المشكلة، أنشئ تذكرة لفريق تكامل البيانات. قم بإرفاق تتبع الشبكة حتى يتمكن فريق تكامل البيانات من وضع علامة على المخططات باعتبارها **ليست قيد التشغيل** في النهاية الخلفية.
