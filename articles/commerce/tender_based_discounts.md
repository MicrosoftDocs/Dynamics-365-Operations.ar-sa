---
title: الخصومات المستندة إلى طريقة الدفع
description: يقدم هذا الموضوع نظرة عامة حول الوظيفة التي تتيح لبائعي التجزئة تكوين خصومات لأنواع معينة من طرق الدفع.
author: bebeale
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 9f6747ff9d68c29612346254928e869d6d34d433
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962925"
---
# <a name="tender-based-discounts"></a>الخصومات المستندة إلى طريقة الدفع

[!include [banner](includes/banner.md)]


ويعتبر هذا الاجراء من الممارسات الشائعة بين بائعي التجزئة لإصدار بطاقات ائتمان خاصة وبطاقات تحمل علامات تجارية. ويستفيد بائعو التجزئة بسبب حصولهم على أسعار مفضلة من البنوك. بالإضافة إلى ذلك، نظرًا لأن بطاقات الائتمان هذه تشجع العملاء على زيارة المتجر بشكل أكثر تكرارا، فإنهم يساعدون في تحسين الخط السفلي لبائع التجزئة. وبالتالي، يكون لبائعي التجزئة حافز لزيادة استخدام العميل لبطاقات الائتمان التي تحمل علاماتهم التجارية. ولتحقيق هذا الهدف، يقوموا غالبًا بتوفير خصومات إضافية إلى العملاء الذين يستخدمون بطاقات الائتمان هذه.

بدلا من ذلك، قد يرغب بائعو التجزئة الذين لا يوفرون بطاقات ائتمان تحمل علامة تجارية في تشجيع العملاء على الدفع باستخدام طرق دفع أخرى، مثل بطاقات الهدايا أو البطاقات النقدية أو نقاط الولاء. بهذه الطريقة، يمكنهم المساعدة في تقليل مصروفات معالجة بطاقة الائتمان. وبالتالي، قد يوفر البائعون خصومات إلى العملاء الذين يستخدمون طرق الدفع البديلة هذه.

في Microsoft Dynamics 365 Commerce، يمكن لبائعي التجزئة تكوين نسبه مئوية للخصم يتم تطبيقها على البنود المؤهلة في حاله دفع العميل باستخدام طريقة الدفع المفضلة. يمكن للعميل أن يقرر ما إذا كنت تريد إجراء دفع جزئي أو دفع كامل، ويقوم Commerce بتحديد مبلغ الخصم المناسب. لاحظ أنه يتم دائما تقديم الخصم في مبلغ ما قبل الضريبة للأصناف المؤهلة.

لا يمكن للخصومات التي تستند إلى طريقة الدفع التنافس مع الخصومات المستندة إلى الأصناف، مثل الخصومات الدورية أو اليدوية. وهي دائمًا تكون مركبة على خصومات الصنف. وبالتالي، حتى في حالة تطبيق خصم دوري حصري على أحد الأصناف، فلا يزال يتم تطبيق الخصم الذي يستند إلى طريقة الدفع على رأس الخصم الدوري الخاص. بالمثل، في حالة تطبيق خصم الحد على الحركة، وكان الخصم المستند إلى طريقة الدفع يقلل الإجمالي الموجود تحت الحد، فلا يزال يتم تطبيق خصم الحد على الحركة.

على الرغم من أن الخصومات المستندة إلى طريقة الدفع تقلل من الإجمالي الفرعي للحركة، إلا أن الرسوم التلقائية التي يتم تطبيقها على الحركة لا تتأثر. على سبيل المثال، إذا تم حساب رسوم التسليم على أنها $5 للن الإجمالي الفرعي قد زاد عن $100، وكان الخصم المستند إلى طريقة الدفع يقلل المبلغ بحيث يقل عن $100، فإن رسوم التسليم لا تزال $5 للأمر.


> [!NOTE]
> يتم توزيع الخصومات المستندة إلى طريقة الدفع بشكل تناسبي على بنود المبيعات المؤهلة وتقليل مبلغ ما قبل الضريبة للبنود الفردية. في حاله تكوين خصومات متعددة مستندة إلى طريقة الدفع لنوع طريقة دفع (علي سبيل المثال، النقد)، يتم تطبيق أفضل خصم قائم على طريقة الدفع فقط.

يمكن تطبيق الخصومات المستندة إلى طريقة الدفع فقط على بنود المبيعات التي لا يتم تأمين الأسعار فيها. في حالة إضافة بنود مبيعات جديدة إلى أمر، يتم تطبيق الخصم المستند إلى طريقة الدفع على بنود المبيعات الجديدة فقط أثناء عملية الدفع. بينما يتم وضع أمر العميل الخاص بالانتقاء أو الشحن، يتم تطبيق الخصم المستند إلى طريقة الدفع فقط على مبلغ الإيداع. بعد وضع الأمر ، وخلال التنفيذ، يتم تأمين أسعار بنود المبيعات. وبالتالي، لا يتم تطبيق خصم يستند إلى طريقة الدفع على أي رصيد يتم دفعه أثناء الانتقاء أو اعتماده أثناء الشحن. يمكن تطبيق الخصم الذي يستند إلى طريقة الدفع على المبلغ الكامل الخاص بأمر العميل فقط في حالة قيام بائع التجزئة بتجميع المبلغ الكامل كايداع أثناء وضع الأمر.

