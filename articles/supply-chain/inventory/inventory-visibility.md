---
title: الوظيفة الاضافيه لرؤية المخزون
description: يوضح هذا الموضوع كيفيه تثبيت الوظيفة الاضافيه لرؤية المخزون وتكوينها لـ Dynamics 365 Supply Chain Management.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114660"
---
# <a name="inventory-visibility-add-in"></a>الوظيفة الاضافيه لرؤية المخزون

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

تعد الوظيفة الاضافيه لرؤية المخزون بمثابه خدمة صغيرة مستقله وقابله للتغيير بشكل كبير والتي تمكن تتبع المخزون الفعلي في الوقت الحقيقي ، مما يوفر عرضا شاملا لرؤية المخزون.

يتم تصدير كافة المعلومات المرتبطة بالمخزون الفعلي إلى الخدمة بالقرب من الوقت الحقيقي خلال تكامل SQL في المستوي المنخفض. تقوم الانظمه الخارجية بالوصول إلى الخدمة من خلال واجهات RESTful API للاستعلام عن المعلومات الفعلية حول المجموعات المحددة من الابعاد ، ومن ثم استرداد قائمه بالمناصب الفعلية المتاحة.

رؤية المخزون عبارة عن خدمة صغيرة مضمنة في Microsoft Dataverse، مما يعني انه يمكنك توسيعها بواسطة إنشاء Power Apps وتطبيق Power BI لتوفير وظيفة مخصصه لتلبيه متطلبات الاعمال الخاصة بك. من الممكن أيضا ترقيه الفهرس للقيام باستعلامات المخزون.

توفر امكانيه رؤية المخزون خيارات التكوين التي تتيح له التكامل مع أنظمه متعددة الجهات الخارجية. وهو يدعم بعد المخزون القياسي والقابلية للتوسعة المخصصة والكميات التي تم حسابها والقياسية القابلة للتكوين.

يصف هذا الموضوع كيفيه تثبيت وتكوين الوظيفة الاضافيه لرؤية المخزون لـ Dynamics 365 Supply Chain Management، وكيفيه استخدام واجهه برمجه التطبيقات (API) الخاصة بها.

## <a name="install-the-inventory-visibility-add-in"></a>تثبيت الوظيفة الاضافيه لرؤية المخزون

يجب تثبيت الوظيفة الاضافيه لرؤية المخزون باستخدام Microsoft Dynamics Lifecycle Services (LCS). LCS عبارة عن مدخل تعاون يوفر بيئة ومجموعه من الخدمات المحدثة بشكل منتظم والتي تساعدك علي أداره دوره حياه التطبيقات الخاصة بتطبيقات Dynamics 365 Finance and Operations الخاصة بك.

