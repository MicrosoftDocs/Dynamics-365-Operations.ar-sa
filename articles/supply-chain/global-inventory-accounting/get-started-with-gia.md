---
title: الشروع في العمل في ‏‫محاسبة المخزون العالمي
description: يصف هذا المقال كيفية الشروع في العمل مع محاسبة المخزون العالمي.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 493e0be8ab56abc2a3253876107b7f4fefabf4ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891078"
---
# <a name="get-started-with-global-inventory-accounting"></a>الشروع في العمل في ‏‫محاسبة المخزون العالمي

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

تتيح لك محاسبة المخزون العالمي إجراء محاسبات متعددة للمخزون في دفاتر الأستاذ العام لمحاسبة المخزون العالمي التي قمت بإعدادها. يمكنك إقران كل دفتر أستاذ لمحاسبة المخزون العالمي بـ *اصطلاح*. والاصطلاح هو مجموعة من الأنواع التالية من سياسات المحاسبة:

- كائن التكلفة
- أساس قياس الإدخال
- افتراض تدفق التكلفة
- عنصر التكلفة

> [!NOTE]
> حتى بعد تشغيل خدمة محاسبة المخزون العالمي، ما يزال بإمكانك إجراء محاسبة المخزون في Microsoft Dynamics 365 Supply Chain Management كما هو معتاد.

تُعد محاسبة المخزون العالمي وظيفة إضافية. ولجعل ميزاتها متوفرة، يجب أن تثبتها من Microsoft Dynamics Lifecycle Services (LCS). يمكنك اختيار تقييمها في بيئة اختبار قبل تشغيلها في بيئات التشغيل.

لا تدعم محاسبة المخزون العالمي حاليًا كافة ميزات إدارة التكلفة المضمنة في Supply Chain Management. بالتالي، من المهم أن تجري تقييمًا بشأن ما إذا كانت مجموعة الميزات المتوفرة حاليًا ستلبي متطلباتك أم لا.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>كيفية الحصول على الوظيفة الإضافية Global Inventory Accounting

> [!IMPORTANT]
> لاستخدام محاسبة المخزون العام، يجب أن يكون لديك بيئة عالية التوفر ممكن بها LCS (ليس بيئة OneBox). بالإضافة إلى ذلك، يجب تشغيل Supply Chain Management الإصدار 10.0.19 أو إصدار لاحق.

### <a name="supply-chain-management-version-10019-to-10026"></a>إصدار Supply Chain Management من 10.0.19 إلى 10.0.26

