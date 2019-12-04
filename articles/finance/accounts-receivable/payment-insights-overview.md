---
title: معلومات دفع العميل (معاينة)
description: يصف هذا الموضوع إمكانيات الرؤى الخاصة بالدفع والتي تساعد في تحسين الفهم الخاص بممارسات الدفع النموذجية للعملاء الفرديين ويمكنه تحديد الحالات التي تقوم بضبط بدء عمليات الجمع قبل القيام بالاجراء السابق
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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773890"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="95ce6-103">معلومات دفع العميل (معاينة)</span><span class="sxs-lookup"><span data-stu-id="95ce6-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="95ce6-104">يصف هذا الموضوع إمكانيات الرؤى الخاصة بالدفع والتي تساعد في تحسين الفهم الخاص بممارسات الدفع النموذجية للعملاء الفرديين ويمكنه تحديد الحالات التي تقوم بضبط بدء عمليات الجمع قبل القيام بالاجراء السابق</span><span class="sxs-lookup"><span data-stu-id="95ce6-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="95ce6-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="95ce6-105">Overview</span></span>

<span data-ttu-id="95ce6-106">تجد المؤسسات في أغلب الأحيان أنه من الصعب توقع الوقت الذي سيقوم فيه العميل بتسديد الفواتير.</span><span class="sxs-lookup"><span data-stu-id="95ce6-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="95ce6-107">وهذا يعني القيام برؤية أعمق لتقديرات تدفقات نقديه دقيقه اقل وعمليات تحصيل تبدا في وقت طويل جدا ، والأوامر التي يتم إصدارها إلى العملاء الذين قد يقومون بعمليات الدفع بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="95ce6-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="95ce6-108">تساعد رؤى دفع العملاء (معاينة) المؤسسات على التنبؤ بموعد دفع فاتورة العميل ، مما يساعد المؤسسة في إنشاء استراتيجيات للتحصيل تعمل على تحسين احتمال الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="95ce6-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="95ce6-109">التوقعات</span><span class="sxs-lookup"><span data-stu-id="95ce6-109">Predictions</span></span>

<span data-ttu-id="95ce6-110">ستمكّن تنبؤات الدفع المؤسسات من تحسين عملياتها التجارية من خلال مساعدتها على تحديد الفواتير التي يُحتمل سدادها في وقت متأخر ، واتخاذ التدابير المناسبة لتحسين فرصها في الحصول على أموال في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="95ce6-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="95ce6-111">باستخدام نموذج للتعلم الآلي ، والذي يعمل على زيادة الفواتير التاريخية والمدفوعات وبيانات العميل ، تتنبأ رؤى دفع العميل (معاينة) بمزيد من الدقة عندما يقوم العميل بدفع فاتورة معلقة.</span><span class="sxs-lookup"><span data-stu-id="95ce6-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="95ce6-112">لكل فاتورة مفتوحة، تتوقع معلومات دفع العميل (المعاينة) ثلاثة احتمالات دفع:</span><span class="sxs-lookup"><span data-stu-id="95ce6-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="95ce6-113">احتماليه اجراء الدفع في الوقت الحالي</span><span class="sxs-lookup"><span data-stu-id="95ce6-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="95ce6-114">احتماليه اجراء الدفع لاحقًا</span><span class="sxs-lookup"><span data-stu-id="95ce6-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="95ce6-115">احتماليه اجراء الدفع في وقت متأخر جدًا</span><span class="sxs-lookup"><span data-stu-id="95ce6-115">Probability of payment being made very late</span></span>

