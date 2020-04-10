---
title: سلسله تبعية الكيان (أمر التزامن)
description: يحدد هذا الموضوع ترتيب المزامنة الذي يجب اتباعه لإنشاء البيانات الأولية.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173121"
---
# <a name="entity-dependency-chain-synchronization-order"></a>سلسله تبعية الكيان (أمر التزامن)

[!include [banner](../../includes/banner.md)]



يتم سرد الجداول والكيانات التالية بحسب الترتيب الذي يجب عليك تمكينها فيه. عندما تقوم بتمكين مخطط للمزامنة الأولية، فإن الكتابة الثنائية تقوم تلقائيًا بالكشف عن المخططات الأخرى التي يجب تمكينها. يمكنك استخدام صفحة **الكتابة الثنائية**في تطبيقات Finance and Operations لتحديد أو إلغاء تحديد الكيانات أثناء المزامنة الأولية.

وفي أحدث إصدار من الكتابة الثنائية، يمكنك تمكين بعض الكيانات فقط، ويتم التعامل مع التبعيات لك.

## <a name="dynamics-365-supply-chain-management-entities"></a>كيانات Dynamics 365 Supply Chain Management

يتم سرد الكيانات التالية لـ Supply Chain Management بحسب الترتيب الذي يجب عليك تمكينها فيه.

