--- 
title: " إنشاء أوامر مركز الاتصال"
description: "يتناول هذا الإجراء البحث عن عميل وإنشاء أمر جديد والبحث عن منتج وتحصيل المدفوعات من العميل."
author: josaw1
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 9280d791c1d846eff2429891c26291ce05d6e6dd
ms.contentlocale: ar-sa
ms.lasthandoff: 09/11/2018

---
# <a name="create-call-center-orders"></a><span data-ttu-id="75298-103"> إنشاء أوامر مركز الاتصال</span><span class="sxs-lookup"><span data-stu-id="75298-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="75298-104">يتناول هذا الإجراء البحث عن عميل وإنشاء أمر جديد والبحث عن منتج وتحصيل المدفوعات من العميل.</span><span class="sxs-lookup"><span data-stu-id="75298-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="75298-105">يستخدم هذا الإجراء شركة بيانات الشركة العرض التوضيحي USRT وهو مخصص لموظف "أمر المبيعات".</span><span class="sxs-lookup"><span data-stu-id="75298-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="75298-106">الشروط المسبقة: يتم إعداد المستخدم الذي يكمل الإجراء كمستخدم مركز اتصال ويتم نشر الكتالوج النصف سنوي لشركة Fabrikam بكود مصدر واحد على الأقل به.</span><span class="sxs-lookup"><span data-stu-id="75298-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="75298-107">انتقل إلى البيع بالتجزئة والتجارة > العملاء > خدمة العملاء.</span><span class="sxs-lookup"><span data-stu-id="75298-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="75298-108">في حقل SearchText، أدخل معايير البحث للبحث عن العميل.</span><span class="sxs-lookup"><span data-stu-id="75298-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="75298-109">لهذا الإجراء المثال، اكتب "كارين" واضغط على مفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="75298-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="75298-110">انقر فوق "بحث".</span><span class="sxs-lookup"><span data-stu-id="75298-110">Click Search.</span></span>
    * <span data-ttu-id="75298-111">لأن هناك عميل واحد فقط يسمى كارين في بيانات العرض التوضيحي، فسيتم تحديده تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="75298-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="75298-112">انقر فوق أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="75298-112">Click New sales order.</span></span>
5. <span data-ttu-id="75298-113">‏‫قم بتوسيع قسم "‏‫رأس أمر المبيعات‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="75298-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="75298-114">حدد كود المصدر للكتالوج.</span><span class="sxs-lookup"><span data-stu-id="75298-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="75298-115">إذا لم تكن هناك أكواد مصدر نشطة، فيمكنك إغلاق حقل المصدر وتخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="75298-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="75298-116">انقر فوق "إضافة بند".</span><span class="sxs-lookup"><span data-stu-id="75298-116">Click Add line.</span></span>
8. <span data-ttu-id="75298-117">في حقل "رقم الصنف"، أدخل مصطلح البحث عن الصنف.</span><span class="sxs-lookup"><span data-stu-id="75298-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="75298-118">لهذا الإجراء المثال، أدخل رقم صنف جزئيًا "8111" واضغط على المفتاح Tab. وهذا سيجعل نافذة البحث عن الصنف تنبثق.</span><span class="sxs-lookup"><span data-stu-id="75298-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="75298-119">حدد المنتج لإضافته إلى أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="75298-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="75298-120">أدخل كمية المبيعات.</span><span class="sxs-lookup"><span data-stu-id="75298-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="75298-121">انقر فوق إنشاء.</span><span class="sxs-lookup"><span data-stu-id="75298-121">Click Create.</span></span>
12. <span data-ttu-id="75298-122">انقر فوق إكمال لتسجيل دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="75298-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="75298-123">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="75298-123">Click Add.</span></span>
    * <span data-ttu-id="75298-124">يوجد "إضافة ارتباط" في علامة التبويب "المدفوعات". قم بتوسيع علامة التبويب "المدفوعات" إذا كانت مطوية.</span><span class="sxs-lookup"><span data-stu-id="75298-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="75298-125">حدد طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="75298-125">Select the payment method.</span></span>
    * <span data-ttu-id="75298-126">لتنفيذ هذا الإجراء، حدد طريقة الدفع النقدي.</span><span class="sxs-lookup"><span data-stu-id="75298-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="75298-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="75298-127">Close the page.</span></span>
16. <span data-ttu-id="75298-128">أدخل المبلغ.</span><span class="sxs-lookup"><span data-stu-id="75298-128">Enter the amount.</span></span>
    * <span data-ttu-id="75298-129">لتنفيذ هذا الإجراء، أدخل مبلغًا يساوي موازنة الأمر والذي يمكن رؤيته في صفحة ملخص أمر المبيعات إلى يسار حقل "المبلغ".</span><span class="sxs-lookup"><span data-stu-id="75298-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="75298-130">وهذا سيسمح لك باستكمال الأمر كأنه مدفوع بالكامل.</span><span class="sxs-lookup"><span data-stu-id="75298-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="75298-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="75298-131">Click OK.</span></span>
18. <span data-ttu-id="75298-132">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="75298-132">Click Submit.</span></span>


