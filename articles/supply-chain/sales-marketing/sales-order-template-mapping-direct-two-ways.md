---
title: مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لتشغيل مزامنة أوامر المبيعات مباشرةً بين Dynamics 365 Sales و Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d30ead63bfba5dc198bd46dfaffe444dde723baa
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261011"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لتشغيل مزامنة أوامر المبيعات مباشرةً بين Dynamics 365 Sales و Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://preview.admin.powerapps.com/dataintegration) . حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة أوامر المبيعات مباشرةً بين Sales وSupply Chain Management:

- **أسماء القوالب في تكامل البيانات:** 

    - أوامر المبيعات (Sales إلى Supply Chain Management) - مباشر
    - أوامر المبيعات (Supply Chain Management إلى Sales) - مباشر

- **أسماء المهام في مشروع تكامل البيانات:**

    - OrderHeader
    - OrderLine

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة رؤوس وبنود فواتير المبيعات.

- المنتجات (من Supply Chain Management إلى Sales) - مباشر
- الحسابات (من Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)
- جهات الاتصال إلى العملاء (من Sales إلى Supply Chain Management) - مباشر (إذا ما تم استخدامه)

## <a name="entity-set"></a>مجموعة الكيانات

| Supply Chain Management  | ال‏‏مبيعات             |
|-------------------------|-------------------|
| Dataverse رؤوس أوامر المبيعات V2 | SalesOrders       |
| Dataverse بنود أمر مبيعات   | SalesOrderDetails |

## <a name="entity-flow"></a>تدفق الكيان

‏‫يتم إنشاء أوامر المبيعات في Sales وتتم مزامنتها إلى Supply Chain Management عند تشغيل **تشغيل المشروع** لأحد المشاريع استنادًا إلى القالب **أوامر المبيعات (Sales إلى Supply Chain Management) - مباشر**. لا يمكنك تنشيط ومزامنة الأوامر من Sales إلا إذا كانت جميع **منتجات الأوامر** تتكون من المنتجات التي تتم المحافظة عليها خارجيًا. لذلك، قد لا يكون هناك أي منتجات مدونة. بعد تنشيط الأمر، يصبح أمر المبيعات للقراءة فقط في واجهة المستخدم (UI). عند هذه النقطة، يتم إجراء التحديثات من Supply Chain Management. بعد حصول أمر المبيعات على الحالة **مؤكد**، يمكن استخدام المشروع الذي يستند القالب **أوامر المبيعات (Supply Chain Management إلى Sales) - مباشر** لمزامنة التحديثات أو حالة الاستيفاء من Supply Chain Management إلى Sales.

لا يتعين عليك إنشاء الأوامر في Sales. يمكنك إنشاء أوامر المبيعات الجديدة في Supply Chain Management بدلاً من ذلك. بعد حصول أمر المبيعات على الحالة **مؤكد**، تتم مزامنته إلى Sales كما هو موضح في الفقرة السابقة.

في Supply Chain Management، تساعد عوامل التصفية الموجودة في القالب على ضمان عدم تضمين غير أوامر المبيعات ذات الصلة في المزامنة:

- في أمر المبيعات، يجب إنشاء كل من عميل الأمر وعميل الفوترة من Sales ليتم تضمينه في المزامنة. في Supply Chain Management، يتم استخدام الأعمدة **OrderingCustomerIsExternallyMaintained** و **InvoiceCustomerIsExternallyMaintained** لتصفية أوامر المبيعات من جداول البيانات.
- يجب تأكيد أمر المبيعات في Supply Chain Management. لا تتم مزامنة غير أوامر المبيعات المؤكدة أو أوامر المبيعات التي لها حالة معالجة أعلى، مثل الحالة **مشحون** أو **مفوتر** إلى Sales.
- بعد إنشاء أمر مبيعات أو تعديله، يجب تنفيذ وظيفة الدُفعة **حساب إجماليات المبيعات‬** في Supply Chain Management. لن تتم مزامنة غير أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها إلى Sales.

