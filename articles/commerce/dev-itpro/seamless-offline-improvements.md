---
title: التبديل السلس دون اتصال لعمليات بطاقة الهدايا وإشعار الدائن
description: يقدم هذا المقال نظرة عامه حول التحسينات التي توفر تبديلا سلسا دون اتصال لأنواع دفع معينه.
author: BrianShook
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: e0416a61bd5fd3b875b427ad8a6313d0e9936f0d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869151"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a>التبديل السلس دون اتصال لعمليات بطاقة الهدايا وإشعار الدائن

[!include [banner](../includes/banner.md)]

إذا كان هناك جهاز نقطه بيع (POS) يفقد اتصاله بقاعدة بيانات القناة، فيمكن متابعه معظم عمليات نقطه البيع والحركات التي كانت قيد التقدم بعد استلام الصراف رسالة تحذير حول فقد الاتصال. ومع ذلك، في بعض الحالات، يكون للحركات عناصر تعتمد على الخدمة في الوقت الحقيقي، ولا يتم دعم هذه العناصر عندما تكون نقطة البيع دون اتصال. يصف هذا المقال بعض الوظائف التي تساعد علي تقليل تأثير الاتصال المفقود في هذه السيناريوهات.

## <a name="completing-gift-card-transactions-in-offline-mode"></a>إكمال حركات بطاقات الهدايا في وضع دون الاتصال

تعتمد بطاقات الهدايا الداخلية على خدمة الوقت الفعلي، وذلك لأنه يجب الاحتفاظ بالرصيد الخاص ببطاقات الهدايا بشكل مركزي في المركز الرئيسي لـ Microsoft Dynamics 365 Commerce. للمساعدة في منع الاحتيال أو أية مشاكل أخرى في المزامنة، يتم تأمين بطاقات الهدايا بمجرد إضافتها إلى إحدى الحركات. تضمن وظيفة التأمين عدم إمكانية استخدام بطاقة الهدايا في العديد من الوحدات الطرفية في نفس الوقت. عند اكتمال الحركة، يتم تحديث وتأمين بطاقة الهدايا تلقائيًا.

ومع ذلك، إذا فقدت نقطة البيع الاتصال بعد إضافة بطاقة الهدايا إلى حركة، فقد تصبح بطاقة الهدايا غير قابله للاستخدام. وللمساعدة في منع حدوث هذا الأمر، تم تزويد Dynamics 365 Commerce بمعلمة تتيح الحركات التي تشتمل على سطر بطاقة الهدايا يتم إكمالها عندما تكون نقطه البيع دون اتصال. عند تشغيل هذه المعلمة، سيتم حفظ حركات بطاقة الهدايا التي تم فرضها دون اتصال مع الحركات غير المتصلة، وستتم مزامنتها في Commerce Headquarters عند مزامنة الحركات دون اتصال. ستؤدي المزامنة أيضا إلى إلغاء تامين بطاقة الهدايا بحيث يمكن استخدامها في وحده طرفيه أخرى.

لتمكين الوظيفة بحيث تُكمل حركات بطاقة الهدايا بعد التبديل إلى وضع دون اتصال، انتقل إلى علامة التبويب **ترحيل** على صفحة **معلمات Commerce**. في علامة التبويب هذه، حدد موقع علامة التبويب السريعة **بطاقة الهدايا** وقم بتعيين **‏‫السماح باختتام حركات بطاقات الهدايا في وضع دون الاتصال‬** إلى **نعم**.

![إعداد بطاقة الهدايا بدون اتصال.](../media/gift.png)

عادة ما يتم تخزين معلمات Commerce مؤقتا. لذلك، بعد تحديث إعداد هذه المعلمة، وبدء قيام جدولة التوزيع بمزامنة التغيير إلى القناة، يمكن أن يستغرق التغيير 24 ساعة ليصبح ساري المفعول. لجعل التغيير فعالا على الفور، قم بإعادة تعيين Microsoft Internet Information Services (IIS).

## <a name="completing-credit-memo-transactions-in-offline-mode"></a>إكمال حركات إشعار دائن في وضع دون الاتصال

على غرار بطاقات الهدايا الداخلية، يتم الاحتفاظ بإشعارات الدائن مركزيًا في Commerce Headquarters. يحتوي Commerce على معلمه تتيح إكمال حركات إشعار الدائن عندما تكون نقطه البيع غير متصلة. تعمل هذه المعلمة كمعلمه بطاقة الهدايا التي تم ذكرها في القسم السابق. عند تشغيل المعلمة، ستتم إعادة مزامنة حركات إشعار الدائن التي تم فرضها دون اتصال إلى قاعدة بيانات القناة، مع الحركات الأخرى التي تم اجراؤها أثناء عدم اتصال نقطه البيع.

لتمكين الوظيفة بحيث تُكمل حركات إشعارات الدائن بعد التبديل إلى وضع دون اتصال، انتقل إلى علامة التبويب **ترحيل** على صفحة **معلمات Commerce**. في علامة التبويب هذه، حدد موقع علامة التبويب السريعة **إشعار دائن** وقم بتعيين **‏‫‏‫السماح باختتام حركات إشعارات الدائن في وضع دون الاتصال‬** إلى **نعم**.

![إعداد إشعار الدائن دون اتصال.](../media/creditmemo.png)

عادة ما يتم تخزين معلمات Commerce مؤقتا. لذلك، بعد تحديث إعداد هذه المعلمة، وبدء قيام جدولة التوزيع بمزامنة التغيير إلى القناة، يمكن أن يستغرق التغيير 24 ساعة ليصبح ساري المفعول. لجعل التغيير فعالاً في الحال، قم بإعادة تعيين IIS.

## <a name="related-articles"></a>مقالات ذات صلة

- [وظيفة نقطة البيع دون اتصال](../pos-offline-functionality.md)
- [عمليات نقاط البيع (POS) أثناء الاتصال وعدم الاتصال بالإنترنت](../pos-operations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]