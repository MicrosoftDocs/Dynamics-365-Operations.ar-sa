---
title: إعداد أكواد تقارير ضريبة المبيعات
description: تشير أكواد ضريبة المبيعات إلى رقم حقل المدرج في تقرير ضريبة المبيعات.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 362d30e56fe35b85d50bfa2df57364733b366fef
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646171"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="f2cb6-103">إعداد أكواد تقارير ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="f2cb6-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2cb6-104">تشير أكواد ضريبة المبيعات إلى رقم حقل المدرج في تقرير ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="f2cb6-105">يتم استخدامها في تخطيطات التقارير الخاصة بالدولة.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="f2cb6-106">كذلك، فإنها تستخدم في دفع ضريبة المبيعات حسب تقرير الكود.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="f2cb6-107">يوضح ذلك التقرير مبالغ ضريبة المبيعات لفترة التسوية الملخصة لكل كود تقرير.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="f2cb6-108">بعد إنشاء أكواد تقارير ضريبة المبيعات، يمكنك الإشارة إلى تلك الأكواد من علامة التبويب السريعة، التي يمكن أن تصل إليها من الصفحة **كود ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="f2cb6-109">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="f2cb6-110">في **جزء التنقل**، انتقل إلى **الضريبة > الإعداد > ضريبة المبيعات > أكواد تقارير ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="f2cb6-111">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-111">Click **New**.</span></span>
3. <span data-ttu-id="f2cb6-112">حدد تخطيط التقرير الذي ينتمي إليه كود التقرير.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="f2cb6-113">يتم استخدام هذا التخطيط لتصفية أكواد التقارير المتوفرة لكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="f2cb6-114">ينتمي كل كود ضريبة مبيعات إلى فترة تسوية، تنتمي بدورها إلى هيئة ضريبة مبيعات، تستخدم تخطيط تقرير.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="f2cb6-115">في الحقل **كود التقرير**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="f2cb6-116">في حقل **نص التقرير**، أدخل وصفًا لعرضه على التقارير.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="f2cb6-117">في الحقل **وصف مختصر**، أدخل وصفًا لأغراض داخلية.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="f2cb6-118">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="f2cb6-118">Click **Save**.</span></span>

