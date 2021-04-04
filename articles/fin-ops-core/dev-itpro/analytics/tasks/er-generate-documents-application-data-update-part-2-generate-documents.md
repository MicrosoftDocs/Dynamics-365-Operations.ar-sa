---
title: تصميم تكوينات لإنشاء مستندات تتضمن بيانات التطبيق
description: يصف هذا الموضوع كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني وارد. (الجزء 1 - استيراد التكوينات)
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563164"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="bafc4-104">تصميم تكوينات لإنشاء مستندات تتضمن بيانات التطبيق</span><span class="sxs-lookup"><span data-stu-id="bafc4-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bafc4-105">لإكمال الخطوات المذكورة في هذا الإجراء، يجب عليك أولاً إكمال الإجراء، التقارير الإلكترونية - إنشاء مستندات بواسطة تحديث بيانات التطبيق (الجزء 1: استيراد التكوينات)‬.</span><span class="sxs-lookup"><span data-stu-id="bafc4-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="bafc4-106">توضح الخطوات الواردة في هذا الإجراء كيفية تصميم تكوينات التقارير الإلكترونية لإنشاء مستند إلكتروني.</span><span class="sxs-lookup"><span data-stu-id="bafc4-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="bafc4-107">في هذا الإجراء، ستقوم بتشغيل تكوين التنسيق المستورد للتقارير الإلكترونية الذي تم إنشاؤها للشركة النموذجية، Litware, Inc. لإنشاء المستندات الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="bafc4-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="bafc4-108">تم إنشاء هذا الإجراء للمستخدمين الذين لديهم دور مسؤول النظام أو مطور التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="bafc4-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="bafc4-109">يمكن إتمام هذه الخطوات باستخدام مجموعة بيانات DEMF.</span><span class="sxs-lookup"><span data-stu-id="bafc4-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="bafc4-110">قبل أن تبدأ، قم بتغيير سياق البلد لشركة DEMF من DEU (ألمانيا) إلى BEL (بلجيكا).</span><span class="sxs-lookup"><span data-stu-id="bafc4-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="bafc4-111">انقر فوق إدارة المؤسسات > المؤسسات > الكيانات القانونية لتحديث رمز البلد في العنوان الرئيسي للكيان القانوني DEMF.</span><span class="sxs-lookup"><span data-stu-id="bafc4-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="bafc4-112">أعد تشغيل التطبيق.</span><span class="sxs-lookup"><span data-stu-id="bafc4-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="bafc4-113">تشغيل تنسيق التقارير الإلكترونية المستورد</span><span class="sxs-lookup"><span data-stu-id="bafc4-113">Run imported ER format</span></span>
1. <span data-ttu-id="bafc4-114">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="bafc4-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bafc4-115">في الشجرة، قم بتوسيع "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)".</span><span class="sxs-lookup"><span data-stu-id="bafc4-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="bafc4-116">في الشجرة، حدد "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نموذج)\نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (تنسيق)".</span><span class="sxs-lookup"><span data-stu-id="bafc4-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="bafc4-117">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="bafc4-117">Click Run.</span></span>
    * <span data-ttu-id="bafc4-118">قم بتشغيل إصدار المسودة لتكوين تنسيق التقارير الإلكترونية لإنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="bafc4-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="bafc4-119">في الحقل "إدخال اسم الملف"، اكتب "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="bafc4-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="bafc4-120">حدد اسم الملف.</span><span class="sxs-lookup"><span data-stu-id="bafc4-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="bafc4-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="bafc4-121">Click OK.</span></span>
    * <span data-ttu-id="bafc4-122">راجع ملف XML المنشأ.</span><span class="sxs-lookup"><span data-stu-id="bafc4-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="bafc4-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bafc4-123">Close the page.</span></span>
8. <span data-ttu-id="bafc4-124">انتقل إلى الضريبة > الإقرارات‬ > التجارة الخارجية > نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="bafc4-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="bafc4-125">افتح هذا النموذج لعرض حركات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المضمنة في المستند الإلكتروني المنشأ.</span><span class="sxs-lookup"><span data-stu-id="bafc4-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="bafc4-126">انقر فوق أرشيف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.</span><span class="sxs-lookup"><span data-stu-id="bafc4-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="bafc4-127">نظرًا لعدم احتواء تنسيق التقارير الإلكترونية الذي تم تنفيذه على أي إعدادات خاصة بتحديث بيانات التطبيق، لم تتم أرشفة تفاصيل تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي المكتمل.</span><span class="sxs-lookup"><span data-stu-id="bafc4-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="bafc4-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bafc4-128">Close the page.</span></span>
11. <span data-ttu-id="bafc4-129">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bafc4-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]