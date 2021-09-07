---
title: تكوين رؤية المخزون
description: يصف هذا الموضوع كيفية تكوين رؤية المخزون.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345023"
---
# <a name="inventory-visibility-configuration"></a>تكوين رؤية المخزون

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

يصف هذا الموضوع كيفية تكوين رؤية المخزون.

## <a name="introduction"></a><a name="introduction"></a>مقدمة

قبل البدء في العمل مع "رؤية المخزون"، يجب إكمال التكوين التالي كما هو موضح في هذا الموضوع:

- [تكوين مصدر البيانات](#data-source-configuration)
- [تكوين التقسيم](#partition-configuration)
- [تكوين التسلسل الهرمي لمؤشر المنتج](#index-configuration)
- [تكوين الحجز (اختياري)](#reservation-configuration)
- [نموذج التكوين الافتراضي](#default-configuration-sample)

> [!NOTE]
> يمكنك عرض تكوينات رؤية المخزون وتحريرها في [Microsoft Power Apps](./inventory-visibility-power-platform.md#configuration). بعد اكتمال التكوين، حدد **تحديث التكوين** في التطبيق.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>تكوين مصدر البيانات

يمثل مصدر البيانات النظام الذي تأتي منه بياناتك. وتشمل الأمثلة `fno` (وهو ما يعني تطبيقات Dynamics 365 Finance and Operations ) و`pos` (وهو ما يعني "نقطة البيع").

يتضمن تكوين مصدر البيانات الأجزاء التالية:

- البعد (تعيين البعد)
- القياس المادي
- القياس المحسوب

> [!NOTE]
> مصدر بيانات `fno` محجوز لـ Dynamics 365 Supply Chain Management.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>البعد (تعيين البعد)

الغرض من تكوين الأبعاد هو توحيد التكامل متعدد الأنظمة لترحيل الأحداث والاستعلامات، بناءً على مجموعات الأبعاد.

تدعم رؤية المخزون الأبعاد الأساسية العامة التالية.

| نوع البعد | البُعد الأساسي |
|---|---|
| منتج | `ColorId` |
| منتج | `SizeId` |
| منتج | `StyleId` |
| منتج | `ConfigId` |
| التعقب | `BatchId` |
| التعقب | `SerialId` |
|  الموق | `LocationId` |
|  الموق | `SiteId` |
| حالة المخزون | `StatusId` |
| خاص بالمستودع | `WMSLocationId` |
| خاص بالمستودع | `WMSPalletId` |
| خاص بالمستودع | `LicensePlateId` |
| غير ذلك | `VersionId` |
| المخزون (مخصص) | `InventDimension1` حتى `InventDimension12` |
| الرقم الداخلي | `ExtendedDimension1` حتى `ExtendedDimension8` |

> [!NOTE]
> أنواع الأبعاد المسردة في الجدول السابق هي للإشارة فقط. ليس عليك تعريفها في "رؤية المخزون".
>
> قد يتم حجز أبعاد المخزون (المخصصة) لـ Supply Chain Management. في هذه الحالة، يمكنك استخدام الأبعاد الموسعة بدلا من ذلك.

يمكن للأنظمة الخارجية الوصول إلى رؤية المخزون من خلال واجهات برمجة التطبيقات RESTful الخاصة بها. بالنسبة للتكامل، تتيح لك رؤية المخزون تكوين _مصدر البيانات الخارجي_ وتعيين من _الأبعاد الخارجية_ إلى _الأبعاد الأساسية_. فيما يلي مثال على جدول تعيين الأبعاد.

| البعد الخارجي | البُعد الأساسي |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

عن طريق تكوين تعيين البعد، يمكنك إرسال الأبعاد الخارجية مباشرة إلى "رؤية المخزون". ستقوم رؤية المخزون بعد ذلك بتحويل الأبعاد الخارجية تلقائيا إلى أبعاد أساسية.

### <a name="physical-measures"></a>القياسات المادية

تقوم المقاييس الفعلية بتعديل الكمية وتعكس حالة المخزون. يمكنك تحديد التدابير المادية الخاصة بك، استنادا إلى الاحتياجات الخاصة بك.

توفر رؤية المخزون قائمة بالمقاييس المادية الافتراضية المرتبطة بـ Supply Chain Management (مصدر بيانات `fno`). يقدم الجدول التالي مثالا للمقاييس المادية.

| اسم القياس المادي | الوصف |
|---|---|
| `NotSpecified` | غير محدد |
| `Arrived` | الوصول |
| `AvailOrdered` | متوفر ومطلوب |
| `AvailPhysical` | الفعلي المتاح |
| `Deducted` | مخفض |
| `OnOrder` | OnOrder |
| `Ordered` | مطلوبة |
| `PhysicalInvent` | المخزون الفعلي |
| `Picked` | المستلَم |
| `PostedQty` | الكمية التي تم ترحيلها |
| `QuotationIssue` | إصدار عرض الأسعار |
| `QuotationReceipt` | إيصال عرض الأسعار |
| `Received` | مستلَم‬ |
| `Registered` | مسجّل |
| `ReservOrdered` | الكمية المطلوبة المحجوزة |
| `ReservPhysical` | المحتجز الفعلي |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>القياسات المحسوبة

توفر المقاييس المحسوبة صيغة حساب مخصصة تتكون من مجموعة من التدابير المادية. تتيح لك هذه الوظيفة تحديد مجموعة من المقاييس المادية التي سيتم إضافتها، و/أو مجموعة من المقاييس المادية التي سيتم طرحها، لتشكيل القياس المخصص.

على سبيل المثال، لديك نتيجة الاستعلام التالية.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

يمكنك بعد ذلك تكوين مقياس محسوب يسمى `MyCustomAvailableforReservation`، كما هو موضح في الجدول التالي. وسيستهلك نظام الاستهلاك هذا التدبير المحسوب.

| نظام الاستهلاك | القياس المحسوب | مصدر البيانات | القياس المادي | نوع الحساب |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

عند استخدام صيغة الحساب هذه، ستتضمن نتيجة الاستعلام الجديدة القياس المخصص.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

إخراج `MyCustomAvailableforReservation`، بناءً على إعداد الحساب في القياسات المخصصة، هو 100 + 50 + 80 + 90 + 30 - 10 - 20 - 60 - 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>تكوين التقسيم

يتكون تكوين القسم من مجموعة من الأبعاد الأساسية. وهو يحدد نمط توزيع البيانات. تدعم عمليات البيانات في نفس القسم الأداء العالي ولا تكلف الكثير. لذلك، يمكن أن تساهم أنماط التقسيم الجيدة في فوائد كبيرة.

توفر رؤية المخزون تكوين القسم الافتراضي التالي.

| البُعد الأساسي | التدرج الهرمي |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> تكوين القسم الافتراضي هو للرجوع إليه فقط. ليس عليك تعريفها في "رؤية المخزون". حاليا، ترقية تكوين القسم غير مدعومة.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>تكوين التسلسل الهرمي لمؤشر المنتج

في معظم الأحيان، لن يكون الاستعلام الفعلي للمخزون فقط عند أعلى مستوى "إجمالي". بدلا من ذلك، قد ترغب أيضا في مشاهدة النتائج التي يتم تجميعها استنادا إلى أبعاد المخزون.

توفر رؤية المخزون المرونة من خلال السماح لك بإعداد _الفهارس_. تستند هذه الفهارس إلى بعد أو مجموعة أبعاد. يتكون الفهرس من *تعيين رقم*، و *بعد*، و *تدرج هرمي*، كما هو محدد في الجدول التالي.

| الاسم | الوصف |
|---|---|
| تعيين الرقم | سيتم تجميع الأبعاد التي تنتمي إلى نفس المجموعة (الفهرس) معًا، وسيتم تخصيص نفس الرقم المحدد لها. |
| البعد | الأبعاد الأساسية التي يتم تجميع نتيجة الاستعلام عليها. |
| التدرج الهرمي | يتم استخدام التدرج الهرمي لتحديد مجموعات الأبعاد المدعومة التي يمكن الاستعلام عنها. على سبيل المثال، يمكنك إعداد مجموعة أبعاد لها تسلسل هرمي لـ `(ColorId, SizeId, StyleId)`. في هذه الحالة، يدعم النظام الاستعلامات على تركيبات الأبعاد الأربعة. المجموعة الأولى فارغة، والثانية هي `(ColorId)`، والثالثة هي `(ColorId, SizeId)`، والرابعة هي `(ColorId, SizeId, StyleId)`. المجموعات الأخرى غير مدعومة. لمزيد من المعلومات، راجع المثال التالي. |

### <a name="example"></a>مثال

يقدم هذا القسم مثالا يوضح كيفية عمل التسلسل الهرمي.

لديك العناصر التالية في المخزون الخاص بك.

| الصنف | ColorId | SizeId | StyleId | الكمية |
|---|---|---|---|---|
| القميص | أسود | صغير | عريض | 1 |
| القميص | أسود | صغير | عادي | 2 |
| القميص | أسود | كبير | عريض | 3 |
| القميص | أسود | كبير | عادي | 4 |
| القميص | أحمر | صغير | عريض | 5 |
| القميص | أحمر | صغير | عادي | 6 |
| القميص | أحمر | كبير | عادي | 7 |

هنا هو الفهرس.

| تعيين الرقم | البعد | التدرج الهرمي |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

يتيح الفهرس الاستعلام عن المخزون الفعلي بالطرق التالية:

- `()` – مجمعة من قبل الجميع

    - قميص، 28

- `(ColorId)` – مجمعة بواسطة `ColorId`

    - قيمص، أسود، 10
    - قميص، أحمر، 18

- `(ColorId, SizeId)` – مجمعة حسب مزيج من `ColorId` و`SizeId`

    - قيمص، أسود، صغير، 3
    - قيمص، أسود، كبير، 7
    - قيمص، أحمر، صغير، 11
    - قيمص، أحمر، كبير، 7

- `(ColorId, SizeId, StyleId)` – مجمعة حسب مزيج من `ColorId`، و`SizeId`، و`StyleId`

    - قيمص، أسود، صغير، عريض، 1
    - قيمص، أسود، صغير، عادي، 2
    - قيمص، أسود، كبير، عريض، 3
    - قيمص، أسود، كبير، عادي، 4
    - قيمص، أحمر، صغير، عريض، 5
    - قيمص، أحمر، صغير، عادي، 6
    - قيمص، أحمر، كبير، عادي، 7

> [!NOTE]
> يجب عدم تعريف الأبعاد الأساسية التي تم تعريفها في تكوين القسم في تكوينات الفهرس.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>تكوين الحجز (اختياري)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

يلزم تكوين الحجز إذا كنت ترغب في استخدام ميزة الحجز الناعمة. يتكون التكوين من جزأين أساسيين:

- تعيين حجز مرن
- تدرج هرمي للحجز المرن

### <a name="soft-reservation-mapping"></a>تعيين حجز مرن

عند إجراء الحجز، قد ترغب في معرفة ما إذا كان المخزون الفعلي متاحا حاليا للحجز. يتم ربط التحقق من الصحة إلى مقياس محسوب يمثل صيغة حساب مجموعة من التدابير الفعلية.

على سبيل المثال، يستند مقياس الحجز إلى مقياس `SoftReservOrdered` الفعلي من مصدر بيانات `iv` (رؤية المخزون). في هذه الحالة، يمكنك إعداد المقياس المحسوب لـ `AvailableToReserve` لمصدر بيانات `iv` كما هو موضح هنا.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `AvailPhysical` |
| الجمع | `pos` | `Inbound` |
| الطرح | `pos` | `Outbound` |
| الطرح | `iv` | `SoftReservOrdered` |

بعد ذلك، قم بإعداد تعيين حجز بسيط لتوفير تعيين من مقياس حجز `SoftReservOrdered` للمقياس المحسوب لـ `AvailableToReserve`.

| مصدر بيانات القياسات الفعلية | القياس المادي | متاح لمصدر بيانات الحجز | متاح للقياس المحسوب للحجز |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

الآن، عند إجراء حجز على `SoftReservOrdered`، ستعثر رؤية المخزون تلقائيًا على `AvailableToReserve` وصيغة الحساب المرتبطة بها لإجراء التحقق من صحة الحجز.

على سبيل المثال، لديك المخزون الفعلي التالي في "رؤية المخزون".

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

في هذه الحالة، يتم تطبيق الحساب التالي:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

لذلك، إذا حاولت إجراء حجوزات على `iv.SoftReservOrdered`، وكانت الكمية أقل من أو تساوي `AvailableToReserve` (10)، يمكنك إجراء الحجز.

### <a name="soft-reservation-hierarchy"></a>تدرج هرمي للحجز المرن

يصف التسلسل الهرمي للحجز تسلسل الأبعاد التي يجب تحديدها عند إجراء الحجوزات. إنه يعمل بنفس الطريقة التي يعمل بها التسلسل الهرمي لفهرس المنتج للاستعلامات الفعلية.

التسلسل الهرمي للحجز مستقل عن التسلسل الهرمي لمؤشر المنتج. يتيح لك هذا الاستقلال تنفيذ إدارة الفئات حيث يمكن للمستخدمين تقسيم الأبعاد إلى تفاصيل لتحديد متطلبات إجراء حجوزات أكثر دقة.

فيما يلي مثال على التسلسل الهرمي للحجز المرن.

| البُعد الأساسي | التدرج الهرمي |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

في هذا المثال، يمكنك الحجز في تسلسلات الأبعاد التالية:

- `()` – لم يتم تحديد بعد.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

يجب أن يتبع تسلسل الأبعاد الصالح بدقة التسلسل الهرمي للحجز، البعد حسب البعد. على سبيل المثال، التسلسل الهرمي `(SiteId, LocationId, SizeId)` غير صالح، لأن `ColorId` مفقود.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>نموذج التكوين الافتراضي

أثناء مرحلة التهيئة الخاصة به، يقوم "رؤية المخزون" بإعداد تكوين افتراضي. يمكنك تعديل التكوين كما تريد.

### <a name="data-source-configuration"></a>تكوين مصدر البيانات

#### <a name="configuration-of-the-iv-data-source"></a>تكوين مصدر البيانات iv

يصف هذا القسم كيفية تكوين مصدر بيانات `iv`.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>القياسات الفعلية التي تم تكوينها لمصدر البيانات iv

يتم تكوين القياسات الفعلية التالية لمصدر بيانات `iv`:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>القياس المحسوب لـ OrderedTotal

يمكنك تكوين المقياس المحسوب لـ `OrderedTotal` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `Ordered` |
| الجمع | `fno` | `Arrived` |
| الجمع | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>القياس المحسوب المتاح

يمكنك تكوين المقياس المحسوب لـ `OnHand` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `PhysicalInvent` |
| الجمع | `iom` | `OnHand` |
| الجمع | `erp` | `Unrestricted` |
| الجمع | `erp` | `QualityInspection` |
| الجمع | `pos` | `PosInbound` |
| الطرح | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>القياس المحسوب لـ ReservedTotal

يمكنك تكوين المقياس المحسوب لـ `ReservedTotal` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `ReservPhysical` |
| الجمع | `fno` | `ReservOrdered` |
| الجمع | `iv` | `SoftReservPhysical` |
| الجمع | `iv` | `SoftReservOrdered` |
| الجمع | `iv` | `ReservPhysical` |
| الجمع | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>القياس المحسوب لـ SoftReserved

يمكنك تكوين المقياس المحسوب لـ `SoftReserved` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `iv` | `SoftReservPhysical` |
| الجمع | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>القياس المحسوب لـ HardReserved

يمكنك تكوين المقياس المحسوب لـ `HardReserved` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `ReservPhysical` |
| الجمع | `fno` | `ReservOrdered` |
| الجمع | `iv` | `ReservPhysical` |
| الجمع | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>القياس المحسوب لـ OpenOrder

يمكنك تكوين المقياس المحسوب لـ `OpenOrder` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `OnOrder` |
| الجمع | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>المقياس المحسوب لـ OnHandAvailable

يمكنك تكوين المقياس المحسوب لـ `OnHandAvailable` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `PhysicalInvent` |
| الجمع | `iom` | `OnHand` |
| الجمع | `erp` | `Unrestricted` |
| الجمع | `erp` | `QualityInspection` |
| الجمع | `pos` | `PosInbound` |
| الطرح | `fno` | `ReservPhysical` |
| الطرح | `iv` | `SoftReservPhysical` |
| الطرح | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>المقياس المحسوب لـ AvailableToReserve

يمكنك تكوين المقياس المحسوب لـ `AvailableToReserve` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `PhysicalInvent` |
| الجمع | `iom` | `OnHand` |
| الجمع | `erp` | `Unrestricted` |
| الجمع | `erp` | `QualityInspection` |
| الجمع | `pos` | `PosInbound` |
| الجمع | `fno` | `Ordered` |
| الجمع | `fno` | `Arrived` |
| الجمع | `iv` | `Ordered` |
| الطرح | `fno` | `ReservPhysical` |
| الطرح | `fno` | `ReservOrdered` |
| الطرح | `iv` | `SoftReservPhysical` |
| الطرح | `iv` | `SoftReservOrdered` |
| الطرح | `iv` | `ReservPhysical` |
| الطرح | `iv` | `ReservOrdered` |
| الطرح | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>المقياس المحسوب لـ InventorySupply

يمكنك تكوين المقياس المحسوب لـ `InventorySupply` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `Ordered` |
| الجمع | `fno` | `Arrived` |
| الجمع | `iv` | `Ordered` |
| الجمع | `fno` | `PhysicalInvent` |
| الجمع | `iom` | `OnHand` |
| الجمع | `erp` | `Unrestricted` |
| الجمع | `erp` | `QualityInspection` |
| الجمع | `pos` | `PosInbound` |
| الطرح | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>المقياس المحسوب لـ InventoryDemand

يمكنك تكوين المقياس المحسوب لـ `InventoryDemand` لمصدر بيانات `iv` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `OnOrder` |
| الجمع | `iom` | `OnOrder` |
| الجمع | `iv` | `SoftReservPhysical` |
| الجمع | `iv` | `SoftReservOrdered` |
| الجمع | `fno` | `ReservPhysical` |
| الجمع | `fno` | `ReservOrdered` |
| الجمع | `iv` | `ReservPhysical` |
| الجمع | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>تكوين مصدر بيانات fno

يصف هذا القسم كيفية تكوين مصدر بيانات `fno`.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>تعيينات الأبعاد لمصدر بيانات fno

يتم تكوين تعيينات الأبعاد المسردة في الجدول التالي لمصدر بيانات `fno`.

| البعد الخارجي | البُعد الأساسي |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>القياسات الفعلية التي تم تكوينها لمصدر بيانات fno

يتم تكوين القياسات الفعلية التالية لمصدر بيانات `fno`:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>تكوين مصدر بيانات pos

يصف هذا القسم كيفية تكوين مصدر بيانات `pos`.

##### <a name="physical-measures-for-the-pos-data-source"></a>القياسات الفعلية لمصدر بيانات pos

يتم تكوين القياسات الفعلية التالية لمصدر بيانات `pos`:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>المقياس المحسوب لـ AvailQuantity

يمكنك تكوين المقياس المحسوب لـ `AvailQuantity` لمصدر بيانات `pos` كما هو موضح في الجدول التالي.

| نوع الحساب | مصدر البيانات | القياس المادي |
|---|---|---|
| الجمع | `fno` | `AvailPhysical` |
| الجمع | `pos` | `PosInbound` |
| الطرح | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>تكوين مصدر بيانات iom

يتم تكوين القياسات الفعلية التالية لمصدر بيانات `iom` (إدارة الأمر الذكي):

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>تكوين مصدر بيانات erp

يتم تكوين القياسات الفعلية التالية لمصدر بيانات `erp` (تخطيط مورد المؤسسة):

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>تكوين التقسيم

يعرض الجدول التالي تكوين التقسيم الافتراضي.

| البُعد الأساسي | التدرج الهرمي |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>تكوين الفهرس

يعرض الجدول التالي تكوين الفهرس الافتراضي.

| تعيين الرقم | البعد | التدرج الهرمي |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>تكوين الحجز

يصف هذا القسم تكوين الحجز الافتراضي.

#### <a name="reservation-mapping"></a>تعيين الحجز

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

يعرض الجدول التالي تعيين الحجز الافتراضي.

| مصدر بيانات القياسات الفعلية | القياس المادي | متاح لمصدر بيانات الحجز | متاح للقياس المحسوب للحجز |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>التدرج الهرمي للحجز

يعرض الجدول التالي التدرج الهرمي للحجز الافتراضي.

| البُعد الأساسي | التدرج الهرمي |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
