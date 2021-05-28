---
title: إعداد أكواد ضريبة الخصم لنوع ضريبة TDS
description: يوضح هذا الموضوع كيفية إعداد أكواد الضريبة المخصومة في المصدر (TDS).
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023010"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>إعداد أكواد ضريبة الخصم لنوع ضريبة TDS

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية إعداد أكواد الضريبة المخصومة في المصدر (TDS).

1. انتقل إلى **الضريبة \> الضرائب غير مباشرة \> ضريبة الخصم \> أكواد ضريبة الخصم**.

    [![صفحة أكواد ضريبة الخصم](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. في جزء الإجراء، حدد **جديد** لإنشاء كود ضريبة خصم لـ TDS، وأدخل التفاصيل المطلوبة.
3. في علامة التبويب السريعة **عام**، في الحقل **نوع الضريبة**، حدد **TDS** لتصنيف كود الضريبة ككود ضريبة TDS.
4. في الحقل **فترة التسوية**، حدد فترة تسوية TDS لكود ضريبة TDS.
5. في الحقل **الحساب الرئيسي**، حدد حساب دفتر الأستاذ الذي يجب ترحيل مبلغ TDS إليه.
6. في الحقل **الحساب المدين**، حدد الحساب المدينة الذي يجب ترحيل مبلغ TDS الذي تم خصمه من حركات المبيعات إليه.

    يتم تعيين الحقل **الأصل** تلقائيًا على **النسبة المئوية للمبلغ الإجمالي**، ولا يمكن تغيير القيمة.

    > [!NOTE]
    > لا يمكنك تعيين الأصل إلى **النسبة المئوية للمبلغ الصافي** لأكواد الضريبة الخاصة بنوع ضريبة TDS.

7. في الحقل **مكون ضريبة الخصم**، حدد مجموعة مكون ضريبة TDS لكود صريبة TDS إليها.
8. في جزء الإجراء، حدد **القيم** لفتح الصفحة **قيم ضريبة الخصم**.
9. حدد الحقل **من تاريخ**، أدخل تاريخ البداية لقيمة TDS. في الحقل **إلى التاريخ**، أدخل تاريخ الانتهاء.

    > [!NOTE]
    > لا تتوفر الحقول **الحد الأدنى** و **الحد الأعلى** و **استبعاد %** لأكواد الضريبة الخاصة بنوع الضريبة TDS.

10. في الحقل **القيمة**، أدخل النسبة لـ TDS لاحتساب ضريبة الخصم.
11. قم بإغلاق الصفحة **قيم ضريبة الخصم** للرجوع إلى الصفحة **أكواد ضريبة الخصم**.

    > [!NOTE]
    > لا يتوافر الزر **الحدود** الموجود على الصفحة **أكواد ضريبة الخصم** لأكواد الضريبة الخاصة بنوع الضريبة TDS.

12. قم بإغلاق الصفحة.