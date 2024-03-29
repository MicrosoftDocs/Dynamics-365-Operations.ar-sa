---
title: إنشاء سير عمل طلب شراء إجازة وبيعها
description: إنشاء سير عمل لطلب شراء إجازة وبيعها لإدارة طلبات شراء وبيع الإجازة بشكل مستمر في Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fabe2333bbf76edf31b77c0d5fce044273333de2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869796"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>إنشاء سير عمل طلب شراء إجازة وبيعها


>[!Important]
>تتوفر الوظيفة المذكورة في هذة المقالة حاليًا للعملاء في Dynamics 365 Human Resources المستقل. ستتوفر بعض الوظائف أو كلها كجزء من الإصدار المستقبلي على بنية Finance الأساسية بعد إصدار 10.0.26 من Finance.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يمكنك إنشاء سير عمل في Dynamics 365 Human Resources لإدارة طلبات شراء وبيع الإجازة. يتيح لك سير عمل **شراء وبيع الإجازة** ما يلي:

- تعريف المهام
- تحديد من يجب أن يقوم بإكمال المهام
- تحديد من يمكنه الموافقة على الطلبات أو رفضها

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>إنشاء سير عمل طلب شراء إجازة وبيعها

1. في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.

2. ضمن **الإعداد**، حدد **سير عمل الموارد البشرية**.

3. حدد **جديد** ، ثم حدد **شراء وبيع طلب إجازة**. 

4. عند ظهور مربع الرسالة **هل تريد فتح هذا الملف؟**، حدد **فتح** وتسجيل الدخول باستخدام بيانات اعتماد الشركة الخاصة بك.

5. استخدم محرر سير العمل لإنشاء سير عمل لطلبات الإجازة الخاصة بك. لمزيد من المعلومات حول العمل مع مهام سير العمل، راجع [إنشاء نظرة عامة حول مهام سير العمل](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>عناصر بيانات سير عمل طلب إجازة وغياب

يمكنك استخدام عناصر البيانات التالية لإنشاء الموافقات الشرطية أو التلقائية في عمليات سير العمل لطلبات بيع وشراء الإجازة:

- **المبلغ**
- **سياسة شراء الإجازة وبيعها**
- **الشركة**
- **تم الإنشاء بواسطة**
- **تاريخ  ووقت الإنشاء**
- **تاريخ الانتهاء**
- **نوع الإجازة**
- **تعديل بواسطة**
- **تاريخ ووقت التعديل**
- **معرف الطلب**
- **تاريخ البدء**
- **الحالة** 
- **تاريخ الإرسال**
- **مُرسل بواسطة**
- **مرسل بواسطة الموارد البشرية**
- **مرسل بواسطة المدير**
- **تم الإرسال بالنيابة**
- **العامل**

## <a name="workflow-examples"></a>أمثلة سير العمل

تظهر هذه الأمثله كيف يمكنك إنشاء أنواع مختلفة من شروط سير العمل باستخدام عناصر البيانات هذه:

- استخدم **مرسل بواسطة الموارد البشرية‬‏‫** و **مرسل بواسطة المدير‬‏‫** في إجراء تلقائي للموافقة تلقائيا علي طلبات شراء وبيع الإجازة التي تُرسلها هذه الأدوار نيابة عن الموظفين. لمزيد من المعلومات حول الإجراءات التلقائية، راجع [‏‫‏‫تكوين عمليات الاعتماد في سير عمل‬](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- استخدم **نوع الإجازة** في عبارة شرطية أو إجراء تلقائي للتحكم في كيفيه قيام سير العمل بتوجيه الطلبات بأنواع إجازة معينة.

## <a name="see-also"></a>راجع أيضًا

[نظرة عامة على الإجازة والغياب](hr-leave-and-absence-overview.md)<br>
[إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
