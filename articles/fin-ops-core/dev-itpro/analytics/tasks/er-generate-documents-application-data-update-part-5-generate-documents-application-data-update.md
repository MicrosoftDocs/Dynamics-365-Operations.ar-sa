---
title: إنشاء مستندات تتضمن بيانات التطبيق
description: لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 4 - تعديل التنسيق)‬".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 6af7113031fd77a0a7e06ec23a149a3fa7ad0012
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026053"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="0a8ef-103">إنشاء مستندات تتضمن بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="0a8ef-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a8ef-104">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، "التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 4: تعديل التنسيق)‬".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="0a8ef-105">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وتحديث بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="0a8ef-106">في هذا الإجراء، يمكنك تنفيذ تكوين تنسيق التقارير الإلكترونية لإنشاء تقرير نظام جمع المعلومات التجارية وتحديث بيانات التطبيق لأرشفة التفاصيل الخاصة بعملية إعداد التقارير.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="0a8ef-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="0a8ef-108">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="0a8ef-109">قبل أن تبدأ، تأكد من أن سياق البلد الخاص بالشركة DEMF هو BEL (بلجيكا).</span><span class="sxs-lookup"><span data-stu-id="0a8ef-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="0a8ef-110">إعداد محددات التجارة الخارجية</span><span class="sxs-lookup"><span data-stu-id="0a8ef-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="0a8ef-111">انتقل إلى الضريبة > الإعداد > التجارة الخارجية > معلمات التجارة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="0a8ef-112">انقر فوق علامة التبويب "التسلسلات الرقمية".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="0a8ef-113">لأرشفة التفاصيل الخاصة بعملية إعداد تقارير نظام جمع المعلومات التجارية، نحتاج إلى تحديد السجلات لكل أرشيف قمنا بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="0a8ef-114">يجب تكوين تسلسلي رقمي خاص لذلك.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="0a8ef-115">حدد المرجع "معرف أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي‬".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="0a8ef-116">في الحقل "كود تسلسل الرقم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="0a8ef-117">في حقل "كود التسلسل الرقمي"، أدخل قيمة "Fore_2" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="0a8ef-118">كود التسلسل الرقمي ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="0a8ef-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-119">Click Save.</span></span>
7. <span data-ttu-id="0a8ef-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="0a8ef-121">تشغيل تنسيق التقارير الإلكترونية المعدّل</span><span class="sxs-lookup"><span data-stu-id="0a8ef-121">Run modified ER format</span></span>
1. <span data-ttu-id="0a8ef-122">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0a8ef-123">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="0a8ef-124">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تنسيق)".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="0a8ef-125">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-125">Click Run.</span></span>
5. <span data-ttu-id="0a8ef-126">في الحقل "إدخال اسم الملف"، اكتب "intrastat2.xml".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="0a8ef-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="0a8ef-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="0a8ef-128">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="0a8ef-129">مراجعة نتائج تنفيذ تنسيق التقارير الإلكترونية</span><span class="sxs-lookup"><span data-stu-id="0a8ef-129">Review ER format execution’s results</span></span>
<span data-ttu-id="0a8ef-130">راجع ملف XML المنشأ.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="0a8ef-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-131">Close the page.</span></span>
2. <span data-ttu-id="0a8ef-132">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="0a8ef-133">افتح هذا النموذج الذي يحتوي على حركات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المضمنة في المستند الإلكتروني المنشأ.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="0a8ef-134">انقر فوق أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="0a8ef-135">نظرًا لاحتواء تنسيق التقارير الإلكترونية الذي تم تنفيذه الآن على إعدادات خاصة بتحديث بيانات التطبيق، تمت أرشفة تفاصيل تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المكتمل.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="0a8ef-136">في هذا النموذج، يمكنك رؤية سجل الرأس للأرشيف الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="0a8ef-137">انقر فوق "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="0a8ef-137">Click Details.</span></span>
    * <span data-ttu-id="0a8ef-138">في هذا النموذج، يمكنك رؤية تفاصيل الأرشيف الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="0a8ef-139">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-139">Close the page.</span></span>
6. <span data-ttu-id="0a8ef-140">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-140">Close the page.</span></span>
7. <span data-ttu-id="0a8ef-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a8ef-141">Close the page.</span></span>

