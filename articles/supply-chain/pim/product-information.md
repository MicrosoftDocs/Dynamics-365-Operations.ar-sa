---
title: نظرة عامة على معلومات المنتجات
description: يوفر هذا الموضوع معلومات حول إدارة معلومات المنتج. تعمل إدارة معلومات المنتج مع تعريف منتج مشترك وتصنيفه ومعرّفاته عبر كافة الكيانات القانونية، وكذلك التكوينات الخاصة بمنتج، لاحتوائها في العمليات التجارية.
author: t-benebo
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bee9b122e916b62c88bdb9299e823d58bf5bfa25e3b401638145fc431c98df53
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766016"
---
# <a name="product-information-overview"></a>نظرة عامة على معلومات المنتجات

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوفر هذا الموضوع معلومات حول إدارة معلومات المنتج. تعمل إدارة معلومات المنتج مع تعريف منتج مشترك وتصنيفه ومعرّفاته عبر كافة الكيانات القانونية، وكذلك التكوينات الخاصة بمنتج، لاحتوائها في العمليات التجارية. 

تُعتبر معلومات المنتج بمثابة العمود الفقري لتطبيقات سلسلة التوريد والتجارة عبر كل الصناعات. وهي تشير إلى العمليات والتقنيات التي تركز على إدارة المعلومات الخاصة بالمنتجات بطريقة مركزية (على سبيل المثال، عبر سلاسل التوريد). من الضروري أن يتم استخدام تعريفات المنتجات المشتركة ووثائقها وسماتها ومعرّفاتها. في مختلف وحدات حل الأعمال، تكون المعلومات والتكوينات الخاصة بالمنتج مطلوبة لإدارة عمليات الأعمال ذات الصلة بمنتجات أو عائلات منتجات أو فئات منتجات معينة.

## <a name="product-definition"></a>تعريف المنتج

يتحدد المنتج بشكل أساسي بواسطة رقمه واسمه ووصفه. ومع ذلك، هناك بيانات أخرى مطلوبة أيضًا لوصف المنتج أو الخدمة:

- نوع المنتج: صنف أو خدمة
- النوع الفرعي للمنتج: منتجات مميزة أو أصول منتجات
- تعريف نموذج متغير المنتج:

     - أبعاد المنتج ومجموعات الأبعاد
     - كود nomenclature للمنتج
     - نماذج تكوين المنتجات

- اقتران المنتج بفئة واحدة أو أكثر
- تعريف سمات المنتجات والفئات
- صور المنتج
- مرفقات
- وحدات القياس والتحويلات ذات الصلة
- ترجمات لكافة الأسماء والأوصاف

## <a name="distribution-export-and-import-of-product-data"></a>توزيع بيانات المنتج وتصديرها واستيرادها

يمكن إنشاء تعريف المنتج في Supply Chain Management. ويمكن أيضًا استيراده من إدارة دورة حياة المنتج (PLM) أو إدارة بيانات المنتج (PDM) أو أنظمة إدارة معلومات المنتج (PIM). عند استخدام أكثر من مثيل واحد من Supply Chain Management، يتم استخدام مثيل عادةً كأصل بيانات المنتج لكل المثيلات الأخرى. هناك مجموعة كبيرة من كيانات البيانات التي تدعم هذا المنتج، وهي تمكّن تصدير واستيراد بيانات تعريف المنتج من مثيل إلى آخر.

لدعم توزيع بيانات المنتج على عدد كبير من المثيلات، يسمح لك Supply Chain Management باستخدام Microsoft Dataverse. يمكن تصدير تعريفات المنتج من مثيل Supply Chain Management إلى Microsoft Dataverse. بعد ذلك، يمكن استخدام تعريفات المنتج لتزويد تطبيقات الأعمال الأخرى، مثل Dynamics 365 Sales، ببيانات المنتج.

لاحظ أنه في المؤسسات الديناميكية ومنخفضة التكلفة، تتغير معلومات المنتج كل يوم. وبالتالي، يعتبر الحفاظ على بيانات المنتج الفعلية والدقيقة عملية أعمال دقيقة بحد ذاتها.

## <a name="product-masters-and-product-variants"></a>أصول ومتغيرات المنتجات

في عالم يتميز بالسرعة والمرونة، حيث يجب أن تتكيف المنتجات بسرعة مع متطلبات العملاء، تحدد تعريفات المنتج مجموعة من المنتجات بدلاً من منتجات مميزة. في Supply Chain Management، تعرف هذه المنتجات العامة باسم *أصول المنتجات*. تتضمن أصول المنتجات التعريف والقواعد التي تحدد كيفية وصف المنتجات المميزة بالإضافة إلى سلوكها عمليات الأعمال. استنادًا إلى هذه التعريفات، يمكن إنشاء منتجات مميزة. تعرف هذه المنتجات مميزة باسم *متغيرات المنتجات*.

يقترن أصل المنتج بمجموعة أبعاد المنتج وبتقنية التكوين لتحديد قواعد العمل. تعتبر أبعاد المنتج (اللون والحجم والنمط والتكوين) بمثابة مجموعة معينة من السمات التي يتم استخدامها في التطبيق لتعريف وتعقب سلوكيات محددة للمنتجات ذات الصلة. باستطاعة هذه الأبعاد أن تساعد المستخدمين أيضًا في البحث عن المنتجات وتحديدها.

