---
title: ضريبة الخصم في حركات المبيعات
description: يسرد هذا الموضوع الخطوات الخاصة بتجنب حساب ضريبة الخصم للعملاء المحددين. بالنسبة للعملاء الذين يحددون ضريبة الخصم في مدفوعاتهم إليك، يمكنك تعيين مجموعة ضريبة الخصم الافتراضية.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060696"
---
# <a name="withholding-tax-in-sales-transactions"></a>ضريبة الخصم في حركات المبيعات

يسرد هذا الموضوع الخطوات الخاصة بتجنب حساب ضريبة الخصم للعملاء المحددين. بالنسبة للعملاء الذين يحددون ضريبة الخصم في مدفوعاتهم إليك، يمكنك تعيين **مجموعة ضريبة الخصم** الافتراضية في صفحة **العملاء**. 

1. انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > العملاء > كافة العملاء**.

2. انقر فوق حساب العميل الخاص، ثم انقر فوق **تحرير**.

3. في علامة التبويب **الفاتورة والتسليم**، قم بتعيين حقل **حساب ضريبة الخصم** إلى **نعم**.

   > [!NOTE] 
   > لن يتم حساب ضريبة الخصم في حالة عدم تبديل **حساب ضريبة الخصم** لهذا العميل في البيانات الرئيسية.

4. حدد مجموعة ضريبة الخصم في **مجموعة ضريبة الخصم**.

5. انقر فوق **حفظ**.

بالنسبة للأصناف/الخدمات، الخاضعة لضريبة الخصم، يمكنك تعيين **مجموعة ضريبة خصم الصنف** الافتراضية في **المنتجات الصادرة**.

1. ‏‫انتقل إلى ‬**جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .

2. انقر فوق رقم الصنف الخاص، ثم انقر فوق **تحرير**.

3. في علامة التبويب **البيع**، انقر فوق **حساب ضريبة الخصم**.

   > [!NOTE] 
   > لن يتم حساب ضريبة الخصم في حالة عدم تعيين **حساب ضريبة الخصم** إلى **نعم** لهذا الصنف في علامة تبويب **البيع** في صفحة **المنتجات الصادرة**.

4. حدد مجموعة ضريبة خصم الصنف في قائمة **مجموعة ضريبة خصم الصنف**.

5. انقر فوق **حفظ**.

يمكن تعيين مجموعات ضريبة الخصم ومجموعات ضريبة خصم الصنف باستخدام صفحة **أمر المبيعات**. 

سيتم استخدام مجموعة ضريبة الخصم الافتراضية ومجموعة ضريبة خصم الصنف كإدخالات افتراضية في بنود أوامر المبيعات عند إنشاء أمر مبيعات جديد.

يتم حساب ضريبة الخصم وترحيلها **بدفتر يومية مدفوعات العميل**. يمكنك تعديل كود ضريبة الخصم القابلة للتطبيق يدويًا بالإضافة إلى مبلغ ضريبة الخصم الفعلية في علامة التبويب **ضريبة الخصم** في صفحة **تسوية الحركات**.

سيتم خصم مبلغ ضريبة الخصم المحتسبة من دفع المورد وترحيله إلى حساب **مقاصة ضريبة الخصم** في إيصال متعلق.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]