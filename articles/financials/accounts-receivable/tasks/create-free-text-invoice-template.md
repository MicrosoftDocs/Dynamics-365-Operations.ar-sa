--- 
title: "إنشاء قالب فاتورة نص حر"
description: "يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="2b290-103">إنشاء قالب فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="2b290-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b290-104">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="2b290-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="2b290-105">التسجيل مخصص للمستخدم المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="2b290-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="2b290-106">انتقل إلى الحسابات المدينة > الفواتير > الفواتير المتكررة > قوالب فاتورة النص الحر‬.</span><span class="sxs-lookup"><span data-stu-id="2b290-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="2b290-107">استخدم هذا النموذج لإنشاء قوالب الفواتير بنص حر التي يمكن أن تتضمن بنود الفاتورة والمصاريف وقالب التوزيع المحاسبي بالإضافة إلى معلومات حساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="2b290-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="2b290-108">انقر فوق "جديد" لإنشاء قالب جديد بنص حر.</span><span class="sxs-lookup"><span data-stu-id="2b290-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="2b290-109">في الحقل "اسم القالب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2b290-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="2b290-110">يعرّف "اسم القالب" بشكل فريد قالب فاتورة بنص حر.</span><span class="sxs-lookup"><span data-stu-id="2b290-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="2b290-111">لا يمكن إعطاء "اسم القالب" نفسه لقالبين.</span><span class="sxs-lookup"><span data-stu-id="2b290-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="2b290-112">في الحقل "الوصف"، أدخل وصفًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="2b290-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="2b290-113">وسّع علامة التبويب "بنود الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="2b290-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="2b290-114">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="2b290-115">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="2b290-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="2b290-116">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="2b290-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="2b290-117">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2b290-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2b290-118">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="2b290-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="2b290-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2b290-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="2b290-120">في الحقل "مجموعة ضرائب الصنف"، حدد مجموعة ضريبة مبيعات الصنف‬ لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="2b290-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="2b290-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2b290-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2b290-122">في الحقل "سعر الوحدة"، أدخل أو اعرض سعر الوحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="2b290-123">يتم ضرب هذا المبلغ في القيمة الموجودة في حقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="2b290-124">أضف بندًا جديدًا إلى قالب فاتورة نص حر.</span><span class="sxs-lookup"><span data-stu-id="2b290-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="2b290-125">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="2b290-126">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="2b290-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="2b290-127">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="2b290-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="2b290-128">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2b290-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2b290-129">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="2b290-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="2b290-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2b290-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="2b290-131">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2b290-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2b290-132">مجموعة ضرائب مبيعات الأصناف لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="2b290-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="2b290-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2b290-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="2b290-134">أدخل أو اعرض عدد الوحدات لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="2b290-135">يتم ضرب هذا الرقم في القيمة الموجودة في حقل "سعر الوحدة" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="2b290-136">أدخل أو اعرض السعر لكل وحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="2b290-137">يتم ضرب هذا المبلغ في القيمة الموجودة في الحقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="2b290-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="2b290-138">اعرض التوزيعات المحاسبية لبند واحد وأية بنود فرعية وعدّلها.</span><span class="sxs-lookup"><span data-stu-id="2b290-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="2b290-139">تحدد التوزيعات المحاسبية كيفية حساب مبلغ، مثل كيفية حساب الإيراد أو الضريبة أو التكاليف في فاتورة بنص حر.</span><span class="sxs-lookup"><span data-stu-id="2b290-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="2b290-140">حدّث التوزيعات المحاسبية لبند الفاتورة المحدد.</span><span class="sxs-lookup"><span data-stu-id="2b290-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="2b290-141">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="2b290-141">Click Close.</span></span>


