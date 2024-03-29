---
title: إعادة تعيين الوظائف الدفعية العالقة
description: توضح هذه المقالة كيفية حل المشكلات المتعلقة بالوظائف الدفعية المتوقفة.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896007"
---
# <a name="reset-stuck-batch-jobs"></a>إعادة تعيين المهام الدفعية العالقة


[!INCLUDE [PEAP](../includes/peap-2.md)]

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

   ![تحديد حالة وظيفة دفعة جديدة.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>راجع أيضًا

[تحسين الأداء عن طريق جدولة الوظائف الدُفعية بعد الساعات](hr-admin-troubleshooting-batch-jobs.md)<br>
[تحسين الأداء باستخدام مهام التنظيف التلقائية](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
