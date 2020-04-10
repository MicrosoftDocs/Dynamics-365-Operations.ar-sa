---
title: ‏‫تحديد شروط دفع المورّد‬
description: يصف هذا الموضوع كيفية إعداد شروط الدفع لفواتير المورّدين.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143877"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="ee422-103">‏‫تحديد شروط دفع المورّد‬</span><span class="sxs-lookup"><span data-stu-id="ee422-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee422-104">يصف هذا الموضوع كيفية إعداد شروط الدفع لفواتير المورّدين.</span><span class="sxs-lookup"><span data-stu-id="ee422-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="ee422-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="ee422-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ee422-106">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > إعداد الدفع‬ > شروط الدفع**.</span><span class="sxs-lookup"><span data-stu-id="ee422-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="ee422-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ee422-107">Select **New**.</span></span> <span data-ttu-id="ee422-108">تُستخدم صفحة "شروط الدفع" لتعريف الطريقة التي سيتم بها حساب تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="ee422-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="ee422-109">ولا تستخدم هذه الصفحة لتعريف كيف سيتم حساب تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="ee422-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="ee422-110">في حقل **شروط الدفع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ee422-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="ee422-111">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ee422-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="ee422-112">في الحقل **الأيام**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ee422-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="ee422-113">سيستخدم الرقم الذي تم إدخاله هنا لإضافته إلى تاريخ الاستحقاق، أو إلى نهاية الفترة المحددة في طريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="ee422-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="ee422-114">على سبيل المثال، إذا قمت بتحديد **الصافي**، فسيضاف الرقم إلى تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="ee422-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="ee422-115">أما إذا حددت **الشهر الحالي**، فسيُضاف الرقم إلى اليوم الأخير من الشهر الحالي لحساب تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="ee422-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="ee422-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ee422-116">Select **Save**.</span></span>
7. <span data-ttu-id="ee422-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ee422-117">Close the page.</span></span>
8. <span data-ttu-id="ee422-118">انتقل إلى **الحسابات المدينة > إعداد الدفع > الخصومات النقدية**‬‬.</span><span class="sxs-lookup"><span data-stu-id="ee422-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="ee422-119">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ee422-119">Select **New**.</span></span>
10. <span data-ttu-id="ee422-120">في الحقل **الخصم النقدي**، أدخل معرفًا.</span><span class="sxs-lookup"><span data-stu-id="ee422-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="ee422-121">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ee422-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="ee422-122">إذا قدم المورّد خصمًا متدرجًا، فحدد الخصم النقدي التالي بعد انتهاء مدة صلاحية الحالي.</span><span class="sxs-lookup"><span data-stu-id="ee422-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="ee422-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ee422-123">Close the page.</span></span>
14. <span data-ttu-id="ee422-124">في الحقل **الأيام**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="ee422-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="ee422-125">سيتم استخدام الكمية المدخلة في حقل **الأيام** لحساب تاريخ الخصم النقدي، استنادًا إلى الخيار الذي تم تحديده في الحقل **الصافي/الحالي**‬".</span><span class="sxs-lookup"><span data-stu-id="ee422-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="ee422-126">إذا تم تحديد **الصافي**، فستضاف الكمية إلى تاريخ الفاتورة لتحديد تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="ee422-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="ee422-127">إذا تم تحديد **الشهر الحالي**، فستضاف الكمية إلى نهاية الشهر الحالي لتحديد تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="ee422-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="ee422-128">أدخل النسبة المئوية للخصم النقدي في حقل **الخصم**.</span><span class="sxs-lookup"><span data-stu-id="ee422-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="ee422-129">أدخل الحساب الرئيسي الذي سيتم ترحيل الخصم النقدي إليه لفواتير العميل، ثم أدخل الحساب الرئيسي الذي سيتم ترحيل الخصم النقدي إليه لفواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="ee422-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="ee422-130">إذا تم تعيين **الحسابات المقابلة للخصومات** إلى **استخدام الحساب الرئيسي لخصم المورد**، فسيتم عندئذٍ استخدام الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="ee422-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="ee422-131">إذا تم تعيين الخيار إلى **الحسابات الموجودة في بنود الفاتورة**، فسيتم ترحيل الخصم النقدي إلى حسابات الأصول/المصروفات على بنود الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="ee422-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="ee422-132">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="ee422-132">Select **Save**.</span></span>

