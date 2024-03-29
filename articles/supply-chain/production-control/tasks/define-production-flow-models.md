---
title: تحديد نماذج تدفق الإنتاج
description: تصف نماذج تدفق الإنتاج تصف كيفية حساب خلايا عمل lean manufacturing والاحتفاظ بها.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlowModel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fb12be6f744cee8af3a845d6b278d1f1462ec5d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579126"
---
# <a name="define-production-flow-models"></a>تحديد نماذج تدفق الإنتاج

[!include [banner](../../includes/banner.md)]

تصف نماذج تدفق الإنتاج تصف كيفية حساب خلايا عمل lean manufacturing والاحتفاظ بها. وبالتالي يُعد تحديد نموذج تدفق الإنتاج متطلبًا أساسيًا لتحديد خلايا العمل. شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="define-a-production-flow-model"></a>حدد نموذج تدفق إنتاج. 
1. انتقل إلى التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > نماذج تدفق الإنتاج.
2. انقر فوق "جديد".
3. في الحقل "نموذج تدفق الإنتاج"، أدخل معرفًا لنموذج تدفق الإنتاج.
4. في الحقل "نوع النموذج"، حدد خيارًا.
    * هناك نوعان من النماذج: نوع الإنتاجية ونوع ساعات. بالنسبة لنوع الإنتاجية، سيتم التعبير عن قدرة خلايا العمل التي تستخدم نموذج تدفق الإنتاج هذا وحسابها باستخدام كميات المنتجات. بالنسبة لنوع الساعات، سيتم التعبير عن قدرة خلايا العمل التي تستخدم نموذج تدفق الإنتاج هذا وحسابها باستخدام الساعات. لاحظ أنه لا يمكن تغيير هذه الخاصية لنموذج تدفق إنتاج موجود. بعد تعيين حجوزات القدرة الإنتاجية لخلية عمل، لن يمكن تغيير نوع نموذج تدفق الإنتاج.  
5. أدخل عدد الأيام في دورة EPE.
    * يصف الفاصل الزمني الفترة التي سيتم بها إنتاج كل جزء ناتج عن تدفق إنتاج أو خلية عمل مرة واحدة على الأقل. كلما قلت مدة دورة EPE، زادت مرونة عملية الإنتاج. إذا كانت دورة EPE تساوي 0، يمكن إنتاج الطلب بالكامل في نفس اليوم. تُستخدم دورة EPE لجدولة مهام العملية محدودة الفاقد. عند جدولة مهمة بخلية عمل وكانت دورة EPE تساوي 5، ستبحث عملية الجدولة عن القدرة في خلية العمل في تاريخ الاستحقاق-دورة EPE" (5 أيام قبل تاريخ الاستحقاق) للتأكد من إمكانية إنتاج المنتج في هذه الدورة. يكون وقت إنتاج المخزون الخاص بأحد المنتجات مساويًا لدورة EPE لعملية الإنتاج ذات الصلة أو أكبر منها في العادة.  
6. في الحقل "فترة التخطيط"، حدد خيارًا.
    * بعد تعيين حجوزات القدرة لخلية عمل، لن يمكن تغيير نوع فترة التخطيط. لا يمكنك تحديد نماذج تدفق الإنتاج إلا مع نفس نوع الفترة الخاص بخلية العمل المحددة هذه.  
7. في الحقل "الحد الزمني للتخطيط" أدخل رقمًا.
    * يصف الحد الزمني للتخطيط عدد الأيام التي يمكن بها إجراء حجوزات القدرة لخلايا العمل ذات الصلة. في الحل "الحد الزمني للتخطيط"، أدخل عدد الأيام.   لا يتم تخطيط وظائف عملية كانبان التي تقع خارج نطاق هذه الفترة باستخدام التخطيط التلقائي. يساوي الحد الزمني للتخطيط عادة ضعف متوسط وقت إنتاج المخزون للمنتجات التي يتم إنتاجها تدفق إنتاج أو خلية عمل. يجب أن تكون دورة EPE أكبر من نصف الحد الزمني للتخطيط.     
8. في الحقل "التفاعل مع العجز في القدرة"، حدد خيارًا.
    * تتضمن الخيارات: تأجيل - تأجيل الطلب الكامل لحدث الجدولة في يوم الإنتاج التالي المتوفر، مع الإنتاجية المتوفرة. إلغاء - إنهاء التخطيط التلقائي لحدث الجدولة وترك الوظائف المرتبطة من دون تخطيط.   إضافة إلى اليوم المطلوب - تخطيط الوظائف المطلوبة للفترة المطلوبة. يؤدي هذا إلى تحميل الخلية بشكل زائد لهذا اليوم ويتطلب من المخطط إجراء مراجعة وتدخل يدوي.   التوزيع على الفترات المتاحة - توزيع الوظائف المختلفة لحدث الجدولة على جميع أيام الإنتاج المتاحة، بدءًا من اليوم الأول المتاح. التوزيع على الفترات المتاحة - توزيع الوظائف المختلفة لحدث الجدولة على جميع أيام الإنتاج المتاحة، بدءًا من اليوم الأول المتاح.‬ الحد الأدنى لكمية التوزيع هو كمية وظيفة كانبان. يعين التوزيع الحد الأدنى لكمية التخطيط (كمية كانبان) لكل يوم بإنتاجية كافية متوفرة.‬‬  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]