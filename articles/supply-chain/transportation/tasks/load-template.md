---
title: قوالب حمل العمل
description: يصف هذا الموضوع كيفية إعداد قوالب حمل وكيفية إقران قالب تحميل بشحنة جديدة.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0a4070a1dd5d53bb502ba2ab0c91dbdc90ded34d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005042"
---
# <a name="load-templates"></a>قوالب حمل العمل

عند إنشاء تحميل جديد ، يمكنك تعيين قالب تحميل. يحتوي قالب التحميل علي معلومات حول المعدات ، وحول المقاييس مثل الارتفاع والعرض والعمق وحجم الحمل.

يصف هذا الموضوع كيفية إعداد قوالب حمل وكيفية إقران قالب تحميل بشحنة جديدة.

## <a name="set-up-a-load-template"></a>إعداد قالب حمل العمل

1. انتقل إلى **أداره النقل \> إعداد \> بناء التحميل \> قالب التحميل**.
1. في جزء الاجراء، حدد **جديد** لأضافه قالب جديد **تحرير** لتحرير قالب موجود.
1. في الصف الخاص بالقالب الجديد أو الموجود ، قم بتعيين الحقول التالية:

    - **معرف قالب التحميل** - إدخال معرف فريد (ID) لقالب التحميل.
    - **المعدات** – تحديد المعدات التي ينبغي استخدامها لشحن الحمل.
    - **ارتفاع التحميل** و **عرض التحميل** و **عمق التحميل** – إدخال ابعاد التحميل.
    - **الحد الأقصى لكميه التحميل** و **الحد الأقصى لوزن الحمل المسموح به** – إدخال الحد الأقصى لحجم الحمل والوزن المسموح به للتحميل.
    - **الحد الأقصى لوزن الإنتاجي المسموح به** – إدخال الحد الأقصى المسموح به لإجمالي وزن الحمل. ‏‫الوزن الإجمالي للحمل يشمل كلِ من وزن الفارغ ووزن التحميل.
    - **الحد الأقصى لعدد قطع الشحن المسموح بها** – إدخال الحد الأقصى لعدد أجزاء الشحن التي يمكن ان يحتويها التحميل.
    - **تحميل المكدس عند الارضيه** – تحديد خانه الاختيار هذه لاستخدام تحميل الارضيه. في سيناريو التحميل الأرضي يتم تكديس الصناديق من الأرض إلى السقف، من الجدار إلى الجدار المقابل داخل الحاوية لزيادة السعة.

1. في جزء الإجراءات، حدد **حفظ**.

## <a name="associate-a-load-template-with-a-new-load"></a>إقران قالب حمل بحمولة جديدة

1. انتقل إلى **إدارة النقل \> التخطيط \> منضدة عمل تخطيط الحِمل‬**.
1. في الجزء العلوي من الصفحة ، حدد أحدي علامات التبويب التالية ، استنادا إلى نوع المستند المصدر الذي تقوم بإنشاء تحميل له: **الشحنات** أو **خطوط المبيعات** أو **بنود التحويل** أو **بنود أمر الشراء**. 
1. حدد المستند المحدد لتخطيط التحميل له.
1. في جزء الإجراءات، في علامة التبويب **العرض والطلب**، في مجموعة **إضافة**، حدد **إلى حمل جديد**.
1. في مربع الحوار **قالب الحمل**، في الحقل **معرف قالب الحمل** حدد القالب المطلوب تطبيقه.
1. حدد **موافق** لتطبيق القالب.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]