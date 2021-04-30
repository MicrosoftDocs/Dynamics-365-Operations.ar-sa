---
title: مراجع إلى الفواتير الأصلية في الإشعارات الدائنة
description: يوضح هذا الموضوع كيفية إعداد أرقام الفواتير الأصلية وطباعتها في الإشعارات الدائنة المرتبطة.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d7f32c5d3d29be8d1d2742c4017c1719cbd47a8
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897322"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="86d18-103">مراجع إلى الفواتير الأصلية في الإشعارات الدائنة</span><span class="sxs-lookup"><span data-stu-id="86d18-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="86d18-104">في بعض البلدان والمناطق، يكون هناك متطلب قانوني بأن تتضمن الإشعارات الدائنة المطبوعة مراجع إلى لفواتير الأصلية.</span><span class="sxs-lookup"><span data-stu-id="86d18-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="86d18-105">يوضح هذا الموضوع كيفية إعداد أرقام الفواتير الأصلية وطباعتها في الإشعارات الدائنة المرتبطة.</span><span class="sxs-lookup"><span data-stu-id="86d18-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86d18-106">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="86d18-106">Prerequisites</span></span>

- <span data-ttu-id="86d18-107">في مساحة عمل **إدارة الميزات**، قم بتشغيل ميزة **تخطيط فوترة الائتمان لتقارير المبيعات وفاتورة المشروع**.</span><span class="sxs-lookup"><span data-stu-id="86d18-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="86d18-108">لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="86d18-108">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="86d18-109">يجب تكوين التنسيقات القابلة للطباعة للمستندات المطلوبة في إدارة الطباعة.</span><span class="sxs-lookup"><span data-stu-id="86d18-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="86d18-110">تنطبق الوظيفة الموضحة في هذا الموضوع على المستندات التالية:</span><span class="sxs-lookup"><span data-stu-id="86d18-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="86d18-111">**الحسابات المدينة**</span><span class="sxs-lookup"><span data-stu-id="86d18-111">**Accounts receivable**</span></span>

- <span data-ttu-id="86d18-112">إشعار دائن بنص حر</span><span class="sxs-lookup"><span data-stu-id="86d18-112">Free text credit note</span></span>
- <span data-ttu-id="86d18-113">اشعار ائتمان العميل</span><span class="sxs-lookup"><span data-stu-id="86d18-113">Customer credit note</span></span>

<span data-ttu-id="86d18-114">**إدارة المشاريع ومحاسبتها**</span><span class="sxs-lookup"><span data-stu-id="86d18-114">**Project management and accounting**</span></span>

- <span data-ttu-id="86d18-115">إشعار الدائن للمشروع</span><span class="sxs-lookup"><span data-stu-id="86d18-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="86d18-116">تكوين معلمات الحسابات المدينة</span><span class="sxs-lookup"><span data-stu-id="86d18-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="86d18-117">اتبع هذه الخطوات لتعيين المعلمة التي تتحكم في ما إذا كانت ستتم طباعة مراجع إلى الفواتير الأصلية في الإشعارات الدائنة ذات صلة.</span><span class="sxs-lookup"><span data-stu-id="86d18-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="86d18-118">انتقل إلى **الحسابات المدينة** \> **إعداد** \> **معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="86d18-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="86d18-119">في علامة التبويب **تحديثات**، في علامة التبويب السريعة **الفاتورة**، قم بتعيين خيار **تطبيق تخطيط فوترة الائتمان على تقارير المبيعات وفاتورة المشروع** على القمية **نعم**.</span><span class="sxs-lookup"><span data-stu-id="86d18-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![تكوين معلمات الحسابات المدينة](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="86d18-121">تعريف مراجع الفواتير الأصلية</span><span class="sxs-lookup"><span data-stu-id="86d18-121">Define references to original invoices</span></span>

<span data-ttu-id="86d18-122">استخدم الإجراءات التالية لتحديد مراجع للفواتير الأصلية استنادا إلى نوع المستند.</span><span class="sxs-lookup"><span data-stu-id="86d18-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="86d18-123">إشعار دائن بنص حر</span><span class="sxs-lookup"><span data-stu-id="86d18-123">Free text credit note</span></span>

