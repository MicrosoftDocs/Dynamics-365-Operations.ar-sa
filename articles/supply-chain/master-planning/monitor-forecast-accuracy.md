---
title: مراقبة دقة التنبؤ
description: توضح هذه المقالة أنواع دقة التنبؤ التي يحسبها Microsoft Dynamics 365 for Finance and Operations، وتشرح لك كيف يمكنك عرض قيم الدقة.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7070c15f9ee23cfdba871af68d1fc5954735651
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "356405"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="a1e0e-103">مراقبة دقة التنبؤ</span><span class="sxs-lookup"><span data-stu-id="a1e0e-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1e0e-104">توضح هذه المقالة أنواع دقة التنبؤ التي يحسبها Microsoft Dynamics 365 for Finance and Operations، وتشرح لك كيف يمكنك عرض قيم الدقة.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="a1e0e-105">يحسب Finance and Operations الأنواع التالية من دقة التنبؤ:</span><span class="sxs-lookup"><span data-stu-id="a1e0e-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="a1e0e-106">دقة التنبؤ التاريخي، عن طريق مقارنة التنبؤ التاريخي الذي يستخدمه "التخطيط الرئيسي" مع الطلب التاريخي.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="a1e0e-107">لعرض القيم (كل من القيم المطلقة والنسب المئوية) لدقة التنبؤ التاريخي، انقر فوق **إظهار الدقة** على الصفحة **تفاصيل التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="a1e0e-108">الدقة المقدرة لنموذج التنبؤ الذي يتم استخدامه لإنشاء التنبؤات.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="a1e0e-109">يمكنك عرض النسبة المئوية للدقة ضمن **تفاصيل النموذج -متوسط النسبة المئوية المطلقة للخطأ** على الصفحة **تفاصيل التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="a1e0e-110">**ملاحظة:** إذا كنت تستخدم خدمة التعلم الآلي من Microsoft Azure للتنبؤ بالطلب في Finance and Operations، يستند حساب دقة النموذج الداخلي إلى مجموعة بيانات الاختبار.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="a1e0e-111">لتحديد حجم مجموعة بيانات الاختبار، قم بضبط المعلمة **TEST\_SET\_SIZE\_PERCENT** في الصفحة **معلمات التنبؤ بالطلب**.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="a1e0e-112">على سبيل المثال، إذا قمت بتعيين القيمة إلى **20**، فإنه سيتم استخدام نسبة 20% الأخيرة من البيانات المسجلة لحساب دقة النموذج الداخلي.</span><span class="sxs-lookup"><span data-stu-id="a1e0e-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="a1e0e-113">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a1e0e-113">Additional resources</span></span>
--------

[<span data-ttu-id="a1e0e-114">تخويل ‏‫التنبؤ الذي تمت تسويته</span><span class="sxs-lookup"><span data-stu-id="a1e0e-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="a1e0e-115">إزالة القيم المتطرفة من بيانات الحركة التاريخية عند حساب التنبؤ بالطلب</span><span class="sxs-lookup"><span data-stu-id="a1e0e-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



