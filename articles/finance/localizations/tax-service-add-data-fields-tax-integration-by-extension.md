---
title: أضافه حقول البيانات في تكامل الضريبة باستخدام الملحقات
description: يوضح هذا الموضوع كيفيه استخدام ملحقات X + + لأضافه حقول البيانات في تكامل الضريبة.
author: qire
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 79b51812eac354072ebf2a0ef6fe8d39610c6385
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649090"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>أضافه حقول البيانات في تكامل الضريبة باستخدام الملحقات

[!include [banner](../includes/banner.md)]


يوضح هذا الموضوع كيفيه استخدام ملحقات X + + لأضافه حقول البيانات في تكامل الضريبة. يمكن توسيع هذه الحقول إلى نموذج بيانات الضريبة لخدمه الضرائب واستخدامها لتحديد أكواد الضريبة. لمزيد من المعلومات، راجع [أضافه حقول البيانات في تكوينات الضريبة](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>نموذج البيانات

يتم تنفيذ البيانات الموجودة في نموذج البيانات بواسطة الكائنات ويتم تنفيذها بواسطة الفئات.

فيما يلي قائمة بالكائنات الرئيسية:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

يبين الرسم التوضيحي التالي كيفيه ارتباط هذه الكائنات.

[![علاقة كائن نموذج البيانات.](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

يمكن أن يحتوي كائن **المستند** على العديد من كائنات **البنود**. يحتوي كل كائن علي بيانات تعريف لخدمه الضرائب.

- إن `TaxIntegrationDocumentObject`تحتوي علي `originAddress` بيانات التعريف التي تحتوي علي معلومات حول عنوان المصدر وبيانات تعريف `includingTax`، والتي تشير إلى ما إذا كان مبلغ البند يتضمن ضريبة المبيعات.
- يحتوي `TaxIntegrationLineObject` على بيانات تعريف `itemId`، و`quantity`، و`categoryId`.

> [!NOTE]
> يقوم `TaxIntegrationLineObject` أيضًا بتطبيق كائنات **التكلفة**.

## <a name="integration-flow"></a>سير عمل التكامل

تتم معالجه البيانات الموجودة في التدفق بواسطة الانشطه.

### <a name="key-activities"></a>الأنشطة الرئيسية

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

يتم تشغيل الانشطه بالترتيب التالي:

1. تعيين الاسترداد
2. استرداد البيانات
3. خدمه الحساب
4. صرف العملة
5. استمرارية البيانات

على سبيل المثال، قم بتوسيع **استرداد البيانات** قبل **خدمة الحساب**.

#### <a name="data-retrieval-activities"></a>أنشطه استرداد البيانات

تسترد أنشطة **استرداد البيانات** البيانات من قاعده البيانات. وتتوفر المحولات الخاصة بالحركات المختلفة لاسترداد البيانات من جداول حركات مختلفه:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

في أنشطة **استرداد البيانات** هذه، يتم نسخ البيانات من قاعده البيانات إلى `TaxIntegrationDocumentObject`و`TaxIntegrationLineObject`. نظرًا لأن كل هذه الأنشطة تمتد إلى نفس فئة القالب المجرد، فإن لها طرقًا شائعة.

#### <a name="calculation-service-activities"></a>أنشطة خدمة الحساب

نشاط **خدمه الحساب** هو الارتباط بين الخدمة الضريبية وتكامل الضريبة. يعد هذا النشاط مسؤولا عن الوظائف التالية:

1. إنشاء الطلب.
2. ترحيل الطلب إلى خدمه الضرائب.
3. الحصول علي الاستجابة من خدمه الضرائب.
4. تحليل الاستجابة.

سيتم ترحيل حقل البيانات الذي تقوم بإضافته إلى الطلب مع بيانات التعريف الأخرى. 

## <a name="extension-implementation"></a>تطبيق ملحق

يوفر هذا المقطع خطوات مفصله تشرح كيفيه تنفيذ الملحق. إنه يستخدم الأبعاد المالية **مركز التكلفة** و **المشروع** كأمثلة.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>الخطوة 1. أضافه متغير البيانات في فئة الكائن

تحتوي فئة الكائن على متغير البيانات وطرق الحاصل/المعين للبيانات. أضف حقل البيانات إلى إما `TaxIntegrationDocumentObject` أو `TaxIntegrationLineObject` حسب مستوى الحقل. يستخدم المثال التالي مستوي البند، ويكون اسم الملف هو `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> إذا كان حقل البيانات الذي تقوم بإضافته موجودا علي مستوي المستند، فقم بتغيير اسم الملف إلى `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

تتم إضافة **مركز التكلفة** و **المشروع** كمتغيرات خاصه. قم بإنشاء أساليب الحاصل والحقل المعين لحقول البيانات هذه لمعالجه البيانات.

### <a name="step-2-retrieve-data-from-the-database"></a>الخطوة 2. استرداد البيانات من قاعده البيانات

حدد الحركة، ثم قم بتوسيع فئات المحول المناسبة لاسترداد البيانات. علي سبيل المثال، إذا كنت تستخدم حركة **أمر شراء**، فيجب عليك توسيع `TaxIntegrationPurchTableDataRetrieval` و`TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval`موروث من `TaxIntegrationPurchTableDataRetrieval`. ولا ينبغي تغييره إلا إذا كان منطق الجدولين `purchTable` و`purchParmTable` مختلفًا.

إذا كان يجب أضافه حقل البيانات لكافة الحركات، قم بتوسيع كافة فئات `DataRetrieval`.

ونظرًا لأن كافة أنشطة **استرداد البيانات** تقوم بتوسيع نفس فئة القالب، فان بني الفئة والمتغيرات والأساليب تكون مشابهة.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

يوضح المثال التالي البنية الاساسيه عند استخدام جدول `PurchTable`.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

عند استدعاء أسلوب `CopyToDocument`، يكون المخزن المؤقت لـ `this.purchTable` موجودًا بالفعل. ويتمثل الغرض من هذه الطريقة في نسخ كافة البيانات المطلوبة من `this.purchTable` إلى كائن `document` باستخدام أسلوب المعين الذي تم إنشاؤه في فئة `DocumentObject`.

وبالمثل، يوجد مخزن `this.purchLine` المؤقت بالفعل في أسلوب `CopyToLine`. ويتمثل الغرض من هذه الطريقة في نسخ كافة البيانات المطلوبة من `this.purchLine` إلى كائن `_line` باستخدام أسلوب المعين الذي تم إنشاؤه في فئة `LineObject`.

النهج المباشر هو توسيع الأسلوبين `CopyToDocument` و`CopyToLine`. ومع ذلك، نوصي بتجريب الأسلوبين `copyToDocumentFromHeaderTable` و`copyToLineFromLineTable` أولاً. إذا لم يعمل التطبيق كما هو مطلوب، فقم بتنفيذ الأسلوب الخاص بك، وقم باستدعائه في `CopyToDocument` و`CopyToLine`. هناك ثلاثه مواقف شائعه حيث يمكنك استخدام هذا الأسلوب:

- الحقل المطلوب موجود في `PurchTable` أو `PurchLine`. في هذه الحالة، يمكنك توسيع `copyToDocumentFromHeaderTable` و`copyToLineFromLineTable`. فيما يلي نموذج للتعليمات البرمجية.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- البيانات المطلوبة ليست موجودة في الجدول الافتراضي للحركة. ومع ذلك، توجد بعض علاقات الصلة مع الجدول الافتراضي، ويكون الحقل مطلوبا في معظم البنود. في هذه الحالة، قم باستبدال `getDocumentQueryObject` أو `getLineObject` للاستعلام عن الجدول بعلاقة الانضمام. في المثال التالي، يتم دمج حقل **التسليم الآن** مع أمر المبيعات على مستوي البند.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    في هذا المثال، يتم الإعلان عن المخزن المؤقت لـ `mcrSalesLineDropShipment`، ويتم تحديد الاستعلام في`getLineQueryObject`. يستخدم الاستعلام العلاقة `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. أثناء التوسع في هذه الحالة، يمكنك استبدال `getLineQueryObject` بكائن الاستعلام الذي قمت بإنشاءه. ومع ذلك، لاحظ النقاط التالية:

    * لأن القيمة المرجعة لأسلوب `getLineQueryObject` هي `SysDaQueryObject`، يجب عليك إنشاء هذا الكائن باستخدام نهج SysDa.
    * لا يمكن حذف الجدول الموجود.

- ترتبط البيانات المطلوبة بجدول المعاملات بعلاقة ربط معقدة، أو أن العلاقة ليست إلى واحد (1: 1) ولكنها علاقة واحدة إلى متعدد (1: N). في هذه الحالة، ستصبح الأمور معقده لبعضها. ينطبق هذا الموقف علي مثال الابعاد المالية. 

    في هذه الحالة، يمكنك تنفيذ الأسلوب الخاص بك لاسترداد البيانات. فيما يلي نموذج للتعليمات البرمجية في ملف `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>الخطوة 3. إضافة البيانات إلى الطلب

قم بتوسيع أسلوب `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` أو أسلوب `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` لإضافة البيانات إلى الطلب. فيما يلي نموذج للتعليمات البرمجية في ملف `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';
    // private const str IOEnumExample = 'Enum Example';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());

        // If the field to be extended is an enum type, use enum2Symbol to convert an enum variable exampleEnum of ExampleEnumType to a string
        // _destination.SetField(IOEnumExample, enum2Symbol(enumNum(ExampleEnumType), _source.getExampleEnum()));
    }
}
```

في هذا الكود، `_destination` هو كائن برنامج التضمين الذي يتم استخدامه لإنشاء الطلب، و`_source` هو كائن `TaxIntegrationLineObject`.

> [!NOTE]
> حدد اسم الحقل المستخدم في نموذج الطلب باعتباره **private const str**. يجب أن تكون السلسلة مطابقة تمامًا لاسم العقدة (وليس التسمية) المضافة في الموضوع [إضافة حقول البيانات في تكوينات الضرائب‬](tax-service-add-data-fields-tax-configurations.md).
> 
> عيّن الحقل في الأسلوب **copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine** باستخدام الأسلوب **SetField**. يجب أن يكون نوع بيانات المعلمة الثانية **سلسلة**. إذا لم يكن نوع البيانات **سلسلة**، فعليك تحويله إلى سلسلة.
> إذا كان نوع البيانات هو **نوع التعداد**، فمن المستحسن استخدام الأسلوب **enum2Symbol** لتحويل قيمة التعداد إلى سلسلة. يجب أن تكون قيمة التعداد المضافة في تكوين الضريبة مماثلة تمامًا لاسم التعداد. فيما يلي قائمة بالاختلافات بين قيمة التعداد وتسميته واسمه.
> 
>   - اسم التعداد enum هو اسم رمزي في التعليمات البرمجية. بإمكان **enum2Symbol()** تحويل قيمة التعداد إلى اسمه.
>   - قيمة التعداد هي عدد صحيح.
>   - بإمكان تسمية التعداد أن تكون مختلفة عبر اللغات المفضلة. بإمكان **enum2Str()** تحويل قيمة التعداد إلى تسميته.

## <a name="model-dependency"></a>تبعية النموذج

لإنشاء المشروع بنجاح ، أضف نماذج المرجع التالية إلى تبعيات النموذج:

- ApplicationPlatform
- ApplicationSuite
- محرك الضريبة
- الأبعاد، إذا كان البعد المالي مستخدمًا
- النماذج الضرورية الأخرى المشار اليها في التعليمات البرمجية

## <a name="validation"></a>التحقق من الصحة

بعد إكمال الخطوات السابقة، يمكنك التحقق من صحة تغييراتك.

1. في Finance، انتقل إلى **الحسابات الدائنة‬** وأضف **&debug=vs%2CconfirmExit&** إلى عنوان URL. على سبيل المثال، https://usnconeboxax1aos.cloud.onebox.dynamics.com/?cmp=DEMF&mi=PurchTableListPage&debug=vs%2CconfirmExit&. رمز **&** النهائي ضروري.
2. افتح صفحة **أمر الشراء** وحدد **جديد** لإنشاء أمر شراء.
3. قم بتعيين القيمة للحقل المخصص، ثم حدد **ضريبة المبيعات**. يتم تنزيل ملف استكشاف الأخطاء وإصلاحها مع البادئة **TaxServiceTroubleshootingLog** بشكل تلقائي. يحتوي هذا الملف على معلومات الحركة التي تم ترحيلها إلى خدمة حساب الضريبة. 
4. تحقق مما إذا كان الحقل المخصص الذي تمت إضافته موجودًا في القسم **إدخال حساب خدمة الضريبة في JSON** ومما إذا كانت قيمته صحيحة. إذا لم تكن القيمة صحيحة، فراجع الخطوات الواردة في هذا المستند.

مثال عن ملف:

```
===Tax service calculation input JSON:===
{
  "TaxableDocument": {
    "Header": [
      {
        "Lines": [
          {
            "Line Type": "Normal",
            "Item Code": "",
            "Item Type": "Item",
            "Quantity": 0.0,
            "Amount": 1000.0,
            "Currency": "EUR",
            "Transaction Date": "2022-1-26T00:00:00",
            ...
            /// The new fields added at line level
            "Cost Center": "003",
            "Project": "Proj-123"
          }
        ],
        "Amount include tax": true,
        "Business Process": "Journal",
        "Currency": "",
        "Vendor Account": "DE-001",
        "Vendor Invoice Account": "DE-001",
        ...
        // The new fields added at header level, no new fields in this example
        ...
      }
    ]
  },
}
...
```

## <a name="appendix"></a>الملحق

يعرض هذا الملحق رمز عينة كاملة لتكامل الأبعاد المالية، **مركز التكلفة** و **المشروع** على مستوى البند.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define the field name in the request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
