---
title: أسعار مبيعات الاشتراكات
description: عند إنشاء اشتراك، فإن سعر المبيعات يكون مشتقًا من إعداد سعر المبيعات الذي تم إنشاؤه في النموذج سعر المبيعات (اشتراك).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974200"
---
# <a name="subscription-sales-prices"></a>أسعار مبيعات الاشتراكات   

[!include [banner](../includes/banner.md)]


عند إنشاء اشتراك، فإن سعر المبيعات يكون مشتقًا من إعداد سعر المبيعات الذي تم إنشاؤه في النموذج **سعر المبيعات (اشتراك)**.

في النموذج **سعر المبيعا (اشتراك)**، يمكن إنشاء أسعار مبيعات لاشتراك محدد لو يمكنك إنشاء أسعار مبيعات يتم تطبيقها بشكل أوسع. بالنسبة لسعر مبيعات المراد تطبيقه على اشتراك ما، فإنه يجب أن يكون كل من كود الفترة وعملة الاشتراك مماثلا لكود الفترة والعملة لسعر المبيعات.

إذا كان كل من كود الفترة والعملة متماثلين مع الاشتراك وسعر المبيعات، فإنه يتم تحديد أسعار مبيعات الاشتراك بناءً على قواعد الأولويات الموضحة في الجدول التالي. تشير الخليفة الفارغة في الجدول إلى وجود حقل فارغ وتوضح علامة X قيمة مساوية للقيمة الموجودة في الاشتراك الذي يتم إنشاء الحركة منه.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>الأولوية </p></th>
<th><p><strong>الفئة</strong></p></th>
<th><p><strong>معرف المشروع</strong></p></th>
<th><p><strong>الاشتراك</strong></p></th>
<th><p><strong>عملة المبيعات</strong></p></th>
<th><p><strong>كود الفترة</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>س</p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>س</p></td>
<td><p>س</p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>س</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>س</p></td>
<td><p>س</p></td>
</tr>
</tbody>
</table>


عند إنشاء رسم اشتراك، فإن سعر المبيعات المحتوي على أعلى مستوى من التفاصيل، مثلما هو ملاحظ في الجدول أعلاه، هو الذي يتم تحديده كسعر مبيعات الاشتراك.

## <a name="update-and-index-subscription-sales-prices"></a>تحديث أسعار مبيعات الاشتراك وفهرستها

يمكن تحديث سعر مبيعات الاشتراك عن طريق تحديث السعر الأساسي أو الفهرس. يمكن التحديث باستخدام نسبة مئوية أو إلى قيمة جديدة.

## <a name="subscription-fee-sales-prices"></a>أسعار مبيعات رسم الاشتراك

عند إنشاء رسم اشتراك، فإن سعر المبيعات يعتمد على إعداد سعر المبيعات الخاص بالاشتراك. من الممكن استخدام السعر الأساسي من إعداد سعر الاشتراك أو إنشاء أسعار مبيعات مفهرسة.

## <a name="example"></a>مثال

ترغب في إعداد أسعار مبيعات اشتراك بمبلغ 500 ريال سعودي لمشروع جديد 9030. في النموذج **سعر المبيعات (الاشتراك)**، عليك إنشاء بند سعر مبيعات اشتراك كما هو موضح في الجدول التالي.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>صالح من</p></th>
<th><p>الفئة</p></th>
<th><p>Project</p></th>
<th><p>الاشتراك</p></th>
<th><p>كود الفترة</p></th>
<th><p>عملة المبيعات</p></th>
<th><p>سعر المبيعات</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>الشهر</p></td>
<td><p>يورو</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


لاحظ أن حقلي **الفئة** و **الاشتراك** فارغين.

عليك بعد ذلك إنشاء الاشتراكات التالية:

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>اشتراك في الخدمة</p></th>
<th><p>Project</p></th>
<th><p>مجموعة المشتركين</p></th>
<th><p>الفئة</p></th>
<th><p>العملة</p></th>
<th><p>كود الفترة</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>الاشتراك 1</p></td>
<td><p>فئة الاشتراك 1</p></td>
<td><p>ريال سعودي</p></td>
<td><p>شهري</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>الاشتراك 1</p></td>
<td><p>SubCat2</p></td>
<td><p>ريال سعودي</p></td>
<td><p>شهري</p></td>
</tr>
</tbody>
</table>


