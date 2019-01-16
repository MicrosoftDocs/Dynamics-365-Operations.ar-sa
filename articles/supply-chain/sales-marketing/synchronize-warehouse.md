---
title: "مزامنة المستودعات من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>مزامنة المستودعات من Finance and Operations إلى Field Service

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.

[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>القوالب والمهام
يُستخدم القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المستودعات من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.

**اسم القالب في تكامل البيانات:**
- المستودعات (Finance and Operations إلى Field Service)

**أسماء المهام في مشروع تكامل البيانات:**
- المستودع

## <a name="entity-set"></a>مجموعة الكيانات
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | المستودعات                             |

## <a name="entity-flow"></a>تدفق الكيان
يمكن مزامنة المستودعات التي يتم إنشاؤها وصيانتها في Finance and Operations إلى Field Service عبر مشروع تكامل بيانات Common Data Service (CDS). يمكن التحكم في المستودعات المطلوبة التي تتزامن مع Field Service بواسطة وظائف الاستعلام والتصفية المتقدمة على المشروع. ويتم إنشاء المستودعات التي تتزامن من Finance and Operations في Field Service مع تعيين الحقل "تتم المحافظة عليه خارجيًا‬" إلى "نعم" والسجل محدد للقراءة فقط.
حل Field Service CRM لدعم التكامل بين Field Service وFinance and Operations، يلزم وجود وظيفة إضافية من حل Field Service CRM. يشتمل الحل على التغييرات التالية.
تمت إضافة الحقل **تتم المحافظة عليه خارجيًا** إلى كيان **المستودع (msdyn_warehouses)**. يساعد هذا الحقل في تحديد ما إذا كانت معالجة المستودع من Operations أو إذا كان موجودًا فقط في Field Service.
- نعم - نشأ المستودع من Finance and Operations ولن يكون قابلاً للتحرير في Sales.
- لا – تم إدخال المستودع مباشرة في Field Service ويتم الاحتفاظ به هنا.

يساعد الحقل **تتم المحافظة عليه خارجيًا** في التحكم في مزامنة مستويات المخزون والتسويات وعمليات التحويل والاستخدام في أوامر العمل. وحدها المستودعات حيث **تتم المحافظة عليها خارجيًا‬‏‫** = نعم يمكن استخدامها للمزامنة مباشرة إلى نفس المستودع في النظام الآخر. 

ملاحظة: من الممكن إنشاء عدة مستودعات في Field Services (باستخدام **تتم المحافظة عليها خارجيًا‬‏‫** = لا") ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف التصفية والاستعلام المتقدمة. يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations. في هذه الحالة، لن تحصل Field service على تحديثات مستوى المخزون من Finance and Operations. اطلع على معلومات إضافية في "مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬" و"مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations‬".

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين
### <a name="in-the-data-integration-project"></a>في مشروع تكامل البيانات
قبل مزامنة المستودعات، تأكد من تحديث وظائف الاستعلام والتصفية المتقدمة بحيث تتضمن فقط المستودعات التي تريد إحضارها من Finance and Operations إلى Field Service. لاحظ أنك ستحتاج إلى المستودع في Field Service لتطبيقه على أوامر العمل والتسويات وعمليات التحويل.  

تأكد من وجود **مفتاح تكامل** لـ **msdyn_warehouses**
1. اذهب إلى تكامل البيانات
2. حدد علامة التبويب **مجموعة الاتصال**
3. حدد مجموعة الاتصال المستخدمة لمزامنة أمر العمل
4. حدد علامة التبويب **مفتاح التكامل**
5. ابحث عن msdyn_warehouses وتأكد نت إضافة المفتاح **msdyn_name (الاسم)**. إذا كان غير معروض، فأضفه بالنقر فوق **إضافة مفتاح**، ثم انقر فوق **حفظ** في الجزء العلوي من الصفحة

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>المستودعات (Finance and Operations إلى Field Service): المستودع

[![تعيين القالب في تكامل البيانات](./media/Warehouse1.png)](./media/Warehouse1.png)

