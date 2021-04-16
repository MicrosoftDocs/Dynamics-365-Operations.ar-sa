---
title: ترقيم المستندات والإيصالات حسب التسلسل الزمني
description: يوضح هذا الموضوع كيفية إعداد الأرقام الزمنية واستخدامها للمستندات القابلة للتطبيق والإيصالات ذات الصلة.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838851"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="afc0a-103">ترقيم المستندات والإيصالات حسب التسلسل الزمني</span><span class="sxs-lookup"><span data-stu-id="afc0a-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="afc0a-104">في بعض البلدان، هناك متطلب قانوني لترقيم المستندات والإيصالات المرتبطة بترتيب زمني.</span><span class="sxs-lookup"><span data-stu-id="afc0a-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="afc0a-105">يجب أن تكون التسلسل الزمني مدعومًا بالفترات.</span><span class="sxs-lookup"><span data-stu-id="afc0a-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="afc0a-106">يجب أن تكون كافة الأرقام التي تنتمي إلى فترات سابقة أقل من الأرقام التي تنتمي إلى فترات لاحقة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="afc0a-107">لتلبية هذا المتطلب، تم تطبيق وظيفة الترقيم الزمني.</span><span class="sxs-lookup"><span data-stu-id="afc0a-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="afc0a-108">يوضح هذا الموضوع كيفية تكوين الأرقام الزمنية واستخدامها للمستندات القابلة للتطبيق والإيصالات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="afc0a-109">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="afc0a-109">Prerequisites</span></span>

<span data-ttu-id="afc0a-110">في مساحة عمل إدارة الميزات، شغَّل ميزة **الترقيم الزمني**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="afc0a-111">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="afc0a-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="afc0a-112">تكوين الترقيم الزمني</span><span class="sxs-lookup"><span data-stu-id="afc0a-112">Configure chronological numbering</span></span>

<span data-ttu-id="afc0a-113">يؤثر الترقيم الزمني على المستندات التالية.</span><span class="sxs-lookup"><span data-stu-id="afc0a-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="afc0a-114">**الحسابات المدينة**</span><span class="sxs-lookup"><span data-stu-id="afc0a-114">**Accounts receivable**</span></span>
- <span data-ttu-id="afc0a-115">فاتورة العميل</span><span class="sxs-lookup"><span data-stu-id="afc0a-115">Customer invoice</span></span>
- <span data-ttu-id="afc0a-116">قيد فاتورة العميل</span><span class="sxs-lookup"><span data-stu-id="afc0a-116">Customer invoice voucher</span></span>
- <span data-ttu-id="afc0a-117">إشعار دائن المبيعات</span><span class="sxs-lookup"><span data-stu-id="afc0a-117">Sales credit note</span></span>
- <span data-ttu-id="afc0a-118">قيد إشعار خصم المبيعات</span><span class="sxs-lookup"><span data-stu-id="afc0a-118">Sales credit note voucher</span></span>
- <span data-ttu-id="afc0a-119">فاتورة ذات نص حر</span><span class="sxs-lookup"><span data-stu-id="afc0a-119">Free text invoice</span></span>
- <span data-ttu-id="afc0a-120">قيد فاتورة بنص حر</span><span class="sxs-lookup"><span data-stu-id="afc0a-120">Free text invoice voucher</span></span>
- <span data-ttu-id="afc0a-121">إشعار دائن بنص حر</span><span class="sxs-lookup"><span data-stu-id="afc0a-121">Free text credit note</span></span>
- <span data-ttu-id="afc0a-122">إيصال إشعار دائن بنص حر</span><span class="sxs-lookup"><span data-stu-id="afc0a-122">Free text credit note voucher</span></span>
- <span data-ttu-id="afc0a-123">إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="afc0a-123">Packing slip</span></span>
- <span data-ttu-id="afc0a-124">رقم قيد إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="afc0a-124">Packing slip voucher</span></span>
- <span data-ttu-id="afc0a-125">إيصال تصحيح إيصال التعبئة</span><span class="sxs-lookup"><span data-stu-id="afc0a-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="afc0a-126">إيصال إشعار الفائدة</span><span class="sxs-lookup"><span data-stu-id="afc0a-126">Interest note voucher</span></span>
- <span data-ttu-id="afc0a-127">إيصال خطاب التحصيل</span><span class="sxs-lookup"><span data-stu-id="afc0a-127">Collection letter voucher</span></span>

