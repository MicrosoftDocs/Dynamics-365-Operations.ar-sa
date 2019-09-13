---
title: إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين
description: يوضح هذا الموضوع كيفية إعداد تسعير يستند إلى سمة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914689"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الموضوع كيفية إعداد تسعير يستند إلى سمة. كشرط مسبق، يجب أن يتوفر لديك نموذج تكوين منتج لديه مكون واحد أو أكثر وسمة واحدة أو أكثر. يستخدم هذا المثال نموذج مكبر الصوت المتطور في شركة بيانات العرض التوضيحي USMF. يستخدم مدير المنتج عادةً هذا الإجراء.


## <a name="create-a-new-price-model"></a>إنشاء نموذج سعر جديد
1. حدد **تعريف نموذج متغير المنتج‬** في الصفحة الرئيسية.
2. حدد **نماذج تكوين المنتج** في قسم **الارتباطات**.
3. في القائمة، حدد **مكبر الصوت المتطور** ولكن لا تنقر فوق الارتباط الخاص بالاسم.
4. في جزء الإجراءات، حدد **النموذج**.
5. حدد **نماذج الأسعار**.
6. حدد **جديد**.
7. في الحقل **اسم نموذج السعر**، اكتب قيمة. استخدم اسمًا يسهّل التعرف على النموذج.  
8. في حقل **الوصف**، اكتب قيمة.
9. حدد **حفظ**.

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

