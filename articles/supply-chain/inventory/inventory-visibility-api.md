---
title: واجهات API العامة لـ Inventory Visibility
description: يصف هذا المقال واجهات برمجة التطبيقات العامة التي يتم توفيرها بواسطة "رؤية المخزون".
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 82a43954db8b10554c449f3e8d32ba7e5d7c7f27
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719305"
---
# <a name="inventory-visibility-public-apis"></a>واجهات API العامة لـ Inventory Visibility

[!include [banner](../includes/banner.md)]


يصف هذا المقال واجهات برمجة التطبيقات العامة التي يتم توفيرها بواسطة "رؤية المخزون".

تقدم واجهة برمجة التطبيقات العامة لـ REST الخاصة بالوظيفة الإضافية لرؤية المخزون العديد من نقاط التكامل الخاصة. ويدعم أربعة أنواع من التفاعلات الرئيسية:

- ترحيل تغييرات المخزون الفعلية إلى الوظيفة الإضافية من نظام خارجي
- تعيين أو تجاوز كميات المخزون الفعلي في الوظيفة الإضافية من نظام خارجي
- ترحيل أحداث الحجز إلى الوظيفة الإضافية من نظام خارجي
- الاستعلام عن الكميات الفعلية الحالية من نظام خارجي

يسرد الجدول التالي واجهات برمجة التطبيقات المتوفرة حاليًا:

