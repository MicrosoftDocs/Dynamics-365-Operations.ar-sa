---
title: كيانات حركات التكلفة
description: يوفر هذا المقال معلومات حول كيانات حركة التكلفة، والتي تتيح تقسيم قيمة التكلفة بين محتويات منطقة التكلفة من خلال تحديد طريقة التوزيع.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166792"
---
# <a name="cost-transaction-entities"></a>كيانات حركات التكاليف

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>التوزيع

تتيح تكلفة الوصول إلى قيمة التكلفة أن يتم تقسيمها بين محتويات منطقة التكلفة (الرحلة، حاوية الشحن، وما إلى ذلك) من خلال اختيار طريقة التوزيع. يتم تعيين طريقة التوزيع كجزء من تكوين التكاليف التلقائية التي تستند إلى قواعد العمل. يتم سحبها كجزء من التكلفة عند إنشاء بند رحلة.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>تكوين مخطط التقسيم للاستخدام مع كيانات البيانات

عندما يتم إنشاء تكلفة من مصدر خارجي مثل وكيل الشحن، لا يمكن لهذا المصدر الخارجي تحديد الطريقة المفضلة لتقسيم قيمة التكلفة. يحدد مخطط التقسيم طريقة التقسيم الافتراضية لكل رمز نوع تكلفة. يتم الوصول إلى جدول تعيين التوزيع من صفحة **مخطط التوزيع** في Microsoft Dynamics 365 Supply Chain Management (**التكلفة شاملة التفريغ \> إعداد التكاليف \> تعيين التوزيع**).

إذا تم تحديد مجموعة التعيين، وتم إنشاء تكلفة تطابق رمز نوع التكلفة باستخدام كيان حركة التكلفة، فسيتم استخدام طريقة التقسيم المعينة بدلاً من أي قيمة تم توفيرها للكيان.

في حالة عدم وجود قيمة في جدول التعيين، ولكن تم توفير قيمة للكيان، فسيتم استخدام القيمة المقدمة.

في حالة عدم وجود قيمة في جدول التعيين أو السجل الذي تم إرساله إلى الكيان، سيفشل الإنشاء.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>تعيين التوزيع (ITMApportionmentMapping)

ينشئ كيان تعيين التقسيم (`ITMApportionmentMapping`) علاقات تعيين التقسيم ويمكّن المستخدمين من إنشاء السجلات أو تحديثها.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| أسلوب التوزيع‬ | ITMApportionmentMapping.ApportionmentMethod | الفترة | لا | لا |
| كود نوع التكلفة | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **نعم** | لا |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>تكاليف الرحلات (ITMCostTransVoyageEntity)

ينشئ كيان تكلفة الرحلة (`ITMCostTransVoyageEntity`) حركات تكلفة الرحلة التي يتم تطبيقها على مستوى الرحلة. أثناء عملية الاستيراد، يستخدم النظام قيم **الفئة** و **طريقة التوزيع** المضمنة في الكيان لتحديد كيفية تقسيم قيمة التكلفة عبر محتويات الرحلة.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| أسلوب التوزيع‬ | ITMCostTrans.ApportionmentMethod | الفترة | لا | لا |
| قيمة التكلفة | ITMCostTrans.CostValue | Numeric(32, 6) | لا | لا |
| عملة | ITMCostTrans.CurrencyCode | Nvarchar(3) | لا | **نعم** |
| رقم البند | ITMCostTrans.LineNum | Numeric(32, 16) | **نعم** | لا |
| نوع التكلفة المرتبطة | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | لا | لا |
| الحد الأدنى للتكلفة | ITMCostTrans.MinCostAmount | Numeric(32, 6) | لا | لا |
| ‏‏الفئة | ITMCostTrans.ShipCostCategory | الفترة | لا | لا |
| كود نوع التكلفة | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | لا | لا |
| الشركة | ITMCostTrans.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| الرحلة البحرية | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| مجموعة ضريبة المبيعات للأصناف | ITMCostTrans.TaxItemGroup | Nvarchar(10) | لا | لا |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>تكاليف حاوية الشحن (ITMCostTransShippingContainerEntity)

