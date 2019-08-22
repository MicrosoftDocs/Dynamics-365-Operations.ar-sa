---
title: إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين
description: يوضح هذا الإجراء كيفية إعداد تسعير يستند إلى سمة.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: ba84fa4de660d16b266763fff5b0b794ed327c81
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844191"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>إعداد تسعير يستند إلى سمة للمنتجات القابلة للتكوين

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إعداد تسعير يستند إلى سمة. كشرط مسبق، يجب أن يتوفر لديك نموذج تكوين منتج لديه مكون واحد أو أكثر وسمة واحدة أو أكثر. يستخدم هذا المثال نموذج مكبر الصوت المتطور في شركة بيانات العرض التوضيحي USMF. يستخدم مدير المنتج عادةً هذا الإجراء.


## <a name="create-a-new-price-model"></a>إنشاء نموذج سعر جديد
1. انقر فوق "تعريف نموذج متغير المنتج"ز
2. انقر فوق "نماذج تكوين المنتجات".
3. في القائمة، حدد بند "مكبر الصوت المتطور"، ولكن لا تنقر فوق الارتباط الخاص بالاسم.
4. في جزء الإجراءات، انقر فوق "النموذج".
5. انقر فوق "نماذج أسعار".
6. انقر فوق "جديد".
7. في الحقل "اسم نموذج السعر"، اكتب قيمة.
    * استخدم اسمًا يسهّل التعرف على النموذج.  
8. في وصف الحقل، اكتب قيمة.
9. انقر فوق "حفظ".

## <a name="add-price-elements"></a>إضافة عناصر السعر
1. انقر فوق "تحرير".
    * بإمكان كل مكون في نموذج المنتج أن يكون له عنصر سعر أساسي وأي عدد من قواعد تعبير السعر. يمكنك أيضًا إضافة أسعار بعملات مختلفة.  
2. في حقل "‏‫تعبير السعر الأساسي"، اكتب قيمة.
    * على سبيل المثال، اكتب "100".   بإمكان تعبير السعر الأساسي أن يكون عبارة عن قيمة رقمية، أو بإمكانه أن يتكون من عملية حسابية تتضمن سمة واحدة أو أكثر.  
3. وانقر فوق إضافة.
4. في حقل "الاسم"، اكتب "خشب الورد".
    * يساعد اسم تعبير السعر على تحديد ما يمثله عنصر السعر. في هذا المثال، نقوم بإنشاء عنصر سعر لخيار خزانة مكبر صوت من خشب الورد.  
5. انقر فوق "تحرير الشرط".
    * يساعد شرط السعر على ضمان تضمين عنصر تعبير السعر في سعر المبيعات فقط في حالة وجود مجموعة محددة من السمات.  
6. في الحقل ConstraintBody، أدخل 'CabinetFinish=="Rosewood"'.
7. انقر فوق "موافق".
8. في حقل "التعبير"، اكتب قيمة.
    * على سبيل المثال، اكتب "50".  
9. قم بإغلاق الصفحة.
10. قم بإغلاق الصفحة.

