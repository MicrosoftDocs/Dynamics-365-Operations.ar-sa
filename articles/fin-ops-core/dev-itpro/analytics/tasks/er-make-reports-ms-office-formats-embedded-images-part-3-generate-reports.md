---
title: إنشاء تقارير بتنسيق Office تحتوي على صور مضمنة
description: تشرح الخطوات التالية كيف يمكن لمستخدم يؤدي دور "مسؤول النظام" أو "مطور التقارير الإلكترونية" تصميم تكوينات تقارير إلكترونية لإنشاء مستندات إلكترونية بتنسيقات MS office (مستندات Excel وWord) تحتوي على صور مضمنة.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64fade6578e9cd4f8a51c524e4f6ebbf63b93f20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184751"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="1507d-103">إنشاء تقارير بتنسيق Office تحتوي على صور مضمنة</span><span class="sxs-lookup"><span data-stu-id="1507d-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1507d-104">تشرح الخطوات التالية كيف يمكن لمستخدم يؤدي دور "مسؤول النظام" أو "مطور التقارير الإلكترونية" تصميم تكوينات تقارير إلكترونية لإنشاء مستندات إلكترونية بتنسيقات MS office (مستندات Excel وWord) تحتوي على صور مضمنة.</span><span class="sxs-lookup"><span data-stu-id="1507d-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="1507d-105">في هذا المثال، سوف تستخدم تكوينات التقارير الإلكترونية التي تم إنشاؤها لشركة نموذجية، وهي "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="1507d-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="1507d-106">لإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في دليل المهام "التقارير الإلكترونية - إنشاء تقارير بتنسيقات MS Office مع صور مضمنة (الجزء 2: مراجعات التكوينات)‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="1507d-107">يمكن تنفيذ هذه الخطوات في شركة "USMF".</span><span class="sxs-lookup"><span data-stu-id="1507d-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="1507d-108">تشغيل التنسيق مع تعيين النموذج الأولى</span><span class="sxs-lookup"><span data-stu-id="1507d-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="1507d-109">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="1507d-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="1507d-110">استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "USMF OPER''.</span><span class="sxs-lookup"><span data-stu-id="1507d-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="1507d-111">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="1507d-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="1507d-112">انقر فوق "تحقق".</span><span class="sxs-lookup"><span data-stu-id="1507d-112">Click Check.</span></span>
5. <span data-ttu-id="1507d-113">انقر فوق "اختبار الطباعة‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-113">Click Print test.</span></span>
    * <span data-ttu-id="1507d-114">قم بتشغيل التنسيق لأغراض الاختبار.</span><span class="sxs-lookup"><span data-stu-id="1507d-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="1507d-115">حدد "نعم" في حقل "تنسيق الشيك القابل للتداول‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="1507d-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1507d-116">Click OK.</span></span>
    * <span data-ttu-id="1507d-117">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="1507d-117">Review the created output.</span></span> <span data-ttu-id="1507d-118">لاحظ أنه يتم تقديم شعار الشركة في التقرير بالإضافة إلى توقيع الشخص المعتمد.</span><span class="sxs-lookup"><span data-stu-id="1507d-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="1507d-119">تؤخذ صورة التوقيع من حقل نوع البيانات "حاوية" لسجل تخطيط الشيك الذي يقترن بالحساب البنكي المحدد.</span><span class="sxs-lookup"><span data-stu-id="1507d-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="1507d-120">قم بتوسيع مقطع "النسخ‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="1507d-121">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="1507d-121">Click Edit.</span></span>
10. <span data-ttu-id="1507d-122">في الحقل "علامة مائية"، أدخل "طباعة العلامة المائية باعتبارها ملغية".</span><span class="sxs-lookup"><span data-stu-id="1507d-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="1507d-123">قم بتغيير إعداد تخطيط العلامة المائية لإظهار نص العلامة المائية في عملية إنشاء مستند في عنصر شكل في Excel.</span><span class="sxs-lookup"><span data-stu-id="1507d-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="1507d-124">انقر فوق "اختبار الطباعة‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-124">Click Print test.</span></span>
12. <span data-ttu-id="1507d-125">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1507d-125">Click OK.</span></span>
    * <span data-ttu-id="1507d-126">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="1507d-126">Review the created output.</span></span> <span data-ttu-id="1507d-127">لاحظ أن العلامة المائية تظهر في التقرير المنشأ وفقًا للخيار المحدد.</span><span class="sxs-lookup"><span data-stu-id="1507d-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="1507d-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-128">Close the page.</span></span>
