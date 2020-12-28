---
title: مزامنة المستودعات من Supply Chain Management إلى Field Service
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 28445592d7a2a8964b1642ae52cff08be6feabbe
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529496"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>مزامنة المستودعات من Supply Chain Management إلى Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.

[![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القوالب والمهام الأساسية التالية لتشغيل مزامنة المستودعات من Supply Chain Management إلى Field Service.

**قالب في تكامل البيانات**
- المستودعات (Supply Chain Management إلى Field Service)

**مهمة في مشروع تكامل البيانات**
- المستودع

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | المستودعات                             |

## <a name="entity-flow"></a>تدفق الكيان
يمكن مزامنة المستودعات التي يتم إنشاؤها وصيانتها في Supply Chain Management إلى Field Service عبر مشروع تكامل بيانات Common Data Service (CDS). يمكن التحكم في المستودعات التي تريد مزامنتها مع Field Service بواسطة وظائف الاستعلام والتصفية المتقدمة على المشروع. ويتم إنشاء المستودعات التي تتزامن من Supply Chain Management في Field Service مع تعيين الحقل **تتم المحافظة عليه خارجيًا‬** إلى **نعم** والسجل محدد للقراءة فقط.

## <a name="field-service-crm-solution"></a>حل Field Service CRM
لدعم التكامل بين Field Service وSupply Chain Management، يلزم وجود وظيفة إضافية من حل Field Service CRM. في الحل، تمت إضافة الحقل **تتم المحافظة عليه خارجيًا** إلى كيان **المستودع (msdyn_warehouses)**. يساعد هذا الحقل في تحديد ما إذا كانت معالجة المستودع تتم من Supply Chain Management أو إذا كان موجودًا فقط في Field Service. تتضمن إعدادات هذا الحقل:
- **نعم** – نشأ المستودع من Supply Chain Management ولن يكون قابلاً للتحرير في Sales.
- **لا** – تم إدخال المستودع مباشرة في Field Service ويتم الاحتفاظ به هنا.

يساعد الحقل **تتم المحافظة عليه خارجيًا** في التحكم في مزامنة مستويات المخزون والتسويات وعمليات التحويل والاستخدام في أوامر العمل. يمكن استخدام فقط المستودعات حيث تم تعيين الخيار **تتم المحافظة عليها خارجيًا‬‏‫** إلى **نعم** للمزامنة مباشرة إلى المستودع نفسه في النظام الآخر. 

> [!NOTE]
> من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا‬‏‫** = لا") ثم تعيينها إلى مستودع واحد باستخدام وظائف التصفية والاستعلام المتقدمة. يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Supply Chain Management. في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Supply Chain Management. للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين
### <a name="data-integration-project"></a>مشروع تكامل البيانات
قبل مزامنة المستودعات، تأكد من تحديث وظائف الاستعلام والتصفية المتقدمة بحيث تتضمن فقط المستودعات التي تريد إحضارها من Supply Chain Management إلى Field Service. لاحظ أنك ستحتاج إلى المستودع في Field Service لتطبيقه على أوامر العمل والتسويات وعمليات التحويل.  

للتأكد من وجود **مفتاح تكامل** لـ **msdyn_warehouses**:
1. انتقل إلى "تكامل البيانات".
2. حدد علامة التبويب **مجموعة الاتصال**.
3. حدد مجموعة الاتصال المستخدمة لمزامنة أمر العمل.
4. حدد علامة التبويب **مفتاح التكامل**.
5. ابحث عن msdyn_warehouses وتأكد من إضافة المفتاح **msdyn_name (الاسم)**. إذا لم يظهر، فأضفه بالنقر فوق **إضافة مفتاح**، ثم انقر فوق **حفظ** في الجزء العلوي من الصفحة.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالية تعيين القالب في تكامل البيانات.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>المستودعات (Supply Chain Management إلى Field Service): المستودع

[![تعيين القالب في تكامل البيانات](./media/Warehouse1.png)](./media/Warehouse1.png)
