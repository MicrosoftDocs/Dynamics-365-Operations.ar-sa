---
title: تنبؤات دفع العميل (معاينة)
description: يصف هذا الموضوع قدرة توقع الدفع والتي يمكن أن تساعد في فهم ممارسات الدفع النموذجية للعملاء الفرديين بشكل أفضل. كذلك، يمكن أن تساعد هذه الميزة في تحديد الحالات التي تجعلك تبدء عمليات الجمع قبل البدء من القيام بذلك.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 84a2342d76dc309fa1fd3de7b2c3de60e62e4d72
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186386"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="e8334-104">تنبؤات دفع العميل (معاينة)</span><span class="sxs-lookup"><span data-stu-id="e8334-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e8334-105">يصف هذا الموضوع قدرة توقع الدفع والتي يمكن أن تساعد في فهم ممارسات الدفع النموذجية للعملاء الفرديين بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="e8334-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="e8334-106">كذلك، يمكن أن تساعد هذه الميزة في تحديد الحالات التي تجعلك تبدء عمليات الجمع قبل البدء من القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="e8334-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="e8334-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="e8334-107">Overview</span></span>

<span data-ttu-id="e8334-108">تجد المؤسسات في أغلب الأحيان أنه من الصعب توقع الوقت الذي سيقوم فيه العميل بتسديد الفواتير.</span><span class="sxs-lookup"><span data-stu-id="e8334-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="e8334-109">وقد يتسبب هذا النقص في النظرة الأعمق في حدوث المشكلات التالية:</span><span class="sxs-lookup"><span data-stu-id="e8334-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="e8334-110">تقديرات تدفقات نقدية أقل دقة</span><span class="sxs-lookup"><span data-stu-id="e8334-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="e8334-111">عمليات الدفع التي تبدأ متأخرة جدًا</span><span class="sxs-lookup"><span data-stu-id="e8334-111">Collections processes that start too late</span></span>
- <span data-ttu-id="e8334-112">الأوامر التي تم إصدارها إلى العملاء الذين قد يقومون بعمليات الدفع بشكل افتراضي</span><span class="sxs-lookup"><span data-stu-id="e8334-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="e8334-113">تساعد توقعات دفع العميل (المعاينة) المؤسسات في توقع الوقت الذي سيقوم فيه العميل بتسديد فاتورة.</span><span class="sxs-lookup"><span data-stu-id="e8334-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="e8334-114">وبالتالي، يمكنهم إنشاء استراتيجيات التحصيلات التي تساعد في زيادة احتمالات دفع الموعد في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8334-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="e8334-115">التوقعات</span><span class="sxs-lookup"><span data-stu-id="e8334-115">Predictions</span></span>

