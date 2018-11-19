--- 
title: "إعداد فترات تسوية ضريبة المبيعات"
description: "تحتوي فترات تسوية ضرائب المبيعات على معلومات عن الفترات الزمنية التي يجب خلالها الإبلاغ عن الضرائب ودفعها."
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 81214cc52b1488bb70ac5fd6ccc817f6f979163d
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.contentlocale: ar-sa
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="418f7-103">إعداد فترات تسوية ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="418f7-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="418f7-104">تحتوي فترات تسوية ضرائب المبيعات على معلومات عن الفترات الزمنية التي يجب خلالها الإبلاغ عن الضرائب ودفعها.</span><span class="sxs-lookup"><span data-stu-id="418f7-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="418f7-105">يمكن تشغيل عملية التسوية لفترة تسوية وفترة تاريخ محددة.</span><span class="sxs-lookup"><span data-stu-id="418f7-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="418f7-106">وستتم تسوية كافة أكواد الضرائب المقترنة بفترة التسوية.</span><span class="sxs-lookup"><span data-stu-id="418f7-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="418f7-107">بالاستناد إلى إعداد هيئة ضريبة المبيعات ذات الصلة، يتم ترحيل الالتزام الضريبي إما إلى حساب مورّد أو حساب دفتر أستاذ عام.</span><span class="sxs-lookup"><span data-stu-id="418f7-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="418f7-108">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="418f7-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="418f7-109">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > فترات تسوية ضرائب المبيعات‬.</span><span class="sxs-lookup"><span data-stu-id="418f7-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="418f7-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="418f7-110">Click New.</span></span>
3. <span data-ttu-id="418f7-111">في الحقل "فترة التسوية‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="418f7-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="418f7-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="418f7-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="418f7-113">في الحقل "الهيئة‬"، حدد هيئة ضريبة المبيعات التي تستلم التقارير والمدفوعات التي يتم إنشاؤها لفترة التسوية.</span><span class="sxs-lookup"><span data-stu-id="418f7-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="418f7-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="418f7-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="418f7-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="418f7-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="418f7-116">في الحقل "شروط الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="418f7-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="418f7-117">يمكن إعداد هيئة ضريبة المبيعات ذات الصلة كمورّد، وستنشئ تسوية ضريبة المبيعات فاتورة مورّد مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="418f7-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="418f7-118">تحدد شروط الدفع تاريخ الاستحقاق الخاص بفاتورة المورّد المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="418f7-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="418f7-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="418f7-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="418f7-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="418f7-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="418f7-121">حدد نوعًا للفترات الزمنية للتسوية.</span><span class="sxs-lookup"><span data-stu-id="418f7-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="418f7-122">أدخل عدد وحدات الفترة الزمنية لكل فترة.</span><span class="sxs-lookup"><span data-stu-id="418f7-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="418f7-123">على سبيل المثال، يتكون ربع السنة من 3 أشهر.</span><span class="sxs-lookup"><span data-stu-id="418f7-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="418f7-124">حدد خانة الاختيار "استخدم معالجة الدُفعة لتسوية ضريبة المبيعات‬" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="418f7-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="418f7-125">يمكن معالجة عملية التسوية لفترة التسوية كوظيفة دفعية في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="418f7-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="418f7-126">ينصح بهذا الأمر لعدد كبير من حركات ضريبة ضمن فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="418f7-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="418f7-127">حدد أو امسح منع إنشاء خانة الاختيار "منع إنشاء حركات الضرائب المقابلة‬".</span><span class="sxs-lookup"><span data-stu-id="418f7-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="418f7-128">بشكل افتراضي، يقوم النظام بإنشاء حركات الضرائب المقابلة‬ خلال عملية التسوية، مما يؤدي إلى حدوث مشكلات في الأداء في حال وجود عدد كبير من حركات الضريبة خلال فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="418f7-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="418f7-129">حدد خانة الاختيار لمنع إنشاء حركات الضرائب المقابلة.</span><span class="sxs-lookup"><span data-stu-id="418f7-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="418f7-130">وسّع علامة التبويب "الفترات الزمنية‬".</span><span class="sxs-lookup"><span data-stu-id="418f7-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="418f7-131">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="418f7-131">Click Add.</span></span>
17. <span data-ttu-id="418f7-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="418f7-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="418f7-133">في الحقل "من تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="418f7-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="418f7-134">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="418f7-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="418f7-135">انقر فوق "الفترة الزمنية الجديدة‬".</span><span class="sxs-lookup"><span data-stu-id="418f7-135">Click New period interval.</span></span>
    * <span data-ttu-id="418f7-136">بمجرد إدخال الفترة الزمنية الأولى، يمكن إنشاء فترات جديدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="418f7-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="418f7-137">ويمكنك العودة وإضافة فترات زمنية جديدة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="418f7-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="418f7-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="418f7-138">Close the page.</span></span>


