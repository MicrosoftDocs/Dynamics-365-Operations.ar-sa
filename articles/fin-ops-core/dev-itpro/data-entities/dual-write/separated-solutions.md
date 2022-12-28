---
title: حزمة تنسيق تطبيق الكتابة المزدوجة المنفصلة
description: لم تعد حزمة تنسيق تطبيق الكتابة المزدوجة حزمة واحدة ولكن تم تقسيمها إلى حزم أصغر. توضح هذه المقالة الحلول والخرائط التي تحتوي عليها كل حزمة وتبعيتها علي الحزم الأخرى.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 7f2a9b9e52b80c0feae0ac0dcb1ddf0a5c0cd27c
ms.sourcegitcommit: 8aba7d2f45ef03a14f33f4b430ce92a11c876e2e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/16/2022
ms.locfileid: "9884106"
---
# <a name="separated-dual-write-application-orchestration-package"></a>حزمة تنسيق تطبيق الكتابة المزدوجة المنفصلة

[!include [banner](../../includes/banner.md)]



في السابق، كانت حزمة تنسيق تطبيق الكتابة المزدوجة عبارة عن حزمة واحدة تحتوي على الحلول التالية:

- ملاحظات حول Dynamics 365
- Dynamics 365 finance and operations Common Anchor
- خرائط كيانات الكتابة المزدوجة في Dynamics 365 Finance and Operations
- تطبيق إدارة أصول Dynamics 365
- إدارة أصول Dynamics 365
- عام HCM
- سلسلة توريد Dynamics 365 الموسعة
- Dynamics 365 Finance Extended
- Dynamics 365 finance and operations Common
- شركة Dynamics 365
- أسعار صرف العملات
- Field Service Common

نظرًا لأنها كانت حزمة واحدة، خلقت هذه الحزمة حالة "الكل أو لا شيء" للعملاء. ومع ذلك، أصبحت Microsoft الآن تفصلها إلى حزم أصغر. وبالتالي، بإمكان العملاء تحديد الحزم الخاصة بالحلول التي يحتاجونها فقط. على سبيل المثال، إذا كنت عميل Microsoft Dynamics 365 Supply Chain Management، ولا تحتاج إلى التكامل مع Dynamics 365 Human Resources والملاحظات وإدارة الأصول، فيمكنك استبعاد تلك الحلول من الحلول التي تم تثبيتها. وبما ان الحلول الاساسيه للأسماء والناشر وإصدارات الخريطة تبقي كما هي، فان هذا التغيير لا يتم كسره. تتم ترقيه عمليات التثبيت الموجودة.

![حزمه مفصوله.](media/separated-package-1.png)

توضح هذه المقالة الحلول والخرائط التي تحتوي عليها كل حزمة وتبعيتها علي الحزم الأخرى.

## <a name="dual-write-application-core"></a>أساس التطبيق ثنائي الكتابة

تتيح الحزمة الرئيسية للتطبيق الثنائي الكتاب للمستخدمين تثبيت وتكوين الكتابة الثنائية دون اي تطبيق للتفاوضات العملاء. يحتوي على الحلول الخمسة التالية.

| اسم فريد                           | الاسم المعروض                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | شركة Dynamics 365                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Common |
| CurrencyExchangeRates                 | أسعار صرف العملات                    |
| msdyn_DualWriteAppCoreMaps            | خرائط الكيانات الأساسية لتطبيقات الكتابة المزدوجة   |
| msdyn_DualWriteAppCoreAnchor          | نقطة الارتساء الأساسية لتطبيقات الكتابة المزدوجة        |

الخرائط التالية متوفرة في هذه الحزمة.

| تطبيقات التمويل والعمليات     | تطبيقات Customer Engagement                    |
|---------------------------------|---------------------------------------------|
| وحدة التشغيل                  | msdyn_internalorganizations                 |
| التدرج الهرمي للمؤسسات          | msdyn_internalorganizationhierarchies       |
| الكيانات القانونية                  | msdyn_internalorganizations                 |
| الكيانات القانونية                  | cdm_companies                               |
| أغراض التدرج الهرمي للمؤسسات | msdyn_internalorganizationhierarchypurposes |
| سعر صرف زوج العملات     | msdyn_currencyexchangeratepairs             |
| ملحقات الاسم                    | msdyn_nameaffixes                           |
| نوع سعر الصرف              | msdyn_exchangeratetypes                     |
| أسعار الصرف في CDS              | msdyn_currencyexchangerates                 |
| نوع التدرج الهرمي للمؤسسات     | msdyn_internalorganizationhierarchytypes    |
| العملات                      | transactioncurrencies                       |
| كيان إرشادات الحقيقة المختلطة     | msmrw_guides                                |

