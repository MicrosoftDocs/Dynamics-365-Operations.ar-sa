---
title: تقدير التدفقات النقدية (معاينة)
description: يصف هذا الموضوع قدرة تقدير التدفقات النقدية.
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 64935db3b50e7598f2076ecbec72aba020d4f908
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186530"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="ebe75-103">تقدير التدفقات النقدية (معاينة)</span><span class="sxs-lookup"><span data-stu-id="ebe75-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ebe75-104">يعد التدفق النقدي ضروريًا لأي عمل.</span><span class="sxs-lookup"><span data-stu-id="ebe75-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="ebe75-105">حتى الشركات الربحية يمكن أن تواجه مشكلة عدم القدرة على الدفع إذا لم تكن تحتفظ بالتدفق النقدي لتلبية الاحتياجات الفورية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="ebe75-106">يمكن لقدرات تقدير التدفقات النقدية في Finance insights أن تساعد الشركات على مراقبة أرصدة النقد وإدارتها بشكل فعال.</span><span class="sxs-lookup"><span data-stu-id="ebe75-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="ebe75-107">تستخدم هذه الميزة التعلم الآلي لمساعدة الشركات في التنبؤ بالتدفقات النقدية بشكل أكثر دقة من التي كانت متوفرة في وقت سابق.</span><span class="sxs-lookup"><span data-stu-id="ebe75-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="ebe75-108">كما يمكن أن تساعد المديرين على اتخاذ قرارات تحسن الفرص في سياق المنصب النقدي الحالي الخاص بهم.</span><span class="sxs-lookup"><span data-stu-id="ebe75-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="ebe75-109">بالنسبة لمعظم الشركات، تعتبر إدارة التدفقات النقدية والتنبؤ بالتدفقات النقدية قيد التشغيل عملية مملة ومتكررة ويدوية</span><span class="sxs-lookup"><span data-stu-id="ebe75-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="ebe75-110">تعتمد معظم الشركات على حلول Microsoft Excel التي بها درجات مختلفة من التعقيد.</span><span class="sxs-lookup"><span data-stu-id="ebe75-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="ebe75-111">تتضمن تحديات التنبؤ النقدي بشكل دقيق ما يلي:</span><span class="sxs-lookup"><span data-stu-id="ebe75-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="ebe75-112">البيانات غير متاحة لصانعي القرارات نظرًا لأنها مبعثرة في أماكن متعددة، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="ebe75-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="ebe75-113">نظام الحسابات أو نظام تخطيط موارد المؤسسة</span><span class="sxs-lookup"><span data-stu-id="ebe75-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="ebe75-114">برنامج التخطيط المالي</span><span class="sxs-lookup"><span data-stu-id="ebe75-114">Financial planning software</span></span>
  - <span data-ttu-id="ebe75-115">Excel</span><span class="sxs-lookup"><span data-stu-id="ebe75-115">Excel</span></span>
  - <span data-ttu-id="ebe75-116">تطبيقات برامج إضافية</span><span class="sxs-lookup"><span data-stu-id="ebe75-116">Additional software applications</span></span> 
