---
title: إعداد أكواد تقارير ضريبة المبيعات
description: تشير أكواد ضريبة المبيعات إلى رقم حقل في تقرير ضريبة المبيعات.
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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916081"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="9fc34-103">إعداد أكواد تقارير ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="9fc34-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fc34-104">تشير أكواد ضريبة المبيعات إلى رقم حقل في تقرير ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="9fc34-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="9fc34-105">ويتم استخدامها على تخطيطات تقارير خاصة ببلد معين وعلى تقرير دفع ضريبة المبيعات حسب الكود‬ لطباعة مبالغ ضرائب المبيعات لفترة تسوية يتم تلخيصها لكل كود التقارير.</span><span class="sxs-lookup"><span data-stu-id="9fc34-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="9fc34-106">بعد إنشاء أكواد تقارير ضريبة المبيعات، يمكنك الإشارة إليها من علامة التبويب السريعة "إعداد التقرير‬" في صفحة "كود ضريبة المبيعات".</span><span class="sxs-lookup"><span data-stu-id="9fc34-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="9fc34-107">يستخدم هذا التسجيل شركة بيانات العرض التوضيحي DEMF.</span><span class="sxs-lookup"><span data-stu-id="9fc34-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="9fc34-108">في **جزء التنقل**، انتقل إلى **الضريبة > الإعداد > ضريبة المبيعات > أكواد تقارير ضريبة المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="9fc34-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="9fc34-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9fc34-109">Click **New**.</span></span>
3. <span data-ttu-id="9fc34-110">حدد تخطيط التقرير الذي ينتمي إليه كود التقرير.</span><span class="sxs-lookup"><span data-stu-id="9fc34-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="9fc34-111">يتم استخدام هذا التخطيط لتصفية أكواد التقارير المتوفرة لكود ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="9fc34-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="9fc34-112">ينتمي كل كود ضريبة مبيعات إلى فترة تسوية تنتمي بدورها إلى هيئة ضريبة مبيعات تستخدم تخطيط تقرير.</span><span class="sxs-lookup"><span data-stu-id="9fc34-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="9fc34-113">في الحقل**كود التقرير**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="9fc34-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="9fc34-114">في حقل **نص التقرير**، أدخل وصفًا لعرضه على التقارير.</span><span class="sxs-lookup"><span data-stu-id="9fc34-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="9fc34-115">في الحقل **وصف مختصر**، أدخل وصفًا لأغراض داخلية.</span><span class="sxs-lookup"><span data-stu-id="9fc34-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="9fc34-116">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9fc34-116">Click **Save**.</span></span>

