---
title: مراجعة التكوينات لإنشاء تقارير بتنسيق Office تحتوي على صور مضمنة
description: يصف هذا الموضوع كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستندات تتضمن صورًا مضمنة. (جزء 1 - إعداد المعلمات).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eee6300350dd96c34f2eab44704d1895e6171ff
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093635"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="8536f-104">مراجعة التكوينات لإنشاء تقارير بتنسيق Office تحتوي على صور مضمنة</span><span class="sxs-lookup"><span data-stu-id="8536f-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8536f-105">لإكمال هذه الخطوات، يجب عليك أولاً إكمال الخطوات المذكورة في دليل المهام "التقارير الإلكترونية - إنشاء تقارير بتنسيقات MS Office مع صور مضمنة (الجزء 1 - إعداد المعلمات)‬".</span><span class="sxs-lookup"><span data-stu-id="8536f-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="8536f-106">يظهر هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية (ER) لإنشاء مستندات إلكترونية تحتوي على صور مضمنة في Microsoft Excel وMicrosoft Word.</span><span class="sxs-lookup"><span data-stu-id="8536f-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="8536f-107">في هذا المثال، سوف تقوم بمراجعة تكوينات التقارير الإلكترونية للشركة النموذجية "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="8536f-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="8536f-108">تم تخصيص هذا الإجراء للمستخدمين الذين تم تعيين دور مسؤول النظام أو مطور التقارير الإلكترونية لهم.</span><span class="sxs-lookup"><span data-stu-id="8536f-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="8536f-109">يمكن إتمام الخطوات باستخدام مجموعة بيانات USMF.</span><span class="sxs-lookup"><span data-stu-id="8536f-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="8536f-110">مراجعة نموذج البيانات المستورد</span><span class="sxs-lookup"><span data-stu-id="8536f-110">Review the imported data model</span></span>
1. <span data-ttu-id="8536f-111">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="8536f-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8536f-112">في الشجرة، حدد "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="8536f-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="8536f-113">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="8536f-113">Click Designer.</span></span>
    * <span data-ttu-id="8536f-114">تم تصميم هذا النموذج لتقديم شيكات الدفع من وجهة الأعمال وتعيين هذا الطراز إلى مصادر البيانات الخاصة بالتطبيق.</span><span class="sxs-lookup"><span data-stu-id="8536f-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="8536f-115">قم بمراجعة هذا النموذج عن طريق مصمم عمليات إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8536f-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="8536f-116">لاحظ السمات الخاصة بعناصر النموذج التي يتم تقديمها: البنية والاسم والوصف ونوع البيانات، وهكذا.</span><span class="sxs-lookup"><span data-stu-id="8536f-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="8536f-117">في الشجرة، قم بتوسيع "جذر".</span><span class="sxs-lookup"><span data-stu-id="8536f-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="8536f-118">في الشجرة ، حدد "جذر\شيكات".</span><span class="sxs-lookup"><span data-stu-id="8536f-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="8536f-119">في الشجرة، قم بتوسيع "جذر\شيكات".</span><span class="sxs-lookup"><span data-stu-id="8536f-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="8536f-120">في الشجرة، قم بتوسيع جذر\شيكات\سمات".</span><span class="sxs-lookup"><span data-stu-id="8536f-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="8536f-121">في الشجرة، قم بتوسيع "جذر\دافع".</span><span class="sxs-lookup"><span data-stu-id="8536f-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="8536f-122">في الشجرة، حدد "جذر\istestrun".</span><span class="sxs-lookup"><span data-stu-id="8536f-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="8536f-123">في الشجرة، حدد "جذر\تخطيط".</span><span class="sxs-lookup"><span data-stu-id="8536f-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="8536f-124">يمثل عنصر التخطيط لهذا النموذج التفاصيل الخاصة بتخطيط نموذج طباعة الشيكات للحساب البنكي المحدد.</span><span class="sxs-lookup"><span data-stu-id="8536f-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="8536f-125">ويتضمن أيضًا عقدتين لنوع بيانات "الحاوية" لتخزين الصور.</span><span class="sxs-lookup"><span data-stu-id="8536f-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="8536f-126">في الشجرة، قم بتوسيع "جذر\تخطيط".</span><span class="sxs-lookup"><span data-stu-id="8536f-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="8536f-127">في الشجرة، حدد "جذر\تخطيط\شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="8536f-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="8536f-128">في الشجرة، قم بتوسيع "جذر\تخطيط\شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="8536f-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="8536f-129">في الشجرة، حدد "جذر\تخطيط\شعار الشركة\صورة".</span><span class="sxs-lookup"><span data-stu-id="8536f-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="8536f-130">في الشجرة، حدد "جذر\تخطيط\شعار الشركة\isprinted".</span><span class="sxs-lookup"><span data-stu-id="8536f-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="8536f-131">في الشجرة، حدد "جذر\تخطيط\توقيع".</span><span class="sxs-lookup"><span data-stu-id="8536f-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="8536f-132">في الشجرة، قم بتوسيع "جذر\تخطيط\توقيع".</span><span class="sxs-lookup"><span data-stu-id="8536f-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="8536f-133">في الشجرة، حدد "جذر\تخطيط\توقيع\صورة".</span><span class="sxs-lookup"><span data-stu-id="8536f-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="8536f-134">في الشجرة، حدد "جذر\تخطيط\توقيع\isprinted".</span><span class="sxs-lookup"><span data-stu-id="8536f-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="8536f-135">لاحظ أنه تم ربط عنصرين من عناصر نموذج بيانات الصورة بحقول الجداول التي تحتوي على صور لشعار الشركة وتوقيع الشخص المعتمد بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="8536f-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="8536f-136">في الشجرة، قم بتوسيع "جذر\تخطيط\علامة مائية".</span><span class="sxs-lookup"><span data-stu-id="8536f-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="8536f-137">انقر فوق "تعيين النموذج لمصدر البيانات".</span><span class="sxs-lookup"><span data-stu-id="8536f-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="8536f-138">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="8536f-138">Click Designer.</span></span>