14. <span data-ttu-id="1507d-129">في جزء الإجراءات‬، انقر فوق "إدارة المدفوعات‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="1507d-130">انقر فوق "الشيكات‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-130">Click Checks.</span></span>
16. <span data-ttu-id="1507d-131">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="1507d-131">Click Show filters.</span></span>
17. <span data-ttu-id="1507d-132">طبّق عوامل التصفية التالية: قم بإدخال قيمة عامل التصفية "381" أو "385" أو "389" في الحقل "رقم الشيك" باستخدام عامل التصفية "أحد ما يلي‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="1507d-133">في القائمة، ضع علامة تمييز أمام جميع الصفوف.</span><span class="sxs-lookup"><span data-stu-id="1507d-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="1507d-134">انقر فوق "طباعة نسخة الشيك".</span><span class="sxs-lookup"><span data-stu-id="1507d-134">Click Print check copy.</span></span>
    * <span data-ttu-id="1507d-135">قم بتشغيل التنسيق لإعادة طباعة الشيكات المحددة.</span><span class="sxs-lookup"><span data-stu-id="1507d-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="1507d-136">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="1507d-136">Review the created output.</span></span> <span data-ttu-id="1507d-137">لاحظ أنه قد تمت إعادة طباعة الشيكات المحددة.</span><span class="sxs-lookup"><span data-stu-id="1507d-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="1507d-138">لم تتم طباعة شعار الشركة وملصقاتها نظرًا لتقديمها في النموذج المطبوع مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1507d-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="1507d-139">تعديل تعيين نموذج البيانات المستورد</span><span class="sxs-lookup"><span data-stu-id="1507d-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="1507d-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-140">Close the page.</span></span>
2. <span data-ttu-id="1507d-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-141">Close the page.</span></span>
3. <span data-ttu-id="1507d-142">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="1507d-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="1507d-143">في الشجرة، حدد "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="1507d-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="1507d-144">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="1507d-144">Click Designer.</span></span>
6. <span data-ttu-id="1507d-145">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="1507d-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="1507d-146">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="1507d-146">Click Designer.</span></span>
    * <span data-ttu-id="1507d-147">سنقوم بتغيير ربط عنصر توقيع نموذج البيانات للحصول على صورة التوقيع من الملف الذي تم إرفاقه بالسجل تخطيط الشيك الذي يقترن بالحساب البنكي المحدد.</span><span class="sxs-lookup"><span data-stu-id="1507d-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="1507d-148">أوقف تشغيل إظهار التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="1507d-148">Turn Show details off.</span></span>
9. <span data-ttu-id="1507d-149">في الشجرة، قم بتوسيع "تخطيط".</span><span class="sxs-lookup"><span data-stu-id="1507d-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="1507d-150">في الشجرة، قم بتوسيع "تخطيط\توقيع".</span><span class="sxs-lookup"><span data-stu-id="1507d-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="1507d-151">في الشجرة، حدد "تخطيط\توقيع\صورة = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp".</span><span class="sxs-lookup"><span data-stu-id="1507d-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="1507d-152">في الشجرة، قم بتوسيع ''chequesaccount".</span><span class="sxs-lookup"><span data-stu-id="1507d-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="1507d-153">في الشجرة، قم بتوسيع "chequesaccount\<علاقات".</span><span class="sxs-lookup"><span data-stu-id="1507d-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="1507d-154">في الشجرة، قم بتوسيع "chequesaccount\<علاقات‏‎\BankChequeLayout".</span><span class="sxs-lookup"><span data-stu-id="1507d-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="1507d-155">في الشجرة، قم بتوسيع "chequesaccount\<علاقات\BankChequeLayout\<علاقات".</span><span class="sxs-lookup"><span data-stu-id="1507d-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="1507d-156">في الشجرة، قم بتوسيع "chequesaccount\<علاقات‏‎\BankChequeLayout\<علاقات\<مستندات".</span><span class="sxs-lookup"><span data-stu-id="1507d-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="1507d-157">في الشجرة، حدد "chequesaccount\<علاقات\BankChequeLayout\<علاقات\<مستندات‏‎\getFileContentAsContainer()".</span><span class="sxs-lookup"><span data-stu-id="1507d-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="1507d-158">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="1507d-158">Click Bind.</span></span>
19. <span data-ttu-id="1507d-159">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1507d-159">Click Save.</span></span>
20. <span data-ttu-id="1507d-160">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-160">Close the page.</span></span>
21. <span data-ttu-id="1507d-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-161">Close the page.</span></span>
22. <span data-ttu-id="1507d-162">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-162">Close the page.</span></span>
23. <span data-ttu-id="1507d-163">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="1507d-164">تشغيل التنسيق باستخدام تعيين النموذج المعدل</span><span class="sxs-lookup"><span data-stu-id="1507d-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="1507d-165">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="1507d-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="1507d-166">استخدم عامل التصفية السريع للبحث عن السجلات.</span><span class="sxs-lookup"><span data-stu-id="1507d-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1507d-167">على سبيل المثال، يمكنك إجراء التصفية على حقل "الحساب البنكي" بقيمة "USMF OPER".</span><span class="sxs-lookup"><span data-stu-id="1507d-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="1507d-168">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="1507d-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="1507d-169">انقر فوق "تحقق".</span><span class="sxs-lookup"><span data-stu-id="1507d-169">Click Check.</span></span>
5. <span data-ttu-id="1507d-170">انقر فوق "اختبار الطباعة‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-170">Click Print test.</span></span>
6. <span data-ttu-id="1507d-171">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1507d-171">Click OK.</span></span>
    * <span data-ttu-id="1507d-172">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="1507d-172">Review the created output.</span></span> <span data-ttu-id="1507d-173">لاحظ أنه يتم تقديم الصورة من المرفق "إدارة المستندات" كتوقيع شخص معتمد.</span><span class="sxs-lookup"><span data-stu-id="1507d-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="1507d-174">استخدام مستند MS Word كقالب في التنسيق المستورد</span><span class="sxs-lookup"><span data-stu-id="1507d-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="1507d-175">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-175">Close the page.</span></span>