ينشئ كيان تكلفة حاوية الشحن (`ITMCostTransShippingContainerEntity`) تكاليف حاوية الشحن التي يتم تطبيقها على مستوى حاوية الشحن. أثناء عملية الاستيراد، يستخدم النظام قيم **الفئة** و **طريقة التوزيع** المضمنة في الكيان لتحديد كيفية تقسيم قيمة التكلفة عبر محتويات حاوية الشحن.

حقول **التجميع**، و **الاتجاه**، و **الاتجاه المرتبط** خاصة بالسجلات حيث تكون قيمة **منطقة التكلفة** هي *حاوية الشحن*. لذلك، فهي غير موجودة في كيانات البيانات لمناطق التكلفة الأخرى.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| تجميع | ITMCostTrans.AggregatedCost | الفترة | لا | لا |
| أسلوب التوزيع‬ | ITMCostTrans.ApportionmentMethod | الفترة | لا | لا |
| قيمة التكلفة | ITMCostTrans.CostValue | Numeric(32, 6) | لا | لا |
| عملة | ITMCostTrans.CurrencyCode | Nvarchar(3) | لا | **نعم** |
| رقم البند | ITMCostTrans.LineNum | Numeric(32, 16) | **نعم** | لا |
| نوع التكلفة المرتبطة | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | لا | لا |
| شُعبة مرتبطة | ITMCostTrans.LinkLegId | Nvarchar(20) | لا | لا |
| الحد الأدنى للتكلفة | ITMCostTrans.MinCostAmount | Numeric(32, 6) | لا | لا |
| حاوية الشحن | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| ‏‏الفئة | ITMCostTrans.ShipCostCategory | الفترة | لا | لا |
| كود نوع التكلفة | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | لا | لا |
| الشركة | ITMCostTrans.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| الرحلة البحرية | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| الشُعبة | ITMCostTrans.ShipLegId | Nvarchar(20) | لا | لا |
| مجموعة ضريبة المبيعات للأصناف | ITMCostTrans.TaxItemGroup | Nvarchar(10) | لا | لا |

## <a name="folio-costs-itmcosttransfolioentity"></a>تكاليف حافظات الأوراق (ITMCostTransFolioEntity)

ينشئ كيان تكلفة حافظة الأوراق (`ITMCostTransFolioEntity`) سجلات معاملات التكلفة التي تنطبق على مستوى السجل. أثناء عملية الاستيراد، يستخدم النظام قيم **الفئة** و **طريقة التوزيع** المضمنة في الكيان لتحديد كيفية تقسيم قيمة التكلفة عبر محتويات كل حافظة ورق.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| أسلوب التوزيع‬ | ITMCostTrans.ApportionmentMethod | الفترة | لا | لا |
| قيمة التكلفة | ITMCostTrans.CostValue | Numeric(32, 6) | لا | لا |
| عملة | ITMCostTrans.CurrencyCode | Nvarchar(3) | لا | **نعم** |
| رقم البند | ITMCostTrans.LineNum | Numeric(32, 16) | **نعم** | لا |
| نوع التكلفة المرتبطة | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | لا | لا |
| الحد الأدنى للتكلفة | ITMCostTrans.MinCostAmount | Numeric(32, 6) | لا | لا |
| ‏‏الفئة | ITMCostTrans.ShipCostCategory | الفترة | لا | لا |
| كود نوع التكلفة | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | لا | لا |
| الشركة | ITMCostTrans.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| حافظة الأوراق | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| مجموعة ضريبة المبيعات للأصناف | ITMCostTrans.TaxItemGroup | Nvarchar(10) | لا | لا |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>تكاليف أوامر الشراء (ITMCostTransPurchaseEntity)

