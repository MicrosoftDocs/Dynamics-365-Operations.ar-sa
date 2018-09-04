--- 
title: "إنشاء قالب فاتورة نص حر"
description: "يوضح هذا الإجراء كيفية إنشاء قالب فاتورة نص حر."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
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
ms.openlocfilehash: 91f2ec2f8ab21616c6a1b886ee89d6faf84023e4
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="c18f5-103">إنشاء قالب فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="c18f5-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c18f5-104">بالنسبة لهذه المعاينة، استخدم شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c18f5-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="c18f5-105">هذا الإجراء مخصص للمستخدم المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="c18f5-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="c18f5-106">إنشاء قالب</span><span class="sxs-lookup"><span data-stu-id="c18f5-106">Create a template</span></span>

1. <span data-ttu-id="c18f5-107">انتقل إلى الحسابات المدينة > الفواتير > الفواتير المتكررة > قوالب فاتورة النص الحر‬.</span><span class="sxs-lookup"><span data-stu-id="c18f5-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="c18f5-108">استخدم هذا النموذج لإنشاء قوالب الفواتير بنص حر التي يمكن أن تتضمن بنود الفاتورة والمصاريف وقالب التوزيع المحاسبي بالإضافة إلى معلومات حساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="c18f5-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="c18f5-109">انقر فوق "جديد" لإنشاء قالب جديد بنص حر.</span><span class="sxs-lookup"><span data-stu-id="c18f5-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="c18f5-110">في الحقل "اسم القالب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="c18f5-111">يعرّف "اسم القالب" بشكل فريد قالب فاتورة بنص حر.</span><span class="sxs-lookup"><span data-stu-id="c18f5-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="c18f5-112">لا يمكن إعطاء "اسم القالب" نفسه لقالبين.</span><span class="sxs-lookup"><span data-stu-id="c18f5-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="c18f5-113">في الحقل "الوصف"، أدخل وصفًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="c18f5-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="c18f5-114">وسّع علامة التبويب "بنود الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="c18f5-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="c18f5-115">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="c18f5-116">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="c18f5-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="c18f5-117">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="c18f5-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="c18f5-118">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c18f5-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c18f5-119">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c18f5-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="c18f5-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c18f5-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c18f5-121">في الحقل "مجموعة ضرائب الصنف"، حدد مجموعة ضريبة مبيعات الصنف‬ لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="c18f5-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="c18f5-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c18f5-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c18f5-123">في الحقل "سعر الوحدة"، أدخل أو اعرض سعر الوحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="c18f5-124">يتم ضرب هذا المبلغ في القيمة الموجودة في حقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="c18f5-125">أضف بندًا جديدًا إلى قالب فاتورة نص حر.</span><span class="sxs-lookup"><span data-stu-id="c18f5-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="c18f5-126">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="c18f5-127">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="c18f5-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="c18f5-128">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="c18f5-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="c18f5-129">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c18f5-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c18f5-130">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c18f5-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="c18f5-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c18f5-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c18f5-132">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c18f5-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c18f5-133">مجموعة ضرائب مبيعات الأصناف لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="c18f5-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="c18f5-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c18f5-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="c18f5-135">أدخل أو اعرض عدد الوحدات لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="c18f5-136">يتم ضرب هذا الرقم في القيمة الموجودة في حقل "سعر الوحدة" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="c18f5-137">أدخل أو اعرض السعر لكل وحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="c18f5-138">يتم ضرب هذا المبلغ في القيمة الموجودة في الحقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c18f5-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="c18f5-139">اعرض التوزيعات المحاسبية لبند واحد وأية بنود فرعية وعدّلها.</span><span class="sxs-lookup"><span data-stu-id="c18f5-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="c18f5-140">تحدد التوزيعات المحاسبية كيفية حساب مبلغ، مثل كيفية حساب الإيراد أو الضريبة أو التكاليف في فاتورة بنص حر.</span><span class="sxs-lookup"><span data-stu-id="c18f5-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="c18f5-141">حدّث التوزيعات المحاسبية لبند الفاتورة المحدد.</span><span class="sxs-lookup"><span data-stu-id="c18f5-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="c18f5-142">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="c18f5-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="c18f5-143">​حفظ فاتورة نص حر كقالب</span><span class="sxs-lookup"><span data-stu-id="c18f5-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="c18f5-144">يمكنك أيضًا حفظ فاتورة نص حر موجودة كقالب.</span><span class="sxs-lookup"><span data-stu-id="c18f5-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="c18f5-145">عندما تقوم بتحديد حفظ من علامة التبويب الفاتورة، قم بإدخال اسم ووصف للقالب.</span><span class="sxs-lookup"><span data-stu-id="c18f5-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="c18f5-146">إذا كان هناك قالب موجود بنفس الاسم، فسوف يظهر إخطار يُفيد بأنه يوجد قالب بنفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="c18f5-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="c18f5-147">يمكنك الاستمرار في الضغط على موافق لاستبداله.</span><span class="sxs-lookup"><span data-stu-id="c18f5-147">You can still click on Ok to replace it.</span></span> 
