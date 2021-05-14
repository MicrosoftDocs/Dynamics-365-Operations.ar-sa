---
title: إعداد فترات تسوية ضريبة المبيعات
description: يشرح هذا الموضوع كيفية إعداد ‏‫فترات تسوية ضريبة المبيعات‬ في Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944767"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="02ba7-103">إعداد فترات تسوية ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="02ba7-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02ba7-104">يشرح هذا الموضوع كيفية إعداد ‏‫فترات تسوية ضريبة المبيعات‬.</span><span class="sxs-lookup"><span data-stu-id="02ba7-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="02ba7-105">تحتوي فترات تسوية ضرائب المبيعات على معلومات عن الفترات الزمنية التي يجب خلالها الإبلاغ عن الضرائب ودفعها.</span><span class="sxs-lookup"><span data-stu-id="02ba7-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="02ba7-106">يمكن تشغيل عملية التسوية لفترة تسوية وفترة تاريخ محددة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="02ba7-107">وستتم تسوية كافة أكواد الضرائب المقترنة بفترة التسوية.</span><span class="sxs-lookup"><span data-stu-id="02ba7-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="02ba7-108">بالاستناد إلى إعداد هيئة ضريبة المبيعات ذات الصلة، يتم ترحيل الالتزام الضريبي إما إلى حساب مورّد أو حساب دفتر أستاذ عام.</span><span class="sxs-lookup"><span data-stu-id="02ba7-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="02ba7-109">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="02ba7-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="02ba7-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > فترات تسوية ضرائب المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="02ba7-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="02ba7-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="02ba7-111">Select **New**.</span></span>
3. <span data-ttu-id="02ba7-112">في الحقل **فترة التسوية‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="02ba7-113">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="02ba7-114">في الحقل **الهيئة‬**، حدد هيئة ضريبة المبيعات التي تستلم التقارير والمدفوعات التي يتم إنشاؤها لفترة التسوية.</span><span class="sxs-lookup"><span data-stu-id="02ba7-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="02ba7-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="02ba7-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="02ba7-116">في حقل **شروط الدفع**، حدد السجل المطلوب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="02ba7-117">يمكن إعداد هيئة ضريبة المبيعات ذات الصلة كمورّد، وستنشئ تسوية ضريبة المبيعات فاتورة مورّد مفتوحة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="02ba7-118">تحدد شروط الدفع تاريخ الاستحقاق الخاص بفاتورة المورّد المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="02ba7-119">حدد نوعًا للفترات الزمنية للتسوية.</span><span class="sxs-lookup"><span data-stu-id="02ba7-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="02ba7-120">أدخل عدد وحدات الفترة الزمنية لكل فترة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="02ba7-121">على سبيل المثال، يتكون ربع السنة من 3 أشهر.</span><span class="sxs-lookup"><span data-stu-id="02ba7-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="02ba7-122">حدد خانة الاختيار **استخدم معالجة الدُفعة لتسوية ضريبة المبيعات‬** أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="02ba7-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="02ba7-123">يمكن معالجة عملية التسوية لفترة التسوية كوظيفة دفعية في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="02ba7-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="02ba7-124">ينصح بهذا الأمر لعدد كبير من حركات ضريبة ضمن فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="02ba7-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="02ba7-125">حدد خانة الاختيار **منع إنشاء حركات الضرائب المقابلة‬** أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="02ba7-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="02ba7-126">بشكل افتراضي، يقوم النظام بإنشاء حركات الضرائب المقابلة‬ خلال عملية التسوية، مما يؤدي إلى حدوث مشكلات في الأداء في حال وجود عدد كبير من حركات الضريبة خلال فترة زمنية.</span><span class="sxs-lookup"><span data-stu-id="02ba7-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="02ba7-127">حدد خانة الاختيار لمنع إنشاء حركات الضرائب المقابلة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="02ba7-128">وسّع علامة التبويب **الفترات الزمنية**.</span><span class="sxs-lookup"><span data-stu-id="02ba7-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="02ba7-129">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="02ba7-129">Select **Add**.</span></span>
14. <span data-ttu-id="02ba7-130">أدخل تاريخًا في الحقل **من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="02ba7-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="02ba7-131">في الحقل **إلى تاريخ**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="02ba7-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="02ba7-132">حدد **الفترة الزمنية الجديدة**.</span><span class="sxs-lookup"><span data-stu-id="02ba7-132">Select **New period interval**.</span></span> <span data-ttu-id="02ba7-133">بمجرد إدخال الفترة الزمنية الأولى، يمكن إنشاء فترات جديدة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="02ba7-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="02ba7-134">ويمكنك العودة وإضافة فترات زمنية جديدة كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="02ba7-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="02ba7-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="02ba7-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
