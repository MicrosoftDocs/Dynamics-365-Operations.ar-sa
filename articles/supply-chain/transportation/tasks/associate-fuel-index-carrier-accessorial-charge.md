---
title: إقران مؤشر وقود بشركة نقل كرسوم إضافية
description: يوضح هذا الدليل كيفية إنشاء المهام الإضافية والتكلفة الإضافية لشركة الشحن‬ والسجل الرئيسي للتكاليف الإضافية للوقود‬ وإقرانها بمؤشر وقود الناقل‬ مع ناقل.
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2df77fe94156e2b60b77fa1c995ea10eab048a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670541"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>إقران مؤشر وقود بشركة نقل كرسوم إضافية

[!include [banner](../../includes/banner.md)]

يوضح هذا الدليل كيفية إنشاء المهام الإضافية والتكلفة الإضافية لشركة الشحن‬ والسجل الرئيسي للتكاليف الإضافية للوقود‬ وإقرانها بمؤشر وقود الناقل‬ مع ناقل. تحتاج إلى إعداد مؤشر وقود الناقل قبل تشغيل هذا الدليل. يمكنك استخدام الدليل "إعداد مؤشر وقود الناقل‬‬" للقيام بذلك. عادة ما يتم تنفيذ هذه المهام من قِبل إدارة اللوجستيات‬. بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.


## <a name="create-an-accessorial-master"></a>إنشاء سجل رئيسي إضافي
1. انتقل إلى إدارة النقل > إعداد > التقييم‬ > الأصول الإضافية.
2. انقر فوق "جديد".
3. في الحقل "الأصول الإضافية‬"، اكتب قيمة.
4. في حقل "الاسم"، اكتب قيمة.
5. انقر فوق "حفظ".

## <a name="create-a-carrier-accessorial-charge"></a>إنشاء التكلفة الإضافية لشركة الشحن
1. انتقل إلى إدارة النقل > إعداد > التقييم‬ > التكاليف الإضافية لشركة النقل‬.
2. انقر فوق "جديد".
3. في الحقل "معرف شركة النقل الإضافية‬"، اكتب قيمة.
4. في الحقل "شركة الشحن "، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * في هذا المثال، اختر "شركة النقل".  
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. ‏‫في الحقل "خدمة الناقل‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.‬
8. في القائمة، انقر فوق الارتباط في الصف المحدد.
9. في الحقل "الأصل الإضافي‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
10. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * في هذا المثال، اختر الأصل الإضافي الذي أنشأته مؤخرًا.‬  
11. انقر فوق "حفظ".

## <a name="create-an-accessorial-assignment"></a>إنشاء مهمة إضافية
1. انقر فوق "المهام الإضافية".
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. بدّل توسيع المقطع "المعايير".
    * في المعايير، يمكنك اختيار تطبيق التكاليف الإضافية للوقود‬ دائمًا أو في هذا المثال اختيار تطبيقها فقط داخل منطقة معينة.  
5. في الحقل "الرمز البريدي من"، اكتب قيمة.
6. في الحقل "الرمز البريدي إلى"، اكتب قيمة.
7. بدّل توسيع المقطع "الحساب".
    * في مقطع الحساب، يمكنك تحديد كيفية حساب التكاليف الإضافية للوقود‬. يعتمد هذا الحساب على الوحدة الإضافية‬ التي اخترتها كأساس للحساب.  
8. في الحقل "نوع الرسوم الإضافية‬"، حدد "التكاليف الإضافية للوقود‬".
9. في الحقل "الوحدة الإضافية‬"، حدد "المسافة المقطوعة بالأميال‬".
10. في الحقل "المنطقة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
11. في القائمة، انقر فوق الارتباط في الصف المحدد.
12. انقر فوق "حفظ".

## <a name="update-the-carrier-rating-profile"></a>تحديث ملف تعريف تصنيف شركة الشحن
1. انتقل إلى إدارة النقل > الإعداد > شركات النقل > شركات الشحن.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. بدّل توسيع المقطع "ملفات تعريف التقييم‬‬".
4. انقر فوق "تحرير".
5. في الحقل "مؤشر وقود الناقل‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.
6. في القائمة، انقر فوق الارتباط في الصف المحدد.
7. انقر فوق "حفظ".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]