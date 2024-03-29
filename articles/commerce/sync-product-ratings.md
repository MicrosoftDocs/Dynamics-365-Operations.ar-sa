---
title: مزامنة تقييمات المنتجات في Dynamics 365 Commerce
description: يوضح هذا المقال كيفية مزامنة تقييمات المنتجات في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 7946bcaa9c6f318115640c6b20b00554a117dd38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282013"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>مزامنة تقييمات المنتجات في Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية مزامنة تقييمات المنتجات في Microsoft Dynamics 365 Commerce.

لاستهلاك تقييمات المنتجات في النقاط متعددة الاتجاهات، كما هو الحال في نقطة البيع (POS) وفي مراكز الاتصال، فإنه يجب استيراد تقييمات المنتجات من خدمة التقييمات والمراجعات إلى قاعدة بيانات قناة Commerce. عندما تتوفر تقييمات المنتجات في نقاط متعددة الاتجاهات، فإنها يمكن أن تساعد العملاء بشكل غير مباشر أثناء التفاعلات مع شركاء المبيعات.

يصف هذا المقال المهام التالية:

1. يمكنك تكوين **مهمة مزامنة تقييمات المنتجات** كمهمة مجموعه لمزامنة تصنيفات المنتجات من **خدمه التقييمات والمراجعات**.
1. تحقق من أن وظيفة الدفعية الخاصة بمزامنة تصنيف المنتجات ناجحة.
1. اجعل تقييمات المنتجات متوفرة عند نقطة البيع.

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>تكوين وظيفة دفعية في لمزامنة تقييمات المنتجات

> [!IMPORTANT]
> قبل البدء، تأكد من تثبيت الإصدار 10.0.6 أو الأحدث من Dynamics 365 Commerce.

### <a name="initialize-the-commerce-scheduler"></a>تهيئة مجدول التجارة

لتهيئة مجدول التجارة، اتبع الخطوات التالية.

1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر الرئيسي \> مجدول Commerce \>تهيئة مجدول التجارة**. بدلاً من ذلك، ابحث عن "تهيئة مجدول التجارة".
1. في مربع الحوار **تهيئة مجدول التجارة**، تأكد من أنه يتم إعداد الخيار **حذف تكوين موجود** على **لا**، ثم حدد **موافق**.

### <a name="verify-the-retailproductrating-subjob"></a>تحقق من الوظيفة الفرعية RetailProductRating

للتحقق من أن الوظيفة الفرعية **RetailProductRating** موجودة، اتبع هذه الخطوات.

1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر الرئيسي \> مجدول Commerce \>الوظائف الفرعية للمجدول**. وبدلاً من ذلك، ابحث عن "وظائف المجدول الفرعية".
1. في قائمة الوظيفة الفرعية، قم بإيجاد عن الوظيفة الفرعية **RetailProductRating** أو قم بالبحث عنها.

يبين الرسم التوضيحي التالي مثالاً على تفاصيل الوظيفة الفرعية في Commerce.