لتثبيت محاسبه المخزون العام لإصدار Supply Chain Management 10.0.19 ل10.0.26 ، أبدا بتثبيت [الوظيفة الاضافيه](#install). ثم قم بإرسال معرف بيئة الLCS واسم الشركة بالبريد الكتروني إلى فريق [محاسبه المخزون العمومي ](mailto:GlobalInvAccount@microsoft.com). سيرسل لك الفريق رسالة متابعة بالبريد الإلكتروني تحتوي على نقاط نهاية خدمة Global Inventory Accounting.

### <a name="supply-chain-management-version-10027-and-later"></a>إصدار Supply Chain Management 10.0.27 والإصدارات الأحدث

لتثبيت Global Inventory Accounting for Supply Chain Management الإصدار 10.0.27 والإصدارات الأحدث،  [فقط ثبّت الوظيفة الإضافي](#install). بالنسبة لهذه الإصدارات من Supply Chain Management ، يتم اعداد النقاط النهائية لخدمه محاسبه المخزون العام تلقائيا ، لذا لا تحتاج إلى البحث عنها يدويا. في حاله مواجهه إيه مشكلات اثناء اعداد الوظيفة الاضافيه ، الرجاء الاتصال بفريق [محاسبه المخزون العام ](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>الترخيص

يجري ترخيص محاسبة المخزون العالمي معًا مع الميزات القياسية لمحاسبة المخزون المتوفرة لـ Supply Chain Management. لا يتعين عليك شراء ترخيص إضافي لاستخدام محاسبة المخزون العالمي.

## <a name="prerequisites"></a>المتطلبات الأساسية

### <a name="set-up-microsoft-power-platform-integration"></a>إعداد تكامل Microsoft Power Platform

قبل تمكين وظيفة الوظيفة الإضافية، فإنه يجب التكامل مع Microsoft Power Platform باتباع الخطوات التالية.

1. افتح بيئة LCS حيث تريد إضافة الخدمة بها.
1. انتقل إلى **التفاصيل الكاملة**.
1. في القسم **تكامل Power Platform**، حدد **إعداد**.
1. في مربع الحوار **إعداد بيئة Power platform**، حدد خانة الاختيار، ثم حدد **إعداد** وعادةً، يستغرق الإعداد بين 60 و90 دقيقة.
1. بعد اكتمال الإعداد الخاص بالبيئة Microsoft Power Platform، تعرض الصفحة اسم البيئة الخاصة بك. بالإضافة إلى ذلك، يعرض القسم تكامل **Power Platform** الكشف و"تم إكمال إعداد البيئة Power Platform". لا تتطلب محاسبة المخزون العالمي تطبيقًا ثنائي الكتابة.

لمزيد من المعلومات، راجع [التمكين بعد نشر البيئة](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

### <a name="set-up-dataverse"></a>إعداد Dataverse

قبل إعداد Dataverse، قم بإضافة مبادئ خدمة محاسبة المخزون العالمي إلى المستأجر باتباع الخطوات التالية.

1. قم بتثبيت وحدة Azure AD النمطية لـ Windows PowerShell الإصدار 2 كما هو موضح في [تثبيت Azure Active Directory PowerShell للرسم البياني](/powershell/azure/active-directory/install-adv2).
1. قم بتشغيل الأمر PowerShell التالي.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

بعد ذلك، قم بإنشاء مستخدمي التطبيق لمحاسبة المخزون العالمي في Dataverse باتباع الخطوات التالية.

1. افتح عنوان URL الخاص ببيئة Dataverse الخاصة بك.
1. انتقل إلى **إعدادات متقدمة \> النظام \> الأمان \> المستخدمين**، وقم بإنشاء مستخدم تطبيق. استخدم الحقل **عرض** لتغيير طريقة عرض الصفحة إلى *مستخدمي التطبيق*.
1. حدد **جديد**.
1. عيّن الحقل **معرف التطبيق** إلى *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. حدد **تعيين دور**، ثم حدد *مسؤول النظام*. إذا كان هناك دور يسمي *مستخدم Common Data Service*، فحدده أيضًا.
1. كرر الخطوات السابقة، ولكن قم بتعيين الحقل **معرف التطبيق** إلى *5f58fc56-0202-49a8-ac9e-0946b049718b*.

لمزيد من المعلومات، راجع [إنشاء مستخدم تطبيق](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

إذا لم تكن اللغة الإنجليزية لتثبيت Dataverse هي اللغة الافتراضية، اتبع الخطوات التالية.

1. انتقل إلى **إعداد متقدم \> الإدارة \> اللغات**.
1. حدد *الإنجليزية* (*LanguageCode=1033*)، ثم حدد **تطبيق**.

## <a name="install-the-add-in"></a><a name="install"></a>تثبيت الوظيفة الإضافية

اتبع هذه الخطوات لتثبيت الوظيفة الإضافية بحيث يمكنك استخدام محاسبة المخزون العالمي.

1. سجل الدخول إلى [LCS](https://lcs.dynamics.com/Logon/Index).
1. افتح بيئة LCS حيث تريد إضافة الخدمة بها.
1. انتقل إلى **التفاصيل الكاملة**.
1. انتقل إلى **تكامل Power Platform**، وحدد **إعداد**.
1. في مربع الحوار **إعداد بيئة Power platform**، حدد خانة الاختيار، ثم حدد **إعداد** وعادةً، يستغرق الإعداد بين 60 و90 دقيقة.
1. بعد إكمال إعداد بيئة Microsoft Power Platform، في علامة التبويب السريعة **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
1. حدد **محاسبة المخزون العالمي**.
1. اتبع دليل التثبيت، ووافق على البنود والشروط.
1. حدد **تثبيت**.
1. في علامة التبويب السريعة **الوظائف الإضافية للبيئة**، يجب أن تشاهد محاسبة المخزون العالمي قد تم تثبيتها. بعد بضع دقائق، يجب أن تغير الحالة من *قيد التثبيت* إلى *مثبت*. (قد تحتاج إلى تحديث الصفحة لعرض هذا التغيير.) في تلك النقطة، تكون محاسبة المخزون العالمي جاهزة للاستخدام.

## <a name="set-up-the-integration"></a>إعداد التكامل

اتبع هذه الخطوات لإعداد التكامل بين محاسبة المخزون العالمي وSupply Chain Management.

1. سجل دخولك إلى Supply Chain Management.
1. انتقل إلى **إدارة النظام \> إدارة الميزات**.
1. حدد **التحقق من وجود تحديثات**.
1. في علامة التبويب **الكل**، ابحث عن الميزة التي تسمى *محاسبة المخزون العالمي*.
1. حدد **تمكين الآن**.
1. انتقل إلى **محاسبة المخزون العالمي \> الإعداد \> معلمات محاسبة المخزون العالمي \> معلمات التكامل**.
1. بناءً على إصدار Supply Chain Management الذي تقوم بتشغيله ، قم بإحدى الخطوات التالية:
    - **10.0.19 إصدار Supply Chain Management ل10.0.26** : في حقول نقطه نهاية **خدمه البيانات** والخاصة **بنقطه نهاية** محاسبه المخزون العام ، ادخل عناوين url التي تم إرسالها اليك من خلال البريد الكتروني من فريق محاسبه المخزون العام (راجع أيضا [كيفيه الحصول علي الوظيفة الاضافيه](#sign-up)لمحاسبه المخزون العمومي).
    - **إصدار Supply Chain Management 10.0.27 وأحدث** : لا يلزم إدخال نقاط النهاية ، لذا يمكنك تخطي هذه الخطوة.

محاسبة المخزون العالمي جاهزة الآن للاستخدام.
