---
title: إعداد تنسيق إيصال دفع لفواتير المشروع
description: تربط الشركات عمومًا إيصالات الدفع المطبو عة بالفواتير لمساعدة العملاء وتوفير مرجع دفع للترحيل والتسوية.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4671e1df3bc86361736b5882d67e6b160b4c5644
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174743"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a><span data-ttu-id="255d8-103">إعداد تنسيق إيصال دفع لفواتير المشروع</span><span class="sxs-lookup"><span data-stu-id="255d8-103">Set up payment slip format for project invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="255d8-104">تربط الشركات عمومًا إيصالات الدفع المطبو عة بالفواتير لمساعدة العملاء وتوفير مرجع دفع للترحيل والتسوية.</span><span class="sxs-lookup"><span data-stu-id="255d8-104">Businesses commonly attach printed payment slips to invoices to assist customers and provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="255d8-105">ويمكن استخدام قسيمة الدفع لفواتير المشروع أو الخدمة، وخطابات التحصيل، وإشعارات الفائدة، وكشوف الحسابات، بالإضافة إلى فواتير المبيعات، وفواتير النص الحر.</span><span class="sxs-lookup"><span data-stu-id="255d8-105">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span> <span data-ttu-id="255d8-106">لمعالجة إيصالات الدفع، قم أولاً بإعداد تنسيقات إرفاق إيصالات الدفع ورقم تعريف الدائن.</span><span class="sxs-lookup"><span data-stu-id="255d8-106">To process payment slips, first set up your creditor identification number and payment slip attachment formats.</span></span>

<span data-ttu-id="255d8-107">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="255d8-107">This procedure uses the DEMF demo company.</span></span> 

<span data-ttu-id="255d8-108">تتوفر هذه الوظيفة للكيانات القانونية التي يوجد عنوانها الرئيسي في الدنمارك.</span><span class="sxs-lookup"><span data-stu-id="255d8-108">This functionality is available for legal entities whose primary address is in Denmark.</span></span>


## <a name="set-up-a-creditor-id-number"></a><span data-ttu-id="255d8-109">إعداد رقم معرف الدائن</span><span class="sxs-lookup"><span data-stu-id="255d8-109">Set up a creditor ID number</span></span>
1. <span data-ttu-id="255d8-110">انتقل إلى إدارة المؤسسة > المؤسسات > الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="255d8-110">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="255d8-111">‏‫قم بتوسيع المقطع "معلومات الحساب البنكي‬" أو طيّه.</span><span class="sxs-lookup"><span data-stu-id="255d8-111">Expand or collapse the Bank account information section.</span></span>
3. <span data-ttu-id="255d8-112">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="255d8-112">Click Edit.</span></span>
4. <span data-ttu-id="255d8-113">في حقل "‏‫معرّف المؤسسة المالية الدائنة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="255d8-113">In the FI-Creditor ID field, type a value.</span></span>
5. <span data-ttu-id="255d8-114">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="255d8-114">Click Save.</span></span>
6. <span data-ttu-id="255d8-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="255d8-115">Close the page.</span></span>

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a><span data-ttu-id="255d8-116">إعداد تنسيق إيصال دفع للفواتير والإشعارات والخطابات والكشوف</span><span class="sxs-lookup"><span data-stu-id="255d8-116">Set up a payment slip format for invoices, notes, letters, and statements</span></span>
1. <span data-ttu-id="255d8-117">انتقل إلى الحسابات المدينة > إعداد > النماذج > إعداد النموذج.</span><span class="sxs-lookup"><span data-stu-id="255d8-117">Go to Accounts receivable > Setup > Forms > Form setup.</span></span>
2. <span data-ttu-id="255d8-118">انقر فوق علامة التبويب "الفاتورة".</span><span class="sxs-lookup"><span data-stu-id="255d8-118">Click the Invoice tab.</span></span>
3. <span data-ttu-id="255d8-119">في حقل "‏‫مرفق الدفع المقترن في فاتورة العميل‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-119">In the Associated payment attachment on customer invoice field, select an option.</span></span>
    * <span data-ttu-id="255d8-120">بلا - عدم طباعة إيصال الدفع.</span><span class="sxs-lookup"><span data-stu-id="255d8-120">None – Do not print a payment slip.</span></span> <span data-ttu-id="255d8-121">حدد هذا الخيار إذا كان مبلغ الدفع بعملة أخرى غير الكرونة الدانمركية (DKK).</span><span class="sxs-lookup"><span data-stu-id="255d8-121">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="255d8-122">FIK 751 – قم بطباعة إيصال دفع FIK 751 إذا كنت تنوي كتابة مبلغ الدفع وتاريخ الاستحقاق في إيصال الدفع يدويًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-122">FIK 751 – Print an FIK 751 payment slip if you intend to manually write the payment amount and due date on the payment slip.</span></span>   <span data-ttu-id="255d8-123">FIK 752 – حدد إيصال الدفع FIK 752 إذا كنت تنوي استخدام إيصال دفع يتم إنشاؤه بواسطة جهاز الكمبيوتر والذي لديه مبلغ دفع وتاريخ استحقاق مطبوعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-123">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