23. <span data-ttu-id="8536f-139">في الشجرة، قم بتوسيع "chequesselected".</span><span class="sxs-lookup"><span data-stu-id="8536f-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="8536f-140">في الشجرة، قم بتوسيع "تخطيط".</span><span class="sxs-lookup"><span data-stu-id="8536f-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="8536f-141">في الشجرة، قم بتوسيع "تخطيط\شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="8536f-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="8536f-142">في الشجرة، قم بتوسيع "تخطيط\توقيع".</span><span class="sxs-lookup"><span data-stu-id="8536f-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="8536f-143">في الشجرة، قم بتوسيع "تخطيط\علامة مائية".</span><span class="sxs-lookup"><span data-stu-id="8536f-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="8536f-144">بدّل زر "إظهار التفاصيل" إلى وضع التشغيل.</span><span class="sxs-lookup"><span data-stu-id="8536f-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="8536f-145">لاحظ أن عنصر نموذج بيانات الشيكات مرتبط بجدول TmpChequePrintout الذي سوف يحتوي، في وقت التشغيل، على سجلات للشيكات التي حددها المستخدم للطباعة.</span><span class="sxs-lookup"><span data-stu-id="8536f-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="8536f-146">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8536f-146">Close the page.</span></span>
30. <span data-ttu-id="8536f-147">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8536f-147">Close the page.</span></span>
31. <span data-ttu-id="8536f-148">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8536f-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="8536f-149">مراجعة التنسيق المستورد</span><span class="sxs-lookup"><span data-stu-id="8536f-149">Review the imported format</span></span>
1. <span data-ttu-id="8536f-150">في الشجرة، قم بتوسيع "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="8536f-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="8536f-151">في الشجرة، حدد "نموذج للشيكات\تنسيق طباعة الشيكات".</span><span class="sxs-lookup"><span data-stu-id="8536f-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="8536f-152">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="8536f-152">Click Designer.</span></span>
4. <span data-ttu-id="8536f-153">انقر فوق "المرفقات".</span><span class="sxs-lookup"><span data-stu-id="8536f-153">Click Attachments.</span></span>
5. <span data-ttu-id="8536f-154">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="8536f-154">Click Open.</span></span>
    * <span data-ttu-id="8536f-155">افتح قالب التقرير المرفق في Excel.</span><span class="sxs-lookup"><span data-stu-id="8536f-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="8536f-156">قم بمراجعة قالب Excel للتقرير المرفق الذي سيتم استخدامه لطباعة الشيكات.</span><span class="sxs-lookup"><span data-stu-id="8536f-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="8536f-157">يحتوي القالب على اثنين من الشيكات في الصفحة، وهو مصمم لطباعة الشيكات على النموذج المطبوع مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="8536f-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="8536f-158">لاحظ أنه تم تضمين صورتين فارغتين.</span><span class="sxs-lookup"><span data-stu-id="8536f-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="8536f-159">الصورتان الفارغتان هما لشعار الشركة وتوقيع الشخص الذي يخول الدفع.</span><span class="sxs-lookup"><span data-stu-id="8536f-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="8536f-160">تحقق من أن أسماء الصور هي CompLogo وSignatureImage، على التوالي، في Excel.</span><span class="sxs-lookup"><span data-stu-id="8536f-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="8536f-161">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8536f-161">Close the page.</span></span>