<span data-ttu-id="afc0a-128">**الحسابات الدائنة**</span><span class="sxs-lookup"><span data-stu-id="afc0a-128">**Accounts payable**</span></span>
- <span data-ttu-id="afc0a-129">قيد الفاتورة</span><span class="sxs-lookup"><span data-stu-id="afc0a-129">Invoice voucher</span></span>
- <span data-ttu-id="afc0a-130">إيصال إشعار الدائن</span><span class="sxs-lookup"><span data-stu-id="afc0a-130">Credit note voucher</span></span>
- <span data-ttu-id="afc0a-131">إيصال استلام المنتجات</span><span class="sxs-lookup"><span data-stu-id="afc0a-131">Product receipt voucher</span></span>

<span data-ttu-id="afc0a-132">**إدارة المشروع**</span><span class="sxs-lookup"><span data-stu-id="afc0a-132">**Project management**</span></span>
- <span data-ttu-id="afc0a-133">الفاتورة</span><span class="sxs-lookup"><span data-stu-id="afc0a-133">Invoice</span></span>
- <span data-ttu-id="afc0a-134">قيد الفاتورة</span><span class="sxs-lookup"><span data-stu-id="afc0a-134">Invoice voucher</span></span>
- <span data-ttu-id="afc0a-135">إشعار دائن</span><span class="sxs-lookup"><span data-stu-id="afc0a-135">Credit note</span></span>
- <span data-ttu-id="afc0a-136">إيصال إشعار الدائن</span><span class="sxs-lookup"><span data-stu-id="afc0a-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="afc0a-137">تحديد التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="afc0a-137">Define number sequences</span></span>