<span data-ttu-id="e8334-116">تسمح عمليات توقع الدفع للمؤسسات بتحسين عمليات الأعمال الخاصة بها من خلال مساعدتهم في تحديد الفواتير التي من المحتمل دفعها متأخرة.</span><span class="sxs-lookup"><span data-stu-id="e8334-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="e8334-117">يمكن للمؤسسة استخدام هذه المعلومات للقيام بالإجراءات التي تحسن فرص السداد في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8334-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="e8334-118">تستخدم ميزة توقعات دفع العميل نموذج التعلم الآلي للتوقع بشكل أكثر دقة عند قيام العميل بدفع فاتورة معلقة.</span><span class="sxs-lookup"><span data-stu-id="e8334-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="e8334-119">يشتمل نموذج التعلم الآلي هذا الفواتير تاريخية والدفع وبيانات العميل.</span><span class="sxs-lookup"><span data-stu-id="e8334-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="e8334-120">بالنسبة لكل فاتورة مفتوحة، تقوم الميزة بتعيين ثلاثة احتمالات للدفع:</span><span class="sxs-lookup"><span data-stu-id="e8334-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="e8334-121">احتمالية إجراء الدفع في الوقت الحالي</span><span class="sxs-lookup"><span data-stu-id="e8334-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="e8334-122">احتمالية إجراء الدفع متأخر</span><span class="sxs-lookup"><span data-stu-id="e8334-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="e8334-123">احتمالية إجراء الدفع متأخر جدًا</span><span class="sxs-lookup"><span data-stu-id="e8334-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="e8334-124">كما توفر الميزة طريقة عرض كاملة للمدفوعات المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="e8334-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="e8334-125">[![العرض المجمع لتنبؤات الدفع](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="e8334-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="e8334-126">يتم تعيين احتمالية الدفع في الوقت المحدد في كل فاتورة.</span><span class="sxs-lookup"><span data-stu-id="e8334-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="e8334-127">يتم وضع علامة دائرة حمراء على الفواتير التي تحتوي على احتمال الدفع في الوقت المحدد أقل من 50 ٪ للإشارة إلى أن هذه الفواتير قد تتطلب اهتمامًا من جانب وكيل التحصيلات.</span><span class="sxs-lookup"><span data-stu-id="e8334-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="e8334-128">[![قائمة احتمالات الدفع](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="e8334-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="e8334-129">كما توفر ميزة تنبؤات الدفع للعميل معلومات سياقية لتوضيح التوقع.</span><span class="sxs-lookup"><span data-stu-id="e8334-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="e8334-130">تتضمن هذه المعلومات أفضل العوامل التي تؤثر على التوقع، وحالة العمل الحالية مع العميل والتفاصيل حول سلوك الدفع القديم للعميل.</span><span class="sxs-lookup"><span data-stu-id="e8334-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="e8334-131">في العديد من الشركات، كان لعملية التحصيلات نشاطًا تفاعليًا.</span><span class="sxs-lookup"><span data-stu-id="e8334-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="e8334-132">بمعني آخر، لا تبدأ عملية التحصيلات حتى تصبح الفواتير مستحقة.</span><span class="sxs-lookup"><span data-stu-id="e8334-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="e8334-133">تتيح رؤى العملاء للدفع للمؤسسات أن تكون أكثر نشاطًا بشأن المجموعات.</span><span class="sxs-lookup"><span data-stu-id="e8334-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="e8334-134">لم يعد عليهم الانتظار حتى تصبح المعاملة مستحقة لبدء عملية التحصيل.</span><span class="sxs-lookup"><span data-stu-id="e8334-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="e8334-135">بدلاً من ذلك، يمكنهم استخدام إمكانية التنبؤات بالدفع لتحديد ما إذا كانت المجموعات الاستباقية ستحسن من احتمال الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="e8334-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="e8334-136">منهجية</span><span class="sxs-lookup"><span data-stu-id="e8334-136">Methodology</span></span>

<span data-ttu-id="e8334-137">وفي الماضي، كان من الصعب عادة تطوير حل الذكاء الاصطناعي (AI) ونشره.</span><span class="sxs-lookup"><span data-stu-id="e8334-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="e8334-138">تطلبت العملية فريقًا يضم علماء البيانات وخبراء الموضوع (SME) والمهندسين، الذين يعملون لفترة طويلة لصياغة وتطوير ونشر وصيانة حل AI صالح للاستعمال.</span><span class="sxs-lookup"><span data-stu-id="e8334-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="e8334-139">تجعل توقعات دفع العميل من السهل نشر حل AI واستخدامه في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e8334-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="e8334-140">تُعد Microsoft حلول AI المعبأة مسبقًا المبنية أعلى Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="e8334-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="e8334-141">لذلك، يمكن للمستخدمين نشر حل AI بنقرة واحدة بالماوس للاستفادة من فوائد التوقعات الذكية.</span><span class="sxs-lookup"><span data-stu-id="e8334-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="e8334-142">إذا لم تكن راضيًا عن دقة التنبؤات، فيمكن للمستخدم القوي (مرة أخر، بنقرة واحدة بالماوس) الدخول في تجربة توسيع AI Builder، ثم تحديد أو إلغاء تحديد الحقول المستخدمة لإنشاء التنبؤات.</span><span class="sxs-lookup"><span data-stu-id="e8334-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="e8334-143">عندما تكون مستعدًا، يمكنك "التدرب" على النموذج ونشر التغييرات.</span><span class="sxs-lookup"><span data-stu-id="e8334-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="e8334-144">سيتم انتقاء النموذج الذي تم التدرب عليه حديثًا تلقائيًا لإنشاء توقعات في Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e8334-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="e8334-145">تفاصيل الإصدار</span><span class="sxs-lookup"><span data-stu-id="e8334-145">Release details</span></span>

<span data-ttu-id="e8334-146">تتوفر معاينة عامة لـ Finance Insights لتجربة عمليات النشر في الولايات المتحدة الأميركية وأوروبا والمملكة المتحدة.</span><span class="sxs-lookup"><span data-stu-id="e8334-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="e8334-147">تُعد Microsoft دعمًا إضافيًا بشكل متزايد لمناطق إضافية.</span><span class="sxs-lookup"><span data-stu-id="e8334-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="e8334-148">يجب أن يتم تشغيل ميزات المعاينة العامة ويجب تشغيلها فقط في بيئات الحماية لتحديد صلاحيات المستوى 2.</span><span class="sxs-lookup"><span data-stu-id="e8334-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="e8334-149">قد لا يمكن ترحيل نماذج الإعداد وAI التي يتم إنشاؤها في بيئة الحماية إلى بيئة التشغيل.</span><span class="sxs-lookup"><span data-stu-id="e8334-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="e8334-150">لمزيد من المعلومات، راجع [شروط الاستخدام الإضافية لمعاينات Microsoft Dynamics 365](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="e8334-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