7. <span data-ttu-id="8536f-162">في الشجرة، قم بتوسيع ''تقرير".</span><span class="sxs-lookup"><span data-stu-id="8536f-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="8536f-163">في الشجرة، قم بتوسيع "تقرير\ChequeLines".</span><span class="sxs-lookup"><span data-stu-id="8536f-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="8536f-164">في الشجرة، حدد "تقرير\ChequeLines\CompLogo".</span><span class="sxs-lookup"><span data-stu-id="8536f-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="8536f-165">بدّل زر "إظهار التفاصيل" إلى وضع التشغيل.</span><span class="sxs-lookup"><span data-stu-id="8536f-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="8536f-166">لاحظ أن عنصر خلية التنسيق 'CompLogo' يمثل عنصر Excel المستخدم لتعبئة صورة شعار الشركة في التقرير.</span><span class="sxs-lookup"><span data-stu-id="8536f-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="8536f-167">يرتبط عنصر التنسيق هذا بعنصر نموذج بيانات الصورة الذي يحتوي، في وقت التشغيل، على صورة شعار الشركة بتنسيق ثنائي.</span><span class="sxs-lookup"><span data-stu-id="8536f-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="8536f-168">انقر فوق علامة التبويب "التعيين".</span><span class="sxs-lookup"><span data-stu-id="8536f-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="8536f-169">انقر فوق "تم تمكين ‏‏التحرير".</span><span class="sxs-lookup"><span data-stu-id="8536f-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="8536f-170">لاحظ أنه يمكنك جعل عنصر خلية التنسيق "CompLogo" بحيث لن يعود ممكّنًا.</span><span class="sxs-lookup"><span data-stu-id="8536f-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="8536f-171">في هذه الحالة، سيقوم عنصر صورة Excel المرتبط بإخفاء شعار الشركة في التقرير الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="8536f-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="8536f-172">إذا قام التعبير الممكّن بإرجاع TRUE ولم يظهر الرابط المحدد أية صورة، فسيبين عنصر صورة Excel المقترن صورة تم حفظها في قالب Excel.</span><span class="sxs-lookup"><span data-stu-id="8536f-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="8536f-173">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8536f-173">Close the page.</span></span>
14. <span data-ttu-id="8536f-174">في الشجرة، قم بتوسيع "تسميات: حاوية".</span><span class="sxs-lookup"><span data-stu-id="8536f-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="8536f-175">سيتم تضمين بعض التسميات التي تظهر في نموذج الشيك المطبوع مسبقًا في التقرير عند إنشائه لأغراض الاختبار.</span><span class="sxs-lookup"><span data-stu-id="8536f-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="8536f-176">ومع ذلك، لن تتم طباعته هذه التسميات أثناء الطباعة الحقيقية، لأن النموذج المطبوع مسبقًا يتضمنها بالفعل لها.</span><span class="sxs-lookup"><span data-stu-id="8536f-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="8536f-177">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8536f-177">Close the page.</span></span>

