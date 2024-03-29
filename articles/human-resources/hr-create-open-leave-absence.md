---
title: إنشاء إجازة غياب مفتوحة النهاية
description: تشرح هذه المقالة كيفية إنشاء إجازة غياب مفتوحة في Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805332"
---
# <a name="create-an-open-ended-leave-of-absence"></a>إنشاء إجازة غياب مفتوحة النهاية

> [!IMPORTANT]
> ستتوفر الوظيفة الموضحة في هذه المقالة على البنية الأساسية المالية كجزء من إصدار مستقبلي بعدإصدار Microsoft Dynamics 365 Finance 10.0.31.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يمكنك إرسال طلبات الحصول على إجازة مفتوحة وعرض حالة طلبات الإجازة الخاصة بك في Dynamics 365 Human Resources.

## <a name="prerequisites"></a>المتطلبات الأساسية

1. ضمن **إدارة الميزات**، تأكد من تشغيل ميزة **الإجازة المفتوحة**.

    > [!IMPORTANT]
    > لا يمكن إيقاف تشغيل هذه الميزة بعد تشغيلها.

2. قم بإنشاء نوع إجازة الغياب.
3. أدخل التفاصيل مثل نوع الإجازة والوصف ومعرف سير العمل.
4. في حقل **نوع الطلب** ، حدد **إجازة الغياب**.
5. في قسم التفاصيل، للأوراق المفتوحة، قم بتعيين الخيار **ذات نهاية مفتوحة** إلى **نعم**.
6. قم بتعيين الخيار **العودة إلى إشعار العمل** إلى **نعم** أو **لا**.
7. يمكن طلب إشعار العودة إلى العمل اختياريًا لطلبات الإجازة المفتوحة.

> [!NOTE]
> بعد تمكين هذه الميزة، سيتم تمكين ميزة **المرفقات المطلوبة** .

## <a name="request-an-open-ended-leave-of-absence"></a>اطلب إجازة غياب مفتوحة

1. في مساحة عمل **الخدمة الذاتية للموظف**، في لوحة **أرصدة الوقت المستقطع**، حدد **المزيد (...)**.
2. لإرسال طلب إجازة، حدد **طلب إجازة غياب**.
3. أدخل المعلومات في الحقلين **نوع الإجازة** و **تاريخ البدء** . في الحقل **تاريخ الانتهاء**، أدخل تاريخ انتهاء مبدئيًا.
4. إذا كان يجب عليك إرسال المستندات الداعمة، ضمن **المرفقات**، حدد **تحميل**.
5. إذا كنت جاهزًا لإرسال طلبك، فحدد **إرسال**. وإلا، حدد **حفظ المسودة**.
6. لتحديث طلب إجازة مفتوح، حدد الطلب، وأدخل **تاريخ انتهاء** في حقل تاريخ الانتهاء، وقم بتعيين خيار **تأكيد تاريخ الانتهاء** إلى **نعم**، وقم بتحميل الوثائق.
7. إذا تم تعيين الخيار **إشعار العودة إلى العمل** إلى **نعم**، فحدد **تحميل**، ثم حدد خانة الاختيار لتأكيد تحميل إشعار عودة إلى العمل صالح.
8. عندما يتم إدخال جميع التفاصيل، حدد **إرسال**.
