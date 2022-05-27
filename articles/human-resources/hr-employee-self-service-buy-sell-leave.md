---
title: شراء الإجازة وبيعها
description: يصف هذا الموضوع كيفية إرسال طلبات لشراء وبيع الإجازات في Dynamics 365 Human Resources.
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
ms.openlocfilehash: 695840516849dcfeb69895f6808d828d5878c59b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688165"
---
# <a name="buy-and-sell-leave"></a>شراء الإجازة وبيعها


>[!Important]
>تتوفر الوظيفة المذكورة في هذا الموضوع حاليًا للعملاء في Dynamics 365 Human Resources المستقل. ستتوفر بعض الوظائف أو كلها كجزء من الإصدار المستقبلي على بنية Finance الأساسية بعد إصدار 10.0.26 من Finance.

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
