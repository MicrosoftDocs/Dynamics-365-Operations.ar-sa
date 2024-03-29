---
title: تحديث موازنات الصيانة
description: يشرح هذا المقال كيفية تحديث موازنة الصيانة في إدارة الأصول.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a9333c9ad48c87159ed4071a8b4843fc0e55ceb5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860946"
---
# <a name="update-maintenance-budgets"></a>تحديث موازنات الصيانة

[!include [banner](../../includes/banner.md)]

 

تعرض صفحة **بنود موازنة الصيانة** جميع بنود الموازنة التي تم إنشاؤها للموازنة المحددة في صفحة **موازنات الصيانة**. (لمزيد من المعلومات، راجع [إنشاء موازنات الصيانة](create-maintenance-budget.md).) يمكنك إعادة حساب بنود موازنة الصيانة وتعديلها حتى يتم اعتماد موازنة الصيانة. بعد مرور فترة الموازنة وترحيل التكاليف في إدارة الأصول، يمكنك أيضًا تحديث بنود الموازنة بواسطة التكاليف الفعلية.

## <a name="recalculate-a-maintenance-budget"></a>إعادة حساب موازنة صيانة

يمكنك إعادة حساب موازنة صيانة في الصفحة **بنود موازنة الصيانة**. عندما تعيد حساب موازنة الصيانة، تُحذف بنود الموازنة الموجودة، ويتم إجراء عملية حسابية جديدة.

1. في الصفحة **بنود موازنة الصيانة**، حدد **إعادة الحساب**.
2. في مربع الحوار **إعادة حساب الموازنة**، أدخل التغييرات المطلوبة للحساب الجديد، ثم حدد **موافق**.

يتم إنشاء بنود الموازنة الجديدة وفقًا للقيم التي تقوم بتعيينها.

## <a name="adjust-budget-lines"></a>تعديل بنود الموازنة

بدلاً من إعادة حساب موازنة الصيانة بأكملها، يمكنك تعديل بنود محددة ترتبط بتكاليف الموازنة.

1. في الصفحة **بنود موازنة الصيانة**، حدد البنود التي تريد تحديث تكلفة الموازنة لها.
2. حدد **تعديل‬**.
3. لإضافة مبلغ إلى البنود المحددة، حدد خانه الاختيار **إضافة تكلفة**، ثم أدخل القيمة في الحقل **إضافة قيمة**.
4. لضرب تكلفة الموازنة على بنود الموازنة المحددة بواسطة عامل، حدد خانة الاختيار **ضرب التكلفة**، وأدخل العامل في حقل **ضرب القيمة**.

    على سبيل المثال، إذا قمت بإدخال **1.2** في حقل **ضرب القيمة**، فأنت تزيد تكلفة الموازنة على البنود المحددة بقيمة 20 بالمائة. وإذا أدخلت **0.7**، فأنت تقوم بتقليل تكلفة الموازنة على البنود المحددة بنسبة 30 بالمئة.

5. حدد **موافق**.

يتم تحديث بنود الموازنة المحددة وفقًا للقيم التي تقوم بتعيينها في الخطوة 3 أو 4.

## <a name="update-actual-costs"></a>تحديث التكاليف الفعلية

بعد مرور التواريخ المذكورة على بنود الموازنة وترحيل التكاليف الفعلية في إدارة الأصول، يمكنك تحديث التكاليف الفعلية على موازنة الصيانة.

1. في الصفحة **بنود موازنة الصيانة**، حدد **تحديث التكلفة**.
2. في مربع الحوار **حساب‏‎ التكلفة الفعلية**، حدد **موافق**.

يتم تحديث حقول **التكلفة الفعلية** على بنود الموازنة إذا تم ترحيل التكاليف الفعلية. قد يتم إنشاء بنود موازنة جديدة إذا تم إنشاء أنواع أصول جديدة منذ قيامك بإنشاء الموازنة، وإذا تم استخدام أنواع الأصول هذه على الأصول التي تم إنشاء أوامر عمل لها وتم ترحيل تكاليف ذات صلة لها. تعرض بنود الموازنة الجديدة التكاليف الفعلية فقط، بسبب عدم حساب تكاليف موازنة لها.

> [!NOTE]
> للاطلاع على نظرة عام حول التكاليف الفعلية المقسمة إلى تكاليف وقائية وتصحيحية واستثمارية، يمكنك إجراء حساب للفترة نفسها في صفحة **مراقبة تكلفة الأصول**. 

## <a name="manually-add-budget-lines"></a>إضافة بنود الموازنة يدويًا

في الصفحة **بنود موازنة الصيانة**، يمكنك إضافة بند موازنة جديد يدويًا من خلال تحديد **جديد** ثم إجراء التحديدات على البند. فيما يلي بعض الأمثلة عن حالات يكون فيها هذا الأسلوب مفيدًا:

- أنت تعلم أن تجديد بعض الأصول هو في مرحلة التخطيط في الوقت الحالي، ولكن لم يتم بعد إنشاء المهام ذات الصلة في إدارة الأصول. ومع ذلك، فأنت ترغب في تضمين تكاليف الموازنة لهذه المهام في موازنة الصيانة.
- تم إنشاء أصول أو أنواع أصول جديدة منذ قيامك بوضع موازنة الصيانة، ولكن لم يتم بعد إعداد خطط الصيانة على هذه الأصول أو أنواع الأصول. ومع ذلك، فأنت ترغب في تضمين تكاليف أنواع الأصول هذه في موازنة الصيانة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]