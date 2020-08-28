---
title: وحدة بطاقة الهدايا
description: يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661232"
---
# <a name="gift-card-module"></a>وحدة بطاقة الهدايا

[!include [banner](includes/banner.md)]

يتناول هذا الموضوع وحدات بطاقة الهدايا ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

تعتبر بطاقات الهدايا طريقة دفع شائعة، ويمكن استخدام وحدة بطاقة الهدايا في وحدة السداد مع الخروج لقبول بطاقات الهدايا. تدعم وحدة بطاقة الهدايا بطاقات هدايا Dynamics 365 وSVS وGivex. يتم استرداد بطاقات الهدايا من SVS وGivex من خلال موفر الدفع Adyen.

لمزيد من المعلومات عن دعم بطاقات الهدايا الخارجية مثل SVS وGivex، راجع [و دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)

تعرض الصورة التالية مثالاً عن وحدة بطاقة هدايا في صفحة السداد مع الخروج.

![مثال عن وحدة بطاقة هدايا](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>خصائص الوحدة النمطية

- **إظهار حقول** - تحدد هذه الخاصية الحقول التي يجب عرضها لبطاقات الهدايا بالإضافة إلى رقم بطاقة الهدايا، الذي يظهر دائمًا بشكل افتراضي. على سبيل المثال، تدعم بعض بطاقات الهدايا رقم تعريف شخصي (PIN) ويدعم البعض الآخر عرض رمز PIN وتاريخ انتهاء الصلاحية. بدلاً من ذلك،،يمكن تعيين هذه الخاصية إلى "بلا"، مما يؤدي إلى عرض رقم بطاقة الهدايا فقط ومن دون حقول إضافية.

القيم المدعومة:
-   رمز PIN
-   تاريخ انتهاء الصلاحية
-   رمز PIN وتاريخ انتهاء الصلاحية 
-   بلا‬‬

## <a name="site-settings-for-gift-card-modules"></a>إعدادات الموقع لوحدات بطاقة الهدايا

في منشئ موقع Commerce، ضمن **إعدادات الموقع \> Extensions**، هناك إعداد لوحدة بطاقة هدايا يسمى **نوع بطاقة الهدايا المدعومة**. يدعم هذا الإعداد ثلاث قيم:
- **بطاقة هدايا Dynamics 365** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 فقط. هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.
- **بطاقات هدايا SVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا SVS وGivex فقط. هذا الإعداد مدعوم للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية بالإضافة إلى المستخدمين المجهولي الهوية.
- **بطاقات هدايا Dynamics 365 وSVS وGivex** - عند تطبيق هذا الإعداد، تسمح وحدة بطاقة الهدايا باسترداد بطاقات هدايا Dynamics 365 وSVS وGivex. هذا الإعداد مدعوم فقط للمستخدمين الذين سجلوا دخولهم في موقع التجارة الإلكترونية.

## <a name="add-a-gift-card-module-to-a-page"></a>إضافة وحدة بطاقة هدايا إلى صفحة

للحصول علي إرشادات حول كيفية إضافة وحدة بطاقة هدايا إلى صفحة السداد مع الخروج‬ وتعيين الخصائص المطلوبة، راجع [وحدة السداد مع الخروج](add-checkout-module.md).

## <a name="additional-resources"></a>الموارد الإضافية

[الوحدة النمطية لعربة التسوق](add-cart-module.md)

[وحدة أيقونة عربة التسوق](cart-icon-module.md)

[الوحدة النمطية للسداد مع الخروج](add-checkout-module.md)

[الوحدة النمطية للدفع](payment-module.md)

[الوحدة النمطية لعنوان الشحن](ship-address-module.md)

[الوحدة النمطية لخيارات التسليم](delivery-options-module.md)

[وحدة تفاصيل الأوامر](order-confirmation-module.md)

[دعم بطاقات الهدايا الخارجية](./dev-itpro/gift-card.md)
