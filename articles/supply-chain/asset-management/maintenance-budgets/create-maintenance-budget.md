---
title: إنشاء موازنات الصيانة
description: يشرح هذا المقال كيفية إنشاء موازنة الصيانة في إدارة الأصول.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1fa5e4c76621634930206c1d89fd8e8f4f541fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858029"
---
# <a name="create-maintenance-budgets"></a>إنشاء موازنات الصيانة

[!include [banner](../../includes/banner.md)]

 



تستخدم موازنات الصيانة لتقديم نظرة عامة حول التكاليف المتوقعة للصيانة الوقائية. يتم حساب بنود الموازنة استنادًا إلى بنود جدول الصيانة التي لديها تاريخ بدء متوقع أثناء فترة الموازنة.

تعتمد موازنات الصيانة على أنواع التكلفة المستخدمة في إدارة الأصول: **وقائية** و **تصحيحية** و **استثمارية**. يتم تضمين تكاليف الموازنة لصيانة الاستثمار للأصول النشطة التي لها تاريخ استبدال أثناء فترة الموازنة وقيمة بديلة مرتبطة. ويتم تضمين تكاليف الموازنة للصيانة التصحيحية إذا تم تضمين تاريخ تصحيحي سابق في حساب الموازنة. وفي هذه الحالة، يتم حساب التكاليف التصحيحية من فترة سابقة لنفس الفترة المستقبلية التي تقوم بحساب موازنة الصيانة لها.

## <a name="create-a-maintenance-budget"></a>إنشاء موازنة الصيانة

1. حدد **إدارة الأصول** \> **استعلامات** \> **موازنة‏‎ الصيانة** \> **الموازنة‏‎**.
2. حدد **إنشاء موازنة**.
3. في الحقل **موازنة الصيانة**، أدخل معرف موازنة.
4. في الحقل **الوصف**، أدخل وصفًا.
4. على علامة التبويب السريعة **الفترة**، في الحقلين **من تاريخ** و **إلى تاريخ**، أدخل تاريخي البدء والانتهاء لفترة الموازنة.
5. لتضمين تكاليف الموازنة التصحيحية التي يتم حسابها استنادًا إلى التكاليف الفعلية من فترة سابقة، في حقل **تصحيحية من تاريخ**، أدخل تاريخ البدء للفترة التي يجب أن يتم تضمين هذه التكاليف منها.
6. وفقًا لمستوى التفاصيل المطلوب في الموازنة، قم بتعيين الخيارات ذات الصلة على علامات التبويب السريعة الخمس **تجميع حسب**.
7. حدد **موافق**.
8. حدد **بنود الموازنة** لفتح صفحة **بنود موازنة الصيانة**، حيث يمكنك عرض كافة بنود الموازنة التي تم إنشاؤها للفترة.
9. لاعتماد الموازنة، حددها في صفحة **موازنات‏‎ الصيانة**، ثم حدد **اعتماد**. ثم، في مربع الحوار‏‎ **اعتماد الموازنة**، حدد **موافق**. يتم إدخال اسمك في الحقل **معتمد بواسطة** في صفحة **موازنات الصيانة**.

    > [!NOTE]
    > بعد اعتماد موازنة الصيانة، لا يمكنك إعادة حساب البنود ذات الصلة أو تعديلها في صفحة **بنود موازنة الصيانة** ما لم تقم أولاً بإزالة اعتماد الموازنة. لإزالة اعتماد موازنة الصيانة، حددها في صفحة **موازنات‏‎ الصيانة**، ثم حدد **اعتماد**. ثم، في مربع الحوار‏‎ **اعتماد الموازنة**، حدد **موافق**.

![موازنات الصيانة.](media/01-maintenance-budgets.png)

يمكنك أيضا إنشاء موازنة صيانة جديدة من خلال نسخ موازنة موجودة. صفحة **موازنات‏‎ الصيانة**، حدد الموازنة التي تريد نسخها، ثم حدد **نسخ**. وتعد هذه الطريقة مفيدة، إذا قمت، على سبيل المثال، بإنشاء موازنة لشهر واحد وأردت نسخها إلى أشهر أخرى.

> [!NOTE]
> تحسب موازنة الصيانة فقط تكاليف الموازنة استنادًا إلى بنود جدول الصيانة. لحساب التكاليف الفعلية لنفس الفترة، يمكنك إجراء هذا الحساب في صفحة **مراقبة تكلفة الأصول**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]