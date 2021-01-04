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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="e87ce-103">تصفية أوامر الشركات الشقيقة لتجنب مزامنة الأوامر وبنود الأوامر</span><span class="sxs-lookup"><span data-stu-id="e87ce-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e87ce-104">يمكنك تصفية أوامر الشركات الشقيقة لتجنب مزامنة كياني **الأوامر** و **بنود الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="e87ce-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="e87ce-105">في بعض السيناريوهات ، لا تكون تفاصيل الطلب بين الشركات الشقيقة ضرورية في تطبيق Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="e87ce-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="e87ce-106">يتم توسيع كل كيان من كيانات Common Data Service القياسية بمراجع إلى حقل **IntercompanyOrder**، ويتم تعديل التعيينات ثنائيه الكتابة للاشاره إلى الحقول الاضافيه في عوامل التصفية.</span><span class="sxs-lookup"><span data-stu-id="e87ce-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="e87ce-107">وتكون النتيجة هي عدم مزامنة الأوامر بين الشركات الشقيقة بعد ذلك.</span><span class="sxs-lookup"><span data-stu-id="e87ce-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="e87ce-108">يتجنب هذا الاجراء البيانات غير الضرورية في تطبيق Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="e87ce-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="e87ce-109">أضف مرجعًا إلى **IntercompanyOrder** إلى **رؤوس أوامر المبيعات CDS‬**.</span><span class="sxs-lookup"><span data-stu-id="e87ce-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="e87ce-110">ويتم ملؤها في الأوامر بين الشركات الشقيقة فقط.</span><span class="sxs-lookup"><span data-stu-id="e87ce-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="e87ce-111">حقل **IntercompanyOrder** متوفر في **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="e87ce-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="تعيين التقسيم المرحلي للاستهداف، SalesOrderHeader":::
    
2. <span data-ttu-id="e87ce-113">بعد توسيع **رؤوس أوامر المبيعات CDS‬**، يتوفر حقل **IntercompanyOrder** في التعيين.</span><span class="sxs-lookup"><span data-stu-id="e87ce-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="e87ce-114">استخدم عامل تصفية `INTERCOMPANYORDER == ""` باعتباره سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="e87ce-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="رؤوس أوامر المبيعات، تحرير الاستعلام":::

3. <span data-ttu-id="e87ce-116">أضف مرجعًا إلى **IntercompanyInventTransId** إلى **‏‫بنود أمر مبيعات CDS‬**.</span><span class="sxs-lookup"><span data-stu-id="e87ce-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="e87ce-117">ويتم ملؤها في الأوامر بين الشركات الشقيقة فقط.</span><span class="sxs-lookup"><span data-stu-id="e87ce-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="e87ce-118">حقل **InterCompanyInventTransID** متوفر في **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="e87ce-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="تعيين التقسيم المرحلي للاستهداف، SalesOrderLine":::

4. <span data-ttu-id="e87ce-120">بعد توسيع **بنود أوامر مبيعات CDS‬**، يتوفر حقل **IntercompanyInventTransId** في التعيين.</span><span class="sxs-lookup"><span data-stu-id="e87ce-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="e87ce-121">استخدم عامل تصفية `INTERCOMPANYINVENTTRANSID == ""` باعتباره سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="e87ce-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="بنود أوامر المبيعات، تحرير الاستعلام":::

5. <span data-ttu-id="e87ce-123">قم بتوسيع **رأس فاتورة المبيعات V2‬** و **بنود فواتير المبيعات V2** بنفس الطريقة التي قمت بها بتوسيع كيانات Common Data Service في الكيانين 1 و2.</span><span class="sxs-lookup"><span data-stu-id="e87ce-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="e87ce-124">أضف بعد ذلك استعلامات التصفية.</span><span class="sxs-lookup"><span data-stu-id="e87ce-124">Then add the filter queries.</span></span> <span data-ttu-id="e87ce-125">سلسلة عامل التصفية لـ **رأس فاتورة المبيعات V2** هي `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="e87ce-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="e87ce-126">سلسلة عامل التصفية لـ **بنود فواتير المبيعات V2** هي `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="e87ce-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="تعيين التقسيم المرحلي للاستهداف، رؤوس فواتير المبيعات":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="رؤوس فواتير المبيعات، تحرير الاستعلام":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="بنود فواتير المبيعات، تحرير الاستعلام":::

6. <span data-ttu-id="e87ce-130">لا يشتمل كيان **عروض الأسعار** على علاقة بين الشركات الشقيقة.</span><span class="sxs-lookup"><span data-stu-id="e87ce-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="e87ce-131">إذا قام شخص ما بإنشاء عرض أسعار لأحد العملاء بين الشركات الشقيقة الخاصة بك، فيمكنك وضع كافة هؤلاء العملاء في مجموعة عملاء واحدة باستخدام حقل **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="e87ce-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="e87ce-132">يمكن توسيع الرأس والبنود لإضافة حقل **CustGroup** ثم التصفية لاستبعاد هذه المجموعة.</span><span class="sxs-lookup"><span data-stu-id="e87ce-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="تعيين التقسيم المرحلي للاستهداف، رأس عرض أسعار المبيعات":::

7. <span data-ttu-id="e87ce-134">بعد قيامك بتوسيع كيان **عروض الأسعار**، قم بتطبيق عامل تصفية باستخدام `CUSTGROUP !=  "<company>"` باعتباره سلسلة الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="e87ce-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="رأس عرض أسعار المبيعات، تحرير الاستعلام":::
