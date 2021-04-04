---
title: المزامنة عند الطلب باستخدام محرك تسعير Supply Chain Management
description: يصف هذا الموضوع كيفية استخدام محرك التسعير في  Microsoft Dynamics 365 Supply Chain Management من Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e2067e83d3f0c98e986873b8eaf1b817de912c0f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570130"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="e2ca8-103">المزامنة عند الطلب باستخدام محرك تسعير Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e2ca8-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e2ca8-104">يتضمن Microsoft Dynamics 365 Supply Chain Management محرك تسعير يتعامل مع اتفاقيات التجارة وقوائم الأسعار وبرامج ولاء العملاء والعروض الترويجية والخصومات.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="e2ca8-105">يستخدم محرك التسعير قواعد معقدة لتحديد أفضل سعر لعرض أسعار أو أمر معين.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="e2ca8-106">عند استخدام الكتابة الثنائية، فإنك تستخدم إما محرك التسعير من Dynamics 365 Supply Chain Managementمن صفحات عرض الأسعار والنظام في Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="e2ca8-107">استخدام محرك التسعير من Supply Chain Management في Sales</span><span class="sxs-lookup"><span data-stu-id="e2ca8-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="e2ca8-108">في Sales، انتقل إلى **Sales \> الأوامر**.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="e2ca8-109">حدد **جديد** لإنشاء أمر جديد أو حدد أمرًا موجودًا في قائمة **الأوامر الخاصة بي**.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="e2ca8-110">أضف بند أمر جديدًا.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-110">Add a new order line.</span></span>
4. <span data-ttu-id="e2ca8-111">إذا كنت تقوم بإنشاء أمر جديد، فحدد **أمر سعر** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="e2ca8-112">إذا كنت تقوم بتحديث أمر موجود، فحدد **إعادة حساب** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="e2ca8-113">يتم ملء الأعمدة التالية تلقائيًا:</span><span class="sxs-lookup"><span data-stu-id="e2ca8-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="e2ca8-114">تفاصيل المبلغ</span><span class="sxs-lookup"><span data-stu-id="e2ca8-114">Detail Amount</span></span>
    + <span data-ttu-id="e2ca8-115">النسبة المئوية للخصم</span><span class="sxs-lookup"><span data-stu-id="e2ca8-115">Discount %</span></span>
    + <span data-ttu-id="e2ca8-116">الخصم</span><span class="sxs-lookup"><span data-stu-id="e2ca8-116">Discount</span></span>
    + <span data-ttu-id="e2ca8-117">مبلغ ما قبل الشحن</span><span class="sxs-lookup"><span data-stu-id="e2ca8-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="e2ca8-118">مبلغ الشحن</span><span class="sxs-lookup"><span data-stu-id="e2ca8-118">Freight Amount</span></span>
    + <span data-ttu-id="e2ca8-119">إجمالي الضريبة</span><span class="sxs-lookup"><span data-stu-id="e2ca8-119">Total Tax</span></span>
    + <span data-ttu-id="e2ca8-120">المبلغ الإجمالي</span><span class="sxs-lookup"><span data-stu-id="e2ca8-120">Total Amount</span></span>
    
5. <span data-ttu-id="e2ca8-121">لضمان أن النظام يضع في الاعتبار اتفاقيات التجارة والبيع لحساب السعر:</span><span class="sxs-lookup"><span data-stu-id="e2ca8-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="e2ca8-122">انتقل إلى بيئة Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="e2ca8-123">انتقل إلى **الحسابات المدينة \> إعداد \> معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="e2ca8-124">حدد علامة تبويب **الأسعار** في شريط التنقل الجانبي.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="e2ca8-125">تحت علامة التبويب السريعة **تقييم اتفاقية التجارة** قم بإلغاء تحديد خيار **الإدخال اليدوي**.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="e2ca8-126">كيف يعمل</span><span class="sxs-lookup"><span data-stu-id="e2ca8-126">How it works</span></span>

<span data-ttu-id="e2ca8-127">عند تحديد **أمر السعر** في Sales، يتم استدعاء وظيفة **الإجماليات** في علامة التبويب **أمر المبيعات\> عرض** في Supply Chain Management لأمر المبيعات المقترن.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="e2ca8-128">يتم استخدام القيم في إجمالي الأمر في Sales لملء الأعمدة المقابلة في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="e2ca8-129">عند حساب إجمالي أمر المبيعات في Supply Chain Management، يقيّم الحساب اتفاقيات التجارة واتفاقيات المبيعات الحالية للعميل والمنتجات المدرجة في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="e2ca8-130">يتم استخدام هذه المعلومات لحساب الإجماليات.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="e2ca8-131">عند تحديد **أمر السعر**، يعكس Sales تلقائيًا كل الإعداد الذي تم إجراؤه في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="e2ca8-132">قيود</span><span class="sxs-lookup"><span data-stu-id="e2ca8-132">Limitations</span></span>

<span data-ttu-id="e2ca8-133">عند ملء الأعمدة في Sales، يتم تطبيق القيود التالية:</span><span class="sxs-lookup"><span data-stu-id="e2ca8-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="e2ca8-134">لا يتم تكرار إعداد الرسوم ومخصصات الرسوم في Supply Chain Management في Sales.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="e2ca8-135">لا يأخذ التشعير بعين الاعتبار تسعير البيع بالتجزئة الخاص المحدد في عمود **قناة البيع بالتجزئة** في صفحة بند أمر المبيعات في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="e2ca8-136">لا يتم الأخذ بعين الاعتبار الخصومات المحددة في قسم **إدارة البدل التجاري‬** في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e2ca8-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]