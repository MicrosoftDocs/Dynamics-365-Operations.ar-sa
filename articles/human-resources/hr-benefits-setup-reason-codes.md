---
title: إعداد أكواد السبب
description: يستخدم Dynamics 365 Human Resources رموز السبب لتوضيح سبب تغيير ميزات الموظف.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 692bd5acd574492526644849fb555e5856b4463f
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323408"
---
# <a name="set-up-reason-codes"></a>إعداد أكواد السبب

يستخدم Dynamics 365 Human Resources رموز السبب لتوضيح سبب تغيير ميزات الموظف.

> [!NOTE]
> اعتبارا من يناير 2021، تم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** بدلاً من مساحة عمل **إدارة الميزات**. لمزيد من المعلومات، راجع [ترحيل أكواد السبب يدويًا إلى إدارة العاملين](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>إنشاء أكواد سبب

1. في مساحة عمل **إدارة العاملين** (أو مساحة عمل **إدارة الميزات** إذا لم يتم ترحيل أكواد السبب الخاصة بك)، فحدد **الارتباطات**، ثم حدد **أكواد السبب**.

2. حدد **جديد**.

3. حدد قيمًا للحقول التالية:

   | الحقل | ‏‏الوصف |
   | --- | --- |
   | **رمز السبب** | اسم فريد لتحديد السبب الذي من أجله قام الموظف بتغيير تسجيل خطة الميزة. |
   | **‏‏الوصف** | وصف كود السبب. |

4. ضمن **السيناريوهات القابلة للتطبيق**، قم بتعيين **إدارة الميزات** إلى **نعم**. (غير قابل للتطبيق إذا لم يتم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين**.)

5. حدد **حفظ**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>ترحيل أكواد السبب يدويًا إلى إدارة العاملين

في يناير 2021، تم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** بدلاً من مساحة عمل **إدارة الميزات**. سيتم تلقائيًا ترحيل معظم بيانات أكواد السبب في البيئة الخاصة بك. وقد لا يتم ترحيل بعض بيانات كود السبب. على سبيل المثال، تحتوي أكواد الأسباب الآن على حد أقصى 15 حرفًا، لذلك لن يتم ترحيل أي أكواد سبب أطول من 15 حرفًا تلقائيًا.

ستشاهد شعارًا على صفحة **الارتباطات** بمساحة عمل **إدارة الميزات** لاعلامك بالترحيل وما إذا كانت أي أكواد سبب لم يتم ترحيلها.

1. حدد **أكواد السبب** للاطلاع على التفاصيل المتعلقة بحالة الترحيل.

   [![رموز السبب.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. حدد كود سبب الفشل في الترحيل.

   [![حالة ترحيل كود السبب.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. حدد **كود سبب الترحيل**.

   [![ترحيل رمز السبب.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. في جزء **ترحيل كود سبب الميزة**، يتوفر لديك خياران للتعيين إلى كود سبب إدارة العاملين:

   - لاستخدام كود سبب موجود في إدارة العاملين، اختر واحدًا من القائمة المنسدلة **استخدام كود السبب الموجود**.
     > [!NOTE]
     > يمكنك فقط استخدام كود سبب موجود في إدارة العاملين إذا لم يتم ترحيل كود سبب إدارة ميزات آخر إليه.
   - لإنشاء كود سبب جديد في إدارة العاملين، أدخل اسمًا جديدًا في **كود السبب الجديد**، ثم أدخل وصفا في **الوصف الجديد**.

   [![التعيين إلى كود سبب إدارة العاملين.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

بعد ترحيل أكواد السبب إلى إدارة العاملين، يتم تعيين الخيار الخاص باستخدامها في إدارة الميزات تلقائيًا إلى **نعم**.

[![استخدام أكواد السبب في إدارة الميزات.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
