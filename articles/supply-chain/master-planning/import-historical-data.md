---
title: استيراد البيانات التاريخية‬ للتنبؤات بالطلب
description: للحصول على تنبؤات بالطلب‬ دقيقة، تحتاج إلى بيانات تاريخية لكل صنف أو مفتاح توزيع الصنف. يشرح هذا الموضوع كيفية استخدام كيانات البيانات لاستيراد بيانات الطلب التاريخية من أي نظام، بحيث تحصل على سجل طويل لبيانات التنبؤات بالطلب.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301640"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="693a8-104">استيراد البيانات التاريخية‬ للتنبؤات بالطلب</span><span class="sxs-lookup"><span data-stu-id="693a8-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="693a8-105">للمساعدة في ضمان دقة التنبؤات بالطلب، يجب أن تكون بيانات الطلب التاريخية لديك بمقدار مماثل لما يمكنك الحصول عليه لكل صنف أو مفتاح توزيع الصنف.</span><span class="sxs-lookup"><span data-stu-id="693a8-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="693a8-106">إذا لم يكن قد تم بعد استيراد بيانات الطلب التاريخية، فاستخدم كيان البيانات **الطلب الخارجي التاريخي‬** (ReqDemPlanHistoricalExternalDemandEntity) في Dynamics 365 Supply Chain Management لاستيرادها.</span><span class="sxs-lookup"><span data-stu-id="693a8-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="693a8-107">في مساحة العمل **إدارة البيانات**، يمكنك الاطلاع على نظرة عامة على كافة الحقول الموجودة في الكيان.</span><span class="sxs-lookup"><span data-stu-id="693a8-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="693a8-108">افتح مساحة العمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="693a8-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="693a8-109">حدد لوحة **كيانات البيانات**.</span><span class="sxs-lookup"><span data-stu-id="693a8-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="693a8-110">ابحث في قائمة الكيانات عن **الطلب الخارجي التاريخي**.</span><span class="sxs-lookup"><span data-stu-id="693a8-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="693a8-111">حدد **الحقول المستهدفة**.</span><span class="sxs-lookup"><span data-stu-id="693a8-111">Select **Target fields**.</span></span> <span data-ttu-id="693a8-112">تُعتبر حقول الكيانات التالية إلزامية: الموقع (**DeliveringSiteId**)، والتاريخ (**DemandDate**) والكمية، (**DemandQuantity**)، وإما رقم الصنف (**ItemNumber**) أو مفتاح توزيع الصنف (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="693a8-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="693a8-113">لاستخدام كيان البيانات، يجب أن يكون لديك ملف Microsoft Excel أو ملف قيم تفصلها الفواصل (CSV) يحتوي على بيانات الطلب التاريخية.</span><span class="sxs-lookup"><span data-stu-id="693a8-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="693a8-114">يوضح المثال التالي كيفية استيراد البيانات من ملف CSV.</span><span class="sxs-lookup"><span data-stu-id="693a8-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="693a8-115">لمزيد من المعلومات حول كيفيه استيراد البيانات، بما في ذلك كيفيه تنظيف البيانات بعد الاستيراد، راجع [نظره عامه حول استيراد البيانات](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)وتصديرها وموضوعاتها ذات صله.</span><span class="sxs-lookup"><span data-stu-id="693a8-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="693a8-116">انظر أيضًا [إنشاء تنبؤ أساسي إحصائي](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="693a8-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]