![تفاصيل الوظيفة الفرعية RetailProductRating.](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> في حالة عدم العثور على الوظيفة الفرعية **RetailProductRating**، فقد تكون قد قمت بالفعل بتشغيل وظيفة **مزامنة تقييمات المنتجات** ووظيفة **1040 CDX** قبل تهيئة مجدول Commerce. في هذه الحالة، اتبع هذه الخطوات لتشغيل وظيفة **مزامنة البيانات بالكامل**.

> 1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المقر الرئيسي \> مجدول Commerce \> قاعدة بيانات القناة**. بدلاً من ذلك، ابحث عن "قاعدة بيانات القناة".
> 1. حدد قاعدة بيانات القناة لمزامنتها.
> 1. في جزء الإجراء، حدد **مزامنة البيانات بالكامل**.
> 1. في مربع الحوار المنسدل **تحديد جدول توزيع**، حدد **1040 - منتجات**، ثم حدد **موافق**.
> 1. كرر خطوات الإجراء السابق للتحقق من أنه قد تم إنشاء الوظيفة الفرعية **RetailProductRating**.

### <a name="import-product-ratings"></a>استيراد تقييمات المنتجات

لاستيراد تقييمات المنتجات في Commerce من خدمة التقييمات والمراجعات، اتبع هذه الخطوات.

1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد المراكز الرئيسية \> مجدول Commerce \> مزامنة وظيفة تقييمات المنتجات**. بدلاً من ذلك، ابحث عن "مزامنة وظيفة تقييمات المنتجات".
1. في مربع حوار **سحب تقييمات المنتج**، في علامة التبويب السريعة **تشغيل في الخلفية**، حدد **التكرار**.
1. في مربع الحوار **تعريف التكرار**، قم بإعداد نمط التكرار. (القيمة المقترحة هي ساعتين). لا تقم بجدولة تكرار أقل من ساعة واحدة.
1. حدد **موافق**.
1. قم بتعيين الخيار **معالجة دفعة** على **نعم**. ويساعد هذا الإعداد على ضمان أنك ستتمكن من تدقيق السجلات والتحقق من حالة تشغيل وظيفة الدفعية.
1. حدد **موافق** لجدولة الوظيفة الدفعية.

يبين الرسم التوضيحي التالي مثالاً على تكوين الوظيفة الدفعية في Commerce.

![تكوين وظيفة دفعية لتقييمات المنتجات المتزامنة.](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>التحقق من أن وظيفة الدفعية الخاصة بمزامنة تصنيف المنتجات ناجحة

للتحقق من نجاح وظيفة دفعية **تقييمات المنتجات المتزامنة**، اتبع هذه الخطوات.

1. انتقل إلى **البيع بالتجزئة والتجارة \> مسؤول النظام \> استعلامات \> وظائف دفعية** أو إذا كنت تستخدم وحدة حفظ المخزون (SKU) لـ Retail and Commerce فقط بدلاً من ذلك، **البيع بالتجزئة والتجارة \> الاستعلامات والتقارير \> وظائف دفعية**. بدلاً من ذلك، ابحث عن "الوظائف الدفعية".
1. لعرض تفاصيل الوظيفة الدفعية، في قائمة الوظيفة الدفعية، في العمود **وصف الوظيفة**، ابحث عن وصف يحتوي على "سحب تقييمات المنتجات".
1. حدد معرف الوظيفة لعرض تفاصيل وظيفة الدفعية،+ مثل تاريخ/وقت البدء المجدول ونص التكرار.

يبين الرسم التوضيحي التالي مثالاً لتفاصيل وظيفة الدفعية في Commerce عندما تتم جدولة وظيفة الدفعية لتشغيل الفترات مدتها ساعتين.

![تفاصيل وظيفة الدفعية لتقييمات المنتجات المتزامنة.](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>جعل تقييمات المنتجات متوفرة عند نقطة البيع

حل التقييمات والمراجعات في Dynamics 365 Commerce حل متعدد الاتجاهات. ومع ذلك، لا يتم عرض تقييمات المنتجات في نقطة البيع بالوضع الافتراضي. لمساعده العملاء في المتاجر، راجع التقييمات والمراجعات عندما يتم الحصول عليها بواسطة إقرانات المبيعات، يجب عليك تشغيل تقييمات المنتجات في نقطة البيع.

لتشغيل تقييمات المنتج في نقطة البيع‬، اتبع الخطوات التالية.

1. انتقل إلى **البيع بالتجزئة والتجارة \> إعداد Commerce \> المعلمات \> معلمات Commerce**. بدلاً من ذلك، ابحث عن "معلمات Commerce".
1. في علامة التبويب **معلمات التكوين**، حدد **جديد**.
1. أدخل اسمًا مثل **RatingsAndReviews.EnableProductRatingsForRetailStores**، وقم بتعيين القيمة على **حقيقة**.
1. حدد **حفظ**.
1. انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**. بدلاً من ذلك، ابحث عن "جدول توزيع".
1. في قائمة الوظيفة ، حدد **1110** (**التكوين العمومي**)، ثم حدد **تشغيل الآن**.
1. بعد تشغيل الوظيفة بنجاح، تحقق من أن تقييمات المنتجات يتم عرضها الآن في نقطة البيع.

يبين الرسم التوضيحي التالي مثالاً لتكوين معلمات Commerce لعرض تقييمات المنتجات في نقطة البيع.

![تكوين معلمات Commerce لتقييمات المنتجات في نقطة البيع.](media/rnr-hq-enable-ratings-in-pos.png)

يبين الرسم التوضيحي التالي مثالاً لتقييمات المنتجات في نقطة البيع.

![تقييمات المنتجات في نقطة البيع.](media/rnr-pos-catalog-ratings.png)

يبين الرسم التوضيحي التالي مثالاً لتقييمات المنتجات في قنوات مركز الاتصال.

![تقييمات المنتجات في قناة مركز الاتصال.](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على التقييمات والمراجعات](ratings-reviews-overview.md)

[الموافقة على استخدام التقييمات والمراجعات](opt-in-ratings-reviews.md)

[إدارة التقييمات والمراجعات](manage-reviews.md)

[تكوين التقييمات والمراجعات](configure-ratings-reviews.md)

[مزامنة تقييمات المنتجات](sync-product-ratings.md)

[تمكين النشر اليدوي لتقييمات ومراجعات بواسطة المشرف](manual-publish-rating-reviews.md)

[استيراد التقييمات والمراجعات وتصديرها](import-export-reviews.md)

[تكوين مصادقة من خدمة إلى خدمة](service-to-service-auth.md)

[الأسئلة المتداولة حول التقييمات والمراجعات](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
