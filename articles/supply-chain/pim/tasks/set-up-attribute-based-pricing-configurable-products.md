---
title: إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين
description: يوضح هذا المقال كيفية إعداد تسعير يستند إلى سمة.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec16a0a8078cddd433c99592aa4a7474cf923aec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849376"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين

[!include [banner](../../includes/banner.md)]

يوضح هذا المقال كيفية إعداد تسعير يستند إلى سمة. كشرط مسبق، يجب أن يتوفر لديك نموذج تكوين منتج لديه مكون واحد أو أكثر وسمة واحدة أو أكثر. يستخدم هذا المثال نموذج مكبر الصوت المتطور في شركة بيانات العرض التوضيحي USMF. يستخدم مدير المنتج عادةً هذا الإجراء.


## <a name="create-a-new-price-model"></a>إنشاء نموذج سعر جديد

1. انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.
1. في القائمة، حدد **مكبر الصوت المتطور** ولكن لا تنقر فوق الارتباط الخاص بالاسم.
1. في جزء الإجراءات، حدد **النموذج**.
1. حدد **نماذج الأسعار**.
1. حدد **جديد**.
1. في الحقل **اسم نموذج السعر**، اكتب قيمة. استخدم اسمًا يسهّل التعرف على النموذج.  
1. في حقل **الوصف**، اكتب قيمة.
1. حدد **حفظ**.

## <a name="add-price-elements"></a>إضافة عناصر السعر

1. حدد **تحرير**. بإمكان كل مكون في نموذج المنتج أن يكون له عنصر سعر أساسي وأي عدد من قواعد تعبير السعر. يمكنك أيضًا إضافة أسعار بعملات مختلفة.  
2. في حقل **‏‫تعبير السعر الأساسي**، اكتب قيمة. على سبيل المثال، اكتب "100". بإمكان تعبير السعر الأساسي أن يكون عبارة عن قيمة رقمية، أو بإمكانه أن يتكون من عملية حسابية تتضمن سمة واحدة أو أكثر.  
3. حدد **إضافة**.
4. في حقل **الاسم**، اكتب `Rosewood`. يساعد اسم تعبير السعر على تحديد ما يمثله عنصر السعر. في هذا المثال، نقوم بإنشاء عنصر سعر لخيار خزانة مكبر صوت من خشب الورد.  
5. حدد **تحرير الشرط**. يساعد شرط السعر على ضمان تضمين عنصر تعبير السعر في سعر المبيعات فقط في حالة وجود مجموعة محددة من السمات.  
6. في الحقل **ConstraintBody**، أدخل `CabinetFinish=="Rosewood"`.
7. حدد **موافق**.
8. في حقل **التعبير**، اكتب قيمة. على سبيل المثال، اكتب `50`. 
9. قم بإغلاق الصفحة.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]