---
title: تصميم تعبيرات التقارير الإلكترونية لاستدعاء أساليب فئات التطبيقات
description: يصف هذا الموضوع كيفية إعادة استخدام منطق التطبيق الموجود في تكوينات التقارير الإلكترونية عن طريق استدعاء أساليب فئات التطبيقات المطلوبة في تعبيرات التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11b4d185703731d8491ad10bdeedea40ce811f5d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564084"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="d8989-103">تصميم تعبيرات التقارير الإلكترونية لاستدعاء أساليب فئات التطبيقات</span><span class="sxs-lookup"><span data-stu-id="d8989-103">Design ER expressions to call application class methods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8989-104">يوفر هذا الدليل معلومات حول كيفية إعادة استخدام منطق التطبيق الموجود في تكوينات التقارير الإلكترونية عن طريق استدعاء أساليب فئات التطبيقات المطلوبة في تعبيرات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d8989-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="d8989-105">يمكن تعريف قيم الوسيطات لاستدعاء الفئات بشكل حيوي في وقت التشغيل: على سبيل المثال، استنادًا إلى المعلومات في مستند التحليل للتأكد من صحتها.</span><span class="sxs-lookup"><span data-stu-id="d8989-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="d8989-106">في هذا الدليل، يمكنك إنشاء تكوينات التقارير الإلكترونية المطلوبة للشركة النموذجية، Litware, Inc.. تم إنشاء هذا الإجراء للمستخدمين الذين تم تعيين دور مسؤول النظام أو مطور التقارير الإلكتروني لهم.</span><span class="sxs-lookup"><span data-stu-id="d8989-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="d8989-107">يمكن إتمام هذه الخطوات باستخدام أي مجموعة بيانات.</span><span class="sxs-lookup"><span data-stu-id="d8989-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="d8989-108">يجب أيضًا تحميل وحفظ الملف التالي محليًا: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="d8989-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="d8989-109">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".</span><span class="sxs-lookup"><span data-stu-id="d8989-109">To complete these steps, you must first complete the steps in the procedure, "ER Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="d8989-110">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="d8989-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d8989-111">تحقق من وجود موفر التكوين للشركة النموذجية Litware, Inc. ومن وضع علامة عليه كنشط.</span><span class="sxs-lookup"><span data-stu-id="d8989-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="d8989-112">إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-112">If you don't see this configuration provider, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>   
    * <span data-ttu-id="d8989-113">أنت تقوم بتصميم عملية لتحليل كشوف الحسابات البنكية الواردة لتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="d8989-113">You are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="d8989-114">سوف تتلقى كشوف الحسابات البنكية الواردة كملفات TXT تحتوي على أكواد IBAN.</span><span class="sxs-lookup"><span data-stu-id="d8989-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="d8989-115">كجزء من عملية استيراد كشف الحساب البنكي، يتعين عليك التحقق من صحة أكواد IBAN هذه باستخدام منطق موجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="d8989-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="d8989-116">استيراد تكوين نموذج تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="d8989-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="d8989-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d8989-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d8989-118">حدد لوحة "موفر Microsoft".</span><span class="sxs-lookup"><span data-stu-id="d8989-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="d8989-119">انقر فوق "المستودعات".</span><span class="sxs-lookup"><span data-stu-id="d8989-119">Click Repositories.</span></span>