## <a name="freight-tax"></a>ضريبة الشحن

لا يدعم Sales الضريبة على مستوى الرأس، لأنه يتم تخزين الضريبة على مستوى البند. لدعم الضريبة على مستوى الرأس من Supply Chain Managements، مثل الضريبة على الشحن، يقوم النظام بمزامنة الضريبة إلى Sales على أنها منتج مدون بالاسم يُسمى **ضريبة الشحن**، ويكون له مبلغ الضريبة من Supply Chain Management. بهذه الطريقة، يمكن استخدام عملية حساب السعر القياسي في Sales للإجماليات، حتى في حالة وجود ضريبة على مستوى الرأس من Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>حساب الخصومات وتقريبها

يختلف نموذج حساب الخصم في Sales عن نموذج حساب الخصم في Supply Chain Management. في Supply Chain Management، يمكن أن يكون مبلغ الخصم النهائي على بند مبيعات نتيجة لمجموعة من مبالغ الخصم والنسب المئوية. إذا كان مبلغ الخصم النهائي هذا مُقسمًا على الكمية في البند، فيمكن أن يحدث تقريب. ومع ذلك، لا يؤخذ هذا التقريب في الاعتبار في حالة مزامنة مبلغ خصم تقريبي لكل وحدة إلى Sales. للمساعدة في ضمان مزامنة مبلغ الخصم الكامل من بند مبيعات في Supply Chain Management بشكل صحيح إلى Sales، يجب مزامنة المبلغ الكامل دون تقسيمه على كمية البند. لذلك، يجب عليك تحديد **طريقة حساب الخصم** كـ **صنف بند** في Sales.

عند مزامنة بند أمر مبيعات من Sales إلى Supply Chain Management، يتم استخدام مبلغ خصم البند الكامل. نظرًا لأن Supply Chain Management لا يحتوي على حقل يمكنه تخزين مبلغ الخصم الكامل لأحد البنود، يتم تقسيم المبلغ على الكمية ويتم تخزينه في الحقل **خصم البند**. يتم تخزين أي تقريب يحدث في هذا التقسيم في الحقل **تكاليف المبيعات** في بند المبيعات.

### <a name="example"></a>مثال

**مزامنة من Sales إلي Supply Chain Management**

- **Sales:** الكمية = 3، خصم لكل بند = 10.00 دولار أمريكي
- **Supply Chain Management:** الكمية = 3 ، مبلغ خصم البند = $3.33 ، رسوم المبيعات =-$0.01 

**مزامنة من Supply Chain Management إلى Sales**

- **Supply Chain Management:** الكمية = 3 ، مبلغ خصم البند = $3.33 ، رسوم المبيعات =-$0.01
- **Sales:** الكمية = 3، خصم لكل بند = (3 × 3.33 دولار أمريكي) + 0.01 دولار أمريكي = 10.00 دولار أمريكي

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

تمت إضافة حقول جديدة إلى جدول **الأمر** وهي تظهر على الصفحة.

- **تتم المحافظة عليها خارجيًا‬‏‫‬‏‫** - عيّن هذا الخيار إلى **نعم** عندما يأتي الأمر من Supply Chain Management.
- **حالة المعالجة** - يستخدم هذا العمود لعرض حالة معالجة الأمر في Supply Chain Management. تتوفر القيم التالية:

    - **مسودة** – الحالة الأولية عند إنشاء أمر في Sales. في Sales، لا يمكن تحرير إلا الأوامر التي بحالة المعالجة هذه.
    - **نشط** – الحالة بعد تنشيط الأمر في Sales باستخدام الزر **تنشيط**.
    - **أوامر المبيعات المؤكدة**
    - **كشف التعبئة**
    - **مفوتر**
    - **منتقي**
    - **منتقى جزئيًا**
    - **معبأ جزئيًا**
    - **مشحون**
    - **مشحون جزئيًا**
    - **مفوتر جزئيًا**
    - **تم الإلغاء**

