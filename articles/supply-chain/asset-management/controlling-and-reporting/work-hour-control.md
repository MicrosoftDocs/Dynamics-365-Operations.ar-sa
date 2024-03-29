---
title: مراقبة ساعات العمل
description: يشرح هذا المقال مراقبة ساعات العمل في إدارة الأصول.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f5f5dbb23c4d6c86bee7612c4ade65ef4b1cee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869738"
---
# <a name="work-hour-control"></a>مراقبة ساعات العمل

[!include [banner](../../includes/banner.md)]

 

في إدارة الأصول، يمكنك حساب الساعات للحصول عل نظرة عامة على الساعات الفعلية مقارنةً بساعات الموازنة على الأصول أو مواقع العمل أو أوامر العمل. تستند الساعات الفعلية إلى الحركات المرحّلة.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>مراقبة ساعات العمل للأصول ومواقع العمل وأوامر العمل

تعتبر العمليات الحسابية التي يتم تنفيذها للأصول ومواقع العمل وأوامر العمل مماثلة تقريبًا. الفرق الوحيد هو أنه يمكنك أيضًا تضمين أصول فرعية ومواقع فرعية في حسابك فيما يتعلق بالأصول ومواقع العمل. التاريخ هو تاريخ الحركة عندما تم إنشاء التسجيل.

1. انقر فوق **إدارة الأصول** > **استعلامات** > **الأصول‏‎** > **مراقبة ساعات الأصول** أو **مراقبة ساعات مواقع العمل** أو **إدارة الأصول** > **استعلامات‏‎** > **أوامر العمل** > **مراقبة ساعات أوامر العمل**.

2. في مربع الحوار **مراقبة ساعات الأصول**.

3. في مربع الحوار **مراقبة ساعات الأصول** / **مراقبة ساعات مواقع العمل** / **مراقبة ساعات أوامر العمل**، حدد فترة ليتم حسابها في الحقلين **من تاريخ** و **إلى تاريخ**.

4. إذا لزم الأمر، حدد **مجموعة أبعاد مالية** لتضمينها في الحساب.

5. حدد "نعم" على زر التبديل **تخطي الصفر** إذا لم ترغب في إظهار النتائج التي تحتوي على صفر.

6. يمكنك استخدام حقل **المستوى** للإشارة إلى مستوى التفصيل الذي ترغب فيه في بنود مراقبة الساعات فيما يتعلق بمواقع العمل. 

    على سبيل المثال، إذا قمت بإدراج الرقم "1" في الحقل، وكان لديك تدرجًا هرميًا لموقع عمل متعدد المستويات، فستظهر جميع بنود مراقبة الساعات لموقع عمل في المستوى العلوي، وبالتالي فإن الساعات على البند قد تُضاف من مواقع عمل موجودة في مستوى أدنى. 
    
    إذا قمت بإدراج الرقم "0" في حقل **المستوى**، فسترى نتيجة مفصلة تعرض جميع بنود مراقبة الساعات على جميع مستويات مواقع العمل التي ترتبط بها.

7. حدد "نعم" على زر التبديل **تضمين الأصول الفرعية** لإظهار التكاليف المرتبطة بالأصول الفرعية كبنود منفصلة.

8. إذا كنت ترغب في تقييد البحث، فيمكنك تحديد أصول / مواقع عمل / أوامر عمل معينة على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**.

9. انقر فوق **موافق** لبدء الحساب.

10. في صفحة **مراقبة ساعات الأصول** ، انقر فوق الأزرار **تجميع حسب** لإظهار مستوى التفاصيل المطلوب للحساب. يتم تمييز أزرار **تجميع حسب** المحددة. انقر فوق زر لتنشيطه أو إلغاء تنشيطه.

## <a name="example"></a>مثال

تعرض لقطة الشاشة أدناه مثالاً لحساب **مراقبة ساعات الأصول**.

- يعرض حقل **الموازنة‏‎ الأصلية** تكاليف الساعات من تنبؤ أمر العمل. 
- يعرض حقل **التكلفة الفعلية** الساعات التي تم ترحيلها على أوامر العمل. 
- يعرض حقل **الساعات الإلزامية** إجمالي عدد الساعات التي تلتزم بها شركتك فيما يتعلق بأوامر العمل.

![مثال على حساب مراقبة ساعات الأصول.](media/04-controlling-and-reporting.png)

ثمة طريقة أخرى لحساب الساعات وهي إجراء تحديدات متعددة للأصول في **كل الأصول** أو **الأصول‏‎ النشطة**. ثم انقر فوق زر **مراقبة الساعات** على علامة التبويب السريعة **عام**. يتم إدراج الأصول المحددة بشكل تلقائي في حقل **الأصل** على علامة التبويب السريعة **السجلات المطلوب تضمينها‬**. انقر فوق **موافق** في مربع الحوار **مراقبة ساعات الأصول**، ويظهر حساب الأصول المحددة. يمكن تنفيذ الإجراء نفسه لمواقع العمل في **جميع مواقع العمل** أو **مواقع العمل النشطة** ولأوامر العمل في **جميع أوامر العمل** أو **أوامر العمل النشطة**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]