**معلومات التبعية**

لا تعتمد حزمة أساس تطبيق الكتابة المزدوجة على الحزم الأخرى.

## <a name="dual-write-human-resources"></a>الموارد البشرية للكتابة المزدوجة

تحتوي حزمه الموارد البشرية للكتابة المزدوجة علي الحلول والخرائط المطلوبة لمزامنة بيانات الموارد البشرية. تحتوي على الحلول الثلاثة التالية.

| اسم فريد                | الاسم المعروض                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | عام HCM                               |
| msdyn_Dynamics365HCMMaps   | تعيينات كيانات Dynamics 365 Human Resources |
| msdyn_Dynamics365HCMAnchor | نقطة ارتساء Dynamics 365 Human Resources      |

الخرائط التالية متوفرة في هذه الحزمة.

| تطبيقات التمويل والعمليات | تطبيقات Customer Engagement         |
|-----------------------------|----------------------------------|
| الأصول العرقية              | cdm_ethnicorigins                |
| مهمة وظيفة التعويض   | cdm_jobfunctions                 |
| المناصب‬ V2                | cdm_jobpositions                 |
| المهام                        | cdm_jobs                         |
| نوع وظيفة التعويض       | cdm_jobtypes                     |
| أكواد اللغة              | cdm_languages                    |
| نوع المنصب               | cdm_positiontypes                |
| تعيينات العاملين بالمناصب | cdm_positionworkerassignmentmaps |
| حالة الخبرة              | cdm_veteranstatuses              |
| العامل                      | cdm_workers                      |
| التوظيف لكل شركة      | cdm_employments                  |

**معلومات التبعية**

تعتمد حزمه الموارد البشرية للكتابة المزدوجة علي حزمة أساس تطبيق الكتابة المزدوجة. لذلك، يجب عليك تثبيت حزمة أساس تطبيق الكتابة المزدوجة قبل تثبيت حزمة الموارد البشرية للكتابة المزدوجة.

## <a name="dual-write-supply-chain"></a>سلسلة توريد الكتابة المزدوجة

تحتوي حزمة سلسلة التوريد المزدوجة الكتابة على الحلول والخرائط المطلوبة لمزامنة بيانات Supply Chain Management. تحتوي على الحلول الثلاثة التالية.

| اسم فريد                                | الاسم المعروض                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | سلسلة توريد Dynamics 365 الموسعة                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | تعيينات الكيانات الموسعة في Dynamics 365 Supply Chain Management |
| msdyn_Dynamics365SupplyChainExtendedAnchor | نقطة الارتساء الموسعة في Dynamics 365 Supply Chain Management      |

الخرائط التالية متوفرة في هذه الحزمة.