يتم استخدام الإعداد **لديه منتجات تتم المحافظة عليها خارجيًا فقط** أثناء تنشيط الأمر للتحقق بشكل مستمر مما إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا. إذا كان أمر المبيعات يتكوّن بكامله من منتجات تتم المحافظة عليها خارجيًا، فستتم المحافظة على المنتجات في Supply Chain Management. يساعد هذا الإعداد على ضمان عدم تنشيط أو محاولة مزامنة بنود أوامر المبيعات التي تشتمل على منتجات غير معروفة إلى Supply Chain Management.

تكون الأزرار **إنشاء فاتورة** و **إلغاء الأمر** و **إعادة الحساب** و **الحصول على منتجات** و **البحث عن عنوان** في صفحة **أمر المبيعات** مخفية للأوامر التي تتم المحافظة عليها خارجيًا إذ سيتم إنشاء الفواتير في Supply Chain Management وستتم مزامنتها إلى Sales. لا يمكن تحرير هذه الأوامر، لأنه ستتم مزامنة معلومات أمر المبيعات من Supply Chain Management بعد التنشيط.

سوف تظل حالة أمر المبيعات **نشطة** للمساعدة في ضمان إمكانية انسياب التغييرات من Supply Chain Management إلى أمر المبيعات في Sales. للتحكم في هذا السلوك، قم بتعيين الإعداد الافتراضي **Statecode \[الحالة\]** إلى **نشط** في مشروع تكامل البيانات.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

قبل إجراء مزامنة لأوامر المبيعات، لا بد من تحديث الإعدادات التالية في النظام.

### <a name="setup-in-sales"></a>الإعداد في Sales

- تأكد من إعداد الأذونات للفريق الذي تم تعيين المستخدم من إعداد الاتصال في Sales إليه. إذا كنت تستخدم بيانات العرض التوضيحي، فعادة ما يكون لدى المستخدم حق وصول المسؤول، ولكن هذا الحق لا يتوفر للفريق. إذا لم يكن لدى الفريق حق وصول المسؤول، عند تشغيل المشروع من تكامل البيانات، فسوف تتلقى رسالة خطأ تفيد بأن الفريق الرئيسي مفقود.

    انتقل إلى **الإعدادات** &gt; **الأمان** &gt; **الفرق**، حدد الفريق المناسب، وحدد **إدارة الأدوار**، ثم حدد دورًا يملك الأذونات المطلوبة على سبيل المثال، **مسؤول النظام**.

- للتأكد من صحة حساب الخصومات في كل من Sales وSupply Chain Management، يجب تعيين **طريقة حساب الخصم** إلى **صنف البند**.
- انتقل إلى **الإعدادات** &gt; **الإدارة** &gt; **إعدادات النظام** &gt; **Sales**‎، وتأكد من أنه يتم استخدام الإعدادات التالية:

    - يكون الخيار **‬‏‫استخدام حساب أسعار النظام** معينًا إلى **نعم**.
    - يكون العمود **طريقة حساب الخصم** معينًا إلى **صنف البند**.

### <a name="setup-in-supply-chain-management"></a>الإعداد في Supply Chain Management

- انتقل إلى **المبيعات والتسويق**&gt;**المهام الدورية**&gt;**حساب إجماليات المبيعات**، وعيِّن الوظيفة لتشغيلها كوظيفة دُفعة. عيّن الخيار **‏‫حساب إجماليات أوامر المبيعات‬** إلى **نعم**. ‏‫تعد هذه الخطوة هامة لأن أوامر المبيعات التي تم حساب إجماليات المبيعات‬ فيها هي فقط أوامر المبيعات التي ستتم مزامنتها إلى Sales. يجب أن يكون مدى تكرار وظيفة الدُفعة متوافقًا مع مدى تكرار مزامنة أوامر المبيعات.

