---
title: إضافة خطأ إلى أمر عمل
description: يوضح هذا الموضوع كيفية إضافة تسجيلات أخطاء إلى أوامر العمل في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 083ceca9605ad044c172ba7aa23739d170f8c301
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019294"
---
# <a name="add-fault-to-work-order"></a>إضافة خطأ إلى أمر العمل

[!include [banner](../../includes/banner.md)]



يمكنك إضافة أخطاء تم إعدادها في مصمم الأخطاء إلى أمر عمل. ينبغي ربط سجل خطأ واحد أو أكثر بأنواع الأصول المستخدمة للأصل المحدد في أمر العمل. لمزيد من المعلومات حول كيفية الإعداد، راجع [إدارة الأخطاء‬](../setup-for-work-orders/fault-management.md).

1. حدد **إدارة الأصول** > **مشترك** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.

2. حدد أمر العمل لإجراء تسجيل خاطئ عليه، ثم في جزء الإجراء، ضمن علامة التبويب **أمر العمل** ، في مجموعة **الأصل** ، حدد **خطأ في الأصل**.

3. على علامة التبويب السريعة **الأعراض** ، حدد **إضافة بند**. يتم إدخال رقم خطأ متسلسل في حقل **الخطأ** بشكل تلقائي.

4. حدد العَرَض المناسب في حقل **عَرَض الخطأ‬‏‫** .

5. في الحقلين **منطقة الخطأ** و **نوع الخطأ** ، حدد القيم المناسبة.

6. في حقل **تاريخ الخطأ**، يتم إدراج التاريخ الحالي بشكل تلقائي. يمكنك تحديد تاريخ مختلف كما تقتضي الحاجة.

7. على علامة التبويب السريعة **أسباب العَرَض المحدد**، أضف سطرًا  يصف سبب المشكلة.

8. على علامة التبويب السريعة **علاجات العَرَض المحدد** ، أضف سطرًا يصف حلاً محتملاً للمشكلة.

9. حدد **حفظ**.

يبين الرسم التوضيحي أدناه مثالاً على تسجيل الأخطاء.

![الشكل 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>عرض أخطاء الأصول

في القائمة **أخطاء الأصول**، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول.

في صفحة قائمة **أخطاء الأصل** ، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول. لفتح الصفحة، حدد **إدارة الأصول** > **استعلامات‬** > **خطأ الأصل** > **أخطاء الأصول‏‎**.


## <a name="print-asset-fault-report"></a>طباعة تقارير أخطاء الأصول

من صفحة قائمة **كل الأصول** ، يمكنك طباعة تقرير أخطاء الأصل الذي يعرض جميع تسجيلات الأخطاء بالإضافة إلى نظرة عامة رسومية لإحصاءات الخطأ.

1. حدد **إدارة الأصول** > **مشترك** > **الأصول** > **كافة الأصول**.

2. حدد الأصل لطباعة تقرير الخطأ له.

3. في جزء الإجراءات، على علامة التبويب **عام** ، في مجموعة **تقارير** ، حدد **خطأ الأصل**.

4. أدخل فترة معينة، أو حدد نوع الخطأ.

5. حدد **موافق** لطباعة التقرير.

>[!NOTE]
>لطباعة تقرير الأخطاء للعديد من الأصول أو أنواع الأصول، حدد **إدارة الأصول** > **التقارير** > **الأصول‏‎** > **خطأ الأصل**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]