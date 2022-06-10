---
title: لا يشمل الإجمالي الفرعي لملخص الطلب الضرائب المفروضة على الرسوم عند استخدام وحدات ملخص الطلب المخصصة
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعدك عند استخدام وحدات نمطية مخصصة لملخص الطلب ولا يتضمن الإجمالي الفرعي لملخص الطلب الضرائب على الرسوم في سيناريو "السعر يشمل ضريبة المبيعات".
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767938"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>لا يشمل الإجمالي الفرعي لملخص الطلب الضرائب المفروضة على الرسوم عند استخدام وحدات ملخص الطلب المخصصة

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها التي يمكن أن تساعدك عند استخدام وحدات نمطية مخصصة لملخص الطلب ولا يتضمن الإجمالي الفرعي لملخص الطلب الضرائب على الرسوم في سيناريو "السعر يشمل ضريبة المبيعات".

## <a name="description"></a>‏‏الوصف‬

اعتبارًا من الإصدار 10.0.27 من Microsoft Dynamics 365 Commerce، تم إجراء التغييرات التالية على سيناريو "السعر يشمل ضريبة المبيعات" لتوفير تجربة متسقة في وحدات ملخص الطلب عبر صفحات موقع التجارة الإلكترونية.

- تم إضافة حقلين جديدين: **TaxOnShippingCharge** و **TaxOnNonShippingCharges**.
- تتضمن واجهات برمجة التطبيقات **GetSalesOrderBySalesId** و **GetSalesOrderByTransactionId** قيم دقيقة للحقول التالية في سيناريو "السعر يشمل ضريبة المبيعات":

    - SubtotalSalesAmount
    - SubtotalAmountWithoutTax
    - SubtotalAmount
    - ShippingChargeAmount
    - OtherChargeAmount

ومع ذلك، إذا كنت تستخدم وحدات ملخص الطلب المخصصة، فقد تؤثر هذه التغييرات على قيم الإجمالي الفرعي لملخص الطلب من خلال عدم تضمين الضرائب في التكاليف.

## <a name="resolution"></a>القرار

إذا كنت تستخدم وحدات نمطية مخصصة لملخص الطلب ولا تريد أن ترث التغييرات التي تم إجراؤها على سيناريو "السعر يشمل ضريبة المبيعات" في الإصدار التجاري 10.0.27 والإصدارات الأحدث، فاتبع الإرشادات الواردة في هذا القسم.

بالرجوع إلى سلوك ملخص الأمر السابق (قبل الإصدار 10.0.27) لحقلي **salesTransaction.SubtotalAmount** و **salesTransaction.SubtotalAmountWithoutTax**،، يمكنك استعادة تضمين إجمالي مبلغ ضريبة التكاليف(**TaxOnShippingCharge** و **TaxOnNonShippingCharges**) في المبالغ الإجمالية الفرعية (**SubtotalAmount** و **SubtotalAmountWithoutTax**).

للعودة إلى سلوك ملخص الأمر السابق، اتبع هذه الخطوات.

1. في Commerce headquarters، افتح صفحة معلمات Commerce (**Retail وCommerce \> إعداد Headquarters \> المعلمات \> معلمات Commerce**).
1. في جزء التنقل الأيسر، حدد **معلمات التكوين**.
1. أضف معلمات التكوين التالية، وقم بتعيين قيمة كل منها على **صواب**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryHydrationEnabled

> [!NOTE]
> إذا سبق لك استخدام معلمة تكوين **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** وتريد الاحتفاظ بنفس السلوك لخاصية  **order.NetAmountWithoutTax**، فيجب عليك أيضًا إضافة معلمة تكوين **IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** وتعيين قيمتها إلى **صواب**.

## <a name="additional-resources"></a>الموارد الإضافية

[إخفاء معلومات التخفيف الضريبي في ملخصات الأوامر](../hide-taxes-breakup.md)
