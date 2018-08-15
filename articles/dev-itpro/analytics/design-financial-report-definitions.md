---
title: "تعريفات التقارير في مصمم التقارير المالية"
description: "توفر هذه المقالة معلومات حول تعريفات التقارير. إن تعريف التقرير عبارة عن مكون تقرير (أو كتلة إنشاء) يستخدم تعريف صف وتعريف عمود وتعريف شجرة تقارير اختياري لإنشاء تقرير. كما يوفر تعريف التقرير خيارات وإعدادات يمكنك استخدامها لتخصيص تقرير."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 322f1cca32053224e1cd6dbaf29c098b983b5e1f
ms.contentlocale: ar-sa
ms.lasthandoff: 08/13/2018

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="749e6-105">تعريفات التقارير في مصمم التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="749e6-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="749e6-106">توفر هذه المقالة معلومات حول تعريفات التقارير.</span><span class="sxs-lookup"><span data-stu-id="749e6-106">This article provides information about report definitions.</span></span> <span data-ttu-id="749e6-107">إن تعريف التقرير عبارة عن مكون تقرير (أو كتلة إنشاء) يستخدم تعريف صف وتعريف عمود وتعريف شجرة تقارير اختياري لإنشاء تقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="749e6-108">كما يوفر تعريف التقرير خيارات وإعدادات يمكنك استخدامها لتخصيص تقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="749e6-109">إن تعريف التقرير عبارة عن مكون تقرير (أو كتلة إنشاء) يستخدم تعريف صف وتعريف عمود وتعريف شجرة تقارير اختياري لإنشاء تقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="749e6-110">ويقدم تعريف التقرير أيضًا خيارات وإعدادات يمكنك استخدامها لتخصيص تقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="749e6-111">وبعد قيامك بتحديد تعريفات الصفوف وتعريفات الأعمدة، يجب الجمع بينها في تعريف تقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="749e6-112">وعند هذه النقطة، يمكنك أيضًا تحديد جوانب أخرى من التعريفات، مثل تاريخ التقرير ومستوى التفصيل.</span><span class="sxs-lookup"><span data-stu-id="749e6-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="749e6-113">ويمكنك بعد ذلك حفظ وإنشاء تقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-113">You can then save and generate a report.</span></span> <span data-ttu-id="749e6-114">تقدم التقارير المالية المستويات التالية للتفاصيل:</span><span class="sxs-lookup"><span data-stu-id="749e6-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="749e6-115">مالي</span><span class="sxs-lookup"><span data-stu-id="749e6-115">Financial</span></span>
- <span data-ttu-id="749e6-116">المالي والحساب</span><span class="sxs-lookup"><span data-stu-id="749e6-116">Financial and Account</span></span>
- <span data-ttu-id="749e6-117">المالي والحساب والحركة</span><span class="sxs-lookup"><span data-stu-id="749e6-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="749e6-118">ومع ذلك، تبعاً لكيفية تخزين البيانات في نظام Microsoft Dynamics ERP، قد لا تكون تفاصيل الحركة متوفرة في التقارير.</span><span class="sxs-lookup"><span data-stu-id="749e6-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="749e6-119">إنشاء تعريف تقرير</span><span class="sxs-lookup"><span data-stu-id="749e6-119">Create a report definition</span></span>
1. <span data-ttu-id="749e6-120">في مصمم التقرير، في القائمة **ملف**، انقر فوق **جديد**، ثم حدد **تعريف التقرير**.</span><span class="sxs-lookup"><span data-stu-id="749e6-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="749e6-121">وحدد المعلومات المناسبة في علامة التبويب **تقرير**، و**إخراج وتوزيع**، و**الرؤوس والتذييلات**، و**إعدادات**.</span><span class="sxs-lookup"><span data-stu-id="749e6-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="749e6-122">محتويات تعريف التقرير</span><span class="sxs-lookup"><span data-stu-id="749e6-122">Contents of a report definition</span></span>
<span data-ttu-id="749e6-123">يصف الجدول التالي علامات التبويب في تعريف التقرير وكيفية استخدام المعلومات.</span><span class="sxs-lookup"><span data-stu-id="749e6-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="749e6-124">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="749e6-124">Tab</span></span></th>
<th><span data-ttu-id="749e6-125">الوصف</span><span class="sxs-lookup"><span data-stu-id="749e6-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="749e6-126">التقرير</span><span class="sxs-lookup"><span data-stu-id="749e6-126">Report</span></span></td>
<td><span data-ttu-id="749e6-127">إنشاء تقرير أو تكوين تقرير أو تعديل تقرير موجود.</span><span class="sxs-lookup"><span data-stu-id="749e6-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="749e6-128">الإخراج والتوزيع</span><span class="sxs-lookup"><span data-stu-id="749e6-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="749e6-129">تغيير نوع الإخراج ووجهة التقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="749e6-130">الرؤوس والتذييلات</span><span class="sxs-lookup"><span data-stu-id="749e6-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="749e6-131">تحديد وتنسيق الرؤوس والتذييلات للتقرير.</span><span class="sxs-lookup"><span data-stu-id="749e6-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="749e6-132">على سبيل المثال، يمكنك إضافة نص أو صور إلى الرأس أو التذييل.</span><span class="sxs-lookup"><span data-stu-id="749e6-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="749e6-133">تدعم التقارير المالية ملفات bmp. وjpg. وpng. للصور.</span><span class="sxs-lookup"><span data-stu-id="749e6-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="749e6-134">كما يمكنك إضافة رمز النص التلقائي لإدراج معلومات أخرى، مثل اسم شركة، أو اسم التقرير، أو رقم الصفحة.</span><span class="sxs-lookup"><span data-stu-id="749e6-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="749e6-135">إعدادات</span><span class="sxs-lookup"><span data-stu-id="749e6-135">Settings</span></span></td>
<td><span data-ttu-id="749e6-136">تحديد إعدادات تعريف التقرير، مثل الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="749e6-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="749e6-137">التنسيق والمبالغ التقريبية</span><span class="sxs-lookup"><span data-stu-id="749e6-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="749e6-138">تنسيق تقارير التفاصيل</span><span class="sxs-lookup"><span data-stu-id="749e6-138">Format detail reports</span></span></li>
<li><span data-ttu-id="749e6-139">تنسيق أشجار التقارير</span><span class="sxs-lookup"><span data-stu-id="749e6-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="749e6-140">إنشاء تقرير استثناء</span><span class="sxs-lookup"><span data-stu-id="749e6-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="749e6-141">تحديد تحويل عملة</span><span class="sxs-lookup"><span data-stu-id="749e6-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="749e6-142">تفاصيل حساب التصفية والإجمالي الفرعي</span><span class="sxs-lookup"><span data-stu-id="749e6-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="749e6-143">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="749e6-143">Additional resources</span></span>

[<span data-ttu-id="749e6-144">التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="749e6-144">Financial reporting</span></span>](financial-reporting-intro.md)

