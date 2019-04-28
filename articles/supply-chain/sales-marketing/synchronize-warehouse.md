---
title: مزامنة المستودعات من Finance and Operations إلى Field Service
description: يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/14/2019
ms.locfileid: "842523"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>مزامنة المستودعات من Finance and Operations إلى Field Service

[!include[banner](../includes/banner.md)]

يصف هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يتم استخدام القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

**قالب في تكامل البيانات**
- المستودعات (Fin and Ops إلى Field Service)

**مهمة في مشروع تكامل البيانات**
- المستودع

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | المستودعات                             |

## <a name="entity-flow"></a>تدفق الكيان
يمكن مزامنة المستودعات التي يتم إنشاؤها وصيانتها في Finance and Operations إلى Field Service عبر مشروع تكامل بيانات Common Data Service (CDS). يمكن التحكم في المستودعات التي تريد مزامنتها مع Field Service بواسطة وظائف الاستعلام والتصفية المتقدمة على المشروع. ويتم إنشاء المستودعات التي تتزامن من Finance and Operations في Field Service مع تعيين الحقل **تتم المحافظة عليه خارجيًا‬** إلى **نعم** والسجل محدد للقراءة فقط.

## <a name="field-service-crm-solution"></a>حل Field Service CRM
لدعم التكامل بين Field Service وFinance and Operations، يُتطلب وجود وظيفة إضافية من حل Field Service CRM. في الحل، تمت إضافة الحقل **تتم المحافظة عليه خارجيًا** إلى كيان **المستودع (msdyn_warehouses)**. يساعد هذا الحقل في تحديد ما إذا كانت معالجة المستودع تتم من Finance and Operations أو إذا كان موجودًا فقط في Field Service. تتضمن إعدادات هذا الحقل:
- **نعم** – نشأ المستودع من Finance and Operations ولن يكون قابلاً للتحرير في Sales.
- **لا** – تم إدخال المستودع مباشرة في Field Service ويتم الاحتفاظ به هنا.

يساعد الحقل **تتم المحافظة عليه خارجيًا** في التحكم في مزامنة مستويات المخزون والتسويات وعمليات التحويل والاستخدام في أوامر العمل. يمكن استخدام فقط المستودعات حيث تم تعيين الخيار **تتم المحافظة عليها خارجيًا‬‏‫** إلى **نعم** للمزامنة مباشرة إلى المستودع نفسه في النظام الآخر. 

> [!NOTE]
> من الممكن إنشاء عدة مستودعات في Field Service (مع تعيين الخيار **تتم المحافظة عليها خارجيًا‬‏‫** = لا") ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف التصفية والاستعلام المتقدمة. يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field Service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations. في هذه الحالة، لن تحصل Field service على تحديثات على مستوى المخزون من Finance and Operations. للحصول على معلومات إضافية، راجع [مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) و[مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين
### <a name="data-integration-project"></a>مشروع تكامل البيانات
قبل مزامنة المستودعات، تأكد من تحديث وظائف الاستعلام والتصفية المتقدمة بحيث تتضمن فقط المستودعات التي تريد إحضارها من Finance and Operations إلى Field Service. لاحظ أنك ستحتاج إلى المستودع في Field Service لتطبيقه على أوامر العمل والتسويات وعمليات التحويل.  

للتأكد من وجود **مفتاح تكامل** لـ **msdyn_warehouses**:
1. انتقل إلى "تكامل البيانات".
2. حدد علامة التبويب **مجموعة الاتصال**.
3. حدد مجموعة الاتصال المستخدمة لمزامنة أمر العمل.
4. حدد علامة التبويب **مفتاح التكامل**.
5. ابحث عن msdyn_warehouses وتأكد من إضافة المفتاح **msdyn_name (الاسم)**. إذا لم يظهر، فأضفه بالنقر فوق **إضافة مفتاح**، ثم انقر فوق **حفظ** في الجزء العلوي من الصفحة.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

يبين الشكل التوضيحي التالية تعيين القالب في تكامل البيانات.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>المستودعات (Fin and Ops إلى Field Service): المستودع

[![تعيين القالب في تكامل البيانات](./media/Warehouse1.png)](./media/Warehouse1.png)