1. <span data-ttu-id="86d18-124">انتقل إلى **الحسابات المدينة** \> **الفواتير** \> **جميع الفواتير ذات نص حر‬**.</span><span class="sxs-lookup"><span data-stu-id="86d18-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="86d18-125">قم بإنشاء إشعار دائن جديد، أو حدد إشعار دائن موجود.</span><span class="sxs-lookup"><span data-stu-id="86d18-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="86d18-126">افتح الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="86d18-126">Open the invoice.</span></span>
4. <span data-ttu-id="86d18-127">في جزء الإجراءات، في علامة التبويب **الفاتورة**، في المجموعة **الوظائف**، حدد **فوترة الائتمان**.</span><span class="sxs-lookup"><span data-stu-id="86d18-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="86d18-128">أدخل المرجع إلى الفاتورة الأصلية، وحدد سبب التصحيح.</span><span class="sxs-lookup"><span data-stu-id="86d18-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![تعريف مرجع لفاتورة نص حر](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="86d18-130">اشعار ائتمان العميل</span><span class="sxs-lookup"><span data-stu-id="86d18-130">Customer credit note</span></span>

1. <span data-ttu-id="86d18-131">انتقل إلى **الحسابات المدينة** \> **الأوامر‬** \> **كافة أوامر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="86d18-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="86d18-132">حدد أمر المبيعات المفوتر الذي يجب تصحيحه وافتحه.</span><span class="sxs-lookup"><span data-stu-id="86d18-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="86d18-133">في جزء الإجراءات، في علامة التبويب **البيع**، في مجموعة **إشعار دائن**، حدد **إشعار دائن**.</span><span class="sxs-lookup"><span data-stu-id="86d18-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="86d18-134">أدخل سبب التصحيح.</span><span class="sxs-lookup"><span data-stu-id="86d18-134">Enter the reason for the correction.</span></span> <span data-ttu-id="86d18-135">يتم إنشاء المرجع إلى الفاتورة الاصلية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="86d18-135">The reference to the original invoice is automatically established.</span></span>

![تعريف المرجع لأمر المبيعات](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="86d18-137">إشعار الدائن للمشروع</span><span class="sxs-lookup"><span data-stu-id="86d18-137">Project credit note</span></span>

1. <span data-ttu-id="86d18-138">انتقل إلى **إدارة المشاريع والمحاسبة** \> **فواتير المشاريع** \> **فواتير المشاريع**.</span><span class="sxs-lookup"><span data-stu-id="86d18-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="86d18-139">حدد فاتورة المشروع التي يجب تصحيحها وافتحها.</span><span class="sxs-lookup"><span data-stu-id="86d18-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="86d18-140">في جزء الإجراءات، في علامة التبويب **فاتورة المشروع**، في المجموعة **الوظائف**، حدد **تحديد لإشعار دائن**.</span><span class="sxs-lookup"><span data-stu-id="86d18-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="86d18-141">حدد **فوترة الائتمان**.</span><span class="sxs-lookup"><span data-stu-id="86d18-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="86d18-142">أدخل سبب التصحيح.</span><span class="sxs-lookup"><span data-stu-id="86d18-142">Enter the reason for the correction.</span></span> <span data-ttu-id="86d18-143">يتم إنشاء المرجع إلى الفاتورة الاصلية تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="86d18-143">The reference to the original invoice is automatically established.</span></span>

![تعريف مرجع لفاتورة مشروع](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="86d18-145">طباعة إشعارات الدائن</span><span class="sxs-lookup"><span data-stu-id="86d18-145">Printing credit notes</span></span>

<span data-ttu-id="86d18-146">عند طباعة إشعارات دائنة نص حر وإشعارات دائمة للعميل وللمشروع، فإنها ستشتمل على مرجع إلى الفاتورة الأصلية وسبب التصحيح.</span><span class="sxs-lookup"><span data-stu-id="86d18-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![اشعار دائن مطبوع](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="86d18-148">تأكد من تكوين التنسيقات القابلة للطباعة الخاصة بالمستندات بشكل صحيح، على افتراض أنه ستتم طباعة مراجع الفواتير الأصلية.</span><span class="sxs-lookup"><span data-stu-id="86d18-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]