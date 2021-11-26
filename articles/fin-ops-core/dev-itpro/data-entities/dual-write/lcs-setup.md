---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: يوضح هذا الموضوع كيفيه اعداد اتصال ثنائي الكتابة من Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1fd15b5d664fead10949750678a2d3eab967af22
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781382"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>إعداد الكتابة المزدوجة من Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوضح هذا الموضوع كيفية تمكين الكتابة المزدوجة من Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب إكمال تكامل Power Platform كما هو موضح في الموضوعات التالية:

+ [Power Platform التكامل - التمكين أثناء نشر البيئة](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [تكامل Power Platform - التمكين أثناء نشر البيئة](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>إعداد الكتابة المزدوجة لبيئات Dataverse الجديدة

اتبع هذه الخطوات لإعداد الكتابة المزدوجة من الصفحة **تفاصيل بيئة** LCS:

1. في الصفحة **تفاصيل البيئة**، قم بتوسيع القسم **تكامل Power Platform**.

2. حدد الزر **تطبيق الكتابة المزدوجة**.

    ![تكامل Power Platform.](media/powerplat_integration_step2.png)

3. راجع البنود والشروط، ثم حدد **تكوين**.

4. حدد **موافق** للمتابعة.

5. يمكنك مراقبة التقدم عن طريق تحديث صفحة تفاصيل البيئة بشكل دوري. يستغرق الإعداد عادة 30 دقيقة أو أقل.  

6. عند اكتمال الإعداد، تقوم رسالة بإعلامك في حالة نجاح العملية أو إذا فشلت. وفي حالة فشل الإعداد، يتم عرض رسالة خطأ مرتبطة. يجب إصلاح أية أخطاء قبل الانتقال إلى الخطوة التالية.

7. حدد **ارتباط إلى بيئة Power Platform** لإنشاء ارتباط بين Dataverse وقواعد البيانات الحالية الخاصة بالبيئة. يستغرق هذا عادة أقل من 5 دقائق.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="الربط ببيئة Power Platform .":::

8. عند اكتمال الارتباط، يتم عرض ارتباط تشعبي. استخدم الارتباط لتسجيل الدخول إلى منطقة إدارة الكتابة المزدوجة في البيئة Finance and Operations. ومن هناك، يمكنك إعداد تعيينات الكيانات.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>إعداد الكتابة المزدوجة لبيئة Dataverse موجودة

لإعداد الكتابة الزدوجة لبيئة Dataverse موجودة، يجب عليك إنشاء [بطاقة دعم Microsoft](../../lifecycle-services/lcs-support.md). يجب أن تتضمن التذكرة:

+ معرف بيئة Finance and Operations الخاص بك.
+ اسم البيئة الخاصة بك من Lifecycle Services.
+ معرف مؤسسة Dataverse أو معرف بيئة Power Platform من مركز مسؤول Power Platform. في البطاقة الخاصة بك، اطلب أن يكون المُعرف هو المثيل المستخدم لتكامل Power Platform.

> [!NOTE]
> لا يمكنك إلغاء ارتباط البيئات باستخدام LCS. لإلغاء ارتباط بيئة، افتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations، ثم حدد **إلغاء الارتباط**.

## <a name="linking-mismatch"></a>ربط عدم التطابق

من الممكن أن يتم ربط بيئة LCS بمثيل Dataverse واحد، بينما ترتبط بيئة الكتابة المزدوجة بمثيل Dataverse آخر. قد يؤدي عدم التطابق هذا الارتباط سلوك غير متوقع ثم قد ينتهي إرسال البيانات إلى بيئة خاطئة. البيئة الموصى بها لاستخدامها للكتابة المزدوجة هي البيئة التي يتم إنشاؤها كجزء من تكامل Power Platform، وعلى المدى الطويل، ستكون هذه هي الطريقة الوحيدة لإنشاء رابط بين البيئات.

إذا كانت البيئة لديك عدم تطابق ارتباط، يعرض LCS تحذيرا على صفحة تفاصيل البيئة الخاصة بك مشابهة ل "Microsoft قد اكتشفت أن البيئة الخاصة بك مرتبطة عبر الكتابة المزدوجة إلى وجهة مختلفة عن المحدد في تكامل Power Platform، وهو أمر غير مستحسن":

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="ارتباط تكامل Power Platform غير متطابق.":::

إذا واجهت هذا الخطأ هناك خياران، استنادا إلى احتياجاتك:

+ [إلغاء ربط وإعادة ربط بيئات الكتابة المزدوجة (إعادة تعيين الارتباط أو تغييره)](relink-environments.md#scenario-reset-or-change-linking)كما هو محدد في صفحة تفاصيل بيئة LCS. هذا هو الخيار المثالي، لأنه يمكنك تشغيله بدون دعم Microsoft.  
+ إذا أردت الاحتفاظ بالارتباط في الكتابة المزدوجة، يمكنك طلب المساعدة من دعم Microsoft لتغيير تكامل Power Platform لاستخدام بيئة Dataverse الموجودة كما هو موثق في المقطع السابق.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
