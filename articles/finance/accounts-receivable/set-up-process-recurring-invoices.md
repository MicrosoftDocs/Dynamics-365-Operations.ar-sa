---
title: إعداد ومعالجة الفواتير المتكررة
description: توضح هذه المقالة كيفية إعداد ومعالجة الفواتير المتكررة. يمكنك استخدام الفواتير المتكررة إذا توجب عليك فوترة العملاء بنفس المبلغ على أساس منتظم.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834dc64ce531fb614bc7836e0def16f27ecf5e18
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188628"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="afad5-104">إعداد ومعالجة الفواتير المتكررة</span><span class="sxs-lookup"><span data-stu-id="afad5-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afad5-105">توضح هذه المقالة كيفية إعداد ومعالجة الفواتير المتكررة.</span><span class="sxs-lookup"><span data-stu-id="afad5-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="afad5-106">يمكنك استخدام الفواتير المتكررة إذا توجب عليك فوترة العملاء بنفس المبلغ على أساس منتظم.</span><span class="sxs-lookup"><span data-stu-id="afad5-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

## <a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="afad5-107">إنشاء قالب فواتير النص الحر المتكررة</span><span class="sxs-lookup"><span data-stu-id="afad5-107">Create a recurring free text invoice template</span></span>

<span data-ttu-id="afad5-108">لفوترة العملاء لنفس الخدمات بشكل منتظم، يجب تحديد قالب فاتورة نص حر يمكن إعادة استخدامه لإنشاء الفواتير.</span><span class="sxs-lookup"><span data-stu-id="afad5-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="afad5-109">يحتوي هذا القالب على المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="afad5-109">This template contains the following information:</span></span>

-   <span data-ttu-id="afad5-110">معلومات الرأس، مثل مجموعات الضرائب، ومدة الدفع، وطريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="afad5-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="afad5-111">معلومات البند، مثل وصف الخدمة، وحسابات الإيرادات، وسعر الوحدة، ومبلغ الفاتورة</span><span class="sxs-lookup"><span data-stu-id="afad5-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="afad5-112">مصاريف الشحن أو المعالجة</span><span class="sxs-lookup"><span data-stu-id="afad5-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="afad5-113">التوزيعات المحاسبية جنبًا إلى جنب مع معلومات البعد المالي، مثل مراكز التكلفة ووحدات الأعمال</span><span class="sxs-lookup"><span data-stu-id="afad5-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="afad5-114">في الواقع، تقوم بإنشاء فاتورة بأكملها وتحفظها كقالب.</span><span class="sxs-lookup"><span data-stu-id="afad5-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="afad5-115">ويمكنك إعداد قوالب استخدام صفحة **الفواتير المتكررة**.</span><span class="sxs-lookup"><span data-stu-id="afad5-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="afad5-116">تعيين قالب فاتورة ذات نص حر إلى عميل وإدخال تفاصيل التكرار</span><span class="sxs-lookup"><span data-stu-id="afad5-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="afad5-117">بعد إنشاء القالب، يجب عليك تعيين القالب للعملاء الذيت تريد فوترتهم.</span><span class="sxs-lookup"><span data-stu-id="afad5-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="afad5-118">بالإضافة إلى ذلك، يجب عليك تحديد متى وكم مرة سيتم استخدام الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="afad5-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="afad5-119">يمكنك تعيين القوالب إلى علامة التبويب **الفاتورة** في صفحة **العملاء**.</span><span class="sxs-lookup"><span data-stu-id="afad5-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="afad5-120">أضف القالب إلى القائمة، وتحديث المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="afad5-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="afad5-121">تاريخ البدء، وبشكل اختياري، تاريخ الانتهاء للفوترة المتكررة</span><span class="sxs-lookup"><span data-stu-id="afad5-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="afad5-122">معدل تكرار الفوترة المتكررة (على سبيل المثال، يوميًا أو مرة واحدة في الشهر)</span><span class="sxs-lookup"><span data-stu-id="afad5-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="afad5-123">الحد الأقصى لمبلغ الفوترة (إذا كانت هذه المعلومات مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="afad5-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="afad5-124">يمكن أن يكون لدى عميل قوالب متعددة ذات تكرارات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="afad5-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="afad5-125">إنشاء الفواتير المتكررة</span><span class="sxs-lookup"><span data-stu-id="afad5-125">Generate the recurring invoices</span></span>
<span data-ttu-id="afad5-126">في صفحة **الفواتير المتكررة**، هناك مهمة تعالج قوالب الفواتير المتكررة.</span><span class="sxs-lookup"><span data-stu-id="afad5-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="afad5-127">ويمكنك تحديد تاريخ الفاتورة والقالب لإنشاء الفواتير منه.</span><span class="sxs-lookup"><span data-stu-id="afad5-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="afad5-128">وسيتم إنشاء الفواتير وتعيين رقم معرف تكرار واحد لكل مجموعة من الفواتير تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="afad5-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

## <a name="post-recurring-free-text-invoices"></a><span data-ttu-id="afad5-129">ترحيل فواتير النص الحر المتكررة</span><span class="sxs-lookup"><span data-stu-id="afad5-129">Post recurring free text invoices</span></span>

<span data-ttu-id="afad5-130">بعد إنشاء الفواتير المتكررة، تظهر معرفات تكرار الفاتورة في مهمة ترحيل في صفحة **الفواتير المتكررة**.</span><span class="sxs-lookup"><span data-stu-id="afad5-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="afad5-131">يمكنك عرض كافة الفواتير للحصول على معرف تكرار عن طريق النقر فوق الارتباط.</span><span class="sxs-lookup"><span data-stu-id="afad5-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="afad5-132">وأثناء مراجعة الفواتير لمعرفة معرف التكرار، يمكنك حذف الفواتير الفردية.</span><span class="sxs-lookup"><span data-stu-id="afad5-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="afad5-133">وستتم إعادة تعيين إعدادات التكرار الخاصة بالعميل لهذا القالب، بحيث يمكن إعادة إنشائه لاحقاً.</span><span class="sxs-lookup"><span data-stu-id="afad5-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="afad5-134">ويمكنك ترحيل واحد أو العديد من أو كافة الفواتير لمعرف التكرار.</span><span class="sxs-lookup"><span data-stu-id="afad5-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="afad5-135">وإذا تم تمكين مهام سير العمل، يجب عليك النقر فوق **إرسال** قبل التمكن من ترحيل الفواتير.</span><span class="sxs-lookup"><span data-stu-id="afad5-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

## <a name="print-recurring-free-text-invoices"></a><span data-ttu-id="afad5-136">طباعة فواتير النص الحر المتكررة</span><span class="sxs-lookup"><span data-stu-id="afad5-136">Print recurring free text invoices</span></span>

<span data-ttu-id="afad5-137">بعد ترحيل الفواتير المتكررة، يمكنك طباعة الفواتير من صفحة قائمة فواتير النص الحر.</span><span class="sxs-lookup"><span data-stu-id="afad5-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="afad5-138">يمكنك طباعة الفواتير التي تم تحديدها، أو يمكنك تحديد مجموعة من الفواتير للطباعة.</span><span class="sxs-lookup"><span data-stu-id="afad5-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]