> [!IMPORTANT]
> في Commerce، يتم تحديد الخصومات المستندة إلى طريقة الدفع حاليا إلى نوعين من أنواع الدفع: بطاقات الائتمان والنقد.

## <a name="pos-user-experience"></a>تجربة مستخدم نقطة البيع

في حالة إعداد الخصم المستند إلى طريقه الدفع لنقدية، وكان الصراف في نقطة البيع (POS) يحدد زرًا يتم تعيينه إلى عملية الدفع النقدي، يتم تطبيق الخصم المستند إلى طريقة الدفع تلقائيًا على الحركة. يتم بعد ذلك إظهار المبلغ المخفض باعتباره الرصيد. ومع ذلك، إذا قام الصراف بتحديد الزر **السابق** على شاشة الدفع، تتم إزالة الخصم، ويتم عرض المبلغ الأصلي على شاشة الحركة. تتم إزالة الخصم الذي يستند إلى طريقة الدفع إذا تم إلغاء بند الدفع.

بالنسبة لمدفوعات البطاقات، يمكن لبائعي التجزئة تعيين الخصم المستند إلى طريقة الدفع بواحد أو أكثر من أنواع بطاقات الائتمان. ومع ذلك، لا يمكن للنظام التحقق من نوع بطاقة الائتمان المستخدمة ما لم يتم اعتماد البطاقة. في حالة تطبيق الخصم بعد التخويل، سيكون تخويل الدفع خاصًا بمبلغ أكبر، ولكن سيكون التقاط الدفع خاصًا بمبلغ أصغر.

للمساعدة في منع هذه الحالة، إذا دفع أحد العملاء باستخدام بطاقة ائتمان، سيشاهد الصراف مربع حوار يسرد بطاقات الائتمان التي ستجلب مدخرات العميل الإضافية. يمكن للصراف عندئذ أن يسأل عما إذا كان العميل يريد استخدام إحدى البطاقات المفضلة للحصول على خصم إضافي. في حالة استخدام الصراف لبطاقة مفضلة، يتم تطبيق الخصم الذي يستند إلى طريقة الدفع على الحركة، ويظهر المبلغ المخفض على شاشة الدفع. سيكون التخويل خاصًا بالمبلغ المخفض. إذا قام العميل بإدراج بطاقة تختلف عن البطاقة التي قام الصراف بتحديدها، تظهر رسالة خطأ، ويتم إلغاء التفويض.


## <a name="call-center-user-experience"></a>تجربة مستخدم مركز الاتصال

عندما يحدد المستخدم **مكتمل** أثناء طلب مركز الاتصال، يتم عرض شاشة **الإجماليات**. في البداية، لا تتضمن الإجماليات الموجودة في هذه الشاشة الخصومات المستندة إلى طريقة الدفع، للن طريقة الدفع لم يتم تحديدها بعد. في شاشة **‏‫إضافة الدفع‬**، إذا قام المستخدم بتحديد طريقة الدفع التي يتم تكوين الخصم المستند إلى طريقة الدفع بناءً عليها، فانه يتم تعديل مبلغ الدفع تلقائيًا بحيث يعكس المبلغ المخصوم. مثل العميل في نقطه البيع، يمكن لعميل مركز الاتصال تقرير ما إذا كان سيتم سداد الدفع الكامل أو الدفع الجزئي. واستنادا إلى المبلغ الذي يتم دفعه، يتم تطبيق الخصم المستند إلى طريقة الدفع على أمر المبيعات.

> [!NOTE]
> لم يتم التحقق من صحة البطاقة لأوامر مركز الاتصال. علي سبيل المثال، إذا قام مستخدم مركز الاتصال بتحديد Visa كبطاقة الائتمان، ولكن العميل يستخدم Mastercard، يستمر النظام في تطبيق الخصم.

## <a name="exclude-items-from-discounts"></a>استبعاد أصناف من الخصومات

غالبًا ما يختار بائعو التجزئة استبعاد بعض المنتجات، مثل الأصناف الجديدة أو الأصناف الموجودة في الطلب، من الخصومات. ومع ذلك، قد لا يزالوا يرغبون في تطبيق الخصومات المستندة إلى طريقة الدفع. على سبيل المثال، يقوم البائع بالتجزئة بتكوين Commerce بحيث لا يسمح بالخصومات التي تعتمد على الأصناف أو الخصومات اليدوية. ومع ذلك، في حالة سداد العميل باستخدام طريقة الدفع المفضلة، يزال Commerce يطبق الخصم المستند إلى طريقة الدفع. لاعداد Commerce بهذه الطريقة، يجب على تجار التجزئة الانتقال إلى **إدارة معلومات المنتج > المنتجات > المنتجات الصادرة**، حددها، ثم في علامة التبويب السريعة **Commerce**، قم بتعيين الخيارين **منع كل الخصومات** و **منع الخصومات استنادًا إلى العطاء** إلى **لا** وخياري **منع خصومات البيع بالتجزئة** و **منع الخصومات اليدوية** إلى **نعم**.

> [!NOTE]
> عند تعيين تكوين **منع كل الخصومات** إلى **نعم**، لن يتم تطبيق أي خصومات على المنتج. ولن يتم تطبيق حتى الخصومات المستندة إلى طريقة الدفع.


[!INCLUDE[footer-include](../includes/footer-banner.md)]