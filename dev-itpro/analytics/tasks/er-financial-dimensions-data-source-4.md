--- 
title: "تشغيل تقرير يستخدم الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e319c9d11ccc4311437ce1e74d4f6c8be0e0de35
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="d5c45-103">تشغيل تقرير يستخدم الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="d5c45-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5c45-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين نموذج التقارير الإلكترونية لاستخدام الأبعاد المالية كمصدر بيانات للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d5c45-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d5c45-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="d5c45-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d5c45-106">لإتمام هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام الأبعاد المالية كمصدر بيانات (الجزء 3: تصميم التقرير)‬".</span><span class="sxs-lookup"><span data-stu-id="d5c45-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="d5c45-107">يجب أيضًا تكوين أنواع المستندات الافتراضية في صفحة محددات ‏‫إعداد التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d5c45-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="d5c45-108">يتم أيضًا تعيين أنواع المستندات الافتراضية عند تنزيل واستيراد أي تكوين للتقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="d5c45-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="d5c45-109">تشغيل تقرير</span><span class="sxs-lookup"><span data-stu-id="d5c45-109">Run report</span></span>
1. <span data-ttu-id="d5c45-110">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="d5c45-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d5c45-111">في الشجرة، قم بتوسيع "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="d5c45-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d5c45-112">في الشجرة، حدد "نموذج الأبعاد المالية\تقرير دفتر يومية دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="d5c45-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="d5c45-113">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="d5c45-113">Click Run.</span></span>
5. <span data-ttu-id="d5c45-114">في الحقل "اسم البُعد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="d5c45-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="d5c45-115">لتحديد كافة الأبعاد في الشركة الحالية، قم بإدخال التالي: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="d5c45-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="d5c45-116">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="d5c45-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="d5c45-117">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="d5c45-117">Click Filter.</span></span>
8. <span data-ttu-id="d5c45-118">حدد الصف في جدول دفتر يومية دفتر الأستاذ وحقل "رقم دُفعة دفتر اليومية‬".</span><span class="sxs-lookup"><span data-stu-id="d5c45-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="d5c45-119">في الحقل "المعايير، اكتب ''00057".</span><span class="sxs-lookup"><span data-stu-id="d5c45-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="d5c45-120">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d5c45-120">Click OK.</span></span>
11. <span data-ttu-id="d5c45-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="d5c45-121">Click OK.</span></span>
    * <span data-ttu-id="d5c45-122">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="d5c45-122">Review the generated output.</span></span> <span data-ttu-id="d5c45-123">لاحظ أنه بالنسبة إلى كل حركة من الدُفعة المحددة، يتم تقديم الأبعاد المالية من مجموعة الأبعاد المناظرة.</span><span class="sxs-lookup"><span data-stu-id="d5c45-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="d5c45-124">شغّل هذا التقرير وحدد أبعادًا مختلفة لمعرفة ما إذا كان التقرير لا يعتمد على عدد الأبعاد المحددة أو عدد الأبعاد التي تم تكوينها لهذا المثيل من Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="d5c45-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


