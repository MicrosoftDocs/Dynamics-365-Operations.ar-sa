---
title: تحديد الفرضية وتحديد المقاييس الخاصة بتجربة
description: يوضح هذا الموضوع كيفيه تحديد مقاييس الفرضية والنجاح لتجربه تقوم بتشغيلها علي موقع ويب خاص بالتجارة الكترونيه في Dynamics 365 Commerce.
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
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930130"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="e1958-103">تحديد الفرضية وتحديد المقاييس الخاصة بتجربة</span><span class="sxs-lookup"><span data-stu-id="e1958-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="e1958-104">تتضمن المرحلة الاولي في دوره حياه التجربة تعريف الفرضية للتجربة وتحديد القياسات التي ستتعقبها لتقييم النجاح.</span><span class="sxs-lookup"><span data-stu-id="e1958-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="e1958-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في [اعداد وتشغيل تجربه](experimentation-overview.md)  علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e1958-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e1958-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="e1958-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="e1958-107">[![رحلة مستخدم التجربة - التحديد](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="e1958-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="e1958-108">الفرضية هو البيان الذي يمكنك التنبؤ بنتيجة التجربة فيه.</span><span class="sxs-lookup"><span data-stu-id="e1958-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="e1958-109">تنتقل العديد من العوامل إلى تعريف الفرضية، علي سبيل المثال، البحث عن سلوك المستخدم وبيانات موقع الويب التي قمت بتجميعها.</span><span class="sxs-lookup"><span data-stu-id="e1958-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="e1958-110">باستخدام الفرضية، ستقوم بتعريف الافتراضات أو النظرية التي ترغب في التحقق من صحتها بتجربتك.</span><span class="sxs-lookup"><span data-stu-id="e1958-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="e1958-111">قد يكون الهدف من المفترض هو ان تكون " *صوره لقميص أبيض علي الصفحة الرئيسية تؤدي إلى تحريك معدل تتبع الاستخدام أكثر من السترات الزرقاء اثناء شهور الصيف نظرا لان الأشخاص يرغبون في وجود شيء خفيف ولون خفيف في الصيف.* "</span><span class="sxs-lookup"><span data-stu-id="e1958-111">An example of a hypothesis for your experiment may be " *a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.* "</span></span> <span data-ttu-id="e1958-112">في هذه الحالة، ستقوم بإنشاء التنوعات التي تتضمن القميص الأبيض والسترة الزرقاء، ونشر كل منهما في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="e1958-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="e1958-113">للتحقق من صحة الفرضية، يجب ان يتم ربط نجاح أو فشل التجربة مباشره بإجراءات المستخدم؛ علي سبيل المثال، إذا قام مستخدم موقع ويب بالنقر فوق ارتباط أو زر.</span><span class="sxs-lookup"><span data-stu-id="e1958-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="e1958-114">يجب ان تتوافق هذه الإجراءات مع الاحداث التي سيتم الاعلام عنها لتعقب خدمه الجهة الأخرى الخاصة بالتجربة.</span><span class="sxs-lookup"><span data-stu-id="e1958-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="e1958-115">بمرور الوقت، سيتم تدوين النسبة المئوية للمستخدمين الذين ياخذون الاجراء كقياس يمكنك استخدامه لإنشاء تقارير واجراء تحليلات.</span><span class="sxs-lookup"><span data-stu-id="e1958-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="e1958-116">قم بالرجوع إلى [احداث مكون التجارة الخاصة بالتشخيص](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)وموضوع استكشاف الأخطاء وإصلاحها لمراجعه كافة الاحداث والسمات المتاحة.</span><span class="sxs-lookup"><span data-stu-id="e1958-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="e1958-117">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="e1958-117">Previous step</span></span>
[<span data-ttu-id="e1958-118">الاختبار في Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e1958-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="e1958-119">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="e1958-119">Next step</span></span>
[<span data-ttu-id="e1958-120">إعداد تجربة</span><span class="sxs-lookup"><span data-stu-id="e1958-120">Set up an experiment</span></span>](experimentation-setup.md)
