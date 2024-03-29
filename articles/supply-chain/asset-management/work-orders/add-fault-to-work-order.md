---
title: إضافة خطأ إلى أمر العمل
description: يوضح هذا المقال كيفية إضافة تسجيلات أخطاء إلى أوامر العمل في إدارة الأصول.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 210db3259a6c64a508119b30598a34dbda2d2dd2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014987"
---
# <a name="add-fault-to-work-order"></a>إضافة خطأ إلى أمر العمل

[!include [banner](../../includes/banner.md)]



يمكنك إضافة أخطاء تم إعدادها في مصمم الأخطاء إلى أمر عمل. ينبغي ربط سجل خطأ واحد أو أكثر بأنواع الأصول المستخدمة للأصل المحدد في أمر العمل. لمزيد من المعلومات حول كيفية الإعداد، راجع [إدارة الأخطاء‬](../setup-for-work-orders/fault-management.md).

1. حدد **إدارة الأصول** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.

2. حدد أمر العمل لإجراء تسجيل خاطئ عليه، ثم في جزء الإجراء، ضمن علامة التبويب **أمر العمل** ، في مجموعة **الأصل** ، حدد **خطأ في الأصل**.

3. على علامة التبويب السريعة **الأعراض** ، حدد **إضافة بند**. يتم إدخال رقم خطأ متسلسل في حقل **الخطأ** بشكل تلقائي.

4. حدد العَرَض المناسب في حقل **عَرَض الخطأ‬‏‫** .

5. في الحقلين **منطقة الخطأ** و **نوع الخطأ** ، حدد القيم المناسبة.

6. في حقل **تاريخ الخطأ**، يتم إدراج التاريخ الحالي بشكل تلقائي. يمكنك تحديد تاريخ مختلف كما تقتضي الحاجة.

7. على علامة التبويب السريعة **أسباب العَرَض المحدد**، أضف سطرًا  يصف سبب المشكلة.

8. على علامة التبويب السريعة **علاجات العَرَض المحدد** ، أضف سطرًا يصف حلاً محتملاً للمشكلة.

9. حدد **حفظ**.

يبين الرسم التوضيحي أدناه مثالاً على تسجيل الأخطاء.

![الشكل 1.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>عرض أخطاء الأصول

في القائمة **أخطاء الأصول**، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول.

في صفحة قائمة **أخطاء الأصل** ، يمكنك الحصول على نظرة عامة على جميع الأخطاء المسجلة على الأصول. لفتح الصفحة، حدد **إدارة الأصول** > **استعلامات‬** > **خطأ الأصل** > **أخطاء الأصول‏‎**.


## <a name="print-asset-fault-report"></a>طباعة تقارير أخطاء الأصول

من صفحة قائمة **كل الأصول** ، يمكنك طباعة تقرير أخطاء الأصل الذي يعرض جميع تسجيلات الأخطاء بالإضافة إلى نظرة عامة رسومية لإحصاءات الخطأ.

1. حدد **إدارة الأصول** > **الأصول** > **كافة الأصول**.

2. حدد الأصل لطباعة تقرير الخطأ له.

3. في جزء الإجراءات، على علامة التبويب **عام** ، في مجموعة **تقارير** ، حدد **خطأ الأصل**.

4. أدخل فترة معينة، أو حدد نوع الخطأ.

5. حدد **موافق** لطباعة التقرير.

>[!NOTE]
>لطباعة تقرير الأخطاء للعديد من الأصول أو أنواع الأصول، حدد **إدارة الأصول** > **التقارير** > **الأصول‏‎** > **خطأ الأصل**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]