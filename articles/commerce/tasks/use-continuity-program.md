---
title: استخدام برامج الاستمرارية
description: يتناول هذا الإجراء بيع برنامج استمرارية ومعالجة أوامر المبيعات ذات الصلة.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd0bfcd99a23e4c639a6317adefb41a947a487a5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021453"
---
# <a name="using-continuity-program"></a><span data-ttu-id="0ebc3-103">استخدام برامج الاستمرارية</span><span class="sxs-lookup"><span data-stu-id="0ebc3-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0ebc3-104">يتناول هذا الإجراء بيع برنامج استمرارية ومعالجة أوامر المبيعات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="0ebc3-105">لإكمال هذا الإجراء، يجب إعداد المستخدم كمستخدم مركز اتصال.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="0ebc3-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="0ebc3-107">انتقل إلى البيع بالتجزئة والتجارة > العملاء > خدمة العملاء.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="0ebc3-108">في حقل "نص البحث"، اكتب "كارين"، ثم اضغط المفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="0ebc3-109">يجب أن ينبثق مربع حوار البحث المتقدم.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="0ebc3-110">إذا لم ينبثق، فانقر فوق "بحث" إلى يسار هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="0ebc3-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0ebc3-112">يجب ظهور صف واحد فقط يعرض كارين بيرغ‬.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="0ebc3-113">حدد الصف بالنقر فوق عمود علامة اختيار في أقصى يمين الشبكة.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="0ebc3-114">انقر فوق تحديد.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-114">Click Select.</span></span>
5. <span data-ttu-id="0ebc3-115">انقر فوق أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-115">Click New sales order.</span></span>
    * <span data-ttu-id="0ebc3-116">من المستحسن تسجيل رقم أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="0ebc3-117">ستحتاجه إليه لاحقًا في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="0ebc3-118">في حقل "رقم الصنف البحث"، اكتب "88000"، ثم اضغط المفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="0ebc3-119">هذا صنف استمرارية في بيانات العرض التوضيحي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="0ebc3-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="0ebc3-120">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="0ebc3-120">Click Complete.</span></span>
8. <span data-ttu-id="0ebc3-121">في الحقل "أسلوب الدفع‬"، أدخل "Visa‬".</span><span class="sxs-lookup"><span data-stu-id="0ebc3-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="0ebc3-122">انقر فوق "‏‫إضافة بطاقة الائتمان‬".</span><span class="sxs-lookup"><span data-stu-id="0ebc3-122">Click Add credit card.</span></span>
    * <span data-ttu-id="0ebc3-123">أدخل معلومات بطاقة الائتمان المطلوبة على هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="0ebc3-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0ebc3-124">Click OK.</span></span>
11. <span data-ttu-id="0ebc3-125">قم بتوسيع قسم الدفع.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="0ebc3-126">لإرسال أمر مركز اتصال، يجب إدخال المدفوعات للأمر.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="0ebc3-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0ebc3-127">Click OK.</span></span>
13. <span data-ttu-id="0ebc3-128">انقر فوق تقديم.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-128">Click Submit.</span></span>
    * <span data-ttu-id="0ebc3-129">انتهيت من إنشاء أمر استمرارية جديد.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="0ebc3-130">وبعد ذلك، عليك تشغيل عمليتين دُفعيتين يتم استخدامهما لمعالجة أوامر الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="0ebc3-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-131">Close the page.</span></span>
15. <span data-ttu-id="0ebc3-132">انتقل إلى البيع بالتجزئة والتجارة > الاستمرارية > معالجة مدفوعات الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="0ebc3-133">في حقل "صنف الاستمرارية"، اكتب "88000"، ثم اضغط المفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="0ebc3-134">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-134">Click OK.</span></span>
18. <span data-ttu-id="0ebc3-135">انتقل إلى البيع بالتجزئة والتجارة > الاستمرارية > إنشاء أوامر فرعية للاستمرارية‬.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="0ebc3-136">ستقوم هذه العملية بإنشاء أوامر مبيعات جديدة استنادًا إلى إعدادات برامج الاستمرارية.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="0ebc3-137">في حقل "صنف الاستمرارية"، اكتب "88000"، ثم اضغط المفتاح Tab.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="0ebc3-138">الصنف "88000'" عبارة عن صنف استمرارية في بيانات العرض التوضيحي USRT.‬</span><span class="sxs-lookup"><span data-stu-id="0ebc3-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="0ebc3-139">في الحقل "أمر المبيعات"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="0ebc3-140">أدخل رقم أمر المبيعات الذي قمت بتسجيله سابقًا في الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="0ebc3-141">سيؤدي ذلك إلى إبقاء وقت المعالجة بالحد الأدنى لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="0ebc3-142">الحقل "أمر المبيعات" اختياري--ستتمكن من معالجة كافة الأوامر في أي برنامج واحد.</span><span class="sxs-lookup"><span data-stu-id="0ebc3-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="0ebc3-143">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0ebc3-143">Click OK.</span></span>
