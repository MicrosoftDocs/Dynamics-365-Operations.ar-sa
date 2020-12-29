---
title: إنشاء قالب فاتورة نص حر
description: يوضح هذا الإجراء كيفية إنشاء قالب فاتورة نص حر.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8281de3cb336d9392a6a97f98e51a2a139a384c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439814"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="c1670-103">إنشاء قالب فاتورة نص حر</span><span class="sxs-lookup"><span data-stu-id="c1670-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1670-104">بالنسبة لهذه المعاينة، استخدم شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c1670-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="c1670-105">هذا الإجراء مخصص للمستخدم المسؤول عن إدارة فواتير الحسابات المدينة ومعالجتها.</span><span class="sxs-lookup"><span data-stu-id="c1670-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="c1670-106">إنشاء قالب</span><span class="sxs-lookup"><span data-stu-id="c1670-106">Create a template</span></span>

1. <span data-ttu-id="c1670-107">انتقل إلى الحسابات المدينة > الفواتير > الفواتير المتكررة > قوالب فاتورة النص الحر‬.</span><span class="sxs-lookup"><span data-stu-id="c1670-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="c1670-108">استخدم هذا النموذج لإنشاء قوالب الفواتير ذات نص حر التي يمكن أن تتضمن بنود الفاتورة والمصاريف وقالب التوزيع المحاسبي بالإضافة إلى معلومات حساب دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="c1670-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="c1670-109">انقر فوق "جديد" لإنشاء قالب جديد ذات نص حر.</span><span class="sxs-lookup"><span data-stu-id="c1670-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="c1670-110">في الحقل "اسم القالب"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c1670-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="c1670-111">يعرّف "اسم القالب" بشكل فريد قالب فاتورة ذات نص حر.</span><span class="sxs-lookup"><span data-stu-id="c1670-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="c1670-112">لا يمكن إعطاء "اسم القالب" نفسه لقالبين.</span><span class="sxs-lookup"><span data-stu-id="c1670-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="c1670-113">في الحقل "الوصف"، أدخل وصفًا للقالب.</span><span class="sxs-lookup"><span data-stu-id="c1670-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="c1670-114">وسّع علامة التبويب "بنود الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="c1670-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="c1670-115">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="c1670-116">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="c1670-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="c1670-117">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="c1670-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="c1670-118">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c1670-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c1670-119">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c1670-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="c1670-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1670-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c1670-121">في الحقل "مجموعة ضرائب الصنف"، حدد مجموعة ضريبة مبيعات الصنف‬ لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="c1670-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="c1670-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1670-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c1670-123">في الحقل "سعر الوحدة"، أدخل أو اعرض سعر الوحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="c1670-124">يتم ضرب هذا المبلغ في القيمة الموجودة في حقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="c1670-125">أضف بندًا جديدًا إلى قالب فاتورة نص حر.</span><span class="sxs-lookup"><span data-stu-id="c1670-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="c1670-126">في الحقل "الوصف"، أدخل وصفًا لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="c1670-127">في حقل "الحساب الرئيسي"، حدد حساب إيرادات.</span><span class="sxs-lookup"><span data-stu-id="c1670-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="c1670-128">يمكنك تحديد حساب الحركة المقابل الخاص بائتمان العميل لإجمالي مبلغ الفاتورة في صفحة "ملفات تعريف ترحيل العميل‬".</span><span class="sxs-lookup"><span data-stu-id="c1670-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="c1670-129">في الحقل "مجموعة ضريبة المبيعات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c1670-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c1670-130">مجموعة ضريبة المبيعات لبند الفاتورة الحالية هي مجموعة ضريبة المبيعات الافتراضية لحساب العميل.</span><span class="sxs-lookup"><span data-stu-id="c1670-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="c1670-131">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1670-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c1670-132">في الحقل "مجموعة ضرائب المبيعات للأصناف‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c1670-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c1670-133">مجموعة ضرائب مبيعات الأصناف لبند الفاتورة الحالي.</span><span class="sxs-lookup"><span data-stu-id="c1670-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="c1670-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1670-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="c1670-135">أدخل أو اعرض عدد الوحدات لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="c1670-136">يتم ضرب هذا الرقم في القيمة الموجودة في حقل "سعر الوحدة" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="c1670-137">أدخل أو اعرض السعر لكل وحدة لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="c1670-138">يتم ضرب هذا المبلغ في القيمة الموجودة في الحقل "الكمية" لتحديد مبلغ بند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c1670-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="c1670-139">اعرض التوزيعات المحاسبية لبند واحد وأية بنود فرعية وعدّلها.</span><span class="sxs-lookup"><span data-stu-id="c1670-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="c1670-140">تحدد التوزيعات المحاسبية كيفية حساب مبلغ، مثل كيفية حساب الإيراد أو الضريبة أو التكاليف في فاتورة ذات نص حر.</span><span class="sxs-lookup"><span data-stu-id="c1670-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="c1670-141">حدّث التوزيعات المحاسبية لبند الفاتورة المحدد.</span><span class="sxs-lookup"><span data-stu-id="c1670-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="c1670-142">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="c1670-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="c1670-143">​حفظ فاتورة نص حر كقالب</span><span class="sxs-lookup"><span data-stu-id="c1670-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="c1670-144">يمكنك أيضًا حفظ فاتورة نص حر موجودة كقالب.</span><span class="sxs-lookup"><span data-stu-id="c1670-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="c1670-145">عندما تقوم بتحديد حفظ من علامة التبويب الفاتورة، قم بإدخال اسم ووصف للقالب.</span><span class="sxs-lookup"><span data-stu-id="c1670-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="c1670-146">إذا كان هناك قالب موجود بنفس الاسم، فسوف يظهر إخطار يُفيد بأنه يوجد قالب بنفس الاسم.</span><span class="sxs-lookup"><span data-stu-id="c1670-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="c1670-147">يمكنك الاستمرار في الضغط على موافق لاستبداله.</span><span class="sxs-lookup"><span data-stu-id="c1670-147">You can still click on Ok to replace it.</span></span> 