ينشئ كيان تكلفة أمر الشراء (`ITMCostTransPurchaseEntity`) حركات التكلفة التي تنطبق على رأس أمر المشتري. أثناء عملية الاستيراد، يستخدم النظام قيم **الفئة** و **طريقة التوزيع** المضمنة في الكيان لتحديد كيفية تقسيم قيمة التكلفة عبر محتويات كل حافظة ورق.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| أسلوب التوزيع‬ | ITMCostTrans.ApportionmentMethod | الفترة | لا | لا |
| قيمة التكلفة | ITMCostTrans.CostValue | Numeric(32, 6) | لا | لا |
| عملة | ITMCostTrans.CurrencyCode | Nvarchar(3) | لا | **نعم** |
| رقم البند | ITMCostTrans.LineNum | Numeric(32, 16) | **نعم** | لا |
| نوع التكلفة المرتبطة | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | لا | لا |
| الحد الأدنى للتكلفة | ITMCostTrans.MinCostAmount | Numeric(32, 6) | لا | لا |
| أمر شراء | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| ‏‏الفئة | ITMCostTrans.ShipCostCategory | الفترة | لا | لا |
| كود نوع التكلفة | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | لا | لا |
| الشركة | ITMCostTrans.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| مجموعة ضريبة المبيعات للأصناف | ITMCostTrans.TaxItemGroup | Nvarchar(10) | لا | لا |

## <a name="item-costs-itmcosttransitementity"></a>تكاليف الأصناف (ITMCostTransItemEntity)

ينشئ كيان تكلفة الصنف (`ITMCostTransItemEntity`) حركات التكلفة التي تنطبق على مستوى الصنف. هذا الكيان خاص بالعناصر الموجودة في سطور أوامر الشراء. يتم تطبيق قيمة التكلفة بالكامل على البند.

حقول **مبلغ التعديل** و **تعديل القيمة** خاصة بمناطق تكلفة مستوى البند. لذلك، فهي غير موجودة في كيانات البيانات لمناطق التكلفة الأخرى.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| مبلغ التسوية | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | لا | لا |
| قيمة التكلفة | ITMCostTrans.CostValue | Numeric(32, 6) | لا | لا |
| عملة | ITMCostTrans.CurrencyCode | Nvarchar(3) | لا | **نعم** |
| رقم البند | ITMCostTrans.LineNum | Numeric(32, 16) | **نعم** | لا |
| نوع التكلفة المرتبطة | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | لا | لا |
| الحد الأدنى للتكلفة | ITMCostTrans.MinCostAmount | Numeric(32, 6) | لا | لا |
| أمر شراء | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| رقم بند أمر الشراء | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| ‏‏الفئة | ITMCostTrans.ShipCostCategory | الفترة | لا | لا |
| كود نوع التكلفة | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | لا | لا |
| الشركة | ITMCostTrans.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| مجموعة ضريبة المبيعات للأصناف | ITMCostTrans.TaxItemGroup | Nvarchar(10) | لا | لا |
| تسوية القيمة | ITMCostTrans.ValueAdjustmentMethod | الفترة | لا | لا |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>تكاليف بنود التحويل (ITMCostTransTransferLineEntity)

ينشئ كيان تكلفة بند النقل (`ITMCostTransTransferLineEntity`) حركات التكلفة التي تنطبق على مستوى بند أمر التحويل. يتم تطبيق قيمة هذه التكاليف بالكامل على بند أمر التحويل.

حقول **مبلغ التعديل** و **تعديل القيمة** خاصة بمناطق تكلفة مستوى البند. لذلك، فهي غير موجودة في كيانات البيانات لمناطق التكلفة الأخرى.

