---
title: المواعيد النهائية لإدخال الأوامر
description: توفر هذه المقالة معلومات حول المواعيد النهائية لإدخال أمر. الموعد نهائي لإدخال أمر هو الانقطاع الذي يحدد ما إذا كان يتم التعامل مع طلب عميل (وتنفيذه) كما لو تم تلقيه في اليوم الحالي أو في اليوم التالي.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable, MCRAutoTaxRules
audience: Application User
ms.reviewer: kamaybac
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71748cb05346f7a31f51baebb86b9accc11c8478
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580518"
---
# <a name="order-entry-deadlines"></a>المواعيد النهائية لإدخال الأوامر

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات حول المواعيد النهائية لإدخال أمر. الموعد نهائي لإدخال أمر هو الانقطاع الذي يحدد ما إذا كان يتم التعامل مع طلب عميل (وتنفيذه) كما لو تم تلقيه في اليوم الحالي أو في اليوم التالي.

في العديد من الشركات، يتم التعامل مع أوامر المبيعات فقط التي تم استلامها قبل وقت محدد من اليوم على أنه قد تم استلامها في هذا اليوم. ويتم التعامل مع أي أوامر تم تلقيها بعد ذلك الوقت كما لو أنه تم تلقيها في يوم العمل التالي. ويُعرف وقت التوقف للأوامر هذا بالموعد النهائي لإدخال الأمر.  

يتم استخدام المواعيد النهائية لإدخال الأوامر كإدخال لأمر متفق عليه. ولذلك، فهي تساعد في إدارة توقعات العملاء بشأن عمليات تسليم الأوامر. على سبيل المثال، يمكن للعملاء مشاهدة أنه إذا كانوا يقدمون أمرًا لك قبل وقت محدد، فستلتزم بشحن البضائع في نفس اليوم. ‏‫ومع ذلك، إذا لم يكن لديهم هذا الموعد النهائي، فإنهم يتوقعون الشحنة فقط في يوم العمل التالي. وتقوم بتعيين المواعيد النهائية لإدخال الأمر على أساس قدرات المستودع والجداول الزمنية لشركة الشحن.‬  

وفي صفحة **المواعيد النهائية لإدخال الأوامر‬**، تقوم بإعداد أوقات المواعيد النهائية لإدخال الأوامر لجميع أيام الأسبوع. وإذا تم استلام الأوامر بعد الأوقات المحددةن فإنه يتم التعامل معها كما لو أنه تم تلقيها في اليوم التالي. وبشكل افتراضي، يتم ضبط هذه الأوقات على 23:59 (أي قبل دقيقة واحدة من منتصف الليل الذي يعبر عن انتهاء هذا اليوم). يمكن تغيير الأوقات الافتراضية حتى تتزامن مع أوقات المواعيد النهائية لعمليات الشحن أو الاستلام الفعلية.  

يمكنك تحديد المواعيد النهائية لإدخال الأوامر لمجموعة معينة من العملاء. على سبيل المثال، قد تحتاج إلى مجموعة محددة من العملاء لترتيب المواعيد النهائية لإدخال الأوامر أحدث من تلك الخاصة بالعملاء الآخرين. وفي هذه الحالة، يمكنك أولاً تحديد مجموعات المواعيد النهائية لإدخال الأوامر في صفحة **مجموعات المواعيد النهائية لإدخال الأوامر**. وتقوم فيما بعد بتعيين المجموعات إلى العملاء في صفحة **العملاء**.  

إذا كانت الشركة تتكون من عدة مواقع، فإنه يمكن إعداد المواعيد النهائية لإدخال الأوامر لكل موقع. إذا كانت المواقع تقع في مناطق زمنية مختلفة، فإن المواعيد النهائية لإدخال الأوامر يتم إعدادها في المنطقة الزمنية لكل موقع. وعلى الرغم من ذلك، فإنه عند العمل مع أوامر المبيعات وعروض أسعار المبيعات، فإن الموعد النهائي لإدخال الأوامر يتحول إلى المنطقة الزمنية في صفحة **مواعيد الشحن والاستلام المتاحة**.  

وفي صفحة **تنشيط مجموعات المواعيد النهائية لإدخال الأوامر**، يمكنك تحديد مجموعات المواقع ومجموعات المواعيد النهائية لإدخال الأوامر المسموح بها.

