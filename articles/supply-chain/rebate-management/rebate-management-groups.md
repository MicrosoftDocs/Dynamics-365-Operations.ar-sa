---
title: مجموعات إدارة الخصومات
description: يصف هذا المقال كيفية إعداد بيانات مجموعات إدارة الخصومات. يمكن استخدام مجموعات أداره الخصم اثناء حسابات الخصومات ويمكن إرفاقها بسجل رئيسي.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2b948e994783d6ec6f00b77d12bd2594a29f6512
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851525"
---
# <a name="rebate-management-groups"></a>مجموعات إدارة الخصومات

[!include [banner](../includes/banner.md)]

يمكن أن تعتمد حسابات إدارة الخصم على المجموعات. يمكن إنشاء مجموعات أداره الخصم للعملاء والموردين والأصناف. يمكن إرفاقها بسجل رئيسي.

## <a name="rebate-management-customer-groups"></a>مجموعات عملاء إدارة الخصومات

غالبًا ما يتم إنشاء الحساب لمجموعة من العملاء لسلسلة من الشركات، مثل سلسلة سوبر ماركت أو شركة امتياز. عاده ما يرتبط هذا النوع من الحساب بالخصم.

غالبا ما يتم حساب الخصم دون الأخذ في الاعتبار من بيع أمر التاهيل. ومع ذلك، هناك استثناءات. على سبيل المثال، قد ينشئ المرخص له مخطط خصم حيث ستحصل مجموعة العملاء أ على 4 في المائة، لكن مجموعة العملاء ب ستحصل على 3 في المائة فقط.

### <a name="set-up-customer-groups"></a>إعداد مجموعات العملاء

للعمل مع مجموعات عملاء إدارة الخصم، انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات\> مجموعات العملاء**. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة المجموعات وإزالتها كما هو مطلوب. بالنسبة لكل مجموعة، قم بتعيين الحقول التالية:

- **مجموعة إدارة الخصومات** – أدخل اسمًا فريدًا للمجموعة.
- **الوصف** – ادخل وصفا للمجموعة لتوفير مزيد من المعلومات حول كيفيه استخدامه.

### <a name="manage-customer-group-assignments"></a>إدارة تعيينات مجموعات العملاء

يمكن ان ينتمي كل عميل إلى اي عدد من مجموعات أداره الخصم. لعرض أعضاء المجموعة وتعيينهم، يمكنك البدء اما من قائمه المجموعات أو من قائمه العملاء.

لعرض العملاء لمجموعه محدده أو اضافتهم أو ازالتهم، اتبع الخطوات التالية.

1. انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات العملاء**.
1. حدد المجموعة المطلوب إدارتها.
1. في جزء الإجراء، حدد **العملاء**. تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة العملاء الأعضاء بالفعل في المجموعة المحددة.
1. لإضافة عميل جديد إلى المجموعة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة. ثم قم بتعيين الحقل التالي للصف الجديد:

    - **حساب العميل** – حدد معرف حساب العميل.

1. لأزاله عميل من المجموعة، حدد العميل، ثم حدد **حذف** في جزء الإجراءات.

لعرض أو إضافة أو إزالة تعيينات المجموعة لعميل محدد، اتبع هذه الخطوات.

1. انتقل إلى **الحسابات المدينة \> العملاء \> كافة العملاء**.
1. حدد العميل المراد التعامل معه.
1. في جزء الإجراء، في علامة التبويب **العميل**، في مجموعة **إدارة الخصومات**، حدد **مجموعات إدارة الخصومات**. تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة المجموعات التي ينتمي إليها العميل المحدد بالفعل.
1. لإضافة العميل إلى مجموعة جديدة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة. ثم قم بتعيين الحقل التالي للصف الجديد:

    - **مجموعه إدارة الخصومات** - حدد المجموعة التي سيتم أضافه العميل اليها.

1. لإزالة عميل من مجموعة، حدد المجموعة، ثم حدد **حذف** في جزء الإجراء.

## <a name="rebate-management-vendor-groups"></a>مجموعات موردين إدارة الخصومات

عاده ما يتم إنشاء حساب لمجموعه من الموردين لمجموعه من نقاط التسليم. عاده ما يرتبط هذا النوع من الحساب بالخصم.

### <a name="set-up-vendor-groups"></a>إعداد مجموعات الموردين

للعمل مع مجموعات موردين إدارة الخصم، انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات\> مجموعات الموردين**. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة المجموعات وإزالتها كما هو مطلوب. بالنسبة لكل مجموعة، قم بتعيين الحقول التالية:

- **مجموعة إدارة الخصومات** – أدخل اسمًا فريدًا للمجموعة.
- **الوصف** – ادخل وصفا للمجموعة لتوفير مزيد من المعلومات حول كيفيه استخدامه.

### <a name="manage-vendor-group-assignments"></a>إدارة تعيينات مجموعات الموردين

يمكن ان ينتمي كل مورد إلى اي عدد من مجموعات أداره الخصم. لعرض أعضاء المجموعة وتعيينهم، يمكنك البدء اما من قائمه المجموعات أو من قائمه الموردين.

لعرض الموردين لمجموعه محدده أو اضافتهم أو ازالتهم، اتبع الخطوات التالية.

1. انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات الموردين**.
1. حدد المجموعة المطلوب إدارتها.
1. في جزء الإجراءات، حدد **المورّدين**. تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة الموردين الأعضاء بالفعل في المجموعة المحددة.
1. لإضافة مورد جديد إلى المجموعة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة. ثم قم بتعيين الحقل التالي للصف الجديد:

    - **حساب المورد** – حدد معرف حساب المورد.

