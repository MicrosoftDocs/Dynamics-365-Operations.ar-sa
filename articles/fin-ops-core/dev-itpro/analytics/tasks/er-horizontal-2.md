---
title: التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 2 - تشغيل التنسيق)
description: يوضح هذا الموضوع كيفيه تكوين تنسيق اعداد التقارير الكترونيه (ER) لإنشاء تقارير كملفات أوبينكسمل (Excel). (جزء 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744977"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="cf287-104">التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 2 - تشغيل التنسيق)</span><span class="sxs-lookup"><span data-stu-id="cf287-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cf287-105">تشرح الخطوات التالية كيف يستطيع مستخدم تم تعيينه إلى دور مسؤول النظام أو دور مطور التقارير الإلكترونية تكوين تنسيق التقارير الإلكترونية لإنشاء التقارير كملفات أوراق عمل (Excel) تنسيق OPENXML حيث يمكن إنشاء الأعمدة المطلوبة بطريقة ديناميكية كنطاقات قابلة للتوسيع أفقيًا.</span><span class="sxs-lookup"><span data-stu-id="cf287-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="cf287-106">يمكن تنفيذ هذه الخطوات في شركة DEMF.</span><span class="sxs-lookup"><span data-stu-id="cf287-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="cf287-107">لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "التقارير الإلكترونية - استخدام النطاقات القابلة للتوسيع أفقيًا لإضافة الأعمدة بشكل حيوي في تقارير Excel (الجزء 1: تصميم التنسيق)‬"</span><span class="sxs-lookup"><span data-stu-id="cf287-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="cf287-108">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="cf287-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="cf287-109">البحث عن تنسيق مُنشأ</span><span class="sxs-lookup"><span data-stu-id="cf287-109">Find created format</span></span>
1. <span data-ttu-id="cf287-110">انتقل إلى إدارة المؤسسة >إعداد التقارير الإلكتروني >التكوينات.</span><span class="sxs-lookup"><span data-stu-id="cf287-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="cf287-111">في الشجرة، قم بتوسيع "نموذج الأبعاد المالية".</span><span class="sxs-lookup"><span data-stu-id="cf287-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="cf287-112">في الشجرة، حدد "نموذج الأبعاد المالية\نموذج تقرير مع نطاقات قابلة للتوسيع أفقيًا‬".</span><span class="sxs-lookup"><span data-stu-id="cf287-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="cf287-113">تنفيذ التنسيق لإنشاء مخرجات Excel</span><span class="sxs-lookup"><span data-stu-id="cf287-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="cf287-114">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="cf287-114">Click Run.</span></span>
2. <span data-ttu-id="cf287-115">في الحقل "اسم البُعد"، اكتب "BusinessUnit;CostCenter;Department".</span><span class="sxs-lookup"><span data-stu-id="cf287-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="cf287-116">في الحقل "اسم البُعد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="cf287-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="cf287-117">لتحديد كافة الأبعاد للشركة الحالية، قم بإدخال التالي: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="cf287-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="cf287-118">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="cf287-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="cf287-119">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="cf287-119">Click Filter.</span></span>
5. <span data-ttu-id="cf287-120">حدد الصف في جدول دفتر يومية دفتر الأستاذ وحقل "رقم دُفعة دفتر اليومية‬".</span><span class="sxs-lookup"><span data-stu-id="cf287-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="cf287-121">في الحقل "المعايير، اكتب "00057..00058".</span><span class="sxs-lookup"><span data-stu-id="cf287-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="cf287-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="cf287-122">00057..00058</span></span>  
7. <span data-ttu-id="cf287-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cf287-123">Click OK.</span></span>
8. <span data-ttu-id="cf287-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="cf287-124">Click OK.</span></span>
    * <span data-ttu-id="cf287-125">اعمل على مراجعة المخرجات المنشأة.</span><span class="sxs-lookup"><span data-stu-id="cf287-125">Review the generated output.</span></span> <span data-ttu-id="cf287-126">لاحظ أن ملف Excel الذي تم إنشاؤه حديثًا يحتوي على عدد الأعمدة نفسه الذي تم تحديده للإبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="cf287-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="cf287-127">يمثل رأس التقرير في هذه الأعمدة أسماء الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="cf287-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="cf287-128">وتمثل بنود الحركات في هذه الأعمدة الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="cf287-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="cf287-129">شغّل هذا التقرير وجدد أبعادً مختلفة لمعرفة ما إذا كان التقرير لا يعتمد على عدد الأبعاد المحددة أو عدد الأبعاد التي تم تكوينها لهذا المثيل.</span><span class="sxs-lookup"><span data-stu-id="cf287-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]