للحصول على مزيد من المعلومات، راجع [موارد Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل أن تتمكن من تثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:

- احصل علي مشروع تنفيذ LCS مع نشر بيئة واحده علي الأقل.
- أنشئ مفاتيح بيتا لتقديمك في LCS.
- قم بتمكين مفاتيح بيتا لعرضك من أجل المستخدم الخاص بك في LCS.
- اتصل بفريق المنتج الخاص برؤية المخزون لـ Microsoft وقم بتوفير معرف البيئة الذي ترغب في نشر الوظيفة الاضافيه لرؤية المخزون فيه.

إذا كانت لديك إيه اسئله حول هذه المتطلبات الاساسيه ، الرجاء الاتصال بفريق رؤية المخزون.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>تثبيت الوظيفة الإضافية

لتثبيت الوظيفة الإضافية لرؤية المخزون، يجب عليك القيام بما يلي:

1. سجل الدخول إلى بوابة [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).
1. في الصفحة الرئيسية ، حدد المشروع حيث يتم نشر البيئة الخاصة بك.
1. في الصفحة المشروع ، حدد البيئة التي ترغب في تثبيت الوظيفة الاضافيه بها.
1. في الصفحة البيئة ، قم بالتمرير لأسفل حتى تشاهد قسم **الوظائف الاضافيه الخاصة بالبيئة**. إذا لم يكن المقطع مرئيا ، فتاكد من انه قد تمت معالجه المفتاح بيتا بشكل كامل.
1. في قسم **الوظائف الإضافية للبيئة**، حدد **تثبيت وظيفة إضافية جديدة**.
    ![صفحة البيئة في LCS](media/inventory-visibility-environment.png "صفحة البيئة في LCS")
1. حدد الرابط **تثبيت وظيفة إضافية جديدة**. يتم فتح قائمه بالوظائف الاضافيه المتاحة.
1. حدد **خدمه المخزون** من القائمة. (ملاحظه، قد يتم ادراج هذا الآن علي انه **الوظيفة الاضافيه لرؤية المخزون لـ Dynamics 365 Supply Chain Management** .)
1. ادخل قيما للحقول التالية الخاصة ببيئتك:

    - **مُعرِّف تطبيق AAD**
    - **معرف مستأجر AAD**

    ![أضافه في صفحه الاعداد](media/inventory-visibility-setup.png "صفحه اعداد الوظيفة الإضافية")

1. الموافقة علي البنود والشروط عن طريق تحديد خانه الاختيار **البنود والشروط**.
1. حدد **تثبيت**. ستظهر حاله الوظيفة الاضافيه باعتبارها **قيد التثبيت**. عند الانتهاء ، قم بتحديث الصفحة لرؤية تغيير الحالة علي **مثبت**.

### <a name="get-a-security-service-token"></a>الحصول علي رمز خدمه أمان

احصل علي رمز خدمه أمان بالقيام بما يلي:

1. سجل دخولك إلى مدخل Azure واستخدمه للعثور علي `clientId`و`clientSecret` لتطبيق Supply Chain Management.
1. إحضار Azure Active Directory رمز مميز (`aadToken`) عن طريق إرسال طلب HTTP بالخصائص التالية:
    - **عنوان URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **الطريقة** - `GET`
    - **محتوي النص الأساسي (بيانات النموذج)**:

        | المفتاح | القيمة |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | مورد | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. يجب ان تتلقي `aadToken` استجابه فيها، والتي تشبه المثال التالي.

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. المستقبل طلب JSON مشابها لما يلي:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    المكان:
    - `client_assertion`يجب ان تكون القيمة هي `aadToken` التي استلمتها في الخطوة السابقة.
    - `context`يجب ان تكون القيمة معرف البيئة حيث تريد توزيع الوظيفة الاضافيه.
    - قم بتعيين كافة القيم الأخرى كما هو موضح في المثال.

1. قم بإرسال طلب HTTP بالخصائص التالية:
    - **عنوان URL** - `https://securityservice.operations365.dynamics.com/token`
    - **الطريقة** - `POST`
    - **راس HTTP** - تضمين إصدار API (`Api-Version` المفتاح هو والقيمة هو `1.0`)
    - **محتوي أساسي** - تضمين طلب JSON الذي قمت بإنشاءه في الخطوة السابقة.

1. ستحصل علي `access_token` في الاستجابة. وهذا ما تحتاجه كرمز مميز في الحامل لاستدعاء امكانيه رؤية API للمخزون. فيما يلي مثال على ذلك.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>إلغاء تثبيت الوظيفة الإضافية

للغاء تثبيت الوظيفة الاضافيه ، حدد **إلغاء التثبيت**. تحديث LCS ستتم أزاله الوظيفة الاضافيه لرؤية المخزون. تقوم عمليه أزاله التثبيت بازاله تسجيل الوظيفة الاضافيه وبدء مهمة أيضا لتنظيف كافة بيانات الاعمال المخزنة في الخدمة.

## <a name="inventory-visibility-add-in-public-api"></a>واجهة API العامة للوظيفة الاضافيه لرؤية المخزون

تقدم واجهه برمجه التطبيقات العامة لـ REST الخاصة بالوظيفة الاضافيه لرؤية المخزون العديد من نقاط التكامل الخاصة. ويدعم ثلاثه أنواع من التفاعلات الرئيسية:

- يتم الآن ترحيل التغييرات الفعلية إلى الوظيفة الاضافيه من نظام خارجي.
- تستعلم عن الكميات الفعلية الحالية من نظام خارجي.
- مزامنة تلقائية مع Supply Chain Management الفعلية.

لا تعد المزامنة التلقائية جزءا من API العامة ، لكن يتم التعامل معها بدلا من ذلك في الخلفية للبيئات التي قامت بتمكين الوظيفة الاضافيه لرؤية المخزون.

### <a name="authentication"></a>مصادقة

يتم استخدام الرمز المميز لامان النظام لاستدعاء الوظيفة الاضافيه لرؤية المخزون ، لذا يجب إنشاء رمز مميز لـ Azure Active Directory باستخدام تطبيق Azure Active Directory.

لمزيد من المعلومات حول كيفيه الحصول علي الرمز المميز للامان ، راجع [تثبيت الوظيفة الاضافيه لرؤية المخزون](#install-add-in).

### <a name="configure-the-inventory-visibility-api"></a>تكوين واجهه برمجه تطبيقات امكانيه رؤية المخزون

قبل استخدام الخدمة ، يجب إكمال التكوينات الموضحة في الأقسام الفرعية التالية. قد يختلف التكوين استنادا إلى تفاصيل البيئة الخاصة بك. وهو يتضمن بشكل أساسي أربعه أجزاء:

- [تقسيم](#partitioning)
- [تكوينات الأبعاد](#dimension-configurations)
- [فهرسة](#indexing)
- [قياس مخصص](#custom-measurement)

#### <a name="partitioning"></a>تقسيم

يمكن للتقسيم ان يؤثر بشكل كبير علي أداء واجهة API الخاصة برؤية المخزون. انها لفكره جيده ان تقوم بتعريف نظام يسمح بالتجميعات الصغيرة للبيانات مع استمرار السماح باستعلامات البيانات ذات المعني.

سيكون `organizationId` (`dataAreaId` في Supply Chain Management) دائما جزءا من التقسيم ، ويتم تعيين رؤية المخزون بشكل افتراضي علي قسم حسب الابعاد *كموقع إلكتروني + موقع جغرافي*. وهذا يعني انه يجب دوما الاستعلام عن الخدمة باستخدام هذه الابعاد المحددة في عوامل التصفية.

> [!NOTE]
> *الموقع الإلكتروني* و *الموقع الجغرافي* هما اثنان من الابعاد الافتراضية في رؤية المخزون. في Supply Chain Management، تسمي هذه الابعاد *بالموقع الإلكتروني* (`InventSiteId`) *والمستودع* (`InventLocationId`)

### <a name="dimension-configurations"></a>تكوينات الأبعاد

ستوفر امكانيه رؤية المخزون قائمه بالابعاد الافتراضية العامة لتمكين تكامل النظام المصدر المتعدد.

يسرد الجدول التالي ابعاد المخزون التي ستكون أسماء الابعاد الافتراضية في رؤية المخزون.

| نوع البعد | اسم البُعد |
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

> [!NOTE]
> يكون نوع البعد المدرج في الجدول السابق كمرجع فقط. لا يلزم تحديد نوع البعد في رؤية المخزون.

في حاله وجود بعد مخصص والحاجة إلى التدفق للقيمة الافتراضية عند استهلاك رؤية المخزون ، يمكنك تكوين **اسم البعد المخصص** في رؤية المخزون.

وصول الانظمه الخارجية إلى رؤية المخزون من خلال واجات برمجه التطبيقات RESTful التي تتيح معلومات الكمية الفعلية حول مجموعات الابعاد المحددة التي سيتم الاستعلام عنها. بالنسبة للتكامل ، يمكنك رؤية المخزون من تكوين *مصدر بيانات القناة الخارجية* وبعد المصدر علي *الابعاد المستهدفة* في رؤية المخزون.

يجب ان تكون الابعاد المستهدفة واحده مما يلي:

- الابعاد الافتراضية في رؤية المخزون
- الأبعاد المخصصة

والغرض من تكوين الابعاد هو توحيد التكامل المتعدد الانظمه للاستعلام علي الابعاد وحدث الترحيل مع الابعاد.

#### <a name="indexing"></a>فهرسة

في معظم الأوقات ، لن يكون الاستعلام الفعلي الخاص بالمخزون علي مستوي "الإجمالي" الأعلى فقط ، ولكن قد ترغب في رؤية النتائج المجمعة استنادا إلى ابعاد المخزون.

توفر امكانيه رؤية المخزون المرونة عن طريق السماح لك باعداد الفهارس ، التي تعتمد علي البعد أو مجموعه الابعاد.

> [!NOTE]
> حاليا ، يمكنك فقط تكوين الفهارس بخمسه كحد اقصي. يجب مراعاه البعد أو مجموعه الابعاد التي ستستخدمها قبل التنفيذ للتاكد من انها ستفي باحتياجات أعمالك. علي سبيل المثال ، إذا كنت ترغب في الاستعلام عن المنتجات كالتالي:

- الاستعلام عن المنتج المجمع الفعلي بواسطة ابعاد *اللون* و *الحجم*.
- في بعض الحالات ، تريد فقط الاستعلام عن المنتج إجمالا.

سيكون لديك فهرسين محددين كالتالي:

- `["ColorId", "SizeId"]`
- `[]`

سيتم تجميع القوس الفارغ استنادا إلى "معرف المنتج" داخل القسم.

تحدد الفهرسة كيفيه تجميع النتائج استنادا إلى اعداد الاستعلام `groupBy`. في هذه الحالة إذا لم تقم بتحديد أي قيم `groupBy`، سيتم الحصول علي الإجماليات بواسطة `productid`. والا إذا قمت بتحديد `groupBy` كـ `groupBy=ColorId&groupBy=SizeId` ، ستحصل علي بنود متعددة يتم إرجاعها ، استنادا إلى مجموعتي اللون والحجم المختلفتين في النظام.

يمكنك وضع معايير الاستعلام في النص الأساسي للطلب.

فيما يلي نموذج استعلام حول المنتج بمجموعه اللون والحجم.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>قياس مخصص

وترتبط كميات القياس الافتراضية بـ Supply Chain Management، ومع ذلك قد ترغب في الحصول علي كميه تتكون من مجموعه من القياسات الافتراضية. وللقيام بذلك ، يمكن ان يكون لديك تكوين كميات مخصصه ، والتي ستتم اضافتها إلى إخراج الاستعلامات الفعلية.

وتتيح الوظيفة ببساطه تحديد مجموعه من القياسات التي ستتم اضافتها ، و/أو مجموعه من المقاييس التي سيتم طرحها ، من أجل القياس المخصص.

علي سبيل المثال ، باستخدام شرط الاستعلام التالي ، ستقوم بتكوين كميه القياس المخصصة باعتبارها `MyCustomAvailableforReservation` ليتم استهلاكها من قبل نظام الاستهلاك.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| نظام الاستهلاك | القياسات المحتسبة | مصدر البيانات | أداه التعديل | نوع حساب أداة التعديل |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | الطرح |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | الطرح |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | الجمع |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | الطرح |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | الطرح |

ومع ذلك ، سيقوم الاستعلام الموجود علي كميه القياس المخصصة بإرجاع المخرجات التالية.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

يعتمد إخراج `MyCustomAvailableforReservation`علي اعداد الحساب في القياسات المخصصة كما يلي:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>ترحيل التغييرات الفعلية

ويعتمد عنوان URL الذي يتم ترحيل الحدث عليه علي المنطقة الجغرافية بالبالضبط. سياخذ النموذج ما يلي:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

عند المصادقة ، يمكن استخدام محدد موقع المعلومات (URL) هذا مع أسلوب `POST` HTTP لإرسال احداث التغيير الفعلي إلى الخدمة.

يتم استخدام الراس الخاص للاتصال مع خدمات Dynamics 365 من خلال طلبات HTTP ، والذي يشير إلى معرف البيئة لمثيل Supply Chain Management الذي ترتبط به البيانات. على سبيل المثال:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>ترحيل التغييرات الفعلية مثال الاستعلام 1

يوضح هذا المثال السيناريو الذي ستقوم فيه باعداد تكوين البعد في Power Apps.

استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك. سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>ترحيل التغييرات الفعلية مثال الاستعلام 2

يوضح هذا المثال السيناريو الذي لا يتم فيه اعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه. يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource` خاليا أو فارغا أو مسافة بيضاء.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>خصائص حقل مستند JSON

تتضمن الحقول الموجودة في أمثله استعلام JSON المتوفرة في السابق الخصائص المسرودة في الجدول التالي.

| معرف الحقل | الوصف |
|---|---|
| `id` | معرف فريد لحدث التغيير المحدد. يتم استخدام هذا المعرف للتاكد من فشل الاتصال بالخدمة اثناء الترحيل ، ولن يؤدي أعاده إرسال الحدث إلى نفس الحدث الذي يتم حسابه مرتين في النظام. |
| `organizationId` | معرف المؤسسة المرتبط بالحدث. وهذا ما يعين لمؤسسات Supply Chain Management أو معرفات مناطق البيانات. |
| `productId` | معرف أمر الإنتاج المحدد. |
| `quantity` | الكمية التي يجب تغيير الكمية الحالية وفقا لها. علي سبيل المثال ، تمت أضافه 10 قطع من خبز البيغلز جديده إلى الرف، ستكون هذه القيمة 10. إذا تمت أزاله 3 قطع من خبز البيغلز من الرف أو بيعه ، ستكون هذه القيمة -3. |
| `dimensionDataSource` | مصدر البيانات الخاص بالابعاد المستخدمة في حدث تغيير الترحيل والاستعلام. إذا قمت بتحديد مصدر البيانات ، يمكنك استخدام الابعاد المخصصة من مصدر البيانات المحدد. باستخدام تكوين البعد ، يمكن ان يقوم ظهور المخزون بتعيين الابعاد المخصصة إلى الابعاد الافتراضية العامة. في حاله عدم تحديد `dimensionDataSource`، يمكنك استخدام الابعاد الافتراضية العامة فقط في الاستعلامات الخاصة بك.   |
| `dimensions` | كيس مجموعه حيوية من أزواج مفتاح/قيمه. سيتم تعيينها لبعض الابعاد في Supply Chain Management، ولكن يمكنك أيضا أضافه ابعاد مخصصه (مثل *المصدر*) والتي قد تشير إلى ما إذا كان الحدث واردا من Supply Chain Management أو من النظام الخارجي. |

### <a name="querying-current-on-hand"></a>الاستعلام عن الكمية الحالية

سيكون للنقطة النهائية للاستعلام عن الكمية الحالية عنوان URL مشابه:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

سيتم الاستعلام عنها باستخدام أسلوب `POST` HTTP.

#### <a name="current-on-hand-query-example-1"></a>مثال علي الاستعلام الفعلي حاليا 1

يوضح هذا المثال السيناريو الذي ستقوم فيه باعداد تكوين البعد في Power Apps.

استخدم الاستعلام التالي لتكوين تعيين البعد في Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

يمكنك الآن تحديد `dimensionDataSource` واستخدام الابعاد المخصصة في الاستعلامات الخاصة بك. سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه. يمكنك تحديد `DimensionDataSource` في `filters` وتحديد ابعاد مخصصه في كل من `filters` و`groupByValues`. سيقوم النظام تلقائيا بتحويل الابعاد المخصصة إلى الابعاد الاساسيه.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>مثال علي الاستعلام الفعلي حاليا 2

يوضح هذا المثال السيناريو الذي لا يتم فيه اعداد تعيينات لتكوين البعد في Power Apps، التالي يجب ان تستخدم الترحيل أيضا الابعاد الاساسيه. يجب ان تكون كافة الابعاد بابعاد أساسيه عندما يكون الحقل `dimensionDataSource`، ضمن `filters` خاليا أو فارغا أو مسافة بيضاء.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>مثال نتيجة الإرجاع

قد تؤدي الاستعلامات المعروضة في الامثله السابقة إلى إرجاع نتيجة مثل هذه.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
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

لاحظ انه يتم بناء حقول الكميات كقاموس للمقاييس والقيم المقترنة بها.
