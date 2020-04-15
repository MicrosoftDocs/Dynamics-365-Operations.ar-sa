---
title: تعمل التقارير الإلكترونية على إنشاء التقارير الإلكترونية للدفعات باستخدام تكوين التنسيق
description: تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية استخدام تكوين تنسيق تقارير إلكترونية جديد يحتوي على نموذج بيانات لإنشاء مستندات الدفع الإلكتروني لمعالجة الدفعات.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fa39a9d459022e391f99e284d41d82215cc10e2b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142560"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="974c3-103">تعمل التقارير الإلكترونية على إنشاء التقارير الإلكترونية للدفعات باستخدام تكوين التنسيق</span><span class="sxs-lookup"><span data-stu-id="974c3-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="974c3-104">تشرح الخطوات التالية كيف يمكن لمستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية استخدام تكوين تنسيق تقارير إلكترونية جديد يحتوي على نموذج بيانات لإنشاء مستندات الدفع الإلكتروني لمعالجة الدفعات.</span><span class="sxs-lookup"><span data-stu-id="974c3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="974c3-105">يمكن تنفيذ هذه الخطوات في عينة شركة GBSI.</span><span class="sxs-lookup"><span data-stu-id="974c3-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="974c3-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء تكوين بتنسيق مستند الدفع".</span><span class="sxs-lookup"><span data-stu-id="974c3-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="974c3-107">تغيير تكوين أسلوب الدفع الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="974c3-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="974c3-108">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="974c3-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="974c3-109">قم بالتبديل بين مقطع تنسيق الملف لتوسيعه، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="974c3-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="974c3-110">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="974c3-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="974c3-111">على سبيل المثال، قم بإجراء التصفية على الحقل "طريقة الدفع" بقيمة "إلكتروني".</span><span class="sxs-lookup"><span data-stu-id="974c3-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="974c3-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="974c3-112">Click Edit.</span></span>
5. <span data-ttu-id="974c3-113">قم بتعيين الحقل "التقارير الإلكترونية العامة" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="974c3-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="974c3-114">حدد "نعم" لاستخدام نمط التقارير الإلكترونية العامة لإنشاء ملفات الدفعات.</span><span class="sxs-lookup"><span data-stu-id="974c3-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="974c3-115">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="974c3-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="974c3-116">حدد تكوين تنسيق BACS (وهمي في المملكة المتحدة).</span><span class="sxs-lookup"><span data-stu-id="974c3-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="974c3-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="974c3-117">Click Save.</span></span>
9. <span data-ttu-id="974c3-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="974c3-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="974c3-119">اختبار تنسيق ملفات الدفع الذي تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="974c3-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="974c3-120">انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="974c3-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="974c3-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="974c3-121">Click New.</span></span>
3. <span data-ttu-id="974c3-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="974c3-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="974c3-123">في الحقل "الاسم"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="974c3-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="974c3-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="974c3-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="974c3-125">حدد VendPay.</span><span class="sxs-lookup"><span data-stu-id="974c3-125">Select VendPay.</span></span>  
6. <span data-ttu-id="974c3-126">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="974c3-126">Click Save.</span></span>
7. <span data-ttu-id="974c3-127">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="974c3-127">Click Lines.</span></span>
8. <span data-ttu-id="974c3-128">في الحقل "الشركة"، اكتب "DEMF".</span><span class="sxs-lookup"><span data-stu-id="974c3-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="974c3-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="974c3-129">DEMF</span></span>  
9. <span data-ttu-id="974c3-130">في حقل الحساب، حدد قيم "DE-01001".</span><span class="sxs-lookup"><span data-stu-id="974c3-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="974c3-131">DE - 01001</span><span class="sxs-lookup"><span data-stu-id="974c3-131">DE-01001</span></span>  
10. <span data-ttu-id="974c3-132">في حقل "الوصف"، اكتب "الدفع".</span><span class="sxs-lookup"><span data-stu-id="974c3-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="974c3-133">المدفوعات</span><span class="sxs-lookup"><span data-stu-id="974c3-133">Payment</span></span>  
11. <span data-ttu-id="974c3-134">في الحقل "مدين"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="974c3-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="974c3-135">1000</span><span class="sxs-lookup"><span data-stu-id="974c3-135">1000</span></span>  
12. <span data-ttu-id="974c3-136">انقر فوق علامة التبويب "الدفع".</span><span class="sxs-lookup"><span data-stu-id="974c3-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="974c3-137">في الحقل "طريقة الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="974c3-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="974c3-138">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="974c3-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="974c3-139">حدد القيمة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="974c3-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="974c3-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="974c3-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="974c3-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="974c3-141">Click Save.</span></span>
17. <span data-ttu-id="974c3-142">انقر فوق إنشاء مدفوعات.</span><span class="sxs-lookup"><span data-stu-id="974c3-142">Click Generate payments.</span></span>
18. <span data-ttu-id="974c3-143">في الحقل "طريقة الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="974c3-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="974c3-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="974c3-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="974c3-145">حدد القيمة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="974c3-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="974c3-146">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="974c3-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="974c3-147">حدد القيمة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="974c3-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="974c3-148">في حقل "اسم الملف"، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="974c3-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="974c3-149">على سبيل المثال، اكتب "دفعات".</span><span class="sxs-lookup"><span data-stu-id="974c3-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="974c3-150">في الحقل "الحساب البنكي"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="974c3-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="974c3-151">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="974c3-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="974c3-152">حدد القيمة GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="974c3-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="974c3-153">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="974c3-153">Click OK.</span></span>
25. <span data-ttu-id="974c3-154">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="974c3-154">Click OK.</span></span>
    * <span data-ttu-id="974c3-155">حلل ملف الدفع الذي تم إنشاؤه بتنسيق XML.</span><span class="sxs-lookup"><span data-stu-id="974c3-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="974c3-156">قارنه بمخطط المستند المصمم وحدد سمات حركة الدفع.</span><span class="sxs-lookup"><span data-stu-id="974c3-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

