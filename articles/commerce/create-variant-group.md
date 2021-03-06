---
title: إنشاء مجموعة متغير
description: يوضح هذا الموضوع كيفية إنشاء مجموعة متغير لون أو نمط أو مقاس لمنتج في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: e19d9a2549fa9957126592f3db7e468147997261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965140"
---
# <a name="create-a-variant-group"></a>إنشاء مجموعة متغير


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

![إنشاء مجموعة مقاس](media/create-variant-group.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على معلومات المنتجات](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[إعداد منتجات البيع بالتجزئة](set-up-retail-products.md)

[أبعاد المنتجات](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]