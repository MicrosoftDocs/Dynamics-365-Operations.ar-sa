---
title: العميل المتوقع إلى النقدية في الكتابة المزدوجة
description: توفر هذه المقالة معلومات عن العميل المتوقع إلى النقدية في الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 4321d980f56e321a653ca4f4c5738ebd1bb0153d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289597"
---
# <a name="prospect-to-cash-in-dual-write"></a>العميل المتوقع إلى النقدية في الكتابة المزدوجة

[!include [banner](../../includes/banner.md)]

ثمة هدف مهم لمعظم الشركات وهو تحويل العملاء المتوقعين إلى عملاء، ثم المحافظة على علاقة عمل مستمرة مع هؤلاء العملاء. في تطبيقات Microsoft Dynamics 365، تحدث عملية العميل المتوقع إلى النقدية من خلال عروض الأسعار أو عمليات سير عمل معالجة الأوامر، وتتم تسوية العمليات المالية والتعرف عليها. يؤدي تكامل عملية العميل المتوقع إلى النقدية مع الكتابة المزدوجة إلى إنشاء سير عمل يأخذ عرض أسعار وأمر ناشئين في Dynamics 365 Sales أو Dynamics 365 Supply Chain Management، ويجعل عرض الأسعار والأمر متاحين في التطبيقين.

في واجهات التطبيقين، يمكنك الوصول إلى حالات المعالجة ومعلومات الفاتورة في الوقت الحقيقي. وبالتالي، يمكنك إدارة وظائف مثل إنشاء مخزون منتجات والتعامل مع المخزون والتنفيذ في Supply Chain Management، من دون الحاجة إلى إعادة إنشاء عروض الأسعار والأوامر.

![تدفق بيانات الكتابة المزدوجة في عملية العميل المتوقع إلى النقدية.](../dual-write/media/dual-write-prospect-to-cash[1].png)

للحصول علي معلومات حول تكامل العميل والاتصال، راجع [السجل الرئيسي المتكامل للعميل](customer-mapping.md). لمزيد من المعلومات حول تكامل المنتج، راجع [تجربه المنتج الموحدة](product-mapping.md).

> [!NOTE]
> في Dynamics 365 Sales، يشير كل من العميل المتوقع والعميل إلى سجل في جدول **الحساب** حيث يكون العمود **RelationshipType** اما **عميل متوقع** أو **عميل**. إذا تضمن منطق العمل الخاص بك عملية تأهيل **الحساب** حيث يتم إنشاء سجل **الحساب** وتأهيله كعميل متوقع أولاً، ثم كعميل، يقوم هذا السجل بالمزامنة مع تطبيق التمويل والعمليات فقط عندما يكون عميلاً (`RelationshipType=Customer`). إذا كنت ترغب في ان يقوم صف **الحساب** بالمزامنة كعميل متوقع، ستحتاج إلى مخطط مخصص لدمج بيانات العميل المتوقع.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

قبل أن تتمكن من مزامنة عروض أسعار المبيعات، يجب تحديث الإعدادات التالية.

### <a name="setup-in-sales"></a>الإعداد في Sales

في Sales، انتقل إلى **الإعدادات‏‎ \> الإدارة‏‎ \> إعدادات النظام \> المبيعات**، وتأكد من استخدام الإعدادات التالية:

- يتم تعيين خيار النظام **‬‏‫حساب تسعير النظام** إلى **نعم**.
- يكون العمود **طريقة حساب الخصم** معينًا إلى **صنف البند**.

### <a name="sites-and-warehouses"></a>المواقع والمستودعات

في Supply Chain Management، عمود **الموقع** وعمود **المستودع‏‎** مطلوبان لبنود عرض الأسعار وبنود الأمر. إذا قمت بتعيين الموقع والمستودع في إعدادات الأمر الافتراضية، فسيتم تعيين هذه الأعمدة بشكل تلقائي عند إضافة منتج إلى بند عرض أسعار أو بند أمر. 

### <a name="number-sequences-for-quotations-and-orders"></a>التسلسلات الرقمية لعروض الأسعار والأوامر

لا تكون Sales and Supply Chain Management. الرقمية لكل من Supply Chain Management وSales متصلة عند إنشاء عروض الأسعار والأوامر ومتزامنة في Sales وSupply Chain Management. إذا تمت مزامنة أمر مبيعات تم إنشاؤه في Sales إلى Supply Chain Management، فسيكون له رقم أمر المبيعات نفسه في Supply Chain Management. للمساعدة في ضمان عدم تكرار رقم أمر المبيعات، يجب استخدام أنظمه تسلسلات رقمية مختلفة في التطبيقين.

على سبيل المثال، إذا كان التسلسل الرقمي في Supply Chain Management على الشكل **1, 2, 3, 4, 5, ...**، والتسلسل الرقمي في Sales على الشكل **100, 99, 98, ...**. إذا أنشأت 100 أمر مبيعات في Sales، سيتم إنشاء رقم أمر موجود في Supply Chain Management. بمعنى آخر، سيتداخل التسلسلين الرقميين عند إنشاء أوامر المبيعات في Supply Chain Management وSales. بدلاً من ذلك، يمكنك استخدام تسلسل رقمي مثل **F1, F2, F3, ...** في Supply Chain Management وتسلسل رقمي مثل **C1, C2, C3, ...** في Sales. لن تنتج هذه التسلسلات الرقمية إطلاقًا أرقام أوامر مبيعات مكررة.

