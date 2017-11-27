---
title: "‏‫تخويل ‏‫التنبؤ الذي تمت تسويته"
description: "يجب عدم تخويل كافة بيانات التنبؤ على الفور. يشرح هذا المقال كيف يمكنك تحديد الفترة التي يتم فيها التخويل لتنبؤ. وهو يوضح أيضًا كيفية تخويل التنبؤ لشركات بعينها ونماذج التنبؤ."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5ce38e94ae4c7b28b4e182018add7c046f685e46
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="ac73d-105">‏‫تخويل ‏‫التنبؤ الذي تمت تسويته</span><span class="sxs-lookup"><span data-stu-id="ac73d-105">Authorize an adjusted forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ac73d-106">يجب عدم تخويل كافة بيانات التنبؤ على الفور.</span><span class="sxs-lookup"><span data-stu-id="ac73d-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="ac73d-107">يشرح هذا المقال كيف يمكنك تحديد الفترة التي يتم فيها التخويل لتنبؤ.</span><span class="sxs-lookup"><span data-stu-id="ac73d-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="ac73d-108">وهو يوضح أيضًا كيفية تخويل التنبؤ لشركات بعينها ونماذج التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="ac73d-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="ac73d-109">يجب عدم تخويل كافة بيانات التنبؤ على الفور.</span><span class="sxs-lookup"><span data-stu-id="ac73d-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="ac73d-110">يمكنك تحديد تواريخ البدء والانتهاء للفترة التي يتم تخويل التنبؤ لها.</span><span class="sxs-lookup"><span data-stu-id="ac73d-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="ac73d-111">تتيح لك هذه الوظيفة تجميد مستودعات معينة.</span><span class="sxs-lookup"><span data-stu-id="ac73d-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="ac73d-112">‏‫يجب أن تتوافق تواريخ البدء والانتهاء التي قمت بتحديدها مع تواريخ البدء والانتهاء من المستودع الذي تم إنشاء التنبؤ به.</span><span class="sxs-lookup"><span data-stu-id="ac73d-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="ac73d-113">يفرض النظام هذا التقييد ويعدل التواريخ تلقائيًا، في حالة طلب التعديل.‬</span><span class="sxs-lookup"><span data-stu-id="ac73d-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="ac73d-114">في علامة التبويب **تفاصيل** في الصفحة **التخويل**، يمكنك عرض تفاصيل حول التنبؤ الذي تم إنشاؤه مؤخرًا.</span><span class="sxs-lookup"><span data-stu-id="ac73d-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="ac73d-115">يمكنك تحديد الشركات ونماذج التنبؤ لتخويل التنبؤ للاستخدام.</span><span class="sxs-lookup"><span data-stu-id="ac73d-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="ac73d-116">بشكل افتراضي، تتضمن الشبكة كافة الشركات التي تم إنشاء طلب للتنبؤ لها.</span><span class="sxs-lookup"><span data-stu-id="ac73d-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="ac73d-117">لكل شركة، تتم تعبئة نموذج التنبؤ الذي يتوافق مع خطة التنبؤ الحالية التي يتم إعدادها في معلمات التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="ac73d-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="ac73d-118">ومع ذلك، يمكنك تغيير نموذج التنبؤ هذا إلى أي نموذج تنبؤ ينتمي إلى هذه الشركة.</span><span class="sxs-lookup"><span data-stu-id="ac73d-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="ac73d-119">إذا لم يتم إنشاء أي بيانات طلب للتنبؤ لشركة محددة، فإنك ستستلم رسالة تحذير في وقت الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="ac73d-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="ac73d-120">من المهم جدًا أن تفهم كيف تعمل خانة اختيار **‏‫حفظ التسويات اليدوية التي تم إدخالها على التنبؤ بالطلب الأساسي ‬**.</span><span class="sxs-lookup"><span data-stu-id="ac73d-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="ac73d-121">إذا قمت بإجراء التسويات اليدوية للتنبؤ الأساسي الإحصائي، فإنه يتم تخويل القيم المعدلة للاستخدام، حتى إذا تم مسح خانة الاختيار هذه.</span><span class="sxs-lookup"><span data-stu-id="ac73d-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="ac73d-122">ومع ذلك، يتم تجاهل التغييرات بعد التخويل.</span><span class="sxs-lookup"><span data-stu-id="ac73d-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="ac73d-123">وبالتالي، في المرة التالية التي يتم فيها إنشاء تنبؤ، يكون هذا التنبؤ إحصائيًا فقط ولا يحتوي على أي تجاوزات يدوية، حتى إذا تم تحديد **‏‫نقل التسويات اليدوية إلى التنبؤ بالطلب‬**.</span><span class="sxs-lookup"><span data-stu-id="ac73d-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="ac73d-124">وبالتالي، يمكنك اعتبار خانة الاختيار **‏‫حفظ التسويات اليدوية التي تم إدخالها على التنبؤ بالطلب الأساسي ‬** آلية تسمح لك الاحتفاظ كافة التغييرات اليدوية أو تجاهلها.</span><span class="sxs-lookup"><span data-stu-id="ac73d-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="see-also"></a><span data-ttu-id="ac73d-125">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="ac73d-125">See also</span></span>
--------

[<span data-ttu-id="ac73d-126">القيام بتسويات يدوية في تنبؤ الخط الأساسي</span><span class="sxs-lookup"><span data-stu-id="ac73d-126">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="ac73d-127">مراقبة دقة التنبؤ</span><span class="sxs-lookup"><span data-stu-id="ac73d-127">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