3. <span data-ttu-id="d8989-120">انقر فوق "إظهار عوامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="d8989-120">Click Show filters.</span></span>
4. <span data-ttu-id="d8989-121">أضف حقل عامل التصفية "اكتب اسمًا".</span><span class="sxs-lookup"><span data-stu-id="d8989-121">Add a filter field 'Type name'.</span></span> <span data-ttu-id="d8989-122">في حقل "الاسم"، أدخل القيمة "موارد" وحدد عامل التصفية "يحتوي"، ثم انقر فوق "تطبيق".</span><span class="sxs-lookup"><span data-stu-id="d8989-122">In the Name field, enter the value "resources", select the "contains" filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="d8989-123">انقر فوق "فتح".</span><span class="sxs-lookup"><span data-stu-id="d8989-123">Click Open.</span></span>
6. <span data-ttu-id="d8989-124">في الشجرة، حدد "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="d8989-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="d8989-125">إذا لم يتم تمكين الزر "استيراد" على علامة التبويب السريعة "إصدارات"، فهذا يعني أنك قمت مسبقًا باستيراد الإصدار 1 من تكوين التقارير الإلكترونية "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="d8989-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration 'Payment model'.</span></span> <span data-ttu-id="d8989-126">يمكنك تخطي الخطوات المتبقية في هذه المهمة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="d8989-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="d8989-127">انقر فوق "استيراد".</span><span class="sxs-lookup"><span data-stu-id="d8989-127">Click Import.</span></span>
8. <span data-ttu-id="d8989-128">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="d8989-128">Click Yes.</span></span>
9. <span data-ttu-id="d8989-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8989-129">Close the page.</span></span>
10. <span data-ttu-id="d8989-130">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8989-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="d8989-131">إضافة تكوين تنسيق تقارير إلكترونية جديد</span><span class="sxs-lookup"><span data-stu-id="d8989-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="d8989-132">انقر فوق "تكوينات إعداد التقارير‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d8989-133">أضف تنسيق تقارير إلكترونية جديدًا لتحليل كشوف الحسابات البنيكية في تنسيق TXT.</span><span class="sxs-lookup"><span data-stu-id="d8989-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="d8989-134">في الشجرة، حدد "نموذج الدفع".</span><span class="sxs-lookup"><span data-stu-id="d8989-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="d8989-135">انقر فوق "إنشاء تكوين" لفتح قائمة مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="d8989-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="d8989-136">في الحقل "جديد"، أدخل 'التنسيق استناداً إلى نموذج الدفع الخاص بنموذج البيانات".</span><span class="sxs-lookup"><span data-stu-id="d8989-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="d8989-137">في حقل "الاسم"، اكتب 'استيراد كشف الحساب البنكي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="d8989-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="d8989-138">تنسيق استيراد كشف حساب بنكي (نموذج)</span><span class="sxs-lookup"><span data-stu-id="d8989-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="d8989-139">حدد "نعم" في الحقل "دعم استيراد البيانات".</span><span class="sxs-lookup"><span data-stu-id="d8989-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="d8989-140">وانقر فوق إنشاء تكوين.</span><span class="sxs-lookup"><span data-stu-id="d8989-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="d8989-141">تصميم تكوين تنسيق تقارير إلكترونية - تنسيق</span><span class="sxs-lookup"><span data-stu-id="d8989-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="d8989-142">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="d8989-142">Click Designer.</span></span>
    * <span data-ttu-id="d8989-143">يمثل التنسيق المصمّم البنية المتوقعة للملف الخارجي بتنسيق TXT.</span><span class="sxs-lookup"><span data-stu-id="d8989-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="d8989-144">انقر فوق "إضافة جذر" لفتح قائمة مربع الحوار‬.</span><span class="sxs-lookup"><span data-stu-id="d8989-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="d8989-145">في الشجرة، حدد "النص\التسلسل".</span><span class="sxs-lookup"><span data-stu-id="d8989-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="d8989-146">في حقل "الاسم" اكتب "الجذر‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="d8989-147">الجذر</span><span class="sxs-lookup"><span data-stu-id="d8989-147">Root</span></span>  