| تطبيقات التمويل والعمليات                 | تطبيقات Customer Engagement                      |
|---------------------------------------------|-----------------------------------------------|
| الوحدات                                       | uoms                                          |
| رؤوس أوامر مبيعات CDS                     | salesorders                                   |
| بنود أمر مبيعات CDS                       | salesorderdetails                             |
| رأس عرض أسعار مبيعات CDS                  | الأسعار                                        |
| بنود عروض أسعار مبيعات CDS                   | quotedetails                                  |
| المنتجات المميزة الصادرة‬ CDS              | المنتجات                                      |
| مناطق المستودعات                             | msdyn_warehousezones                          |
| مجموعات مناطق المستودعات                       | msdyn_warehousezonegroups                     |
| سطور عمل المستودع                        | msdyn_warehouseworklines                      |
| رؤوس أعمال المستودع                      | msdyn_warehouseworkheaders                    |
| المستودعات                                  | msdyn_warehouses                              |
| ممر المخزون                             | msdyn_warehouseaisles                         |
| تحويلات الوحدات                            | msdyn_unitofmeasureconversions                |
| شروط التسليم                           | msdyn_termsofdeliveries                       |
| طرق التسليم                           | msdyn_shipvias                                |
| أنماط أصل المنتج                       | msdyn_sharedproductstyles                     |
| بنود فواتير المبيعات V2                      | invoicedetails                                |
| رؤوس فواتير المبيعات V2                    | الفواتير                                      |
| أحجام أصل المنتج                        | msdyn_sharedproductsizes                      |
| المنتجات الصادرة V2                        | msdyn_sharedproductdetails                    |
| تكوينات أصل المنتج               | msdyn_sharedproductconfigurations             |
| ألوان أصل المنتج                       | msdyn_sharedproductcolors                     |
| أكواد أصول أوامر المبيعات                    | msdyn_salesorderorigins                       |
| رأس إيصال استلام المنتج                      | msdyn_purchaseorderreceipts                   |
| سطر إيصال استلام المنتج                        | msdyn_purchaseorderreceiptproducts            |
| رؤوس أوامر الشراء V2                   | msdyn_purchaseorders                          |
| الكيان المحذوف المبدئي لبند أمر الشراء CDS | msdyn_purchaseorderproducts                   |
| كيان بند أمر شراء CDS              | msdyn_purchaseorderproducts                   |
| مجموعات أبعاد التعقب                   | msdyn_producttrackingdimensiongroups          |
| الأنماط                                      | msdyn_productstyles                           |
| مجموعات أبعاد التخزين                    | msdyn_productstoragedimensiongroups           |
| تحويلات الوحدات‬ الخاصة بالمنتج           | msdyn_productspecificunitofmeasureconversions |
| إعدادات الأوامر الافتراضية للمنتج V2           | msdyn_productspecificdefaultordersettings     |
| الأحجام                                       | msdyn_productsizes                            |
| مجموعات أبعاد المنتجات                    | msdyn_productdimensiongroups                  |
| إعدادات الأوامر الافتراضية                      | msdyn_productdefaultordersettings             |
| التكوينات                              | msdyn_productconfigurations                   |
| كل المنتجات                                | msdyn_globalproducts                          |
| الألوان                                      | msdyn_productcolors                           |
| أدوار التدرجات الهرمية لفئات المنتجات            | msdyn_productcategoryhierarchyroles           |
| التدرجات الهرمية لفئات المنتجات                | msdyn_productcategoryhierarchies              |
| تعيينات فئات المنتج                | msdyn_productcategoryassignments              |
| فئات المنتج                          | msdyn_productcategories                       |
| مواقع المستودع                         | msdyn_inventorylocations                      |
| مخزون CDS في                            | msdyn_inventoryonhandentries                  |
| فئات المنتج                          | msdyn_productcategories                       |
| مخزون CDS في                            | msdyn_inventoryonhandrequests                 |
| عرض الأكواد الشريطية المحددة لأرقام المنتجات           | msdyn_productbarcodes                         |
| بطاقة الولاء                                | msdyn_loyaltycards                            |
| نقاط مكافآت الولاء                       | msdyn_loyaltyrewardpoints                     |
| مجموعات أسعار للعملاء                       | msdyn_pricecustomergroups                     |
| المواقع                                       | msdyn_operationalsites                        |
| بنود عروض أسعار مبيعات CDS                   | quotedetails                                  |
| بنود أمر مبيعات CDS                       | salesorderdetails                             |

**معلومات التبعية**

تعتمد حزمة سلسلة توريد الكتابة المزدوجة على الحزم الثلاث التالية. لذلك، يجب عليك تثبيت هذه الحزم قبل تثبيت حزمة سلسلة توريد الكتابة المزدوجة.

- حزمة أساس تطبيق الكتابة المزدوجة
- حزمة Finance للكتابة المزدوجة
- حزمة الموارد البشرية للكتابة المزدوجة
- جداول الموارد البشرية العام في Dynamics 365

## <a name="dual-write-finance"></a>Finance للكتابة المزدوجة

تحتوي حزمة Finance للكتابة المزدوجة علي الحلول والخرائط المطلوبة لمزامنة بيانات Dynamics 365 Finance. تحتوي على الحلول الأربعة التالية.

| اسم فريد                            | الاسم المعروض                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | خرائط الكيانات في ‬‏‫Dynamics 365 Finance Extended |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | نقطة الارتساء في Dynamics 365 Finance Extended      |

الخرائط التالية متوفرة في هذه الحزمة.

