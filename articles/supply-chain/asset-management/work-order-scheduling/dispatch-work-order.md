---
title: إرسال أمر العمل
description: يوضح هذا المقال كيفية إرسال أمر عمل في إدارة الأصول.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f78e8642715b0c3fd3d01e8072645ccd9c58d685
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016844"
---
# <a name="dispatch-work-order"></a>إرسال أمر العمل

[!include [banner](../../includes/banner.md)]

 

يمكنك جدولة أمر عمل واحد أو مهام أوامر عمل إلى عامل واحد باستخدام الوظيفة **إرسال**.

1. انقر فوق **إدارة الأصول** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.

2. حدد أمر العمل في القائمة.

3. في علامة التبويب **عام**، انقر فوق **إرسال**.

4. في مربع الحوار **جدولة أمر العمل** ، حدد العامل في حقل **العامل** .

5. في حقل **جدولة الساعات**، يمكنك إدخال ساعات العمل المتوقعة في حال كانت ساعات العمل المتوقعة تختلف عن الساعات المتنبأ بها.

6. في حقل **البداية المجدولة**، يمكنك تحرير تاريخ ووقت البدء إذا لزم الأمر.

7. إذا كان من الضروري أن تأخذ عملية الجدولة في الاعتبار القيود على القدرة الإنتاجية فيما يتعلق بالموارد المجدولة مسبقًا لمهام أخرى، فمن ثم تأكد من تعيين أزرار التبديل **الأصل**، و **الأداة**، و **العامل** إلى **نعم**. إذا أردت الاطلاع على معلومات مفصلة حول عملية الجدولة، حدد **نعم** على زر التبديل **مطولّ‬** . وهذا يعني أن معلومات تفصيلية حول الدرجات المحسوبة على أمر العمل سوف تظهر في سجل المعلومات.

8. حدد **نعم** في زر التبديل **تجاهل الجدولة** لتجاهل الأيام المغلقة في التقويم (ينطبق ذلك على الأصل والعامل والأدوات). حدد **نعم** في زر التبديل **تجاهل التنفيذ المجدول** لتجاهل القيود التي قد يكون تم تحديدها في أمر العمل فيما يتعلق بالجدولة. 

    راجع قسم [التنفيذ المجدول](../setup-for-work-orders/scheduled-execution.md) للحصول على معلومات حول إعداد التنفيذ المجدول.

9. انقر فوق **موافق**. يتم تحديث حالة دورة حياة أمر العمل تلقائيًا إلى حالة دورة الحياة **المجدولة** المحددة في **إدارة الأصول** > **الإعداد** > **أوامر العمل** > **نماذج دورة الحياة**.

يعرض الشكل المبين أدناه مثالاً حول تحديدات الإرسال في مربع الحوار **جدولة أمر العمل**.

![الشكل 1.](media/04-work-order-scheduling.png)

[!NOTE]
إذا كنت ترغب في حذف الجدولة في أمر العمل، يتم إجراء ذلك عن طريق تحديد أمر العمل في **كافة أوامر العمل**، والنقر فوق **حذف الجدولة** في علامة التبويب **عام** . تذكر تحديث أمر العمل يدويًا حالة دورة حياة أمر العمل إذا قمت بحذف الجدولة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]