5. <span data-ttu-id="d8989-148">في الحقل "أحرف خاصة‬"، حدد "سطر جديد - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="d8989-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="d8989-149">تم تحديد الخيار "سطر جديد - Windows (CR LF)" في الحقل "أحرف خاصة‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-149">The option 'New line - Windows (CR LF)' has been selected in the 'Special characters' field.</span></span> <span data-ttu-id="d8989-150">استنادًا إلى هذا الإعداد، يتم اعتبار كل سطر في ملف التحليل سجلاً منفصلاً.</span><span class="sxs-lookup"><span data-stu-id="d8989-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="d8989-151">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8989-151">Click OK.</span></span>
7. <span data-ttu-id="d8989-152">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d8989-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="d8989-153">في الشجرة، حدد "النص\التسلسل".</span><span class="sxs-lookup"><span data-stu-id="d8989-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="d8989-154">في حقل "الاسم"، اكتب "صفوف".</span><span class="sxs-lookup"><span data-stu-id="d8989-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="d8989-155">صفوف</span><span class="sxs-lookup"><span data-stu-id="d8989-155">Rows</span></span>  
10. <span data-ttu-id="d8989-156">في حقل "التعدد"، حدد "واحد كثير‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="d8989-157">تم تحديد الخيار "واحد متعدد" في حقل "التعدد".</span><span class="sxs-lookup"><span data-stu-id="d8989-157">The option 'One many' has been selected in the 'Multiplicity' field.</span></span> <span data-ttu-id="d8989-158">استنادًا إلى هذا الإعداد، من المتوقع أن يتم تقديم سطر واحد على الأقل في ملف التحليل.</span><span class="sxs-lookup"><span data-stu-id="d8989-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="d8989-159">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8989-159">Click OK.</span></span>
12. <span data-ttu-id="d8989-160">في الشجرة، حدد "جذر\صفوف".</span><span class="sxs-lookup"><span data-stu-id="d8989-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="d8989-161">انقر فوق "إضافة تسلسل".</span><span class="sxs-lookup"><span data-stu-id="d8989-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="d8989-162">في حقل "الاسم" ، اكتب "حقول".</span><span class="sxs-lookup"><span data-stu-id="d8989-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="d8989-163">الحقول</span><span class="sxs-lookup"><span data-stu-id="d8989-163">Fields</span></span>  
15. <span data-ttu-id="d8989-164">في حقل "التعدد"، حدد "واحد فقط‬‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="d8989-165">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8989-165">Click OK.</span></span>
17. <span data-ttu-id="d8989-166">في الشجرة ، حدد "جذر\صفوف\حقول".</span><span class="sxs-lookup"><span data-stu-id="d8989-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="d8989-167">انقر فوق "إضافة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="d8989-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="d8989-168">في الشجرة، حدد "Text\String".</span><span class="sxs-lookup"><span data-stu-id="d8989-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="d8989-169">في الحقل "الاسم، اكتب "IBAN".</span><span class="sxs-lookup"><span data-stu-id="d8989-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="d8989-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="d8989-170">IBAN</span></span>  
21. <span data-ttu-id="d8989-171">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8989-171">Click OK.</span></span>
    * <span data-ttu-id="d8989-172">تم تكوينه بحيث يحتوي كل سطر في ملف التحليل على كود IBAN فقط.</span><span class="sxs-lookup"><span data-stu-id="d8989-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="d8989-173">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8989-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="d8989-174">تصميم تكوين تنسيق تقارير إلكترونية – تعيين إلى نموذج بيانات</span><span class="sxs-lookup"><span data-stu-id="d8989-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="d8989-175">انقر فوق "تعيين تنسيق لنموذج‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-175">Click Map format to model.</span></span>
2. <span data-ttu-id="d8989-176">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d8989-176">Click New.</span></span>
3. <span data-ttu-id="d8989-177">في حقل التعريف، اكتب "BankToCustomerDebitCreditNotificationInitiation".</span><span class="sxs-lookup"><span data-stu-id="d8989-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="d8989-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="d8989-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="d8989-179">حل تغييرات التعريف.</span><span class="sxs-lookup"><span data-stu-id="d8989-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="d8989-180">في حقل "الاسم"، اكتب "تعيين إلى نموذج البيانات‬".</span><span class="sxs-lookup"><span data-stu-id="d8989-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="d8989-181">تعيين إلى نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="d8989-181">Mapping to data model</span></span>  
6. <span data-ttu-id="d8989-182">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8989-182">Click Save.</span></span>
7. <span data-ttu-id="d8989-183">انقر فوق المصمم.</span><span class="sxs-lookup"><span data-stu-id="d8989-183">Click Designer.</span></span>
8. <span data-ttu-id="d8989-184">في الشجرة، حدد 'Dynamics 365 for Operations\فئة'.</span><span class="sxs-lookup"><span data-stu-id="d8989-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="d8989-185">انقر فوق "إضافة جذر".</span><span class="sxs-lookup"><span data-stu-id="d8989-185">Click Add root.</span></span>
    * <span data-ttu-id="d8989-186">قم بإضافة مصدر بيانات جديد لاستدعاء منطق التطبيق الموجود للتحقق من صحة أكواد IBAN.</span><span class="sxs-lookup"><span data-stu-id="d8989-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="d8989-187">في حقل "الاسم"، اكتب "check_codes".</span><span class="sxs-lookup"><span data-stu-id="d8989-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="d8989-188">التحقق من الأكواد</span><span class="sxs-lookup"><span data-stu-id="d8989-188">check_codes</span></span>  
