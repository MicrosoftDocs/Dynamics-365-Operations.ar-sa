---
title: وحدة أيقونة عربة التسوق
description: يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793071"
---
# <a name="cart-icon-module"></a>الوحدة النمطية لرمز عربة التسوق

[!include [banner](includes/banner.md)]

يتناول هذا الموضوع وحدة أيقونة عربة التسوق ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

تمثل وحدة أيقونة عربة التسوق في وحدة الرأس على الصفحة، وتُظهر عدد الأصناف في سلة التسوق. تعرض أيضًا وحدة أيقونة سلة التسوق ملخص السلة (تعرف أيضًا بسلة تسوق صغيرة) عند تمرير الماوس فوق أيقونة السلة. توفر سلة التسوق الصغيرة للمستخدم ملخص الأصناف الموجودة في سلة التسوق دون الحاجة إلى الانتقال إلى صفحة سلة التسوق. بالإضافة إلى ذلك، تسمح أيضًا للمستخدم بالانتقال مباشرةً إلى صفحة السداد مع الخروج إذا أعجبه الملخص. يؤدي ذلك إلى تقليل عدد عمليات التنقل في الصفحات ويسهل عملية السداد والخروج. 

> [!NOTE]
> يتوفر دعم الوحدة النمطية لأيقونة عربة التسوق في الوحدات النمطية للرأس في Dynamics 365 Commerce الإصدار 10.0.11.

تظهر الصورة التالية مثالاً عن وحدة أيقونة سلة تسوق تعرض سلة تسوق صغيرة في رأس Fabrikam.

![مثال عن وحدة أيقونة سلة التسوق](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>خصائص الوحدة النمطية

- **إظهار سلة التسوق الصغيرة** – تمكّن هذه الخاصية، عندما تكون قيمتها صواب، عرض ملخص سلة التسوق (سلة التسوق الصغيرة) عند تمرير الماوس فوق أيقونة سلة التسوق. هذه الوظيفة مدعومة فقط لمنافذ عرض سطح المكتب.

## <a name="add-a-cart-icon-module-to-a-page"></a>إضافة وحدة سلة التسوق إلى صفحة

لإضافة وحدة ايقونة سلة التسوق، راجع [وحدة الرأس](author-header-module.md).

## <a name="additional-resources"></a>الموارد الإضافية

[الوحدة النمطية لعربة التسوق](add-cart-module.md)

[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md)

[الوحدة النمطية للدفع](payment-module.md)

[الوحدة النمطية لعنوان الشحن](ship-address-module.md)

[الوحدة النمطية لخيارات التسليم](delivery-options-module.md)

[الوحدة النمطية لمعلومات الانتقاء](pickup-info-module.md)

[الوحدة النمطية لتفاصيل الأوامر](order-confirmation-module.md)

[الوحدة النمطية لبطاقة الهدايا](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]