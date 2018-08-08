---
title: "استيراد البيانات التاريخية‬ للتنبؤات بالطلب"
description: "للحصول على تنبؤات بالطلب‬ دقيقة، تحتاج إلى بيانات تاريخية لكل صنف أو مفتاح توزيع الصنف. يشرح هذا الموضوع كيفية استخدام كيانات البيانات لاستيراد بيانات الطلب التاريخية من أي نظام، بحيث تحصل على سجل طويل لبيانات التنبؤات بالطلب."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 018694c79c6dd64e19b010848aad8acd36b0a9a8
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="ad61f-104">استيراد البيانات التاريخية‬ للتنبؤات بالطلب</span><span class="sxs-lookup"><span data-stu-id="ad61f-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad61f-105">للمساعدة في ضمان دقة التنبؤات بالطلب، يجب أن تكون بيانات الطلب التاريخية لديك بمقدار مماثل لما يمكنك الحصول عليه لكل صنف أو مفتاح توزيع الصنف.</span><span class="sxs-lookup"><span data-stu-id="ad61f-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="ad61f-106">إذا لم يكن قد تم بعد استيراد بيانات الطلب التاريخية، فاستخدم كيان البيانات **الطلب الخارجي التاريخي** (ReqDemPlanHistoricalExternalDemandEntity) في in Microsoft Dynamics 365 for Finance and Operations لاستيرادها.</span><span class="sxs-lookup"><span data-stu-id="ad61f-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="ad61f-107">في مساحة العمل **إدارة البيانات**، يمكنك الاطلاع على نظرة عامة على كافة الحقول الموجودة في الكيان.</span><span class="sxs-lookup"><span data-stu-id="ad61f-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="ad61f-108">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="ad61f-109">انقر فوق لوحة **كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="ad61f-110">ابحث في قائمة الكيانات عن **الطلب الخارجي التاريخي**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="ad61f-111">انقر فوق **الحقول الهدف**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-111">Click **Target fields**.</span></span> <span data-ttu-id="ad61f-112">تُعتبر حقول الكيانات التالية إلزامية: الموقع (**DeliveringSiteId**)، والتاريخ (**DemandDate**) والكمية، (**DemandQuantity**)، وإما رقم الصنف (**ItemNumber**) أو مفتاح توزيع الصنف (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="ad61f-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="ad61f-113">لاستخدام كيان البيانات، يجب أن يكون لديك ملف Microsoft Excel أو ملف قيم تفصلها الفواصل (CSV) يحتوي على بيانات الطلب التاريخية.</span><span class="sxs-lookup"><span data-stu-id="ad61f-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="ad61f-114">يوضح المثال التالي كيفية استيراد البيانات من ملف CSV.</span><span class="sxs-lookup"><span data-stu-id="ad61f-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="ad61f-115">مثال</span><span class="sxs-lookup"><span data-stu-id="ad61f-115">Example</span></span>

<span data-ttu-id="ad61f-116">يمكن استخدام الملف التالي كمثال.</span><span class="sxs-lookup"><span data-stu-id="ad61f-116">You can use the following file as an example.</span></span> <span data-ttu-id="ad61f-117">قم بتنزيل [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="ad61f-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="ad61f-118">يحتوي هذا الملف على بيانات الطلب التاريخية للصنف D0001.</span><span class="sxs-lookup"><span data-stu-id="ad61f-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="ad61f-119">إنه يحتوي على الحقول الإلزامية التالية فقط: الموقع والكمية وتاريخ الطلب.</span><span class="sxs-lookup"><span data-stu-id="ad61f-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="ad61f-120">حدد الشركة لاستيراد بيانات الطلب التاريخية إليها.</span><span class="sxs-lookup"><span data-stu-id="ad61f-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="ad61f-121">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="ad61f-122">انقر فوق اللوحة **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="ad61f-123">أدخل اسمًا لمشروع الاستيراد، مثل **استيراد الطلب التاريخي للصنف D0001**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="ad61f-124">في الحقل **تنسيق بيانات المصدر** ، حدد تنسيق الملف للملف الذي تريد استيراده.</span><span class="sxs-lookup"><span data-stu-id="ad61f-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="ad61f-125">لاستيراد الملف HistoricalDemandData لهذا المثال، حدد **CSV**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="ad61f-126">في الحقل **اسم الكيان**، حدد **الطلب الخارجي التاريخي‬**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="ad61f-127">احفظ الملف في الكمبيوتر، ثم قم بتحميله.</span><span class="sxs-lookup"><span data-stu-id="ad61f-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="ad61f-128">انقر فوق **استيراد**.</span><span class="sxs-lookup"><span data-stu-id="ad61f-128">Click **Import**.</span></span>
9. <span data-ttu-id="ad61f-129">تفتح صفحة **ملخص التنفيذ** بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="ad61f-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="ad61f-130">تحقق من صحة البيانات التي تم استيرادها في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad61f-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="ad61f-131">بعد استيراد بيانات الطلب التاريخية، يمكنك إنشاء تنبؤ بالطلب.</span><span class="sxs-lookup"><span data-stu-id="ad61f-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad61f-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ad61f-132">Additional resources</span></span>

[<span data-ttu-id="ad61f-133">إنشاء تنبؤ أساسي إحصائي</span><span class="sxs-lookup"><span data-stu-id="ad61f-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

