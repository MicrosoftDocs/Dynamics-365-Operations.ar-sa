---
title: مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة الحسابات من Dynamics 365 Sales إلى Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8aa03f94e0fb89a6d34ce014dbb6004a1a666327
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529200"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Common Data Service للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة الحسابات من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales.  تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://preview.admin.powerapps.com/dataintegration) . حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب والمهمة الأساسية التالية لمزامنة الحسابات من Sales إلى Supply Chain Management:

- **اسم القالب في تكامل البيانات:** الحسابات (Sales إلى Fin and Ops) - مباشر
- **اسم المهمة في المشروع:** الحسابات - العملاء

لا توجد مهام مزامنة مطلوبة قبل إجراء مزامنة الحساب/العميل.

## <a name="entity-set"></a>مجموعة الكيانات

| ال‏‏مبيعات    | Supply Chain Management |
|----------|------------------------|
| الحسابات | العملاء V2           |

## <a name="entity-flow"></a>تدفق الكيان

تُدار الحسابات في Sales وتتم مزامنتها إلى Supply Chain Management: كعملاء. يتم تعيين الخاصية **تتم المحافظة عليها خارجيًا** على هؤلاء العملاء إلى **نعم** لتعقب العملاء الناشئين من Sales. أثناء الفوترة، يتم استخدام هذه المعلومات لتصفية الفواتير التي سيتم مزامنتها إلى Sales.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

يتوفر حقل **رقم الحساب** في صفحة **الحساب**. تم إنشاء مفتاح طبيعي وفريد له لدعم التكامل. قد تؤثر ميزة المفتاح الطبيعي في حل إدارة علاقات العملاء (CRM)‬ على العملاء الذين يستخدمون حقل **رقم الحساب**، ولكنهم لا يستخدمون قيم **رقم الحساب** لكل حساب. في الوقت الحالي، لا يدعم حل التكامل هذه الحالة.

عند إنشاء حساب جديد، إذا لم تكن قيمة **رقم الحساب** موجودة، فسيتم إنشاؤها تلقائيًا باستخدام تسلسل رقمي. تتكون القيمة من **ACC**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. فيما يلي مثال على ذلك: **ACC-01000-BVRCPS**

عند تطبيق حل التكامل على Sales، يقوم برنامج نصي للترقية بتعيين حقل **رقم الحساب** للحسابات الموجودة في Sales. في حال عدم وجود قيم في **رقم الحساب**، سيتم استخدام التسلسل الرقمي الذي تم ذكره في وقت سابق.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

- يجب تحديث تعيين **CustomerGroupId** إلى قيمة صالحة في Supply Chain Management. يمكنك تحديد قيمة افتراضية، أو يمكنك تعيين القيمة باستخدام تعيين القيمة.

    قيمة القالب الافتراضية هي **10**.

- عن طريق إضافة التعيينات التالية، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Supply Chain Management. يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.

    - **SiteId** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management. يمكن أخذ موقع افتراضي إما من المنتج، أو من العميل من رأس الأمر.

        قيمة القالب الافتراضية هي **1**.

    - **WarehouseId** – المستودع مطلوب لمعالجة بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management. يمكن أخذ مستودع افتراضي إما من المنتج، أو من العميل من رأس الأمر في Supply Chain Management.

        قيمة القالب الافتراضية هي **13**.

    - **LanguageId‎** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management. بشكل افتراضي، يتم استخدام اللغة من رأس الأمر من العميل.

        قيمة القالب الافتراضية هي **ar-sa**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

> [!NOTE]
> لا يتم تضمين الحقول **شروط الدفع** و **شروط الشحن** و **شروط التسليم** و **أسلوب الشحن** و **وضع التسليم** في التعيينات الافتراضية. لتعيين هذه الحقول، يجب إعداد تعيين قيمة خاصة بالبيانات الموجودة في المؤسسات التي تتم مزامنة الكيان بينها.

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.

![تعيين القالب في تكامل البيانات](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>مواضيع مرتبطة


[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎](accounts-template-mapping-direct.md)

[مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎](contacts-template-mapping-direct.md)

[مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales](sales-invoice-template-mapping-direct.md)

