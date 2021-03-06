---
title: إعداد أكواد السبب
description: يستخدم Dynamics 365 Human Resources رموز السبب لتوضيح سبب تغيير ميزات الموظف.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae82c8312d344f5380adec8413766304681a0a05
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111317"
---
# <a name="set-up-reason-codes"></a>إعداد أكواد السبب

يستخدم Dynamics 365 Human Resources رموز السبب لتوضيح سبب تغيير ميزات الموظف.

> [!NOTE]
> اعتبارا من يناير 2021، يتم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** بدلا من مساحة عمل **إدارة الميزات**. لمزيد من المعلومات، راجع [ترحيل أكواد السبب يدويًا إلى إدارة العاملين](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>إنشاء أكواد سبب

1. في مساحة عمل **إدارة العاملين** (أو مساحة عمل **إدارة الميزات** إذا لم يتم ترحيل أكواد السبب الخاصة بك بعد) ، حدد **الارتباطات**، ثم حدد **أكواد السبب**.

2. حدد **جديد**.

3. حدد قيمًا للحقول التالية:

   | الحقل | ‏‏الوصف |
   | --- | --- |
   | **رمز السبب** | اسم فريد لتحديد السبب الذي من أجله قام الموظف بتغيير تسجيل خطة الميزة. |
   | **‏‏الوصف** | وصف كود السبب. |

4. ضمن **السيناريوهات القابلة للتطبيق**، قم بتعيين **إدارة الميزات** إلى **نعم**. (غير قابل للتطبيق إذا لم يتم بعد ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** .)

5. حدد **حفظ**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>ترحيل أكواد السبب يدويًا إلى إدارة العاملين

في يناير 2021، يتم ترحيل أكواد السبب إلى مساحة عمل **إدارة العاملين** بدلا من مساحة عمل **إدارة الميزات**. سيتم تلقائيًا ترحيل معظم بيانات أكواد السبب في البيئة الخاصة بك. وقد لا يتم ترحيل بعض بيانات كود السبب. على سبيل المثال، تحتوي أكواد الأسباب الآن على حد أقصى 15 حرفًا، لذلك لن يتم ترحيل أي أكواد سبب أطول من 15 حرفًا تلقائيًا.

ستشاهد شعارًا على صفحة **الارتباطات** بمساحة عمل **إدارة الميزات** لاعلامك بالترحيل وما إذا كانت أي أكواد سبب لم يتم ترحيلها.

1. حدد **أكواد السبب** للاطلاع على التفاصيل المتعلقة بحالة الترحيل.

   [![رموز السبب](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. حدد كود سبب الفشل في الترحيل.

   [![حالة ترحيل كود السبب](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. حدد **كود سبب الترحيل**.

   [![ترحيل رمز السبب](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. في جزء **ترحيل كود سبب الميزة**، يتوفر لديك خياران للتعيين إلى كود سبب إدارة العاملين:

   - لاستخدام كود سبب موجود في إدارة العاملين، اختر واحدًا من القائمة المنسدلة **استخدام كود السبب الموجود**.
     > [!NOTE]
     > يمكنك فقط استخدام كود سبب موجود في إدارة العاملين إذا لم يتم ترحيل كود سبب إدارة ميزات آخر إليه.
   - لإنشاء كود سبب جديد في إدارة العاملين، أدخل اسمًا جديدًا في **كود السبب الجديد**، ثم أدخل وصفا في **الوصف الجديد**.

   [![التعيين إلى كود سبب إدارة العاملين](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

بعد ترحيل أكواد السبب إلى إدارة العاملين، يتم تعيين الخيار الخاص باستخدامها في إدارة الميزات تلقائيًا إلى **نعم**.

[![استخدام أكواد السبب في إدارة الميزات](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]