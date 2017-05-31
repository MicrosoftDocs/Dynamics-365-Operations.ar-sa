---
title: "تسوية الشحن في إدارة النقل"
description: "توضح هذه المقالة عملية تسوية الشحن."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 88633426fd23370f64730480629ab33ad7124812
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>تسوية الشحن في إدارة النقل

[!include[banner](../includes/banner.md)]


توضح هذه المقالة عملية تسوية الشحن.

يمكن تسوية الشحن يدويًا، أو يمكن إعدادها بحيث تحدث تلقائيًا. لاستخدام تسوية الشحن التلقائية، يجب إعداد السجل الرئيسي للتدقيق‬ حيث يمكنك تعريف المعايير التي تحدد فواتير الشحن التي تتم مطابقتها تلقائيًا.

## <a name="the-freight-reconciliation-process"></a>عملية تسوية الشحن
يتم حساب أسعار الشحن بواسطة محرك الشحن الذي يقترن بشركة الشحن ذات الصلة. عندما يتم تأكيد الحمل, يتم إنشاء فاتورة الشحن وتُنقل إليها أسعار الشحن. ,يتم تقسيم أسعار الشحن كتكاليف متنوعة في المستند المصدر ذي الصلة (أمر الشراء و/أو أمر المبيعات و/أو أمر التحويل)، بالاستناد إلى الإعداد المستخدم لعملية الفوترة العادية. بإمكان عملية تسوية الشحن (وتُعرف أيضًا بعملية المطابقة) أن تبدأ فور وصول فاتورة الشحن من شركة الشحن. يمكنك تلقي الفاتورة إلكترونيًا أو على الورق. في حالة تلقي الفاتورة على الورق، يمكنك إنشاء فاتورة إلكترونية باستخدام فاتورة الشحن كقالب. 

[![عملية تسوية الشحن](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>التسوية اليدوية
إذا كنت تعمل على تسوية الشحن يدويًا، فيجب عليك مطابقة كل بند في الفاتورة مع بند أو بنود فاتورة الشحن للحمل الجاري فوترته. ستجري هذه مطابقة في صفحة **مطابقة فاتورة الشحن والفاتورة‬**. إذا لم يتطابق المبلغ في بند الفاتورة مع مبلغ فاتورة الشحن، فيجب تحديد سبب تسوية للفرق. في حال وجود أسباب متعددة للتسوية، يمكنك تقسيم المبلغ غير المتطابق فيما بينها. يحدد سبب التسوية كيفية ترحيل مبالغ الفروقات في دفتر الأستاذ العام. عندما يتم حساب تسوية مبلغ الفاتورة بالكامل، يتم إرساله للموافق عليه، ثم يتم ترحيل دفتر اليومية. يعرض التوضيح التالي كيفية إنشاء فاتورة شحن وإجراء تسوية الشحن في Microsoft Dynamics 365 for Operations. 
[![مهام تسوية الشحن في Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>التسوية التلقائية
لاستخدام التسوية التلقائية، يجب تحديد جدول للتسوية، والفواتير وشركات الشحن التي يجب استخدامها. تتم مطابقة بنود الفواتير وفواتير الشحن وفقًا لإعداد السجل الرئيسي للتدقيق‬ ونوع فاتورة الشحن. بعد تشغيل التسوية التلقائية، يجب معالجة الفواتير التي يتعذر على النظام مطابقتها. بعد ذلك، يجب معالجة هذه الفواتير يدويًا قبل أن تتمكن من ترحيل كافة الفواتير للدفع.




