---
title: إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب
description: يصف هذا المقال كيفية استبعاد القيم المتطرفة من البيانات التاريخية التي يتم استخدامها لحساب التنبؤ بطلب. وباستبعاد الأخطاء، يمكنك تحسين دقة التنبؤ.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2131ae11e634f9ced0d9696acb61d7b8a94c59cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841805"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="647ae-104">إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="647ae-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="647ae-105">يصف هذا المقال كيفية استبعاد القيم المتطرفة من البيانات التاريخية التي يتم استخدامها لحساب التنبؤ بطلب.</span><span class="sxs-lookup"><span data-stu-id="647ae-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="647ae-106">وباستبعاد الأخطاء، يمكنك تحسين دقة التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="647ae-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="647ae-107">يمكنك استبعاد القيم المتطرفة لتحسين دقة التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="647ae-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="647ae-108">هذه المهمة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="647ae-108">This is an optional task.</span></span> <span data-ttu-id="647ae-109">وفيما يلي نظرة عامة على العملية:</span><span class="sxs-lookup"><span data-stu-id="647ae-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="647ae-110">انقر فوق **التخطيط الرئيسي** &gt; **إعداد‏‎** &gt; **التنبؤ بالطلب** &gt; **‎إزالة الأخطاء** لفتح صفحة **إزالة الأخطاء**، حيث يمكنك استخدام استعلام لتحديد الحركات لاستبعادها.</span><span class="sxs-lookup"><span data-stu-id="647ae-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="647ae-111">حدد الشركة التي ينطبق عليها الاستعلام، ثم أدخل اسمًا ووصفًا.</span><span class="sxs-lookup"><span data-stu-id="647ae-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="647ae-112">ويتم تعيين حقل **تاريخ الاستعلام** تلقائياً تعيين إلى التاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="647ae-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="647ae-113">حدد خانة الاختيار **نشطة** لاستبعاد الحركات التي تم العثور عليها من قِبل الاستعلام من البيانات التاريخية.</span><span class="sxs-lookup"><span data-stu-id="647ae-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="647ae-114">سيتم تطبيق هذا الإعداد عند إنشاء تنبؤ أساسي.</span><span class="sxs-lookup"><span data-stu-id="647ae-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="647ae-115">في صفحة **استعلام إزالة الأخطاء‬**، يمكنك إضافة وإزالة وتحديد المعايير التي تحدد الحركات التي سيتم استبعادها عندما يتم حساب التنبؤ الأساسي.</span><span class="sxs-lookup"><span data-stu-id="647ae-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="647ae-116">على سبيل المثال، حدد صنف أو حركة أمر معين تريد استبعادها.</span><span class="sxs-lookup"><span data-stu-id="647ae-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="647ae-117">انقر فوق **عرض الحركات**.</span><span class="sxs-lookup"><span data-stu-id="647ae-117">Click **Display transactions**.</span></span> <span data-ttu-id="647ae-118">تسرد صفحة **حركات الأخطاء** الحركات التي تفي بالمعيار المحدد في الاستعلام والتي سيتم استبعاده من البيانات التاريخية عند حساب التنبؤ بالطلب.</span><span class="sxs-lookup"><span data-stu-id="647ae-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="647ae-119">**ملاحظة:** يمكنك أيضًا إنشاء استعلام يستند إلى استعلام موجود.</span><span class="sxs-lookup"><span data-stu-id="647ae-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="647ae-120">حدد الاستعلام المراد نسخه، ثم انقر فوق **نسخ**.</span><span class="sxs-lookup"><span data-stu-id="647ae-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="647ae-121">يحدد حقل **تاريخ الاستعلام** الإصدار.</span><span class="sxs-lookup"><span data-stu-id="647ae-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="647ae-122">يمكنك استخدام الاستعلام كما هو، أو يمكنك النقر فوق **تحرير استعلام** لتعديل المعايير.</span><span class="sxs-lookup"><span data-stu-id="647ae-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="647ae-123">ويمكنك بشكل اختياري تعديل اسم ووصف الاستعلام الجديد.</span><span class="sxs-lookup"><span data-stu-id="647ae-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="647ae-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="647ae-124">Additional resources</span></span>
--------

[<span data-ttu-id="647ae-125">نظرة عامة على التنبؤ بالطلب‬</span><span class="sxs-lookup"><span data-stu-id="647ae-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="647ae-126">رصد دقة التنبؤ​</span><span class="sxs-lookup"><span data-stu-id="647ae-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]