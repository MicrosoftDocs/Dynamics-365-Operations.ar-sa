---
title: استيراد إخطارات ASN الواردة عبر كيان البيانات V3
description: يوضح هذا الموضوع كيفية إدارة استيراد إشعارات الشحن المقدم (ASN) الواردة من خلال كيان بيانات ASN الوارد.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 44ec0230236451a413d483b3e9f3ddc58b49a0b0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740127"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>استيراد إخطارات ASN الواردة عبر كيان البيانات V3

[!include [banner](../../includes/banner.md)]

تقوم إشعارات الشحن المقدم (ASN) بإعلامك بتسليمات المورد. وتساعد المرسل في وصف محتويات الشحنة والمعلومات الإضافية الخاصة بها، مثل الأصناف والتعبئة.

يمكن أن تساعد إشعارات شحن المقدم (ASN) العاملين في المستودع على معرفة ما يصل إليه. وبالتالي، يمكنهم تجهيزها. بالإضافة إلى ذلك، يمكن لعاملي المستودع استخدام ASN لمطابقة تفاصيل الشحنة بأمر الشراء المرتبط الذي تم إنشاؤه سابقًا.

يقدم هذا الموضوع مجموعة من السيناريوهات التي تظهر من خلال الأمثلة كيفية التعامل مع ملفات ASN.

> [!IMPORTANT]
> لا ينطبق استيراد *ASN الوارد* إلا على الأصناف التي يتم تمكينها في إدارة المستودعات المتقدمة (WMS). قبل استلام ASN، يجب تسجيل أمر الشراء في النظام مقابل المورد الذي يقوم بإرسال ASN.

## <a name="inbound-asn-v3-entity"></a>كيان ASN V3 الوارد

يمكنك استيراد إشعارات الشحن المقدم (ASN) الواردة باستخدام كيان بيانات المركبة *ASN V3 الوارد*. يستفيد *ASN V3 الوارد* من الكيانات التالية:

- رأس حمل العمل الوارد
- رأس الشحنة الوارد
- بنى التعبئة لحمل العمل الوارد
- حالات بنية التعبئة لحمل العمل الوارد
- بنود حالة بنية التعبئة لحمل العمل الوارد
- بنود بنية التعبئة لحمل العمل الوارد

يخصص كيان بيانات مركبة *ASN V3 الوارد* لسيناريوهات تكامل غير متزامنة حيث يتم استخدم عمليات الاستيراد المستندة إلى ملف XML.

## <a name="xml-format-for-importing-asns"></a>تنسيق XML لاستيراد إشعارات الشحن المقدم (ASN)

تدعم شركة Microsoft Dynamics 365 Supply Chain Management تنسيق XML التالي لاستيراد إشعارات الشحن المقدم (ASN). تمثل كل عقدة في ملف XML سمة من كيان فردي.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>أمثلة

توفر الأقسام الفرعية التالية أمثلة على ملفات استيراد ASN بتنسيق XML لشحنات المورد.

### <a name="example-1"></a>مثال1

يوضح المثال التالي ملف XML لاستيراد شحنات المورد لأمر شراء واحد في حالة عدم تضمين أية تفاصيل حالة.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>مثال2

يوضح المثال التالي ملف XML لاستيراد شحنات المورد لأمر شراء واحد عند تضمين تفاصيل حالة.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>المثال الثالث

يوضح المثال التالي ملف XML لاستيراد شحنات المورد لأوامر شراء متعددة عند تضمين تفاصيل حالة.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>فحص نتائج استيراد ملف ASN

اتبع الخطوات التالية لفحص نتائج استيراد ملف ASN.

1. انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.
1. ابحث عن حمل عمل تم إنشاؤه كجزء من عملية استيراد ASN وافتحه.
1. في علامة التبويب السريعة **حمل العمل**، يجب أن ترى القيم التي تستند إلى ملف XML.
1. في علامة التبويب السريعة **بنود حمل العمل**، يجب عليك رؤية أرقام أوامر الشراء وتفاصيل الأصناف التي تستند إلى ملف XML.
1. في جزء الإجراءات، ضمن علامة التبويب **الشحن والاستلام**، في المجموعة **استلام** ، حدد **بنية التعبئة** لمراجعة بنية التعبئة الخاصة بحمل العمل.
1. في علامة التبويب السريعة **البالتات**، يجب أن ترى لوحات الترخيص التي تستند إلى ملف XML.
1. في علامة التبويب السريعة **الحالات**، يجب أن ترى الحالات التي تستند إلى ملف XML.
1. في علامة التبويب السريعة **الأصناف**، يجب أن ترى الأصناف والكميات التي تستند إلى ملف XML.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
