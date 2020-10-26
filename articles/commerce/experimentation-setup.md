---
title: إعداد تجربة
description: يصف هذا الموضوع كيفيه إعداد تجربه في خدمه جهة خارجيه.
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
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930132"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="3f6ae-103">إعداد تجربة</span><span class="sxs-lookup"><span data-stu-id="3f6ae-103">Set up an experiment</span></span>

<span data-ttu-id="3f6ae-104">بعد [تعريف الفرضية وتحديد معايير النجاح التي ترغب في استخدامها](experimentation-identify.md)، سيتعين عليك اعداد التجربة الخاصة بك في الخدمة التابعة لجهة خارجية.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="3f6ae-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3f6ae-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="3f6ae-107">[![رحلة مستخدم التجربة - الإعداد](./media/experimentation_setup.svg)](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="3f6ae-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="3f6ae-108">اعداد التجربة الخاصة بك في خدمه الجهة الخارجية</span><span class="sxs-lookup"><span data-stu-id="3f6ae-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="3f6ae-109">يمكنك الآن اختيار خدمه الجهات الخارجية الخاصة بك لتشغيل التجربة ومراقبتها، واعداد موصل التجربة.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="3f6ae-110">ويتم سرد هذه المتطلبات الاساسيه في [التجربة في Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="3f6ae-111">اتبع الخطوات المطلوبة لإنشاء تجربه في الخدمة التابعة لجهة خارجية.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="3f6ae-112">إذا تم تكوين الموصل بشكل صحيح، فان قائمه التجارب الكاملة التي يتم اعدادها في الخدمات التابعة لجهة خارجية ستكون في منشئ الموقع خلال حوالي 5 دقائق.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="3f6ae-113">قم باعداد معايير النجاح الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="3f6ae-113">Set up your success metrics</span></span>
<span data-ttu-id="3f6ae-114">ويحتاج كل تجربه إلى معايير لقياس تاثير التباينات وللتحقق من صحة الفرضية.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="3f6ae-115">اتبع الخطوات التالية لتمكين حساب المقاييس في خدمه الجهة الأخرى باستخدام احداث بيانات تتبع الاستخدام النشطة من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="3f6ae-116">في منشئ الموقع، حدد علامة التبويب **صفحات** في جزء التنقل الأيمن، ثم حدد الصفحة التي ترغب في تجميع المقاييس عليها.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="3f6ae-117">انتقل إلى القسم **معرفات الاحداث للتعقب** الموجود في جزء الخصائص الأيمن للصفحة أو الوحدة النمطية التي تريد تعقبها.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="3f6ae-118">حدد **عرض** .</span><span class="sxs-lookup"><span data-stu-id="3f6ae-118">Select **View** .</span></span> <span data-ttu-id="3f6ae-119">يتم عرض قائمه بكافة معرفات الاحداث.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="3f6ae-120">انسخ الحدث الذي تريد تعقبه، ثم ألصق مفتاح الحدث في الموقع المعين في خدمه الجهة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="3f6ae-121">إذا كنت تريد أكثر من حدث واحد، فقم بنسخ المفاتيح الواحدة كل مره.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="3f6ae-122">لمعرفه كيفيه عرض كافة الاحداث والسمات المتاحة، بما في ذلك طرق عرض الصفحة وتعقب الإيرادات، راجع [احداث مكونات التجارة لعمليات التشخيص واستكشاف الأخطاء وإصلاحها ](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="3f6ae-123">قم باجراء إيه خطوات أخرى لتعقب المقاييس وفقا لما هو مطلوب في الخدمات التابعة لجهة خارجية.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="3f6ae-124">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="3f6ae-124">Previous step</span></span>
[<span data-ttu-id="3f6ae-125">تحديد الفرضية وتحديد المقاييس الخاصة بتجربة</span><span class="sxs-lookup"><span data-stu-id="3f6ae-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="3f6ae-126">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="3f6ae-126">Next step</span></span>
[<span data-ttu-id="3f6ae-127">الاتصال بتجربة وتحريرها</span><span class="sxs-lookup"><span data-stu-id="3f6ae-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
