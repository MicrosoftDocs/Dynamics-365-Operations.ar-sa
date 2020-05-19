---
title: المزامنة مع محرك التسعير عند الطلب في Dynamics 365 Supply Chain Management
description: يصف هذا الموضوع كيفية استخدام محرك التسعير في  Microsoft Dynamics 365 Supply Chain Management من Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 5ffc0358ff58b2a05aa84b4467a27d88b5e1ec42
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270326"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="a44fb-103">المزامنة مع محرك التسعير عند الطلب في Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a44fb-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a44fb-104">يتضمن Microsoft Dynamics 365 Supply Chain Management محرك تسعير يتعامل مع اتفاقيات التجارة وقوائم الأسعار وبرامج ولاء العملاء والعروض الترويجية والخصومات.</span><span class="sxs-lookup"><span data-stu-id="a44fb-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="a44fb-105">يستخدم محرك التسعير قواعد معقدة لتحديد أفضل سعر لعرض أسعار أو أمر معين.</span><span class="sxs-lookup"><span data-stu-id="a44fb-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="a44fb-106">عند استخدام الكتابة الثنائية، فإنك تستخدم إما محرك التسعير من Dynamics 365 Supply Chain Managementمن صفحات عرض الأسعار والنظام في Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a44fb-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="a44fb-107">استخدام محرك التسعير من Supply Chain Management في Sales</span><span class="sxs-lookup"><span data-stu-id="a44fb-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="a44fb-108">في Sales، انتقل إلى **Sales \> الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="a44fb-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="a44fb-109">حدد **جديد** لإنشاء أمر جديد أو حدد أمرًا موجودًا في قائمة **الأوامر الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="a44fb-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="a44fb-110">أضف بند أمر جديدًا.</span><span class="sxs-lookup"><span data-stu-id="a44fb-110">Add a new order line.</span></span>
4. <span data-ttu-id="a44fb-111">إذا كنت تقوم بإنشاء أمر جديد، فحدد **أمر سعر** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="a44fb-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="a44fb-112">إذا كنت تقوم بتحديث أمر موجود، فحدد **إعادة حساب** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="a44fb-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="a44fb-113">يتم ملء الحقول التالية تلقائيًا:</span><span class="sxs-lookup"><span data-stu-id="a44fb-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="a44fb-114">تفاصيل المبلغ</span><span class="sxs-lookup"><span data-stu-id="a44fb-114">Detail Amount</span></span>
    + <span data-ttu-id="a44fb-115">النسبة المئوية للخصم</span><span class="sxs-lookup"><span data-stu-id="a44fb-115">Discount %</span></span>
    + <span data-ttu-id="a44fb-116">الخصم</span><span class="sxs-lookup"><span data-stu-id="a44fb-116">Discount</span></span>
    + <span data-ttu-id="a44fb-117">مبلغ ما قبل الشحن</span><span class="sxs-lookup"><span data-stu-id="a44fb-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="a44fb-118">مبلغ الشحن</span><span class="sxs-lookup"><span data-stu-id="a44fb-118">Freight Amount</span></span>
    + <span data-ttu-id="a44fb-119">إجمالي الضريبة</span><span class="sxs-lookup"><span data-stu-id="a44fb-119">Total Tax</span></span>
    + <span data-ttu-id="a44fb-120">المبلغ الإجمالي</span><span class="sxs-lookup"><span data-stu-id="a44fb-120">Total Amount</span></span>
    
5. <span data-ttu-id="a44fb-121">لضمان أن النظام يضع في الاعتبار اتفاقيات التجارة والبيع لحساب السعر:</span><span class="sxs-lookup"><span data-stu-id="a44fb-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="a44fb-122">انتقل إلى بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a44fb-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="a44fb-123">انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="a44fb-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="a44fb-124">حدد علامة تبويب **الأسعار** في شريط التنقل الجانبي.</span><span class="sxs-lookup"><span data-stu-id="a44fb-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="a44fb-125">تحت علامة التبويب السريعة **تقييم اتفاقية التجارة** قم بإلغاء تحديد خيار **الإدخال اليدوي**.</span><span class="sxs-lookup"><span data-stu-id="a44fb-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="a44fb-126">كيف يعمل</span><span class="sxs-lookup"><span data-stu-id="a44fb-126">How it works</span></span>

<span data-ttu-id="a44fb-127">عند تحديد **أمر السعر** في Sales، يتم استدعاء وظيفة **الإجماليات** في علامة التبويب **أمر المبيعات\> عرض** في Supply Chain Management لأمر المبيعات المقترن.</span><span class="sxs-lookup"><span data-stu-id="a44fb-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="a44fb-128">يتم استخدام القيم في إجمالي الأمر في Sales لملء الحقول المقابلة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a44fb-128">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="a44fb-129">عند حساب إجمالي أمر المبيعات في Supply Chain Management، يقيّم الحساب اتفاقيات التجارة واتفاقيات المبيعات الحالية للعميل والمنتجات المدرجة في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a44fb-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="a44fb-130">يتم استخدام هذه المعلومات لحساب الإجماليات.</span><span class="sxs-lookup"><span data-stu-id="a44fb-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="a44fb-131">عند تحديد **أمر السعر**، يعكس Sales تلقائيًا كل الإعداد الذي تم إجراؤه في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a44fb-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="a44fb-132">قيود</span><span class="sxs-lookup"><span data-stu-id="a44fb-132">Limitations</span></span>

<span data-ttu-id="a44fb-133">عند ملء الحقول في Sales، يتم تطبيق القيود التالية:</span><span class="sxs-lookup"><span data-stu-id="a44fb-133">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="a44fb-134">لا يتم تكرار إعداد الرسوم ومخصصات الرسوم في Supply Chain Management في Sales.</span><span class="sxs-lookup"><span data-stu-id="a44fb-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="a44fb-135">لا يأخذ التشعير بعين الاعتبار تسعير البيع بالتجزئة الخاص المحدد في حقل **قناة البيع بالتجزئة** في صفحة بند أمر المبيعات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a44fb-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="a44fb-136">لا يتم الأخذ بعين الاعتبار الخصومات المحددة في قسم **إدارة البدل التجاري‬** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a44fb-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>