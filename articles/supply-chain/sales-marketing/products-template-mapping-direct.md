---
title: مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
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
ms.openlocfilehash: 6ffd55585ff43f993876de6c669eb61e74a9fd79
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527304"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Common Data Service للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المنتجات مباشرة من Dynamics 365 Supply Chain Management إلى Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [Power Apps مركز الإدارة](https://admin.powerapps.com/dataintegration) . حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القالب والمهام الأساسية التالية لمزامنة المنتجات من Supply Chain Management إلى Sales.

- **اسم القالب في تكامل البيانات:** المنتجات (Supply Chain Management إلى Sales) - مباشر
- **اسم المهمة في مشروع تكامل البيانات:** المنتجات

لا توجد مهام مزامنة مطلوبة قبل إجراء مزامنة المنتج.

## <a name="entity-set"></a>مجموعة الكيانات

| Supply Chain Management    | ال‏‏مبيعات    |
|----------------------------|----------|
| منتجات قابلة للبيع تم إصدارها | المنتجات |

## <a name="entity-flow"></a>تدفق الكيان

تُدار المنتجات في Supply Chain Management وتتم مزامنتها إلى Sales. ‏‫يقوم كيان البيانات **منتجات قابلة للبيع تم إصدارها** في Supply Chain Management بتصدير المنتجات *القابلة للبيع* فقط. المنتجات القابلة للبيع هي المنتجات التي تشتمل على المعلومات المطلوبة لكي يتم استخدامها في أمر مبيعات. تنطبق القواعد نفسها عند التحقق من صحة منتج باستخدام وظيفة **التحقق من الصحة** في صفحة **المنتج الذي تم إصداره**.

يتم استخدام رقم المنتج كمفتاح. لذلك، عند مزامنة متغيرات المنتج إلى Sales، يكون لكل متغير منتج معرف فردي له.

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

في Sales، تمت إضافة حقل جديد على المنتجات وهو **تتم المحافظة عليها خارجيًا** للإشارة إلى المحافظة على منتج محدد خارجيًا‬‏‫‏‎. يتم تعيين القيمة إلى **نعم** بشكل افتراضي أثناء عملية الاستيراد إلى Sales. تتوفر القيم التالية:

- **نعم** – إنشاء المنتج من Supply Chain Management ولن يكون قابلاً للتحرير في Sales.
- **لا** - المنتج تم إدخاله مباشرةً في Sales.
- **(فارغ)** - المنتج موجود في Sales قبل تمكين ‏‫حل العميل المتوقع إلى النقدية.

يُساعد الحقل **تتم المحافظة عليها خارجيًا** في ضمان عدم مزامنة غير عروض الأسعار وأوامر المبيعات التي تشتمل على منتجات تتم المحافظة عليها خارجيًا إلى Supply Chain Management.

تُضاف المنتجات التي تتم المحافظة عليها خارجيًا بشكل تلقائي إلى أول قائمة أسعار صالحة لها العملة نفسها. يتم تنظيم قوائم الأسعار أبجديًا بالاسم. يتم استخدام سعر مبيعات المنتج من Supply Chain Management على أنه السعر على قائمة الأسعار. لذلك، يجب أن تكون هناك قائمة أسعار في Sales لكل عملة مبيعات منتج في Supply Chain Management. يتم تعيين العملة على المنتجات القابلة البيع إلى عملة المحاسبة في الكيان القانوني الذي تم تصدير المنتج منه.

> [!NOTE]
> - لن تنجح عملية مزامنة المنتج إلا في حال وجود قائمة أسعار تحتوي على عمله مطابقة.
> - يمكنك التحكم في قائمة الأسعار المستخدمة مع التكامل عن طريق تعيين pricelevelid.name [قائمة الأسعار الافتراضية (الاسم)] في مشروع تكامل البيانات. يجب أن يكون الإدخال بجميع الأحرف الصغيرة. على سبيل المثال، قد يكون الإعداد الافتراضي لقائمة أسعار في Sales مسماة 'قياسي': حقل الوجهة: pricelevelid.name [قائمة الأسعار الافتراضية (الاسم)] ونوع التعيين: [ { "transformType": "افتراضي"، "defaultValue": "قياسي" } ].

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

- قبل أن تقوم بتشغيل المزامنة للمرة الأولى، يتعين عليك ملء جدول المنتج المميز للمنتجات الموجودة في Supply Chain Management. لن تتم مزامنة المنتجات الموجودة حتى استكمال هذه الوظيفة.

    1. في Supply Chain Management، استخدم "البحث" للبحث عن **تعبئة جدول المنتج المميز‬**.
    2. حدد **تعبئة جدول المنتج المميز‬** لتشغيل الوظيفة. يجب تشغيل هذه المهمة مرة واحدة فقط.

- تأكد من أن تعيين القيمة المطلوب لوحدة القياس الخاصة بالبيع (UOM) بين Supply Chain Management وSales موجود في تعيين **SalesUnitSymbol** إلى **DefaultUnit (الاسم)**.
- قم بتحديث تعيين القيمة لـ **مجموعة الوحدات** (**defaultuomscheduleid.name**) لمطابقة **مجموعات الوحدات** في Sales.

    قيمة القالب الافتراضية هي **الوحدة الافتراضية**.

- تأكد من أن وحدات القياس الخاصة بالبيع لجميع المنتجات من Supply Chain Management موجودة في Sales.
- تأكد من وجود قوائم أسعار في Sales لكل عملة مبيعات منتج في Supply Chain Management.
- عند إنشاء منتجات في Sales، يمكن أن يكون لها الحالة **مسودة** أو **نشطة**. يتم التحكم في السلوك في **الإعدادات** > **الإدارة** > **إعدادات النظام** > **المبيعات** في Sales.

    يجب تنشيط المنتجات التي لها الحالة **مسودة** عند إنشائها قبل أن يمكن إضافتها إلى عروض الأسعار أو أوامر المبيعات.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالي مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات الحقل التي ستتم مزامنتها من Sales إلى Supply Chain Management.

![تعيين القالب في موحد البيانات](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎](accounts-template-mapping-direct.md)

[مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎](contacts-template-mapping-direct.md)

[مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]