---
title: المهام الدورية لإدارة الائتمان
description: يصف هذا الموضوع المهام الدورية التي تعتبر جزءًا ضروريًا من عملية إدارة الحدود الائتمانية للعملاء.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ca9bb7f77283ec30d4648d6763f4156494050ac
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124152"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="07647-103">مهام إدارة الائتمان الدورية</span><span class="sxs-lookup"><span data-stu-id="07647-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07647-104">يصف هذا الموضوع المهام الدورية التي تعتبر جزءًا ضروريًا من عملية إدارة الحدود الائتمانية للعملاء.</span><span class="sxs-lookup"><span data-stu-id="07647-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="07647-105">تحديث نتائج المخاطر</span><span class="sxs-lookup"><span data-stu-id="07647-105">Update risk scores</span></span>

<span data-ttu-id="07647-106">مع التطور الذي تشهده الأعمال والتغييرات التي تطرأ على الظروف، قد تتغير أيضًا المخاطر الائتمانية لعميل معين.</span><span class="sxs-lookup"><span data-stu-id="07647-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="07647-107">للمساعدة في المحافظة على الحدود الائتمانية المناسبة لعملائك، يجب عليك إجراء مراجعات دورية للمعايير الموضوعة لكل نقاط المخاطرة وتحديث النقاط لكل عميل.</span><span class="sxs-lookup"><span data-stu-id="07647-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="07647-108">يمكنك تحديث النقاط التالية باستخدام صفحة **تحديث نقاط المخاطرة** (**عمليات التحصيل والائتمان‬ \> المهام الدورية \> إدارة الائتمان \> تحديث نقاط المخاطرة**).</span><span class="sxs-lookup"><span data-stu-id="07647-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="07647-109">كما تتم معالجة كافة الحسابات المعرفة من قبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="07647-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="07647-110">**متوسط أيام الدفع** – تمثل هذه النقاط متوسط عدد الأيام التي يدفع خلالها العميل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="07647-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="07647-111">**عميل منذ‬** – تمثل هذه النقاط هو السنوات التي كان خلالها العميل من عملاء مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="07647-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="07647-112">**في الأعمال منذ** – تمثل هذه النقاط عدد السنوات التي مرت على ممارسة الأعمال من قبل العميل.</span><span class="sxs-lookup"><span data-stu-id="07647-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="07647-113">إنها تستخدم قيمة الحقل **بدء العمل** في صفحة **العملاء‏‎**.</span><span class="sxs-lookup"><span data-stu-id="07647-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="07647-114">**أيام المبيعات المستحقة‬** – تستند هذه النقاط إلى رصيد الحسابات المدينة وإيرادات المبيعات وعدد الأيام لفترة 12 شهرًا الماضية.</span><span class="sxs-lookup"><span data-stu-id="07647-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="07647-115">**متوسط الرصيد** – تستند هذه النقاط إلى رصيد الحسابات المدينة لفترة 12 شهرًا الماضية.</span><span class="sxs-lookup"><span data-stu-id="07647-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="07647-116">**مجموعة إدارة الائتمان**، و**حالة الحساب**، و**البلد** – تستخدم هذه النقاط معلومات من العميل.</span><span class="sxs-lookup"><span data-stu-id="07647-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="07647-117">تحديث إحصاءات رصيد العميل</span><span class="sxs-lookup"><span data-stu-id="07647-117">Update customer balance statistics</span></span>

<span data-ttu-id="07647-118">يمكنك تشغيل عملية **تحديث إحصاءات رصيد العميل‬** لتحديث حساب إحصاءات الرصيد التي تظهر في صفحة‬ **استعلام حول إحصاءات الرصيد**.</span><span class="sxs-lookup"><span data-stu-id="07647-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="07647-119">يتم استخدام هذه المعلومات لحساب معدلات المخاطرة والقيم التي تظهر في مربعات حقائق إحصاءات الائتمان في صفحة **العميل**.</span><span class="sxs-lookup"><span data-stu-id="07647-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="07647-120">عند تشغيل العملية، يقوم بتحديث إحصاءات رصيد العميل لعميل واحد.</span><span class="sxs-lookup"><span data-stu-id="07647-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="07647-121">لإعداد مهمة دفعية لتشغيل العملية لعدة عملاء، يمكنك استخدام الصفحة **حساب إحصاءات الرصيد** (**إدارة الائتمان \> المهام الدورية \> حساب إحصاءات الرصيد**).</span><span class="sxs-lookup"><span data-stu-id="07647-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