4. <span data-ttu-id="255d8-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="255d8-124">Click Save.</span></span>
5. <span data-ttu-id="255d8-125">انقر فوق علامة التبويب "‏‫فاتورة نص حر".</span><span class="sxs-lookup"><span data-stu-id="255d8-125">Click the Free text invoice tab.</span></span>
6. <span data-ttu-id="255d8-126">في حقل "‏‫‏‫مرفق الدفع المقترن في فاتورة النص الحر‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-126">In the Associated payment attachment on free text invoice field, select an option.</span></span>
    * <span data-ttu-id="255d8-127">بلا - عدم طباعة إيصال الدفع.</span><span class="sxs-lookup"><span data-stu-id="255d8-127">None – Do not print a payment slip.</span></span> <span data-ttu-id="255d8-128">حدد هذا الخيار إذا كان مبلغ الدفع بعملة أخرى غير الكرونة الدانمركية (DKK).</span><span class="sxs-lookup"><span data-stu-id="255d8-128">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="255d8-129">FIK 751 – قم بطباعة إيصال دفع FIK 751 إذا كنت تنوي كتابة مبلغ الدفع وتاريخ الاستحقاق في إيصال الدفع يدويًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-129">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="255d8-130">FIK 752 – حدد إيصال الدفع FIK 752 إذا كنت تنوي استخدام إيصال دفع يتم إنشاؤه بواسطة جهاز الكمبيوتر والذي لديه مبلغ دفع وتاريخ استحقاق مطبوعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-130">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
7. <span data-ttu-id="255d8-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="255d8-131">Click Save.</span></span>
8. <span data-ttu-id="255d8-132">انقر فوق علامة التبويب "إشعار الفائدة".</span><span class="sxs-lookup"><span data-stu-id="255d8-132">Click the Interest note tab.</span></span>
9. <span data-ttu-id="255d8-133">في حقل "‏‫‏‫مرفق الدفع المقترن في إشعار الفائدة‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-133">In the Associated payment attachment on interest note field, select an option.</span></span>
    * <span data-ttu-id="255d8-134">بلا - عدم طباعة إيصال الدفع.</span><span class="sxs-lookup"><span data-stu-id="255d8-134">None – Do not print a payment slip.</span></span> <span data-ttu-id="255d8-135">حدد هذا الخيار إذا كان مبلغ الدفع بعملة أخرى غير الكرونة الدانمركية (DKK).</span><span class="sxs-lookup"><span data-stu-id="255d8-135">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="255d8-136">FIK 751 – قم بطباعة إيصال دفع FIK 751 إذا كنت تنوي كتابة مبلغ الدفع وتاريخ الاستحقاق في إيصال الدفع يدويًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-136">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="255d8-137">FIK 752 – حدد إيصال الدفع FIK 752 إذا كنت تنوي استخدام إيصال دفع يتم إنشاؤه بواسطة جهاز الكمبيوتر والذي لديه مبلغ دفع وتاريخ استحقاق مطبوعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-137">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
10. <span data-ttu-id="255d8-138">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="255d8-138">Click Save.</span></span>
11. <span data-ttu-id="255d8-139">انقر فوق علامة التبويب "‏‫خطاب التحصيل‬".</span><span class="sxs-lookup"><span data-stu-id="255d8-139">Click the Collection letter tab.</span></span>
12. <span data-ttu-id="255d8-140">في حقل "‏‫‏‫‏‫مرفق الدفع المقترن في خطاب التحصيل‬‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-140">In the Associated payment attachment on collection letter field, select an option.</span></span>
    * <span data-ttu-id="255d8-141">بلا - عدم طباعة إيصال الدفع.</span><span class="sxs-lookup"><span data-stu-id="255d8-141">None – Do not print a payment slip.</span></span> <span data-ttu-id="255d8-142">حدد هذا الخيار إذا كان مبلغ الدفع بعملة أخرى غير الكرونة الدانمركية (DKK).</span><span class="sxs-lookup"><span data-stu-id="255d8-142">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="255d8-143">FIK 751 – قم بطباعة إيصال دفع FIK 751 إذا كنت تنوي كتابة مبلغ الدفع وتاريخ الاستحقاق في إيصال الدفع يدويًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-143">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="255d8-144">FIK 752 – حدد إيصال الدفع FIK 752 إذا كنت تنوي استخدام إيصال دفع يتم إنشاؤه بواسطة جهاز الكمبيوتر والذي لديه مبلغ دفع وتاريخ استحقاق مطبوعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-144">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
13. <span data-ttu-id="255d8-145">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="255d8-145">Click Save.</span></span>
14. <span data-ttu-id="255d8-146">انقر فوق علامة التبويب "كشف الحساب".</span><span class="sxs-lookup"><span data-stu-id="255d8-146">Click the Account statement tab.</span></span>
15. <span data-ttu-id="255d8-147">في حقل "‏‫‏‫‏‫‏‫مرفق الدفع المقترن في كشف الحسابات‬‬‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-147">In the Associated payment attachment on account statement field, select an option.</span></span>
    * <span data-ttu-id="255d8-148">بلا - عدم طباعة إيصال الدفع.</span><span class="sxs-lookup"><span data-stu-id="255d8-148">None – Do not print a payment slip.</span></span> <span data-ttu-id="255d8-149">حدد هذا الخيار إذا كان مبلغ الدفع بعملة أخرى غير الكرونة الدانمركية (DKK).</span><span class="sxs-lookup"><span data-stu-id="255d8-149">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="255d8-150">FIK 751 – قم بطباعة إيصال دفع FIK 751 إذا كنت تنوي كتابة مبلغ الدفع وتاريخ الاستحقاق في إيصال الدفع يدويًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-150">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="255d8-151">FIK 752 – حدد إيصال الدفع FIK 752 إذا كنت تنوي استخدام إيصال دفع يتم إنشاؤه بواسطة جهاز الكمبيوتر والذي لديه مبلغ دفع وتاريخ استحقاق مطبوعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="255d8-151">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
16. <span data-ttu-id="255d8-152">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="255d8-152">Click Save.</span></span>
17. <span data-ttu-id="255d8-153">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="255d8-153">Close the page.</span></span>

