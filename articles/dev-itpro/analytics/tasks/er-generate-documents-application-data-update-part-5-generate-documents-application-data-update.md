--- 
title: "إنشاء مستندات بواسطة بيانات التطبيق"
description: "لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، \"التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 4 - تعديل التنسيق)‬\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fbdd9f3937053f29b2cbd1f7f801ee17be0ae207
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="generate-documents-with-application-data"></a><span data-ttu-id="c54b6-103">إنشاء مستندات بواسطة بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="c54b6-103">Generate documents with application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c54b6-104">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 4: تعديل التنسيق)‬".</span><span class="sxs-lookup"><span data-stu-id="c54b6-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="c54b6-105">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="c54b6-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="c54b6-106">في هذا الإجراء، يمكنك تنفيذ تكوين تنسيق التقارير الإلكترونية لإنشاء تقرير نظام جمع المعلومات التجارية وتحديث بيانات التطبيق لأرشفة التفاصيل الخاصة بعملية إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="c54b6-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="c54b6-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="c54b6-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c54b6-108">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="c54b6-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="c54b6-109">قبل أن تبدأ، تأكد من أن سياق البلد الخاص بالشركة DEMF هو BEL (بلجيكا).</span><span class="sxs-lookup"><span data-stu-id="c54b6-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="c54b6-110">إعداد محددات التجارة الخارجية</span><span class="sxs-lookup"><span data-stu-id="c54b6-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="c54b6-111">انتقل إلى الضريبة > الإعداد > التجارة الخارجية > معلمات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="c54b6-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="c54b6-112">انقر فوق علامة التبويب "التسلسلات الرقمية".</span><span class="sxs-lookup"><span data-stu-id="c54b6-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="c54b6-113">لأرشفة التفاصيل الخاصة بعملية إعداد تقارير نظام جمع المعلومات التجارية، نحتاج إلى تحديد السجلات لكل أرشيف قمنا بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="c54b6-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="c54b6-114">يجب تكوين تسلسلي رقمي خاص لذلك.</span><span class="sxs-lookup"><span data-stu-id="c54b6-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="c54b6-115">حدد المرجع "معرف أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬".</span><span class="sxs-lookup"><span data-stu-id="c54b6-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="c54b6-116">في الحقل "كود تسلسل الرقم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c54b6-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="c54b6-117">في حقل "كود التسلسل الرقمي"، أدخل قيمة "Fore_2" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="c54b6-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="c54b6-118">كود التسلسل الرقمي ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="c54b6-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="c54b6-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="c54b6-119">Click Save.</span></span>
7. <span data-ttu-id="c54b6-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c54b6-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="c54b6-121">تشغيل تنسيق التقارير الإلكترونية المعدّل</span><span class="sxs-lookup"><span data-stu-id="c54b6-121">Run modified ER format</span></span>
1. <span data-ttu-id="c54b6-122">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="c54b6-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c54b6-123">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="c54b6-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="c54b6-124">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تنسيق)".</span><span class="sxs-lookup"><span data-stu-id="c54b6-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="c54b6-125">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="c54b6-125">Click Run.</span></span>
5. <span data-ttu-id="c54b6-126">في الحقل "إدخال اسم الملف"، اكتب "intrastat2.xml".</span><span class="sxs-lookup"><span data-stu-id="c54b6-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="c54b6-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="c54b6-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="c54b6-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c54b6-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="c54b6-129">مراجعة نتائج تنفيذ تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="c54b6-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="c54b6-130">راجع ملف XML المنشأ.</span><span class="sxs-lookup"><span data-stu-id="c54b6-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="c54b6-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c54b6-131">Close the page.</span></span>
2. <span data-ttu-id="c54b6-132">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="c54b6-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="c54b6-133">افتح هذا النموذج الذي يحتوي على حركات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المضمنة في المستند الإلكتروني المنشأ.</span><span class="sxs-lookup"><span data-stu-id="c54b6-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="c54b6-134">انقر فوق أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="c54b6-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="c54b6-135">نظرًا لاحتواء تنسيق التقارير الإلكترونية الذي تم تنفيذه الآن على إعدادات خاصة بتحديث بيانات التطبيق، تمت أرشفة تفاصيل تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المكتمل.</span><span class="sxs-lookup"><span data-stu-id="c54b6-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="c54b6-136">في هذا النموذج، يمكنك رؤية سجل الرأس للأرشيف الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="c54b6-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="c54b6-137">انقر فوق "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="c54b6-137">Click Details.</span></span>
    * <span data-ttu-id="c54b6-138">في هذا النموذج، يمكنك رؤية تفاصيل الأرشيف الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="c54b6-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="c54b6-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c54b6-139">Close the page.</span></span>
6. <span data-ttu-id="c54b6-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c54b6-140">Close the page.</span></span>
7. <span data-ttu-id="c54b6-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c54b6-141">Close the page.</span></span>


