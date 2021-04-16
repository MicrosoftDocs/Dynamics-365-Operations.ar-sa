---
title: تعريفات التقارير في مصمم التقارير المالية
description: توفر هذه المقالة معلومات حول تعريفات التقارير.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755434"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="cb187-103">تعريفات التقارير في مصمم التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="cb187-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb187-104">توفر هذه المقالة معلومات حول تعريفات التقارير.</span><span class="sxs-lookup"><span data-stu-id="cb187-104">This article provides information about report definitions.</span></span> <span data-ttu-id="cb187-105">إن تعريف التقرير عبارة عن مكون تقرير (أو كتلة إنشاء) يستخدم تعريف صف وتعريف عمود وتعريف شجرة تقارير اختياري لإنشاء تقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="cb187-106">كما يوفر تعريف التقرير خيارات وإعدادات يمكنك استخدامها لتخصيص تقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="cb187-107">إن تعريف التقرير عبارة عن مكون تقرير (أو كتلة إنشاء) يستخدم تعريف صف وتعريف عمود وتعريف شجرة تقارير اختياري لإنشاء تقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="cb187-108">ويقدم تعريف التقرير أيضًا خيارات وإعدادات يمكنك استخدامها لتخصيص تقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="cb187-109">وبعد قيامك بتحديد تعريفات الصفوف وتعريفات الأعمدة، يجب الجمع بينها في تعريف تقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="cb187-110">وعند هذه النقطة، يمكنك أيضًا تحديد جوانب أخرى من التعريفات، مثل تاريخ التقرير ومستوى التفصيل.</span><span class="sxs-lookup"><span data-stu-id="cb187-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="cb187-111">ويمكنك بعد ذلك حفظ وإنشاء تقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-111">You can then save and generate a report.</span></span> <span data-ttu-id="cb187-112">تقدم التقارير المالية المستويات التالية للتفاصيل:</span><span class="sxs-lookup"><span data-stu-id="cb187-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="cb187-113">مالي</span><span class="sxs-lookup"><span data-stu-id="cb187-113">Financial</span></span>
- <span data-ttu-id="cb187-114">المالي والحساب</span><span class="sxs-lookup"><span data-stu-id="cb187-114">Financial and Account</span></span>
- <span data-ttu-id="cb187-115">المالي والحساب والحركة</span><span class="sxs-lookup"><span data-stu-id="cb187-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="cb187-116">ومع ذلك، قد لا تكون تفاصيل الحركة متوفرة في التقارير وفقًا لكيفية تخزين البيانات في نظام Microsoft Dynamics ERP.</span><span class="sxs-lookup"><span data-stu-id="cb187-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="cb187-117">إنشاء تعريف تقرير</span><span class="sxs-lookup"><span data-stu-id="cb187-117">Create a report definition</span></span>
1. <span data-ttu-id="cb187-118">في مصمم التقرير، في القائمة **ملف**، انقر فوق **جديد**، ثم حدد **تعريف التقرير**.</span><span class="sxs-lookup"><span data-stu-id="cb187-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="cb187-119">وحدد المعلومات المناسبة في علامة التبويب **تقرير**، و **إخراج وتوزيع**، و **الرؤوس والتذييلات**، و **إعدادات**.</span><span class="sxs-lookup"><span data-stu-id="cb187-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="cb187-120">محتويات تعريف التقرير</span><span class="sxs-lookup"><span data-stu-id="cb187-120">Contents of a report definition</span></span>
<span data-ttu-id="cb187-121">يصف الجدول التالي علامات التبويب في تعريف التقرير وكيفية استخدام المعلومات.</span><span class="sxs-lookup"><span data-stu-id="cb187-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cb187-122">علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="cb187-122">Tab</span></span></th>
<th><span data-ttu-id="cb187-123">الوصف</span><span class="sxs-lookup"><span data-stu-id="cb187-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cb187-124">التقرير</span><span class="sxs-lookup"><span data-stu-id="cb187-124">Report</span></span></td>
<td><span data-ttu-id="cb187-125">إنشاء تقرير أو تكوين تقرير أو تعديل تقرير موجود.</span><span class="sxs-lookup"><span data-stu-id="cb187-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb187-126">الإخراج والتوزيع</span><span class="sxs-lookup"><span data-stu-id="cb187-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="cb187-127">تغيير نوع الإخراج ووجهة التقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb187-128">الرؤوس والتذييلات</span><span class="sxs-lookup"><span data-stu-id="cb187-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="cb187-129">تحديد وتنسيق الرؤوس والتذييلات للتقرير.</span><span class="sxs-lookup"><span data-stu-id="cb187-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="cb187-130">على سبيل المثال، يمكنك إضافة نص أو صور إلى الرأس أو التذييل.</span><span class="sxs-lookup"><span data-stu-id="cb187-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="cb187-131">تدعم التقارير المالية ملفات bmp. وjpg. وpng. للصور.</span><span class="sxs-lookup"><span data-stu-id="cb187-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="cb187-132">كما يمكنك إضافة رمز النص التلقائي لإدراج معلومات أخرى، مثل اسم شركة، أو اسم التقرير، أو رقم الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cb187-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cb187-133">إعدادات</span><span class="sxs-lookup"><span data-stu-id="cb187-133">Settings</span></span></td>
<td><span data-ttu-id="cb187-134">تحديد إعدادات تعريف التقرير، مثل الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="cb187-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="cb187-135">التنسيق والمبالغ التقريبية</span><span class="sxs-lookup"><span data-stu-id="cb187-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="cb187-136">تنسيق تقارير التفاصيل</span><span class="sxs-lookup"><span data-stu-id="cb187-136">Format detail reports</span></span></li>
<li><span data-ttu-id="cb187-137">تنسيق أشجار التقارير</span><span class="sxs-lookup"><span data-stu-id="cb187-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="cb187-138">إنشاء تقرير استثناء</span><span class="sxs-lookup"><span data-stu-id="cb187-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="cb187-139">تحديد تحويل عملة</span><span class="sxs-lookup"><span data-stu-id="cb187-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="cb187-140">تفاصيل حساب التصفية والإجمالي الفرعي</span><span class="sxs-lookup"><span data-stu-id="cb187-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="cb187-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cb187-141">Additional resources</span></span>

[<span data-ttu-id="cb187-142">التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="cb187-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]