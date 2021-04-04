---
title: تصفية أوامر الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر
description: يوضح هذا الموضوع كيفيه تصفيه الأوامر بين الشركات الشقيقة بحيث لا تتم مزامنة الأوامر والكيانات الأورديرلينيسه.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 9a736c8e93dfa7dbcd0739b52e2da987dcefdc0e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568092"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>تصفية أوامر الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر

[!include [banner](../../includes/banner.md)]

يمكنك تصفية أوامر الشركات الشقيقة لتجنب مزامنة كياني **الأوامر** و **بنود الأوامر**. في بعض السيناريوهات ، لا تكون تفاصيل الطلب بين الشركات الشقيقة ضرورية في تطبيق Customer Engagement.

يتم توسيع كل جدول من جداول Dataverse القياسية بمراجع إلى عمود **IntercompanyOrder**، ويتم تعديل التعيينات ثنائيه الكتابة للاشاره إلى الحقول الاضافيه في عوامل التصفية. ولذلك، لا تتم مزامنة الأوامر بين الشركات الشقيقة بعد ذلك. يتجنب هذا الاجراء البيانات غير الضرورية في تطبيق Customer Engagement.

1. توسيع جدول **رؤوس أوامر التوريد CDS** عن طريق أضافه مرجع إلى العمود **IntercompanyOrder**. يتم ملء هذا العمود فقط في الأوامر بين الشركات الشقيقة. عمود **IntercompanyOrder** متوفر في جدول **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لـ CDS التي تكون رؤوس أوامر التوريد":::

2. بعد توسيع **رؤوس أوامر المبيعات CDS‬**، يتوفر عمود **IntercompanyOrder** في التعيين. استخدم عامل تصفية `INTERCOMPANYORDER == ""` باعتباره سلسلة الاستعلام.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="مربع الحوار تحرير الاستعلام لـ CDS لرؤوس أوامر التوريد":::

3. توسيع جدول **بنود أوامر التوريد CDS** عن طريق أضافه مرجع إلى العمود **IntercompanyInventTransId**. يتم ملء هذا العمود فقط في الأوامر بين الشركات الشقيقة. عمود **InterCompanyInventTransId** متوفر في جدول **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لبنود أوامر مبيعات CDS":::

4. بعد توسيع **بنود أوامر مبيعات CDS‬**، يتوفر عمود **IntercompanyInventTransId** في التعيين. استخدم عامل تصفية `INTERCOMPANYINVENTTRANSID == ""` باعتباره سلسلة الاستعلام.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="مربع الحوار تحرير الاستعلام لبنود أوامر مبيعات CDS":::

5. كرر الخطوتين 1 و2 لتوسيع جدول **راس فاتورة المبيعات V2** وأضافه استعلام تصفيه. في هذه الحالة، استخدم `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` كسلسلة استعلام لعامل التصفية.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لرأس فاتورة المبيعات V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="مربع الحوار تحرير الاستعلام لرأس فاتورة المبيعات V2":::

6. كرر الخطوتين 3 و2 لتوسيع جدول **بنود فاتورة المبيعات V2** وأضافه استعلام تصفيه. في هذه الحالة، استخدم `INTERCOMPANYINVENTTRANSID == ""` كسلسلة استعلام لعامل التصفية.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="مربع الحوار تحرير الاستعلام لبنود فاتورة المبيعات V2":::

7. لا يشتمل جدول **عروض الأسعار** على علاقة بين الشركات الشقيقة. إذا قام شخص ما بإنشاء عرض أسعار لأحد العملاء بين الشركات الشقيقة الخاصة بك، فيمكنك وضع كافة هؤلاء العملاء في مجموعة عملاء واحدة باستخدام حقل **CustGroup**. يمكنك توسيع الراس والخطوط عن طريق أضافه العمود **CustGroup**، ثم التصفية بحيث لا يتم تضمين المجموعة.

    :::image type="content" source="media/filter-cust-group.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لرأس عرض أسعار مبيعات CDS":::

8. بعد قيامك بتوسيع **عروض الأسعار**، قم بتطبيق عامل تصفية باستخدام `CUSTGROUP != "<company>"` باعتباره سلسلة الاستعلام.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="مربع الحوار تحرير الاستعلام لرأس عروض أسعار المبيعات CDS":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]