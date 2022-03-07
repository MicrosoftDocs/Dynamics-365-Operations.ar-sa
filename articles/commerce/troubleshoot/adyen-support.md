---
title: استكشاف أخطاء موصل دفع Dynamics 365 لمشكلات Adyen
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعدك في الحصول على الدعم في حالة وجود مشكلات في موصل دفع Microsoft Dynamics 365 لـ Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019579"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>استكشاف أخطاء موصل دفع Dynamics 365 لمشكلات Adyen

[!include [banner](../../includes/banner.md)]

يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعدك في الحصول على الدعم في حالة وجود مشكلات في موصل دفع Microsoft Dynamics 365 لـ Adyen.

## <a name="description"></a>الوصف

لديك مشكلات في موصل دفع Dynamics 365 لـ Adyen في المناطق التالية، وطلبت الدعم من فريق Adyen:

- تكوين نقطة البيع (POS) أو نقطة البيع الحديثة (MPOS) أو مركز الاتصال أو Dynamics 365 Commerce
- رقم المرجع لموفر دفع لـ Adyen (PSP) (على سبيل المثال، إذا كان لديك أسئلة حول عمليات الرفض، يشمل ذلك عمليات رفض الإدخال اليدوي \[MKE\])
- أي شيء لا يعمل في بيئات الاختبار أو التاجر المباشر

## <a name="resolution"></a>الدقة

استخدم قالب البريد الإلكتروني التالي لبدء عملية الدعم مع فريق Adyen. للإسراع في استكشاف الأخطاء وإصلاحها، تأكد من احتواء البريد الإلكتروني على كافة التفاصيل المطلوبة.

| الحقل        | قيمة |
|--------------|-------|
| إلى           | `support@adyen.com` |
| نسخة           | |
| سطر الموضوع | طلب دعم Microsoft Dynamics |
| النص الأساسي         | <p>مرحبًا فريق الدعم،</p><p>الرجاء توفير الدعم للمشكلة التالية:</p><ul><li>حساب التاجر</li><li>البيئة (اختبار/إنتاج)</li><li>القناة (نقطة بيع/مركز اتصال/تجارة إلكترونية عبر Commerce)</li><li>رقم مرجع PSP، إذا كانت المشكلة متضمنة لحركة محددة (يمكنك العثور على رقم مرجع PSP في الإيصال، في منطقة عملاء Adyen أو في قائمة الحركات في الوحدة الطرفية لنقطة البيع.)</li><li>لقطة شاشة أو صورة لرسالة الخطأ، إذا كانت ممكنة</li><li>سجلات عارض الأحداث (بتنسيق txt.)</li><li>وصف المشكلة وخطوات استكشاف الأخطاء وإصلاحها التي حاولتها</li></ul> |

## <a name="additional-resources"></a>الموارد الإضافية

[قبول المدفوعات باستخدام موصل Adyen لـ Dynamics 365 Commerce](https://www.adyen.com/partners/dynamics-365-commerce)

[موصل دفع Dynamics 365 لـ Adyen](../dev-itpro/adyen-connector.md)

[إعداد موصل دفع Adyen لـ Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
