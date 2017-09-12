---
title: "‏‫الإبلاغ عن أوامر الإنتاج كمنتهية‬"
description: "يعتبر الإبلاغ عن الانتهاء مرحلة من مراحل الإنتاج. في هذه المرحلة، يتم الإبلاغ عن منتج منته ويتم نقله من أمر الإنتاج إلى المخزون."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8adcbcc2157058151c26179eb2eb925b0092d2d
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="1bbd2-104">‏‫الإبلاغ عن أوامر الإنتاج كمنتهية‬</span><span class="sxs-lookup"><span data-stu-id="1bbd2-104">Report production orders as finished</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1bbd2-105">يعتبر الإبلاغ عن الانتهاء مرحلة من مراحل الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-105">Report as finished is a production stage.</span></span> <span data-ttu-id="1bbd2-106">في هذه المرحلة، يتم الإبلاغ عن منتج منته ويتم نقله من أمر الإنتاج إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="1bbd2-107">عند الإبلاغ عن كمية السلع المنتهية كمنتهية في أمر الإنتاج، فإنه يتم تحديثه كمتوفر في المخزون.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="1bbd2-108">ويمكن الإبلاغ عن الكميات الجزئية لكمية الأمر المخطط لها في الأصل كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="1bbd2-109">ومن الممكن أيضًا الإبلاغ عن كميات الأخطاء مع سبب خطأ مقترن عند الإبلاغ عن الكميات كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="1bbd2-110">وعند وصول أمر الإنتاج إلى مرحلة الإبلاغ عنه كمنتهٍ، فإنه يشير إلى أنه لم تعد هناك أي كمية أخرى يتعين الإبلاغ عنها في أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="1bbd2-111">كما أن الخصائص التالية مقترنة بعملية **الإبلاغ عنه كمنتهٍ**:</span><span class="sxs-lookup"><span data-stu-id="1bbd2-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="1bbd2-112">من الممكن إعداد استهلاك الوقت والمواد الخام المتناسبة مع الكمية التي تم الإبلاغ عنها (المسح الخلفي)</span><span class="sxs-lookup"><span data-stu-id="1bbd2-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="1bbd2-113">يمكن إنشاء عمل الإبعاد للأصناف التي تم تمكينها لعمليات المستودع.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="1bbd2-114">يمكن إعداد قيمة التكلفة المخططة أو القياسية للسلع المنتهية للإبلاغ عنها لحسابات دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="1bbd2-115">يمكن إنشاء أمر جودة للكمية التي تم الإبلاغ عنها استناداً إلى إعداد اقتران الجودة.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="1bbd2-116">تم الإبلاغ عن الكمية لموقع الإخراج.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="1bbd2-117">ويتم فيما بعد إنشاء عمل المستودع لنقل الكمية من موقع الإخراج إلى وجهته النهائية بواسطة توجيه الموقع لعمل الإبعاد.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="1bbd2-118">يمكن إنشاء أمر جودة عند الإبلاغ عن أمر إنتاج كمنتهٍ، إذا تم إعداد اقتران جودة.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="1bbd2-119">تعيين أمر إنتاج للإبلاغ عنه كمنتهٍ</span><span class="sxs-lookup"><span data-stu-id="1bbd2-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="1bbd2-120">يمكن تعيين أمر إنتاج إلى **الإبلاغ عنه كمنتهٍ** من خلال وظيفة تحديث أمر الإنتاج القياسي، أو من خلال دفاتر يومية بطاقة الوظيفة والمسار، أو من خلال دفتر يومية **الإبلاغ عنه كمنتهٍ**.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="1bbd2-121">كما يمكنك تحديث المرحلة إلى **الإبلاغ عنه كمنتهٍ** من خلال محطة بطاقة الوظيفة وصفحات جهاز بطاقة الوظيفة، عند الإبلاغ عن الوظيفة الأخيرة لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="1bbd2-122">وأخيراً، يمكنك تمكين خيار **الإبلاغ عنه كمنتهٍ** كعملية لحل جهاز المستودع المحمول يدويًا.</span><span class="sxs-lookup"><span data-stu-id="1bbd2-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