## <a name="sales-quotations"></a>عروض أسعار المبيعات

يمكن إنشاء عروض أسعار المبيعات في Sales أو Supply Chain Management. إذا قمت بإنشاء عرض أسعار في Sales، ستتم مزامنته إلى Supply Chain Management في الوقت الحقيقي. وبطريقة مماثلة، إذا قمت بإنشاء عرض أسعار في Supply Chain Management، ستتم مزامنته إلى Sales في الوقت الحقيقي. لاحظ النقاط التالية:

+ يمكنك إضافة خصم إلى المنتج في عرض الأسعار. وفي هذه الحالة، ستتم مزامنة الخصم إلى Supply Chain Management. تخضع أعمدة **الخصم** و **التكاليف** و **الضريبة** للإعدادات في Supply Chain Management. لا يدعم هذا الإعداد تعيين التكامل. بدلاً من ذلك، يتولى Supply Chain Management المحافظة على الحقول **السعر** و **الخصم** و **التكاليف** و **الضريبة** والتعامل معها.
+ أعمدة **% الخصم‬** و **الخصم‬** و **مبلغ الشحن** في رأس عرض أسعار المبيعات للقراءة فقط.
+ لا تعتبر أعمدة **شروط الشحن** و **شروط التسليم** و **طريقة الشحن** و **وضع التسليم** جزءًا من التعيينات الافتراضية. لتعيين هذه الأعمدة، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الجدول بينها.

إذا كنت تستخدم أيضًا حل Field Service، فتأكد من إعادة تمكين المعلمة **إنشاء سريع لبند عرض الأسعار**. تتيح لك إعادة تمكين المعلمة الاستمرار في إنشاء بنود عرض الأسعار باستخدام وظيفة الإنشاء السريع.

1. انتقل إلى تطبيق Dynamics 365 Sales الخاص بك.
2. حدد رمز الإعدادات في شريط التنقل العلوي.
3. حدد **الإعدادات المتقدمة**.
4. اختر خيار **تخصيص النظام**.
5. حدد عنصر قائمة **بند عرض الأسعار**.
6. انتقل إلى القسم **خدمات البيانات**، ثم حدد خانة الاختيار **السماح بالإنشاء السريع**.

## <a name="sales-orders"></a>أوامر المبيعات

يمكن إنشاء أوامر المبيعات في Sales أو Supply Chain Management. إذا قمت بإنشاء أمر مبيعات في Sales، ستتم مزامنته إلى Supply Chain Management في الوقت الحقيقي. وبطريقة مماثلة، إذا قمت بإنشاء أمر مبيعات في Supply Chain Management، ستتم مزامنته إلى Sales في الوقت الحقيقي. لاحظ النقاط التالية:

+ سوف تظهر المنتجات المدونة في Dynamics 365 Sales كفئات منتجات في Dynamics 365 Supply Chain Management.
+ حساب الخصومات وتقريبها:

    - يختلف نموذج حساب الخصم في Sales عن نموذج حساب الخصم في Supply Chain Management. في Supply Chain Management، يمكن أن يكون مبلغ الخصم النهائي على بند مبيعات نتيجة لمجموعة من مبالغ الخصم والنسب المئوية. إذا كان مبلغ الخصم النهائي هذا مُقسمًا على الكمية في البند، فيمكن أن يحدث تقريب. ومع ذلك، لا يؤخذ هذا التقريب في الاعتبار في حالة مزامنة مبلغ خصم مقرّب لكل وحدة إلى Sales. للمساعدة في ضمان مزامنة مبلغ الخصم الكامل من بند مبيعات في Supply Chain Management بشكل صحيح إلى Sales، يجب مزامنة المبلغ الكامل دون تقسيمه على كمية البند. وبالتالي، يجب عليك تحديد طريقة حساب الخصم على أنه **صنف بند** في Sales.
    - عند مزامنة بند أمر مبيعات من Sales إلى Supply Chain Management، يتم استخدام مبلغ خصم البند الكامل. نظرًا لأن Supply Chain Management لا يحتوي على عمود يمكنه تخزين مبلغ الخصم الكامل لأحد البنود، يتم تقسيم المبلغ على الكمية ويتم تخزينه في العمود **خصم البند**. يتم تخزين أي تقريب يحدث أثناء هذا التقسيم في العمود **تكاليف المبيعات** في بند المبيعات.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>مثال: مزامنة من Sales إلي Supply Chain Management

لديك أمر المبيعات التالي:

+ **Sales:** الكمية = 3، خصم لكل بند = 10.00 دولار أمريكي
+ **Supply Chain Management:** الكمية = 3، مبلغ خصم البند = $3.33، رسوم المبيعات = –$0.01

إذا أجريت المزامنة من Supply Chain Management إلى Sales، ستحصل على النتيجة التالية:

