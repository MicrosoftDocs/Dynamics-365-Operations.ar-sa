---
title: إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫
description: يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421364"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>إنشاء nomenclature لرقم منتج متغيرات المنتج المعرفة مسبقًا‬‏‫

[!include [banner](../../includes/banner.md)]

يوضح هذا الموضوع كيفية إعداد nomenclature لرقم المنتج لمتغيرات منتجات معرّفة مسبقًا، وكيف يمكنك تعيينها إلى مجموعة أبعاد المنتجات المناسبة. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF. يتم تعيين nomenclature رقم المنتج إلى مجموعة أبعاد المنتجات "اللون والحجم". وعادة ما تُنفذ هذه المهمة عن طريق مصمم المنتج.


## <a name="create-a-product-number-nomenclature"></a>إنشاء nomenclature لرقم المنتج
1. حدد **تعريف نموذج متغير المنتج**.
2. حدد **كود nomenclature للمنتج‬**.
3. حدد **جديد**.
4. في الحقل **الاسم**، أدخل اسم nomenclature يساعد على تحديد مجموعة أبعاد المنتجات الهدف، على سبيل المثال، `ColorSize`.
5. في حقل **الوصف**، اكتب قيمة.
6. حدد **إضافة**.
7. حدد رقم **أصل المنتج**.
8. حدد **إضافة**.
9. حدد **الثابت النصي**.
10. في الحقل **النص**، اكتب قيمة.
11. حدد **إضافة**.
12. حدد **اللون**.
13. حدد **إضافة**.
14. حدد **الثابت النصي**.
15. في الحقل **النص**، اكتب قيمة.
16. حدد **إضافة**.
17. حدد **الحجم**.
18. قم بإغلاق الصفحة.

## <a name="assign-the-nomenclature-to-a-product-master"></a>تعيين nomenclature إلى أصل المنتج
1. حدد **مجموعات أبعاد المنتجات**.
2. حدد **مجموعة أبعاد المنتجات SizeCol**.
3. حدد **تحرير**.
4. حدد **نعم** في الحقل **استخدام كود nomenclature**.
5. أدخل قيمة أو حددها في حقل **كود nomenclature لرقم متغير المنتج‬**.
6. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]