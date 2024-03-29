---
title: حساب القدرة الإنتاجية على أوامر العمل المجدولة
description: يوضح هذا المقال كيفية حساب القدرة الإنتاجية على أوامر العمل المجدولة في إدارة الأصول.
author: johanhoffmann
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857942"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>حساب القدرة الإنتاجية على أوامر العمل المجدولة

[!include [banner](../../includes/banner.md)]

 

يمكنك حساب القدرة الإنتاجية على أوامر العمل المجدولة للحصول على نظرة عامة حول حمل العمل على الموارد لفترة محددة. يمكن إجراء الحسابات للموارد التالية: عاملو الصيانة ومجموعات العاملين والأدوات والأصول.

1. انقر فوق **إدارة الأصول** > **استعلامات** > **الجدول** > **القدرة الإنتاجية**.

2. في مربع الحوار **حساب‏‎ القدرة الإنتاجية** > الحقل **إظهار** ، حدد نوع الحمل الذي تريد حسابه: **القدرة**، **المحجوز** أو **المتبقي‬**.

3. حدد **نعم** على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج التي تحتوي على صفر.

4. حدد أنواع الموارد التي ترغب في حساب القدرة الإنتاجية لها من خلال تحديد **نعم** على أزرار التبديل الملائمة: **العامل**، و **مجموعة عاملي الصيانة**، و **الأداة**، و **الأصل**.

5. حدد تاريخ بدء الحساب في الحقل **من تاريخ**.

6. في الحقل **نوع الفاصل الزمني** ، حدد الفاصل الزمني للحساب: **يوم**، أو **أسبوع**، أو **شهر**، أو **ربع السنة**.

7. في الحقل **تكرار الفترة‬**، أدخل عدد الفواصل الزمنية التي تريد حسابها. على سبيل المثال، إذا حددت **يوم** كنوع فاصل زمني، وأدرجت الرقم "5" في هذا الحقل، سيتم إجراء حساب خمسة أيام من تاريخ البدء.

8. انقر فوق **موافق** لبدء الحساب.

يظهر الشكل أدناه نتيجة الحساب الذي يغطي ثلاثة أسابيع لنوع حمل العمل **محجوز**.

![الشكل 1.](media/08-work-order-scheduling.png)

[!NOTE]
إذا قمت بتحديد أنواع حمل العمل **القدرة** أو **المتبقي** لعملية الحساب، فستظهر النتيجة نفسها إذا لم يتم إجراء أي حجوزات للموارد في الفترة المحددة.

للحصول على معلومات حول كيفيه حساب القدرة الإنتاجية على بنود جدول الصيانة وليس على أوامر العمل المجدولة، راجع [حساب القدرة الإنتاجية](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]