+ **Supply Chain Management:** الكمية = 3، مبلغ خصم البند = $3.33، رسوم المبيعات = –$0.01
+ **Sales:** الكمية = 3، خصم لكل بند = (3 × 3.33 دولار أمريكي) + 0.01 دولار أمريكي = 10.00 دولار أمريكي

## <a name="dual-write-solution-for-sales"></a>حل الكتابة المزدوجة لتطبيق Sales

تمت إضافة حقول جديدة إلى جدول **الأمر** وهي تظهر على الصفحة. يظهر معظم هذه الأعمدة على علامة تبويب **التكامل** في Sales. لمعرفة المزيد حول كيفية تعيين أعمدة الحالات، راجع [إعداد تعيين أعمدة حالات أوامر المبيعات](sales-status-map.md).

+ لا يظهر الزران **إنشاء فاتورة** و **إلغاء الأمر** في صفحة **أمر المبيعات** في Sales.
+ قيمة **حالة أمر المبيعات** تبقى **نشطة** للمساعدة في ضمان إمكانية تدفق التغييرات من Supply Chain Management إلى أمر المبيعات في Sales. للتحكم في هذا السلوك، قم بتعيين الإعداد الافتراضي **Statecode \[الحالة\]** إلى **نشط**.

## <a name="invoices"></a>الفواتير

يتم إنشاء فواتير المبيعات في Supply Chain Management وتتم مزامنتها إلى Sales. لاحظ النقاط التالية:

+ تمت إضافة عمود **رقم الفاتورة** إلى جدول **الفاتورة** ويتم عرضه على الصفحة.
+ يكون الزر **إنشاء فاتورة** في صفحة **أمر المبيعات** مخفيًا لأن إنشاء الفواتير سيتم في Supply Chain Management وستتم مزامنتها إلى Sales. لا يمكن تحرير صفحة **الفاتورة**، لأن مزامنة الفواتير ستتم من Supply Chain Management.
+ تتغير **حالة أمر المبيعات** تلقائيًا إلى **مفوتر** عندما تتم مزامنة الفاتورة ذات الصلة من Supply Chain Management إلى Sales. بالإضافة إلى ذلك، يتم تعيين مالك أمر المبيعات الذي تم إنشاء الفاتورة منه كمالك للفاتورة. لذلك، يمكن لمالك أمر المبيعات عرض الفاتورة.
+ لا يتم تضمين الأعمدة **شروط الشحن** و **شروط التسليم** و **وضع التسليم** في التعيينات الافتراضية. لتعيين هذه الأعمدة، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الجدول بينها.

## <a name="templates"></a>القوالب

تتضمن عملية العميل المتوقع إلى النقدية مجموعة من خرائط الجداول الرئيسية التي تعمل معًا أثناء تفاعل البيانات، كما هو موضح في الجدول التالي.

| تطبيقات التمويل والعمليات | تطبيقات Customer Engagement | ‏‏الوصف‬ |
|-----------------------------|-----------------------------------|-------------|
[كل المنتجات](mapping-reference.md#138) | msdyn_globalproducts | |
[العملاء V3](mapping-reference.md#101) | الحسابات | |
[العملاء V3](mapping-reference.md#116) | جهات الاتصال | |
[جهات اتصال V2](mapping-reference.md#221) | msdyn_contactforparties | |
[رؤوس أوامر مبيعات CDS](mapping-reference.md#217) | salesorders | |
[بنود أمر مبيعات CDS](mapping-reference.md#216) | salesorderdetails | |
[رأس عرض أسعار مبيعات CDS](mapping-reference.md#215) | الأسعار | |
[بنود عروض أسعار مبيعات CDS](mapping-reference.md#214) | quotedetails | |
[المنتجات الصادرة V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[رؤوس فواتير المبيعات V2](mapping-reference.md#118) | الفواتير | يحتوي الجدول الذي يتضمن رؤوس فاتورة المبيعات في تطبيقات التمويل والعمليات علي فواتير لأوامر البيع وفواتير النص الحر. يتم تطبيق عامل التصفية في Dataverse للكتابة الثنائية التي ستقوم بتصفية إيه مستندات فاتورة ذات نص حر. |
[بنود فواتير المبيعات V2](mapping-reference.md#117) | invoicedetails | |
[أكواد أصول أوامر المبيعات](mapping-reference.md#186) | msdyn_salesorderorigins | |

لمزيد من المعلومات حول قوائم الأسعار، راجع [تجربه المنتج الموحدة](product-mapping.md).

## <a name="limitations"></a>قيود

- أوامر الإرجاع غير معتمده.
- الإشعارات الدائنة غير مدعومة.
- يجب تعيين الابعاد المالية للبيانات الرئيسية، علي سبيل المثال، العميل والمورد. عند أضافه عميل إلى عرض أسعار أو أمر توريد، فان الابعاد المالية المرتبطة بسجل العميل يتم تدفقها إلى الأمر تلقائيا. لا يتضمن الكتابة الثنائية حاليا بيانات الابعاد المالية للبيانات الرئيسية.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

