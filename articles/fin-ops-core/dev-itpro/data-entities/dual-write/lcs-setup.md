---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: توضح هذه المقالة كيفية إعداد اتصال ثنائي الكتابة من Microsoft Dynamics Lifecycle Services‏ (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a002bae22044ea10be30340a87a191305f6c6b92
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111959"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>إعداد الكتابة المزدوجة من Lifecycle Services

[!include [banner](../../includes/banner.md)]



توضح هذه المقالة كيفية تمكين الكتابة المزدوجة من Microsoft Dynamics Lifecycle Services‏ (LCS).

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب على العملاء إكمال تكامل Power Platform كما هو موضح في المواضيع التالية:

- إذا كنت لا تستخدم Microsoft Power Platform حتى الآن وتريد توسيع بيئات Finance and Operations الخاصة بك عن طريق إضافة إمكانات النظام الأساسي، فراجع [تكامل Power Platform - التمكين أثناء نشر البيئة](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- إذا كان لديك بيئتا Dataverse وPower Platform بالفعل، وتريد توصيلهما ببيئات Finance and Operations، فراجع [تكامل Power Platform - التمكين بعد نشر البيئة](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>إعداد الكتابة المزدوجة لبيئات Dataverse جديدة أو موجودة

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

8. عند اكتمال الارتباط، يتم عرض ارتباط تشعبي. استخدم الارتباط لتسجيل الدخول إلى منطقة إدارة الكتابة المزدوجة في بيئة التمويل والعمليات. ومن هناك، يمكنك إعداد تعيينات الكيانات.

## <a name="linking-mismatch"></a>ربط عدم التطابق

من الممكن أن تكون بيئة الكتابة المزدوجة الخاصة بك مرتبطة بمثيل Dataverse بينما لم يتم إعداد LCS لتكامل Power Platform. يمكن أن يتسبب عدم تطابق الارتباط هذا في حدوث سلوك غير متوقع. من المستحسن أن تتطابق تفاصيل بيئة LCS مع ما تتصل به في الكتابة المزدوجة بحيث يمكن استخدام نفس الاتصال بواسطة أحداث العمل والجداول الافتراضية والوظائف الإضافية.

إذا كانت بيئتك بها عدم تطابق في الارتباط، يعرض LCS تحذيرًا يشبه المثال التالي في صفحة تفاصيل البيئة الخاصة بك: "اكتشفت Microsoft أن بيئتك مرتبطة عبر الكتابة المزدوجة إلى وجهة مختلفة عن تلك المحددة في تكامل Power Platform، وهو أمر غير موصى به".

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="ارتباط تكامل Power Platform غير متطابق.":::

إذا تلقيت هذا التحذير، فجرب أحد الحلول التالية:

- إذا لم يتم إعداد بيئة LCS الخاصة بك من أجل تكامل Power Platform، فيمكنك الاتصال بمثيل Dataverse، الذي تم تكوينه في الكتابة المزدوجة باتباع التعليمات الواردة في هذه المقالة.
- إذا تم إعداد بيئة LCS بالفعل لتكامل Power Platform، فيجب إلغاء ربط الكتابة المزدوجة وإعادة توصيلها بالبيئة المحددة بواسطة LCS باستخدام [السيناريو: إعادة تعيين الارتباط أو تغييره](relink-environments.md#scenario-reset-or-change-linking).

في الماضي، كان خيار تذكرة الدعم اليدوي متاحًا، ولكن كان ذلك قبل وجود الخيار 1 أعلاه.  لم تعد Microsoft تدعم طلبات إعادة الربط اليدوية عبر تذاكر الدعم.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

