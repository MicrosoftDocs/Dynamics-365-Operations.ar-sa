---
title: إنشاء سير عمل طلب شراء إجازة وبيعها
description: إنشاء سير عمل لطلب شراء إجازة وبيعها لإدارة طلبات شراء وبيع الإجازة بشكل مستمر في Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417165"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>إنشاء سير عمل طلب شراء إجازة وبيعها

يمكنك إنشاء سير عمل في Dynamics 365 Human Resources لإدارة طلبات شراء وبيع الإجازة. يتيح لك سير عمل **شراء وبيع الإجازة** ما يلي:

- تعريف المهام
- تحديد من يجب أن يقوم بإكمال المهام
- تحديد من يمكنه الموافقة على الطلبات أو رفضها

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>إنشاء سير عمل طلب شراء إجازة وبيعها

1. في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.

2. ضمن **الإعداد**، حدد **سير عمل الموارد البشرية**.

3. حدد **جديد** ، ثم حدد **شراء وبيع طلب إجازة**. 

4. عند ظهور مربع الرسالة **هل تريد فتح هذا الملف؟**، حدد **فتح** وتسجيل الدخول باستخدام بيانات اعتماد الشركة الخاصة بك.

5. استخدم محرر سير العمل لإنشاء سير عمل لطلبات الإجازة الخاصة بك. لمزيد من المعلومات حول العمل مع مهام سير العمل، راجع [إنشاء نظرة عامة حول مهام سير العمل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

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

- استخدم **مرسل بواسطة الموارد البشرية‬‏‫** و **مرسل بواسطة المدير‬‏‫** في إجراء تلقائي للموافقة تلقائيا علي طلبات شراء وبيع الإجازة التي تُرسلها هذه الأدوار نيابة عن الموظفين. لمزيد من المعلومات حول الإجراءات التلقائية، راجع [‏‫‏‫تكوين عمليات الاعتماد في سير عمل‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- استخدم **نوع الإجازة** في عبارة شرطية أو إجراء تلقائي للتحكم في كيفيه قيام سير العمل بتوجيه الطلبات بأنواع إجازة معينة.

## <a name="see-also"></a>راجع أيضًا

[نظرة عامة على الإجازة والغياب](hr-leave-and-absence-overview.md)<br>
[إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]