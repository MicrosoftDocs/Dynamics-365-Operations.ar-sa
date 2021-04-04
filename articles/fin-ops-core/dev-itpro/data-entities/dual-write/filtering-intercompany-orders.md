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
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="5a27c-103">تصفية أوامر الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر</span><span class="sxs-lookup"><span data-stu-id="5a27c-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a27c-104">يمكنك تصفية أوامر الشركات الشقيقة لتجنب مزامنة كياني **الأوامر** و **بنود الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="5a27c-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="5a27c-105">في بعض السيناريوهات ، لا تكون تفاصيل الطلب بين الشركات الشقيقة ضرورية في تطبيق Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="5a27c-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="5a27c-106">يتم توسيع كل جدول من جداول Dataverse القياسية بمراجع إلى عمود **IntercompanyOrder**، ويتم تعديل التعيينات ثنائيه الكتابة للاشاره إلى الحقول الاضافيه في عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="5a27c-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="5a27c-107">ولذلك، لا تتم مزامنة الأوامر بين الشركات الشقيقة بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="5a27c-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="5a27c-108">يتجنب هذا الاجراء البيانات غير الضرورية في تطبيق Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="5a27c-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="5a27c-109">توسيع جدول **رؤوس أوامر التوريد CDS** عن طريق أضافه مرجع إلى العمود **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="5a27c-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="5a27c-110">يتم ملء هذا العمود فقط في الأوامر بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="5a27c-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="5a27c-111">عمود **IntercompanyOrder** متوفر في جدول **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="5a27c-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لـ CDS التي تكون رؤوس أوامر التوريد":::

2. <span data-ttu-id="5a27c-113">بعد توسيع **رؤوس أوامر المبيعات CDS‬**، يتوفر عمود **IntercompanyOrder** في التعيين.</span><span class="sxs-lookup"><span data-stu-id="5a27c-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="5a27c-114">استخدم عامل تصفية `INTERCOMPANYORDER == ""` باعتباره سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="5a27c-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="مربع الحوار تحرير الاستعلام لـ CDS لرؤوس أوامر التوريد":::

3. <span data-ttu-id="5a27c-116">توسيع جدول **بنود أوامر التوريد CDS** عن طريق أضافه مرجع إلى العمود **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="5a27c-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="5a27c-117">يتم ملء هذا العمود فقط في الأوامر بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="5a27c-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="5a27c-118">عمود **InterCompanyInventTransId** متوفر في جدول **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="5a27c-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لبنود أوامر مبيعات CDS":::

4. <span data-ttu-id="5a27c-120">بعد توسيع **بنود أوامر مبيعات CDS‬**، يتوفر عمود **IntercompanyInventTransId** في التعيين.</span><span class="sxs-lookup"><span data-stu-id="5a27c-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="5a27c-121">استخدم عامل تصفية `INTERCOMPANYINVENTTRANSID == ""` باعتباره سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="5a27c-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="مربع الحوار تحرير الاستعلام لبنود أوامر مبيعات CDS":::

5. <span data-ttu-id="5a27c-123">كرر الخطوتين 1 و2 لتوسيع جدول **راس فاتورة المبيعات V2** وأضافه استعلام تصفيه.</span><span class="sxs-lookup"><span data-stu-id="5a27c-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="5a27c-124">في هذه الحالة، استخدم `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` كسلسلة استعلام لعامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="5a27c-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لرأس فاتورة المبيعات V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="مربع الحوار تحرير الاستعلام لرأس فاتورة المبيعات V2":::

6. <span data-ttu-id="5a27c-127">كرر الخطوتين 3 و2 لتوسيع جدول **بنود فاتورة المبيعات V2** وأضافه استعلام تصفيه.</span><span class="sxs-lookup"><span data-stu-id="5a27c-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="5a27c-128">في هذه الحالة، استخدم `INTERCOMPANYINVENTTRANSID == ""` كسلسلة استعلام لعامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="5a27c-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="مربع الحوار تحرير الاستعلام لبنود فاتورة المبيعات V2":::

7. <span data-ttu-id="5a27c-130">لا يشتمل جدول **عروض الأسعار** على علاقة بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="5a27c-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="5a27c-131">إذا قام شخص ما بإنشاء عرض أسعار لأحد العملاء بين الشركات الشقيقة الخاصة بك، فيمكنك وضع كافة هؤلاء العملاء في مجموعة عملاء واحدة باستخدام حقل **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="5a27c-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="5a27c-132">يمكنك توسيع الراس والخطوط عن طريق أضافه العمود **CustGroup**، ثم التصفية بحيث لا يتم تضمين المجموعة.</span><span class="sxs-lookup"><span data-stu-id="5a27c-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="تعيين الاعداد المرحلي للصفحة الهدف لرأس عرض أسعار مبيعات CDS":::

8. <span data-ttu-id="5a27c-134">بعد قيامك بتوسيع **عروض الأسعار**، قم بتطبيق عامل تصفية باستخدام `CUSTGROUP != "<company>"` باعتباره سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="5a27c-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="مربع الحوار تحرير الاستعلام لرأس عروض أسعار المبيعات CDS":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]