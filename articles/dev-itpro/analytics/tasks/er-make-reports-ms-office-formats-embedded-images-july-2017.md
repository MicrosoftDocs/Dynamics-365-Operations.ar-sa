---
title: تصميم التكوينات لإنشاء تقارير بتنسيق Office تحتوي على صور مضمنة
description: توفر الخطوات الواردة في هذا الموضوع معلومات حول كيفية تصميم تكوينات التقارير الإلكترونية (ER) التي تُنشئ مستندات إلكترونية بتنسيقات Microsoft Office ‏(Excel‏‏ ‏وWord) تحتوي على صور مضمنة.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "358084"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="bb335-103">تصميم التكوينات لإنشاء تقارير بتنسيق Office تحتوي على صور مضمنة</span><span class="sxs-lookup"><span data-stu-id="bb335-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb335-104">لإكمال الخطوات الواردة في هذا الإجراء، أكمل أولاً الإجراء "التقارير الإلكترونية تُنشئ موفر تكوين وتضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="bb335-105">يوضح هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية (ER) لإنشاء مستند Microsoft Excel أو Word يحتوي على صور مضمنة.</span><span class="sxs-lookup"><span data-stu-id="bb335-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="bb335-106">في هذا الإجراء، ستقوم بإنشاء تكوينات التقارير الإلكترونية المطلوبة للشركة النموذجية، Litware, Inc. يمكن إكمال هذه الخطوات باستخدام مجموعة بيانات USMF.</span><span class="sxs-lookup"><span data-stu-id="bb335-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="bb335-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="bb335-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="bb335-108">قبل البدء، قم بتنزيل وحفظ الملفات الواردة ضمن موضوع التعليمات، [قم بتضمين الصور والأشكال في مستندات العمل التي تم إنشاؤها باستخدام أداة إعداد التقارير الإلكترونية](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="bb335-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="bb335-109">الملفات هي: Model for cheques.xml، وCheques printing format.xml، وCompany logo.png، وSignature image.png، وSignature image 2.png، وCheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="bb335-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="bb335-110">التحقق من المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="bb335-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="bb335-111">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="bb335-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="bb335-112">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="bb335-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="bb335-113">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="bb335-114">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="bb335-115">إضافة تكوين نموذج تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="bb335-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="bb335-116">بدلاً من إنشاء نموذج جديد، يمكنك تحميل ملف التكوين نموذج تكوين التقارير الإلكترونية (Model for cheques.xml) الذي قمت بحفظه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="bb335-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="bb335-117">يحتوي هذا الملف على عينة نموذج البيانات لشيكات الدفع وتعيين نموذج البيانات إلى مكونات البيانات لتطبيق Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="bb335-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="bb335-118">على علامة التبويب السريعة "الإصدارات"، انقر فوق "التبادل‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="bb335-119">انقر فوق "تحميل من ملف XML".</span><span class="sxs-lookup"><span data-stu-id="bb335-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="bb335-120">انقر فوق استعراض، ومن ثم حدد Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="bb335-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="bb335-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bb335-121">Click OK.</span></span>  
 6. <span data-ttu-id="bb335-122">سيتم استخدام النموذج الذي تم تحميله كمصدر بيانات للمعلومات المتعلقة بإنشاء المستندات التي تحتوي على صور في Word وExcel.</span><span class="sxs-lookup"><span data-stu-id="bb335-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="bb335-123">إضافة تكوين تنسيق تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="bb335-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="bb335-124">بدلاً من إنشاء تنسيق جديد، يمكنك تحميل ملف تموين تنسيق التقارير الإلكترونية (Cheques printing format.xml) الذي قمت بحفظه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="bb335-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="bb335-125">يحتوي هذا الملف على تخطيط النموذجي لتنسيق طباعة الشيكات باستخدام النموذج المطبوع مسبقًا وتعيين هذا التنسيق إلى نموذج البيانات "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="bb335-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="bb335-126">انقر فوق "التبادل‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="bb335-127">انقر فوق "تحميل من ملف XML".</span><span class="sxs-lookup"><span data-stu-id="bb335-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="bb335-128">انقر فوق "استعراض" وحدد الملف Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="bb335-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="bb335-129">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bb335-129">Click OK.</span></span>  
 6. <span data-ttu-id="bb335-130">في الشجرة، قم بتوسيع "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="bb335-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="bb335-131">في الشجرة، حدد "نموذج للشيكات\تنسيق طباعة الشيكات".</span><span class="sxs-lookup"><span data-stu-id="bb335-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="bb335-132">سيتم استخدام التنسيق الذي تم تحميله لإنشاء المستندات التي تحتوي على صور في Word وExcel.</span><span class="sxs-lookup"><span data-stu-id="bb335-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="bb335-133">تكوين معلمات مستخدم التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="bb335-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="bb335-134">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="bb335-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="bb335-135">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="bb335-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="bb335-136">حدد "نعم" في حقل "تشغيل الإعدادات".</span><span class="sxs-lookup"><span data-stu-id="bb335-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="bb335-137">قم بتشغيل علامة "تشغيل مسودة" لبدء تشغيل إصدار المسودة للتنسيق المحدد بدلاً من ذلك المكتمل.</span><span class="sxs-lookup"><span data-stu-id="bb335-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="bb335-138">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bb335-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="bb335-139">تكوين محددات إدارة البنك والنقد</span><span class="sxs-lookup"><span data-stu-id="bb335-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="bb335-140">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="bb335-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="bb335-141">استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "USMF OPER''.</span><span class="sxs-lookup"><span data-stu-id="bb335-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="bb335-142">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="bb335-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="bb335-143">انقر فوق "تحقق".</span><span class="sxs-lookup"><span data-stu-id="bb335-143">Click Check.</span></span>  
 5. <span data-ttu-id="bb335-144">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="bb335-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="bb335-145">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="bb335-145">Click Edit.</span></span>  
 7. <span data-ttu-id="bb335-146">حدد "نعم" في الحقل "شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="bb335-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="bb335-147">انقر فوق "شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="bb335-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="bb335-148">انقر فوق تغيير.</span><span class="sxs-lookup"><span data-stu-id="bb335-148">Click Change.</span></span>  
 10. <span data-ttu-id="bb335-149">انقر فوق "استعراض" وحدد الملف الذي قمت بتنزيله في وقت سابق، Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="bb335-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="bb335-150">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bb335-150">Click Save.</span></span>  
 12. <span data-ttu-id="bb335-151">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bb335-151">Close the page.</span></span>  
 13. <span data-ttu-id="bb335-152">وسّع مقطع "التوقيع".</span><span class="sxs-lookup"><span data-stu-id="bb335-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="bb335-153">حدد "نعم" في الحقل "طباعة التوقيع الأول‬‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="bb335-154">انقر فوق تغيير.</span><span class="sxs-lookup"><span data-stu-id="bb335-154">Click Change.</span></span>  
 16. <span data-ttu-id="bb335-155">انقر فوق "استعراض" وحدد الملف الذي قمت بتنزيله في وقت سابق، Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="bb335-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="bb335-156">قم بتوسيع مقطع "النسخ‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="bb335-157">في الحقل "علامة مائية"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="bb335-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="bb335-158">حدد "نعم" في الحقل "تنسيق التصدير الإلكتروني العام‬‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="bb335-159">حدد التكوين "نموذج طباعة الشيكات".</span><span class="sxs-lookup"><span data-stu-id="bb335-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="bb335-160">سيتم الآن استخدام التنسيق التقارير الإلكترونية المحدد لطباعة الشيكات.</span><span class="sxs-lookup"><span data-stu-id="bb335-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="bb335-161">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="bb335-161">Click Attach.</span></span>  
 23. <span data-ttu-id="bb335-162">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="bb335-162">Click New.</span></span>  
 24. <span data-ttu-id="bb335-163">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="bb335-163">Click File.</span></span>  
 25. <span data-ttu-id="bb335-164">انقر فوق "استعراض" وحدد الملف الذي قمت بتنزيله في وقت سابق، Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="bb335-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="bb335-165">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bb335-165">Close the page.</span></span>  
 27. <span data-ttu-id="bb335-166">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bb335-166">Close the page.</span></span>  
 28. <span data-ttu-id="bb335-167">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bb335-167">Close the page.</span></span>  
 29. <span data-ttu-id="bb335-168">انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="bb335-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="bb335-169">حدد "نعم" في الحقل "السماح بإنشاء إشعار مسبق على حسابات البنك غير النشطة:‬".</span><span class="sxs-lookup"><span data-stu-id="bb335-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="bb335-170">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="bb335-170">Click Save.</span></span>  
 32. <span data-ttu-id="bb335-171">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bb335-171">Close the page.</span></span>  
