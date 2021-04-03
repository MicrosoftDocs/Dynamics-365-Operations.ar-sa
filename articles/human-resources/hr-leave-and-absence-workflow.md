---
title: إنشاء سير عمل طلب إجازة
description: إنشاء سير عمل لطلب أجازه وغياب لأداره طلبات الإجازات بشكل مستمر في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c2020c68c4aca3594a2532d32f968ab76f6b7b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463300"
---
# <a name="create-a-leave-request-workflow"></a>إنشاء سير عمل طلب إجازة

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يمكنك إنشاء سير عمل في Dynamics 365 Human Resources لإدارة طلبات الإجازة والغياب بشكل مستمر. يتيح لك سير عمل **الإجازة والغياب** ما يلي:

- تعريف المهام
- تحديد من يجب أن يقوم بإكمال المهام
- تحديد من يمكنه الموافقة على الطلبات أو رفضها

## <a name="create-a-leave-and-absence-request-workflow"></a>إنشاء سير عمل طلب إجازة وغياب

1. في صفحة **‏‫الإجازة والغياب‬** حدد علامة التبويب **الارتباطات**.

2. ضمن **الإعداد**، حدد **سير عمل الموارد البشرية**.

3. حدد **جديد‬**، ثم حدد **طلب الإجازة والغياب**. 

4. عند ظهور مربع الرسالة **هل تريد فتح هذا الملف؟**، حدد **فتح** وتسجيل الدخول باستخدام بيانات اعتماد الشركة الخاصة بك.

5. استخدم محرر سير العمل لإنشاء سير عمل لطلبات الإجازة الخاصة بك. لمزيد من المعلومات حول العمل مع مهام سير العمل، راجع [إنشاء نظرة عامة حول مهام سير العمل](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>عناصر بيانات سير عمل طلب إجازة وغياب

يمكنك استخدام عناصر البيانات التالية لإنشاء الموافقات الشرطية أو التلقائية في عمليات سير العمل لطلبات الإجازة والغياب:

- **المبلغ**
- **تعليق**
- **الشركة**
- **تم الإنشاء بواسطة**
- **تاريخ  ووقت الإنشاء**
- **تاريخ الإنهاء**
- **نوع الإجازة**
- **تعديل بواسطة**
- **تاريخ ووقت التعديل**
- **رمز السبب**
- **معرف الطلب**
- **تاريخ البدء**
- **الحالة** 
- **تاريخ الإرسال**
- **مُرسل بواسطة**
- **مرسل بواسطة الموارد البشرية**
- **مرسل بواسطة المدير**
- **تم الإرسال بالنيابة**
- **العامل**
- **نوع العامل**

تظهر هذه الأمثله كيف يمكنك إنشاء أنواع مختلفة من شروط سير العمل باستخدام عناصر البيانات هذه:

- استخدم **كود السبب** في العبارة الشرطية لتوجيه طلبات الإجازات المرضية مع كود السبب **جراحة** إلى الموارد البشرية للموافقة، بينما يتم توجيه كافة أكواد الأسباب الأخرى إلى المدير. لمزيد من المعلومات حول العبارات الشرطية، راجع [‏‫تكوين القرارات الشرطية في سير عمل‬‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow). 

- استخدم **مرسل بواسطة الموارد البشرية‬‏‫** و **مرسل بواسطة المدير‬‏‫** في إجراء تلقائي للموافقة تلقائيا علي طلبات الإجازات التي تُرسلها هذه الأدوار نيابة عن الموظفين. لمزيد من المعلومات حول الإجراءات التلقائية، راجع [‏‫‏‫تكوين عمليات الاعتماد في سير عمل‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- استخدم **نوع الإجازة** في عبارة شرطية أو إجراء تلقائي للتحكم في كيفيه قيام سير العمل بتوجيه الطلبات بأنواع إجازة معينة.

## <a name="see-also"></a>راجع أيضًا

- [نظرة عامة على الإجازة والغياب](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]