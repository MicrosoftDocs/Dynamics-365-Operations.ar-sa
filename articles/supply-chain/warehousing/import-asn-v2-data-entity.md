---
title: استيراد إشعارات شحن مقدم (ASN) واردة من خلال كيان البيانات V2
description: يوضح هذا الموضوع كيفية إدارة استيراد إشعارات الشحن المقدم (ASN) الواردة من خلال كيان بيانات ASN V2 الوارد.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249051"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="6a7a1-103">استيراد إشعارات شحن مقدم (ASN) واردة من خلال كيان البيانات V2</span><span class="sxs-lookup"><span data-stu-id="6a7a1-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a7a1-104">تقوم إشعارات الشحن المقدم (ASN) بإعلامك بتسليمات المورد.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="6a7a1-105">وتساعد المرسل في وصف محتويات الشحنة والمعلومات الإضافية الخاصة بها، مثل الأصناف والتعبئة.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="6a7a1-106">يمكن أن تساعد إشعارات شحن المقدم (ASN) العاملين في المستودع على معرفة ما يصل إليه.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="6a7a1-107">وبالتالي، يمكنهم تجهيزها.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-107">Therefore, they can prepare.</span></span> <span data-ttu-id="6a7a1-108">بالإضافة إلى ذلك، يمكن لعاملي المستودع استخدام ASN لمطابقة تفاصيل الشحنة بأمر الشراء المرتبط الذي تم إنشاؤه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="6a7a1-109">يقدم هذا الموضوع مجموعة من السيناريوهات التي تظهر من خلال الأمثلة كيفية التعامل مع ملفات ASN.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a7a1-110">لا ينطبق استيراد *ASN الوارد* إلا على الأصناف التي يتم تمكينها في إدارة المستودعات المتقدمة (WMS).</span><span class="sxs-lookup"><span data-stu-id="6a7a1-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="6a7a1-111">قبل استلام ASN، يجب تسجيل أمر الشراء في النظام مقابل المورد الذي يقوم بإرسال ASN.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="6a7a1-112">كيان ASN V2 الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="6a7a1-113">يمكنك استيراد إشعارات الشحن المقدم (ASN) الواردة باستخدام كيان بيانات المركبة *ASN V2 الوارد*.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="6a7a1-114">يستفيد *ASN V2 الوارد* من الكيانات التالية:</span><span class="sxs-lookup"><span data-stu-id="6a7a1-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="6a7a1-115">رأس حمل العمل الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-115">Inbound load header</span></span>
- <span data-ttu-id="6a7a1-116">رأس الشحنة الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-116">Inbound shipment header</span></span>
- <span data-ttu-id="6a7a1-117">بنى التعبئة لحمل العمل الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-117">Inbound load packing structures</span></span>
- <span data-ttu-id="6a7a1-118">حالات بنية التعبئة لحمل العمل الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="6a7a1-119">بنود حالة بنية التعبئة لحمل العمل الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="6a7a1-120">بنود بنية التعبئة لحمل العمل الوارد</span><span class="sxs-lookup"><span data-stu-id="6a7a1-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="6a7a1-121">يخصص كيان بيانات مركبة *ASN V2 الوارد* لسيناريوهات تكامل غير متزامنة حيث يتم استخدم عمليات الاستيراد المستندة إلى ملف XML.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="6a7a1-122">تنسيق XML لاستيراد إشعارات الشحن المقدم (ASN)</span><span class="sxs-lookup"><span data-stu-id="6a7a1-122">XML format for importing ASNs</span></span>

<span data-ttu-id="6a7a1-123">تدعم شركة Microsoft Dynamics 365 Supply Chain Management تنسيق XML التالي لاستيراد إشعارات الشحن المقدم (ASN).</span><span class="sxs-lookup"><span data-stu-id="6a7a1-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="6a7a1-124">تمثل كل عقدة في ملف XML سمة من كيان فردي.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="6a7a1-125">أمثلة</span><span class="sxs-lookup"><span data-stu-id="6a7a1-125">Examples</span></span>

<span data-ttu-id="6a7a1-126">توفر الأقسام الفرعية التالية أمثلة على ملفات استيراد ASN بتنسيق XML لشحنات المورد.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="6a7a1-127">مثال1</span><span class="sxs-lookup"><span data-stu-id="6a7a1-127">Example 1</span></span>

<span data-ttu-id="6a7a1-128">يوضح المثال التالي ملف XML لاستيراد شحنات المورد لأمر شراء واحد في حالة عدم تضمين أية تفاصيل حالة.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="6a7a1-129">مثال2</span><span class="sxs-lookup"><span data-stu-id="6a7a1-129">Example 2</span></span>

<span data-ttu-id="6a7a1-130">يوضح المثال التالي ملف XML لاستيراد شحنات المورد لأمر شراء واحد عند تضمين تفاصيل حالة.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="6a7a1-131">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="6a7a1-131">Example 3</span></span>

<span data-ttu-id="6a7a1-132">يوضح المثال التالي ملف XML لاستيراد شحنات المورد لأوامر شراء متعددة عند تضمين تفاصيل حالة.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="6a7a1-133">فحص نتائج استيراد ملف ASN</span><span class="sxs-lookup"><span data-stu-id="6a7a1-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="6a7a1-134">اتبع الخطوات التالية لفحص نتائج استيراد ملف ASN.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="6a7a1-135">انتقل إلى **إدارة المستودعات \> الأحمال‏‎ \> جميع الأحمال‏‎**.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6a7a1-136">ابحث عن حمل عمل تم إنشاؤه كجزء من عملية استيراد ASN وافتحه.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="6a7a1-137">في علامة التبويب السريعة **حمل العمل**، يجب أن ترى القيم التي تستند إلى ملف XML.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="6a7a1-138">في علامة التبويب السريعة **بنود حمل العمل**، يجب عليك رؤية أرقام أوامر الشراء وتفاصيل الأصناف التي تستند إلى ملف XML.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="6a7a1-139">في جزء الإجراءات، ضمن علامة التبويب **الشحن والاستلام**، في المجموعة **استلام** ، حدد **بنية التعبئة** لمراجعة بنية التعبئة الخاصة بحمل العمل.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="6a7a1-140">في علامة التبويب السريعة **البالتات**، يجب أن ترى لوحات الترخيص التي تستند إلى ملف XML.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="6a7a1-141">في علامة التبويب السريعة **الحالات**، يجب أن ترى الحالات التي تستند إلى ملف XML.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="6a7a1-142">في علامة التبويب السريعة **الأصناف**، يجب أن ترى الأصناف والكميات التي تستند إلى ملف XML.</span><span class="sxs-lookup"><span data-stu-id="6a7a1-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
