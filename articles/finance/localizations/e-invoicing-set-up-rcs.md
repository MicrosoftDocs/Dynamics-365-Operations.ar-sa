---
title: إعداد Regulatory configuration service (RCS)
description: يشرح هذا الموضوع كيفية إعداد Regulatory Configuration Service (RCS).
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 33aab6f0a482ce3d90a7e9828015a8e7bebb7827
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371498"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>إعداد Regulatory configuration service (RCS)

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية إعداد Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>تشغيل ميزات العولمة

1. سجل دخولك إلى حساب RCS.
2. حدد الإطار المتجانب **إدارة الميزات**.
3. في مساحة عمل **إدارة الميزات**، حدد **ميزات العولمة** في القائمة، ثم حدد **تمكين الآن**.

يجب أن يظهر تجانب مساحة عمل **ميزات العولمة** على لوحة معلومات RCS الرئيسية.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>إعداد المعلمات لتكامل RCS باستخدام الفوترة الإلكترونية

1. في مساحة عمل **ميزات العولمة**، في قسم **الإعدادات ذات الصلة**، حدد **معلمات التقارير الإلكترونية**.
2. في علامة التبويب **الفوترة الإلكترونية**، في حقل **عنوان URI لنقطة نهاية الخدمة**، أدخل نقطة نهاية الخدمة المناسبة لجغرافية Microsoft Azure، كما هو موضح في الجدول التالي.

    | منطقة Azure الجغرافية لمركز البيانات | عنوان URI لنقطة نهاية الخدمة |
    |----------------------------|----------------------|
    | الولايات المتحدة              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | أوروبا                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | المملكة المتحدة             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | آسيا                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | اليابان                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. تأكد من أنه تم تعيين حقل **معرف التطبيق** إلى **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. هذه القيمة هي قيمة ثابتة. تاكد من إدخال معرف فريد عمومي (GUID) فقط، وان القيمة التي لا تتضمن إيه رموز أخرى، مثل المسافات أو الفاصلات أو الفترات أو علامات الاقتباس.
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
