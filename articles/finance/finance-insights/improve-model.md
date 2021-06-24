---
title: تحسين نموذج التنبؤ (معاينة)
description: يوضح هذا الموضوع الميزات التي يمكنك استخدامها لتحسين أداء نماذج التنبؤ.
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186632"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="e153b-103">تحسين نموذج التنبؤ (معاينة)</span><span class="sxs-lookup"><span data-stu-id="e153b-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e153b-104">يوضح هذا الموضوع الميزات التي يمكنك استخدامها لتحسين أداء نماذج التنبؤ.</span><span class="sxs-lookup"><span data-stu-id="e153b-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="e153b-105">ستبدأ في تحسين النموذج الخاص بك في مساحة العمل **توقعات دفع العميل** في Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e153b-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="e153b-106">عندئذ يتم إكمال خطوات التحسين في AI Builder.</span><span class="sxs-lookup"><span data-stu-id="e153b-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="e153b-107">تحديد النتائج التاريخية</span><span class="sxs-lookup"><span data-stu-id="e153b-107">Select historical outcomes</span></span>

<span data-ttu-id="e153b-108">قم أولاً بتحديد واحدًا أو أكثر من النتائج الثلاثة المحتملة للفواتير: **في الوقت المحدد** و **متأخر** و **متأخر جدًا**.</span><span class="sxs-lookup"><span data-stu-id="e153b-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="e153b-109">يجب تحديد كافة النتائج الثلاثة.</span><span class="sxs-lookup"><span data-stu-id="e153b-109">All three outcomes should be selected.</span></span> <span data-ttu-id="e153b-110">إذا قمت بإلغاء تحديد أي من النتائج، فإنه سيتم تصفية الفواتير خارج عملية التدريب وسيتم تقليل دقة التوقع.</span><span class="sxs-lookup"><span data-stu-id="e153b-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="e153b-111">[![تأكيد النتائج](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="e153b-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="e153b-112">إذا كانت مؤسستك تتطلب اثنين من النتائج فقط، فقم بتغيير الحدود **متأخر** و **متأخر جدًا** إلى 0 (صفر) يومًا.</span><span class="sxs-lookup"><span data-stu-id="e153b-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="e153b-113">بهذه الطريقة، يمكنك بشكل فعال طي التوقع إلى الحالة الثنائية **في الوقت المحدد** أو **متأخر**.</span><span class="sxs-lookup"><span data-stu-id="e153b-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="e153b-114">تحديد الحقول</span><span class="sxs-lookup"><span data-stu-id="e153b-114">Select fields</span></span>

<span data-ttu-id="e153b-115">عند تحديد الحقول التي سيتم تضمينها في النموذج، يجب الانتباه إلى أن القائمة تتضمن كافة الحقول المتوفرة في جدول Microsoft Dataverse الذي تم تعيينه إلى البيانات في Azure data lake.</span><span class="sxs-lookup"><span data-stu-id="e153b-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="e153b-116">يجب **عدم** تحديد بعض هذه الحقول.</span><span class="sxs-lookup"><span data-stu-id="e153b-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="e153b-117">تقع الحقول التي يجب عدم تحديدها ضمن واحدة من الفئات الثلاثة التالية:</span><span class="sxs-lookup"><span data-stu-id="e153b-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="e153b-118">الحقل مطلوب للجدول Dataverse، ولكن لا توجد بيانات احتياطية له في data lake.</span><span class="sxs-lookup"><span data-stu-id="e153b-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="e153b-119">يعتبر هذا الحقل معرف وبالتالي لا يكون له معنى لميزة "التعلم الآلي".</span><span class="sxs-lookup"><span data-stu-id="e153b-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="e153b-120">يمثل الحقل المعلومات التي لن تكون متوفرة أثناء التوقع.</span><span class="sxs-lookup"><span data-stu-id="e153b-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="e153b-121">توضح الأقسام التالية الحقول المتاحة لكيانات الفاتورة والعميل، وتسرد الحقول التي يجب **عدم** تحديدها للتدريب.</span><span class="sxs-lookup"><span data-stu-id="e153b-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="e153b-122">تشير الفئة المحددة لكل من هذه الحقول إلى الفئات الموجودة في القائمة السابقة.</span><span class="sxs-lookup"><span data-stu-id="e153b-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="e153b-123">جدول فاتورة Dataverse</span><span class="sxs-lookup"><span data-stu-id="e153b-123">Invoice Dataverse table</span></span>

<span data-ttu-id="e153b-124">يبين الرسم التوضيحي التالي الحقول المتوفرة لجدول الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="e153b-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="e153b-125">[![الحقول المتوفرة لجدول الفاتورة](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="e153b-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="e153b-126">يجب عدم تحديد الحقول التالية للتدريب:</span><span class="sxs-lookup"><span data-stu-id="e153b-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="e153b-127">**حساب الفاتورة** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="e153b-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="e153b-128">**مغلق** (الفئة 3) – يتم استخدام هذا الحقل لتصفية فواتير التدريب (مغلق) والتوقع (غير مغلق).</span><span class="sxs-lookup"><span data-stu-id="e153b-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="e153b-129">**الاسم** (الفئة 1)</span><span class="sxs-lookup"><span data-stu-id="e153b-129">**Name** (category 1)</span></span>
- <span data-ttu-id="e153b-130">**معرف المصدر** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="e153b-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="e153b-131">**سجل المصدر** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="e153b-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="e153b-132">**جدول المصدر** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="e153b-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="e153b-133">جدول عملاء Dataverse</span><span class="sxs-lookup"><span data-stu-id="e153b-133">Customer Dataverse table</span></span>

<span data-ttu-id="e153b-134">يبين الرسم التوضيحي التالي الحقول المتوفرة لجدول العملاء.</span><span class="sxs-lookup"><span data-stu-id="e153b-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="e153b-135">[![الحقول المتوفرة لجدول العملاء](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="e153b-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="e153b-136">يجب عدم تحديد الحقل التالي للتدريب:</span><span class="sxs-lookup"><span data-stu-id="e153b-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="e153b-137">**مفتاح فريد للصف** (الفئة 2)</span><span class="sxs-lookup"><span data-stu-id="e153b-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="e153b-138">عوامل التصفية</span><span class="sxs-lookup"><span data-stu-id="e153b-138">Filters</span></span>

<span data-ttu-id="e153b-139">لا تدعم عوامل التصفية حاليًا سيناريو توقعات دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="e153b-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="e153b-140">لذلك، حدد **تخطي هذه الخطوة**، وتابع إلى صفحة الملخص.</span><span class="sxs-lookup"><span data-stu-id="e153b-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="e153b-141">[![وضع التركيز باستخدام عوامل التصفية](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="e153b-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
