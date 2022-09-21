---
title: إعداد تدفق البيانات البديل لهذه التوصيات
description: توضح هذه المقالة كيفيه تكوين بيئة باستخدام تدفق بيانات بديل لتوفير البيانات لخدمه التوصيات.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460154"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>إعداد تدفق البيانات البديل لهذه التوصيات

[!include [banner](includes/banner.md)]

توضح هذه المقالة كيفيه تكوين بيئة باستخدام تدفق بيانات بديل لتوفير البيانات لخدمه التوصيات.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>مقارنه تدفق البيانات الجاهزة مع تدفق بيانات بديل

يصف الرسم التوضيحي التالي تدفق البيانات الذي يكون جاهزًا في البيئة.

![تدفق البيانات خارج الصندوق في بيئة](media/reco-out-of-the-box-dataflow-2.png)

يصف الرسم التوضيحي التالي تدفق بيانات بديل، حيث يتم استبدال وظيفة مجموعه مزامنة مخزن الوحدة بخطوات تدفق بيانات بديلة.

![تدفق بيانات بديل في بيئة](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>الافتراضات

- تفترض هذه المقالة أنك قد قمت بالفعل بتمكين خدمه التوصيات للبيئة الخاصة بك. لمزيد من المعلومات، راجع [توصيات المنتجات‬](enable-product-recommendations.md).
- عند العمل باستخدام الملفات والمجلدات في حساب Data Lake storage Microsoft Azure:

    - يمكنك استخدام إما واجهه موقع Azure علي الويب أو تطبيق مستكشف التخزين الخاص ب Azure.
    - نقاط البداية للعمل مع الملفات والمجلدات موجودة في الحاوية **dynamics365-financeandoperations** الموجودة ضمن المجلد الذي يسمي بأنه مطابق لمحدد موقع المعلومات الخاص بالبيئة.
    - إذا كان اسم بيئة **MyUAT** ، سيكون محدد موقع المعلومات الأساسي للبيئة `myuat.sandbox.operations.dynamics.com`.
    - في حاله اتصال أكثر من بيئة واحده بنفس حساب التخزين، سيكون لكل بيئة مجلد الجذر الخاص بها.

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب تلبية المتطلبات التالية، قبل أن تتمكن من استكمال الإجراء في هذه المقالة:

### <a name="set-up-microsoft-power-platform"></a>إعداد Microsoft Power Platform

لإعداد Microsoft Power Platform، اتبع الإرشادات الموجودة في [تمكين التكامل Microsoft Power Platform ](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>قم بتثبيت الوظيفة الإضافية ‏‫تصدير إلى Data Lake‬

لتثبيت التصدير إلى الوظيفة الإضافية Data Lake‬، اتبع الإرشادات الموجودة في [تثبيت التصدير إلى الوظيفة الإضافية Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> قم بتدوين قيم التكوين، لأنك ستحتاجها لبعض الخطوات التالية.

### <a name="configure-tables-to-export-in-dynamics-365"></a>تكوين الجداول لتصديرها في Dynamics 365

تتم أداره مزامنة الجدول من Dynamics 365 إلى Azure Data Lake Storage على صفحة **التصدير إلى Data Lake**. بسبب عدم وجود عنصر قائمه لهذه الصفحة في الوقت الحالي، يمكن للمستخدمين الموجودين في دور الأمان **مسؤول النظام** فتحه.

لتكوين جداول للتصدير في Dynamics 365، اتبع هذه الخطوات.

1. لفتح صفحة **تصدير إلى Data Lake** أضف السلسلة `?mi=DataFeedsDefinitionWorkspace`إلى عنوان URL الأساسي للبيئة، كما هو موضح في المثال التالي:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. في صفحة **تصدير Data Lake** ، ثم قم بنسخ الجداول المدرجة في [قائمه جداول](#list-of-retailsales-cube-tables) مكعب RetailSales من هذه المقالة.
1. في عمود **اسم النظام** ، قم بتوسيع قائمه خيارات التصفية.
1. بالنسبة لنوع عامل التصفية ، حدد **واحدا منهم**. ثم قم بوضع المؤشر في مربع النص، وقم بلصق قائمه الجداول التي قمت بنسخها من صفحه **تصدير إلى Data Lake** .
1. في أسفل قائمه خيارات التصفية، حدد **تطبيق**.
1. حدد كافة الصفوف الموجودة في الشبكة، ثم حدد **تنشيط**.

> [!NOTE]
> قبل الانتقال إلى الخطوة التالية، يجب تحديث كافة الصفوف إلى حالة **التشغيل**. استكشاف أخطاء وحلها كما هو مطلوب.

### <a name="create-a-synapse-workspace"></a>إنشاء مساحة عمل Synapse تلقائيًا

لإنشاء مساحة عمل Synapse إذا لم تكن لديك واحده بالفعل، اتبع الإرشادات الموجودة في [تشغيل سريع: إنشاء مساحة عمل Synapse](/azure/synapse-analytics/quickstart-create-workspace).

للاحتفاظ بتنظيم موارد Azure، نوصي بوضع حساب التخزين Data Lake ومساحة عمل Synapse معا في مجموعه موارد في Azure. يمكنك إعادة استخدام حساب التخزين الذي قمت بإنشائه أثناء تثبيت التصدير إلى الوظيفة الإضافية Data Lake.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>إنشاء قاعده بيانات في Synapse لمعالجه بيانات التوصية

استخدم تطبيق وحده تحكم الاداه المساعدة لنموذج البيانات العامة (CDMUtil_ConsoleApp) لإنشاء قاعده بيانات في مساحة عمل Synapse ونشرها من جداول نموذج البيانات العامة في تخزين Data Lake. نوصي باستخدام الأداه المساعدة الخاصة بنموذج البيانات العامة مع قاعده بيانات في بيئة التطوير، في حاله وجود إيه ملحقات.

> [!NOTE]
> تفترض الخطوات التالية أنه لا تتم إضافه إيه بيانات ملحقه إلى مكعب RetailSales.

اتبع هذه الخطوات لإنشاء قاعدة بيانات في Synapse.

1. انتقل إلى [Dynamics-365-FastTrack-تنفيذ الأصول GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app)، واتبع الخطوات لتنزيل ملف **CDMUtilConsoleApp.zip**.
1. استخرج الملف المضغوط إلى مجلد محلي.
1. قم بفتح **ملف الCDMUtil_ConsoleApp web.config** في محرر نص وقم بتحديث القيم التالية:

    1. تعيين **معرف المستأجر** - قيمة معرف مستأجر Azure الخاص بك.
    1. قم بتعيين قيمه مفتاح **الوصول** (مفتاح الوصول لحساب تخزينData Lake).

        1. في مدخل Azure، قم بفتح حساب التخزين الخاص بك.
        1. في القائمة الموجودة علي الجانب الأيسر من الصفحة، حدد **مفاتيح الوصول**.
        1. حدد **مفاتيح العرض** في أعلى الصفحة.
        1. حدد زر نسخ لأحد الحقلين الأساسيين، ثم قم بلصق القيمة بين علامتي الاقتباس المزدوجتين في ملف التكوين.

    1. قم بتعيين القيمة **ManifestURL‎** إلى محدد موقع المعلومات (URL) الخاص بالملف **ManifestURL‎** في Azure Data Lake Storage. للحصول علي عنوان URL، استعرض بحثًا عن الملف في مدخل Azure ، وحدد علامة القطع (**...**) علي الجانب الأيسر من طريقه العرض، ثم حدد **خصائص**. محدد موقع المعلومات (URL) هو الخاصية الاولي التي يتم عرضها في علامة التبويب **نظره عامه** .
    1. قم بتعيين القيمة **TargetDbConnectionString** لسلسله الاتصال لتجمع SQL بلا خادم المضمن الخاص بمساحة عمل Synapse الخاصة بك.

        1. في مساحة عمل Synapse، حدد علامة التبويب **إدارة**.
        1. في القائمة الفرعية، حدد **تجمعات SQL**.
        1. حدد الاسم **المضمن** لعرض خصائص التجمع.
        1. في مربع حوار الخصائص، حدد نوع اتصال ADO.NET الذي تريد استخدامه. ثم قم بنسخ قيمة سلسله الاتصال، ثم قم بلصقها بين علامات الاقتباس المزدوجة في ملف التكوين.

        > [!NOTE]
        > يجب أن يكون لديك إذن لإنشاء قاعدة بيانات. لتسهيل الاستخدام، قد تحتاج إلى استخدام حساب مسؤول **sqladminuser**.

    1. قم بإلغاء تحديد العقدة **ProcessEntities‎** ، وقم بتعيين قيمتها علي **true** (علي سبيل المثال `<add key="ProcessEntities" value ="true"/>`).

1. قم بحفظ الملف **‎CDMUtil_ConsoleApp.dll.config** وإغلاقه.
1. يستخدم الملف **EntityList.json** إلى دليل **/Manifest**.
1. في إطار موجه الأوامر، قم بتشغيل **cdmutil_consoleapp**.

> [!NOTE]
> عند مراجعه الإخراج، يجب ان يكون هناك 35 كيان/طرق عرض و75 جدول علي الأقل، ولا توجد أخطاء.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>إعداد دليل تجميع مقاسات Data Lake RetailSales

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>عمل نسخه احتياطيه من بيانات مكعب RetailSales الحالي من وحدة تخزين Data Lake

أسهل طريقه لإجراء نسخ احتياطي لبيانات مكعب RetailSales الحالي هي إعاده تسميه الدليل **RetailSales** في تخزين Data Lake **RetailSales-النسخ الاحتياطي** أو شيء مشابه. تحتفظ هذه الطريقة بالبيانات الموجودة في حالة عدم الحاجة إلى استكشاف الأخطاء وإصلاحها في وقت لاحق.

يمكن العثور علي مجلد مكعب **RetailSales‎** في الموقع التالي:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>إنشاء مجلد RetailSales‎ جديد وتحميل ملف النموذج

لإنشاء دليل **RetailSales‎** جديد وتحميل ملف **النموذج Json** إلى تخزين Data Lake، اتبع الخطوات التالية

1. قم بإنشاء دليل فارغ جديد في نفس المستوي مثل الدليل السابق ، وقم بتسميته **RetailSales‎**.
1. تحميل ملف **النموذج json** إلى الدليل الجديد.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>إنشاء تدفقات لنسخ بيانات مكعب RetailSales

ستقرأ التدفقات طرق عرض المكعب RetailSales وتقوم بتصدير البيانات إلى ملفات .csv في تخزين Data Lake.

لإنشاء تدفق لنسخ بيانات مكعب RetailSales، اتبع هذه الخطوات.

1. في مساحة عمل Synapse، حدد علامة التبويب **تكامل**.
1. حدد علامة الجمع (**+**)، ثم حدد **استيراد من قالب التدفق** .
1. قم بتحميل وتحديد [ExportRetailSalesCubeViews.zip file](https://aka.ms/reco-alternate-dataflow-files).
1. حدد الخدمة المرتبطة بقاعده بيانات SQL.
1. حدد الخدمة المرتبطة بحساب التخزين الخاص بك.
1. فتح أداة **نسخ البيانات** وتغيير خاصية **مسار المجلد** إلى **\<environment_name\> /**....

### <a name="test-execution-of-the-pipeline"></a>تنفيذ اختبار التدفق

نوصي باختبار التدفقات باستخدام طريقه عرض واحده فقط. تعمل طريقه عرض **RetailSales_RetailMediaTemplateView** بشكل جيد لأنها عاده ما تحتوي علي اقل من 10 صفوف.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>جدولة التدفق ليتم تشغيله حسب جدول متكرر

وفي كل مره يتم فيها تشغيل التدفق، يحدث استهلاك لAzure. نوصي بجدولة عمليات التنفيذ في فترات 48 ساعة أو أطول. يمكنك دائمًا تشغيل التدفق يدويًا إذا كان يجب عليك مزامنة البيانات مباشره. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>قائمه جداول المزامنة من Dynamics 365 إلى تخزين Data Lake

القائمة التالية من الجداول عبارة عن مجموعه فرعيه من كافة الجداول المطلوبة لمكعب RetailSales بأكمله. يتم استخدام 15 فقط من طرق العرض الموجودة في مكعب RetailSales بواسطة خدمه التوصيات، وتمت تصفيه قائمه الجداول المطلوبة وفقا لذلك.

### <a name="list-of-retailsales-cube-tables"></a>قائمه جداول مكعب RetailSales

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- الكتالوج
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- ريتايلكوستينفويسيجورتابل
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>عرض قائمه للمعلمة التي سيتم تمريرها إلى تدفقات Synapse

تحتوي القائمة المفصولة بفاصله التالية علي طرق عرض المكعب RetailSales التي ستنفذ التدفقات عمليه "تحديد" عليها. ثم ستقوم بنسخ النتائج إلى تخزين Data Lake.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> يجب ان تكون معلمه التدفقات قائمه بأسماء طرق العرض المفصولة بفواصل مفرده. يجب ألا يكون هناك فراغات أو اي من مواجز الأسطر.

## <a name="environment-specific-fixes"></a>الإصلاحات الخاصة بالبيئة

### <a name="retailchannelview-fix"></a>إصلاح RETAILCHANNELVIEW

يحتوي عرض **RETAILCHANNELVIEW‎** على عدد صحيح ضمني يمثل مؤسسه من نوع "قناه البيع بالتجزئة". يمكن أن تتغير القيمة الفعلية من النوع من بيئة إلى بيئة أو من مستاجر إلى مستاجر.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

لتحديث العدد الصحيح الضمني، اتبع هذه الخطوات.

1. في Dynamics 365، ابحث عن قيمة **معرف ChannelID‎** لقناة الإنترنت الخاصة بك.
1. في مثيل من SQL Server Management Studio (SSMS) المرفقة بقاعده بيانات Synapse، قم بتشغيل الاستعلام التالي.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. يستخدم هذا الزر في نسخ القيمة من العمود الأول (**INSTANCERELATIONTYPE‎**)، ولصقها في تعريف طريقه العرض.

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها

### <a name="pipeline-task-fails"></a>فشلت مهمة التدفق

يجب ان يكون هناك 15 مهمة تدفق لعميات تنفيذ خاصة بمهمة **CopyData**. في حاله فشل اي تنفيذ، يجب التحقق من وجود كافة كائنات SQL التابعة، ومن تشغيل الاستعلامات. تعد أسهل طريقه للوصول إلى كافة التبعيات هي استخدام SSMS للاتصال بقاعده البيانات. يمكنك بعد ذلك تحديد واحتجاز (أو النقر بزر الماوس الأيمن) علي طريقه عرض وتحديد **إنشاء CREATE باسم لاطار جديد**.

قد تحتوي رسالة الخطأ على النص التالي:

- خطا: حدث فشل علي جانب 'المصدر'
- خطا في معالجه الملف الخارجي: 'الحد الأقصى لعدد الأخطاء '.
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>سيناريو كمثال

في هذا المثال، تفشل المهمة **RetailSales_RetailProductCategory** وتتلقي الخطا "الحد الأقصى لعدد الأخطاء".

اتبع الخطوات التالية لتصحيح الخطأ.

1. افتح ملف **EntityList.json** في محرر نص (علي سبيل المثال، Code Visual Studio ).
1. ابحث عن تعريف طريقة العرض ل **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. تعتمد طريقه العرض هذه علي طريقه عرض أخرى واحده فقط: **RetailProductCategoryView** _. ابحث عن تعريف طريقة العرض ل *RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. وتعتمد طريقه العرض هذه علي ثلاث طرق عرض أخرى: **RETAILPRODUCTCATEGORY** و **ECORESPRODUCTTRANSLATIONS** و **RETAILCATEGORYEXPANDE**. ابحث عن تعريف لكل طريقه من طرق العرض هذه، وقم بسرد التبعيات الخاصة به. استمر إلى ان تعثر علي كافة طرق العرض التابعة لها.

    وهذه هي القائمة بالكامل في أمر شجره التبعية. يجب التحقق من صحة ثلاثة عشر عرضًا.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. في Excel، قم بإنشاء العدد التالي 13 **حدد العدد(\*) من \<view_name\>** الكشوفات. تشغيل هذه العبارات في SSMS وإرسال النتائج إلى نص. ثم قم بالتمرير خلال النتائج لمعرفه ما إذا كانت هناك أي طرق عرض فشلت. يقترح الخطا الأولي انه سيفشل أحد طرق العرض علي الأقل.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. أحد الطرق للتحقق من صحة ما تبحث فيه هو إنشاء عرض يعتمد علي الجذر لإنشاء تعريف طريقه العرض في SSMS. تحقق بعد ذلك من وجود عمود ملف Azure Data Lake الذي يسمي **‎r.filepath**. يشير وجود هذا العمود إلى ان طريقه العرض التي تقوم بفحصها هي قراءه البيانات من تخزين Data Lake.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على توصيات المنتجات](product-recommendations.md)

[تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce](enable-adls-environment.md)

[تمكين التوصيات المخصصة](personalized-recommendations.md)

[تمكين توصيات "تسوق منتجات تبدو مماثلة"](shop-similar-looks.md)

[إلغاء الاشتراك في التوصيات المخصصة](personalization-gdpr.md)

[إضافة توصيات المنتجات على نقطة البيع](product.md)

[إضافة توصيات إلى شاشة المعاملة](add-recommendations-control-pos-screen.md)

[إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)](modify-product-recommendation-results.md)

[إنشاء توصيات مختارة يدويًا](create-editorial-recommendation-lists.md)

[إنشاء توصيات بواسطة بيانات العرض التوضيحي](product-recommendations-demo-data.md)

[الأسئلة المتداولة حول توصيات المنتجات](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