<span data-ttu-id="95ce6-116">لمساعدة المؤسسات على فهم إجمالي مبلغ الدفع الذي يمكن أن تتوقعه من أحد العملاء في أحد المجموعات الثلاثة ، توفر أيضًا رؤى دفع العملاء (معاينة) في الوقت المحدد والمتأخر والمتأخر جدًا طريقة عرض مجمعة للمدفوعات المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="95ce6-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="95ce6-117">[![العرض المجمع لتنبؤات الدفع](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="95ce6-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="95ce6-118">ويتم تعيين احتماليه الدفع في كل فاتورة علي الوقت.</span><span class="sxs-lookup"><span data-stu-id="95ce6-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="95ce6-119">إذا كان احتمال الدفع في الوقت المحدد أقل من 50 ٪ ، يتم وضع علامة الفواتير مع دائرة حمراء للإشارة إلى أن هذه الفواتير قد تتطلب اهتمام المجموعات.</span><span class="sxs-lookup"><span data-stu-id="95ce6-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="95ce6-120">[![قائمة احتمالات الدفع](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="95ce6-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="95ce6-121">توفر رؤى دفع العملاء (معاينة) أيضًا معلومات سياقية لشرح التنبؤ ، مثل أهم العوامل التي أثرت على التنبؤات ، وحالة العمل الحالية مع العميل ، وتفاصيل عن سلوك الدفع للعملاء السابقين.</span><span class="sxs-lookup"><span data-stu-id="95ce6-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="95ce6-122">في العديد من الشركات ، كانت عملية التحصيلات نشاطًا تفاعليًا ؛ لا تبدأ عملية المجموعات إلا بعد استحقاق الفواتير.</span><span class="sxs-lookup"><span data-stu-id="95ce6-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="95ce6-123">من خلال رؤى العملاء للدفع (معاينة) ، يمكن للمؤسسات أن تكون أكثر نشاطًا بشأن المجموعات.</span><span class="sxs-lookup"><span data-stu-id="95ce6-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="95ce6-124">لم يعد عليهم الانتظار حتى تصبح المعاملات مستحقة لبدء عملية التحصيل.</span><span class="sxs-lookup"><span data-stu-id="95ce6-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="95ce6-125">بدلاً من ذلك ، يمكنهم استخدام إمكانية التنبؤ بالدفع لتحديد ما إذا كانت المجموعات الاستباقية ستحسن من احتمال الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="95ce6-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="95ce6-126">كما يوفر التنبؤ بالدفع للشركات المعلومات اللازمة لتبرير بدء عملية التحصيل مبكرًا.</span><span class="sxs-lookup"><span data-stu-id="95ce6-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="95ce6-127">منهجية</span><span class="sxs-lookup"><span data-stu-id="95ce6-127">Methodology</span></span>

<span data-ttu-id="95ce6-128">يعد تطوير حل AI ونشره أمرا صعبا.</span><span class="sxs-lookup"><span data-stu-id="95ce6-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="95ce6-129">يتطلب الأمر فريقًا من علماء البيانات وخبراء الموضوع والمهندسين ، يعملون لفترة طويلة من الزمن لصياغة وتطوير ونشر وصيانة حل AI صالح للاستعمال.</span><span class="sxs-lookup"><span data-stu-id="95ce6-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="95ce6-130">نحن نسهل نشر واستخدام حلول الذكاء الاصطناعي في Finance.</span><span class="sxs-lookup"><span data-stu-id="95ce6-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="95ce6-131">نحن نعد حلول AI المعبأة مسبقًا في Finance المبنية أعلى Microsoft AI Builder.</span><span class="sxs-lookup"><span data-stu-id="95ce6-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="95ce6-132">يمكن للمستخدم النهائي ، بنقرة زر واحدة ، نشر حل الذكاء الاصطناعي والبدء في الاستفادة من فوائد التنبؤات الذكية.</span><span class="sxs-lookup"><span data-stu-id="95ce6-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="95ce6-133">إذا لم تكن أي مؤسسة راضية عن دقة التنبؤات، فيمكن للمستخدم القوي، مرة أخرى باستخدام نقرة واحدة، الدخول في تجربة توسيع AI builder، ثم تحديد أو إلغاء تحديد الحقول المستخدمة لإنشاء التنبؤات.</span><span class="sxs-lookup"><span data-stu-id="95ce6-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="95ce6-134">بمجرد الاستعداد ، يمكنهم تدريب ونشر التغييرات ، وسيتم اختيار النموذج المدربين حديثًا تلقائيًا للتنبؤات في Finance.</span><span class="sxs-lookup"><span data-stu-id="95ce6-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="95ce6-135">كيفية الحصول على معلومات دفع العميل (المعاينة)</span><span class="sxs-lookup"><span data-stu-id="95ce6-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="95ce6-136">يُرجى إرسال بريد إلكتروني إلى [معلومات دفع العميل (المعاينة)](mailto:fiap@microsoft.com)، إذا كنت ترغب في تجربة معلومات دفع العميل (المعاينة).</span><span class="sxs-lookup"><span data-stu-id="95ce6-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="95ce6-137">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="95ce6-137">Privacy Notice</span></span>

<span data-ttu-id="95ce6-138">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="95ce6-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


