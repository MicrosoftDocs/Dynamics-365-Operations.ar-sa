---
title: تحسين نموذج التنبؤ (معاينة)
description: يوضح هذا الموضوع الميزات التي يمكنك استخدامها لتحسين أداء نماذج التنبؤ.
author: ShivamPandey-msft
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 197aba724ea68ef79c2d16028c23533d952329a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809996"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="c9a78-103">تحسين نموذج التنبؤ (معاينة)</span><span class="sxs-lookup"><span data-stu-id="c9a78-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c9a78-104">يوضح هذا الموضوع الميزات التي يمكنك استخدامها لتحسين أداء نماذج التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="c9a78-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="c9a78-105">ستبدأ في تحسين النموذج الخاص بك في مساحة العمل **توقعات دفع العميل** في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c9a78-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="c9a78-106">عندئذ يتم إكمال خطوات التحسين في AI Builder.</span><span class="sxs-lookup"><span data-stu-id="c9a78-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="c9a78-107">تحديد النتائج التاريخية</span><span class="sxs-lookup"><span data-stu-id="c9a78-107">Select historical outcomes</span></span>

<span data-ttu-id="c9a78-108">قم أولاً بتحديد واحدًا أو أكثر من النتائج الثلاثة المحتملة للفواتير: **في الوقت المحدد** و **متأخر** و **متأخر جدًا**.</span><span class="sxs-lookup"><span data-stu-id="c9a78-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="c9a78-109">يجب تحديد كافة النتائج الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="c9a78-109">All three outcomes should be selected.</span></span> <span data-ttu-id="c9a78-110">إذا قمت بإلغاء تحديد أي من النتائج، فإنه سيتم تصفية الفواتير خارج عملية التدريب وسيتم تقليل دقة التوقع.</span><span class="sxs-lookup"><span data-stu-id="c9a78-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="c9a78-111">[![تأكيد النتائج](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="c9a78-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="c9a78-112">إذا كانت مؤسستك تتطلب اثنين من النتائج فقط، فقم بتغيير الحدود **متأخر** و **متأخر جدًا** إلى 0 (صفر) يومًا.</span><span class="sxs-lookup"><span data-stu-id="c9a78-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="c9a78-113">بهذه الطريقة، يمكنك بشكل فعال طي التوقع إلى الحالة الثنائية **في الوقت المحدد** أو **متأخر**.</span><span class="sxs-lookup"><span data-stu-id="c9a78-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="c9a78-114">تحديد الحقول</span><span class="sxs-lookup"><span data-stu-id="c9a78-114">Select fields</span></span>

<span data-ttu-id="c9a78-115">عند تحديد الحقول التي سيتم تضمينها في النموذج، يجب الانتباه إلى أن القائمة تتضمن كافة الحقول المتوفرة في جدول Microsoft Dataverse الذي تم تعيينه إلى البيانات في Azure data lake.</span><span class="sxs-lookup"><span data-stu-id="c9a78-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="c9a78-116">يجب **عدم** تحديد بعض هذه الحقول.</span><span class="sxs-lookup"><span data-stu-id="c9a78-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="c9a78-117">تقع الحقول التي يجب عدم تحديدها ضمن واحدة من الفئات الثلاثة التالية:</span><span class="sxs-lookup"><span data-stu-id="c9a78-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="c9a78-118">الحقل مطلوب للجدول Dataverse، ولكن لا توجد بيانات احتياطية له في data lake.</span><span class="sxs-lookup"><span data-stu-id="c9a78-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="c9a78-119">يعتبر هذا الحقل معرف وبالتالي لا يكون له معنى لميزة "التعلم الآلي".</span><span class="sxs-lookup"><span data-stu-id="c9a78-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="c9a78-120">يمثل الحقل المعلومات التي لن تكون متوفرة أثناء التوقع.</span><span class="sxs-lookup"><span data-stu-id="c9a78-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="c9a78-121">توضح الأقسام التالية الحقول المتاحة لكيانات الفاتورة والعميل، وتسرد الحقول التي يجب **عدم** تحديدها للتدريب.</span><span class="sxs-lookup"><span data-stu-id="c9a78-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="c9a78-122">تشير الفئة المحددة لكل من هذه الحقول إلى الفئات الموجودة في القائمة السابقة.</span><span class="sxs-lookup"><span data-stu-id="c9a78-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="c9a78-123">جدول فاتورة Dataverse</span><span class="sxs-lookup"><span data-stu-id="c9a78-123">Invoice Dataverse table</span></span>

<span data-ttu-id="c9a78-124">يبين الرسم التوضيحي التالي الحقول المتوفرة لجدول الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="c9a78-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="c9a78-125">[![الحقول المتوفرة لجدول الفاتورة](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="c9a78-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="c9a78-126">يجب عدم تحديد الحقول التالية للتدريب:</span><span class="sxs-lookup"><span data-stu-id="c9a78-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="c9a78-127">**حساب الفاتورة** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="c9a78-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="c9a78-128">**مغلق** (الفئة 3) – يتم استخدام هذا الحقل لتصفية فواتير التدريب (مغلق) والتوقع (غير مغلق).</span><span class="sxs-lookup"><span data-stu-id="c9a78-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="c9a78-129">**الاسم** (الفئة 1)</span><span class="sxs-lookup"><span data-stu-id="c9a78-129">**Name** (category 1)</span></span>
- <span data-ttu-id="c9a78-130">**معرف المصدر** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="c9a78-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="c9a78-131">**سجل المصدر** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="c9a78-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="c9a78-132">**جدول المصدر** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="c9a78-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="c9a78-133">جدول عملاء Dataverse</span><span class="sxs-lookup"><span data-stu-id="c9a78-133">Customer Dataverse table</span></span>

<span data-ttu-id="c9a78-134">يبين الرسم التوضيحي التالي الحقول المتوفرة لجدول العملاء.</span><span class="sxs-lookup"><span data-stu-id="c9a78-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="c9a78-135">[![الحقول المتوفرة لجدول العملاء](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="c9a78-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="c9a78-136">يجب عدم تحديد الحقل التالي للتدريب:</span><span class="sxs-lookup"><span data-stu-id="c9a78-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="c9a78-137">**مفتاح فريد للصف** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="c9a78-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="c9a78-138">عوامل التصفية</span><span class="sxs-lookup"><span data-stu-id="c9a78-138">Filters</span></span>

<span data-ttu-id="c9a78-139">لا تدعم عوامل التصفية حاليًا سيناريو توقعات دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="c9a78-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="c9a78-140">لذلك، حدد **تخطي هذه الخطوة**، وتابع إلى صفحة الملخص.</span><span class="sxs-lookup"><span data-stu-id="c9a78-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="c9a78-141">[![وضع التركيز باستخدام عوامل التصفية](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="c9a78-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="c9a78-142">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="c9a78-142">Privacy notice</span></span>
<span data-ttu-id="c9a78-143">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="c9a78-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]