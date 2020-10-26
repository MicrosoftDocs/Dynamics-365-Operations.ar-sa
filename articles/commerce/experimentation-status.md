---
title: مراجعة حالة التجربة
description: يشرح هذا الموضوع الحالة التي تحتوي عليها التجربة في دوره حياه التجربة في Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930129"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="8ceac-103">مراجعة حالة التجربة</span><span class="sxs-lookup"><span data-stu-id="8ceac-103">Review the status of an experiment</span></span>
<span data-ttu-id="8ceac-104">هناك العديد من الخطوات المتضمنة في اعداد وتشغيل تجربه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ceac-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8ceac-105">للحصول علي معلومات حول دوره حياه التجربة، راجع [التجربة في Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8ceac-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="8ceac-106">لمعرفه المكان الذي توجد فيه التجارب في دوره الحياة، انتقل إلى علامة التبويب **التجارب** في منشئ الموقع.</span><span class="sxs-lookup"><span data-stu-id="8ceac-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="8ceac-107">يتم عرض قائمه بالتجارب مع حاله كل تجربه في كل من التجارة وخدمه الجهة الخارجية المستخدمة لتمكين إنشاء التجارب، وتعيين التباينات، وتحليل البيانات.</span><span class="sxs-lookup"><span data-stu-id="8ceac-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="8ceac-108">في العمود **حاله التجارة** ، قد يتم عرض القيم التالية.</span><span class="sxs-lookup"><span data-stu-id="8ceac-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="8ceac-109">**مسودة** - التجربة متصلة بصفحه أو جزء منها في التجارة ويتم تحريرها.</span><span class="sxs-lookup"><span data-stu-id="8ceac-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="8ceac-110">**تم النشر** - تباينات التجربة جاهزه للعرض علي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8ceac-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="8ceac-111">في حاله تشغيل الاختبار في خدمه الجهة الخارجية، سيشاهد مستخدمو موقع الويب تباين الصفحة أو الجزء كما هو محدد من قبل خدمه الجهة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8ceac-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="8ceac-112">**غير منشور** - لم يعد الاختبار متاحا علي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="8ceac-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="8ceac-113">سيشاهد مستخدمو موقع الويب تباين الصفحة أو الجزء، حتى في حاله تشغيل التجربة في خدمه الجهة الخارجية.</span><span class="sxs-lookup"><span data-stu-id="8ceac-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="8ceac-114">**مكتمل** - قامت التجربة بتشغيل الدورة التدريبية وترقيه تباين لكافة مستخدمي مواقع الويب.</span><span class="sxs-lookup"><span data-stu-id="8ceac-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="8ceac-115">بالمثل، في عمود **حالة الجهة الخارجية** ، قد يتم عرض القيم التالية لتوضيح الحالة التي تكون فيها التجارب في الخدمة التابعة لجهة خارجية.</span><span class="sxs-lookup"><span data-stu-id="8ceac-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="8ceac-116">**مسودة** - تم اعداد التجربة في خدمه الجهة الخارجية ولكن لم يتم بدء تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="8ceac-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="8ceac-117">**قيد التشغيل** - تم بدء التجربة في الخدمة التابعة لجهة خارجية وتقوم بتجميع البيانات.</span><span class="sxs-lookup"><span data-stu-id="8ceac-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="8ceac-118">**متوقف مؤقتا** - يتم إيقاف التجربة مؤقتا ولا تقوم بتجميع البيانات.</span><span class="sxs-lookup"><span data-stu-id="8ceac-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="8ceac-119">يجب عليك استئناف التجربة لتجميع البيانات مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="8ceac-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="8ceac-120">**مؤرشف** - قامت التجربة بتشغيل الدورة التدريبية لها وتمت أرشفتها في الخدمة التابعة لجهة أخرى كمرجع مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="8ceac-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="8ceac-121">يعرض الرسم التخطيطي أدناه كلا من مجموعات الحالات وكيفيه ارتباطها ببعضها البعض.</span><span class="sxs-lookup"><span data-stu-id="8ceac-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="8ceac-122">[![حالات التجربة](./media/experimentation_statuses.svg)](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8ceac-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
