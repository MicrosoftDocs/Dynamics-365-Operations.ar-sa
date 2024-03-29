---
title: حالات دورة حياة موقع العمل
description: يصف هذا المقال كيفية إعداد حالات موقع العمل ونماذج دورة الحياة في إدارة الأصول.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae56c2b734339343b134be95abe0ce40b70c8a0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934652"
---
# <a name="functional-location-lifecycle-states"></a>حالات دورة حياة موقع العمل

[!include [banner](../../includes/banner.md)]

 

يصف هذا المقال كيفية إعداد حالات دور حياة موقع العمل ونماذج دورة الحياة في إدارة الأصول. تحدد حالات دورة حياة موقع العمل الحالات التي يمكن أن يمر بها موقع العمل، على سبيل المثال، تم إنشاؤه ونشط ومنتهٍ. يمكنك عرض كافة مواقع العمل، بغض النظر عن حالة دورة حياتها في صفحة قائمة **جميع مواقع العمل‬**. يمكنك تغيير حالة موقع عمل عن طريق تحديده في صفحة قائمة **جميع مواقع العمل** وتحديد **تحديث حالة موقع العمل**.

## <a name="set-up-functional-location-lifecycle-states"></a>إعداد حالات دورة حياة مواقع العمل

1. حدد **إدارة الأصول** > **الإعداد** > **مواقع العمل** > **حالات دورة الحياة.**.
2. حدد **جديد** لإنشاء حالة موقع عمل جديدة.
3. أدخل معرف الحالة في حقل **حالة دورة الحياة**، وأدخل اسمًا لحالة موقع العمل في حقل **الاسم**. في الحقل **نماذج دورة الحياة**، يمكنك رؤية عدد نماذج دورة حياة مواقع العمل التي تستخدم حالة موقع العمل.
4. على علامة التبويب السريعة **عام**، حدد "نعم" على زر التبديل **نشط**، إذا كان يجب أن يكون موقع العمل نشطًا في هذه الحالة.
5. حدد "نعم" على زر التبديل **إنشاء أصول** إذا كان من الممكن إنشاء أصل بنفس اسم موقع العمل بشكل تلقائي وتثبيته على موقع العمل في هذه الحالة.  
>[!NOTE]
>يرتبط زر التبديل هذا بالحقل **نوع الأصل** على علامة التبويب السريعة **عام** في النموذج **أنواع مواقع العمل** (**إدارة الأصول** > **الإعداد** > **مواقع العمل** > **أنواع مواقع العمل**).

6. حدد "نعم" على زر التبديل **إعادة تسمية** إذا كان يجب أن يكون من الممكن تغيير اسم موقع العمل في هذه الحالة.
7. حدد "نعم" على زر التبديل **مواقع فرعية جديدة** إذا كان يجب أن يكون من الممكن إضافة مواقع فرعية جديدة إلى موقع العمل في هذه الحالة.
8. حدد "نعم" على زر التبديل **تثبيت الأصول** إذا كان يجب أن يكون من الممكن تثبيت أصول على موقع العمل في هذه الحالة.
9. حدد "نعم" على زر التبديل **حذف موقع العمل** إذا كان يجب أن يكون من الممكن حذف موقع العمل في هذه الحالة.
10. حدد حالة أصل في حقل **حالة دورة الحياة** إذا كنت تريد تحديث حالة دورة حياة الأصل لجميع الأصول المثبتة في موقع العمل بشكل تلقائي في هذه الحالة. على سبيل المثال: إذا قمت بإغلاق موقع عمل، ثم قمت بتعيين حالة دورة حياة موقع العمل إلى "منتهٍ"، فقد تحتاج إلى تغيير حالة دورة حياة الأصول المثبتة في نوقع العمل هذا بشكل تلقائي إلى "غير مستخدم".


>[!NOTE]
>ترتبط حالات دورة حياة موقع العمل وأنواع ونماذج دورة الحياة ببعضها، ويتم استخدامها بالطريقة نفسها كحالات دورة حياة أمر عمل ونماذج حياة أمر العمل وأنواع أمر العمل. 

## <a name="set-up-functional-location-lifecycle-models"></a>إعداد نماذج دورة حياة مواقع العمل

عند إنشاء حالات دورة الحياة المطلوبة لمواقع العمل، يمكن تقسيمها إلى مجموعات. ويتم ذلك لإنشاء سير مهام نموذج دورة الحياة الذي يمكن استخداما لأنواع مختلفة من مواقع العمل. كحد أدنى، يجب إنشاء نموذج دورة حياة موقع عمل قياسي واحد.

1. حدد **إدارة الأصول** > **الإعداد** > **مواقع العمل** > **نماذج دورة الحياة.**.
2. حدد **جديد** لإنشاء نموذج دورة حياة جديد.
3. أدخل معرف نموذج دورة الحياة في حقل **نموذج دورة الحياة**، وأدخل اسمًا لنموذج دورة الحياة في حقل **الاسم**. في الحقلين **أنواع مواقع العمل** و **حالات دورة الحياة**، يمكنك رؤية عدد أنواع مواقع العمل التي تستخدم نموذج دورة الحياة وعدد الحالات المحددة في نموذج دورة الحياة.
4. على علامة التبويب السريعة **حالات دورة الحياة**، حدد الحالات التي يجب تضمينها في النموذج. ويتم ذلك بالنقر فوق حالة في القسم **دورة الحياة المتبقية** والنقر فوق زر ![السهم للأمام.](media/02-setup-for-functional-locations.png) .
5. إذا كنت ترغب في تحديد كافة الحالات المتوفرة لنموذج، فانقر فوق الزر ![تحديد جميع المراحل المتوفرة.](media/03-setup-for-functional-locations.png) . يتم نقل جميع الحالات إلى القسم **حالات دورة الحياة المحددة**.
6. إذا كنت ترغب في إزالة حالة محددة من النموذج، فحدد الحالة في القسم **حالات دورة الحياة المحددة** ثم حدد الزر ![سهم للخلف.](media/04-setup-for-functional-locations.png). .
7. حدد **تحديثات حالة دورة الحياة** لتحديد حالات دورة الحياة التي يمكنها أن تتبع حالة محددة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
