---
title: إعداد Regulatory configuration service (RCS)
description: تشرح هذه المقالة كيفية إعداد Regulatory Configuration Service‏ (RCS).
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710771"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>إعداد Regulatory configuration service (RCS)

[!include [banner](../includes/banner.md)]

تشرح هذه المقالة كيفية إعداد Regulatory Configuration Service‏ (RCS).

## <a name="turn-on-globalization-features"></a>تشغيل ميزات العولمة

1. سجل دخولك إلى حساب RCS.
2. حدد الإطار المتجانب **إدارة الميزات**.
3. في مساحة عمل **إدارة الميزات**، حدد **ميزات العولمة** في القائمة، ثم حدد **تمكين الآن**.

يجب أن يظهر تجانب مساحة عمل **ميزات العولمة** على لوحة معلومات RCS الرئيسية.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>إعداد المعلمات لتكامل RCS باستخدام الفوترة الإلكترونية

1. في مساحة عمل **ميزات العولمة**، في قسم **الإعدادات ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.
2. في المرة الأولى التي تقوم فيها بإعداد المعلمات، ستتم مطالبتك بالاتصال بـ Life Cycle Services (LCS). حدد **انقر هنا للاتصال بـ Lifecycle Services**، وبعد إنشاء الاتصال، حدد **موافق**.

    > [!IMPORTANT]
    > في البلدان أو المناطق التي يتم فيها فرض إقامة البيانات، وإذا تم توفير RCS في منطقة مختلفة حيث يتم توفير LCS، فقد تتلقى رسالة خطأ الاتصال التالية في RCS: "لم يتم العثور على مورد HTTP يطابق URI للطلب". حدد **موافق**. قد تتلقى رسالة خطأ أخرى في RCS: "فشل إنشاء الرمز المميز للمستخدم لـ Dynamics Lifecycle services نيابةً عن المستخدم (). يُرجى الاتصال بمسؤول النظام".
    >  
    > يحدث ذلك لأن LCS هي خدمة عالمية ويتم توفيرها في منطقة الولايات المتحدة. بسبب سياسة إقامة البيانات، يتعذر على RCS من منطقتك الحالية الاتصال بـ LCS. في ظل هذه الظروف، هناك حلان محتملان:
    > - احذف RCS من منطقتك الحالية وأعد إنشائه في منطقة الولايات المتحدة.
    > - تجاهل الأخطاء وتابع إعداد الفواتير الإلكترونية. لا تؤثر هذه الأخطاء على وظيفة الفوترة الإلكترونية.

3. في علامة التبويب **الفوترة الإلكترونية**، في حقل **عنوان URI لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لجغرافية Microsoft Azure، كما هو موضح في الجدول التالي.

    | منطقة Azure الجغرافية لمركز البيانات | عنوان URI لنقطة نهاية الخدمة |
    |----------------------------|----------------------|
    | الولايات المتحدة              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | أوروبا                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | المملكة المتحدة             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | آسيا                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | اليابان                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | سويسرا                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | البرازيل                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | الإمارات العربية المتحدة       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | أستراليا                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | كندا                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | فرنسا                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | الهند                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | النرويج                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | جنوب أفريقيا               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. راجع الحقل **معرف التطبيق**، وأدخل القيمة الثابتة **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. تاكد من إدخال معرف فريد عمومي (GUID) فقط، وان القيمة التي لا تتضمن إيه رموز أخرى، مثل المسافات أو الفاصلات أو الفترات أو علامات الاقتباس.
4. في حقل **معرف بيئة LCS**، أدخل معرف بيئة Microsoft Dynamics ‏Lifecycle Services ‏(LCS). هذه القيمة هي المرجع إلى بيئة Finance أو Supply Chain Management التي ستستخدمها مع خدمة الفوترة الإلكترونية. للحصول علي المعرف الخاص بك، قم بتسجيل الدخول إلى [LCS](https://lcs.dynamics.com/)، ثم افتح مشروعك، ثم في علامة التبويب **إدارة البيئة**، في قسم **تفاصيل البيئة**، ابحث في حقل **معرف البيئة**.

    > [!IMPORTANT]
    > إذا تم تثبيت الوظيفة الإضافية للفواتير الإلكترونية في العديد من بيئات Finance أو Supply Chain Management في LCS، فاستخدم دائمًا معرّف البيئة لأحدث بيئة تم تثبيتها. إذا قررت تثبيت الوظيفة الإضافية في بيئة جديدة بعد إعداد وظيفة الفواتير الإلكترونية والعمل معها، فقم بتحديث **معرف بيئة LCS** في RCS إلى أحدث قيمة.

5. حدد **حفظ** ثم قم بإغلاق الصفحة.

## <a name="configuration-providers"></a>موفرو التكوين

يمكنك استخدام موفري التكوين للتمييز بين مالكي تكوينات إعداد التقارير الإلكترونية (ER) المستخدمة في عمليات الفوترة الإلكترونية وميزات عولمة الملاك. بالنسبة لجميع ميزات العولمة التي توفرها Microsoft ويتم نشرها في المستودع العمومي، يتم تعيين موفر التكوين على **Microsoft** (`http://microsoft.com`).

يمكنك فقط ضبط تكوينات التقارير الإلكترونية وميزات العولمة التي تنتمي إلى موفر التكوين النشط. يمكنك استخدام هذه التكوينات والميزات كقوالب لإنشاء التكوينات والميزات التي تنتمي إلى موفر التكوين النشط، بحيث يمكنك تعديلها.

أولاً، قم بإنشاء موفري التكوين. ثم قم بتعيين أحدهم كنشط. لا يمكنك تعيين موفر تكوين **Microsoft** على أنه نشط.

### <a name="create-a-configuration-provider"></a>إنشاء موفر تكوين

1. في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **الارتباطات‬ ذات الصلة**، حدد **موفرو التكوين**.
2. حدد **جديد**.
3. في حقل **الاسم**، أدخل اسمًا فريدًا لموفر التكوين.
4. في حقل **عنوان الإنترنت**، أدخل عنوان URL لموفر التكوين.
5. حدد **حفظ** ثم قم بإغلاق الصفحة.

### <a name="select-a-configuration-provider-as-active"></a>تحديد موفر تكوين كنشط

1. في قائمة موفري التكوين، حدد موفر التكوين الذي تريد تعيينه كنشط.
2. حدد **تعيين كنشط**.

## <a name="import-er-configurations-from-the-global-repository"></a>استيراد تكوينات التقارير الإلكترونية من المستودع العمومي

1. في مساحة عمل **إعداد التقارير الإلكترونية**، في قسم **الارتباطات‬ ذات الصلة**، حدد **موفرو التكوين**.
2. في قائمة موفري التكوين، حدد **Microsoft**، ثم حدد **المستودعات**.
3. حدد **عمومي**، ثم في جزء الإجراءات، حدد **فتح**.
4. استيراد نماذج ER التالية:

    - **نموذج سياق فاتورة العميل**
    - **نموذج الفاتورة**
    - **المستندات المالية** (للسيناريوهات البرازيلية، إذا تطلب الأمر ذلك)
    - **نموذج رسالة الاستجابة**

5. إذا لم يتم **تعيين نموذج الفاتورة** تلقائيًا، فقم باستيراده.
6. قم بإغلاق الصفحة.