11. <span data-ttu-id="d8989-189">في حقل "الفئة"، اكتب "ISO7064".</span><span class="sxs-lookup"><span data-stu-id="d8989-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="d8989-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="d8989-190">ISO7064</span></span>  
12. <span data-ttu-id="d8989-191">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8989-191">Click OK.</span></span>
13. <span data-ttu-id="d8989-192">في الشجرة، قم بتوسيع "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="d8989-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="d8989-193">في الشجرة، وسّع "تنسيق\جذر: تسلسل(جذر)".</span><span class="sxs-lookup"><span data-stu-id="d8989-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="d8989-194">في الشجرة، حدد "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)".</span><span class="sxs-lookup"><span data-stu-id="d8989-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="d8989-195">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="d8989-195">Click Bind.</span></span>
17. <span data-ttu-id="d8989-196">في الشجرة، وسّع "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)".</span><span class="sxs-lookup"><span data-stu-id="d8989-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="d8989-197">في الشجرة، وسّع "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)\حقول: تسلسل 1..1 (حقول)".</span><span class="sxs-lookup"><span data-stu-id="d8989-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="d8989-198">في الشجرة، حدد "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)\حقول: تسلسل 1..1 (حقول)\IBAN: سلسلة(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="d8989-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="d8989-199">في الشجرة، وسّع "دفعات = format.Root.Rows".</span><span class="sxs-lookup"><span data-stu-id="d8989-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="d8989-200">في الشجرة، وسّع "دفعات = format.Root.Rows\حساب الدائن(CreditorAccount)".</span><span class="sxs-lookup"><span data-stu-id="d8989-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="d8989-201">في الشجرة، وسّع "دفعات = format.Root.Rows\حساب الدائن(CreditorAccount)\تعريف".</span><span class="sxs-lookup"><span data-stu-id="d8989-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="d8989-202">في الشجرة، حدد "دفعات = format.Root.Rows\حساب الدائن(CreditorAccount)\تعريف\IBAN".</span><span class="sxs-lookup"><span data-stu-id="d8989-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="d8989-203">انقر فوق "ربط".</span><span class="sxs-lookup"><span data-stu-id="d8989-203">Click Bind.</span></span>
25. <span data-ttu-id="d8989-204">انقر فوق علامة التبويب "عمليات التحقق من الصحة".</span><span class="sxs-lookup"><span data-stu-id="d8989-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="d8989-205">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d8989-205">Click New.</span></span>
    * <span data-ttu-id="d8989-206">أضف قاعدة تحقق من الصحة جديدة تعرض رسالة خطأ لأي سطر في ملف التحليل يحتوي على كود IBAN غير صالح.</span><span class="sxs-lookup"><span data-stu-id="d8989-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="d8989-207">انقر فوق "تحرير الشرط".</span><span class="sxs-lookup"><span data-stu-id="d8989-207">Click Edit condition.</span></span>