قم الآن بإنشاء رسوم اشتراك للاشتراكين الموجودين في مجموعة الاشتراك Sub1:

1.  انقر فوق **إدارة الخدمة** \> **إعداد** \> **اشتراكات الخدمة** \> **مجموعات الاشتراك**.

2.  في نموذج **مجموعات المشتركين**، انقر فوق **الوظيفة** \> **إنشاء رسوم اشتراك**.

3.  في نموذج **إنشاء رسوم اشتراك**، أدخل المعلومات المناسبة. لمزيد من المعلومات، راجع [إنشاء حركات رسوم الاشتراك](create-subscription-fee-transactions.md).

يتم إنشاء رسوم الاشتراك التي تحتوي على سعر مبيعات 500 يورو للاشتراكات، كما هو موضح في الجدول التالي.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>تاريخ المشروع</p></th>
<th><p>اشتراك في الخدمة</p></th>
<th><p>Project</p></th>
<th><p>الفئة</p></th>
<th><p>تاريخ البدء</p></th>
<th><p>تاريخ الانتهاء</p></th>
<th><p>عملة المبيعات</p></th>
<th><p>سعر المبيعات</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>فئة الاشتراك 1</p></td>
<td><p>01-012007-</p></td>
<td><p>31-03-2007</p></td>
<td><p>ريال سعودي</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01-012007-</p></td>
<td><p>31-03-2007</p></td>
<td><p>ريال سعودي</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


قرر بعد ذلك أنك ترغب في تحديد أسعار مبيعات للفئة SubCat1 في المشروع 9030. وبالتالي يمكنك إنشاء بند سعر مبيعات جديد بقيمة 550 يورو للمجموعة المؤلفة من المشروع 9030 وفئة الرسوم SubCat1. يوجد الآن بندان جديدان لسعر مبيعات الاشتراك للمشروع 9030، كما هو موضح في الجدول التالي.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>صالح من</p></th>
<th><p>الفئة</p></th>
<th><p>Project</p></th>
<th><p>الاشتراك</p></th>
<th><p>كود الفترة</p></th>
<th><p>العملة</p></th>
<th><p>سعر المبيعات</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>شهر</p></td>
<td><p>ريال سعودي</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2007</p></td>
<td><p>فئة الاشتراك 1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>شهر</p></td>
<td><p>ريال سعودي</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


كرر الإجراء الموضح أعلاه لإنشاء رسوم اشتراك للاشتراكين الموجودين في مجموعة الاشتراك Sub1. يوضح الجدول التالي الحركات التي تم إنشائها لكل اشتراك ويتم إرفاق كل منها بمجموعة الاشتراك.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>تاريخ المشروع</p></th>
<th><p>الاشتراك</p></th>
<th><p>Project</p></th>
<th><p>الفئة</p></th>
<th><p>تاريخ البدء</p></th>
<th><p>تاريخ الإنهاء</p></th>
<th><p>عملة المبيعات</p></th>
<th><p>سعر المبيعات</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>فئة الاشتراك 1</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>ريال سعودي</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>يورو</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


في الحركة الأولى للاشتراك 00020\_135 يُشتق سعر المبيعات بقيمة 550 يورو من سعر مبيعات الاشتراك الذي تم إعداده لمجموعة معينة من المشروع والفئة. في الحركة الثانية للاشتراك 00021\_135 سعر المبيعات بقيمة 500 يورو يستخدم كسعر مبيعات الاشتراك للمشروع وذلك لعدم وجود أي سعر تم إعداده لمجموعة المشروع 9030 والفئة SubCat2.

## <a name="see-also"></a>راجع أيضًا

[تحديث أسعار مبيعات الاشتراك وفهرستها](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]