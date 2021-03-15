---
title: مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة كيانات جهات الاتصال (جهات الاتصال) وجهات الاتصال (العملاء) من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8cbc2909c3f4533b4ea68e522f0874873989f3ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994032"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>مزامنة جهات الاتصال مباشرةً من Sales إلى جهات الاتصال أو العملاء في Supply Chain Management‎

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> قبل أن تتمكن من استخدام حل العميل المتوقع إلى النقدية، يجب عليك الاطلاع على [تكامل البيانات في Microsoft Dataverse للتطبيقات‏‎](https://docs.microsoft.com/powerapps/administrator/data-integrator).

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة جداول جهات الاتصال (جهات الاتصال) وجهات الاتصال (العملاء) مباشرةً من Dynamics 365 Sales إلى Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>تدفق البيانات في حل العميل المتوقع إلى النقدية

يستخدم حل العميل المتوقع إلى النقدية ميزة تكامل البيانات لمزامنة البيانات عبر مثيلات Supply Chain Management وSales. تسمح قوالب حل العميل المتوقع إلى النقدية المتوفرة مع ميزة تكامل البيانات بتدفق بيانات الحسابات وجهات الاتصال والمنتجات وعروض أسعار المبيعات وأوامر المبيعات وفواتير المبيعات بين Supply Chain Management وSales. يبين الرسم التوضيحي التالي كيف تتم مزامنة البيانات بين Supply Chain Management وSales.

[![تدفق البيانات في حل العميل المتوقع إلى النقدية](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>القوالب والمهام

للوصول إلى القوالب المتوفرة، افتح [مركز إدارة PowerApps](https://preview.admin.powerapps.com/dataintegration). حدد **المشاريع**، وبعد ذلك، في الزاوية العلوية اليسرى، حدد **مشروع جديد** لتحديد القوالب العامة.

يتم استخدام القوالب والمهام الأساسية التالية لمزامنة جداول جهة الاتصال (جهات الاتصال) في Sales إلى جداول جهة الاتصال (العملاء) في Supply Chain Management.

- **أسماء القوالب في تكامل البيانات**

    - جهات الاتصال (Sales إلى Supply Chain Management) - مباشر
    - جهات الاتصال إلى العميل (Sales إلى Supply Chain Management) - مباشر

- **أسماء المهام في مشروع تكامل البيانات**

    - جهات الاتصال
    - ContactToCustomer

يجب تنفيذ مهمة المزامنة التالية قبل إجراء مزامنة جهة الاتصال: الحسابات (Sales إلى Supply Chain Management)

## <a name="entity-sets"></a>مجموعات الكيانات

| ال‏‏مبيعات    | Supply Chain Management |
|----------|------------------------|
| جهات الاتصال | Dataverse جهات اتصال           |
| جهات الاتصال | العملاء V2           |

## <a name="entity-flow"></a>تدفق الكيان

تُدار الحسابات في Sales وتتم مزامنتها إلى Supply Chain Management.

يمكن أن تصبح جهة اتصال في Sales إما جهة اتصال أو عميل في Supply Chain Management. لتحديد ما إذا كانت جهة اتصال في Sales يفترض أن تتم مزامنتها إلى Supply Chain Management كجهة اتصال أو كعميل، يبحث النظام في الخصائص التالية في جهة الاتصال في Sales:

- **المزامنة إلى عميل في Supply Chain Management:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **نعم**
- **المزامنة إلى جهة اتصال في Supply Chain Management:** جهات الاتصال حيث تم تعيين **هو عميل نشط** إلى **لا** وحيث تشير **الشركة** (الحساب الأصل‬/جهة الاتصال الأصل) إلى حساب (وليس إلى جهة اتصال)

## <a name="prospect-to-cash-solution-for-sales"></a>حل العميل المتوقع إلى النقدية في Sales

تمت إضافة عمود **هو عميل نشط** جديد إلى جهة الاتصال. يستخدم هذا العمود للتمييز بين جهات الاتصال التي لها نشاط في مجال المبيعات وجهات الاتصال التي ليس لديها نشاط في مجال المبيعات. تم تعيين **هو عميل نشط** إلى **نعم** فقط لجهات الاتصال التي لديها عروض أسعار أو أوامر أو فواتير ذات صلة. تتم مزامنة جهات الاتصال هذه فقط إلى Supply Chain Management كعملاء.

تمت إضافة عمود **IsCompanyAnAccount‎** جديد إلى جهة الاتصال. يشير هذا العمود إلى ما إذا كانت جهة الاتصال مرتبطة بشركة (الحساب الأصل‬/جهة الاتصال الأصل) من النوع **حساب**. يتم استخدام هذه المعلومات لتحديد جهات الاتصال التي يجب أن تتم مزامنتها إلى Supply Chain Management كجهات اتصال.

تمت إضافة حقل **رقم جهة الاتصال** جديد إلى جهة الاتصال للمساعدة في ضمان مفتاح طبيعي وفريد للتكامل. عند إنشاء جهة اتصال جديدة، يتم إنشاء قيمة **رقم جهة الاتصال** بشكل تلقائي باستخدام تسلسل رقمي. تتكون القيمة من **CON**، يليه تسلسل رقمي متزايد ثم لاحقة من ستة أحرف. فيما يلي مثال على ذلك: **CON-01000-BVRCPS**

عند تطبيق حل التكامل لـ Sales، يقوم برنامج نصي للترقية بتعيين عمود **رقم جهة الاتصال** لجهات الاتصال الموجودة باستخدام التسلسل الرقمي الذي تم ذكره سابقًا. يقوم أيضًا البرنامج النصي للترقية بتعيين العمود **هو عميل نشط** إلى **نعم** لأي من جهات الاتصال التي لديها نشاط في مجال المبيعات.

## <a name="in-supply-chain-management"></a>في Supply Chain Management

توضع علامة على جهات الاتصال باستخدام الخاصية **IsContactPersonExternallyMaintained**. تشير هذه الخاصية إلى الاحتفاظ بجهة اتصال معينة خارجيًا. في هذه الحالة، يتم الاحتفاظ بجهات الاتصال التي تم الاحتفاظ بها خارجيًا في Sales.

## <a name="preconditions-and-mapping-setup"></a>الشروط المسبقة وإعداد التعيين

### <a name="contact-to-customer"></a>جهة اتصال إلى عميل

- **CustomerGroup** مطلوب في Supply Chain Management. للمساعدة على منع أخطاء المزامنة، يمكنك تحديد قيمة افتراضية في التعيين. يتم عندئذٍ استخدام هذه القيمة الافتراضية إذا ترك العمود فارغًا في Sales.

    قيمة القالب الافتراضية هي **10**.

- عن طريق إضافة التعيينات التالية، يمكنك المساعدة على تقليل عدد التحديثات اليدوية المطلوبة في Supply Chain Management. يمكنك استخدام قيمة افتراضية قيمة أو تعيين قيمة من، على سبيل المثال، **البلد/المنطقة** أو **المدينة**.

    - **SiteId** - يمكن أيضًا تعريف موقع افتراضي على المنتجات في Supply Chain Management. الموقع مطلوب لإنشاء أوامر المبيعات وعروض الأسعار في Supply Chain Management.

        قيمة قالب **SiteId** غير محددة.

    - **WarehouseId‎** - يمكن أيضًا تعريف مستودع افتراضي على المنتجات في Supply Chain Management. المستودع مطلوب لإنشاء أوامر المبيعات وعروض الأسعار في Supply Chain Management.

        قيمة قالب **WarehouseId** غير محددة.

    - **LanguageId‎** – الموقع مطلوب لإنشاء بنود أوامر المبيعات وعروض الأسعار في Supply Chain Management.
    
        قيمة القالب الافتراضية هي **ar-sa**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية مثالاً لتعيين قالب في تكامل البيانات. 

> [!NOTE]
> يعرض التعيين معلومات العمود التي ستتم مزامنتها من Sales إلى Supply Chain Management.

### <a name="contact-to-contact"></a>جهة اتصال إلى جهة اتصال

![تعيين القالب في موحد البيانات](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>جهة اتصال إلى عميل

![تعيين القالب في موحد البيانات](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>مواضيع مرتبطة

[العميل المتوقع إلى النقدية](prospect-to-cash.md)

[مزامنة الحسابات مباشرةً من Sales إلى العملاء في Supply Chain Management‎](accounts-template-mapping-direct.md)

[مزامنة المنتجات مباشرةً من Supply Chain Management إلى المنتجات في Sales‎‎](products-template-mapping-direct.md)

[مزامنة أوامر المبيعات مباشرة بين Sales وSupply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[مزامنة رؤوس وبنود فواتير المبيعات مباشرةً من Supply Chain Management إلى Sales](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]