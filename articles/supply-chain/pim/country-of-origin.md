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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596198"
---
# <a name="country-of-origin"></a><span data-ttu-id="c78d1-105">بلد المنشأ</span><span class="sxs-lookup"><span data-stu-id="c78d1-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c78d1-106">تصدر العديد من المؤسسات شهادات إلى الموردين الخاصين بهم لضمان أن المنتجات تفي بمعايير الشهادة المحددة.</span><span class="sxs-lookup"><span data-stu-id="c78d1-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="c78d1-107">وغالبًا ما تعتمد هذه الشهادات على بلد المنشأ.</span><span class="sxs-lookup"><span data-stu-id="c78d1-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="c78d1-108">تتيح لك ميزة "بلد المنشأ" ربط منتج ببلد المنشأ الخاص به وتعقب شهادات المنتج الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="c78d1-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="c78d1-109">تكوين البلدان المصدر والوجهة</span><span class="sxs-lookup"><span data-stu-id="c78d1-109">Configure source and destination countries</span></span>

<span data-ttu-id="c78d1-110">قبل إصدار شهادة لمنتج ما، يجب ربط المنتج بالبلد الوجهة الخاصة به وبلده الأصلي.</span><span class="sxs-lookup"><span data-stu-id="c78d1-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="c78d1-111">الانتقال إلى **إدارة معلومات المنتج \>إعداد \>توافق المنتجات \> بلد المنشأ \> قواعد بلد المنشأ**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="c78d1-112">حدد إعداد بلد موجود لتحريره، أو حدد **جديد** في جزء الإجراءات لإنشاء إعداد بلد جديد.</span><span class="sxs-lookup"><span data-stu-id="c78d1-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="c78d1-113">عيِّن القيم التالية للبلد المحدد أو البلد الجديد.</span><span class="sxs-lookup"><span data-stu-id="c78d1-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="c78d1-114">الحقل</span><span class="sxs-lookup"><span data-stu-id="c78d1-114">Field</span></span> | <span data-ttu-id="c78d1-115">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="c78d1-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="c78d1-116">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="c78d1-116">Item number</span></span> | <span data-ttu-id="c78d1-117">أدخل عدد أصناف المنتج.</span><span class="sxs-lookup"><span data-stu-id="c78d1-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="c78d1-118">بلد الوجهة</span><span class="sxs-lookup"><span data-stu-id="c78d1-118">Destination country</span></span> | <span data-ttu-id="c78d1-119">حدد البلد الذي تقوم بإرسال المنتج إليه.</span><span class="sxs-lookup"><span data-stu-id="c78d1-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="c78d1-120">بلد المنشأ</span><span class="sxs-lookup"><span data-stu-id="c78d1-120">Origin country</span></span> | <span data-ttu-id="c78d1-121">حدد البلد الذي تقوم بإرسال المنتج منه.</span><span class="sxs-lookup"><span data-stu-id="c78d1-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="c78d1-122">والغرض من هذا الإعداد هو مساعدتك في إنشاء تقرير شجره المواد (BOM) حيث يمكنك تضمين البلد الخاص بالأصل لكل جزء من الأجزاء التي يتم تحديد المصدر والوجهة لها.</span><span class="sxs-lookup"><span data-stu-id="c78d1-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="c78d1-123">يساعدك هذا التقرير في الحصول علي صوره شاملة للمكان الذي تأتي إليه الأجزاء والمكان التي سيتم نقلها إليه.</span><span class="sxs-lookup"><span data-stu-id="c78d1-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="c78d1-124">تتبع شهادات الموردين</span><span class="sxs-lookup"><span data-stu-id="c78d1-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="c78d1-125">يمكنك استخدام الصفحة **شهادات الموردين للبلد المنشأ** لتعقب الشهادات التي تصدرها إلى الموردين.</span><span class="sxs-lookup"><span data-stu-id="c78d1-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="c78d1-126">يجب تحديد مستندات الشهادة التي تقوم بإصدارها وكيف ستقوم بالإبلاغ عنها للعملاء.</span><span class="sxs-lookup"><span data-stu-id="c78d1-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="c78d1-127">تساعدك هذه الميزة في متابعة تعقب الشهادات.</span><span class="sxs-lookup"><span data-stu-id="c78d1-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="c78d1-128">كما تتيح لك إمكانية اختيار ما إذا كانت تظهر أرقام الشهادات ذات الصلة في الفواتير وكشوف التعبئة و/أو تأكيدات الأوامر.</span><span class="sxs-lookup"><span data-stu-id="c78d1-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="c78d1-129">لإعداد معلومات الشهادة‬، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="c78d1-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="c78d1-130">الانتقال إلى **إدارة معلومات المنتج \>إعداد \>توافق المنتجات \> بلد المنشأ \> شهادات الموردين لبلد المنشأ**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="c78d1-131">حدد إعداد شهادة موجودة لتحريره، أو حدد **جديد** في جزء الإجراءات لإنشاء شهادة جديدة.</span><span class="sxs-lookup"><span data-stu-id="c78d1-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="c78d1-132">عيِّن الإعدادات التالية للشهادة المحددة أو الجديدة.</span><span class="sxs-lookup"><span data-stu-id="c78d1-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="c78d1-133">الحقل</span><span class="sxs-lookup"><span data-stu-id="c78d1-133">Field</span></span> | <span data-ttu-id="c78d1-134">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="c78d1-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="c78d1-135">حساب المورد</span><span class="sxs-lookup"><span data-stu-id="c78d1-135">Vendor account</span></span> | <span data-ttu-id="c78d1-136">حدد المورد الذي قمت بإصدار الشهادة له.</span><span class="sxs-lookup"><span data-stu-id="c78d1-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="c78d1-137">رقم العنصر</span><span class="sxs-lookup"><span data-stu-id="c78d1-137">Item number</span></span> | <span data-ttu-id="c78d1-138">حدد البند الذي قمت بإصدار الشهادة له.</span><span class="sxs-lookup"><span data-stu-id="c78d1-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="c78d1-139">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="c78d1-139">Country/region</span></span> | <span data-ttu-id="c78d1-140">البلد أو المنطقة الوجهة التي يجب استخدام هذه الشهادة فيها.</span><span class="sxs-lookup"><span data-stu-id="c78d1-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="c78d1-141">رقم الشهادة</span><span class="sxs-lookup"><span data-stu-id="c78d1-141">Certificate number</span></span> | <span data-ttu-id="c78d1-142">أدخل رقم تعريف الشهادة الذي قمت بإصداره.</span><span class="sxs-lookup"><span data-stu-id="c78d1-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="c78d1-143">ساري المفعول</span><span class="sxs-lookup"><span data-stu-id="c78d1-143">Effective</span></span> | <span data-ttu-id="c78d1-144">حدد التاريخ الأول لصلاحية الشهادة الحالية.</span><span class="sxs-lookup"><span data-stu-id="c78d1-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="c78d1-145">انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="c78d1-145">Expiration</span></span> | <span data-ttu-id="c78d1-146">حدد التاريخ الأخير لصلاحية الشهادة الحالية.</span><span class="sxs-lookup"><span data-stu-id="c78d1-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="c78d1-147">الطباعة في فاتورة</span><span class="sxs-lookup"><span data-stu-id="c78d1-147">Print on invoice</span></span> | <span data-ttu-id="c78d1-148">حدد خانة الاختيار هذه لطباعة رقم الشهادة في الفواتير الموجهة إلى البلد المحدد أثناء نطاق التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="c78d1-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="c78d1-149">الطباعة في إيصال تعبئة</span><span class="sxs-lookup"><span data-stu-id="c78d1-149">Print on packing slip</span></span> | <span data-ttu-id="c78d1-150">حدد خانة الاختيار هذه لطباعة رقم الشهادة في إيصالات التعبئة الموجهة إلى البلد المحدد أثناء نطاق التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="c78d1-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="c78d1-151">الطباعة في أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="c78d1-151">Print on sales order</span></span> | <span data-ttu-id="c78d1-152">حدد خانة الاختيار هذه لطباعة رقم الشهادة في أوامر المبيعات الموجهة إلى البلد المحدد أثناء نطاق التاريخ المحدد.</span><span class="sxs-lookup"><span data-stu-id="c78d1-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="c78d1-153">تضمين بلد المنشأ في تقارير قائمة مكونات الصنف</span><span class="sxs-lookup"><span data-stu-id="c78d1-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="c78d1-154">عند إنشاء تقرير شجرة مواد، يمكنك تضمين بلد المنشأ لكل جزء من الأجزاء التي قمت بتحديدها وبلدان الوجهة والخاصة بها في الصفحة **قواعد بلد المنشأ**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="c78d1-155">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c78d1-156">حدد منتجًا أو قم بإنشائه لفتح صفحة **تفاصيل المنتج الصادر** له.</span><span class="sxs-lookup"><span data-stu-id="c78d1-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="c78d1-157">في جزء الإجراءات، في علامة تبويب **المهندس** في مجموعة **قائمة مكونات الصنف‏‎‬**، حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="c78d1-158">في صفحة القائمة التي تظهر، في جزء الإجراءات، حدد **قائمة مكونات الصنف \> طباعة**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="c78d1-159">في مربع الحوار **بنود قائمة مكونات الصنف**، قم بتعيين حقل **البلد الوجهة** إلى البلد الوجهة التي ترغب في عرضها في التقرير.</span><span class="sxs-lookup"><span data-stu-id="c78d1-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="c78d1-160">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c78d1-160">Select **OK**.</span></span>

<span data-ttu-id="c78d1-161">ويتم إنشاء تقرير يعرض معلومات حول بلد المنشأ لكل جزء ويتم إظهاره.</span><span class="sxs-lookup"><span data-stu-id="c78d1-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="c78d1-162">فيما يلي مثال التقرير.</span><span class="sxs-lookup"><span data-stu-id="c78d1-162">Here is an example of the report.</span></span>

<span data-ttu-id="c78d1-163">![تقرير بلد المنشأ](media/country-of-origin-report.png "تقرير بلد المنشأ")</span><span class="sxs-lookup"><span data-stu-id="c78d1-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
