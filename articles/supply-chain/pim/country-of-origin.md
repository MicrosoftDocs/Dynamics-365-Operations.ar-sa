---
title: بلد المنشأ
description: تصدر العديد من المؤسسات شهادات إلى الموردين الخاصين بهم لضمان أن المنتجات تفي بمعايير الشهادة المحددة. وغالبًا ما تعتمد هذه الشهادات على بلد المنشأ. يوفر هذا الموضوع معلومات حول الميزة "بلد المنشأ"، والتي تتيح لك ربط منتج ببلد المنشأ الخاص به وتعقب شهادات المنتج الخاصة به.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895538"
---
# <a name="country-of-origin"></a><span data-ttu-id="caade-105">بلد المنشأ</span><span class="sxs-lookup"><span data-stu-id="caade-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="caade-106">تصدر العديد من المؤسسات شهادات إلى الموردين الخاصين بهم لضمان أن المنتجات تفي بمعايير الشهادة المحددة.</span><span class="sxs-lookup"><span data-stu-id="caade-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="caade-107">وغالبًا ما تعتمد هذه الشهادات على بلد المنشأ.</span><span class="sxs-lookup"><span data-stu-id="caade-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="caade-108">تتيح لك ميزة "بلد المنشأ" ربط منتج ببلد المنشأ الخاص به وتعقب شهادات المنتج الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="caade-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="caade-109">تشغيل ميزة بلد المنشأ</span><span class="sxs-lookup"><span data-stu-id="caade-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="caade-110">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="caade-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="caade-111">بإمكان المسؤولين استخدام إعدادات [دارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها.</span><span class="sxs-lookup"><span data-stu-id="caade-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="caade-112">في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="caade-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="caade-113">**الوحدة النمطية** *إدارة معلومات المنتج*</span><span class="sxs-lookup"><span data-stu-id="caade-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="caade-114">**اسم الميزة:** *ميزة إدارة بلد المنشأ*</span><span class="sxs-lookup"><span data-stu-id="caade-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="caade-115">تكوين البلدان المصدر والوجهة</span><span class="sxs-lookup"><span data-stu-id="caade-115">Configure source and destination countries</span></span>

