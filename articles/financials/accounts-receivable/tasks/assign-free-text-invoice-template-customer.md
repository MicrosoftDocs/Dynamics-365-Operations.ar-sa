--- 
title: "‏‫تعيين قالب فاتورة ذات نص حر إلى عميل"
description: "توضح هذه المهمة كيفية تعيين قالب فاتورة نص حر إلى عميل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e29122fa775385ca4d407ddbe190626d743da69b
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="c71b5-103">‏‫تعيين قالب فاتورة ذات نص حر إلى عميل</span><span class="sxs-lookup"><span data-stu-id="c71b5-103">Assign a free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c71b5-104">توضح هذه المهمة كيفية تعيين قالب فاتورة نص حر إلى عميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="c71b5-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF وهي مخصصة للمستخدم المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="c71b5-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="c71b5-106">انتقل إلى الحسابات المدينة > العملاء > كافة العملاء‬.</span><span class="sxs-lookup"><span data-stu-id="c71b5-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="c71b5-107">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c71b5-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c71b5-108">في جزء "الإجراءات"، انقر فوق "فاتورة".</span><span class="sxs-lookup"><span data-stu-id="c71b5-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="c71b5-109">انقر فوق "الفواتير المتكررة".</span><span class="sxs-lookup"><span data-stu-id="c71b5-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="c71b5-110">استخدم هذه الصفحة لتعيين قوالب فاتورة النص الحر للعملاء وتحديد مدى تكرار إرسال الفواتير للعميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="c71b5-111">انقر فوق "جديد" لتعيين قالب جديد إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="c71b5-112">حدد قالب فاتورة النص الحر الذي تريد تعيينه إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="c71b5-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c71b5-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c71b5-114">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c71b5-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c71b5-115">أدخل التاريخ عند إنشاء أول فاتورة.</span><span class="sxs-lookup"><span data-stu-id="c71b5-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="c71b5-116">أدخل تاريخ انتهاء متكررًا.</span><span class="sxs-lookup"><span data-stu-id="c71b5-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="c71b5-117">حدد واحدًا مما يلي: لا يوجد تاريخ انتهاء – سيتم إنشاء الفواتير إلى أجل غير مسمى حتى تتم إزالة القالب من حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="c71b5-118">تاريخ انتهاء الفوترة – حدد هذا الخيار وأدخل آخر تاريخ يمكن إنشاء الفاتورة فيه.</span><span class="sxs-lookup"><span data-stu-id="c71b5-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="c71b5-119">الحد الأقصى للمبلغ التراكمي الذي سيتوقف بعده إنشاء الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c71b5-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="c71b5-120">أدخل الحد الأقصى للمبلغ التراكمي الذي يمكن الوصول إليه باستخدام القالب المحدد.</span><span class="sxs-lookup"><span data-stu-id="c71b5-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="c71b5-121">على سبيل المثال، إذا أدخلت 1,000.00 وأنشأت الفواتير الشهرية لكل 100.00، فسيتوقف إنشاء الفواتير بعد إنشاء الفاتورة العاشرة.</span><span class="sxs-lookup"><span data-stu-id="c71b5-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="c71b5-122">أنشئ فواتير متكررة باستخدام القيم الافتراضية من قالب فاتورة النص الحر أو حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="c71b5-123">حدد ما إذا كنت تريد استخدام قالب فاتورة النص الحر أو حساب العميل لتحديد القيم الافتراضية للغة، وترحيل ملف التعريف، ومجموعة ضرائب المبيعات، ومجموعة ضرائب مبيعات الأصناف، وكود القائمة، والبلد/المنطقة للتسليم، والعملة، وشروط الدفع، وطريقة الدفع، ومواصفات الدفع، وجدول الدفع، والخصم النقدي، والأبعاد المالية، وقسيمة التحويل البنكي عندما يتم إنشاء فواتير.</span><span class="sxs-lookup"><span data-stu-id="c71b5-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="c71b5-124">حدد نمط التكرار.</span><span class="sxs-lookup"><span data-stu-id="c71b5-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="c71b5-125">يوميًا – حدد هذا الخيار وأدخل عدد الأيام في الحقل "كل".</span><span class="sxs-lookup"><span data-stu-id="c71b5-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="c71b5-126">على سبيل المثال، إذا قمت بإدخال 15، فسيتم إنشاء فاتورة كل 15 يومًا لهذا العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="c71b5-127">أسبوعيًا - حدد هذا الخيار وأدخل عدد الأسابيع في الحقل "كل".</span><span class="sxs-lookup"><span data-stu-id="c71b5-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="c71b5-128">على سبيل المثال، إذا قمت بإدخال 2، فسيتم إنشاء فاتورة كل أسبوعين لهذا العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="c71b5-129">شهريًا - حدد هذا الخيار وأدخل عدد الأشهر في الحقل "كل".</span><span class="sxs-lookup"><span data-stu-id="c71b5-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="c71b5-130">على سبيل المثال، إذا قمت بإدخال 6، فسيتم إنشاء فاتورة كل ستة أشهر لهذا العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="c71b5-131">سنويًا – حدد هذا الخيار وأدخل عدد السنوات في الحقل "كل".</span><span class="sxs-lookup"><span data-stu-id="c71b5-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="c71b5-132">على سبيل المثال، إذا قمت بإدخال 2، فسيتم إنشاء فاتورة كل سنتين لهذا العميل.</span><span class="sxs-lookup"><span data-stu-id="c71b5-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="c71b5-133">في الحقل "لكل‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c71b5-133">In the Per field, enter a number.</span></span>