## <a name="example-order-entry-deadline"></a>مثال: الموعد النهائي لإدخال الأمر
تم تعيين الموعد النهائي لإدخال الأمر في أيام الثلاثاء إلى 16:00. وفي يوم ثلاثاء معين، في الساعة 17:00، تحاول تعيين التاريخ الحالي كتاريخ للشحن. ‏‫(لاحظ أنه لا توجد مهلة زمنية لهذا المثال).‬ إذا تم تحديد خانة الاختيار **التحكم في تاريخ التسليم**، تتلقى تحذيرًا ينص على أن التاريخ غير صحيح. ويظهر هذا التحذير في صفحة **تواريخ الشحن والاستلام المتاحة**، حيث يمكنك تحديد تواريخ بديلة.

## <a name="example-different-order-entry-deadlines-per-site"></a>مثال: المواعيد النهائية المختلف لإدخال الأوامر لكل موقع
تتألف شركتك من موقعين. توجد المواقع في مناطق زمنية مختلفة، كما هو موضح في الجدول التالي.

| الموقع أ                      | الموقع ب                      |
|-----------------------------|-----------------------------|
| كاليفورنيا                  | فلوريدا                     |
| PST (التوقيت الرسمي الباسيفيكي) | EST (التوقيت الرسمي الشرقي) |

تم تحديد المواعيد النهائية لإدخال الأوامر التالية بواسطة الموقعين أ وب.

| يوم من الأسبوع             | أ: المواعيد النهائية لإدخال الأوامر (PST) | ب: المواعيد النهائية لإدخال الأوامر (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| الاثنين                      | 13:00                          | 00:14                          |
| الثلاثاء                     | 13:00                          | 00:14                          |
| الأربعاء                   | 13:00                          | 00:14                          |
| الخميس                    | 13:00                          | 00:14                          |
| الجمعة                      | 13:00                          | 00:14                          |

أنت معالج الأمر وتوجد في يوتاه التي تتبع المنطقة الزمنية MST (التوقيت الجبلي الرسمي). إن هذا يعني أنه طالما قمت بإدخال الأوامر في الموقع أ قبل الساعة 14:00 بتوقيت MST وفي الموقع ب قبل الساعة 12:00 بتوقيت MST، فإنه يتم بذلك تلبية المواعيد النهائية لإدخال الأوامر لكلا الموقعين.  

يوضح الجدول التالي كيفية تحويل المواعيد النهائية لإدخال الأوامر للموقعين أ وب إلى التوقيت MST.

| الموقع أ: PST         | الموقع أ: MST        | الموقع ب: EST           | الموقع ب: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 00:14              | 00:14                 | 12:00              |

**ملاحظة:** إذا كان تعديل التوقيت الصيفي قيد التفعيل، فإنه يتم تعديل المواعيد النهائية لإدخال الأوامر وفقًا لذلك.

## <a name="example-same-order-entry-deadline-per-site"></a>مثال: الموعد النهائي نفسه لإدخال الأوامر لكل موقع
تتألف شركتك من موقعين. توجد المواقع في مناطق زمنية مختلفة، كما هو موضح في الجدول التالي.

| الموقع أ                      | الموقع ب                      |
|-----------------------------|-----------------------------|
| كاليفورنيا                  | فلوريدا                     |
| PST (التوقيت الرسمي الباسيفيكي) | EST (التوقيت الرسمي الشرقي) |

تم تحديد المواعيد النهائية لإدخال الأوامر التالية بواسطة الموقعين أ وب.

| يوم من الأسبوع | PST وEST |
|-----------------|-------------|
| الاثنين          | 13:00       |
| الثلاثاء         | 13:00       |
| الأربعاء       | 13:00       |
| الخميس        | 13:00       |
| الجمعة          | 13:00       |

أنت معالج الأمر وتوجد في يوتاه التي تتبع المنطقة الزمنية MST (التوقيت الجبلي الرسمي). إن هذا يعني أنه طالما قمت بإدخال الأوامر في الموقع أ قبل الساعة 14:00 بتوقيت MST وفي الموقع ب قبل الساعة 11:00 بتوقيت MST، فإنه يتم بذلك تلبية المواعيد النهائية لإدخال الأوامر لكلا الموقعين. 

يوضح الجدول التالي كيفية تحويل المواعيد النهائية لإدخال الأوامر للموقعين أ وب إلى التوقيت MST.

| الموقع أ: PST         | الموقع أ: MST        | الموقع ب: EST           | الموقع ب: MST        |
|---------------------|--------------------|-----------------------|--------------------|
| 13:00               | 00:14              | 13:00                 | 11:00              |

**ملاحظة:** إذا كان تعديل التوقيت الصيفي قيد التفعيل، فإنه يتم تعديل المواعيد النهائية لإدخال الأوامر وفقًا لذلك.

## <a name="additional-resources"></a>الموارد الإضافية

[جداول التسليم](delivery-schedules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]