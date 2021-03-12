---
title: إعداد سياسات فواتير المورِّدين
description: يصف هذا الموضوع كيفية إعداد سياسات فواتير المورِّدين‬.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995433"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="cc2d1-103">إعداد سياسات فواتير المورِّدين</span><span class="sxs-lookup"><span data-stu-id="cc2d1-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc2d1-104">يصف هذا الموضوع كيفية إعداد سياسات فواتير المورِّدين‬.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="cc2d1-105">يتم تشغيل سياسات فاتورة المورّد عند ترحيل فاتورة مورّد باستخدام صفحة "فاتورة المورّد" وعند فتح صفحة "مخالفات سياسة فاتورة المورّد"‬.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="cc2d1-106">يمكنك أيضًا تكوين سير عمل فاتورة المورّد لتشغيل سياسات فواتير المورّدين في كل وقت تقوم فيه بإرسال فاتورة إلى سير العمل.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="cc2d1-107">لا تنطبق سياسات فواتير المورّدين على الفواتير التي تم إنشاؤها في سجل الفواتير‬ أو دفتر يومية الفواتير‬.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="cc2d1-108">لا تستخدم عملية التحقق من مطابقة الفاتورة سياسات فواتير المورِّدين‬، ولكن يتم إعدادها بدلاً من ذلك في صفحة "محددات الحسابات الدائنة‬".</span><span class="sxs-lookup"><span data-stu-id="cc2d1-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="cc2d1-109">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="cc2d1-110">قد ينفذ دور مدير الحسابات الدائنة أو دور مدير الحسابات‬ هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="cc2d1-111">قبل أن تبدأ، تأكد من تحديد مفتاح تكوين مطابقة الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="cc2d1-112">التحضير لإنشاء سياسات فواتير المورّدين</span><span class="sxs-lookup"><span data-stu-id="cc2d1-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="cc2d1-113">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > الإعداد > معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="cc2d1-114">حدد علامة التبويب **التحقق من صحة الفواتير**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="cc2d1-115">حدد أو امسح خانة الاختيار **التحديث التلقائي لحالة رأس الفاتورة**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="cc2d1-116">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-116">Select **OK**.</span></span>
5. <span data-ttu-id="cc2d1-117">في الحقل **ترحيل الفاتورة التي بها اختلافات**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="cc2d1-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-118">Close the page.</span></span>
7. <span data-ttu-id="cc2d1-119">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > إعداد السياسة > سياسات فواتير المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="cc2d1-120">حدد **معلمات**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="cc2d1-121">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-121">Select **Add**.</span></span>
10. <span data-ttu-id="cc2d1-122">عد إلى الصفحة الرئيسية بعد إغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="cc2d1-123">إنشاء أنواع قواعد سياسات لفواتير المورّدين</span><span class="sxs-lookup"><span data-stu-id="cc2d1-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="cc2d1-124">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > إعداد السياسة > أنواع قواعد سياسات فواتير المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="cc2d1-125">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-125">Select **New**.</span></span>
3. <span data-ttu-id="cc2d1-126">اكتب قيمًا في حقلي **اسم القاعدة** و **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="cc2d1-127">في الحقل **اسم الاستعلام**، حدد زر القائمة المنسدلة لفتح البحث، ثم حدد السجل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="cc2d1-128">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-128">Select **Save**.</span></span>
6. <span data-ttu-id="cc2d1-129">عد إلى الصفحة الرئيسية بعد إغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="cc2d1-130">تعريف سياسة فاتورة المورّد</span><span class="sxs-lookup"><span data-stu-id="cc2d1-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="cc2d1-131">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات الدائنة > إعداد السياسة > سياسات فواتير المورّدين**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="cc2d1-132">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-132">Select **New**.</span></span>
3. <span data-ttu-id="cc2d1-133">اكتب قيمًا في حقلي **الاسم** و **الوصف**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="cc2d1-134">قم بتوسيع المقطع **مؤسسات السياسات** أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="cc2d1-135">في الشجرة، حدد **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="cc2d1-136">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-136">Select **Add**.</span></span>
7. <span data-ttu-id="cc2d1-137">قم بتوسيع المقطع **قواعد السياسة‬** أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="cc2d1-138">حدد **إنشاء قاعدة السياسة**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="cc2d1-139">في الحقل **وصف قاعدة السياسة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="cc2d1-140">حدد **عامل تصفية**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-140">Select **Filter**.</span></span>
11. <span data-ttu-id="cc2d1-141">حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-141">Select **Add**.</span></span> <span data-ttu-id="cc2d1-142">حدد السجل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-142">Select the desired record.</span></span>
12. <span data-ttu-id="cc2d1-143">في حقول **الجدول** و **الجدول المشتق** و **الحقل**، حدد خيارات أو أدخلها من القوائم المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="cc2d1-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-144">Close the page.</span></span>
14. <span data-ttu-id="cc2d1-145">في الحقل **المعايير**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="cc2d1-146">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-146">Select **OK**.</span></span>
16. <span data-ttu-id="cc2d1-147">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-147">Select **OK**.</span></span>
17. <span data-ttu-id="cc2d1-148">عد إلى الصفحة الرئيسية بعد إغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="cc2d1-148">Close the pages to return to the home page.</span></span>

