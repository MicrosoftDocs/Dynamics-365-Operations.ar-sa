---
title: تقدير التدفقات النقدية (معاينة)
description: يصف هذا الموضوع قدرة تقدير التدفقات النقدية.
author: ShivamPandey-msft
ms.date: 05/19/2020
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6e4713aa4662714d1b2a3eeb62adce8608907054
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811401"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="7a664-103">تقدير التدفقات النقدية (معاينة)</span><span class="sxs-lookup"><span data-stu-id="7a664-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7a664-104">يعد التدفق النقدي ضروريًا لأي عمل.</span><span class="sxs-lookup"><span data-stu-id="7a664-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="7a664-105">حتى الشركات الربحية يمكن أن تواجه مشكلة عدم القدرة على الدفع إذا لم تكن تحتفظ بالتدفق النقدي لتلبية الاحتياجات الفورية.</span><span class="sxs-lookup"><span data-stu-id="7a664-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="7a664-106">يمكن لقدرات تقدير التدفقات النقدية في Finance insights أن تساعد الشركات على مراقبة أرصدة النقد وإدارتها بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="7a664-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="7a664-107">تستخدم هذه الميزة التعلم الآلي لمساعدة الشركات في التنبؤ بالتدفقات النقدية بشكل أكثر دقة من التي كانت متوفرة في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="7a664-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="7a664-108">كما يمكن أن تساعد المديرين على اتخاذ قرارات تحسن الفرص في سياق المنصب النقدي الحالي الخاص بهم.</span><span class="sxs-lookup"><span data-stu-id="7a664-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="7a664-109">بالنسبة لمعظم الشركات، تعتبر إدارة التدفقات النقدية والتنبؤ بالتدفقات النقدية قيد التشغيل عملية مملة ومتكررة ويدوية</span><span class="sxs-lookup"><span data-stu-id="7a664-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="7a664-110">تعتمد معظم الشركات على حلول Microsoft Excel التي بها درجات مختلفة من التعقيد.</span><span class="sxs-lookup"><span data-stu-id="7a664-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="7a664-111">تتضمن تحديات التنبؤ النقدي بشكل دقيق ما يلي:</span><span class="sxs-lookup"><span data-stu-id="7a664-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="7a664-112">البيانات غير متاحة لصانعي القرارات نظرًا لأنها مبعثرة في أماكن متعددة، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="7a664-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="7a664-113">نظام الحسابات أو نظام تخطيط موارد المؤسسة</span><span class="sxs-lookup"><span data-stu-id="7a664-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="7a664-114">برنامج التخطيط المالي</span><span class="sxs-lookup"><span data-stu-id="7a664-114">Financial planning software</span></span>
  - <span data-ttu-id="7a664-115">Excel</span><span class="sxs-lookup"><span data-stu-id="7a664-115">Excel</span></span>
  - <span data-ttu-id="7a664-116">تطبيقات برامج إضافية</span><span class="sxs-lookup"><span data-stu-id="7a664-116">Additional software applications</span></span> 
