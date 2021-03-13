---
title: استيراد البيانات التاريخية‬ للتنبؤات بالطلب
description: للحصول على تنبؤات بالطلب‬ دقيقة، تحتاج إلى بيانات تاريخية لكل صنف أو مفتاح توزيع الصنف. يشرح هذا الموضوع كيفية استخدام كيانات البيانات لاستيراد بيانات الطلب التاريخية من أي نظام، بحيث تحصل على سجل طويل لبيانات التنبؤات بالطلب.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6ba2e1a3a884d29bff491f914aa2d5f9ece2b84
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154217"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="04653-104">استيراد البيانات التاريخية‬ للتنبؤات بالطلب</span><span class="sxs-lookup"><span data-stu-id="04653-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04653-105">للمساعدة في ضمان دقة التنبؤات بالطلب، يجب أن تكون بيانات الطلب التاريخية لديك بمقدار مماثل لما يمكنك الحصول عليه لكل صنف أو مفتاح توزيع الصنف.</span><span class="sxs-lookup"><span data-stu-id="04653-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="04653-106">إذا لم يكن قد تم بعد استيراد بيانات الطلب التاريخية، فاستخدم كيان البيانات **الطلب الخارجي التاريخي‬** (ReqDemPlanHistoricalExternalDemandEntity) في Dynamics 365 Supply Chain Management لاستيرادها.</span><span class="sxs-lookup"><span data-stu-id="04653-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="04653-107">في مساحة العمل **إدارة البيانات**، يمكنك الاطلاع على نظرة عامة على كافة الحقول الموجودة في الكيان.</span><span class="sxs-lookup"><span data-stu-id="04653-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="04653-108">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="04653-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="04653-109">حدد لوحة **كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="04653-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="04653-110">ابحث في قائمة الكيانات عن **الطلب الخارجي التاريخي**.</span><span class="sxs-lookup"><span data-stu-id="04653-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="04653-111">حدد **الحقول المستهدفة**.</span><span class="sxs-lookup"><span data-stu-id="04653-111">Select **Target fields**.</span></span> <span data-ttu-id="04653-112">تُعتبر حقول الكيانات التالية إلزامية: الموقع (**DeliveringSiteId**)، والتاريخ (**DemandDate**) والكمية، (**DemandQuantity**)، وإما رقم الصنف (**ItemNumber**) أو مفتاح توزيع الصنف (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="04653-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="04653-113">لاستخدام كيان البيانات، يجب أن يكون لديك ملف Microsoft Excel أو ملف قيم تفصلها الفواصل (CSV) يحتوي على بيانات الطلب التاريخية.</span><span class="sxs-lookup"><span data-stu-id="04653-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="04653-114">يوضح المثال التالي كيفية استيراد البيانات من ملف CSV.</span><span class="sxs-lookup"><span data-stu-id="04653-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="04653-115">لمزيد من المعلومات حول كيفيه استيراد البيانات، بما في ذلك كيفيه تنظيف البيانات بعد الاستيراد، راجع [نظره عامه حول استيراد البيانات](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)وتصديرها وموضوعاتها ذات صله.</span><span class="sxs-lookup"><span data-stu-id="04653-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="04653-116">مثال</span><span class="sxs-lookup"><span data-stu-id="04653-116">Example</span></span>

<span data-ttu-id="04653-117">يمكن استخدام الملف التالي كمثال.</span><span class="sxs-lookup"><span data-stu-id="04653-117">You can use the following file as an example.</span></span> <span data-ttu-id="04653-118">قم بتنزيل [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="04653-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="04653-119">يحتوي هذا الملف على بيانات الطلب التاريخية للصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="04653-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="04653-120">إنه يحتوي على الحقول الإلزامية التالية فقط: الموقع والكمية وتاريخ الطلب.</span><span class="sxs-lookup"><span data-stu-id="04653-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="04653-121">حدد الشركة لاستيراد بيانات الطلب التاريخية إليها.</span><span class="sxs-lookup"><span data-stu-id="04653-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="04653-122">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="04653-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="04653-123">تحديد تجانب **الاستيراد**.</span><span class="sxs-lookup"><span data-stu-id="04653-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="04653-124">أدخل اسمًا لمشروع الاستيراد، مثل **استيراد الطلب التاريخي للصنف D0001**.</span><span class="sxs-lookup"><span data-stu-id="04653-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="04653-125">في الحقل **تنسيق بيانات المصدر** ، حدد تنسيق الملف للملف الذي تريد استيراده.</span><span class="sxs-lookup"><span data-stu-id="04653-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="04653-126">لاستيراد الملف HistoricalDemandData لهذا المثال، حدد **CSV**.</span><span class="sxs-lookup"><span data-stu-id="04653-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="04653-127">في الحقل **اسم الكيان**، حدد **الطلب الخارجي التاريخي‬**.</span><span class="sxs-lookup"><span data-stu-id="04653-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="04653-128">احفظ الملف في الكمبيوتر، ثم قم بتحميله.</span><span class="sxs-lookup"><span data-stu-id="04653-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="04653-129">حدد **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="04653-129">Select **Import**.</span></span>
9. <span data-ttu-id="04653-130">تفتح صفحة **ملخص التنفيذ** بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="04653-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="04653-131">تحقق من صحة البيانات التي تم استيرادها في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="04653-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="04653-132">بعد استيراد بيانات الطلب التاريخية، يمكنك إنشاء تنبؤ بالطلب.</span><span class="sxs-lookup"><span data-stu-id="04653-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04653-133">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="04653-133">Additional resources</span></span>

[<span data-ttu-id="04653-134">إنشاء تنبؤ أساسي إحصائي</span><span class="sxs-lookup"><span data-stu-id="04653-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="04653-135">نظرة عامة حول مهام استيراد البيانات وتصديرها</span><span class="sxs-lookup"><span data-stu-id="04653-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)