2. <span data-ttu-id="1507d-176">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-176">Close the page.</span></span>
3. <span data-ttu-id="1507d-177">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="1507d-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="1507d-178">في الشجرة، قم بتوسيع "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="1507d-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="1507d-179">في الشجرة، حدد "نموذج للشيكات\تنسيق طباعة الشيكات".</span><span class="sxs-lookup"><span data-stu-id="1507d-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="1507d-180">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="1507d-180">Click Designer.</span></span>
7. <span data-ttu-id="1507d-181">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="1507d-181">Click Attachments.</span></span>
8. <span data-ttu-id="1507d-182">انقر فوق حذف.</span><span class="sxs-lookup"><span data-stu-id="1507d-182">Click Delete.</span></span>
9. <span data-ttu-id="1507d-183">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="1507d-183">Click Yes.</span></span>
10. <span data-ttu-id="1507d-184">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1507d-184">Click New.</span></span>
11. <span data-ttu-id="1507d-185">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="1507d-185">Click File.</span></span>
    * <span data-ttu-id="1507d-186">انقر فوق "استعراض" وحدد ملف "Cheque template Word.docx" الذي تم تنزيله مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1507d-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="1507d-187">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-187">Close the page.</span></span>
13. <span data-ttu-id="1507d-188">في حقل "القالب"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1507d-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="1507d-189">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1507d-189">Click Save.</span></span>
15. <span data-ttu-id="1507d-190">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-190">Close the page.</span></span>
16. <span data-ttu-id="1507d-191">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="1507d-191">Click Edit.</span></span>
17. <span data-ttu-id="1507d-192">حدد "نعم" في حقل "تشغيل المسودة‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="1507d-193">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1507d-193">Close the page.</span></span>
19. <span data-ttu-id="1507d-194">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="1507d-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="1507d-195">استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "USMF OPER''.</span><span class="sxs-lookup"><span data-stu-id="1507d-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="1507d-196">انقر فوق "تحقق".</span><span class="sxs-lookup"><span data-stu-id="1507d-196">Click Check.</span></span>
22. <span data-ttu-id="1507d-197">انقر فوق "اختبار الطباعة‬".</span><span class="sxs-lookup"><span data-stu-id="1507d-197">Click Print test.</span></span>
23. <span data-ttu-id="1507d-198">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="1507d-198">Click OK.</span></span>
    * <span data-ttu-id="1507d-199">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="1507d-199">Review the created output.</span></span> <span data-ttu-id="1507d-200">لاحظ أنه قد تم إنشاء المخرجات كمستند MS Word مع صور مضمنة تقدم شعار الشركة وتوقيع شخص معتمد والنص المحدد للعلامة المائية.</span><span class="sxs-lookup"><span data-stu-id="1507d-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