1. لأزاله مورد من المجموعة، حدد المورد، ثم حدد **حذف** في جزء الإجراءات.

لعرض أو إضافة أو إزالة تعيينات المجموعة لمورد محدد، اتبع هذه الخطوات.

1. انتقل إلى **الحسابات الدائنة \> الموردين \> جميع الموردين**.
1. حدد المورد المراد التعامل معه.
1. في جزء الإجراء، في علامة التبويب **المورد**، في مجموعة **إدارة الخصومات**، حدد **مجموعات إدارة الخصومات**. تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة المجموعات التي ينتمي إليها المورد المحدد بالفعل.
1. لإضافة المورد إلى مجموعة جديدة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة. ثم قم بتعيين الحقل التالي للصف الجديد:

    - **مجموعه إدارة الخصومات** - حدد المجموعة التي سيتم أضافه المورد اليها.

1. لإزالة مورد من مجموعة، حدد المجموعة، ثم حدد **حذف** في جزء الإجراء.

## <a name="item-rebate-groups"></a>مجموعات الخصم للصنف

من خلال تجميع الأصناف، يكون لديك المزيد من المرونة عند حساب التخفيضات والخصومات. غالبًا ما يكون هذا النهج طريقة أكثر فاعلية لإعداد التخفيضات والخصومات للعملاء والموردين.

### <a name="set-up-item-groups"></a>إعداد مجموعات الأصناف

للعمل مع مجموعات أصناف إدارة الخصم، انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات\> مجموعات الأصناف**. يمكنك استخدام الأزرار الموجودة في جزء الإجراءات لإضافة المجموعات وإزالتها كما هو مطلوب. بالنسبة لكل مجموعة، قم بتعيين الحقول التالية:

- **مجموعة إدارة الخصومات** – أدخل اسمًا فريدًا للمجموعة.
- **الوصف** – ادخل وصفا للمجموعة لتوفير مزيد من المعلومات حول كيفيه استخدامه.

### <a name="manage-item-group-assignments"></a>إدارة تعيينات مجموعات الأصناف

يمكن ان ينتمي كل صنف إلى اي عدد من مجموعات أداره الخصم. لعرض أعضاء المجموعة وتعيينهم، يمكنك البدء اما من قائمه المجموعات أو من قائمه الأصناف. يمكنك أيضا أضافه أصناف استنادا إلى التدرج الهرمي للفئات الخاص بك.

لعرض الأصناف أو إضافتها أو إزالتها لمجموعة محددة، اتبع هذه الخطوات.

1. انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات الأصناف**.
1. حدد المجموعة المطلوب إدارتها.
1. في جزء الإجراءات، حدد **الأصناف**. تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة الأصناف الأعضاء بالفعل في المجموعة المحددة.
1. لإضافة صنف جديدة إلى المجموعة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة. ثم قم بتعيين الحقل التالي للصف الجديد:

    - **حساب الصنف** – حدد معرف حساب الصنف.

1. لأزاله صنف من المجموعة، حدد الصنف، ثم حدد **حذف** في جزء الإجراءات.

لعرض أو إضافة أو إزالة تعيينات المجموعة لصنف محدد، اتبع هذه الخطوات.

1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.
1. حدد الصنف المراد التعامل معه.
1. في جزء الإجراء، في علامة التبويب **المنتج**، في مجموعة **إدارة الخصومات**، حدد **مجموعات إدارة الخصومات**. تظهر صفحة **مجموعة إدارة الخصومات** وتعرض قائمة المجموعات التي ينتمي إليها الصنف المحدد بالفعل.
1. لإضافة الصنف إلى مجموعة جديدة، حدد **جديد** في جزء الإجراءات لإضافة صف إلى الشبكة. ثم قم بتعيين الحقل التالي للصف الجديد:

    - **مجموعه إدارة الخصومات** - حدد المجموعة التي سيتم أضافه الصنف اليها.

1. لأزاله صنف من مجموعة، حدد المجموعة، ثم حدد **حذف** في جزء الإجراءات.

لإضافة أصناف إلى مجموعة بناءً على التسلسل الهرمي للفئات، اتبع هذه الخطوات.

1. انتقل إلى **إدارة الخصومات \> إعداد مجموعات إدارة الخصومات \> مجموعات الأصناف**.
1. حدد المجموعة المطلوب إدارتها.
1. في جزء الإجراءات، حدد **إضافة أصناف**.
1. في مربع الحوار **إضافة أصناف**، في حقل **التدرج الهرمي للفئات**، حدد فئة المستوى الأعلى.
1. يتم فتح التدرج الهرمي للأصناف في الجزء الأيمن. حدد مستوي التدرج الهرمي الذي تقوم بالبحث عنه. 
1. يتم الآن ادراج أصناف من التدرج الهرمي المحدد ومستوي التدرج الهرمي في الجزء الأيسر. اتبع هذه الخطوات للعمل مع الجزء:

    - حدد خانة الاختيار لكل صنف تريد إضافته.
    - حدد خانه الاختيار في راس الشبكة لتحديد كافة الأصناف المدرجة.
    - حدد الزر **إظهار المحدد** لتصفيه الشبكة بحيث تظهر فقط الأصناف التي قمت بتحديدها حتى الآن. حدد الزر مره أخرى للرجوع إلى القائمة بأكملها.

1. حدد **موافق** لتطبيق تحديد الصنف علي المجموعة المحددة.
