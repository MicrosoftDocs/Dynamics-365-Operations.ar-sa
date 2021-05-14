---
title: تصميم التكوينات لإنشاء تقارير بتنسيق Office تحتوي على صور مضمنة
description: يصف هذا الموضوع كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستندات بتنسيقات Excel وWord تتضمن صورًا مضمنة.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944547"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="8deb4-103">تصميم التكوينات لإنشاء تقارير بتنسيق Office تحتوي على صور مضمنة</span><span class="sxs-lookup"><span data-stu-id="8deb4-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8deb4-104">لإكمال الخطوات الواردة في هذا الإجراء، أكمل أولاً الإجراء "التقارير الإلكترونية تُنشئ موفر تكوين وتضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="8deb4-105">يوضح هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية (ER) لإنشاء مستند Microsoft Excel أو Word يحتوي على صور مضمنة.</span><span class="sxs-lookup"><span data-stu-id="8deb4-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="8deb4-106">في هذا الإجراء، ستقوم بإنشاء تكوينات التقارير الإلكترونية المطلوبة للشركة النموذجية، Litware, Inc. يمكن إكمال هذه الخطوات باستخدام مجموعة بيانات USMF.</span><span class="sxs-lookup"><span data-stu-id="8deb4-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="8deb4-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8deb4-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="8deb4-108">قبل أن تبدأ ، قم بتنزيل وحفظ الملفات التالية:</span><span class="sxs-lookup"><span data-stu-id="8deb4-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="8deb4-109">الوصف</span><span class="sxs-lookup"><span data-stu-id="8deb4-109">Description</span></span>                                          | <span data-ttu-id="8deb4-110">اسم الملف</span><span class="sxs-lookup"><span data-stu-id="8deb4-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="8deb4-111">تكوين نموذج بيانات التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="8deb4-111">ER data model configuration</span></span>                          | [<span data-ttu-id="8deb4-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="8deb4-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="8deb4-113">تنسيق تكوين ER</span><span class="sxs-lookup"><span data-stu-id="8deb4-113">ER format configuration</span></span>                              | [<span data-ttu-id="8deb4-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="8deb4-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="8deb4-115">صورة شعار الشركة</span><span class="sxs-lookup"><span data-stu-id="8deb4-115">Company logo image</span></span>                                   | [<span data-ttu-id="8deb4-116">Company logo.png</span><span class="sxs-lookup"><span data-stu-id="8deb4-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="8deb4-117">صورة التوقيع</span><span class="sxs-lookup"><span data-stu-id="8deb4-117">Signature image</span></span>                                      | [<span data-ttu-id="8deb4-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="8deb4-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="8deb4-119">صورة توقيع بديل</span><span class="sxs-lookup"><span data-stu-id="8deb4-119">Alternative signature image</span></span>                          | [<span data-ttu-id="8deb4-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="8deb4-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="8deb4-121">قالب Microsoft Word لطباعة شيكات الدفع</span><span class="sxs-lookup"><span data-stu-id="8deb4-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="8deb4-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="8deb4-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="8deb4-123">التحقق من المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="8deb4-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="8deb4-124">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="8deb4-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="8deb4-125">تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="8deb4-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="8deb4-126">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="8deb4-127">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="8deb4-128">إضافة تكوين نموذج تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="8deb4-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="8deb4-129">بدلاً من إنشاء نموذج جديد، يمكنك تحميل ملف التكوين نموذج تكوين التقارير الإلكترونية (Model for cheques.xml) الذي قمت بحفظه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="8deb4-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="8deb4-130">يحتوي هذا الملف على عينة نموذج البيانات لشيكات الدفع وتعيين نموذج البيانات إلى مكونات البيانات لتطبيق Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="8deb4-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="8deb4-131">على علامة التبويب السريعة "الإصدارات"، انقر فوق "التبادل‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="8deb4-132">انقر فوق "تحميل من ملف XML".</span><span class="sxs-lookup"><span data-stu-id="8deb4-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="8deb4-133">انقر فوق استعراض، ومن ثم حدد Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="8deb4-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="8deb4-134">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8deb4-134">Click OK.</span></span>  
 6. <span data-ttu-id="8deb4-135">سيتم استخدام النموذج الذي تم تحميله كمصدر بيانات للمعلومات المتعلقة بإنشاء المستندات التي تحتوي على صور في Word وExcel.</span><span class="sxs-lookup"><span data-stu-id="8deb4-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="8deb4-136">إضافة تكوين تنسيق تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="8deb4-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="8deb4-137">بدلاً من إنشاء تنسيق جديد، يمكنك تحميل ملف تموين تنسيق التقارير الإلكترونية (Cheques printing format.xml) الذي قمت بحفظه سابقًا.</span><span class="sxs-lookup"><span data-stu-id="8deb4-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="8deb4-138">يحتوي هذا الملف على تخطيط النموذجي لتنسيق طباعة الشيكات باستخدام النموذج المطبوع مسبقًا وتعيين هذا التنسيق إلى نموذج البيانات "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="8deb4-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="8deb4-139">انقر فوق "التبادل‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="8deb4-140">انقر فوق "تحميل من ملف XML".</span><span class="sxs-lookup"><span data-stu-id="8deb4-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="8deb4-141">انقر فوق "استعراض" وحدد الملف Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="8deb4-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="8deb4-142">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8deb4-142">Click OK.</span></span>  
 6. <span data-ttu-id="8deb4-143">في الشجرة، قم بتوسيع "نموذج للشيكات".</span><span class="sxs-lookup"><span data-stu-id="8deb4-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="8deb4-144">في الشجرة، حدد "نموذج للشيكات\تنسيق طباعة الشيكات".</span><span class="sxs-lookup"><span data-stu-id="8deb4-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="8deb4-145">سيتم استخدام التنسيق الذي تم تحميله لإنشاء المستندات التي تحتوي على صور في Word وExcel.</span><span class="sxs-lookup"><span data-stu-id="8deb4-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="8deb4-146">تكوين معلمات مستخدم التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="8deb4-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="8deb4-147">في جزء الإجراءات، انقر فوق "التكوينات".</span><span class="sxs-lookup"><span data-stu-id="8deb4-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="8deb4-148">انقر فوق "محددات المستخدم".</span><span class="sxs-lookup"><span data-stu-id="8deb4-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="8deb4-149">حدد "نعم" في حقل "تشغيل الإعدادات".</span><span class="sxs-lookup"><span data-stu-id="8deb4-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="8deb4-150">قم بتشغيل علامة "تشغيل مسودة" لبدء تشغيل إصدار المسودة للتنسيق المحدد بدلاً من ذلك المكتمل.</span><span class="sxs-lookup"><span data-stu-id="8deb4-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="8deb4-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8deb4-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="8deb4-152">تكوين محددات إدارة البنك والنقد</span><span class="sxs-lookup"><span data-stu-id="8deb4-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="8deb4-153">انتقل إلى إدارة النقد والبنوك > الحسابات البنكية > الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="8deb4-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="8deb4-154">استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "USMF OPER''.</span><span class="sxs-lookup"><span data-stu-id="8deb4-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="8deb4-155">في جزء الإجراءات، انقر فوق "إعداد".</span><span class="sxs-lookup"><span data-stu-id="8deb4-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="8deb4-156">انقر فوق "تحقق".</span><span class="sxs-lookup"><span data-stu-id="8deb4-156">Click Check.</span></span>  
 5. <span data-ttu-id="8deb4-157">قم بتوسيع قسم "الإعداد".</span><span class="sxs-lookup"><span data-stu-id="8deb4-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="8deb4-158">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="8deb4-158">Click Edit.</span></span>  
 7. <span data-ttu-id="8deb4-159">حدد "نعم" في الحقل "شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="8deb4-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="8deb4-160">انقر فوق "شعار الشركة".</span><span class="sxs-lookup"><span data-stu-id="8deb4-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="8deb4-161">انقر فوق تغيير.</span><span class="sxs-lookup"><span data-stu-id="8deb4-161">Click Change.</span></span>  
 10. <span data-ttu-id="8deb4-162">انقر فوق "استعراض" وحدد الملف الذي قمت بتنزيله في وقت سابق، Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="8deb4-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="8deb4-163">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8deb4-163">Click Save.</span></span>  
 12. <span data-ttu-id="8deb4-164">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8deb4-164">Close the page.</span></span>  
 13. <span data-ttu-id="8deb4-165">وسّع مقطع "التوقيع".</span><span class="sxs-lookup"><span data-stu-id="8deb4-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="8deb4-166">حدد "نعم" في الحقل "طباعة التوقيع الأول‬‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="8deb4-167">انقر فوق تغيير.</span><span class="sxs-lookup"><span data-stu-id="8deb4-167">Click Change.</span></span>  
 16. <span data-ttu-id="8deb4-168">انقر فوق "استعراض" وحدد الملف الذي قمت بتنزيله في وقت سابق، Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="8deb4-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="8deb4-169">قم بتوسيع مقطع "النسخ‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="8deb4-170">في الحقل "علامة مائية"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="8deb4-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="8deb4-171">حدد "نعم" في الحقل "تنسيق التصدير الإلكتروني العام‬‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="8deb4-172">حدد التكوين "نموذج طباعة الشيكات".</span><span class="sxs-lookup"><span data-stu-id="8deb4-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="8deb4-173">سيتم الآن استخدام التنسيق التقارير الإلكترونية المحدد لطباعة الشيكات.</span><span class="sxs-lookup"><span data-stu-id="8deb4-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="8deb4-174">انقر فوق "إرفاق".</span><span class="sxs-lookup"><span data-stu-id="8deb4-174">Click Attach.</span></span>  
 23. <span data-ttu-id="8deb4-175">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="8deb4-175">Click New.</span></span>  
 24. <span data-ttu-id="8deb4-176">انقر فوق "ملف".</span><span class="sxs-lookup"><span data-stu-id="8deb4-176">Click File.</span></span>  
 25. <span data-ttu-id="8deb4-177">انقر فوق "استعراض" وحدد الملف الذي قمت بتنزيله في وقت سابق، Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="8deb4-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="8deb4-178">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8deb4-178">Close the page.</span></span>  
 27. <span data-ttu-id="8deb4-179">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8deb4-179">Close the page.</span></span>  
 28. <span data-ttu-id="8deb4-180">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8deb4-180">Close the page.</span></span>  
 29. <span data-ttu-id="8deb4-181">انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="8deb4-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="8deb4-182">حدد "نعم" في الحقل "السماح بإنشاء إشعار مسبق على حسابات البنك غير النشطة:‬".</span><span class="sxs-lookup"><span data-stu-id="8deb4-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="8deb4-183">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="8deb4-183">Click Save.</span></span>  
 32. <span data-ttu-id="8deb4-184">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8deb4-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
