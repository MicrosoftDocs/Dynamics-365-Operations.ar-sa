---
title: "مزامنة فواتير الاتفاقية في Field Service في الفواتير ذات النص الحر‬ في Finance and Operations"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فواتير الاتفاقيات في Microsoft Dynamics 365 for Field Service لفواتير النص الحر في Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: 6672e283a5e56b068e3494d53a0fd6dd08253ba9
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>مزامنة فواتير الاتفاقية في Field Service في الفواتير ذات النص الحر‬ في Finance and Operations

[!include[banner](../includes/banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فواتير الاتفاقيات في Microsoft Dynamics 365 for Field Service لفواتير النص الحر في Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>القوالب والمهام

يتم استخدام القالب والمهام الأساسية التالية لتشغيل مزامنة فواتير الاتفاقيات من Field Service لفواتير النص الحر في Finance and Operations.

**اسم القالب في تكامل البيانات:**

- فواتير الاتفاقيات (Field Service لـ Fin and Ops)

**أسماء المهام في مشروع تكامل البيانات:**

- عناوين الفواتير
- سطور الفاتورة

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة فواتير الاتفاقيات:

- الحسابات (Sales إلى Fin and Ops)‬ - المباشرة

## <a name="entity-set"></a>مجموعة الكيانات

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| الفواتير       | رؤوس فاتورة النص الحر لعميل CDS |
| invoicedetails | بنود فاتورة النص الحر لعميل CDS   |

## <a name="entity-flow"></a>تدفق الكيان

يمكن مزامنة الفواتير التي تم إنشاؤها من اتفاقية في Field Service لـ Finance and Operations عبر مشروع تكامل بيانات Common Data Service (CDS). ستتم مزامنة التحديثات لهذه الفواتير لفواتير النص الحر في Finance and Operations إذا كانت حالة المحاسبة للفواتير ذات النص الحر **قيد المعالجة**. بعد ترحيل فواتير النص الحر في Finance and Operations، وتحديث حالة المحاسبة إلى **مكتمل**، لن تتمكن بعد ذلك من مزامنة التحديثات من Field Service.

## <a name="field-service-crm-solution"></a>حل Field Service CRM

تمت إضافة حقل **لديه بنود في أصل الاتفاقية** إلى كيان **الفاتورة**. يساعد هذا الحقل على ضمان مزامنة الفواتير التي تم إنشاؤها من اتفاقية. تكون القيمة **صواب** إذا كانت الفاتورة تحتوي على بند فاتورة واحد على الأقل موجودة أصلاً في اتفاقية.

تمت إضافة حقل **لديه أصل اتفاقية** إلى كيان **بند الفاتورة**. يساعد هذا الحقل على ضمان مزامنة فقط بنود الفواتير التي تم إنشاؤها من اتفاقية. تكون القيمة **صواب** إذا كان بند الفاتورة نشأ من اتفاقية.

**تاريخ الفاتورة** عبارة عن حقل إلزامي في Finance and Operations. لذلك، يجب أن يكون للحقل قيمة في Field Service قبل إجراء المزامنة. لتلبية هذا المتطلب، تتم إضافة المنطق التالي:

- إذا كان حقل **تاريخ الفاتورة** فارغًا في كيان **الفاتورة** (بمعنى، في حالة عدم وجود قيمة)، يتم تعيينه إلى التاريخ الحالي عندما تتم إضافة بند فاتورة ينشأ من اتفاقية.
- يمكن للمستخدم تغيير حقل **تاريخ الفاتورة**. ومع ذلك، عندما يحاول المستخدم حفظ فاتورة تنشأ من اتفاقية، فإنه يتلقى خطأ في عملية أعمال إذا كان حقل **تاريخ الفاتورة** فارغاً في الفاتورة.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="in-finance-and-operations"></a>في Finance and Operations

يجب إعداد أصل فاتورة للتكامل، لتمييز الفواتير ذات النص الحر في Finance and Operations والتي تم إنشاؤها من فواتير الاتفاقيات في Field Service. عندما تشتمل فاتورة على أصل فاتورة من نوع **تكامل فاتورة الاتفاقية**، يتم عرض حقل **رقم الفاتورة الخارجية** في عنوان **فاتورة المبيعات**.

بالإضافة إلى الظهور في عنوان الفاتورة، يمكن استخدام معلومات **رقم الفاتورة الخارجية** للمساعدة في ضمان تصفية الفواتير التي تم إنشاؤها من الفواتير اتفاقيات Field Service أثناء مزامنة الفواتير من Finance and Operations لـ Field Service.

1. انتقل إلى **الحسابات المدينة** \> **الإعداد** \> **أكواد أصل الفاتورة**.
2. حدد **جديد** لإنشاء أصل فاتورة جديد.
3. في حقل **أصل الفاتورة**، أدخل اسمًا لأصل الفاتورة، مثل **FS**.
4. في حقل **الوصف**، أدخل وصفاً، مثل **فاتورة اتفاقية Field Service**.
5. حدد خانة الاختيار **مهمة نوع الأصل**.
6. قم بتعيين حقل **نوع أصل الفاتورة** إلى **تكامل فاتورة الاتفاقية**.
7. حدد **حفظ**.

### <a name="in-the-data-integration-project"></a>في مشروع تكامل البيانات

المهمة: **بنود الفاتورة**  

تأكد من تحديث القيمة الافتراضية لحقل Finance and Operations **قيمة عرض الحساب الرئيسي** لمطابقة القيمة المطلوبة.

قيمة القالب الافتراضية هي **401100**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>فواتير الاتفاقيات (Field Service لـ Fin and Ops): رؤوس الفواتير

[![تعيين القالب في تكامل البيانات](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>فواتير الاتفاقيات (Field Service لـ Fin and Ops): بنود الفواتير

[![تعيين القالب في تكامل البيانات](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)

