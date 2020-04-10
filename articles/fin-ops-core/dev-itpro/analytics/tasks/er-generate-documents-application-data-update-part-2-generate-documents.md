---
title: تصميم تكوينات لإنشاء مستندات تتضمن بيانات التطبيق
description: لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 1 - استيراد التكوينات)‬.
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
ms.openlocfilehash: 0ca80a2cc1e58723d1f1b39c1fde003fa990a93c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142422"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="6d1d5-103">تصميم تكوينات لإنشاء مستندات تتضمن بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="6d1d5-103">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d1d5-104">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 1: استيراد التكوينات)‬.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="6d1d5-105">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="6d1d5-106">في هذا الإجراء، ستقوم بتشغيل تكوين التنسيق المستورد للتقارير الإلكترونية الذي تم إنشاؤها للشركة النموذجية، Litware, Inc. لإنشاء المستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="6d1d5-107">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="6d1d5-108">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="6d1d5-109">قبل أن تبدأ، قم بتغيير سياق البلد لشركة DEMF من DEU (ألمانيا) إلى BEL (بلجيكا).</span><span class="sxs-lookup"><span data-stu-id="6d1d5-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="6d1d5-110">انقر فوق إدارة المؤسسات > المؤسسات > الكيانات القانونية لتحديث رمز البلد في العنوان الرئيسي للكيان القانوني DEMF.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="6d1d5-111">أعد تشغيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="6d1d5-112">تشغيل تنسيق التقارير الإلكترونية المستورد</span><span class="sxs-lookup"><span data-stu-id="6d1d5-112">Run imported ER format</span></span>
1. <span data-ttu-id="6d1d5-113">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6d1d5-114">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="6d1d5-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="6d1d5-115">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تنسيق)".</span><span class="sxs-lookup"><span data-stu-id="6d1d5-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="6d1d5-116">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="6d1d5-116">Click Run.</span></span>
    * <span data-ttu-id="6d1d5-117">قم بتشغيل إصدار المسودة لتكوين تنسيق التقارير الإلكترونية لإنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="6d1d5-118">في الحقل "إدخال اسم الملف"، اكتب "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="6d1d5-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="6d1d5-119">حدد اسم الملف.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="6d1d5-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6d1d5-120">Click OK.</span></span>
    * <span data-ttu-id="6d1d5-121">راجع ملف XML المنشأ.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="6d1d5-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-122">Close the page.</span></span>
8. <span data-ttu-id="6d1d5-123">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="6d1d5-124">افتح هذا النموذج لعرض حركات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المضمنة في المستند الإلكتروني المنشأ.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="6d1d5-125">انقر فوق أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="6d1d5-126">نظرًا لعدم احتواء تنسيق التقارير الإلكترونية الذي تم تنفيذه على أي إعدادات خاصة بتحديث بيانات التطبيق، لم تتم أرشفة تفاصيل تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المكتمل.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="6d1d5-127">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-127">Close the page.</span></span>
11. <span data-ttu-id="6d1d5-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="6d1d5-128">Close the page.</span></span>

