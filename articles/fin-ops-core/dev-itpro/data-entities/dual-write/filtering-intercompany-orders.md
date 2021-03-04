---
title: تصفية أوامر الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر
description: يصف هذا الموضوع كيفية تصفية الطلبات بين الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701023"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>تصفية أوامر الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر

[!include [banner](../../includes/banner.md)]

يمكنك تصفية أوامر الشركات الشقيقة لتجنب مزامنة كياني **الأوامر** و **بنود الأوامر**. في بعض السيناريوهات ، لا تكون تفاصيل الطلب بين الشركات الشقيقة ضرورية في تطبيق Customer Engagement.

يتم توسيع كل كيان من كيانات Common Data Service القياسية بمراجع إلى حقل **IntercompanyOrder**، ويتم تعديل التعيينات ثنائيه الكتابة للاشاره إلى الحقول الاضافيه في عوامل التصفية. وتكون النتيجة هي عدم مزامنة الأوامر بين الشركات الشقيقة بعد ذلك. يتجنب هذا الاجراء البيانات غير الضرورية في تطبيق Customer Engagement.

1. أضف مرجعًا إلى **IntercompanyOrder** إلى **رؤوس أوامر المبيعات CDS‬**. ويتم ملؤها في الأوامر بين الشركات الشقيقة فقط. حقل **IntercompanyOrder** متوفر في **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="تعيين التقسيم المرحلي للاستهداف، SalesOrderHeader":::
    
2. بعد توسيع **رؤوس أوامر المبيعات CDS‬**، يتوفر حقل **IntercompanyOrder** في التعيين. استخدم عامل تصفية `INTERCOMPANYORDER == ""` باعتباره سلسلة الاستعلام.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="رؤوس أوامر المبيعات، تحرير الاستعلام":::

3. أضف مرجعًا إلى **IntercompanyInventTransId** إلى **‏‫بنود أمر مبيعات CDS‬**.  ويتم ملؤها في الأوامر بين الشركات الشقيقة فقط. حقل **InterCompanyInventTransID** متوفر في **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="تعيين التقسيم المرحلي للاستهداف، SalesOrderLine":::

4. بعد توسيع **بنود أوامر مبيعات CDS‬**، يتوفر حقل **IntercompanyInventTransId** في التعيين. استخدم عامل تصفية `INTERCOMPANYINVENTTRANSID == ""` باعتباره سلسلة الاستعلام.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="بنود أوامر المبيعات، تحرير الاستعلام":::

5. قم بتوسيع **رأس فاتورة المبيعات V2‬** و **بنود فواتير المبيعات V2** بنفس الطريقة التي قمت بها بتوسيع كيانات Common Data Service في الكيانين 1 و2. أضف بعد ذلك استعلامات التصفية. سلسلة عامل التصفية لـ **رأس فاتورة المبيعات V2** هي `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. سلسلة عامل التصفية لـ **بنود فواتير المبيعات V2** هي `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="تعيين التقسيم المرحلي للاستهداف، رؤوس فواتير المبيعات":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="رؤوس فواتير المبيعات، تحرير الاستعلام":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="بنود فواتير المبيعات، تحرير الاستعلام":::

6. لا يشتمل كيان **عروض الأسعار** على علاقة بين الشركات الشقيقة. إذا قام شخص ما بإنشاء عرض أسعار لأحد العملاء بين الشركات الشقيقة الخاصة بك، فيمكنك وضع كافة هؤلاء العملاء في مجموعة عملاء واحدة باستخدام حقل **CustGroup**.  يمكن توسيع الرأس والبنود لإضافة حقل **CustGroup** ثم التصفية لاستبعاد هذه المجموعة.

    :::image type="content" source="media/filter-cust-group.png" alt-text="تعيين التقسيم المرحلي للاستهداف، رأس عرض أسعار المبيعات":::

7. بعد قيامك بتوسيع كيان **عروض الأسعار**، قم بتطبيق عامل تصفية باستخدام `CUSTGROUP !=  "<company>"` باعتباره سلسلة الاستعلام.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="رأس عرض أسعار المبيعات، تحرير الاستعلام":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]