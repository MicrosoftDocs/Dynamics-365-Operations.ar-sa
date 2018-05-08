---
title: "إعداد انتقاء نظام المجموعة"
description: "يصف هذا الموضوع كيفية إعداد انتقاء نظام مجموعة وكيفية تطبيق تأكيد الصنف بانتقاء نظام المجموعة."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2ec0890963b2b01407acac8003453faf370894b4
ms.openlocfilehash: 1c23421ddfda8c5f6fa27a31831a00ead6094db9
ms.contentlocale: ar-sa
ms.lasthandoff: 04/11/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a>إعداد انتقاء نظام المجموعة

يصف هذا الموضوع كيفية تمكين العاملين من استخدام الأجهزة المحمولة الخاصة بهم لتجميع عمل الانتقاء في نظم مجموعات، حيث يمكنهم انتقاء الأصناف من موقع واحد لأوامر عمل متعددة في نفس الوقت. وهذا ما يسمى *انتقاء نظام المجموعة*.

## <a name="about-cluster-picking"></a>حول انتقاء نظام المجموعة

بعد إصدار أوامر العمل إلى المستودع، يمكن للعامل استخدام جهاز محمول لتعيين الأوامر لنظام مجموعة. ينظم نظام المجموعة عمل الانتقاء للعامل. عند تعيين أمر عمل لنظام مجموعة، يجب على العامل استخدام انتقاء نظام المجموعة لتنفيذ عمل الانتقاء للأمر. لا يمكن للعامل استخدام أساليب انتقاء أخرى. إذا تم تعيين أمر عمل لنظام مجموعة عن طريق الخطأ، فيجب على العامل إيقاف نظام المجموعة ثم إعادة إنشائه.

وإذا لزم الأمر، يمكن للعامل تمرير نظام مجموعة إلى عامل آخر. يؤدي هذا إلى تغيير حالة نظام المجموعة إلى تم الاجتياز. عند استخدام العامل لجهاز محمول للإشارة إلى اكتمال عمل الانتقاء والاستبعاد، فيجب تأكيد الشحنة أو حمل العمل في عميل Dynamics 365 for Finance and Operations.

## <a name="set-up-cluster-picking"></a>إعداد انتقاء نظام المجموعة

لتمكين انتقاء نظام المجموعة، يجب إعداد ما يلي:

-   **ملفات تعريف نظام المجموعة** – تحديد ما إذا كان سيتم تلقائيًا إنشاء معرفات نظام المجموعة، وعدد المواضع المستخدمة، ومتى يمكن إيقاف نظم المجموعات، وكيفية التسلسل والتحقق من عمل الانتقاء.

-   **قوالب العمل** – تحديد كيفية إنشاء عمل الانتقاء لانتقاء نظام المجموعة.

-   **توجيهات الموقع‬** – تحديد من أين يمكن انتقاء الأصناف وأين يمكن وضعها.

-   **‏‫أصناف قائمة الجهاز المحمول‬** – تكوين عنصر قائمة للجهاز المحمول لاستخدام العمل الموجود الذي يتم توجيهه بواسطة انتقاء نظام المجموعة. ثم يجب عليك إضافة عنصر قائمة إلى قائمة الجهاز المحمول حتى يتم عرضه على الأجهزة المحمولة.

-   **محددات إدارة المستودعات‬** – تحديد التسلسل الرقمي لاستخدامه إذا كنت تريد إنشاء معرفات لنظام المجموعات.

## <a name="set-up-a-cluster-profile"></a>إعداد ملف تعريف نظام المجموعة

لإعداد ملف تعريف نظام المجموعة، اتبع هذه الخطوات:

1.  انقر فوق **إدارة المستودعات**\>**الإعداد**\>**الجهاز المحمول**\>**ملفات تعريف نظام المجموعة**.

2.  انقر فوق **جديد** لإنشاء ملف تعريف جديد.

3.  انقر فوق **إنشاء نظام مجموعة**، وضمن **فرز نظام المجموعة**، انقر فوق **جديد** لإعداد معايير الفرز لنظام المجموعة. تتحكم معايير الفرز في الترتيب الذي سيقوم العامل على أساسه تنفيذ عمل الانتقاء. يمكنك إضافة أي عدد من المعايير حسب الضرورة.

4.  في حقل **رقم التسلسل**، قم بإدخال رقم لتحديد الترتيب الذي ستتم به معالجة معايير الفرز.

5.  في **اسم الحقل**، حدد الحقل الذي سيحدد الفرز. على سبيل المثال، إذا قمت بتحديد الحقل **WMSLocationId**، فسيتم تصنيف العمل حسب الموقع.

6.  في حقل **الفرز**، حدد أحد الخيارات التالية.

| **خيار**     | **الوصف**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **تصاعدي**  | يتم تعيين تسلسل عمل الانتقاء في ترتيب تصاعدي استنادًا إلى معايير الفرز. على سبيل المثال، إذا استخدمت الحقل **WMSLocationId** بمثابة معايير الفرز، وكانت معرفات الموقع الخاصة بك هي 1 و2 و3 و4، فستقوم بالانتقاء من الموقع 4 أولاً. |
| **تنازلي** | يتم تعيين تسلسل عمل الانتقاء في ترتيب تنازلي استنادًا إلى معايير الفرز. على سبيل المثال، إذا استخدمت الحقل **WMSLocationId** بمثابة معايير الفرز، وكانت معرفات الموقع الخاصة بك هي 1 و2 و3 و4، فستقوم بالانتقاء من الموقع 1 أولاً. |

## <a name="item-confirmation"></a>تأكيد الأصناف

عند تطبيق انتقاء نظام المجموعة، يُعد تأكيد الصنف أمرًا هامًا للتحقق من الأصناف التي تمت إضافتها إلى نظم المجموعات. يمكنك التحقق من الأصناف في انتقاء نظام المجموعة خلال عملية انتقاء نظام المجموعة. يستند الإعداد على إعداد الرمز الشريطي للمنتج.

### <a name="set-up-item-verification-with-cluster-picking"></a>إعداد التحقق من الصنف مع انتقاء نظام مجموعة

1.  في عنصر قائمة جهاز محمول، قم بفتح نموذج الإعداد من تأكيد العمل: **إدارة المستودعات** \> **إدارة المستودعات** \> **الإعداد** \> **جهاز محمول** \> **عناصر قائمة الجهاز المحمول**.

2.  من عنصر قائمة الجهاز المحمول، قم بفتح **إعداد تأكيد العمل**. يسمح لك الخيار **تأكيد المنتج** بالتحقق من كل جزء من المخزون من خلال الهاتف المحمول عند مسحه ضوئيًا.