## <a name="configuration-technologies"></a>تقنيات التكوين

يمكنك الاختيار من ضمن ثلاث تقنيات تكوين:

- يتم تعريف المتغيرات المعرفة مسبقًا بواسطة أبعاد المنتجات المحددة مسبقًا. ويتضمن تعريف المتغير تعريف مجموعة أبعاد معينة صالحة، مثل اللون والحجم. وتنتج كل مجموعة متغير منتج مميز.
- يُستخدم عادة التكوين المستند إلى بُعد في سيناريوهات التصنيع ويسمح لك باستخدام بُعد التكوين في تعريف قائمة مكونات الصنف (BOM). بعد تحديد تكوين معين، يستخدم النظام المجموعة الفرعية لبنود قائمة مكونات الصنف الصالحة لهذا التكوين للإنتاج والتخطيط. يُعرف هذا المفهوم أيضًا باسم *قائمة مكونات الصنف العامة*، نظرًا استخدام قائمة مكونات صنف واحدة مشتركة لكافة تكوينات منتج ما.
- يستخدم التكوين المستند إلى قيد نموذج تكوين منتج لوصف كافة السمات والمكونات المحتملة المطلوبة لوصف كافة المتغيرات الممكنة لأحد المنتجات في نموذج واحد. يمكن وصف قيود مجموعات السمات من خلال تعابير عادية أو قيود تستند إلى جدول. تصبح نماذج التكوين وأدوات التكوين أكثر أهمية في إدارة معلومات المنتج ويتم استخدامها عبر كل الصناعات.

عند التخطط لتنفيذ Supply Chain Management، من الضروري أن تختار تقنية التكوين الصحيحة لعملية أعمال. يتعذر تحويل منتج من نموذج إلى آخر بعد التنفيذ.

## <a name="product-variant-model-definition-workspace"></a>مساحة عمل تعريف نموذج متغير المنتج

توفر لك مساحة العمل **تعريف نموذج متغير المنتج** نظرة عامة على أصول المنتجات. وهي تبين أيضًا حالة إصدار الأصول والمتغيرات ذات الصلة لكيانات قانونية محددة.

## <a name="released-products"></a>المنتجات الصادرة

تعرف المنتجات التي تم إصدارها لكيان قانوني محدد باسم *المنتجات الصادرة‬*. ويمكن إصدار المنتجات بشكل مجمع لكيان قانوني واحد أو العديد من الكيانات القانونية مرة واحدة. نظرًا لاحتمال وجود حاجة إلى إضافة العديد من الخصائص والسمات الخاصة بالمنتجات لكل كيان قانوني، تسمح لك مساحة عمل **صيانة المنتج الذي تم إصداره‬** بمراقبة وإكمال المنتجات التي تم إصدارها حديثًا في كل كيان قانوني، أو في المؤسسات الفرعية لكيان قانوني.

### <a name="released-product-maintenance-workspace"></a>مساحة عمل صيانة المنتج الذي تم إصداره‬

يمكنك تكوين مساحة عمل **صيانة المنتج الذي تم إصداره‬** من عنصر قائمة **تكوين مساحة العمل الخاصة بي**. حدد تدرجًا هرميًا للفئات وفئة لتصفية مساحة العمل باستخدامها. لضبط بيانات المنتج ذات الصلة في مساحة العمل، يمكنك أيضًا تعريف، بالأيام، الحدود الزمنية لكل من **المنتجات التي تم إصدارها مؤخرًا‬** و **المنتجات التي تم إصدارها المتوقفة‬**.

تتكون مساحة العمل من ملخص لوحتين وقائمتين. تبين قائمة **الحالات المفتوحة‬** حالات تغييرات المنتج التي لديها منتجات في التدرج الهرمي لفئات المنتج لم تكتمل وتغلق. تقين قائمة **المُصدر مؤخرًا‬** المنتجات التي تم إصدارها في إطار الحد الزمني الذي تم تعيينه في تكوين مساحة العمل. لكل صنف في القائمة، يتم تشغيل عملية التحقق من الصحة، ويتم عرض حالة التحقق من الصحة. قد تشير هذه الحالة إلى عدم إكمال التكوينات المطلوبة للكيان القانوني. من القائمة، يمكنك الوصول مباشرة إلى صفحة **تفاصيل المنتج الذي تم إصداره‬** و **صيانة سمات المنتج** و **صيانة فئات المنتج** و **إعدادات الأمر الافتراضية** و **ترجمة للنص** لإكمال التكوين المطلوب للمنتج.

### <a name="manually-creating-a-new-released-product"></a>إنشاء منتج صادر جديد يدويًا

يمكنك إنشاء منتج صادر يدويًا في جولة واحدة، استنادًا إلى عمليات أعمال المؤسسة الإضافة إلى أية قواعد حول ما إذا كان يجب استخدام هذه الوظيفة. تنشئ هذه الوظيفة منتجًا جديدًا وتصدره تلقائيًا في الكيان القانوني الحالي. لإنشاء منتج جديد، انقر فوق **المنتجات الصادرة** في مساحة عمل **صيانة المنتج الذي تم إصداره‬** أو في صفحة قائمة **المنتجات الصادرة**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]