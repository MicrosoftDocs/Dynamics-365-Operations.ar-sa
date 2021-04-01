---
title: تحديد الفرضية وتحديد المقاييس الخاصة بتجربة
description: يوضح هذا الموضوع كيفيه تحديد مقاييس الفرضية والنجاح لتجربه تقوم بتشغيلها علي موقع ويب خاص بالتجارة الكترونيه في Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 91614cda804cae4574fce4c9cfb31c63d876f19b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238620"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="2da3d-103">تحديد الفرضية وتحديد المقاييس الخاصة بتجربة</span><span class="sxs-lookup"><span data-stu-id="2da3d-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="2da3d-104">تتضمن المرحلة الاولي في دوره حياه التجربة تعريف الفرضية للتجربة وتحديد القياسات التي ستتعقبها لتقييم النجاح.</span><span class="sxs-lookup"><span data-stu-id="2da3d-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="2da3d-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في [اعداد وتشغيل تجربه](experimentation-overview.md)  علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2da3d-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="2da3d-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="2da3d-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="2da3d-107">[![رحلة مستخدم التجربة - التحديد](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="2da3d-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="2da3d-108">الفرضية هو البيان الذي يمكنك التنبؤ بنتيجة التجربة فيه.</span><span class="sxs-lookup"><span data-stu-id="2da3d-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="2da3d-109">تنتقل العديد من العوامل إلى تعريف الفرضية، علي سبيل المثال، البحث عن سلوك المستخدم وبيانات موقع الويب التي قمت بتجميعها.</span><span class="sxs-lookup"><span data-stu-id="2da3d-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="2da3d-110">باستخدام الفرضية، ستقوم بتعريف الافتراضات أو النظرية التي ترغب في التحقق من صحتها بتجربتك.</span><span class="sxs-lookup"><span data-stu-id="2da3d-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="2da3d-111">قد يكون الهدف من المفترض هو ان تكون "*صوره لقميص أبيض علي الصفحة الرئيسية تؤدي إلى تحريك معدل تتبع الاستخدام أكثر من السترات الزرقاء اثناء شهور الصيف نظرا لان الأشخاص يرغبون في وجود شيء خفيف ولون خفيف في الصيف.*"</span><span class="sxs-lookup"><span data-stu-id="2da3d-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="2da3d-112">في هذه الحالة، ستقوم بإنشاء التنوعات التي تتضمن القميص الأبيض والسترة الزرقاء، ونشر كل منهما في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="2da3d-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="2da3d-113">للتحقق من صحة الفرضية، يجب أن يتم ربط نجاح أو فشل التجربة مباشرة بإجراءات المستخدم؛ على سبيل المثال، إذا قام مستخدم موقع ويب بالنقر فوق ارتباط أو زر.</span><span class="sxs-lookup"><span data-stu-id="2da3d-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="2da3d-114">يجب ان تتوافق هذه الإجراءات مع الاحداث التي سيتم الاعلام عنها لتعقب خدمه الجهة الأخرى الخاصة بالتجربة.</span><span class="sxs-lookup"><span data-stu-id="2da3d-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="2da3d-115">بمرور الوقت، سيتم تدوين النسبة المئوية للمستخدمين الذين ياخذون الاجراء كقياس يمكنك استخدامه لإنشاء تقارير واجراء تحليلات.</span><span class="sxs-lookup"><span data-stu-id="2da3d-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="2da3d-116">لمراجعة جميع الأحداث والسمات المتوفرة، راجع [حداث مكونات Commerce للتشخيصات واستكشاف الأخطاء وإصلاحها‬](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="2da3d-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="2da3d-117">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="2da3d-117">Previous step</span></span>
[<span data-ttu-id="2da3d-118">الاختبار في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2da3d-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="2da3d-119">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="2da3d-119">Next step</span></span>
[<span data-ttu-id="2da3d-120">إعداد تجربة</span><span class="sxs-lookup"><span data-stu-id="2da3d-120">Set up an experiment</span></span>](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]