28. <span data-ttu-id="d8989-208">في الشجرة، وسّع "check_codes".</span><span class="sxs-lookup"><span data-stu-id="d8989-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="d8989-209">في الشجرة، حدد "check_codes\verifyMOD1271_36".</span><span class="sxs-lookup"><span data-stu-id="d8989-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="d8989-210">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="d8989-210">Click Add data source.</span></span>
31. <span data-ttu-id="d8989-211">في حقل الصيغة، أدخل "check_codes.verifyMOD1271_36(".</span><span class="sxs-lookup"><span data-stu-id="d8989-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="d8989-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="d8989-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="d8989-213">في الشجرة، قم بتوسيع "تنسيق".</span><span class="sxs-lookup"><span data-stu-id="d8989-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="d8989-214">في الشجرة، وسّع "تنسيق\جذر: تسلسل(جذر)".</span><span class="sxs-lookup"><span data-stu-id="d8989-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="d8989-215">في الشجرة، وسّع "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)".</span><span class="sxs-lookup"><span data-stu-id="d8989-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="d8989-216">في الشجرة، وسّع "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)\حقول: تسلسل 1..1 (حقول)".</span><span class="sxs-lookup"><span data-stu-id="d8989-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="d8989-217">في الشجرة، حدد "تنسيق\جذر: تسلسل(جذر)\صفوف: تسلسل 1..\* (صفوف)\حقول: تسلسل 1..1 (حقول)\IBAN: سلسلة(IBAN)".</span><span class="sxs-lookup"><span data-stu-id="d8989-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="d8989-218">انقر فوق "إضافة مصدر بيانات".</span><span class="sxs-lookup"><span data-stu-id="d8989-218">Click Add data source.</span></span>
38. <span data-ttu-id="d8989-219">في حقل صيغة، أدخل "check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)".</span><span class="sxs-lookup"><span data-stu-id="d8989-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="d8989-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="d8989-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="d8989-221">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8989-221">Click Save.</span></span>
40. <span data-ttu-id="d8989-222">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8989-222">Close the page.</span></span>
    * <span data-ttu-id="d8989-223">تم تكوين شرط التحقق من الصحة لإرجاع FALSE لأي كود IBAN غير صالح عن طريق استدعاء الأسلوب موجود "verifyMOD1271_36" لفئة التطبيق "ISO7064".</span><span class="sxs-lookup"><span data-stu-id="d8989-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method 'verifyMOD1271_36' of the application class 'ISO7064'.</span></span> <span data-ttu-id="d8989-224">لاحظ أن قيمة كود IBAN يجري تعريفها بشكل حيوي في وقت التشغيل كوسيطة أسلوب الاستدعاء المستند إلى المحتوى الخاص بملف التحليل بتنسيق TXT.</span><span class="sxs-lookup"><span data-stu-id="d8989-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="d8989-225">انقر فوق "تحرير الرسالة".</span><span class="sxs-lookup"><span data-stu-id="d8989-225">Click Edit message.</span></span>
42. <span data-ttu-id="d8989-226">في حقل الصيغة، أدخل "CONCATENATE("تم العثور على كود IBAN غير صالح:  ", format.Root.Rows.Fields.IBAN)".</span><span class="sxs-lookup"><span data-stu-id="d8989-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="d8989-227">CONCATENATE("تم العثور على كود IBAN غير صالح:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="d8989-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="d8989-228">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8989-228">Click Save.</span></span>
44. <span data-ttu-id="d8989-229">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8989-229">Close the page.</span></span>
45. <span data-ttu-id="d8989-230">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d8989-230">Click Save.</span></span>
46. <span data-ttu-id="d8989-231">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d8989-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="d8989-232">تشغيل تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="d8989-232">Run the format mapping</span></span>
<span data-ttu-id="d8989-233">لأغراض الاختبار، قم بتنفيذ تعيين التنسيق باستخدام الملف SampleIncomingMessage.txt الذي قمت بتنزيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="d8989-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="d8989-234">سوف تتضمن المخرجات الناشئة البيانات التي سيتم استيرادها من ملف TXT المحدد وتعبئتها في نموذج البيانات المخصص أثناء الاستيراد الحقيقي.</span><span class="sxs-lookup"><span data-stu-id="d8989-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="d8989-235">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="d8989-235">Click Run.</span></span>
    * <span data-ttu-id="d8989-236">انقر فوق "استعراض"، وانتقل إلى الملف SampleIncomingMessage.txt الذي قمت بتنزيله في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="d8989-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="d8989-237">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d8989-237">Click OK.</span></span>
    * <span data-ttu-id="d8989-238">راجع المخرجات بتنسيق XML التي تمثل البيانات التي تم استيرادها من الملف المحدد ونقلها إلى نموذج البيانات.</span><span class="sxs-lookup"><span data-stu-id="d8989-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="d8989-239">لاحظ أنه قد تمت معالجة 3 أسطر فقط من ملف TXT الذي تم استيراده.</span><span class="sxs-lookup"><span data-stu-id="d8989-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="d8989-240">تم تخطي رمز IBAN غير الصالح على السطر 4 وتم توفير رسالة خطأ في سجل المعلومات.</span><span class="sxs-lookup"><span data-stu-id="d8989-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]