<span data-ttu-id="afc0a-138">لتحديد التسلسلات الرقمية، انتقل إلى **إدارة المؤسسات** > **التسلسلات الرقمية** > **التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="afc0a-139">يمكنك تحديد العديد من التسلسلات الرقمية كما هو مطلوب لتغطية الفترات المتأثرة بالمستندات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="afc0a-140">حدد شركة لكل تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="afc0a-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="afc0a-141">يجب تحديد أجزاء التسلسلات الرقمية لكي توفر ترتيبًا زمنيًا للفترات.</span><span class="sxs-lookup"><span data-stu-id="afc0a-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="afc0a-142">على سبيل المثال، يمكن أن تحتوي أسماء الأجزاء على بادئة خاصة تُعرِّف فترة معينة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![إعداد التسلسل الرقمي](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="afc0a-144">تكوين مجموعات التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="afc0a-144">Configure number sequence groups</span></span>

<span data-ttu-id="afc0a-145">لتكوين مجموعات تسلسلات رقمية، انتقل إلى **الحسابات المدينة** > **الإعداد** > **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="afc0a-146">في علامة تبويب **التسلسلات الرقمية**، حدد أكبر عدد مطلوب من مجموعات التسلسلات الرقمية لتغطية الفترات المتأثرة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="afc0a-147">بالنسبة لكل مجموعة، في قسم **المرجع**، حدد أحد مراجع المستندات المدعومة، وفي حقل **كود التسلسل الرقمي**، أشر إلى التسلسل الرقمي الذي تم إنشاؤه مسبقا للفترة ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![إعداد مجموعة التسلسلات الرقمية](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="afc0a-149">بطريقة مماثلة، قم بتكوين مجموعات تسلسل الأرقام في وحدات **الحسابات الدائنة** و **إدارة المشاريع والمحاسبة**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="afc0a-150">تكوين الترتيب الزمني لمجموعات التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="afc0a-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="afc0a-151">لتكوين الترتيب الزمني لمجموعات التسلسلات الرقمية، انتقل إلى **إدارة المؤسسات** > **تسلسلات أرقام** > **مجموعات تسلسلات أرقام المرتبة زمنيًا**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="afc0a-152">حدد شروط التطبيق لمجموعات التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="afc0a-152">Define the applicability conditions for number sequence groups.</span></span>

![إعداد الأرقام الزمنية](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="afc0a-154">الحقل</span><span class="sxs-lookup"><span data-stu-id="afc0a-154">Field</span></span>            | <span data-ttu-id="afc0a-155">الوصف</span><span class="sxs-lookup"><span data-stu-id="afc0a-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afc0a-156">السريان</span><span class="sxs-lookup"><span data-stu-id="afc0a-156">Effective</span></span>  | <span data-ttu-id="afc0a-157">تاريخ بدء تطبيق مجموعة التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="afc0a-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="afc0a-158">انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="afc0a-158">Expiration</span></span>      | <span data-ttu-id="afc0a-159">تاريخ انتهاء تطبيق مجموعة التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="afc0a-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="afc0a-160">إذا لم يتم تطبيق تاريخ انتهاء، فحدد **أبدا**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="afc0a-161">مجموعة التسلسلات الرقمية</span><span class="sxs-lookup"><span data-stu-id="afc0a-161">Number sequence group</span></span> | <span data-ttu-id="afc0a-162">مجموعة التسلسلات الرقمية التي سيتم استخدامها لإنشاء أرقام المستندات أثناء الفترة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="afc0a-163">مجموعة التسلسلات الرقمية الأصلية</span><span class="sxs-lookup"><span data-stu-id="afc0a-163">Original number sequence group</span></span> | <span data-ttu-id="afc0a-164">يتم استخدام كود مجموعة التسلسلات الرقمية هذا للتصفية الإضافية للحالات حينما تتضمن المستندات بالفعل مجموعة تسلسل رقمي *دائمة* معينة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="afc0a-165">تعتبر القيمة الفارغة قيمة خاصة.</span><span class="sxs-lookup"><span data-stu-id="afc0a-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="afc0a-166">إذا كنت ترغب في تجاهل إحدى المجموعات الأولية المعينة، فاستخدم خيار **الافتراضي** لهذا الإعداد.</span><span class="sxs-lookup"><span data-stu-id="afc0a-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="afc0a-167">افتراضية</span><span class="sxs-lookup"><span data-stu-id="afc0a-167">Default</span></span> | <span data-ttu-id="afc0a-168">وفي حالة تشغيله، يتجاهل النظام مجموعة التسلسل الرقمي للمستند المعين الأولي ويستخدم فقط تواريخ بدء وانتهاء الفترات لتحليل قابلية التطبيق.</span><span class="sxs-lookup"><span data-stu-id="afc0a-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="afc0a-169">في حالة إيقاف التشغيل، يستخدم النظام **الفعالية** + **انتهاء الصلاحية** + **مجموعة التسلسلات الرقمية** للتحديد.</span><span class="sxs-lookup"><span data-stu-id="afc0a-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="afc0a-170">ترحيل المستند</span><span class="sxs-lookup"><span data-stu-id="afc0a-170">Document posting</span></span>
<span data-ttu-id="afc0a-171">عندما تقوم بترحيل مستند، يتم تعيين مجموعة التسلسلات الرقمية المناسبة إلى المستند، استنادا إلى تاريخ ترحيل المستند، ثم تُستخدم لإنشاء رقم مستند استنادا إلى التسلسل الرقمي الذي تم اكتشافه.</span><span class="sxs-lookup"><span data-stu-id="afc0a-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="afc0a-172">يوفر النظام رسالة تتعلق بتعيين مجموعة التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="afc0a-172">The system provides a message regarding the number sequence group assignment.</span></span>

![رقم المستند](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="afc0a-174">بالنسبة لبعض البلدان، يوجد منطق معين تم تنفيذه بالفعل لترقيم المستندات.</span><span class="sxs-lookup"><span data-stu-id="afc0a-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="afc0a-175">في هذه الحالة، سيتجاوز المنطق الخاص بالبلد ميزة **الترقيم الزمني**.</span><span class="sxs-lookup"><span data-stu-id="afc0a-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
