---
title: معلومات دفع العميل (معاينة)
description: يصف هذا الموضوع إمكانيات الرؤى الخاصة بالدفع والتي تساعد في تحسين فهم ممارسات الدفع النموذجية للعملاء الفرديين. يمكن أن تساعدك الميزة في تحديد الحالات التي تقوم بضبط بدء عمليات الجمع قبل الانتهاء من القيام بذلك.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 21516cb7ef6e95dcef27638ddb72520f492958a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207317"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="d4877-104">معلومات دفع العميل (معاينة)</span><span class="sxs-lookup"><span data-stu-id="d4877-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d4877-105">يصف هذا الموضوع إمكانيات الرؤى الخاصة بالدفع والتي تساعد في تحسين فهم ممارسات الدفع النموذجية للعملاء الفرديين.</span><span class="sxs-lookup"><span data-stu-id="d4877-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="d4877-106">يمكن أن تساعدك الميزة في تحديد الحالات التي تقوم بضبط بدء عمليات الجمع قبل الانتهاء من القيام بذلك.</span><span class="sxs-lookup"><span data-stu-id="d4877-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="d4877-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d4877-107">Overview</span></span>

<span data-ttu-id="d4877-108">يمكن أن يكون من الصعب توقع الوقت الذي سيقوم فيه العميل بتسديد الفواتير.</span><span class="sxs-lookup"><span data-stu-id="d4877-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="d4877-109">وهذا يعني القيام برؤية أعمق لتقديرات تدفقات نقديه دقيقه اقل وعمليات تحصيل تبدا في وقت طويل جدا ، والأوامر التي يتم إصدارها إلى العملاء الذين قد يقومون بعمليات الدفع بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="d4877-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="d4877-110">تساعد معلومات دفع العميل (المعاينة) المؤسسات في توقع الوقت الذي سيقوم فيه العميل بتسديد فاتورة.</span><span class="sxs-lookup"><span data-stu-id="d4877-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="d4877-111">يمكن أن تساعد هذه المعلومات المؤسسات في إنشاء استراتيجيات التحصيلات التي تحسن احتمال الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4877-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="d4877-112">التوقعات</span><span class="sxs-lookup"><span data-stu-id="d4877-112">Predictions</span></span>

<span data-ttu-id="d4877-113">ستمكّن تنبؤات الدفع المؤسسات من تحسين عملياتها التجارية من خلال مساعدتها على تحديد الفواتير التي يُحتمل سدادها في وقت متأخر ، واتخاذ التدابير المناسبة لتحسين فرصها في الحصول على أموال في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4877-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="d4877-114">باستخدام نموذج للتعلم الآلي ، والذي يعمل على زيادة الفواتير التاريخية والمدفوعات وبيانات العميل ، تتنبأ رؤى دفع العميل (معاينة) بمزيد من الدقة عندما يقوم العميل بدفع فاتورة معلقة.</span><span class="sxs-lookup"><span data-stu-id="d4877-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="d4877-115">لكل فاتورة مفتوحة، يمكن أن تتوقع معلومات دفع العميل (المعاينة) ثلاثة احتمالات دفع:</span><span class="sxs-lookup"><span data-stu-id="d4877-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="d4877-116">احتماليه اجراء الدفع في الوقت الحالي</span><span class="sxs-lookup"><span data-stu-id="d4877-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="d4877-117">احتماليه اجراء الدفع لاحقًا</span><span class="sxs-lookup"><span data-stu-id="d4877-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="d4877-118">احتماليه اجراء الدفع في وقت متأخر جدًا</span><span class="sxs-lookup"><span data-stu-id="d4877-118">Probability of payment being made very late</span></span>

