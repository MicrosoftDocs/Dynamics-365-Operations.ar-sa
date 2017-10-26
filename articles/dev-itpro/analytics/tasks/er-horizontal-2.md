--- 
title: "تشغيل تنسيق يستخدم نطاقات قابلة للتوسيع أفقيًا لإضافة الأعمدة ديناميكيًا في تقارير Excel للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a><span data-ttu-id="b41c8-103">تشغيل تنسيق يستخدم نطاقات قابلة للتوسيع أفقيًا لإضافة الأعمدة ديناميكيًا في تقارير Excel للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="b41c8-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b41c8-104">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا.</span><span class="sxs-lookup"><span data-stu-id="b41c8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="b41c8-105">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="b41c8-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b41c8-106">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1: تصميم التنسيق)‬"</span><span class="sxs-lookup"><span data-stu-id="b41c8-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="b41c8-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="b41c8-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="b41c8-108">البحث عن تنسيق مُنشأ</span><span class="sxs-lookup"><span data-stu-id="b41c8-108">Find created format</span></span>
1. <span data-ttu-id="b41c8-109">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="b41c8-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b41c8-110">في الشجرة، قم بتوسيع "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="b41c8-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b41c8-111">في الشجرة، حدد "نموذج الأبعاد المالية\نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا‬".</span><span class="sxs-lookup"><span data-stu-id="b41c8-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="b41c8-112">تنفيذ التنسيق لإنشاء مخرجات Excel</span><span class="sxs-lookup"><span data-stu-id="b41c8-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="b41c8-113">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="b41c8-113">Click Run.</span></span>
2. <span data-ttu-id="b41c8-114">في الحقل "اسم البُعد"، اكتب "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="b41c8-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="b41c8-115">في الحقل "اسم البُعد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="b41c8-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="b41c8-116">لتحديد كافة الأبعاد للشركة الحالية، قم بإدخال التالي: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="b41c8-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="b41c8-117">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="b41c8-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b41c8-118">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="b41c8-118">Click Filter.</span></span>
5. <span data-ttu-id="b41c8-119">حدد الصف في جدول دفتر يومية دفتر الأستاذ وحقل "رقم دُفعة دفتر اليومية‬".</span><span class="sxs-lookup"><span data-stu-id="b41c8-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="b41c8-120">في الحقل "المعايير، اكتب "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="b41c8-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="b41c8-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="b41c8-121">00057..00058</span></span>  
7. <span data-ttu-id="b41c8-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b41c8-122">Click OK.</span></span>
8. <span data-ttu-id="b41c8-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="b41c8-123">Click OK.</span></span>
    * <span data-ttu-id="b41c8-124">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="b41c8-124">Review the generated output.</span></span> <span data-ttu-id="b41c8-125">لاحظ أن ملف Excel الذي تم إنشاؤه حديثًا يحتوي على عدد الأعمدة نفسه الذي تم تحديده للإبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="b41c8-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="b41c8-126">يمثل رأس التقرير في هذه الأعمدة أسماء الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="b41c8-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="b41c8-127">وتمثل بنود الحركات في هذه الأعمدة الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="b41c8-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="b41c8-128">شغّل هذا التقرير وحدد أبعادًا مختلفة لمعرفة ما إذا كان التقرير لا يعتمد على عدد الأبعاد المحددة أو عدد الأبعاد التي تم تكوينها لهذا المثيل من Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="b41c8-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  