| تطبيقات التمويل والعمليات             | تطبيقات Customer Engagement        |
|-----------------------------------------|---------------------------------|
| مجموعات ضرائب الخصم                  | msdyn_withholdingtaxgroups      |
| جهات اتصال CDS رقم V2 (العميل)              | جهات الاتصال                        |
| جهات اتصال CDS رقم V2 (المورد)                | جهات الاتصال                        |
| العملاء V3                            | جهات الاتصال                        |
| أكواد ضريبة الخصم                   | msdyn_withholdingtaxcodes       |
| موردو V2                              | msdyn_vendors                   |
| طريقة دفع المورّد                   | msdyn_vendorpaymentmethods      |
| مجموعات الموردين                           | msdyn_vendorgroups              |
| دليل الحسابات                       | msdyn_chartofaccountses         |
| مجموعات ترحيل دفتر أستاذ ضريبة المبيعات V2      | msdyn_taxpostinggroups          |
| مجموعة ضريبة المبيعات للأصناف                    | msdyn_taxitemgroups             |
| مجموعات ضريبة المبيعات                        | msdyn_taxgroups                 |
| كيان أكواد الإعفاء من ضريبة المبيعات CDS        | msdyn_taxexemptcodes            |
| مجموعات العملاء                         | msdyn_customergroups            |
| طريقة دفع العميل                 | msdyn_customerpaymentmethods    |
| الأبعاد المالية                    | msdyn_dimensionattributes       |
| هيئات ضريبة المبيعات                   | msdyn_taxauthorities            |
| تنسيق البعد المالي              | msdyn_financialdimensionformats |
| فترة التقويم المالي                  | msdyn_fiscalcalendarperiods     |
| كيان تكامل التقويم المالي      | msdyn_fiscalcalendars           |
| كيان تكامل سنة التقويم المالي | msdyn_fiscalcalendaryears       |
| شروط الدفع                        | msdyn_paymentterms              |
| جدول الدفع                        | msdyn_paymentschedules          |
| بنود جدول الدفع                  | msdyn_paymentschedulelines      |
| أيام الدفع CDS                        | msdyn_paymentdays               |
| بنود يوم الدفع CDS V2                | msdyn_paymentdaylines           |
| الحساب الرئيسي                            | msdyn_mainaccounts              |
| فئات الحساب الرئيسية                 | msdyn_mainaccountcategories     |
| دفتر الأستاذ                                  | msdyn_ledgers                   |
| العملاء V3                            | الحسابات                        |

**معلومات التبعية**

تعتمد حزمه Finance للكتابة المزدوجة علي حزمة أساس تطبيق الكتابة المزدوجة. لذلك، يجب عليك تثبيت حزمة أساس تطبيق الكتابة المزدوجة قبل تثبيت حزمة Finance للكتابة المزدوجة.

## <a name="dual-write-notes"></a>ملاحظات حول الكتابة المزدوجة

تحتوي حزمه الملاحظات حول الكتابة المزدوجة علي الحلول والخرائط المطلوبة لمزامنة بيانات ملاحظة أو تعليق توضيحي. تحتوي على الحلول الأربعة التالية.

| اسم فريد                  | الاسم المعروض                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | ملاحظات حول Dynamics 365             |
| Dynamics365NotesExtended     | تم توسيع ملاحظات Dynamics 365    |
| msdyn_Dynamics365NotesMaps   | تعيينات كيانات ملاحظات Dynamics 365 |
| msdyn_Dynamics365NotesAnchor | نقطة ارتساء ملاحظات Dynamics 365      |

الخرائط التالية متوفرة في هذه الحزمة.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| مرفقات مستند رأس أمر المبيعات    | تعليقات توضيحية         |
| مرفقات العملاء                       | تعليقات توضيحية         |
| مرفقات مستندات المورّد                | تعليقات توضيحية         |
| مرفقات مستند رأس أمر الشراء | تعليقات توضيحية         |

**معلومات التبعية**

تعتمد حزمة ملاحظات الكتابة المزدوجة على الحزمتين التاليتين. لذلك، يجب عليك تثبيت هذه الحزم قبل تثبيت حزمة ملاحظات الكتابة المزدوجة.

- حزمة أساس تطبيق الكتابة المزدوجة
- حزمة Finance للكتابة المزدوجة

## <a name="dual-write-asset-management"></a>إدارة أصول الكتابة المزدوجة

تحتوي حزمة إدارة الأصول المزدوجة الكتابة على الحلول والخرائط المطلوبة لمزامنة بيانات الأصول من Supply Chain Management أو Dynamics 365 Field Service. تحتوي على الحلول الأربعة التالية.

| اسم فريد                          | الاسم المعروض                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | إدارة أصول Dynamics 365             |
| Dynamics365AssetManagementApp        | تطبيق إدارة أصول Dynamics 365          |
| msdyn_DualWriteAssetManagementMaps   | تعيينات كيانات إدارة أصول Dynamics 365 |
| msdyn_DualWriteAssetManagementAnchor | نقطة ارتساء إدارة أصول Dynamics 365      |

الخرائط التالية متوفرة في هذه الحزمة.