<span data-ttu-id="d4877-119">توفر أيضًا رؤى دفع العملاء (معاينة) في الوقت المحدد والمتأخر والمتأخر جدًا طريقة عرض مجمعة للمدفوعات المتوقعة، الأمر الذي يمكن أن يساعد المؤسسات على فهم إجمالي مبلغ الدفع الذي يمكن أن تتوقعه من أحد العملاء في أحد المجموعات الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="d4877-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="d4877-120">[![العرض المجمع لتنبؤات الدفع](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="d4877-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="d4877-121">ويتم تعيين احتماليه الدفع في كل فاتورة علي الوقت.</span><span class="sxs-lookup"><span data-stu-id="d4877-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="d4877-122">إذا كان احتمال الدفع في الوقت المحدد أقل من 50 ٪ ، يتم وضع علامة الفواتير مع دائرة حمراء للإشارة إلى أن هذه الفواتير قد تتطلب اهتمام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="d4877-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="d4877-123">[![قائمة احتمالات الدفع](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="d4877-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="d4877-124">توفر رؤى دفع العملاء (معاينة) أيضًا معلومات سياقية لشرح التنبؤ ، مثل أهم العوامل التي أثرت على التنبؤات ، وحالة العمل الحالية مع العميل ، وتفاصيل عن سلوك الدفع للعملاء السابقين.</span><span class="sxs-lookup"><span data-stu-id="d4877-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="d4877-125">في العديد من الشركات ، كانت عملية التحصيلات نشاطًا تفاعليًا ؛ لا تبدأ عملية المجموعات إلا بعد استحقاق الفواتير.</span><span class="sxs-lookup"><span data-stu-id="d4877-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="d4877-126">من خلال رؤى العملاء للدفع (معاينة) ، يمكن للمؤسسات أن تكون أكثر نشاطًا بشأن المجموعات.</span><span class="sxs-lookup"><span data-stu-id="d4877-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="d4877-127">لم يعد عليهم الانتظار حتى تصبح المعاملات مستحقة لبدء عملية التحصيل.</span><span class="sxs-lookup"><span data-stu-id="d4877-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="d4877-128">بدلاً من ذلك ، يمكنهم استخدام إمكانية التنبؤ بالدفع لتحديد ما إذا كانت المجموعات الاستباقية ستحسن من احتمال الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d4877-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="d4877-129">كما يوفر التنبؤ بالدفع للشركات المعلومات اللازمة لتبرير بدء عملية التحصيل مبكرًا.</span><span class="sxs-lookup"><span data-stu-id="d4877-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="d4877-130">منهجية</span><span class="sxs-lookup"><span data-stu-id="d4877-130">Methodology</span></span>

<span data-ttu-id="d4877-131">يعد تطوير حل AI ونشره أمرا صعبا.</span><span class="sxs-lookup"><span data-stu-id="d4877-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="d4877-132">يتطلب الأمر فريقًا من علماء البيانات وخبراء الموضوع والمهندسين، يعملون لفترة طويلة من الزمن لصياغة وتطوير ونشر وصيانة حل AI صالح للاستعمال.</span><span class="sxs-lookup"><span data-stu-id="d4877-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="d4877-133">نحن نسهل نشر واستخدام حلول الذكاء الاصطناعي في Finance.</span><span class="sxs-lookup"><span data-stu-id="d4877-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="d4877-134">نحن نعد حلول AI المعبأة مسبقًا في Finance المبنية أعلى Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="d4877-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="d4877-135">يمكن للمستخدم النهائي ، بنقرة زر واحدة ، نشر حل الذكاء الاصطناعي والبدء في الاستفادة من فوائد التنبؤات الذكية.</span><span class="sxs-lookup"><span data-stu-id="d4877-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="d4877-136">إذا لم تكن أي مؤسسة راضية عن دقة التنبؤات، فيمكن للمستخدم القوي، مرة أخرى باستخدام نقرة واحدة، الدخول في تجربة توسيع AI builder، ثم تحديد أو إلغاء تحديد الحقول المستخدمة لإنشاء التنبؤات.</span><span class="sxs-lookup"><span data-stu-id="d4877-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="d4877-137">بمجرد الاستعداد ، يمكنهم تدريب ونشر التغييرات ، وسيتم اختيار النموذج المدربين حديثًا تلقائيًا للتنبؤات في Finance.</span><span class="sxs-lookup"><span data-stu-id="d4877-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="d4877-138">كيفية الحصول على معلومات دفع العميل (المعاينة)</span><span class="sxs-lookup"><span data-stu-id="d4877-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="d4877-139">أرسل بريد إلكتروني إلى [معلومات دفع العميل (المعاينة)](mailto:fiap@microsoft.com)، إذا كنت ترغب في تجربة معلومات دفع العميل (المعاينة).</span><span class="sxs-lookup"><span data-stu-id="d4877-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="d4877-140">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="d4877-140">Privacy Notice</span></span>

<span data-ttu-id="d4877-141">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="d4877-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]