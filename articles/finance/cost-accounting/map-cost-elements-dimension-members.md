---
title: تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد
description: من خلال تعيين أعضاء أبعاد عنصر تكلفة مختلفين إلى مجموعة مشتركة من أعضاء أبعاد عنصر تكلفة، ستقوم بدمج البيانات في تنسيق مشترك لأغراض التحليل.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 79b235af60e452b80d99c13a2fc80d322a02fc04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976155"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>تعيين أعضاء أبعاد عنصر التكلفة لمجموعة شائعة من أعضاء الأبعاد

[!include [banner](../includes/banner.md)]

من خلال تعيين أعضاء أبعاد عنصر تكلفة مختلفين إلى مجموعة مشتركة من أعضاء أبعاد عنصر تكلفة، ستقوم بدمج البيانات في تنسيق مشترك لأغراض التحليل.

إذا كنت شركة عالمية تمتثل لمتطلبات المحاسبة القانونية، فقد تستخدم أدلة حسابات متعددة. عندما تقوم باستيراد أعضاء أبعاد عنصر تكلفة من أدلة حسابات مختلفة، قد ينتهي بك الأمر بالحصول على مزيج حسابات. ومع ذلك، فإن هذه الحسابات قد تكون مماثلة في الواقع من حيث طبيعتها، وقد تحتاج إلى تحليل وتوزيع التكاليف الخاصة بها باستخدام تنسيق مشترك.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>تعيين أعضاء أبعاد عنصر التكلفة‬ إلى تنسيق مشترك
يوضح المثال التالي كيف يمكنك أنت، بصفتك مراقب التكاليف، إنشاء بُعد جديد لعنصر تكلفة في محاسبة التكاليف يقوم بتعيين أعضاء أبعاد عنصر التكلفة من بنية دليل الحسابات الأمريكي وبنية دليل الحسابات الفرنسي إلى مجموعة مشتركة من أعضاء أبعاد عنصر التكلفة. ويمكنك عندئذٍ استخدام المجموعة المشتركة من أعضاء أبعاد عنصر التكلفة لتحليل بيانات التكلفة من الكيانين القانونيين في دفتر أستاذ محاسبة التكاليف.

| المصدر: دليل الحسابات الأمريكي                                          | المصدر: دليل الحسابات الفرنسي                                          | مجموعة مشتركة جديدة من أعضاء أبعاد عنصر التكلفة                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| استيراد أعضاء أبعاد عنصر التكلفة من دليل الحسابات الأمريكي | أعضاء أبعاد عنصر التكلفة المستوردون من دليل الحسابات الفرنسي | تعيين أعضاء أبعاد عنصر التكلفة الأمريكيين والفرنسيين إلى مجموعة مشتركة |
| 5001: المبيعات                                                           | 5001: المبيعات والإعلانات                                               | 5000: المبيعات والإعلانات                                             |
| 5030: الإعلانات                                                     | 6390: شراء المخزون\*                                                    | 7000: مصروفات التنظيف                                                 |
| 7001: مصروفات التنظيف                                               | 7001: مصروفات السفر                                                      | 7001: مصروفات السفر                                                   |

\*لم يتم تعيين عضو بُعد عنصر التكلفة الفرنسي لشراء المخزون.

## <a name="currency-conversion"></a>تحويل العملة
من المحتمل أن يكون قد تم إعداد أدلة الحسابات المختلفة التي تستخدمها لاستخدام عملات مختلفة. في هذه الحالة، تأكد من تحديد تحويل عملة، بحيث تتم معالجة بيانات التكلفة باستخدام العملة الصحيحة، كما هو محدد في دفتر أستاذ محاسبة التكاليف حيث يتم استخدام أعضاء أبعاد عنصر التكلفة. في المثال السابق، إذا تم استخدام الدولار الأمريكي (USD) في دفتر أستاذ محاسبة التكاليف، فيجب إنشاء تحويل عملة من الدولار إلى اليورو (EUR) لمعالجة الحركات لأعضاء أبعاد عنصر التكلفة المعينين.

## <a name="update-mappings-at-any-time"></a>تحديث التعيينات في أي وقت
يمكنك تحديث تعريفات التعيينات لبُعد عنصر تكلفة في أي وقت. ولأن التعيينات غير محددة بتاريخ سريان، فسيتم تطبيق التغييرات في المرة التالية التي تقوم فيها بمعالجة حركات التكلفة أو تشغيل حسابات التكلفة.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]