---
title: شراء الإجازة وبيعها
description: توضح هذه المقالة كيفية إرسال الطلبات لشراء وبيع الإجازات في Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a6d38a69a73ce14f099beb6b6b560bf6c5686b0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875702"
---
# <a name="buy-and-sell-leave"></a>شراء الإجازة وبيعها


>[!Important]
>تتوفر الوظيفة المذكورة في هذة المقالة حاليًا للعملاء في Dynamics 365 Human Resources المستقل. ستتوفر بعض الوظائف أو كلها كجزء من الإصدار المستقبلي على بنية Finance الأساسية بعد إصدار 10.0.26 من Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

في Dynamics 365 Human Resources ، يمكن إرسال طلبات لشراء الإجازة وبيعها استنادًا إلى إعداد سياسات شراء وبيع الإجازات الخاص بشركتك.  

## <a name="request-to-buy-leave"></a>طلب شراء إجازة

1. في مساحة عمل **خدمة الموظف الذاتية** حدد **طلب شراء إجازة** في اللوحة **أرصدة زمن التوقف**. 

2. أضف **نوع إجازة** وفي حقل **المقدار** أدخل مقدار الإجازة الذي ترغب في شرائه. 

3. حدد **إرسال** عندما تكون مستعدا لتقديم طلبك. 

سيتم إما تحديث رصيدك تلقائيًا أو المرور بعملية اعتماد قبل التحديث. ويعتمد ذلك علي كيفية تكوين سياسة الشراء.

## <a name="request-to-sell-leave"></a>طلب بيع إجازة

1. في مساحة عمل **خدمة الموظف الذاتية** حدد **طلب بيع إجازة** في اللوحة **أرصدة زمن التوقف**. 

2. أضف **نوع إجازة** وفي حقل **المقدار** أدخل مقدار الإجازة الذي ترغب في بيعه. 

3. حدد **إرسال** عندما تكون مستعدا لتقديم طلبك.

سيتم إما تحديث رصيدك تلقائيًا أو المرور بعملية اعتماد قبل التحديث. ويعتمد ذلك علي كيفية تكوين سياسة الشراء.


## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها 

في حالة فشل سير عمل طلب شراء أو بيع، يمكن للمستخدمين الذين لديهم الامتياز **EssLeaveBuySellRequestApprover** مراجعة سجل الرسائل لكافة طلبات الشراء والبيع. للقيام بذلك، انتقل إلى **الإجازة والغياب > الارتباطات > طلبات شراء وبيع الإجازة > سجل الرسائل** (في الجانب العلوي الأيسر). يعرض **سجل الرسائل** للمستخدمين كيفية معالجة الحركات ومحفوظات سير العمل المرتبطة.


## <a name="see-also"></a>راجع أيضًا

[نظرة عامة على الإجازة والغياب](hr-leave-and-absence-overview.md)</br>
[إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
