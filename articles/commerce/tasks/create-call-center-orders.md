---
title: " إنشاء أوامر مركز الاتصال"
description: يتناول هذا الإجراء البحث عن عميل وإنشاء أمر جديد والبحث عن منتج وتحصيل المدفوعات من العميل.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dce2fdd9d91c2bd867f0455573733aefb0796fa7
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107342"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="4ac52-103"> إنشاء أوامر مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="4ac52-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ac52-104">يتناول هذا الإجراء البحث عن عميل وإنشاء أمر جديد والبحث عن منتج وتحصيل المدفوعات من العميل.</span><span class="sxs-lookup"><span data-stu-id="4ac52-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="4ac52-105">يستخدم هذا الإجراء شركة بيانات الشركة العرض التوضيحي USRT وهو مخصص لموظف "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="4ac52-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="4ac52-106">الشروط المسبقة: يتم إعداد المستخدم الذي يكمل الإجراء كمستخدم مركز اتصال ويتم نشر الكتالوج النصف سنوي لشركة Fabrikam بكود مصدر واحد على الأقل به.</span><span class="sxs-lookup"><span data-stu-id="4ac52-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="4ac52-107">انتقل إلى **البيع بالتجزئة والتجارة \> العملاء \> خدمة العملاء**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="4ac52-108">بالنسبة لـ **SearchText** ، أدخل معايير البحث للبحث عن العميل.</span><span class="sxs-lookup"><span data-stu-id="4ac52-108">For **SearchText** , enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="4ac52-109">بالنسبة لهذا الإجراء في المثال، اكتب "كارين" وحدد **Tab**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="4ac52-110">حدد بحث.</span><span class="sxs-lookup"><span data-stu-id="4ac52-110">Select Search.</span></span>
    * <span data-ttu-id="4ac52-111">لأن هناك عميل واحد فقط يسمى "كارين" في بيانات العرض التوضيحي، فسيتم تحديد النتيجة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="4ac52-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="4ac52-112">حدد **أمر مبيعات جديد**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="4ac52-113">‏‫قم بتوسيع قسم "‏رأس **أمر المبيعات** أو طيه.</span><span class="sxs-lookup"><span data-stu-id="4ac52-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="4ac52-114">حدد كود المصدر للكتالوج.</span><span class="sxs-lookup"><span data-stu-id="4ac52-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="4ac52-115">إذا لم تكن هناك أكواد مصدر نشطة، فيمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="4ac52-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="4ac52-116">حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-116">Select **Add line**.</span></span>
8. <span data-ttu-id="4ac52-117">بالنسبة لـ **رقم الصنف** ، أدخل مصطلح البحث عن صنف.</span><span class="sxs-lookup"><span data-stu-id="4ac52-117">For **Item number** , enter the item search term.</span></span>
    * <span data-ttu-id="4ac52-118">بالنسبة لهذا الإجراء في المثال، أدخل رقم صنف جزئيًا "8111" واضغط على المفتاح Tab. وهذا الإجراء سيعمل على إظهار نافذة البحث عن الصنف.</span><span class="sxs-lookup"><span data-stu-id="4ac52-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="4ac52-119">حدد المنتج لإضافته إلى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="4ac52-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="4ac52-120">أدخل كمية المبيعات.</span><span class="sxs-lookup"><span data-stu-id="4ac52-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="4ac52-121">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-121">Select **Create**.</span></span>
12. <span data-ttu-id="4ac52-122">حدد **إكمال** لتسجيل دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="4ac52-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="4ac52-123">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-123">Select **Add**.</span></span>
    * <span data-ttu-id="4ac52-124">يوجد "إضافة ارتباط" في علامة التبويب "المدفوعات". قم بتوسيع علامة التبويب "المدفوعات" إذا كانت مطوية.</span><span class="sxs-lookup"><span data-stu-id="4ac52-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="4ac52-125">حدد طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="4ac52-125">Select the payment method.</span></span>
    * <span data-ttu-id="4ac52-126">لتنفيذ هذا الإجراء، حدد طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="4ac52-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="4ac52-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4ac52-127">Close the page.</span></span>
16. <span data-ttu-id="4ac52-128">أدخل المبلغ.</span><span class="sxs-lookup"><span data-stu-id="4ac52-128">Enter the amount.</span></span>
    * <span data-ttu-id="4ac52-129">لتنفيذ هذا الإجراء، أدخل مبلغًا يساوي موازنة الأمر والذي يمكن رؤيته في صفحة ملخص أمر المبيعات إلى يسار حقل "المبلغ".</span><span class="sxs-lookup"><span data-stu-id="4ac52-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="4ac52-130">سيسمح لك هذا الإجراء باستكمال الأمر كأنه مدفوع بالكامل.</span><span class="sxs-lookup"><span data-stu-id="4ac52-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="4ac52-131">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-131">Select **OK**.</span></span>
18. <span data-ttu-id="4ac52-132">حدد **إرسال**.</span><span class="sxs-lookup"><span data-stu-id="4ac52-132">Select **Submit**.</span></span>

