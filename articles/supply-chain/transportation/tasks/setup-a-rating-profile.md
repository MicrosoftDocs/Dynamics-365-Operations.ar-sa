---
title: ملفات تعريف التقييم
description: يصف هذا المقال كيفية إعداد بيانات ملفات تعريف التصنيف.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7408574187ddb099181bd2566c46c52307f603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850456"
---
# <a name="rating-profiles"></a>ملفات تعريف التقييم

[!include [banner](../../includes/banner.md)]

يمثل ملف تعريف التقييم عقد التجهيز (لكن ليس عقدا قانونيا). وهو يستخدم لتحديد تعريفات نقل الحمولات. 

يعتبر كل ملف تعريف تقييم فريداً لشركة شحن. في كل ملف تعريف، يتم إقران أسعار شركة الشحن بسجل أسعار رئيسي. يحدد سجل الأسعار الرئيسي مهمة قاعدة الأسعار وقاعدة الأسعار. تحدد قاعدة السعر سعر الناقل.

يمكنك إعداد ملف تعريف تقييم باستخدام صفحة عامة تعرض نظرة عامة على كافة ملفات تعريف التقييم الموجودة. بدلاً من ذلك، يمكنك إعداد ملف تعريف تقييم مباشرة من شركة الشحن. وفي كلتا الحالتين ، تكون المعلومات التي قمت بإعدادها لملف تعريف التصنيف هي نفسها.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>إنشاء ملف تعريف التقييم أو تحريره في صفحه ملفات تعريف التصنيف

في صفحه **ملفات تعريف التصنيف**، يمكنك مراجعه كافة ملفات تعريف التصنيف المتوفرة. يمكنك أيضا تحرير ملفات تعريف موجودة وإنشاء ملفات تعريف جديده.

1. انتقل إلى **إدارة النقل \> إعداد \> التقييم‬ \> السجل الرئيسي للأسعار**.
1. في جزء الاجراء، حدد **جديد** لأضافه ملف تعريف تقييم جديد إلى الشبكة ، أو حدد **تحرير** لتحرير ملف تعريف موجود.
1. في الصف الخاص بملف تعريف التقييم الجديد أو الموجود ، قم بتعيين الحقول التالية:

    - **ملف تعريف التصنيف** أدخل معرّفًا فريدًا (ID) ووصفًا لملف تعريف التقييم.
    - **الاسم** - أدخل اسمًا وصفيًا لملف تعريف التصنيف.
    - **شركه الشحن** - تحديد شركه شحن. سيظهر أيضا ملف تعريف التقييم الذي تقوم بإعداده في الصفحة **شركات الشحن** لشركه الشحن المحددة.
    - **الموقع** و **المستودع** - تحديد موقع ومستودع.
    - **محرك الأسعار** – تحديد محرك الأسعار لملف تعريف التصنيف.
    - **السجل الرئيسي للأسعار** – تحديد السجل الرئيسي للأسعار لملف تعريف التصنيف. يمكنك استخدام سجل الأسعار الرئيسي لتعريف نوع قاعد السعر وقاعدة السعر. لمزيد من المعلومات، راجع [إعداد السجلات الرئيسية اللأسعار‬‬‬‬](set-up-rate-masters.md).
    - **محرك وقت تحديد عدد أيام النقل** – تحديد محرك الوقت الخاص بتحديد عدد أيام النقل لملف تعريف التقييم.
    - **مؤشر الوقود لشركة النقل** - تحديد مؤشر الوقود لشركة النقل لملف تعريف التقييم.
    - **تاريخ ووقت بدء السريان** و **تاريخ ووقت انتهاء السريان** - تحديد الفترة التي يجب ان يكون فيها ملف تعريف التصنيف نشطا.

1. في جزء الإجراءات، حدد **حفظ**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>إنشاء ملف تعريف التقييم مباشرة في صفحه شركات الشحن

1. انتقل إلى **إدارة النقل \> إعداد \> شركات النقل‬‬ \> شركات الشحن‬‬**.
1. حدد شركة شحن في القائمة.
1. في علامة التبويب السريعة **ملفات تعريف التصنيف**، حدد **جديد** لإنشاء ملف تعريف تقييم.
1. تتيح تعيين الحقول لملف تعريف التقييم الجديد. تتوافق هذه الحقول مع الحقول الموجودة في صفحه **ملفات تعريف التصنيف**، كما هو موضح في القسم السابق من هذا المقال.

> [!NOTE]
> ويتم أيضا عرض ملفات التعريف التي تم إنشاؤها في الصفحة **شركات الشحن** في صفحه **ملفات تعريف التصنيف**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]