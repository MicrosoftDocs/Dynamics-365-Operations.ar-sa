---
title: إعداد التقارير المالية
description: تسمح التقارير المالية في تطبيق للأخصائيين العاملين في مجالات المال والأعمال بإنشاء القوائم المالية وصيانتها ونشرها وعرضها. إنها تتجاوز قيود التقارير التقليدية لكي تقدم لك مساعدة فعالة على صعيد تصميم مختلف أنواع التقارير.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cdfa9ed24d0456d9beaec03ebac89098131d0675
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771132"
---
# <a name="financial-reporting"></a><span data-ttu-id="f6079-104">إعداد التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="f6079-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6079-105">تسمح التقارير المالية في التطبيق للأخصائيين العاملين في مجالات المال والأعمال بإنشاء القوائم المالية وصيانتها ونشرها وعرضها.</span><span class="sxs-lookup"><span data-stu-id="f6079-105">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="f6079-106">إنها تتجاوز قيود التقارير التقليدية لكي تقدم لك مساعدة فعالة على صعيد تصميم مختلف أنواع التقارير.</span><span class="sxs-lookup"><span data-stu-id="f6079-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="f6079-107">تتضمن التقارير المالية ميزة دعم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="f6079-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="f6079-108">وبالتالي، ستكون أقسام الحساب أو أبعاده متوفرة على الفور.</span><span class="sxs-lookup"><span data-stu-id="f6079-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="f6079-109">لا حاجة إلى أدوات أو خطوات تكوين إضافية.</span><span class="sxs-lookup"><span data-stu-id="f6079-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="f6079-110">إعداد التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="f6079-110">Financial reporting setup</span></span>
<span data-ttu-id="f6079-111">تشتمل صفحة **إعداد التقارير المالية** على قائمة بجميع الأبعاد المالية في النظام.</span><span class="sxs-lookup"><span data-stu-id="f6079-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="f6079-112">**دفتر الأستاذ العام** \> **إعداد دفتر الأستاذ** \> **إعداد التقارير المالية**.</span><span class="sxs-lookup"><span data-stu-id="f6079-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="f6079-113">تشتمل صفحة **إعداد التقارير المالية** على قسمين يحددان البيانات التي تُبلغ عنها في التقارير المالية:</span><span class="sxs-lookup"><span data-stu-id="f6079-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="f6079-114">**علامة التبويب الأبعاد** - نظرًا لأن الشركات المختلفة تستخدم أبعاد وبنيات حسابات مختلفة، لا توجد أي طريقة لتحديد الترتيب الذي يريد به المستخدمون عرض جميع الأبعاد المالية في التقارير.</span><span class="sxs-lookup"><span data-stu-id="f6079-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="f6079-115">تتيح لك هذه الصفحة إمكانية تعيين الترتيب الذي ترغب في أن تظهر الأبعاد المالية به عند إنشاء وعرض تقرير في التقارير المالية.</span><span class="sxs-lookup"><span data-stu-id="f6079-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="f6079-116">**علامة التبويب سمات** حيث يمكنك تحديد ما إذا كنت تريد أن تكون قادرًا على استخدام **الموردين** و**العملاء** كسمات للتصفية وتصميم التقارير.</span><span class="sxs-lookup"><span data-stu-id="f6079-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="f6079-117">لن تكون التقارير المتعلقة بالعميل والمورد قيّمة إلا إذا لم تقم بإدخال عملاء أو موردين متعددين في قسيمة واحدة عند ترحيل الحركات.</span><span class="sxs-lookup"><span data-stu-id="f6079-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="f6079-118">سيضيف اختيار مورد و/أو عميل وقتًا إضافيًا إلى التكامل.</span><span class="sxs-lookup"><span data-stu-id="f6079-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="f6079-119">مكونات التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="f6079-119">Financial reporting components</span></span>
<span data-ttu-id="f6079-120">تسهل المكونات التالية للتقارير المالية إنشاء التقارير وعرضها وجدولتها.</span><span class="sxs-lookup"><span data-stu-id="f6079-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="f6079-121">المكون</span><span class="sxs-lookup"><span data-stu-id="f6079-121">Component</span></span>        | <span data-ttu-id="f6079-122">الوظائف</span><span class="sxs-lookup"><span data-stu-id="f6079-122">Functions</span></span> | <span data-ttu-id="f6079-123">المعلومات الإضافية</span><span class="sxs-lookup"><span data-stu-id="f6079-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="f6079-124">أداة تصميم التقارير</span><span class="sxs-lookup"><span data-stu-id="f6079-124">Report Designer</span></span>  | <span data-ttu-id="f6079-125">إنشاء كتل إنشاء التقارير التي يمكن دمجها لتحديد تقرير وإنشائه.</span><span class="sxs-lookup"><span data-stu-id="f6079-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="f6079-126">ويرشد معالج التقارير المستخدمين قليلي الخبرة خلال عملية التصميم.</span><span class="sxs-lookup"><span data-stu-id="f6079-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="f6079-127">وبإمكان المستخدمين المتقدمين إنشاء كتل إنشاء تقارير جديدة أو تعديل كتل إنشاء موجودة لتلبية متطلباتهم.</span><span class="sxs-lookup"><span data-stu-id="f6079-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="f6079-128">جداول التقارير</span><span class="sxs-lookup"><span data-stu-id="f6079-128">Report schedules</span></span> | <span data-ttu-id="f6079-129">جدولة تقرير واحد أو مجموعة من التقارير لتمكين إنشائها على أساس منتظم.</span><span class="sxs-lookup"><span data-stu-id="f6079-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="f6079-130">إنشاء التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="f6079-130">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="f6079-131">الميزات</span><span class="sxs-lookup"><span data-stu-id="f6079-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="f6079-132">الميزة</span><span class="sxs-lookup"><span data-stu-id="f6079-132">Feature</span></span></th>
<th><span data-ttu-id="f6079-133">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="f6079-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6079-134">مرونة تصميم التقارير</span><span class="sxs-lookup"><span data-stu-id="f6079-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="f6079-135">يوفر مصمم التقارير خيارات إعداد التقارير التالية عندما تقوم بتصميم تقرير:</span><span class="sxs-lookup"><span data-stu-id="f6079-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="f6079-136">حفظ مجموعات الأبعاد وإعادة استخدام الأبعاد لتقارير متعددة.</span><span class="sxs-lookup"><span data-stu-id="f6079-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="f6079-137">التحكم في كيفية تنسيق وعرض أوصاف الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="f6079-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="f6079-138">تحديد الحسابات أو الأبعاد التي تم حذفها من اللبنات الأساسية للتقارير.</span><span class="sxs-lookup"><span data-stu-id="f6079-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="f6079-139">تنسيق الرؤوس لتنبؤات التداول.</span><span class="sxs-lookup"><span data-stu-id="f6079-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="f6079-140">تعاون التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="f6079-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="f6079-141">تساعدك الميزات التالية في إدارة إنشاء التقارير وتوزيعها:</span><span class="sxs-lookup"><span data-stu-id="f6079-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="f6079-142">جدولة التقارير لتمكين إنشائها تلقائيًا على أساس يومي أو أسبوعي أو شهري أو سنوي.</span><span class="sxs-lookup"><span data-stu-id="f6079-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="f6079-143">التصدير إلى تنسيق XPS للقراءة فقط، مما يوفر مستوى أمان أفضل للمستندات عبر التواقيع الرقمية.</span><span class="sxs-lookup"><span data-stu-id="f6079-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="f6079-144">تصدير إلى ورقة عمل Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f6079-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="f6079-145">لمشاركة التقارير، يمكنك إنشاء رسائل بريد إلكتروني تحتوي على ارتباطات إلى التقارير.</span><span class="sxs-lookup"><span data-stu-id="f6079-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="f6079-146">عرض التقارير التفاعلي</span><span class="sxs-lookup"><span data-stu-id="f6079-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="f6079-147">تُمكّنك الميزات التفاعلية من تنفيذ بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="f6079-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="f6079-148">تغيير تاريخ التقرير للتقرير الذي تقوم بعرضه.</span><span class="sxs-lookup"><span data-stu-id="f6079-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="f6079-149">تغيير عملة التقرير للتقرير الذي تقوم بعرضه.</span><span class="sxs-lookup"><span data-stu-id="f6079-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="f6079-150">عرض التقرير في طريقة عرض مفصلة أو ملخصة.</span><span class="sxs-lookup"><span data-stu-id="f6079-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="f6079-151">إضافة عوامل تصفية الأبعاد بحيث يتحدد محتوى التقرير من خلال بُعد معين أو مجموعة أبعاد.</span><span class="sxs-lookup"><span data-stu-id="f6079-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="f6079-152">إضافة عوامل تصفية السمات بحيث يتحدد محتوى التقرير من خلال سمة معينة أو مجموعة سمات.</span><span class="sxs-lookup"><span data-stu-id="f6079-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="f6079-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f6079-153">Additional resources</span></span>
[<span data-ttu-id="f6079-154">إنشاء التقارير المالية</span><span class="sxs-lookup"><span data-stu-id="f6079-154">Generate financial reports</span></span>](generate-financial-report.md)