إذا كنت تستخدم أيضًا تكامل أمر العمل، ستحتاج إلى إعداد أصل المبيعات. يتم استخدام أصل المبيعات لتمييز أوامر المبيعات في Supply Chain Management التي تم إنشاؤها من أوامر العمل في Field Service. عندما يشتمل أمر مبيعات على أصل مبيعات من نوع **تكامل أمر العمل**، يظهر حقل **حالة أمر العمل الخارجي** في عنوان أمر المبيعات. بالإضافة إلى ذلك، يساعد أصل المبيعات في ضمان تصفية أوامر المبيعات التي تم إنشاؤها من أوامر العمل في Field Service أثناء مزامنة أوامر المبيعات من Supply Chain Management إلى Field Service.

1. انتقل إلى **المبيعات والتسويق** \> **الإعداد** \> **أوامر المبيعات** \> **أصل المبيعات**.
2. حدد **جديد** لإنشاء أصل مبيعات جديد.
3. في العمود **أصل المبيعات**، أدخل اسمًا لأصل المبيعات، مثل **SalesOrder**.
4. في العمود **الوصف**، أدخل وصفاً، مثل **أمر مبيعات من Sales‎**.
5. حدد خانة الاختيار **مهمة نوع الأصل**.
6. قم بتعيين عمود **نوع أصل المبيعات** إلى **تكامل أمر المبيعات**.
7. حدد **حفظ**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>الإعداد في أوامر المبيعات (Sales إلى Supply Chain Management)- مشروع تكامل البيانات المباشر

- تأكد من وجود التعيين المطلوب لـ **Shipto\_country** إلى **DeliveryAddressCountryRegionISOCode**. يمكنك تعيين قيمة افتراضية فارغة في تعيين القيمة لتجنب الاضطرار إلى إدخال بلد للأوامر المحلية. عيّن الجانب الأيمن إلى "فارغ"، وعيّن الجانب الأيسر إلى البلد أو المنطقة المطلوبة.

    قيمة القالب هي تعيين قيمة حيث يتم تعيين العديد من البلدان أو المناطق، وحيث "فارغ" = US.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>الإعداد في مشروع تكامل البيانات: أوامر المبيعات (Supply Chain Management إلى Sales)‬ - مباشر

#### <a name="salesheader-task"></a>مهمة SalesHeader

- تكون قائمة الأسعار مطلوبة لإنشاء الأوامر في Sales. حدّث تعيين القيمة لـ **pricelevelid.name \[اسم قائمة الأسعار\]** إلى قائمة الأسعار المستخدمة في Sales لكل عملة. يمكنك استخدام قائمة الأسعار الافتراضية لعمله واحدة. بدلاً من ذلك، إذا كان لديك قوائم أسعار بعملات متعددة، يمكنك استخدام تعيين قيمة.

    قيمة القالب الافتراضية لـ **pricelevelid.name \[اسم قائمة الأسعار\]** تكون **CRM Service USA (نموذج)**.

#### <a name="salesline-task"></a>مهمة SalesLine

- تأكد من وجود تعيين القيمة المطلوب لـ **SalesUnitSymbol** في Supply Chain Management.
- تأكد من تحديد الوحدات المطلوبة في Sales.

    يتم تعريف قيمة القالب التي لها تعيين قيمة لـ **SalesUnitSymbol** إلى **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE]
> لا تشكل الأعمدة **شروط الدفع** و **شروط الشحن** و **شروط التسليم** و **أسلوب الشحن** و **وضع التسليم** جزءًا من التعيينات الافتراضية. لتعيين هذه الأعمدة، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الجدول بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات.

> [!NOTE]
> يعرض التعيين معلومات العمود التي ستتم مزامنتها من Sales إلى Supply Chain Management أو من Supply Chain Management إلى Sales.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>أوامر المبيعات (Supply Chain Management إلى Sales) - مباشر: OrderHeader

[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>أوامر المبيعات (Supply Chain Management إلى Sales) - مباشر: OrderLine

[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>أوامر المبيعات (Sales إلي Supply Chain Management) - مباشر: OrderHeader

[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>أوامر المبيعات (Sales إلى Supply Chain Management) - مباشر: OrderLine

[![تعيين القالب في تكامل البيانات](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]