---
title: مجموعات أمر العمل
description: يصف هذا الموضوع كيفية التعامل مع مجموعات أوامر العمل في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: afea5b8d0f958c3ab53d6cef8c9a0e9030d7c67b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017506"
---
# <a name="work-order-pools"></a>مجموعات أمر العمل

[!include [banner](../../includes/banner.md)]


يمكنك استخدام مجموعات أوامر العمل لتجميع أوامر العمل التي يجمع ما بينها شيء مشترك. فيما يلي بعض أمثلة الأشياء التي يمكنك إنشاء مجموعات أوامر عمل لها:

- لأطقم العمل، على سبيل المثال، طاقم الصيانة A أو طاقم الصيانة B  

- المهارات المهنية، مثل عمال الكهرباء أو السباكة  

- المواقع الفعلية  

- الجداول الزمنية، مثل أسابيع أو فترات أخرى  

حسب الحاجة، يمكنك وضع أمر عمل واحد في مجموعات أوامر العمل متعددة.


## <a name="create-a-work-order-pool"></a>إنشاء مجموعة أوامر عمل

في **جميع مجموعات أوامر العمل** أو صفحة قائمة **مجموعات أوامر العمل النشطة**، يمكنك الحصول على نظرة عامة على مجموعات أوامر العمل وإنشاء مجموعات جديدة.

1. حدد **إدارة الأصول** > **عام** > **مجموعات أوامر العمل** > **جميع مجموعات أوامر العمل** أو **مجموعات أوامر العمل النشطة**.

2. حدد **جديد**.

3. في الحقل **الوعاء**، أدخل معرفًا لمجموعة أمر العمل.

4. في حقل **الاسم**، أدخل اسمًا.

5. قم بتعيين الخيار **نشط** على **نعم** للإشارة إلى أن مجموعة أمر العمل نشطة.

6. قم بتعيين الخيار **حذف علاقات أوامر العمل** على **نعم** إذا أردت أن تتم إزالة أوامر العمل بشكل تلقائي من مجموعة أمر العمل.

7. في الحقل **حذف حالة دورة الحياة**، حدد حالة دورة حياة أمر العمل. على سبيل المثال، يمكن تعيين حالة دورة حياة أمر العمل لحذف العلاقات بمجموعات أوامر العمل بشكل تلقائي.

    يمكنك بدء إضافة أوامر العمل إلى مجموعة أوامر العمل على الفور.

8. على علامة التبويب السريعة **أوامر العمل**، حدد **إضافة بند**.

9. في الحقل **أمر العمل**، حدد أمر عمل. يتم عندئذٍ تحديث الحقول المرتبطة تلقائيًا.

10. كرر الخطوات من 8 إلى 9 لإضافة مزيد من أوامر العمل.

11. إذا كانت أوامر العمل التي قمت بإضافتها يجب تنفيذها ببترتيب معين، ففي حقل **‏‫ترتيب الفرز**، يمكنك إدخال الأرقام **1** و **2** و **3** وهكذا لتحديد ذلك الأمر.

12. لعرض قائمة بجميع أوامر العمل المضمنة في مجموعة أمر العمل، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل** في مجموعة **عرض مجموعة أمر العمل المرتبطة**، حدد **أوامر العمل** لفتح صفحة قائمة **جميع أوامر العمل**.

13. لحساب القدرة الإنتاجية وعرضها لجدول الصيانة وأوامر العمل غير المجدولة وأوامر العمل المجدولة، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل**، في مجموعة **عرض مجموعة أمر العمل المرتبطة**، حدد **القدرة الإنتاجية** لفتح مربع الحوار **حساب القدرة الإنتاجية**.

14. لحساب التنبؤات وعرضها للأصناف (قطع الغيار والأصناف المطلوبة الأخرى) المرتبطة بجدول الصيانة وأوامر العمل غير المجدولة وأوامر العمل المجدولة، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل**، في مجموعة **عرض مجموعة أمر العمل المرتبطة**، حدد **‏‫التنبؤ بالأصناف‬** لفتح مربع الحوار **‏‫حساب تنبؤ العنصر‬**.

15. لعرض قائمة بطلبات الشراء المرتبطة بأوامر العمل في مجموعة أمر العمل، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل** في مجموعة **التدبير‬**، حدد **‏‫طلب الشراء لأمر العمل‬** لفتح صفحة قائمة **‏‫طلب الشراء لأمر العمل‬**.

16. لعرض قائمة بأوامر الشراء المرتبطة بأوامر العمل في مجموعة أمر العمل، في جزء الإجراءات، في علامة التبويب **مجموعة أمر العمل** في مجموعة **التدبير‬**، حدد **‏‫‏‫شراء أمر العمل‬** لفتح صفحة قائمة **‏‫‏‫شراء أمر العمل‬**.

>[!NOTE]
>عندما لا تعود مجموعة أوامر العمل ذات صلة بتخطيط عملك، قم بتعيين الخيار **نشط** لتلك المجموعة إلى **لا** في طريقة عرض القائمة بصفحة **مجموعة أوامر العمل**.

لحذف جميع بنود أمر العامل، قم بتعيين الخيار **حذف علاقات أوامر العمل** إلى **نعم**. ويعد هذا الخيار مفيدًا إذا كنت ترغب على سبيل المثال في إنشاء مجموعة فارغة يمكنك استخدامها لاحقا لأوامر العمل الأخرى. تذكر تعيين الخيار **حذف علاقات أوامر العمل** على **لا** إذا كنت جاهزًا لاستخدام مجموعة أوامر العمل لإنشاء علاقات أوامر عمل جديدة في وقت لاحق.

يوضح الرسم التوضيحي المبين أدناه مثال لصفحة قائمة **مجموعة أمر العمل‬**.

![الشكل 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>إضافة أمر عمل إلى مجموعة أمر العمل

كما هو موضح في القسم السابق، يمكنك إضافة أوامر العمل إلى مجموعة أوامر العمل عندما تقوم بإنشاء تلك المجموعة. يمكنك أيضا إضافة أوامر العمل إلى مجموعة أمر عمل في صفحة قائمة **جميع أوامر العمل** أو  **أوامر العمل النشطة**.

1. حدد أمر العمل ثم في جزء الإجراءات، من علامة التبويب **أمر العمل**، في مجموعة **صيانة‬** ، حدد **مجموعة أمر العمل**.

2. حدد أمر العمل في القائمة، وانقر فوق **مجموعة أوامر العمل**.

3. في مربع الحوار **صيانة مجموعة أمر العمل** في الحقل **إضافة/إزالة**، حدد **إضافة**.

4. في الحقل **الوعاء**، حدد مجموعة‏‎ أمر العمل.

5. حدد **موافق**.

6. لوضع أمر العمل الذي قمت بإضافته بترتيب معين في مجموعة أمر العمل، في **جميع مجموعات أوامر العمل** أو صفحة قائمة **‏‫مجموعات أوامر العمل النشطة‬**، حدد المجموعة، ثم حدد **تحرير**. ثم في الصفحة **مجموعة أمر العمل** على علامة التبويب السريعة **أوامر العمل** استخدم الحقل **ترتيب الفرز** لتعديل ترتيب الفرز الخاص بأوامر العمل المضمنة في المجموعة.

لإزالة أمر عمل من مجموعة أمر العمل، كرر تلك الخطوات، ولكن حدد **إزالة** في الخطوة 3.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]