| المسار | الطريقة | الوصف |
|---|---|---|
| /api/environment/{environmentId}/onhand | ترحيل | [إنشاء حدث تغيير واحد مباشر](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | ترحيل | [إنشاء أحداث تغيير متعددة](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | ترحيل | [تعيين/تجاوز الكميات المتاحة](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | ترحيل | [إنشاء حدث حجز واحد](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | ترحيل | [إنشاء أحداث حجز متعددة](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | ترحيل | [حدث حجز واحد](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | ترحيل | [Reverse multiple reservation events](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | ترحيل | [إنشاء تغيير فعلي مجدول](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | ترحيل | [إنشاء تغييرات فعلية مجدولة](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | ترحيل | [الاستعلام باستخدام أسلوب الترحيل](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | إحضار | [الاستعلام باستخدام أسلوب الحصول](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | ترحيل | [الاستعلام الدقيق باستخدام أسلوب الترحيل](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation/allocate | ترحيل | [إنشاء حدث تخصيص واحد](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/unallocate | ترحيل | [إنشاء حدث إلغاء تخصيص واحد](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/reallocate | ترحيل | [إنشاء حدث إعادة تخصيص واحد](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/consume | ترحيل | [إنشاء حدث استهلاك واحد](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation/query | ترحيل | [نتيجة تخصيص استعلام](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> جزء {environmentId} من المسار هو معرف البيئة في Microsoft Dynamics Lifecycle Services (LCS).
> 
> يمكن لواجهة برمجة التطبيقات المجمعة إرجاع 512 سجلاً كحد أقصى لكل طلب.

قدمت Microsoft مجموعة طلبات *ساعي بريد* الجاهزة. يمكنك استيراد هذه المجموعة إلى برنامج *ساعي البريد* باستخدام الارتباط المشترك التالي: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>.

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>البحث عن نقطة النهاية وفقًا لبيئة Lifecycle Services الخاصة بك

يتم نشر الخدمة المصغرة الخاصة برؤية المخزون على Microsoft Azure Service Fabric، في مناطق جغرافية متعددة ومناطق متعددة. لا توجد حاليا نقطة نهاية مركزية يمكنها إعادة توجيه طلبك تلقائيا إلى الجغرافية والمنطقة المقابلة. لذلك، يجب إنشاء أجزاء من المعلومات في URL باستخدام النمط التالي:

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

يمكن العثور على اسم المنطقة القصير في بيئة Microsoft Dynamics Lifecycle Services (LCS). يسرد الجدول التالي المناطق المتوفرة حاليًا.

| منطقة Azure        | اسم المنطقة القصير |
| ------------------- | ----------------- |
| شرق أستراليا      | eau               |
| جنوب شرق أستراليا | seau              |
| وسط كندا      | cca               |
| شرق كندا         | eca               |
| شمال أوروبا        | neu               |
| غرب أوروبا         | weu               |
| شرق الولايات المتحدة             | eus               |
| غرب الولايات المتحدة             | wus               |
| جنوب المملكة المتحدة            | suk               |
| غرب المملكة المتحدة             | wuk               |
| شرق اليابان          | ejp               |
| غرب اليابان          | wjp               |
| جنوب البرازيل        | sbr               |
| وسط جنوب الولايات المتحدة    | scus              |

رقم الجزيرة هو المكان الذي يتم فيه نشر بيئة LCS على نسيج الخدمة. لا توجد حاليًا طريقة للحصول على هذه المعلومات من جانب المستخدم.

قامت Microsoft بإنشاء واجهة مستخدم (UI) في Power Apps بحيث يمكنك الحصول على نقطة النهاية الكاملة للخدمة المصغرة. للحصول على مزيد من المعلومات، راجع [البحث عن نقطة نهاية الخدمة](inventory-visibility-configuration.md#get-service-endpoint).

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>مصادقة

يتم استخدام رمز أمان النظام الأساسي لاستدعاء واجهة برمجة التطبيقات العامة لرؤية المخزون. لذلك، يجب إنشاء الرمز المميز _Azure Active Directory (Azure AD)_ باستخدام تطبيق Azure AD. يجب استخدام رمز Azure AD المميز للحصول على _رمز الوصول المميز_ من خدمة الأمان.

توفر Microsoft مجموعة الحصول على الرمز المميز *ساعي بريد* الجاهزة. يمكنك استيراد هذه المجموعة إلى برنامج *ساعي البريد* باستخدام الارتباط المشترك التالي: <https://www.getpostman.com/collections/496645018f96b3f0455e>.

للحصول على رمز خدمة الأمان، اتبع هذه الخطوات.

1. قم بتسجيل الدخول إلى مدخل Azure، واستخدمه للبحث عن قيم `clientId` و`clientSecret` لتطبيق Dynamics 365 Supply Chain Management الخاص بك.
1. إحضار Azure AD رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:

   - **عنوان URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
   - **الأسلوب:** `GET`
   - **محتوي النص الأساسي (بيانات النموذج):**

     | المفتاح           | قيمة                                            |
     | ------------- | -------------------------------------------------|
     | client_id     | ${aadAppId}                                      |
     | client_secret | ${aadAppSecret}                                  |
     | grant_type    | client_credentials                               |
     | النطاق         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2(افتراضية)    |

   يجب أن تتلقى رمز Azure AD المميز (`aadToken`) في الاستجابة. يجب أن تشبه المثال التالي.

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "access_token": "eyJ0eX...8WQ"
   }
   ```

1. قم بصياغة طلب JavaScript Object Notation ‏(JSON) يشبه المثال التالي.

   ```json
   {
       "grant_type": "client_credentials",
       "client_assertion_type": "aad_app",
       "client_assertion": "{Your_AADToken}",
       "scope": "https://inventoryservice.operations365.dynamics.com/.default",
       "context": "{$LCS_environment_id}",
       "context_type": "finops-env"
   }
   ```

   لاحظ النقاط التالية:

   - يجب أن تكون قيمة `client_assertion` رمز Azure AD المميز (`aadToken`) الذي استلمته في الخطوة السابقة.
   - قيمة `context` يجب أن تكون معرف البيئة حيث تريد توزيع الوظيفة الإضافية.
   - قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.

1. إحضار رمز مميز للوصول (`access_token`) عن طريق إرسال طلب HTTP بالخصائص التالية:

   - **عنوان URL:** `https://securityservice.operations365.dynamics.com/token`
   - **الأسلوب:** `POST`
   - **رأس HTTP:** تضمين إصدار API. (المفتاح هو `Api-Version`، والقيمة هي `1.0`.)
   - **محتوي النص الأساسي:** تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.

   يجب أن تتلقى رمز المميز للوصول (`access_token`) في الاستجابة. يجب عليك استخدام هذا الرمز المميز كرمز لحامله لاستدعاء واجهة برمجة تطبيقات رؤية المخزون. وفيما يلي مثال على ذلك.

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> عند استخدام مجموعة طلب *ساعي البريد* لاستدعاءات واجهات API العامة لرؤية المخزون، يجب إضافة رمز مميز للحامل إلى كل طلب. للحصول على الرمز المميز للحامل، حدد علامة التبويب **تخويل** ضمن عنوان URL للطلب، وحدد نوع **الرمز المميز للحامل**، وانسخ الرمز المميز للوصول الذي تم إحضاره في الخطوة الأخيرة. في الأقسام اللاحقة من هذا المقال، سيتم استخدام `$access_token` لتمثيل الرمز المميز الذي تم إحضاره في الخطوة الأخيرة.

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>إنشاء أحداث التغيير المتاحة

هناك نوعان من واجهات برمجة التطبيقات لإنشاء أحداث التغيير المتاحة:

- إنشاء سجل واحد: `/api/environment/{environmentId}/onhand`
- إنشاء سجلات متعددة: `/api/environment/{environmentId}/onhand/bulk`

يلخص الجدول التالي معنى كل حقل في نص JSON.

| معرف الحقل | Description |
|---|---|
| `id` | معرف فريد لحدث التغيير المحدد. إذا حدثت إعادة الإرسال بسبب فشل الخدمة ، فسيتم استخدام هذا المعرف لضمان عدم احتساب نفس الحدث مرتين في النظام. |
| `organizationId` | معرّف المؤسسة المرتبطة بالحدث. يتم تعيين هذه القيمة إلى مؤسسة أو معرّف منطقة البيانات في Supply Chain Management. |
| `productId` | معرف المنتج. |
| `quantities` | الكمية التي يجب تغيير الكمية المتوفرة بها. على سبيل المثال، إذا تمت إضافة 10 كتب جديدة إلى الرف، ستكون هذه القيمة `quantities:{ shelf:{ received: 10 }}`. إذا تمت إزالة ثلاثة كتب من الرف أو بيعها، ستكون هذه القيمة `quantities:{ shelf:{ sold: 3 }}`. |
| `dimensionDataSource` | مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام. إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد. يمكن أن تستخدم رؤية المخزون تكوين البعد لتعيين الأبعاد المخصصة إلى الأبعاد الافتراضية العامة. إذا لم يتم تحديد قيمة `dimensionDataSource`، يمكنك فقط استخدام [الأبعاد الأساسية](inventory-visibility-configuration.md#data-source-configuration-dimension) العامة في استعلاماتك. |
| `dimensions` | زوج قيمة مفتاح ديناميكي. يتم تعيين القيم لبعض الأبعاد في Supply Chain Management. ومع ذلك، يمكنك أيضا إضافة أبعاد مخصصة (على سبيل المثال، _المصدر_) للإشارة إلى ما إذا كان الحدث قادما من Supply Chain Management أو نظام خارجي. |

> [!NOTE]
> تنشئ معلمتا  `siteId` و`locationId` [تكوين التقسيم](inventory-visibility-configuration.md#partition-configuration). بالتالي، يجب تحديدها في الأبعاد عند إنشاء أحداث التغيير الفعلي أو تحديد الكميات الفعلية أو تجاوزها أو إنشاء أحداث حجز.

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>إنشاء حدث تغيير واحد متاح

تنشئ واجهة برمجة التطبيقات هذه حدثًا فرديًا للتغيير.

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

يظهر المثال التالي نموذج محتوى النص الأساسي. في هذه العينة، يمكنك نشر حدث تغيير لمنتج *القميص*. هذا الحدث من نظام نقاط البيع (POS)، وقد أعاد العميل قميصًا أحمر إلى متجرك. هذا الحدث سيزيد من كمية منتج *القميص* بمعدل 1.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

يظهر المثال التالي نموذج محتوى النص الأساسي دون `dimensionDataSource`. في هذه الحالة، فإن `dimensions` سيكون [الأبعاد الأساسية](inventory-visibility-configuration.md#data-source-configuration-dimension). إذا تم تعيين `dimensionDataSource`، فإن `dimensions` يمكن أن يكون إما أبعاد مصدر البيانات أو الأبعاد الأساسية.

```json
{
    "id": "123456",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>إنشاء أحداث تغيير متعددة

يمكن لواجهة برمجة التطبيقات هذه إنشاء سجلات متعددة في نفس الوقت. الاختلافات الوحيدة بين واجهة برمجة التطبيقات هذه و[واجهة برمجة تطبيقات الحدث الواحد](#create-one-onhand-change-event) هي قيم `Path` و`Body`. بالنسبة لواجهة برمجة التطبيقات هذه، يوفر `Body` مجموعة من السجلات. الحد الأقصى لعدد السجلات هو 512، مما يعني أن API المجمعة للتغييرات المتاحة يمكن أن تدعم ما يصل إلى 512 حدث تغيير في المرة الواحدة.

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

يظهر المثال التالي نموذج محتوى النص الأساسي.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "posSite1",
            "posLocationId": "posLocation1",
            "posMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "SCM_IV",
        "productId": "iv_postman_product_2",
        "dimensions": {
            "siteId": "iv_postman_site",
            "locationId": "iv_postman_location",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>تعيين/تجاوز الكميات المتاحة

تتجاوز _تعيين واجهة برمجة تطبيقات_ المتاحة البيانات الحالية للمنتج المحدد.

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

يظهر المثال التالي نموذج محتوى النص الأساسي. يختلف سلوك واجهة برمجة التطبيقات هذه عن سلوك واجهات برمجة التطبيقات الموضحة في قسم [إنشاء أحداث تغيير متاحة](#create-onhand-change-event) لاحقًا في هذا المقال. في هذ النموذج، سيتم تعيين كمية منتج *القميص* إلى 1.

```json
[
    {
        "id": "123456",
        "organizationId": "SCM_IV",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "posSiteId": "iv_postman_site",
            "posLocationId": "iv_postman_location",
            "posMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>إنشاء أحداث الحجز

لاستخدام واجهة برمجة تطبيقات *الحجز* ، يجب عليك تشغيل ميزة الحجز وإكمال تكوين الحجز. لمزيد من المعلومات، راجع [تكوين الحجز (اختياري)](inventory-visibility-configuration.md#reservation-configuration).

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>إنشاء حدث حجز واحد

يمكن إجراء الحجز مقابل إعدادات مصدر بيانات مختلفة. لتكوين هذا النوع من الحجز ، حدد أولا مصدر البيانات في معلمة `dimensionDataSource`. ثم، في معلمة `dimensions`، حدد الأبعاد وفقاً لإعدادات البعد في مصدر البيانات الهدف.

عند استدعاء API للحجز، يمكنك التحكم في التحقق من صحة الحجز عن طريق تحديد المعلمة المنطقية `ifCheckAvailForReserv` في النص الأساسي للطلب. تعني القيمة `True` أن التحقق من الصحة مطلوب، بينما تعني القيمة `False` أن التحقق من الصحة غير مطلوب. القيمة الافتراضية هي `True`.

إذا كنت ترغب في إلغاء حجز أو إبطال حجز كميات مخزون محددة، فقم بتعيين الكمية على قيمة سالبة، وقم بتعيين معلمة `ifCheckAvailForReserv` إلى `False` لتخطي عملية التحقق من الصحة. يوجد أيضا أونريسيرفي مخصص لواجهه برمجه التطبيقات (API) للقيام بنفس الاجراء. الفرق فقط هو الطريقة التي يتم بها استدعاء APIs. من الأسهل عكس حدث حجز معين باستخدام `reservationId` بواسطة *غير متحفظ* واجهة برمجة التطبيقات. لمزيد من المعلومات ، راجع [_مقطع حدث_](#reverse-reservation-events) حجز واحد أونريسيرفي.

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

يظهر المثال التالي نموذج محتوى النص الأساسي.

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

يوضح المثال التالي استجابه ناجحه.

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>إنشاء أحداث حجز متعددة

واجهة برمجة التطبيقات هذه هي إصدار مجمع من [واجهة برمجة تطبيقات الحدث الواحد](#create-reservation-events).

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>أحداث الحجز العكسي

ال *غير احتياطي* واجهة برمجة التطبيقات بمثابة عملية عكسية ل [*الحجز*](#create-reservation-events) الأحداث. ويوفر طريقه للغاء حدث حجز محدد بواسطة `reservationId` أو لتقليل كميه الحجز.

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>عكس حدث حجز واحد

وعند إنشاء عمليه حجز ، `reservationId` سيتم تضمينها في نص الاستجابة. ويجب عليك توفير نفسه `reservationId` للغاء الحجز ، وتضمين نفس `organizationId` واستخدام `dimensions` استدعاء API للحجز. وأخيرا ، قم بتحديد `OffsetQty` القيمة التي تمثل عدد الأصناف التي سيتم تحريرها من عمليه الحجز السابقة. يمكن ان يتم عكس الحجز بالبالكامل أو جزئيا بناء علي المحدد `OffsetQty`. علي سبيل المثال ، إذا *تم حجز الوحدات 100* الخاصة بالأصناف ، يمكنك تحديد `OffsetQty: 10` لأونريسيرفي *10* من المبلغ المحجوز المبدئي.

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

يُظهر الكود التالي مثالاً لمحتوى الجسم.

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

يوضح الكود التالي مثالاً لهيئة استجابة ناجحة.

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> في جسد الاستجابة ، متى `OffsetQty` أقل من أو يساوي كمية الحجز, `processingStatus` سيكون "*ناجح*" و `totalInvalidOffsetQtyByReservId` سيكون *0*.
>
> لو `OffsetQty` أكبر من المبلغ المحجوز, `processingStatus` سيكون "*partialSuccess*" و `totalInvalidOffsetQtyByReservId` سيكون الفرق بين `OffsetQty` والمبلغ المحجوز.
>
>على سبيل المثال ، إذا كان الحجز يحتوي على كمية *10*, و `OffsetQty` لديها قيمة *12*, `totalInvalidOffsetQtyByReservId` سيكون *2*.

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>عكس أحداث الحجز المتعددة

واجهة برمجة التطبيقات هذه هي إصدار مجمع من [واجهة برمجة تطبيقات الحدث الواحد](#reverse-one-reservation-event).

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [      
        {
            id: string,
            organizationId: string,
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>الاستعلام المتاح

استخدم واجهة برمجة تطبيقات *الاستعلام المتاح* لجلب بيانات المخزون الحالية الفعلية لمنتجاتك. تدعم واجهه برمجه التطبيقات حاليا الاستعلام حتى 5000 صنفا فرديا حسب قيمة `productID`. يمكن أيضًا تحديد قيم `siteID` و`locationID` المتعددة في كل استعلام. يتم تعريف الحد الأقصى بواسطة المعادلة التالية:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*.

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>الاستعلام باستخدام أسلوب الترحيل

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

في الجزء الأساسي من هذا الطلب، ما يزال `dimensionDataSource` معلمة اختيارية. وإذا لم يتم تعيينه، فسوف تتم معاملة `filters` كـ *أبعاد أساسية*. توجد أربعة حقول مطلوبه لـ `filters`: `organizationId`، و`productId`، و`siteId`، و`locationId`.

- يجب أن يحتوي `organizationId` قيمة واحدة فقط ، لكنها لا تزال مجموعة.
- `productId` يمكن أن تحتوي على قيمة واحدة أو أكثر.. إذا كان فارغًا، فسيتم إرجاع كافة المنتجات.
- يتم استخدام `siteId` و`locationId` للتقسيم في رؤية المخزون. يمكنك تحديد أكثر من قيمة `siteId` و`locationId` واحدة في طلب *الاستعلام المتاح‬*. في الإصدار الحالي، يجب تحديد قيم لكل من `siteId` و`locationId`.

نقترح عليك استخدام `groupByValues` المعلمة لمتابعة التكوين الخاص بك للفهرسة. لمزيد من المعلومات، راجع [تكوين التدرج الهرمي لفهارس المنتجات](./inventory-visibility-configuration.md#index-configuration).

تتحكم المعلمة `returnNegative` فيما إذا كانت النتائج تحتوي على إدخالات سالبة أم لا.

> [!NOTE]
> إذا قمت بتمكين الميزتين جدولة التغييرات الفعلية والمتاحة للتعهد (ATP)، فيمكن أن يتضمن استعلامك أيضًا المعلمة المنطقية `QueryATP`، والتي تتحكم في ما إذا كانت نتائج الاستعلام تتضمن معلومات ATP أم لا. لمزيد من المعلومات والأمثلة، راجع [جداول التغيير الفعلي لرؤية المخزون والمتوفر حسب التعهد](inventory-visibility-available-to-promise.md).

يظهر المثال التالي نموذج محتوى النص الأساسي.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

يوضح المثال التالي كيفية الاستعلام عن جميع المنتجات في موقع وموقع معين.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "siteId": ["iv_postman_site"],
        "locationId": ["iv_postman_location"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>الاستعلام باستخدام أسلوب الحصول

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

هذا نموذج لعنوان URL للحصول. طلب الحصول هذا مماثل تمامًا لعينة المشاركة التي تم توفيرها مسبقًا.

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>الاستعلام الدقيق باستخدام أسلوب الترحيل

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

في الجزء الأساسي من هذا الطلب، تُعد المعلمة `dimensionDataSource` معلمة اختيارية. إذا لم يتم تعيينه، فسوف تتم معاملة `dimensions` في `filters` بصفتها *أبعاد أساسية*. توجد أربعة حقول مطلوبه لـ `filters`: `organizationId`، و`productId`، و`dimensions`، و`values`.

- يجب أن يحتوي `organizationId` قيمة واحدة فقط ، لكنها لا تزال مجموعة.
- `productId` يمكن أن تحتوي على قيمة واحدة أو أكثر.. إذا كان فارغًا، فسيتم إرجاع كافة المنتجات.
- في المصفوفة `dimensions`، مطلوب `siteId` و`locationId` ولكن يمكن أن يظهر مع العناصر الأخرى بأي ترتيب.
- يمكن أن تحتوي `values` على واحد أو أكثر من مجموعات القيم المميزة المقابلة لـ `dimensions`.

ستتم إضافة `dimensions` في `filters` تلقائيًا إلى `groupByValues`.

تتحكم المعلمة `returnNegative` فيما إذا كانت النتائج تحتوي على إدخالات سالبة أم لا.

يظهر المثال التالي نموذج محتوى النص الأساسي.

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

يوضح المثال التالي كيفية الاستعلام عن جميع المنتجات في مواقع وأماكن متعددة.

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>متوفر حسب التعهد

يمكنك إعداد رؤية المخزون للسماح بجدولة التغييرات الفعلية المستقبلية وحساب الكميات المتوفرة حسب التعهد (ATP). ATP ‏– هو كمية الصنف المتوفرة ويمكن التعهد بها لعميل في الفترة التالية. قد يؤدي استخدام حساب الكميات المتوفرة حسب التعهد (ATP) إلى زيادة قدرة تنفيذ الطلبات بشكل كبير. للحصول على معلومات حول كيفية تمكين هذه الميزة، وكيفية التفاعل مع رؤية المخزون من خلال واجهة برمجة التطبيقات (API) الخاصة بها بعد تمكين الميزة، راجع  [جداول التغييرات الفعلية لرؤية المخزون والمتوفر حسب التعهد](inventory-visibility-available-to-promise.md#api-urls).

## <a name="allocation"></a>التوزيع

توجد واجهات برمجة التطبيقات المتعلقة بالتخصيص في [تخصيص رؤية المخزون](inventory-visibility-allocation.md#using-allocation-api).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