| Name | التعيين | نوع البيانات | مفتاح | إلزامي |
|---|---|---|---|---|
| مبلغ التسوية | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | لا | لا |
| قيمة التكلفة | ITMCostTrans.CostValue | Numeric(32, 6) | لا | لا |
| عملة | ITMCostTrans.CurrencyCode | Nvarchar(3) | لا | **نعم** |
| رقم البند | ITMCostTrans.LineNum | Numeric(32, 16) | **نعم** | لا |
| نوع التكلفة المرتبطة | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | لا | لا |
| الحد الأدنى للتكلفة | ITMCostTrans.MinCostAmount | Numeric(32, 6) | لا | لا |
| ‏‏الفئة | ITMCostTrans.ShipCostCategory | الفترة | لا | لا |
| كود نوع التكلفة | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | لا | لا |
| الشركة | ITMCostTrans.ShipDataArea | Nvarchar(4) | لا | **نعم** |
| أمر التحويل | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| رقم بند أمر التحويل | ITMCostTrans.TransRecId | Nvarchar(20) | **نعم** | لا |
| مجموعة ضريبة المبيعات للأصناف | ITMCostTrans.TaxItemGroup | Nvarchar(10) | لا | لا |
| تسوية القيمة | ITMCostTrans.ValueAdjustmentMethod | الفترة | لا | لا |

### <a name="transaction-table"></a>جدول الحركات

يقترن سجل حركة التكلفة بمنطقة التكلفة من خلال تعيين رقم جدول الحركة (`TransTableId`). عندما تكون أرقام تعريف الجدول المحددة مطلوبة، يتم تقسيم الكيانات بناءً على هذه القيم، بحيث يوجد كيان لكل منطقة تكلفة.

قيمة جدول الحركات (`TransTableId`) ضمنية في اختيار كيان حركة التكلفة.

### <a name="calculated-fields"></a>الحقول المحسوبة

الحقول التالية غير متاحة للإدراج أو التحديث عند استخدام كيان لحركة التكلفة، لأنه يتم تعيين هذه الحقول فقط عند اتخاذ إجراءات معينة ضد سجل الرحلة:

- **التكلفة المقدرة** – يتم تعيين هذا الحقل عند ترحيل فاتورة للرحلة (أمر الشراء) أو عند استلام تحويل.
- **عملة التكلفة المقدرة** – يتم تعيين هذا الحقل عند ترحيل فاتورة للرحلة (أمر الشراء) أو عند استلام تحويل.
- **التكلفة الفعلية** – يتم تعيين هذا الحقل عند ترحيل فاتورة البائع. إنها مرتبطة بالتكلفة.

### <a name="find-auto-costs"></a>البحث عن التكاليف التلقائية

يوفر الزر **البحث عن تكاليف السيارات** المتاح لكل منطقة تكلفة (الرحلة وحاوية الشحن وما إلى ذلك) طريقة لتحديث حركات التكلفة لمنطقة التكلفة تلك من المعلومات الواردة في جداول التكوين. عند تحديد الزر لمنطقة التكلفة، يمسح النظام التكاليف الحالية لمنطقة التكلفة هذه وينشئ سجلات جديدة، بناءً على التكوين الحالي لجداول إعداد التكلفة التلقائية.

يتم تمييز سجلات حركات التكلفة التي تم إنشاؤها باستخدام كيان بيانات على أنها مستوردة. لا يتم حذف هذه السجلات عند تحديد **البحث عن تكاليف السيارات**، لأنه لن يتم إعادة إنشائها من جداول إعداد تكلفة السيارات. ومع ذلك، لا يزال من الممكن حذف سجل حركة التكلفة الذي تم تمييزه على أنه مستورد.

### <a name="linked-fields"></a>الحقول المرتبطة

يمكن إقران كل حركة تكلفة بسجل آخر في نفس منطقة التكلفة. تم إنشاء هذا الاقتران من خلال حقل **نوع التكلفة المرتبطة**. يتيح حساب قيمة التكلفة كنسبة مئوية من تكلفة أخرى.

لا يمكن التحقق من صحة الحقل **نوع التكلفة المرتبطة** إلا إذا تمت معالجة السجل الذي تتم الإشارة إليه أولاً، أو إذا كان بالفعل موجود في الجدول. ينطبق نفس المطلب على حقل **الاتجاه المرتبط** المستخدم للتكاليف في منطقة تكلفة حاوية الشحن فقط.