<span data-ttu-id="caade-116">قبل إصدار شهادة لمنتج ما، يجب ربط المنتج بالبلد الوجهة الخاصة به وبلده الأصلي.</span><span class="sxs-lookup"><span data-stu-id="caade-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="caade-117">الانتقال إلى **إدارة معلومات المنتج \>إعداد \>توافق المنتجات \> بلد المنشأ \> قواعد بلد المنشأ**.</span><span class="sxs-lookup"><span data-stu-id="caade-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="caade-118">حدد إعداد بلد موجود لتحريره، أو حدد **جديد** في جزء الإجراءات لإنشاء إعداد بلد جديد.</span><span class="sxs-lookup"><span data-stu-id="caade-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="caade-119">عيِّن القيم التالية للبلد المحدد أو البلد الجديد.</span><span class="sxs-lookup"><span data-stu-id="caade-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="caade-120">الحقل</span><span class="sxs-lookup"><span data-stu-id="caade-120">Field</span></span> | <span data-ttu-id="caade-121">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="caade-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="caade-122">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="caade-122">Item number</span></span> | <span data-ttu-id="caade-123">أدخل عدد أصناف المنتج.</span><span class="sxs-lookup"><span data-stu-id="caade-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="caade-124">بلد الوجهة</span><span class="sxs-lookup"><span data-stu-id="caade-124">Destination country</span></span> | <span data-ttu-id="caade-125">حدد البلد الذي تقوم بإرسال المنتج إليه.</span><span class="sxs-lookup"><span data-stu-id="caade-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="caade-126">بلد المنشأ</span><span class="sxs-lookup"><span data-stu-id="caade-126">Origin country</span></span> | <span data-ttu-id="caade-127">حدد البلد الذي تقوم بإرسال المنتج منه.</span><span class="sxs-lookup"><span data-stu-id="caade-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="caade-128">والغرض من هذا الإعداد هو مساعدتك في إنشاء تقرير شجره المواد (BOM) حيث يمكنك تضمين البلد الخاص بالأصل لكل جزء من الأجزاء التي يتم تحديد المصدر والوجهة لها.</span><span class="sxs-lookup"><span data-stu-id="caade-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="caade-129">يساعدك هذا التقرير في الحصول على صوره شاملة للمكان الذي تأتي إليه الأجزاء والمكان التي سيتم نقلها إليه.</span><span class="sxs-lookup"><span data-stu-id="caade-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="caade-130">تتبع شهادات الموردين</span><span class="sxs-lookup"><span data-stu-id="caade-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="caade-131">يمكنك استخدام الصفحة **شهادات الموردين للبلد المنشأ** لتعقب الشهادات التي تصدرها إلى الموردين.</span><span class="sxs-lookup"><span data-stu-id="caade-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="caade-132">يجب تحديد مستندات الشهادة التي تقوم بإصدارها وكيف ستقوم بالإبلاغ عنها للعملاء.</span><span class="sxs-lookup"><span data-stu-id="caade-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="caade-133">تساعدك هذه الميزة في متابعة تعقب الشهادات.</span><span class="sxs-lookup"><span data-stu-id="caade-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="caade-134">كما تتيح لك إمكانية اختيار ما إذا كانت تظهر أرقام الشهادات ذات الصلة في الفواتير وكشوف التعبئة و/أو تأكيدات الأوامر.</span><span class="sxs-lookup"><span data-stu-id="caade-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="caade-135">لإعداد معلومات الشهادة‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="caade-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="caade-136">الانتقال إلى **إدارة معلومات المنتج \>إعداد \>توافق المنتجات \> بلد المنشأ \> شهادات الموردين لبلد المنشأ**.</span><span class="sxs-lookup"><span data-stu-id="caade-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="caade-137">حدد إعداد شهادة موجودة لتحريره، أو حدد **جديد** في جزء الإجراءات لإنشاء شهادة جديدة.</span><span class="sxs-lookup"><span data-stu-id="caade-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="caade-138">عيِّن الإعدادات التالية للشهادة المحددة أو الجديدة.</span><span class="sxs-lookup"><span data-stu-id="caade-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="caade-139">الحقل</span><span class="sxs-lookup"><span data-stu-id="caade-139">Field</span></span> | <span data-ttu-id="caade-140">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="caade-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="caade-141">حساب المورد</span><span class="sxs-lookup"><span data-stu-id="caade-141">Vendor account</span></span> | <span data-ttu-id="caade-142">حدد المورد الذي قمت بإصدار الشهادة له.</span><span class="sxs-lookup"><span data-stu-id="caade-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="caade-143">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="caade-143">Item number</span></span> | <span data-ttu-id="caade-144">حدد البند الذي قمت بإصدار الشهادة له.</span><span class="sxs-lookup"><span data-stu-id="caade-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="caade-145">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="caade-145">Country/region</span></span> | <span data-ttu-id="caade-146">البلد أو المنطقة الوجهة التي يجب استخدام هذه الشهادة فيها.</span><span class="sxs-lookup"><span data-stu-id="caade-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="caade-147">رقم الشهادة</span><span class="sxs-lookup"><span data-stu-id="caade-147">Certificate number</span></span> | <span data-ttu-id="caade-148">أدخل رقم تعريف الشهادة الذي قمت بإصداره.</span><span class="sxs-lookup"><span data-stu-id="caade-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="caade-149">ساري المفعول</span><span class="sxs-lookup"><span data-stu-id="caade-149">Effective</span></span> | <span data-ttu-id="caade-150">حدد التاريخ الأول لصلاحية الشهادة الحالية.</span><span class="sxs-lookup"><span data-stu-id="caade-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="caade-151">انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="caade-151">Expiration</span></span> | <span data-ttu-id="caade-152">حدد التاريخ الأخير لصلاحية الشهادة الحالية.</span><span class="sxs-lookup"><span data-stu-id="caade-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="caade-153">الطباعة في فاتورة</span><span class="sxs-lookup"><span data-stu-id="caade-153">Print on invoice</span></span> | <span data-ttu-id="caade-154">حدد خانة الاختيار هذه لطباعة رقم الشهادة في الفواتير الموجهة إلى البلد المحدد أثناء نطاق التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="caade-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="caade-155">الطباعة في إيصال تعبئة</span><span class="sxs-lookup"><span data-stu-id="caade-155">Print on packing slip</span></span> | <span data-ttu-id="caade-156">حدد خانة الاختيار هذه لطباعة رقم الشهادة في إيصالات التعبئة الموجهة إلى البلد المحدد أثناء نطاق التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="caade-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="caade-157">الطباعة في أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="caade-157">Print on sales order</span></span> | <span data-ttu-id="caade-158">حدد خانة الاختيار هذه لطباعة رقم الشهادة في أوامر المبيعات الموجهة إلى البلد المحدد أثناء نطاق التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="caade-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="caade-159">تضمين بلد المنشأ في تقارير قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="caade-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="caade-160">عند إنشاء تقرير شجرة مواد، يمكنك تضمين بلد المنشأ لكل جزء من الأجزاء التي قمت بتحديدها وبلدان الوجهة والخاصة بها في الصفحة **قواعد بلد المنشأ**.</span><span class="sxs-lookup"><span data-stu-id="caade-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="caade-161">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="caade-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="caade-162">حدد منتجًا أو قم بإنشائه لفتح صفحة **تفاصيل المنتج الصادر** له.</span><span class="sxs-lookup"><span data-stu-id="caade-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="caade-163">في جزء الإجراءات، في علامة تبويب **المهندس** في مجموعة **قائمة مكونات الصنف‏‎‬**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="caade-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="caade-164">في صفحة القائمة التي تظهر، في جزء الإجراءات، حدد **قائمة مكونات الصنف \> طباعة**.</span><span class="sxs-lookup"><span data-stu-id="caade-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="caade-165">في مربع الحوار **بنود قائمة مكونات الصنف**، قم بتعيين حقل **البلد الوجهة** إلى البلد الوجهة التي ترغب في عرضها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="caade-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="caade-166">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="caade-166">Select **OK**.</span></span>

<span data-ttu-id="caade-167">ويتم إنشاء تقرير يعرض معلومات حول بلد المنشأ لكل جزء ويتم إظهاره.</span><span class="sxs-lookup"><span data-stu-id="caade-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="caade-168">فيما يلي مثال التقرير.</span><span class="sxs-lookup"><span data-stu-id="caade-168">Here is an example of the report.</span></span>

<span data-ttu-id="caade-169">![تقرير بلد المنشأ](media/country-of-origin-report.png "تقرير بلد المنشأ")</span><span class="sxs-lookup"><span data-stu-id="caade-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
