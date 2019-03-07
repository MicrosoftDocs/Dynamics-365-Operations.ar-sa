---
title: معلومات دفع العميل (المعاينة)
description: يصف هذا الموضوع كيف يمكن لمعلومات دفع العميل المساعدة في توقع الوقت الذي سيتم فيه دفع فاتورة ما ومساعدة المؤسسات على إنشاء استراتيجيات تحسين تعمل على تحسين احتمال تلقي الدفع في الوقت المحدد.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "344652"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="d16ac-103">معلومات دفع العميل (المعاينة)</span><span class="sxs-lookup"><span data-stu-id="d16ac-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="d16ac-104">هذه الميزة عبارة عن جزء من إصدار مستهدف، وهي تتوفر فقط للمستخدمين الذين اختاروا الاشتراك في المعاينة الخاصة‬.</span><span class="sxs-lookup"><span data-stu-id="d16ac-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="d16ac-105">سيتم تضمين هذه الميزة في إصدار توفر عام قادم.</span><span class="sxs-lookup"><span data-stu-id="d16ac-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="d16ac-106">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d16ac-106">Overview</span></span>

<span data-ttu-id="d16ac-107">تجد المؤسسات في أغلب الأحيان أنه من الصعب توقع الوقت الذي سيقوم فيه العميل بتسديد الفواتير.</span><span class="sxs-lookup"><span data-stu-id="d16ac-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="d16ac-108">قد يؤدي هذا القصور في المعرفة إلى تنبؤات غير دقيقة تتعلق بالتدفقات النقدية وعمليات تحصيل غير فعالة وإمكانية تنفيذ أوامر صادرة عن عملاء قد يشكلون خطرًا ائتمانيًا.</span><span class="sxs-lookup"><span data-stu-id="d16ac-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="d16ac-109">تستخدم معلومات دفع العميل (المعاينة) التعلم الآلي‬ لتوقع الوقت الذي سيتم فيه تسديد فاتورة.</span><span class="sxs-lookup"><span data-stu-id="d16ac-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="d16ac-110">وهي توفر أيضًا استراتيجيات تحسين يمكن تخصيصها لزيادة احتمال قيام العملاء بتسديد الدفع في الوقت المحدد إلى أقصى حد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="d16ac-111">التوقعات</span><span class="sxs-lookup"><span data-stu-id="d16ac-111">Predictions</span></span>

