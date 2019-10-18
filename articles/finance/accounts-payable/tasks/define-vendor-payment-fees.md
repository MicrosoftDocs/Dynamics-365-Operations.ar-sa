---
title: ‏‫تحديد رسوم دفع المورّد‬
description: إعداد رسوم مدفوعات المورّد.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9e723ec54b6f34082c422ce4c8e48bf52d2e3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189443"
---
# <a name="define-vendor-payment-fees"></a>‏‫تحديد رسوم دفع المورّد‬

[!include [task guide banner](../../includes/task-guide-banner.md)]

إعداد رسوم مدفوعات المورّد. تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.

1. انتقل إلى الحسابات المدينة > إعداد الدفع‬ > رسوم الدفع‬.
2. انقر فوق "جديد".
3. في الحقل "معرف الرسوم"، اكتب قيمة.
    * يجب أن يصف "معرف الرسوم" الوقت الذي سيتم استخدام هذه الرسوم، مثل "EFT_Fee".  
4. في حقل "الاسم"، اكتب قيمة.
5. في حقل "وصف الرسوم"، اكتب قيمة.
    * أضف وصفًا لتوفير مزيد من التفاصيل حول الوقت الذي سيتم فيه فرض الرسوم.  
6. في الحقل "التكلفة‬"، حدد المورّد أو دفتر الأستاذ.
    * يتم استخدام دفتر الأستاذ عندما يتم تسجيل نفقات الرسوم لمؤسستك.  يتم استخدام المورّد عند فرض الرسوم على المورّد.  
7. أدخل حسابًا رئيسيًا حيث سيتم تسجيل نفقات الرسوم.
    * يتوفر هذا الخيار فقط عند تحديد "دفتر الأستاذ" كخيار "تكلفة".  
8. حدد دفتر اليومية الذي يمكن استخدام هذه الرسوم عليه. 
    * بالنسبة إلى رسوم الدفع الخاصة بالمورّد، يمكنك تحديد "نفقة المورّد" لدفتر اليومية.  
9. انقر فوق "حفظ".
10. انقر فوق "إعداد رسوم الدفع‬".
    * تابع إلى "إعداد رسوم الدفع" لتعريف متى يجب تعيين الرسوم كافتراضية في دفتر اليومية الذي قمت بتحديده.  
11. حدد "الجدول" أو "المجموعة" أو "الكل".
    * يُستخدم خيار "الجدول" لتحديد حساب بنكي واحد, ويُستخدم خيار "المجموعة" لتحديد مجموعة بنكية ويُستخدم خيار "الكل" لاستخدام إعداد الرسوم هذا لجميع الحسابات البنكية  
12. حدد مجموعة بنكية أو حسابًا بنكيًا.
    * سوف يعرض البحث المجموعة البنكية إذا قمت بتحديد "المجموعة"، وسيعرض الحسابات البنكية إذا قمت بتحديد "الجدول".  
13. حدد طريقة الدفع التي يجب فرض هذه الرسوم عليها.
14. حدد مواصفات الدفع لطريقة الدفع المحددة.
    * يتم استخدام مواصفات الدفع مع طرق الدفع التي تتم بواسطة تحويل الأموال إلكترونيًا.  
15. حدد ما إذا كانت الرسوم عبارة عن نسبة مئوية أو مبلغ أو فاصل زمني.
16. أدخل النسبة المئوية للرسوم أو مبلغ الرسوم.
    * إذا كانت الرسوم عبارة عن نسبة مئوية، فأدخل النسبة المئوية. وإذا كانت الرسوم عبارة عن مبلغ، فأدخل مبلغ الرسوم. أما إذا كانت الرسوم عبارة عن "فاصل زمني"، فاستخدم علامة التبويب "الفاصل الزمني" لتحديد الرسوم المتدرجة.  
17. في حقل "عملة الرسوم‬"، حدد العملة التي سيتم فرض الرسوم بها.
    * هذه العملة تتعلق بالرسوم. يتم استخدام عملة الدفع لتعريف متى ينبغي أن يتم تقييم قاعدة الرسوم استنادًا إلى عملة الدفع. على سبيل المثال، قد يفرض عليك البنك رسومًا عند إجراء الدفع باليورو، ولكن لا يتم فرض أي رسوم على جميع المدفوعات الأخرى.  
18. انقر فوق "حفظ".
