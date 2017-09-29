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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="86b07-103">إنشاء قالب فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="86b07-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86b07-104">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="86b07-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="86b07-105">التسجيل مخصص للمستخدم المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="86b07-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="86b07-106">انتقل إلى الحسابات المدينة > الفواتير > الفواتير المتكررة > قوالب فاتورة النص الحر‬.</span><span class="sxs-lookup"><span data-stu-id="86b07-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="86b07-107">استخدم هذا النموذج لإنشاء قوالب الفواتير بنص حر التي يمكن أن تتضمن بنود الفاتورة والمصاريف وقالب التوزيع المحاسبي بالإضافة إلى معلومات حساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="86b07-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="86b07-108">انقر فوق "جديد" لإنشاء قالب جديد بنص حر.</span><span class="sxs-lookup"><span data-stu-id="86b07-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="86b07-109">في الحقل "اسم القالب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="86b07-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="86b07-110">يعرّف "اسم القالب" بشكل فريد قالب فاتورة بنص حر.</span><span class="sxs-lookup"><span data-stu-id="86b07-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="86b07-111">لا يمكن إعطاء "اسم القالب" نفسه لقالبين.</span><span class="sxs-lookup"><span data-stu-id="86b07-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="86b07-112">في الحقل "الوصف"، أدخل وصفًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="86b07-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="86b07-113">وسّع علامة التبويب "بنود الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="86b07-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="86b07-114">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="86b07-115">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="86b07-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="86b07-116">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="86b07-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="86b07-117">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="86b07-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="86b07-118">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="86b07-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="86b07-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="86b07-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="86b07-120">في الحقل "مجموعة ضرائب الصنف"، حدد مجموعة ضريبة مبيعات الصنف‬ لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="86b07-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="86b07-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="86b07-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="86b07-122">في الحقل "سعر الوحدة"، أدخل أو اعرض سعر الوحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="86b07-123">يتم ضرب هذا المبلغ في القيمة الموجودة في حقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="86b07-124">أضف بندًا جديدًا إلى قالب فاتورة نص حر.</span><span class="sxs-lookup"><span data-stu-id="86b07-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="86b07-125">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="86b07-126">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="86b07-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="86b07-127">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="86b07-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="86b07-128">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="86b07-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="86b07-129">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="86b07-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="86b07-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="86b07-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="86b07-131">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="86b07-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="86b07-132">مجموعة ضرائب مبيعات الأصناف لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="86b07-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="86b07-133">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="86b07-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="86b07-134">أدخل أو اعرض عدد الوحدات لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="86b07-135">يتم ضرب هذا الرقم في القيمة الموجودة في حقل "سعر الوحدة" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="86b07-136">أدخل أو اعرض السعر لكل وحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="86b07-137">يتم ضرب هذا المبلغ في القيمة الموجودة في الحقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86b07-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="86b07-138">اعرض التوزيعات المحاسبية لبند واحد وأية بنود فرعية وعدّلها.</span><span class="sxs-lookup"><span data-stu-id="86b07-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="86b07-139">تحدد التوزيعات المحاسبية كيفية حساب مبلغ، مثل كيفية حساب الإيراد أو الضريبة أو التكاليف في فاتورة بنص حر.</span><span class="sxs-lookup"><span data-stu-id="86b07-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="86b07-140">حدّث التوزيعات المحاسبية لبند الفاتورة المحدد.</span><span class="sxs-lookup"><span data-stu-id="86b07-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="86b07-141">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="86b07-141">Click Close.</span></span>


