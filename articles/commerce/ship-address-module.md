---
title: الوحدة النمطية لعنوان الشحن
description: يتناول هذا الموضوع الوحدة النمطية لعنوان الشحن ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/07/2020
ms.locfileid: "4410053"
---
# <a name="shipping-address-module"></a>الوحدة النمطية لعنوان الشحن

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الوحدة النمطية لعنوان الشحن ويشرح كيفية تكوينها في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

تسمح الوحدة النمطية لعنوان الشحن للعملاء بإضافة أو تحديد عنوان الشحن لأحد الأوامر أثناء سير مهام السداد مع الخروج. إذا قام العميل بتسجيل الدخول، فسوف يتم عرض أي عناوين تم حفظها في وقت سابق لهذا العميل، ويمكن للعميل الاختيار من بينها. ويُمكن للعميل أيضًا إضافة عنوان جديد. يتم استخدام الوحدة النمطية لعنوان الشحن لكافة الأصناف في الأمر التي تتطلب الشحن.

يمكن تحديد تنسيقات عناوين الشحن في مركز Commerce الرئيسي لكل بلد أو منطقة، وعندئذ تقوم الوحدة النمطية لعنوان الشحن بفرض القواعد الخاصة بالبلد/المنطقة.

عندما يقوم العملاء بإدخال عنوان شحن أثناء سير مهام السداد مع الخروج، يمكنهم حفظ العنوان كعنوان رئيسي. يظهر هذا الخيار فقط إذا سجل العميل دخوله.

وعلى الرغم من أن الوحدة النمطية لعنوان الشحن لا توفر ميزة التحقق من صحة العنوان، إلا أنه يُمكن تطبيق هذه الميزة من خلال التخصيص.

يبين الشكل التوضيحي التالي مثالاُ عن وحدة عنوان شحن جديدة في صفحة السداد مع الخروج.

![مثال عن الوحدة النمطية لعنوان الشحن على صفحة السداد مع الخروج](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>خصائص الوحدة النمطية

| اسم الخاصية | القيم | الوصف |
|---------------|--------|-------------|
| العنوان | نص العنوان وعلامة العنوان (**H1** أو **H2** أو **H3** أو **H4** أو **H5**  أو **H6**) | عنوان اختياري للوحدة النمطية لعنوان الشحن. |
| إظهار نوع العنوان | **صحيح** أم **خطأ** | إذا تم تعيين هذه الخاصية الاختيارية إلى **صواب**، فسيظهر نوع عنوان مثل **المنزل** أو **العمل**. إذا لم يتم تحديد نوع عنوان، سيتم حفظ العنوان تلقائيًا **النوع**=**غير ذلك**. |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>إضافة الوحدة النمطية لعنوان الشحن إلى صفحة السداد مع الخروج وتعيين الخصائص المطلوبة

يمكن إضافة وحدة نمطية لعنوان الشحن فقط إلى وحدة نمطية للسداد مع الخروج. لمزيد من المعلومات حول كيفية تكوين الوحدة النمطية لعنوان الشحن وإضافتها إلى صفحة السداد مع الخروج، راجع [الوحدة النمطية للسداد مع الخروج](add-checkout-module.md).

## <a name="additional-resources"></a>الموارد الإضافية

[الوحدة النمطية لعربة التسوق](add-cart-module.md)

[الوحدة النمطية لرمز عربة التسوق](cart-icon-module.md)

[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md)

[الوحدة النمطية للدفع](payment-module.md)

[الوحدة النمطية لخيارات التسليم](delivery-options-module.md)

[وحده معلومات الانتقاء](pickup-info-module.md)

[الوحدة النمطية لتفاصيل الأوامر](order-confirmation-module.md)

[الوحدة النمطية لبطاقة الهدايا](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]