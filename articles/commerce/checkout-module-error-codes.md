---
title: أكواد مرجع الخطأ للوحدة النمطية للسداد
description: توضح هذه المقالة أكواد مرجع الخطأ للوحدة النمطية للسداد التي يتم عرضها في رسائل الخطأ الخاصة بالمستخدم في Microsoft Dynamics 365 Commerce
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709641"
---
# <a name="checkout-module-error-reference-codes"></a>أكواد مرجع الخطأ للوحدة النمطية للسداد

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

توضح هذه المقالة أكواد خطأ الوحدة النمطية للسداد التي تظهر في رسائل الخطأ التي تواجه المستخدم في Microsoft Dynamics 365 Commerce.

يقدم Dynamics 365 Commerce مراجع أخطاء قياسية يمكن تضمينها في أخطاء السداد للقناة عبر الإنترنت التي يتم تقديمها للعملاء عبر الإنترنت. في الإصدار التجاري 10.0.31 والإصدارات الأحدث، تتضمن رسائل الخطأ في الوحدة النمطية للسداد أكواد الخطأ ولا تعرض معلومات غير ضرورية للعميل عبر الإنترنت. تشير أكواد الخطا إلى الأخطاء التي يتم تفصيلها في هذه المقالة.

استناداً إلى الخطأ الذي تمت مواجهته، يتضمن الجدول الموجود في هذه المقالة التفاصيل التالية:

- وصف الحالة التي تسببت في الخطأ أو تفاصيل إضافية
- معلومات يجب مراعاتها في تكوينات البيئة أو موصل الدفع
- المعلومات التي يمكن الرجوع إليها في حالة الدعم، إذا كانت هناك حاجة إلى مساعدة إضافية

## <a name="checkout-module-error-reference-codes"></a>أكواد مرجع الخطأ للوحدة النمطية للسداد

استخدم الجدول التالي للحصول على مزيد من التفاصيل حول مراجع كود الخطأ التي يتم توفيرها بواسطة العملاء أو من ذوي الخبرة في المتجر عبر الإنترنت.

| رمز الخطأ | كود الخطأ مرتبط بالديناميات | وصف الخطأ |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | لا يمكن السماح بالدفع. يكون معرف نوع البطاقة في **TokenizedPaymentCard** مفقودًا، أو يكون معرف نوع البطاقة المقدم غير مدعوم. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | مرفوض. لا يمكن السماح بالدفع. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | لا يمكن السماح بالدفع. معلومات إضافية مطلوبة من العميل. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | عذرًا، حدث خطأ ما. تعذر الحصول على نتيجة قبول الدفع بالبطاقة. حاول مرة أخرى أو اتصل بمسؤول النظام. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | تعذر السداد بسبب فقدان خصائص الدفع للتاجر. اتصل بمسؤول النظام. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | تعذر استرداد خدمة طريقة الدفع للعملية. تحقق من إعداد طريقة الدفع الخاصة بك لطريقة الدفع المحددة. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | تم تطبيق دفعة حساب العميل بالفعل ولا يُسمح إلا بدفعة واحدة لكل حركة. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | يختلف حد حساب العميل عن المبلغ المستحق. جرب طريقة دفع مختلفة أو اتصل بدعم العملاء للحصول على المساعدة. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | تجاوزت مدفوعات حساب العميل إجمالي المستحق للعناصر المدرجة. حاول مرة أخرى لاحقًا أو اتصل بدعم العملاء للحصول على المساعدة. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | يتطلب دفع حساب العميل حسابه الخاص أو حساب الفاتورة المطابق في بند الدفع. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | تعذرت معالجة دفع حساب العميل في هذا الوقت – تم تجاوز قيمة الحد الأدنى. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | لا يُسمح لهذا العميل بالدفع على الحساب. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | عذرًا، حدث خطأ ما. لا يمكن إلغاء الدفع. حاول مرة أخرى. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | حدث خطأ أثناء معالجة الدفع. حاول مرة أخرى في وقت لاحق. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | ‏‫يتجاوز مبلغ دفع الولاء المسموح به لبطاقة الولاء هذه في تلك الحركة. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | ‏‫يتجاوز مبلغ استرداد الولاء المسموح به لبطاقة الولاء المستخدمة في تلك الحركة.‬ |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | لم يتم العثور على رقم بطاقة الولاء. قم بتنشيط رقم بطاقة الولاء أو أدخل رقم بطاقة مختلفًا، ثم أعد المحاولة مرة أخرى.‬ |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | رقم بطاقة الولاء غير متوفر. أدخل رقم بطاقة مختلف، ثم حاول مرة أخرى. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | تُعد بطاقة الولاء هذه غير مؤهلة لاسترداد نقاط الولاء لهذه الحركة. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | واجه رقم بطاقة الهدايا خطأ. جرب بطاقة هدايا مختلفة أو اتصل بدعم العملاء للحصول على المساعدة. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | تجاوز المبلغ الرصيد المتبقي في بطاقة الهدايا. أدخل مبلغ مختلف، ثم حاول مرة أخرى. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | لا يمكن أن تتضمن الحركة أكثر من بند دفع ولاء واحد. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | معلومات الدفع إما أن تكون مفقودة أو غير صحيحة. تحقق من معلومات الدفع ثم حاول مرة أخرى. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | لا يمكن معالجة الطلب في هذا الوقت. حاول مرة أخرى في وقت لاحق. |
| CCR025     | مهلة الواجهة الأمامية لواجهه برمجه تطبيقات السداد | انتهت مهلة عملية الواجهة الأمامية. قم بتأكيد ما إذا كان الطلب قد تمت معالجته في Dynamics 365 Commerce headquarters. |
| CCR026     | تم تغيير المبلغ التفويض الأصلي | تم تغيير مبلغ الطلب من مبلغ التفويض الأصلي الذي تمت معالجته باستخدام بوابة الدفع. قد يكون هذا بسبب انتهاء صلاحية القسيمة أو العرض الترويجي أو البيع. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | حدث خطأ أثناء معالجة الدفع. يحتوي المرجع الذي تم توفيره لواجهه برمجه التطبيقات السلة علي مرجع مختلف عن المرجع المتوقع (وهذا ما يشير إلى حدوث عدم تناسق محتمل اثناء عملية السداد). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | واجهت طريقة الدفع التي تمت تجريبها خطأً. اتصل بالدعم لمراجعة إعدادات حسابك أو حاول مرة أخرى بطريقة دفع مختلفة. |

## <a name="additional-resources"></a>الموارد الإضافية

[الأسئلة المتداولة حول الدفعات](dev-itpro/payments-retail.md)

[وحدة السداد مع الخروج](add-checkout-module.md)

[وحدة للدفع](payment-module.md)
