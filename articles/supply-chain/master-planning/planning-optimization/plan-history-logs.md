---
title: عرض سجل محفوظات الخطط والتخطيط
description: يوضح هذا الموضوع كيفيه عرض تاريخ مهام التخطيط التي يتم تشغيلها بواسطة وظيفة تحسين التخطيط.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187237"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="053ef-103">عرض سجل محفوظات الخطط والتخطيط</span><span class="sxs-lookup"><span data-stu-id="053ef-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="053ef-104">يوضح هذا الموضوع كيفيه عرض تاريخ مهام التخطيط التي يتم تشغيلها بواسطة وظيفة تحسين التخطيط في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="053ef-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="053ef-105">لعرض محفوظات أحدي الخطط ، افتح الخطة من خلال الانتقال **التخطيط الرئيسي** \> **إعداد**\> **خطط** \> **الخطط الرئيسية** وتحديد **المحفوظات**.</span><span class="sxs-lookup"><span data-stu-id="053ef-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="053ef-106">تسرد المحفوظات كافة الوظائف الخاصة بالخطة المحددة.</span><span class="sxs-lookup"><span data-stu-id="053ef-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="053ef-107">تشتمل القائمة على المهام المكتملة والنشطة.</span><span class="sxs-lookup"><span data-stu-id="053ef-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="053ef-108">تحتفظ محفوظات الوظائف الخاصة بالتخطيط الرئيسي للتخطيط الرئيسي بعدد يصل إلى 60 سجلاً لكل خطة رئيسية.</span><span class="sxs-lookup"><span data-stu-id="053ef-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="053ef-109">عند تشغيل حساب تخطيط رئيسي جديد، يتم حذف السجل الخاص بالمحفوظات الأسبق لهذه الخطة.</span><span class="sxs-lookup"><span data-stu-id="053ef-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="053ef-110">بالإضافة إلى رؤية وقت بدء الوظائف وحالتها ، يمكنك عرض السجل لوظيفة معينه.</span><span class="sxs-lookup"><span data-stu-id="053ef-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="053ef-111">يتضمن السجل معلومات اضافيه وتحذيرات.</span><span class="sxs-lookup"><span data-stu-id="053ef-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="053ef-112">لا تحتوي كافة المهام على سجل.</span><span class="sxs-lookup"><span data-stu-id="053ef-112">Not all jobs have a log.</span></span> <span data-ttu-id="053ef-113">لعرض السجل الخاص بأحدي الوظائف، حدد **سجل**.</span><span class="sxs-lookup"><span data-stu-id="053ef-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="053ef-114">يتم تخزين إدخالات السجل فقط لمدة 30 يومًا بعد تاريخ انتهاء الوظيفة، وذلك بعد حذفها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="053ef-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="053ef-115">الموارد ذات الصلة</span><span class="sxs-lookup"><span data-stu-id="053ef-115">Related resources</span></span>

- [<span data-ttu-id="053ef-116">نظرة عامة على تحسين التخطيط‬</span><span class="sxs-lookup"><span data-stu-id="053ef-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="053ef-117">بدء تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="053ef-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="053ef-118">تحليل ملاءمة تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="053ef-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="053ef-119">تطبيق عوامل تصفية على خطة</span><span class="sxs-lookup"><span data-stu-id="053ef-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="053ef-120">إلغاء وظيفة تخطيط</span><span class="sxs-lookup"><span data-stu-id="053ef-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]