<span data-ttu-id="d16ac-112">تسمح توقعات الدفع للمؤسسات بتحسين عملياتها التجارية عبر مساعدتها على القيام بما يلي.</span><span class="sxs-lookup"><span data-stu-id="d16ac-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="d16ac-113">التعرف بسهولة على الفواتير التي من المتوقع أن يتم تسديدها في وقت متأخر.</span><span class="sxs-lookup"><span data-stu-id="d16ac-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="d16ac-114">اتخاذ الإجراءات المناسبة لتحسين فرص تلقي الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="d16ac-115">تستخدم معلومات دفع العميل (المعاينة) التعلم الآلي‬ لتوقع الوقت الذي سيتم فيه تسديد فاتورة.</span><span class="sxs-lookup"><span data-stu-id="d16ac-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="d16ac-116">وهي تستخدم بيانات الفواتير والدفع القديمة الخاصة بالعميل لإنشاء نموذج تعلم آلي يُستخدم لتوقع الوقت الذي سيتم فيه تسديد الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d16ac-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="d16ac-117">لكل فاتورة مفتوحة، تتوقع معلومات دفع العميل (المعاينة) ثلاثة احتمالات دفع:</span><span class="sxs-lookup"><span data-stu-id="d16ac-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="d16ac-118">احتمال الدفع في الوقت المحدد (ضمن تاريخ استحقاق الفاتورة).</span><span class="sxs-lookup"><span data-stu-id="d16ac-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="d16ac-119">احتمال الدفع في غضون 30 يومًا من تاريخ استحقاق الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d16ac-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="d16ac-120">احتمال الدفع بعد مرور 30 يومًا على تاريخ استحقاق الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="d16ac-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="d16ac-121">يمكن عرض احتمالات الدفع في قسم التوقعات.</span><span class="sxs-lookup"><span data-stu-id="d16ac-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="d16ac-122">[![توقعات الدفع](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="d16ac-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="d16ac-123">يتم أيضًا تعيين احتمال دفع لكل فاتورة باستخدام أحد سيناروهات احتمالات الدفع المتوقعة المحددة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="d16ac-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="d16ac-124">وسيكون السيناريو الفائز السيناريو ذي احتمال دفع أعلى.</span><span class="sxs-lookup"><span data-stu-id="d16ac-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="d16ac-125">على سبيل المثال، لنفترض أنه بالنسبة إلى فاتورة ما يُظهر التوقع احتمالاً بنسبة 71 بالمئة بأن الفاتورة ستُدفع في الوقت المحدد واحتمالاً بنسبة 13 بالمئة بأن الفاتورة ستُدفع في غضون 30 يومًا من تاريخ الاستحقاق واحتمالاً بنسبة 16 بالمئة بأن الفاتورة ستُدفع بعد مرور 30 يومًا على تاريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="d16ac-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="d16ac-126">يُظهر الاحتمال الأعلى أن الفاتورة ستكون في سيناريو الدفع في الوقت المحدد، وبالتالي ستوضع عليها علامة احتمال الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="d16ac-127">[![توقعات الدفع](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="d16ac-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="d16ac-128">استراتيجيات التحسين</span><span class="sxs-lookup"><span data-stu-id="d16ac-128">Optimization strategies</span></span>

<span data-ttu-id="d16ac-129">بالإضافة إلى توقعات الدفع، تستخدم معلومات دفع العميل (المعاينة) استراتيجيات تحسين الأداء لتحسين فرص استلام الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="d16ac-130">يسمح هذا الأمر المؤسسات بإجراء تحليلات "ماذا لو" من خلال السماح للمستخدمين بضبط معلمات الفواتير والعملاء ثم مقارنة التأثير المطابق على احتمال استلام الدفع على الفواتير في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="d16ac-131">على سبيل المثال، قد ترغب إحدى المؤسسات في تقييم تأثير تحديث الخصم النقدي على الفواتير على احتمال استلام الدفع في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="d16ac-132">وعندما يتم تحسين الفواتير لاستخدام خصم جديد، يستطيع المستخدمون مراجعة تأثير تطبيق الخصم على احتمال استلام دفعات هذه الفواتير في الوقت المحدد.</span><span class="sxs-lookup"><span data-stu-id="d16ac-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="d16ac-133">إذا كانت تكلفة تطبيق الخصم النقدي قليلة عند مقارنته بفائدة تحصيل الدفع في الوقت المحدد، قد تختار المؤسسة تطبيق الخصم المحدد على كافة الأوامر المفتوحة المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="d16ac-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="d16ac-134">في الوقت الحالي، يتوفر الخصم فقط كاستراتيجية تحسين لمعلومات دفع العميل (المعاينة).</span><span class="sxs-lookup"><span data-stu-id="d16ac-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="d16ac-135">[![التوقعات المحسنة](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="d16ac-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="d16ac-136">كيفية الحصول على معلومات دفع العميل (المعاينة)</span><span class="sxs-lookup"><span data-stu-id="d16ac-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="d16ac-137">إذا كنت ترغب في تجربة معلومات دفع العميل (المعاينة)، الرجاء إرسال بريد إلكتروني إلى [فريق Finance Insights Preview](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="d16ac-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="d16ac-138">بيان الخصوصية</span><span class="sxs-lookup"><span data-stu-id="d16ac-138">Privacy Statement</span></span>

<span data-ttu-id="d16ac-139">معاينات بيانات العملاء في المتجر في الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="d16ac-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="d16ac-140">بالإضافة إلى ذلك، فإن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 for Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="d16ac-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
