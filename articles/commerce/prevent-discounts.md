---
title: خيارات منع الخصومات لمنتجات البيع بالتجزئة
description: هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7c408068ece94d47c0f41e286a2ce0ae7efd23dd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972477"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>خيارات منع الخصومات لمنتجات البيع بالتجزئة

[!include [banner](includes/banner.md)]

هناك أسباب مختلفة تكمن خلف رغبة تجار التجزئة في منع تطبيق الخصومات على بعض المنتجات، سواء من عرض ترويجي أو أثناء عملية البيع في نقطة البيع.

سوف تسمح الخيارات التالية الموجودة على علامة تبويب **Commerce** للمنتجات الصادرة بتكوين المنتج لمنع جميع الخصومات أو الخصومات اليدوية. يمكن أيضًا تحديد الإعدادات على مستوى الفئة من التدرج الهرمي للفئات.

- **منع كافة الخصومات** – حدد هذا الخيار لمنع تطبيق كافة أنواع الخصومات على هذا المنتج. وهذا يشمل العروض الترويجية مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد، بالإضافة إلى خصومات البنود والحركات اليدوية التي يتم تطبيقها أثناء عملية البيع من قبل مستخدم نقطة البيع.
- **منع الخصومات اليدوية** – حدد هذا الخيار لمنع فقط خصومات البنود أو الحركات اليدوية التي يتم تطبيقها أثناء عملية بيع من قبل مستخدم نقطة البيع. تبقى المنتجات التي تم تحديد هذا الخيار لها مؤهلة للعروض الترويجية، مثل خصومات أصناف الخلط والمطابقة والكمية وخصومات الحد.

> [!NOTE]
> لا تقيد هذه الإعدادات عملية تجاوز السعر، حيث تقوم بتعيين السعر الأساسي ولا تتم معاملتها على أنها خصم.

[![حقل منع الخصومات](./media/prevent-discounts.png)](./media/prevent-discounts.png)
