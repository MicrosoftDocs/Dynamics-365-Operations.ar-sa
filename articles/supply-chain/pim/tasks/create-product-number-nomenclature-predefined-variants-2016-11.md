---
title: إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا المقال كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887301"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم". وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.


## <a name="create-a-product-number-nomenclature"></a>إنشاء nomenclature لرقم المنتج

1. انتقل إلى **إدارة معلومات المنتج \> إعداد \> ‏‫كود nomenclature للمنتج‬**.
1. حدد **جديد**.
1. في الحقل **الاسم**، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، `ColorSize`.
1. في حقل **الوصف**، اكتب قيمة.
1. حدد **إضافة**.
1. حدد رقم **أصل المنتج**.
1. حدد **إضافة**.
1. حدد **الثابت النصي**.
1. في الحقل **النص**، اكتب قيمة.
1. حدد **إضافة**.
1. حدد **اللون**.
1. حدد **إضافة**.
1. حدد **الثابت النصي**.
1. في الحقل **النص**، اكتب قيمة.
1. حدد **إضافة**.
1. حدد **الحجم**.
1. قم بإغلاق الصفحة.

## <a name="assign-the-nomenclature-to-a-product-master"></a>تعيين nomenclature إلى أصل المنتج

1. حدد **مجموعات أبعاد المنتجات**.
2. حدد **مجموعة أبعاد المنتجات SizeCol**.
3. حدد **تحرير**.
4. حدد **نعم** في الحقل **استخدام كود nomenclature**.
5. أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬**.
6. قم بإغلاق الصفحة.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]