| تطبيقات التمويل والعمليات                           | تطبيقات Customer Engagement                |
|-------------------------------------------------------|-----------------------------------------|
| ضمان إدارة الأصول                             | msdyn_warranties                        |
| نماذج إدارة الأصول                               | msdyn_models                            |
| الشركات المصنعة في إدارة الأصول                        | msdyn_manufacturers                     |
| أنواع مواقع العمل في إدارة الأصول            | msdyn_functionallocationtypes           |
| مواقع العمل في إدارة الأصول                 | msdyn_functionallocations               |
| حالات دورة حياة موقع العمل في إدارة الأصول | msdyn_functionallocationlifecyclestates |
| نماذج دورة حياة موقع العمل في إدارة الأصول | msdyn_functionallocationlifecyclemodels |
| أصول إدارة الأصول                               | msdyn_customerassets                    |
| أنواع الأصول في إدارة الأصول                          | msdyn_customerassetcategories           |
| حالات دورة حياة الأصول في إدارة الأصول               | msdyn_assetlifecyclestates              |
| نماذج دورة حياة الأصول في إدارة الأصول               | msdyn_assetlifecyclemodels              |

**معلومات التبعية**

تعتمد حزمه إدارة أصول الكتابة المزدوجة علي حزمة أساس تطبيق الكتابة المزدوجة. لذلك، يجب عليك تثبيت حزمة أساس تطبيق الكتابة المزدوجة قبل تثبيت حزمة إدارة أصول الكتابة المزدوجة.

## <a name="packages-required-for-project-operations"></a>الحزم المطلوبة لـ Project Operations
يعتمد Project Operations على الحزم التالية. لذلك، يجب عليك تثبيت هذه الحزم قبل تثبيت Project Operations.

- حزمة أساس تطبيق الكتابة المزدوجة
- حزمة Finance للكتابة المزدوجة
- حزمة سلسلة توريد الكتابة المزدوجة
- حزمة إدارة أصول الكتابة المزدوجة
- حزمة الموارد البشرية للكتابة المزدوجة

## <a name="dual-write-party-and-global-address-book-solutions"></a>حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي

تحتوي حزمة حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي على الحلول والخرائط التالية المطلوبة لمزامنة بيانات الطرف ودفتر العناوين العمومي. 

| اسم فريد                       | الاسم المعروض                            |
|-----------------------------------|-----------------------------------------|
| الطرف                             | الطرف                                   |
| Dynamics365GABExtended            | دفتر العناوين الموسع في Dynamics 365               |
| Dynamics365GABDualWriteEntityMaps | خرائط كيانات الكتابة المزدوجة في دفتر العناوين العمومي في Dynamics 365 |
| Dynamics365GABParty_Anchor        | الطرف ودفتر العناوين العمومي في Dynamics 365              |

الخرائط التالية متوفرة في هذه الحزمة.

| تطبيقات التمويل والعمليات | تطبيقات Customer Engagement | 
|-----------------------------|--------------------------|
| أطراف CDS | msdyn_parties | 
| مواقع العناوين البريدية لـ CDS | msdyn_postaladdresscollections | 
| سجل العناوين البريدية لـ CDS الإصدار V2 | msdyn_postaladdresses | 
| مواقع العناوين البريدية لطرف CDS | msdyn_partypostaladdresses | 
| جهات اتصال الأطراف V3 | msdyn_partyelectronicaddresses | 
| العملاء V3 | الحسابات | 
| العملاء V3 | جهات الاتصال | 
| موردو V2 | msdyn_vendors | 
| ألقاب جهات الاتصال | msdyn_salescontactpersontitles | 
| الختامات الإطرائية | msdyn_complimentaryclosings | 
| التحيات | msdyn_salutations | 
| أدوار صنع القرار | msdyn_decisionmakingroles | 
| مهام وظائف التوظيف | msdyn_employmentjobfunctions | 
| مستويات الولاء | msdyn_loyaltylevels | 
| أنواع الخصائص الشخصية | msdyn_personalcharactertypes | 
| جهات الاتصال V2 | msdyn_contactforparties | 
| رأس عرض أسعار مبيعات CDS | الأسعار | 
| رؤوس أوامر مبيعات CDS | salesorders | 
| رؤوس فواتير المبيعات V2 | الفواتير | 
| أدوار عناوين CDS | msdyn_addressroles |

**معلومات التبعية**

تعتمد حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي على الحزم الثلاث التالية. لذلك، يجب عليك تثبيت هذه الحزم قبل تثبيت حزمة حلول الكتابة المزدوجة للطرف ودفتر العناوين العمومي‬‏‫.

- حزمة أساس تطبيق الكتابة المزدوجة
- حزمة Finance للكتابة المزدوجة
- حزمة سلسلة توريد الكتابة المزدوجة

