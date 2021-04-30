---
title: إعادة تعيين المهام الدفعية العالقة
description: يشرح هذا الموضوع كيفية حل المشكلات المتعلقة بالوظائف الدفعية المتوقفة.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881750"
---
# <a name="reset-stuck-batch-jobs"></a>إعادة تعيين المهام الدفعية العالقة

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>إصدار

يمكن أن يواجه Microsoft Dynamics 365 Human Resources مشكلات في وظائف الدفعات المتوقفة إما في حالة **قيد التنفيذ** أو **قيد الإلغاء** ولم تكتمل.

## <a name="resolution"></a>الدقة

عندما تكون وظيفة الدفعة متوقفة في حالة **قيد التنفيذ** أو **قيد إلغاء**، يمكنك إعادة تعيين الحالة من خلال فرض إلغاء الوظيفة. وبعد إلغائها، يمكنك إعادة تعيين وظيفة الدفعة عن طريق تعيينها على حالة **قيد الانتظار**. سيتم بعد ذلك انتقاؤها مرة أخرى للتنفيذ في تشغيل الدُفعة المجدولة التالي.

1. في مساحة عمل **إدارة النظام**، حدد صفحة **الارتباطات**، وحدد **وظائف الدفعات**.

2. في صفحة قائمة **وظيفة الدفعة**، حدد الوظيفة التي تحتاج إلى إعادة التعيين.

3. على شريط الاجراء، حدد **فرض الإلغاء**، وقم بتأكيد الإجراء.

   > [!NOTE]
   > يتوفر إجراء **فرض الإلغاء** فقط عندما تكون حالة وظيفة الدفعة المحددة هي إما **قيد التنفيذ** أو **قيد الإلغاء**، ولا يتم تشغيل عمليات تنفيذ الدفعة أو إلغائها للوظيفة.

4. على شريط الإجراء، حدد **تغيير الحالة**.

5. في صفحة **تحديد الحالة الجديدة**، حدد **قيد الانتظار**، ثم حدد **موافق**.

   ![تحديد حالة وظيفة دفعة جديدة](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>راجع أيضًا

[تحسين الأداء عن طريق جدولة الوظائف الدُفعية بعد الساعات](hr-admin-troubleshooting-batch-jobs.md)<br>
[تحسين الأداء باستخدام مهام التنظيف التلقائية](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
