---
title: معلومات دفع العميل (معاينة)
description: توضح هذه المقالة إمكانيات الرؤى الخاصة بالدفع والتي تساعد على تحسين فهم ممارسات الدفع النموذجية للعملاء الفرديين. يمكن أن تساعدك الميزة في تحديد الحالات التي تقوم بضبط بدء عمليات الجمع قبل الانتهاء من القيام بذلك.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5d2c811ac48a6bf29267192f61a33b6b47721659
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068155"
---
# <a name="customer-payment-insights-preview"></a>معلومات دفع العميل (معاينة)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

توضح هذه المقالة إمكانيات الرؤى الخاصة بالدفع والتي تساعد على تحسين فهم ممارسات الدفع النموذجية للعملاء الفرديين. يمكن أن تساعدك الميزة في تحديد الحالات التي تقوم بضبط بدء عمليات الجمع قبل الانتهاء من القيام بذلك. 

## <a name="overview"></a>نظرة عامة

يمكن أن يكون من الصعب توقع الوقت الذي سيقوم فيه العميل بتسديد الفواتير. وهذا يعني القيام برؤية أعمق لتقديرات تدفقات نقديه دقيقه اقل وعمليات تحصيل تبدا في وقت طويل جدا ، والأوامر التي يتم إصدارها إلى العملاء الذين قد يقومون بعمليات الدفع بشكل افتراضي. تساعد معلومات دفع العميل (المعاينة) المؤسسات في توقع الوقت الذي سيقوم فيه العميل بتسديد فاتورة. يمكن أن تساعد هذه المعلومات المؤسسات في إنشاء استراتيجيات التحصيلات التي تحسن احتمال الدفع في الوقت المحدد. 

## <a name="predictions"></a>التوقعات

ستمكّن تنبؤات الدفع المؤسسات من تحسين عملياتها التجارية من خلال مساعدتها على تحديد الفواتير التي يُحتمل سدادها في وقت متأخر ، واتخاذ التدابير المناسبة لتحسين فرصها في الحصول على أموال في الوقت المحدد.

باستخدام نموذج للتعلم الآلي ، والذي يعمل على زيادة الفواتير التاريخية والمدفوعات وبيانات العميل ، تتنبأ رؤى دفع العميل (معاينة) بمزيد من الدقة عندما يقوم العميل بدفع فاتورة معلقة.

لكل فاتورة مفتوحة، يمكن أن تتوقع معلومات دفع العميل (المعاينة) ثلاثة احتمالات دفع:

-   احتماليه اجراء الدفع في الوقت الحالي 
-   احتماليه اجراء الدفع لاحقًا
-   احتماليه اجراء الدفع في وقت متأخر جدًا

توفر أيضًا رؤى دفع العملاء (معاينة) في الوقت المحدد والمتأخر والمتأخر جدًا طريقة عرض مجمعة للمدفوعات المتوقعة، الأمر الذي يمكن أن يساعد المؤسسات على فهم إجمالي مبلغ الدفع الذي يمكن أن تتوقعه من أحد العملاء في أحد المجموعات الثلاثة.

[![العرض المجمع لتنبؤات الدفع.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

ويتم تعيين احتماليه الدفع في كل فاتورة علي الوقت. إذا كان احتمال الدفع في الوقت المحدد أقل من 50 ٪ ، يتم وضع علامة الفواتير مع دائرة حمراء للإشارة إلى أن هذه الفواتير قد تتطلب اهتمام المجموعات. 

[![قائمة احتمالات الدفع.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

توفر رؤى دفع العملاء (معاينة) أيضًا معلومات سياقية لشرح التنبؤ ، مثل أهم العوامل التي أثرت على التنبؤات ، وحالة العمل الحالية مع العميل ، وتفاصيل عن سلوك الدفع للعملاء السابقين. في العديد من الشركات ، كانت عملية التحصيلات نشاطًا تفاعليًا ؛ لا تبدأ عملية المجموعات إلا بعد استحقاق الفواتير. 

من خلال رؤى العملاء للدفع (معاينة) ، يمكن للمؤسسات أن تكون أكثر نشاطًا بشأن المجموعات. لم يعد عليهم الانتظار حتى تصبح المعاملات مستحقة لبدء عملية التحصيل. بدلاً من ذلك ، يمكنهم استخدام إمكانية التنبؤ بالدفع لتحديد ما إذا كانت المجموعات الاستباقية ستحسن من احتمال الدفع في الوقت المحدد. كما يوفر التنبؤ بالدفع للشركات المعلومات اللازمة لتبرير بدء عملية التحصيل مبكرًا.

## <a name="methodology"></a>منهجية

يعد تطوير حل AI ونشره أمرا صعبا. يتطلب الأمر فريقًا من علماء البيانات وخبراء الموضوع والمهندسين، يعملون لفترة طويلة من الزمن لصياغة وتطوير ونشر وصيانة حل AI صالح للاستعمال. نحن نسهل نشر واستخدام حلول الذكاء الاصطناعي في Finance. نحن نعد حلول AI المعبأة مسبقًا في Finance المبنية على Microsoft AI Builder. يمكن للمستخدم النهائي ، بنقرة زر واحدة ، نشر حل الذكاء الاصطناعي والبدء في الاستفادة من فوائد التنبؤات الذكية. إذا لم تكن أي مؤسسة راضية عن دقة التنبؤات، فيمكن للمستخدم القوي، مرة أخرى باستخدام نقرة واحدة، الدخول في تجربة توسيع AI builder، ثم تحديد أو إلغاء تحديد الحقول المستخدمة لإنشاء التنبؤات. بمجرد الاستعداد ، يمكنهم تدريب ونشر التغييرات ، وسيتم اختيار النموذج المدربين حديثًا تلقائيًا للتنبؤات في Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>كيفية الحصول على معلومات دفع العميل (المعاينة)

أرسل بريد إلكتروني إلى [معلومات دفع العميل (المعاينة)](mailto:fiap@microsoft.com)، إذا كنت ترغب في تجربة معلومات دفع العميل (المعاينة).

## <a name="privacy-notice"></a>إشعار الخصوصية

قد تستخدم الإصدارات الأولية (1) تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) لديها دعم محدود.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]

