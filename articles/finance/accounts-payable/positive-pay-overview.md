---
title: نظرة عامة على الدفع الإيجابي
description: توفر هذه المقالة معلومات حول الدفع الإيجابي الذي يُستخدم لإنشاء قائمة إلكترونية بالشيكات التي يمكن تقديمها إلى البنك.
author: panolte
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ffb2ded8c6f1e86657f298f3638da39ac4c63b66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972096"
---
# <a name="positive-pay-overview"></a>نظرة عامة على الدفع الإيجابي

[!include [banner](../includes/banner.md)]

توفر هذه المقالة معلومات حول الدفع الإيجابي الذي يُستخدم لإنشاء قائمة إلكترونية بالشيكات التي يمكن تقديمها إلى البنك. 

يُستخدم الدفع الإيجابي لإنشاء قائمة إلكترونية بالشيكات التي يمكن تقديمها إلى البنك. بإمكان ملفات الدفع الإيجابي أن تساعد البنوك على منع تزوير الشيكات المصرفية. ستقوم بإعداد الدفع الإيجابي لإنشاء قائمة إلكترونية بالشيكات في كل مرة تتم فيها طباعة الشيكات. بعد ذلك، عندما يتم تقديم أحد الشيكات إلى البنك، يقارن البنك الشيك بقائمة الشيكات التي قدمتها في وقت سابق. إذا تطابق الشيك مع شيك آخر في القائمة، فسيقوم البنك بمخالصته. أما إذا لم يتطابق الشيك لم تطابق مع أي شيك آخر في القائمة، فسيحتفظ البنك به لمراجعته.

يُعرف أيضًا الدفع الإيجابي بالدفع الآمن. 

يمكن أن تحتوي ملفات الدفع الإيجابي على معلومات هامة حول المستفيدين ومبالغ الشيكات. لذلك، تأكد من استخدام تدابير أمنية مناسبة اعتبارًا من وقت إنشاء الملفات وحى استلام البنك لها. يتم تنزيل ملفات الدفع الإيجابي وفقًا لإرشادات التنزيل لمستعرض ويب. 

يتم إنشاء ملفات الدفع الإيجابي باستخدام كيانات البيانات. وقبل إنشاء ملف دفع إيجابي، يجب إعداد تنسيقات التحويل الخاصة بتنسيق XML الذي يترجم البيانات إلى تنسيق يستطيع البنك استخدامه. 

لكل حساب بنكي تريد إنشاء معلومات دفع إيجابي له، يجب تعيين تنسيق الدفع الإيجابي. بعد إنشاء الدفعات، يمكنك إنشاء ملف دفع إيجابي لكيان قانوني واحد وحساب بنكي واحد. أو، يمكنك إنشاء ملفات الدفع الإيجابي لعدة كيانات قانونية وحسابات بنكية في الوقت نفسه. 

بعد اتمام دفع كل الشيكات المدرجة في ملف الدفع الإيجابي، ستتلقى رقم تأكيد من البنك. يمكنك عندئذٍ تأكيد ملف الدفع الإيجابي في النظام. 

إذا لزم تغيير ملف دفع إيجابي، فيمكنك إعادة استدعائه. بعد ذلك، ولكل شيك في ملف الدفع الإيجابي، يُعاد تعيين الحقل الذي يشير إلى ما إذا تم تضمين الشيك في ملف دفع إيجابي.

لمزيد من المعلومات، راجع [إعداد ملفات الدفع الإيجابي وإنشاؤها‬‏‫](set-up-generate-positive-pay-files.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]