| اسم التعيين في صفحة الكتابة الثنائية | اسم بيانات تعريف الكيان في Supply Chain Management | اسم بيانات تعريف الكيان في Common Data Service | الملاحظات |
|---|---|---|---|
| الوحدات ... وحدات القياس                                                                      | UnitOfMeasureEntity                                    | وحدة القياس                                          | |
| تحويلات الوحدات ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| جميع المنتجات ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| مجموعات أبعاد المنتج ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| مجموعات أبعاد التخزين ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| مجموعات أبعاد التعقب ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| الألوان ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| الأحجام ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| الأنماط ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| التكوينات ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| المنتجات الصادرة V2‏ ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service منتجات مميزة صادرة من ... منتجات                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | منتج                                      | |
| كود شريطي معرف برقم المنتج ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| إعدادات الأمر الافتراضية ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| إعدادات الأمر الافتراضية للمنتج V2‏ ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| تحويلات وحدة خاصة بالمنتج ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| المواقع ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| المستودعات ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | راجع [الملاحظة 1](#scm-notes). |
| ألوان أصل المنتج ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| أحجام أصل المنتج ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| أنماط أصل المنتج ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| تكوينات أصل المنتج ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| فئات المنتجات ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | راجع [الملاحظة 2](#scm-notes). |
| تعيينات فئات المنتجات ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| التدرجات الهرمية لفئات المنتجات ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| أدوار التدرجات الهرمية لفئات المنتجات ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| ممر المخزون ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| مناطق المستودعات ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| مجموعات مناطق المستودعات ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| مواقع المستودع ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | راجع [الملاحظة 3](#scm-notes). |
| رؤوس عمل المستودعات ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| بنود عمل المستودعات ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | راجع [الملاحظة 4](#scm-notes). |
| أوضاع التسليم ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| شروط التسليم ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| أكواد أصول أوامر المبيعات ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| رؤوس أوامر مبيعات Common Data Service ... أوامر المبيعات                             | SalesOrderHeaderCommon Data ServiceEntity              | أمر المبيعات                                   | |
| بنود أمر مبيعات Common Data Service ... تفاصيل أوامر المبيعات                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| رأس عرض أسعار مبيعات Common Data Service ... عروض الأسعار                               | SalesQuotationHeaderCommon Data ServiceEntity          | عرض أسعار                                        | |
| بنود عروض أسعار مبيعات Common Data Service ... تفاصيل عروض الأسعار                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| رؤوس فواتير المبيعات V2 ... الفواتير                                               | SalesInvoiceHeaderV2Entity                             | فاتورة                                      | |
| بنود فواتير المبيعات V2 ... تفاصيل الفواتير                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>الملاحظات الخاصة بالتعيين

1. بسبب التبعية الذاتية، قد تضطر إلى تشغيل المزامنة الأولية مرتين.
2. افتراضيًا، يتم إيقاف تشغيل المزامنة الأوليه بسبب علاقة الأصل-التابع (لا تتم معالجه الترتيب "الذكي" بواسطة النظام الأساسي). وبالتالي، يجب مزامنة فئات المنتجات الموجودة يدويًا (على سبيل المثال، عن طريق تحديث وصف الفئة) بالترتيب الصحيح (الفئة الأساسية أولاً، ثم الفئات الفرعية، ثم الفئات التابعة للفئات الفرعية). انتقل إلى **إدارة معلومات المنتج \> الإعداد \> الفئات والسمات \> التدرجات الهرمية للفئات**. في صفحة **التدرجات الهرمية للفئات**، يمكنك تحديد كل تدرج هرمي ومراجعه فئات المنتجات فيه.
3. سيتسبب تعيين حقول بحث **ItemNumberInLocation** الفارغة ومناطق المستودعات الإضافية الأولى والثانية والثالثة في فشل المزامنة الأولية. ولذلك، تتم إزالة هذه التعيينات الآن.
4. سيتسبب تعيين حقل **CaptureWeight** الفارغ في فشل المزامنة الأولية. ولذلك، تتم إزالة هذا التعيين الآن.

### <a name="setup-related-information"></a>المعلومات ذاتالصلة بالإعداد

+ عندما يتم إنشاء السجلات لأول مرة في كيان **المنتجات** في التطبيقات المستندة إلى النماذج في تطبيقات Dynamics 365، فإنها تكون بالحالة **مسودة**. لتغيير الحالة إلى **نشط**، انتقل إلى **إعدادات \>الإدارة \> إعدادات النظام \> المبيعات** في التطبيق المستند إلى النموذج، وقم بتعيين خيار **إنشاء المنتجات في حالة نشطة** إلى **نعم**.
+ إذا قمت بإنشاء السجلات في كيان **المنتجات** في التطبيقات المستندة إلى النماذج في Dynamics 365 أو في Common Data Service قبل تمكين الكتابة الثنائية، فإن هذه السجلات سيتم تحديثها فقط إذا كان المفتاح بأكمله، بما في ذلك **الشركة**، يتطابق مع البيانات في تطبيق Finance and Operations.
+ وتُعد مزامنة كيان **المنتجات** أحادية الاتجاهات من تطبيقات Finance and Operations إلى Common Data Service. إذا تم تحديث حقل معين في كيان **المنتجات** في التطبيقات المستندة إلى النماذج في Dynamics 365، فستتم الكتابة فوق التحديث أثناء عملية المزامنة التالية من Finance and Operations.

### <a name="known-issues"></a>مشكلات معروفة

- يحدث خطأ عند حذف وحدة في تطبيق Finance and Operations. عند مزامنة وحدات القياس من تطبيق Finance and Operations إلى Common Data Service، سيتم إنشاء الوحدة الأولى من فئة محددة كوحدة أساسية وسيمنع الحذف.

    **التخفيف** : قم أولاً بحذف الوحدة في Common Data Service. ويمكن بعد ذلك حذفه في تطبيق Finance and Operations.

- يحدث خطأ عند حذف موقع تشغيلي في تطبيق Common Data Service. حالات رسالة الخطأ، "سجل معلومات: تحذير: لا يمكن حذف العنوان الأساسي. تحذير: تعذر حذف سجل الكيان بسبب فشل التحقق من صحة مصدر البيانات التالي: InventSiteLogisticsLocation (InventSiteLogisticsLocation)." يحدث هذا الخطأ نتيجة لوجود مشكلة في كيان البيانات في تطبيق Finance and Operations.

    **التخفيف:** يمكنك حذف الموقع في تطبيق Finance and Operations. سيتم بعد ذلك حذف الموقع في Common Data Service في حالة تشغيل مخطط الكتابة الثنائية المطابقة.

## <a name="dynamics-365-finance-entities"></a>كيانات Dynamics 365 Finance

يتم سرد الكيانات التالية لـ Dynamics 365 Finance بحسب الترتيب الذي يجب عليك تمكينها فيه.

| اسم التعيين في صفحة الكتابة الثنائية | اسم بيانات تعريف الكيان في Finance | اسم بيانات تعريف الكيان في Common Data Service | الملاحظات |
|---|---|---|---|
| العملات ... transactioncurrencies                                            | CurrencyEntity                              | عملة                                   | |
| نوع سعر الصرف ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| زوج عملة سعر الصرف ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service أسعار الصرف ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | راجع [الملاحظة 1](#fin-notes). |
| كيان تكامل التقويم المالي ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| كيان تكامل سنة التقويم المالي ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| فتره التقويم المالي ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| نوع التدرج الهرمي للمؤسسات ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | راجع [الملاحظة 1](#fin-notes). |
| أغراض التدرج الهرمي للمؤسسات ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | راجع [الملاحظة 1](#fin-notes). |
| الكيانات القانونية ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | راجع [الملاحظة 1](#fin-notes). |
| الكيانات القانونية ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| وحدة التشغيل ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | راجع [الملاحظة 1](#fin-notes). |
| التدرج الهرمي للمؤسسات - المنشور ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | راجع [الملاحظة 1](#fin-notes). |
| ملحقات الأسماء ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| أيام الدفع Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| بنود يوم الدفع Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| جدول الدفع ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| بنود جدول الدفع ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| شروط الدفع ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| طريقة دفع العميل ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| طريقة دفع المورد ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| مجموعات العملاء ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| مجموعات الموردين ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| مجموعات ضريبة المبيعات ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| مجموعات ضريبة مبيعات الصنف ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| مجموعات ترحيل دفتر أستاذ ضريبة المبيعات V2‏ ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Common Data Service لكيان كود الإعفاء من ضريبة المبيعات ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| هيئات ضريبة المبيعات ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| كود ضريبة المبيعات ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | راجع [الملاحظة 1](#fin-notes). |
| تنسيق البعد المالي ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| الأبعاد المالية ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| مجموعات ضريبة الخصم ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| أكواد ضريبة الخصم ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| دليل الحسابات ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| دفتر الأستاذ ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | راجع [الملاحظة 1](#fin-notes). |
| فئات الحساب الرئيسي ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| الحساب الرئيسي ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| العملاء V3 ... الحسابات                                                       | CustCustomerV3Entity                        | حساب                                    | راجع [الملاحظة 2](#fin-notes). |
| العملاء V3 ... جهات الاتصال                                                       | CustCustomerV3Entity                        | جهة الاتصال                                    | راجع [الملاحظة 3](#fin-notes). |
| الموردون V2 ‏... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | راجع [الملاحظة 2](#fin-notes). |
| جهات اتصال Common Data Service  V2 ... جهات الاتصال                                    | smmContactPersonCommon Data ServiceV2Entity | جهة الاتصال                                    | راجع [الملاحظة 4](#fin-notes). |
| جهات اتصال Common Data Service  V2 ... جهات الاتصال                                    | smmContactPersonCommon Data ServiceV2Entity | جهة الاتصال                                    | راجع [الملاحظة 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>الملاحظات الخاصة بالتعيين

1. تحدث مزامنة أحادية الاتجاه من تطبيقات Finance and Operations إلى Common Data Service.
2. بسبب التبعية الذاتية، قد تضطر إلى تشغيل المزامنة الأولية أكثر من مرة واحدة. تأكد من تحديد **العميل** كنوع علاقة عند إنشاء حساب باستخدام صفحة **الحسابات** في Common Data Service. إذا واجهتك مشكلات في حقل **جهة الاتصال الرئيسية** أثناء المزامنة الأولية، قم بإزالة هذا الحقل من التعيين، ثم قم بتشغيل المزامنة الأولية مرة أخرى. بعد إكمال المزامنة الأولية بنجاح، قم بإيقاف التعيين، ثم أضف حقل **جهة الاتصال الرئيسية** إليه مرة أخرى. ثم ابدأ التعيين، ولكن مع تخطي المزامنة الأولية. لن يتم تضمين قيمة حقل **جهة الاتصال الرئيسية** في المزامنة الأولية، ويجب ترحيل القيم يدويًا.
3. تأكد من تعيين خيار **قابل للبيع** إلى **نعم** في صفحة **جهات الاتصال** في Common Data Service عند محاولة إنشاء عميل من نوع **الشخص**.
4. يحتوي هذا التعيين على عامل تصفية على الجانبين لربط جهات اتصال العملاء. افتح تفاصيل التعيين، وحدد زر التصفية (رمز القمع) بجانب اسم كيان **Sales.Contact**، وتأكد من أن معايير الملف تحتوي على **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. يحتوي هذا التعيين على عامل تصفية على الجانبين لربط جهات اتصال الموردين. افتح تفاصيل التعيين، وحدد زر التصفية (رمز القمع) بجانب اسم كيان **Sales.Contact**، وتأكد من أن معايير الملف تحتوي على **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>كيانات Dynamics 365 Human Resources

يتم سرد الكيانات التالية لـ Dynamics 365 Human Resources بحسب الترتيب الذي يجب عليك تمكينها فيه.

| اسم التعيين في صفحة الكتابة الثنائية | اسم بيانات تعريف الكيان في Human Resources | اسم بيانات تعريف الكيان في Common Data Service | الملاحظات |
|---|---|---|---|
| cdm_jobfunction - مهمة الوظيفة                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - أنواع الوظائف                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - الوظائف                                               |                                   | cdm_jobs                         | |
| cdm_jobs - تفاصيل الوظيفة                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - المنصب الأساسي                              | HcmPositionBaseEntity             | cdm_jobposition                  | راجع [الملاحظة 1](#hr-notes). |
| cdm_jobposition - تفاصيل المناصب                            | HcmPositionDetailEntity           | cdm_jobposition                  | راجع [الملاحظة 1](#hr-notes). |
| cdm_jobposition - مدة المنصب                           | HcmPositionDurationEntity         | cdm_jobposition                  | راجع [الملاحظة 1](#hr-notes). |
| cdm_jobposition - التدرجات الهرمية للمناصب                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | راجع [الملاحظة 1](#hr-notes). |
| cdm_veteranstatus - حالة الخبرة                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - الأصل العرقي‬                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - كود اللغة                              |                                   | cdm_languagecode                 | |
| cdm_worker - العامل                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - عمليات التوظيف                                 |                                   | cdm_employments                  | |
| cdm_employments - تفاصيل التوظيف                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - تعيين العاملين بالمناصب | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | راجع [الملاحظة 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>الملاحظات الخاصة بالتعيين

1. يتم تعيين كيان Common Data Service واحد إلى عدة كيانات تطبيق Finance and Operations.
2. يحتوي هذا التعيين على مرجع ذاتي.

## <a name="asset-management-entities"></a>كيانات إدارة الأصول

يتم سرد الكيانات التالية لإدارة الأصول لـ Dynamics 365 Supply Chain Management بحسب الترتيب الذي يجب عليك تمكينها فيه.

| اسم التعيين في صفحة الكتابة الثنائية | اسم بيانات تعريف الكيان في إدارة الأصول | اسم بيانات تعريف الكيان في Common Data Service | الملاحظات |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | حالات دورة حياة الأصول في إدارة الأصول               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | نماذج دورة حياة الأصول في إدارة الأصول               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | نماذج دورة حياة موقع العمل في إدارة الأصول | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | حالات دورة حياة موقع العمل في إدارة الأصول | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | أنواع الأصول في إدارة الأصول                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | أنواع مواقع العمل في إدارة الأصول            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | مواقع العمل في إدارة الأصول                 | msdyn_functionallocations                | راجع [الملاحظة](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | أصول إدارة الأصول                               | msdyn_customerassets                     | راجع [الملاحظة](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | الشركات المصنعة في إدارة الأصول                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | نماذج إدارة الأصول                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | ضمان إدارة الأصول                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>الملاحظات الخاصة بالتعيين

- بسبب التبعية الذاتية، قد تضطر إلى تشغيل المزامنة الأولية أكثر من مرة واحدة.
