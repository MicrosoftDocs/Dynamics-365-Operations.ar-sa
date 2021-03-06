---
title: الشركات المصنعة للأصول ونماذج الأصول
description: يشرح هذا الموضوع كيفية إعداد الشركات المصنعة للأصول والنماذج ذات الصلة في "إدارة الأصول".
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1eca3112b95bc7d1a049f101fc1d461272a63aa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022246"
---
# <a name="asset-manufacturers-and-models"></a>الشركات المصنعة للأصول ونماذج الأصول

[!include [banner](../../includes/banner.md)]

 

يشرح هذا الموضوع كيفية إعداد الشركات المصنعة للأصول والنماذج ذات الصلة في "إدارة الأصول". قد ترتبط النماذج بأنواع الأصول.

## <a name="set-up-product-model-relations"></a>إعداد علاقات المنتجات والنماذج

1. حدد **إدارة الأصول** \> **الإعداد** \> **الأصول‏‎** \> **الشركة المصنعة والنموذج‬**.
2. حدد **جديد** لإنشاء منتج جديد.
3. في الحقل **الشركة المصنعة**، أدخل اسمًا للشركة المصنعة للأصل.
4. في الحقل **الوصف**، أدخل وصفًا.
5. على علامة التبويب السريعة **النماذج،** حدد **إضافة** لإنشاء نموذج أصل يجب أن يكون مرتبطًا بالشركة المصنعة للأصل.
6. في الحقل **النموذج**، أدخل اسمًا لنموذج الأصل.
7. في الحقل **الوصف**، أدخل وصفًا.
8. في الحقل **نوع الأصل**، حدد نوع الأصل الذي يجب أن يرتبط به نموذج الشركة المصنعة.

    > [!NOTE]
    > يمكنك أيضًا إعداد علاقات لأنواع الأصول والشركات المصنعة والنماذج في بحث **أنواع الأصول**. لمزيد من المعلومات، راجع [أنواع الأصول](../setup-for-objects/object-types.md).

    على علامة التبويب السريعة **التفاصيل** يعرض حقل **النماذج** عدد نماذج الأصول التي تم إعدادها على الشركة المصنعة للأصول المحددة. يعرض حقل **الأصول** عدد الأصول التي تستخدم الشركة المصنعة المحددة.
    
    يعرض حقل **الأصول** عدد الكائنات التي تستخدم نموذج الشركة المصنعة.

> [!NOTE]
> قد لا يكون لنوع الأصل أي علاقات بين نماذج الشركة المصنعة للأصول، أو يمكنه أن يكون مرتبطًا بنموذج واحد للشركة المصنعة للأصول، أو يمكنه أن يكون مرتبطًا بنماذج متعددة للشركة المصنعة للأصول. إذا كان نوع الأصل مرتبطًا بنموذج شركة مصنعة واحد على الأقل، فيمكن تحديد فقط المجموعات التي تم إعدادها في بحث **نموذج الشركة المصنعة** على صفحات "إدارة الأصول" حيث يمكن إعداد مجموعة من نوع الأصل والشركة المصنعة والنموذج. تتضمن هذه الصفحات **كل الأصول** و **مستويات خدمة الأصول‬** و **الإعدادات الافتراضية لنوع الوظيف** و **بنود موازنة الصيانة**. إذا كانت بعض أنواع الأصول غير مرتبطة بأي نموذج من نماذج الشركة المصنعة، فلن تظهر على الصفحات سوى أنواع الأصول هذه والشركات المصنعة التي لا علاقة لها أيضًا بأنواع الأصول.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>تحديد شركة مصنعة ونموذج على كائن

1. حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **كل الأصول‏‎**.
2. في عمود ‏‎**الأصل**، حدد الارتباط الخاص بالأصل. تظهر الصفحة **التفاصيل‬**.
3. حدد **تحرير**.
4. على علامة التبويب السريعة **عام**، حدد القيم في الحقلين **الشركة‏‎ المصنعة** و **النموذج**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]