- <span data-ttu-id="ebe75-117">يعتمد التنبؤ على المعارف الداخلية الموجودة في "مستودعات" داخل كل مجال أو قسم.</span><span class="sxs-lookup"><span data-stu-id="ebe75-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="ebe75-118">يُعد قياس دقة تقدير التدفق النقدي بعد تحقيق الماليات أمرًا غير مؤكد وصعب.</span><span class="sxs-lookup"><span data-stu-id="ebe75-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="ebe75-119">تفاصيل قدرة تقديرات التدفقات النقدية</span><span class="sxs-lookup"><span data-stu-id="ebe75-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="ebe75-120">تتضمن ميزة تقديرات التدفقات النقدية الوظائف التالية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="ebe75-121">يسهل تكامل بيانات التدفق النقدي عن الأنظمة الخارجية إلى Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ebe75-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="ebe75-122">يمكن أن تستخدم تقديرات التدفقات النقدية أيضًا إطار عمل استيراد-تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="ebe75-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="ebe75-123">يسهل إطار العمل هذا عملية التكامل مع Excel OData.</span><span class="sxs-lookup"><span data-stu-id="ebe75-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="ebe75-124">يمكنك أيضًا جمع البيانات من مصادر متعددة لإنشاء حل تدفق نقدي شامل.</span><span class="sxs-lookup"><span data-stu-id="ebe75-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="ebe75-125">يقدم وظيفة نقدية ذكية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="ebe75-126">يتم إنشاء المنصب النقدي استنادًا إلى سلوك الدفع الخاص بالعميل للتنبؤ بالوقت الذي يمكن أن تتوقع به الشركة الدفع في حساباتها.</span><span class="sxs-lookup"><span data-stu-id="ebe75-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="ebe75-127">ويقوم أيضًا بتحليل الأنماط التاريخية للموردين المدفوعين، للتنبؤ باحتمال دفع الفواتير والأوامر المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="ebe75-128">يقدم تقديرًا لتدفق النقدية الذكية للتنبؤ من المدى البعيد، باستخدام التنبؤ بالتسلسل الزمني من خلال التكامل التلقائي AI Builder.</span><span class="sxs-lookup"><span data-stu-id="ebe75-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="ebe75-129">يوفر إمكانية حفظ موضع تدفق نقدي معين أو التنبؤات وتحريرها، ثم مقارنة أداء التنبؤ وقياسه بسهولة في الأمور المالية الفعلية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="ebe75-130">يعمل على تمكين تحليل ماذا إذا خلال مقارنة اللقطات.</span><span class="sxs-lookup"><span data-stu-id="ebe75-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="ebe75-131">على سبيل المثال، يمكنك إنشاء لقطات متعددة تمثل طرق عرض تدفق نقد متفائلة ومتشائمة وأكثر واقعية، ثم مقارنة الاختلافات وعرضها.</span><span class="sxs-lookup"><span data-stu-id="ebe75-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="ebe75-132">يوفر إمكانية عرض تقدير التدفقات النقدية بعملات متعددة وعبر الكيانات القانونية وتصفية وعرض التدفق النقدي المرتبط بحساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="ebe75-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="ebe75-133">يتيح لك تصفية الحسابات البنكية المرتبطة بالأبعاد المالية وعرضها.</span><span class="sxs-lookup"><span data-stu-id="ebe75-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="ebe75-134">ستعمل وظيفة تقدير التدفقات في Dynamics 365 Finance على زيادة موظفين المؤسسة لتحويل توقع التدفقات النقدية المعقد والممل والمتكرر إلى عملية بسيطة وتلقائية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="ebe75-135">يتيح لك التركيز على أهم الأوجه الخاصة بتقدير التدفقات النقدية التركيز على القرارات الهامة للحصول على نتائج الأعمال المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="ebe75-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="ebe75-136">إعداد الأبعاد الخاصة بتقدير التدفقات النقدية</span><span class="sxs-lookup"><span data-stu-id="ebe75-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="ebe75-137">تتيح لك علامة التبويب الجديدة في الصفحة **إعداد التنبؤ بالتدفق النقدي** التحكم في الأبعاد المالية التي يجب استخدامها للتصفية في مساحة العمل **تقدير التدفقات النقدية**.</span><span class="sxs-lookup"><span data-stu-id="ebe75-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="ebe75-138">لن تظهر علامة التبويب هذه إلا في حالة تمكين ميزة تقديرات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="ebe75-139">من علامة التبويب **الأبعاد**، اختر من قائمة الأبعاد المراد استخدامها للتصفية، واستخدم مفاتيح الأسهم لنقلها إلى العمود الأيمن.</span><span class="sxs-lookup"><span data-stu-id="ebe75-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="ebe75-140">يمكن تحديد بُعدين فقط لتصفية بيانات تقدير التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="ebe75-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
