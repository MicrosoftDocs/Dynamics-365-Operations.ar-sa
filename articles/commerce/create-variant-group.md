---
title: إنشاء مجموعة متغير
description: يوضح هذا الموضوع كيفية إنشاء مجموعة متغير لون أو نمط أو مقاس لمنتج في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b47f38375fc8925288db36f066ed7820bab3fe9b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353146"
---
# <a name="create-a-variant-group"></a>إنشاء مجموعة متغيرات


[!include [banner](includes/banner.md)]

يوضح هذا الموضوع كيفية إنشاء مجموعة متغير لون أو نمط أو مقاس لمنتج في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

يدعم Dynamics 365 Commerce متغيرات متعددة للمنتجات. ويعد من المثالي إعداد مجموعات المتغير لفئات منتجات مختلفة. على سبيل المثال، يمكن إنشاء مجموعة حجم لقمصان بالمقاسات صغير جدًا وصغير ومتوسط وكبير وكبيرة جدًا، أو مجموعة لون يمكن إنشاؤها لتضمين كافة الألوان المتوفرة لأحد المنتجات. يجب إضافة مجموعات المتغير قبل إضافة المنتجات.

في هذا الموضوع، سيتم إنشاء مجموعة مقاس وتكوينها. يمكن استخدام إجراءات مشابهة لإضافة مجموعات النمط ومجموعات اللون وتكوينها.

## <a name="create-a-size-group"></a>إنشاء مجموعة مقاس

لإنشاء مجموعة مقاس، اتبع الخطوات التالية.
 
1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> مجموعات المتغير \> مجموعات المقاس**.
1. في جزء الإجراءات، حدد **جديد**.
1. في المربع **مجموعة المقاس**، أدخل اسمًا لمجموعة المقاس.
1. في مربع **الوصف**، أدخل وصفًا مناسبًا.
1. في جزء الإجراءات، حدد **حفظ**.

## <a name="add-attributes-to-the-size-group"></a>إضافة سمات إلى مجموعة المقاس

لإضافة سمات إلى مجموعة المقاس، اتبع الخطوات التالية.

1. في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> المنتجات والفئات \> مجموعات المتغير \> مجموعات المقاس**
1. في جزء التنقل، حدد مجموعة المقاس.
1. ضمن **سطور مجموعة المقاس**، حدد **إضافة**.
1. في مربع **المقاس**، أدخل سلسلة لتمثيل المقاس (على سبيل المثال "XL").
1. في المربع **اسم المقاس**، أدخل اسمًا للمقاس (على سبيل المثال، "كبير جدًا").
1. في المربع **وزن التزويد**، أدخل رقمًا يمثل وزن التزويد.
1. في المربع **الرقم في الكود الشريطي**، أدخل رقمًا يمثل الكود الشريطي.
1. في المربع **ترتيب العرض**، أدخل رقمًا يمثل ترتيب العرض.
1. عند الانتهاء من إضافة المقاسات، حدد **حفظ** في جزء الإجراءات.

تعرض الصورة التالية مثالاً لمجموعة مقاس "لمقاسات قمصان غير رسمية".

![إنشاء مجموعة مقاس.](media/create-variant-group.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على معلومات المنتجات](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[إعداد منتجات البيع بالتجزئة](set-up-retail-products.md)

[أبعاد المنتجات](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]