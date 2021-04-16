---
title: مزامنة فواتير الاتفاقيات في Field Service مع فواتير النص الحر في Supply Chain Management
description: يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فواتير الاتفاقيات في Dynamics 365 Field Service مع فواتير النص الحر في Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f3066741781bd9058e09d7f577a35df4c9b453d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819198"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>مزامنة فواتير الاتفاقيات في Field Service مع فواتير النص الحر في Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة فواتير الاتفاقيات في Dynamics 365 Field Service مع فواتير النص الحر في Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>القوالب والمهام

يتم استخدام القالب والمهام الأساسية التالية لتشغيل مزامنة فواتير الاتفاقيات من Field Service لفواتير النص الحر في Supply Chain Management.

**اسم القالب في تكامل البيانات**

- فواتير الاتفاقيات (Field Service إلى Supply Chain Management)

**أسماء المهام في مشروع تكامل البيانات**

- عناوين الفواتير
- بنود الفاتورة

يجب تنفيذ مهام المزامنة التالية قبل حدوث مزامنة فواتير الاتفاقيات:

- الحسابات (Sales إلى Supply Chain Management) - مباشر

## <a name="entity-set"></a>مجموعة الكيانات

| Field Service  | Supply Chain Management                 |
|----------------|----------------------------------------|
| الفواتير       | رؤوس فاتورة النص الحر لعميل Dataverse |
| invoicedetails | بنود فاتورة النص الحر لعميل Dataverse   |

## <a name="entity-flow"></a>تدفق الكيان

يمكن مزامنة الفواتير التي يتم إنشاؤها من اتفاقية في Field Service مع Supply Chain Management عبر مشروع تكامل بيانات Microsoft Dataverse. ستتم مزامنة تحديثات هذه الفواتير مع فواتير النص الحر في Supply Chain Management إذا كانت حالة المحاسبة للفواتير ذات النص الحر **قيد المعالجة**. بعد ترحيل فواتير النص الحر في Supply Chain Management، وتحديث حالة المحاسبة إلى **مكتمل**، لن تتمكن بعد ذلك من مزامنة التحديثات من Field Service.

## <a name="field-service-crm-solution"></a>حل Field Service CRM

تمت إضافة عمود **لديه بنود في أصل الاتفاقية** إلى جدول **الفاتورة**. يساعد هذا العمود على ضمان مزامنة الفواتير التي تم إنشاؤها من اتفاقية. تكون القيمة **صواب** إذا كانت الفاتورة تحتوي على بند فاتورة واحد على الأقل موجودة أصلاً في اتفاقية.

تمت إضافة عمود **لديه أصل الاتفاقية** إلى جدول **الفاتورة**. يساعد هذا العمود على ضمان مزامنة بنود الفواتير التي تم إنشاؤها من اتفاقية. تكون القيمة **صواب** إذا كان بند الفاتورة نشأ من اتفاقية.

**تاريخ الفاتورة** عبارة عن حقل إلزامي في Supply Chain Management. لذلك، يجب أن يكون للعمود قيمة في Field Service قبل إجراء المزامنة. لتلبية هذا المتطلب، تتم إضافة المنطق التالي:

- إذا كان عمود **تاريخ الفاتورة** فارغًا في جدول **الفاتورة** (بمعنى، في حالة عدم وجود قيمة)، يتم تعيينه إلى التاريخ الحالي عندما تتم إضافة بند فاتورة ينشأ من اتفاقية.
- يمكن للمستخدم تغيير عمود **تاريخ الفاتورة**. ومع ذلك، عندما يحاول المستخدم حفظ فاتورة تنشأ من اتفاقية، فإنه يتلقى خطأ في عملية أعمال إذا كان عمود **تاريخ الفاتورة** فارغاً في الفاتورة.

## <a name="prerequisites-and-mapping-setup"></a>المتطلبات الأساسية وإعداد التعيين

### <a name="in-supply-chain-management"></a>في Supply Chain Management

يجب إعداد أصل فاتورة للتكامل، لتمييز الفواتير ذات النص الحر في Supply Chain Management والتي تم إنشاؤها من فواتير الاتفاقيات في Field Service. عندما تشتمل فاتورة على أصل فاتورة من نوع **تكامل فاتورة الاتفاقية**، يتم عرض حقل **رقم الفاتورة الخارجية** في عنوان **فاتورة المبيعات**.

بالإضافة إلى الظهور في عنوان الفاتورة، يمكن استخدام معلومات **رقم الفاتورة الخارجية** للمساعدة في ضمان تصفية الفواتير التي تم إنشاؤها من فواتير الاتفاقيات في Field Service أثناء مزامنة الفواتير من Supply Chain Management إلى Field Service.

1. انتقل إلى **الحسابات المدينة** \> **الإعداد** \> **أكواد أصل الفاتورة**.
2. حدد **جديد** لإنشاء أصل فاتورة جديد.
3. في حقل **أصل الفاتورة**، أدخل اسمًا لأصل الفاتورة، مثل **FS**.
4. في حقل **الوصف**، أدخل وصفاً، مثل **فاتورة اتفاقية Field Service**.
5. حدد خانة الاختيار **مهمة نوع الأصل**.
6. قم بتعيين حقل **نوع أصل الفاتورة** إلى **تكامل فاتورة الاتفاقية**.
7. حدد **حفظ**.

### <a name="in-the-data-integration-project"></a>في مشروع تكامل البيانات

المهمة: **بنود الفاتورة**  

تأكد من تحديث القيمة الافتراضية لحقل Supply Chain Management **قيمة عرض الحساب الرئيسي** لمطابقة القيمة المطلوبة.

قيمة القالب الافتراضية هي **401100**.

## <a name="template-mapping-in-data-integration"></a>تعيين القالب في تكامل البيانات

تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>فواتير الاتفاقيات (Field Service إلى Supply Chain Management): رؤوس الفواتير

[![تعيين القالب في تكامل البيانات](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>فواتير الاتفاقيات (Field Service إلى Supply Chain Management): بنود الفواتير

[![تعيين القالب في تكامل البيانات](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]