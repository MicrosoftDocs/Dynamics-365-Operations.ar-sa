---
title: وقت تعطل الصيانة لأوامر العمل
description: يصف هذا الموضوع كيفية إنشاء تسجيلات وقت تعطل الصيانة على الأصل المحدد في أمر العمل.
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
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020901"
---
# <a name="maintenance-downtime-for-work-orders"></a>وقت تعطل الصيانة لأوامر العمل

[!include [banner](../../includes/banner.md)]


يمكن إنشاء تسجيلات وقت تعطل الصيانة على الأصل المحدد في أمر العمل. وتكون هذه الإمكانية مفيدة إذا كنت ترغب في تسجيل وقت تعطل الصيانة على جهاز واحد أو أكثر في منطقه الإنتاج. تقوم أولاً بإنشاء أكواد أسباب وقت تعطل الصيانة التي ترغب في استخدامها، على سبيل المثال، **التفصيل** و **التوقف المخطط**. يتم إجراء هذه الخطوة في صفحة **أكواد أسباب وقت تعطل الصيانة**. بعد ذلك، يمكنك إنشاء تسجيلات وقت تعطل الصيانة في صفحة **وقت تعطل الصيانة** وإضافة أكواد أسباب وقت تعطل الصيانة ذات الصلة.

## <a name="create-maintenance-downtime-reason-codes"></a>إنشاء أكواد أسباب وقت تعطل الصيانة

1. حدد **إدارة الأصول** > **إعداد** > **أوامر العمل** > **أكواد أسباب وقت تعطل الصيانة**.

2. حدد **جديد**.

3. في الحقل **كود سبب وقت تعطل الصيانة** ، ادخل معرفًا لكود سبب وقت تعطل الصيانة.

4. في حقل **الاسم**، أدخل اسمًا.

5. حدد خانه الاختيار **تضمين KPI** إذا كان يجب تضمين كود السبب في حسابات مؤشرات الأداء الرئيسية (KPIs) للأصل. وبشكل عام، لا يجب تضمين توقفات الإنتاج المخططة في حسابات مؤشرات الأداء الأساسية، لأنها لا تؤثر على الأداء المتوقع.

6. حدد **حفظ**.

يبين الرسم التوضيحي أدناه مثالًا لصفحة **أكواد أسباب وقت تعطل الصيانة**.

![الشكل 1](media/15-work-orders.png)

بعد إنشاء أكواد أسباب وقت تعطل الصيانة التي ترغب في استخدامها، يمكن إنشاء تسجيلات وقت تعطل الصيانة الخاصة بأوامر العمل والأصول.


## <a name="create-maintenance-downtime-registrations"></a>إنشاء تسجيلات وقت تعطل الصيانة

1. انقر فوق **إدارة الأصول** > **عام** > **أوامر العمل** > **جميع أوامر العمل** أو **أوامر العمل النشطة**.

2. حدد أمر العمل، ثم من علامة التبويب **أمر العمل** ، في مجموعة **الأصول** ، حدد **وقت تعطل الصيانة**.

3. حدد **جديد**.

4. حدد التاريخ والفترة الزمنية لتسجيل وقت تعطل الصيانة في الحقلين **من** و **إلى** .

>[!NOTE]
>عندما تغادر الحقل **إلى**، يتم إدراج المدة بالساعات بشكل تلقائي في حقل **المدة**.

5. حدد كود السبب في حقل **كود سبب وقت تعطل الصيانة** .

6. كرر الخطوات من 3 إلى 5 لإضافة مزيد من التسجيلات.

7. حدد **حفظ**.

يبين الرسم التوضيحي أدناه مثالاً على تسجيل وقت تعطل الصيانة.

![الشكل 2](media/16-work-orders.png)

يتوقف التقويم المستخدم في حساب تسجيل وقت تعطل الصيانة على تحديدك في إعداد الأصول والمعلمات. إذا تم تحديد مورد على أحد الأصول في حقل **مورد** على علامة التبويب السريعة **الأصل الثابت** لصفحة **كافة الأصول** ، فسيتم استخدام إعداد التقويم لمجموعة الموارد المقترنة، كما هو مبين في الشكل التوضيحي التالي.

![الشكل 3](media/17-work-orders.png)

إذا لم يتم تحديد أي مورد على الأصل، فسيتم استخدام التقويم القياسي المحدد في صفحة **معلمات إدارة الأصول** ، كما هو مبين في الشكل التوضيحي التالي.

![الشكل 4](media/18-work-orders.png)

انقر فوق **إدارة الأصول** > **استعلامات** > **وقت تعطل الصيانة** للاطلاع على نظرة عامة على تسجيلات وقت تعطل الصيانة.

>[!NOTE]
>تم إعداد كافة التقويمات المستخدمة في الوحدة النمطية **إدارة الأصول** في **إدارة المؤسسة** > **إعداد** > **التقويمات** > **التقويمات**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]