- <span data-ttu-id="7a664-117">يعتمد التنبؤ على المعارف الداخلية الموجودة في "مستودعات" داخل كل مجال أو قسم.</span><span class="sxs-lookup"><span data-stu-id="7a664-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="7a664-118">يُعد قياس دقة تقدير التدفق النقدي بعد تحقيق الماليات أمرًا غير مؤكد وصعب.</span><span class="sxs-lookup"><span data-stu-id="7a664-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="7a664-119">تفاصيل قدرة تقديرات التدفقات النقدية</span><span class="sxs-lookup"><span data-stu-id="7a664-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="7a664-120">تتضمن ميزة تقديرات التدفقات النقدية الوظائف التالية.</span><span class="sxs-lookup"><span data-stu-id="7a664-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="7a664-121">يسهل تكامل بيانات التدفق النقدي عن الأنظمة الخارجية إلى Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7a664-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="7a664-122">يمكن أن تستخدم تقديرات التدفقات النقدية أيضًا إطار عمل استيراد-تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="7a664-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="7a664-123">يسهل إطار العمل هذا عملية التكامل مع Excel OData.</span><span class="sxs-lookup"><span data-stu-id="7a664-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="7a664-124">يمكنك أيضًا جمع البيانات من مصادر متعددة لإنشاء حل تدفق نقدي شامل.</span><span class="sxs-lookup"><span data-stu-id="7a664-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="7a664-125">يقدم وظيفة نقدية ذكية.</span><span class="sxs-lookup"><span data-stu-id="7a664-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="7a664-126">يتم إنشاء المنصب النقدي استنادًا إلى سلوك الدفع الخاص بالعميل للتنبؤ بالوقت الذي يمكن أن تتوقع به الشركة الدفع في حساباتها.</span><span class="sxs-lookup"><span data-stu-id="7a664-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="7a664-127">ويقوم أيضًا بتحليل الأنماط التاريخية للموردين المدفوعين، للتنبؤ باحتمال دفع الفواتير والأوامر المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="7a664-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="7a664-128">يقدم تقديرًا لتدفق النقدية الذكية للتنبؤ من المدى البعيد، باستخدام التنبؤ بالتسلسل الزمني من خلال التكامل التلقائي AI Builder.</span><span class="sxs-lookup"><span data-stu-id="7a664-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="7a664-129">يوفر إمكانية حفظ موضع تدفق نقدي معين أو التنبؤات وتحريرها، ثم مقارنة أداء التنبؤ وقياسه بسهولة في الأمور المالية الفعلية.</span><span class="sxs-lookup"><span data-stu-id="7a664-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="7a664-130">يعمل على تمكين تحليل ماذا إذا خلال مقارنة اللقطات.</span><span class="sxs-lookup"><span data-stu-id="7a664-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="7a664-131">على سبيل المثال، يمكنك إنشاء لقطات متعددة تمثل طرق عرض تدفق نقد متفائلة ومتشائمة وأكثر واقعية، ثم مقارنة الاختلافات وعرضها.</span><span class="sxs-lookup"><span data-stu-id="7a664-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="7a664-132">يوفر إمكانية عرض تقدير التدفقات النقدية بعملات متعددة وعبر الكيانات القانونية وتصفية وعرض التدفق النقدي المرتبط بحساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="7a664-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="7a664-133">يتيح لك تصفية الحسابات البنكية المرتبطة بالأبعاد المالية وعرضها.</span><span class="sxs-lookup"><span data-stu-id="7a664-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="7a664-134">ستعمل وظيفة تقدير التدفقات في Dynamics 365 Finance على زيادة موظفين المؤسسة لتحويل توقع التدفقات النقدية المعقد والممل والمتكرر إلى عملية بسيطة وتلقائية.</span><span class="sxs-lookup"><span data-stu-id="7a664-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="7a664-135">يتيح لك التركيز على أهم الأوجه الخاصة بتقدير التدفقات النقدية التركيز على القرارات الهامة للحصول على نتائج الأعمال المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="7a664-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="7a664-136">إعداد الأبعاد الخاصة بتقدير التدفقات النقدية</span><span class="sxs-lookup"><span data-stu-id="7a664-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="7a664-137">تتيح لك علامة التبويب الجديدة في الصفحة **إعداد التنبؤ بالتدفق النقدي** التحكم في الأبعاد المالية التي يجب استخدامها للتصفية في مساحة العمل **تقدير التدفقات النقدية**.</span><span class="sxs-lookup"><span data-stu-id="7a664-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="7a664-138">لن تظهر علامة التبويب هذه إلا في حالة تمكين ميزة تقديرات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="7a664-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="7a664-139">من علامة التبويب **الأبعاد**، اختر من قائمة الأبعاد المراد استخدامها للتصفية، واستخدم مفاتيح الأسهم لنقلها إلى العمود الأيمن.</span><span class="sxs-lookup"><span data-stu-id="7a664-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="7a664-140">يمكن تحديد بُعدين فقط لتصفية بيانات تقدير التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="7a664-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="7a664-141">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="7a664-141">Privacy notice</span></span>
<span data-ttu-id="7a664-142">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="7a664-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]